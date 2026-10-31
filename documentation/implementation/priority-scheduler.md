# Priority Scheduler Implementation

## Project
**Modifying a Small OS Kernel — MentOS**

**Team:** The Kernel Pair  
**Members:** Namit Gawade and Manav Kumar

## Objective

Implement priority-based task selection in MentOS by replacing the placeholder priority scheduling algorithm with a functional implementation.

## Implementation

The priority scheduler examines the runqueue and selects an eligible runnable task with the highest scheduling priority (the lowest numerical priority value).

The implementation:
- Ignores tasks that are not in the `TASK_RUNNING` state.
- Supports skipping periodic tasks when requested.
- Selects the task with the lowest numerical priority value.
- Rotates selection among equal-priority runnable tasks to avoid repeatedly favoring the same queue entry.
- Returns `NULL` when no eligible runnable task exists.

The existing scheduler dispatch mechanism is retained.

## Source Files

The implementation and related configuration changes are provided in:

- `implementation/kernel/src/process/scheduler_algorithm.c`
- `implementation/kernel/src/tests/unit/test_scheduler.c`
- `implementation/lib/inc/sched.h`

## Unit Tests

Priority-scheduler tests cover:
- Selection of the highest-priority runnable task.
- Equal-priority selection order.
- Skipping blocked tasks.
- Handling an empty runqueue.

## Build and Test Environment

- Operating system: Ubuntu 22.04 on WSL2
- Compiler: GCC 11.4.0
- Build system: CMake 3.22.1
- Emulator: QEMU 6.2.0
- Kernel configuration: `SCHEDULER_PRIORITY`
- Realtime scheduler feedback: disabled

## Test Results

| Test suite | Result |
|---|---:|
| Kernel unit-test suites | 17/17 passed |
| Failed kernel assertions | 0 |
| Userspace tests | 90/90 passed |
| Source whitespace validation (`git diff --check`) | Passed |

The kernel unit tests completed successfully under QEMU. The userspace test suite also completed with zero failures.

## Conclusion

The placeholder priority scheduler was replaced with a functional priority-based task-selection implementation. The modified kernel built successfully, and both the kernel unit-test suites and userspace test suite passed.
