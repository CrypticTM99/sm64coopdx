# Documentation TODO, I'll write more to this later, just moving it over from my test build.

Small, focused tasks for improving the docs and filling in the missing guides.
Nothing major here, just looking to work on this slowly towards a potential PR.

## High priority stuff

- [ ] **First Lua Mod guide**  
  I'll write a short beginner walkthrough: create a `main.lua`, drop it in the mods folder, hook `HOOK_MARIO_UPDATE`, change something simple like gravity or swim speed, and run with `--console`.  
  Link the existing small examples at the end so people know where to go next. (May use the examples I already made for API Learning mod DX)
  Right now the tips + examples assume too much for someone opening the docs for the first time.

- [ ] **Networking & sync tables guide**  
  Clear, short explanation of:
  - localIndex vs globalIndex
  - how `gPlayerSyncTable` works and why it auto-translates
  - when to use `network_send` / `network_send_to` vs object networking
  - basic host-only vs “everyone runs it” patterns  
  Pair it with the existing bytestring packet example.

- [ ] **Mod Menu & basic DJUI**  
  How to use the `hook_mod_menu_*` functions and simple HUD drawing.  
  Most people currently just dig through other mods to figure this out.

## Medium priority

- [ ] **Custom behaviors & object lists**  
  Expand the existing object-lists page (or make a sibling guide) into a practical “how to safely replace or extend a behavior” walkthrough.  
  Cover `hook_behavior`, the replaceBehavior flag, init vs loop, and `network_init_object`.

- [ ] **Surfaces & collision**  
  Short written guide that ties together the runtime surface examples.  
  Raycasts, custom collision, common gotchas.

- [ ] **Audio & sequences**  
  How to play custom sounds, override sequences, and the relevant hooks (`HOOK_ON_PLAY_SOUND`, `HOOK_ON_SEQ_LOAD`).  
  Currently this info is mostly buried in the giant functions list.

## Lower priority / polish

- [ ] **C contribution starter**  
  The C docs are basically just naming conventions.  
  A one-page “add a simple C function and expose it to Lua” would help a lot.

- [ ] **Common pitfalls**  
  Short troubleshooting list:  
  why a hook isn’t firing, sync table not updating for others, console not showing prints, mod not loading, etc.

- [ ] **Wiki home page**  
  The wiki currently just repeats the README.  
  Turn it into a clean index that points to the docs and the new guides.

---

I'll fix this up and add to it as I continue to go through the recent docs and anything I may have missed while studying other contributors PRs. 
Don't want this to come across as buggy or invalid or overall messy to read, so I'll make sure its PR ready prior to sending in coop resources
