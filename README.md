# MPIR Binary on Windows

This project include MPIR 3.0.0 `win32|x64` `Debug|Release` `LIB|DLL` binary which is built by Visual C++ 15.

## License

See [README.MPIR](./README.MPIR)

## Usage

### Dynamic Link:

1. Import 'dll/XX/XX/mpir.lib'
2. Import 'lib/XX/XX/XX/mpirxx.lib' (if use "gmpxx.h" or "mpirxx.h").
3. Use 'mpir.dll' while running.

### Static Link:

1. Import 'lib/XX/XX/XX/mpir.lib'
2. Import 'lib/XX/XX/XX/mpirxx.lib' (if use "gmpxx.h" or "mpirxx.h").

## The way to configure

1. cd 'build.vc15'

2. call msbuild

```
call msbuild gc DLL Win32 Debug
call msbuild gc DLL Win32 Release
call msbuild gc DLL x64 Debug
call msbuild gc DLL x64 Release
call msbuild gc LIB Win32 Debug
call msbuild gc LIB Win32 Release
call msbuild gc LIB x64 Debug
call msbuild gc LIB x64 Release
call msbuild cxx LIB Win32 Debug
call msbuild cxx LIB Win32 Release
call msbuild cxx LIB x64 Debug
call msbuild cxx LIB x64 Release
```

note:

1. This Binary include mpirxx with /MT & /MD in 'lib'.

2. There is a bug in yasm 1.3.0, use old version or rebuid it from newest in GitHub.

3. Configure in VS, you can use variables to import .lib file, like this : `MPIR-Binary\lib\MD\$(Platform)\$(Configuration)\mpir.lib`.
