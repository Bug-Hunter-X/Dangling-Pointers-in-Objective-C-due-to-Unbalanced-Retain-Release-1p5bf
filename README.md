# Dangling Pointers in Objective-C due to Unbalanced Retain/Release

This repository demonstrates a common error in Objective-C related to memory management, specifically an unbalanced `retain`/`release` cycle that leads to dangling pointers. The bug is illustrated in `bug.m`, while the corrected version is provided in `bugSolution.m`. Understanding this issue is crucial for writing stable and efficient Objective-C applications.

## Bug Description
The bug involves improper handling of object ownership leading to premature deallocation of objects. This happens when an object is released before its sub-objects which it retains. This situation creates dangling pointers, potentially causing crashes or undefined behavior.

## Solution
The solution involves correctly balancing the `retain`/`release` operations (or using ARC's automatic management effectively).  The `bugSolution.m` file demonstrates the correct handling of object ownership.