# MG3
## Devlog
Xiangyi Li, she/her

1. float = 0, int = 0, bool = unchecked (false), string = empty
2. Unity calls it automatically, once every frame. My code never calls Update(), but Unity finds the exact method name and calls it by itself, the same way Start() runs once when the game begins.
3. KickWeapon holds a Timer in _lifeTimer. On kick, ActivateKick() calls _lifeTimer.BeginTimer(_lifetimeSeconds) to start a 0.2-second countdown. Two Updates cooperate: the Timer's Update() ticks time down each frame, and the KickWeapon's Update() checks _lifeTimer.IsFinished() each frame, calling gameObject.SetActive(false) when time is up.

## Open-Source Assets
- [Cat fighter spritesheet](https://opengameart.org/content/cat-fighter-sprite-sheet)
- [Food sprites](https://rcpstd.itch.io/pixel-food-pack)
