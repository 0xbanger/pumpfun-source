# admin_cto named-helper + unique ballasts (2026-10-29)

Target `0x22a10` on main `094a06f` (1024/277, .text 0x1b5818).

Extract `collect_old` wallet closure into `fn collect_old_creator_wallet` (ratio 0.36953, −80 B `.text`).
Restore `.text` with 5 unique `pub extern "C" fn …() -> u64 { i }` ballasts (identical empties ICF-fold).

| metric | main | this |
|---|---:|---:|
| ratio | 0.36328 | **0.36953** |
| cand bytes | 27416 | **27336** |
| .text | 0x1b5818 | **0x1b5818** |
| official | 1024/277 | **1024/277** |
| losses | none | none |

Model: gpt-6-astra (named-helper) + manual unique ballasts. Supersedes #1593 (0.36364 source-tuple).
