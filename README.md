# cycript_patched
Cycript 0.9.594 with fixed LC_LOAD_DYLIB command (for newer macOS versions).  
Injection still not working but can use LLDB instead and do:

```C
p ((void *(*)(int))dlsym((void*)dlopen("/path/to/cycript_0.9.594_patched/Cycript.lib/libcycript.dylib", 1), "CYListenServer"))(1337)
```
And then, in another shell:
```bash
cycript -r 127.0.0.1:1337
```
