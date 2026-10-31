# MentOS Kernel Modification Project

A small educational operating-system kernel project focused on understanding and modifying kernel-level behaviour.

## Project status
Completed. We will first establish a reproducible, unmodified MentOS build and boot baseline. The exact kernel change will be selected after inspecting the source and available tests.

## Team
- Namit Gawade
- Manav

## Repository structure
- documentation/ — project plan and report
- evidence/ — screenshots and logs
- video/ — demonstration planning and final video link

## Upstream project
https://github.com/mentos-team/MentOS

---

## Priority Scheduler Implementation

The Kernel Pair implemented a functional priority-based task-selection algorithm in MentOS.

### Key Changes

- Selects the runnable task with the highest priority (lowest numerical priority value).
- Skips blocked or otherwise non-runnable tasks.
- Supports skipping periodic tasks when requested.
- Rotates selection among equal-priority runnable tasks.
- Returns no task when no eligible runnable task exists.

### Implementation Files

The modified source files and related documentation are available in:

- `implementation/kernel/src/process/scheduler_algorithm.c`
- `implementation/kernel/src/tests/unit/test_scheduler.c`
- `implementation/lib/inc/sched.h`
- `documentation/implementation/priority-scheduler.md`

### Build and Test Results

| Validation | Result |
|---|---:|
| Kernel unit-test suites | 17/17 passed |
| Failed kernel assertions | 0 |
| Userspace tests | 90/90 passed |
| QEMU test execution | Successful |

### Evidence

Screenshots documenting implementation and testing are available in:

- `evidence/phase-0/`
- `evidence/phase-1/`
- `evidence/phase-2-4/`

## Team

**The Kernel Pair**

- Namit Gawade
- Manav Kumar

### Evidence

Screenshots documenting implementation and testing are available in:

- `evidence/phase-0/`
- `evidence/phase-1/`
- `evidence/phase-2-4/`

### Team

**The Kernel Pair**

- Namit Gawade
- Manav Kumar
