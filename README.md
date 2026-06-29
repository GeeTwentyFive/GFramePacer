Cross-platform single-header-only frame pacer which sets up process in OS scheduler for smooth frame pacing, minimizes context switching and disk swapping, and provides precise frame delta times

# Usage
```c++
GFramePacer gfp;
gfp.target_frametime_ms = 2.0;  // (2.0 = 500 FPS)
for (;;) {
        double delta_time = gfp.Wait();

        // ...
}
```