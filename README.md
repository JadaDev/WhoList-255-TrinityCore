# TrinityCore /Who 1-255 Allowance Modification

This modification is intended for TrinityCore. It allows you to disable the level check for certain situations by simply commenting out a few lines of code in the `MiscHandler.cpp` file.

## Before Modification

In the original code, there is a level check that verifies if a target's level is within a specified level range. If the target's level falls outside of this range, the code continues without processing further.

```cpp
// check if target's level is in level range
uint8 lvl = target.GetLevel();
if (lvl < level_min || lvl > level_max)
    continue;
```
## After Modification

With this modification, you can disable the level check by commenting out the relevant lines of code. This can be useful if you want to allow actions to proceed regardless of the target's level.

```cpp
// check if target's level is in level range
uint8 lvl = target.GetLevel();
/*if (lvl < level_min || lvl > level_max)
    continue;*/
```
Remember that you could alternatively change the level check condition to `lvl >= 256` if that better suits your needs.

**File Location**: `src\server\game\Handlers\MiscHandler.cpp`

Please make sure to test this modification thoroughly in your TrinityCore environment to ensure it meets your requirements.
