# ⚙️ `Task_Type`

Here you will find a full description of `Task_Type`.

## 👓 Overview

In order to allow the entire system to perform multi-threaded operations, Xila uses `Task_Type`. These execute functions 
These are functions that are executed in parallel to each others. Currently, Xila rely on the FreeRTOS scheduler to manage tasks and `Task_Class` is mainly a class wrapper of `vTaskHandle`. This wrapper also provide additional feature and insights / metrics on tasks.

When a task is run, it is given a priority. The scheduler will then run the task with the highest priority that is ready to run. You have to let the scheduler run by calling `Task_Type::Delay` or `Task_Type::Delay_Until` in order to allow other tasks to run. If you don't do that within a certain amount of time (5 seconds by default), the task will be frozen by the watchdog.

:::{note}
By default, each software has a main task created when the software is loaded. If you want to perform multi-threaded operations, you will have to create a second task, using `Task_Type::Create` or `Task_Type(...)` (not the default constructor).
:::

## 💡 Example

```cpp
    using namespace Xila;

    class My_Software : public Software_Class
    {
        // ...
        
        static void My_Task_Start_Function(void*);  // Must be static.
        void My_Task_Function();

        Task_Type My_Task;    // Create a second task.
    };

    static class My_Software_Handle : public Software_Handle_Class
    {
        // ...
    };

    void My_Software::My_Software()
    {
        My_Task.Create(this, My_Task_Start_Function, "My Task", 4 * 1024, this); // Create a second task.
    }

    void My_Software::My_Task_Start(void* Instance)
    {
        (My_Software*)Instance->My_Task_Function(); // This is the easiest way to allow access to the instance.
    }

    void My_Software::My_Task_Function()
    {
        while (true)    // Endless loop because task must never return.
        {
            // Do stuff.

            Task.Delay(50);   // Don't forget to add delay to reset watchdog and allow other tasks to run.
        }
    }
```

## 📚 API reference

```{eval-rst}
.. doxygentypedef:: Xila_Namespace::Task_Type

.. doxygenclass:: Xila_Namespace::Task_Class
    :members:
```