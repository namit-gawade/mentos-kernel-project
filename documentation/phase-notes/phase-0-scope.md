# Phase 0 — Scope and Project Control

## Selected Operating System

MentOS (Mentoring Operating System) is an educational operating-system project selected for this kernel modification mini project.

- Upstream repository: https://github.com/mentos-team/MentOS
- Project type: Educational operating system
- Development environment: Ubuntu 22.04 on WSL2
- Emulator: QEMU

## Project Objective

The objective is to make one focused, demonstrable modification to actual MentOS kernel source code.

The exact subsystem and modification will be selected after inspecting the source code, build configuration, and available tests. No feature will be claimed as newly implemented until the existing source has been checked.

## Team Members

- Namit Gawade
- Manav

Both members will document their contributions and explain their work in the final demonstration.

## Project Phases

1. Phase 0 — Scope, OS selection, and repository setup.
2. Phase 1 — Build and boot the original, unmodified kernel.
3. Phase 2 — Inspect the kernel and design the modification.
4. Phase 3 — Implement the kernel modification.
5. Phase 4 — Build, test, and verify the modified kernel.
6. Phase 5 — Organise screenshots, logs, and GitHub updates.
7. Phase 6 — Prepare the final PDF report.
8. Phase 7 — Record the demonstration video and complete submission.

## Baseline Rule

The original kernel must be built and booted before kernel source modifications begin. The original source revision and build evidence will be recorded.

## Evidence Checklist

- P0_01_Repository.png — project GitHub repository.
- P0_02_Upstream_Source.png — upstream MentOS repository.
- P0_03_Environment.png — Ubuntu and development tool versions.
- P0_04_Source_Revision.png — source branch and commit.
- P0_05_Source_Layout.png — source directory structure.
- P1_01_CMake_Configure.png — baseline configuration.
- P1_02_Build_Result.png — original kernel build.
- P1_03_Boot_Result.png — original kernel running in QEMU.

## Current Status

- [x] MentOS selected.
- [x] Project repository created.
- [x] Initial local folder structure created.
- [ ] Collaborator invitation accepted.
- [ ] Original kernel built.
- [ ] Original kernel booted.
- [ ] Kernel modification selected.
- [ ] Modification implemented and tested.
- [ ] Final report and video completed.

## Reproducibility

All commands, tool versions, source revisions, test results, obstacles, and fixes will be recorded. Failed or incomplete tests will not be reported as successful.
