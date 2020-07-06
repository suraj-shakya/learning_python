# File Handling in Python
---
- Create
- Read
- Write
- Update
- Delete

**```open()``` function**
- Built-in function
- helps in opening a file for different modes
- returns the file object
- raises OS Error in case of failure
- commonly used with two arguments ```open(filename, mode)```



```python
help(open)
```

    Help on built-in function open in module io:
    
    open(file, mode='r', buffering=-1, encoding=None, errors=None, newline=None, closefd=True, opener=None)
        Open file and return a stream.  Raise OSError upon failure.
        
        file is either a text or byte string giving the name (and the path
        if the file isn't in the current working directory) of the file to
        be opened or an integer file descriptor of the file to be
        wrapped. (If a file descriptor is given, it is closed when the
        returned I/O object is closed, unless closefd is set to False.)
        
        mode is an optional string that specifies the mode in which the file
        is opened. It defaults to 'r' which means open for reading in text
        mode.  Other common values are 'w' for writing (truncating the file if
        it already exists), 'x' for creating and writing to a new file, and
        'a' for appending (which on some Unix systems, means that all writes
        append to the end of the file regardless of the current seek position).
        In text mode, if encoding is not specified the encoding used is platform
        dependent: locale.getpreferredencoding(False) is called to get the
        current locale encoding. (For reading and writing raw bytes use binary
        mode and leave encoding unspecified.) The available modes are:
        
        ========= ===============================================================
        Character Meaning
        --------- ---------------------------------------------------------------
        'r'       open for reading (default)
        'w'       open for writing, truncating the file first
        'x'       create a new file and open it for writing
        'a'       open for writing, appending to the end of the file if it exists
        'b'       binary mode
        't'       text mode (default)
        '+'       open a disk file for updating (reading and writing)
        'U'       universal newline mode (deprecated)
        ========= ===============================================================
        
        The default mode is 'rt' (open for reading text). For binary random
        access, the mode 'w+b' opens and truncates the file to 0 bytes, while
        'r+b' opens the file without truncation. The 'x' mode implies 'w' and
        raises an `FileExistsError` if the file already exists.
        
        Python distinguishes between files opened in binary and text modes,
        even when the underlying operating system doesn't. Files opened in
        binary mode (appending 'b' to the mode argument) return contents as
        bytes objects without any decoding. In text mode (the default, or when
        't' is appended to the mode argument), the contents of the file are
        returned as strings, the bytes having been first decoded using a
        platform-dependent encoding or using the specified encoding if given.
        
        'U' mode is deprecated and will raise an exception in future versions
        of Python.  It has no effect in Python 3.  Use newline to control
        universal newlines mode.
        
        buffering is an optional integer used to set the buffering policy.
        Pass 0 to switch buffering off (only allowed in binary mode), 1 to select
        line buffering (only usable in text mode), and an integer > 1 to indicate
        the size of a fixed-size chunk buffer.  When no buffering argument is
        given, the default buffering policy works as follows:
        
        * Binary files are buffered in fixed-size chunks; the size of the buffer
          is chosen using a heuristic trying to determine the underlying device's
          "block size" and falling back on `io.DEFAULT_BUFFER_SIZE`.
          On many systems, the buffer will typically be 4096 or 8192 bytes long.
        
        * "Interactive" text files (files for which isatty() returns True)
          use line buffering.  Other text files use the policy described above
          for binary files.
        
        encoding is the name of the encoding used to decode or encode the
        file. This should only be used in text mode. The default encoding is
        platform dependent, but any encoding supported by Python can be
        passed.  See the codecs module for the list of supported encodings.
        
        errors is an optional string that specifies how encoding errors are to
        be handled---this argument should not be used in binary mode. Pass
        'strict' to raise a ValueError exception if there is an encoding error
        (the default of None has the same effect), or pass 'ignore' to ignore
        errors. (Note that ignoring encoding errors can lead to data loss.)
        See the documentation for codecs.register or run 'help(codecs.Codec)'
        for a list of the permitted encoding error strings.
        
        newline controls how universal newlines works (it only applies to text
        mode). It can be None, '', '\n', '\r', and '\r\n'.  It works as
        follows:
        
        * On input, if newline is None, universal newlines mode is
          enabled. Lines in the input can end in '\n', '\r', or '\r\n', and
          these are translated into '\n' before being returned to the
          caller. If it is '', universal newline mode is enabled, but line
          endings are returned to the caller untranslated. If it has any of
          the other legal values, input lines are only terminated by the given
          string, and the line ending is returned to the caller untranslated.
        
        * On output, if newline is None, any '\n' characters written are
          translated to the system default line separator, os.linesep. If
          newline is '' or '\n', no translation takes place. If newline is any
          of the other legal values, any '\n' characters written are translated
          to the given string.
        
        If closefd is False, the underlying file descriptor will be kept open
        when the file is closed. This does not work when a file name is given
        and must be True in that case.
        
        A custom opener can be used by passing a callable as *opener*. The
        underlying file descriptor for the file object is then obtained by
        calling *opener* with (*file*, *flags*). *opener* must return an open
        file descriptor (passing os.open as *opener* results in functionality
        similar to passing None).
        
        open() returns a file object whose type depends on the mode, and
        through which the standard file operations such as reading and writing
        are performed. When open() is used to open a file in a text mode ('w',
        'r', 'wt', 'rt', etc.), it returns a TextIOWrapper. When used to open
        a file in a binary mode, the returned class varies: in read binary
        mode, it returns a BufferedReader; in write binary and append binary
        modes, it returns a BufferedWriter, and in read/write mode, it returns
        a BufferedRandom.
        
        It is also possible to use a string or bytearray as a file for both
        reading and writing. For strings StringIO can be used like a file
        opened in a text mode, and for bytes a BytesIO can be used like a file
        opened in a binary mode.
    
    


```python
# Create a file
# can use either "a", "x" or "w" as mode
# x will raise error if file already exists
# a and w will create the file if not exists
f = open("newFile.txt","w")
f.write("This is a new file...\nEach time the command runs: \nif the file not present \n\tIt will create \nelse\n\t truncates the content\n")
f.close()

```


```python
# Read a file

f = open("newFile.txt")
print(f.read())
f.close()
```

    This is a new file...
    Each time the command runs: 
    if the file not present 
    	It will create 
    else
    	 truncates the content
    
    


```python
help(f.read)
```

    Help on built-in function read:
    
    read(size=-1, /) method of _io.TextIOWrapper instance
        Read at most n characters from stream.
        
        Read from underlying buffer until we have n characters or we hit EOF.
        If n is negative or omitted, read until EOF.
    
    


```python
# reading few characters
f = open("newFile.txt")
print(f.read(10)) # reads first 10 characters
print(f.read(20)) # reads another 20 characters
f.close()
```

    This is a 
    new file...
    Each tim
    


```python
#reading line by line
f = open("newFile.txt")
print(f.readline()) 
print(f.readline()) 
f.close()
```

    This is a new file...
    
    Each time the command runs: 
    
    


```python
#read all the lines using loop
f = open("newFile.txt")
for line in f:
    print(line) 
f.close()
```

    This is a new file...
    
    Each time the command runs: 
    
    if the file not present 
    
    	It will create 
    
    else
    
    	 truncates the content
    
    

## Escape file.close() function

Use ```with``` keyword when dealing with the file objects. The advantage is that the file is properly closed after its suite finishes, even if an exception is raised at some point. Using ```with``` is also much shorter than writing equivalent ```try-finally``` blocks.


```python
with open("newFile.txt") as f:
    print(f.read())
    
f.closed # check if the file has been automatically closed
```

    This is a new file...
    Each time the command runs: 
    if the file not present 
    	It will create 
    else
    	 truncates the content
    
    




    True



## Updating a file
---
- modes : 
    - "a" : **Append**, adds the new content to the end of the file
    - "w" : **Write**, overwrites the existing content by new content


```python
with open("newFile.txt","a") as f:
    f.write("New Content Alert!!!")

# since we cannot read in the append mode
with open("newFile.txt") as f:
    print(f.read())

```

    This is a new file...
    Each time the command runs: 
    if the file not present 
    	It will create 
    else
    	 truncates the content
    New Content Alert!!!
    

# Delete a file  
To delete a file, ```import``` the ```OS``` module, and run ```os.remove()``` function


```python
import os
dir(os)
```




    ['DirEntry',
     'F_OK',
     'MutableMapping',
     'O_APPEND',
     'O_BINARY',
     'O_CREAT',
     'O_EXCL',
     'O_NOINHERIT',
     'O_RANDOM',
     'O_RDONLY',
     'O_RDWR',
     'O_SEQUENTIAL',
     'O_SHORT_LIVED',
     'O_TEMPORARY',
     'O_TEXT',
     'O_TRUNC',
     'O_WRONLY',
     'P_DETACH',
     'P_NOWAIT',
     'P_NOWAITO',
     'P_OVERLAY',
     'P_WAIT',
     'PathLike',
     'R_OK',
     'SEEK_CUR',
     'SEEK_END',
     'SEEK_SET',
     'TMP_MAX',
     'W_OK',
     'X_OK',
     '_AddedDllDirectory',
     '_Environ',
     '__all__',
     '__builtins__',
     '__cached__',
     '__doc__',
     '__file__',
     '__loader__',
     '__name__',
     '__package__',
     '__spec__',
     '_check_methods',
     '_execvpe',
     '_exists',
     '_exit',
     '_fspath',
     '_get_exports_list',
     '_putenv',
     '_unsetenv',
     '_wrap_close',
     'abc',
     'abort',
     'access',
     'add_dll_directory',
     'altsep',
     'chdir',
     'chmod',
     'close',
     'closerange',
     'cpu_count',
     'curdir',
     'defpath',
     'device_encoding',
     'devnull',
     'dup',
     'dup2',
     'environ',
     'error',
     'execl',
     'execle',
     'execlp',
     'execlpe',
     'execv',
     'execve',
     'execvp',
     'execvpe',
     'extsep',
     'fdopen',
     'fsdecode',
     'fsencode',
     'fspath',
     'fstat',
     'fsync',
     'ftruncate',
     'get_exec_path',
     'get_handle_inheritable',
     'get_inheritable',
     'get_terminal_size',
     'getcwd',
     'getcwdb',
     'getenv',
     'getlogin',
     'getpid',
     'getppid',
     'isatty',
     'kill',
     'linesep',
     'link',
     'listdir',
     'lseek',
     'lstat',
     'makedirs',
     'mkdir',
     'name',
     'open',
     'pardir',
     'path',
     'pathsep',
     'pipe',
     'popen',
     'putenv',
     'read',
     'readlink',
     'remove',
     'removedirs',
     'rename',
     'renames',
     'replace',
     'rmdir',
     'scandir',
     'sep',
     'set_handle_inheritable',
     'set_inheritable',
     'spawnl',
     'spawnle',
     'spawnv',
     'spawnve',
     'st',
     'startfile',
     'stat',
     'stat_result',
     'statvfs_result',
     'strerror',
     'supports_bytes_environ',
     'supports_dir_fd',
     'supports_effective_ids',
     'supports_fd',
     'supports_follow_symlinks',
     'symlink',
     'sys',
     'system',
     'terminal_size',
     'times',
     'times_result',
     'truncate',
     'umask',
     'uname_result',
     'unlink',
     'urandom',
     'utime',
     'waitpid',
     'walk',
     'write']




```python
filename = "newFile.txt"
if os.path.exists(filename):
    os.remove(filename)
    print("File: {file} removed successfully.".format(file=filename))
else:
    print("File: {file} does not exists".format(file=filename))

```

    File: newFile.txt does not exists
    
