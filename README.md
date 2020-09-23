<div align="center">

## ^\! write your own copy command to copy files


</div>

### Description

just like DOS Copy command
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[my name  is Nitin Jindal \(from Panchkula,Haryana\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/my-name-is-nitin-jindal-from-panchkula-haryana.md)
**Level**          |Intermediate
**User Rating**    |3.6 (32 globes from 9 users)
**Compatibility**  |C, C\+\+ \(general\)
**Category**       |[System Services/ Functions](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/system-services-functions__3-23.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/my-name-is-nitin-jindal-from-panchkula-haryana-write-your-own-copy-command-to-copy-files__3-7577/archive/master.zip)





### Source Code

```
/******** Now you can write your own copy command to copy.exe or .com or any large file................. Please Vote for me.....Nitin Jindal............*/
#include <stdio.h>
#include <io.h>
#include <fcntl.h>
#include <sys\stat.h>
void fcopy(char *,char *);
main()
{
fcopy("fcopy.exe","fcopy2.exe");
/* fcopy("a:\\fcopy.exe","C:\\test.exe");
 this will copy fcopy.exe file from floppy disk to harddisk */
return 0;
}
void fcopy(char *sname,char *tname)
{
void *buffer;
int bytes,inhandle,outhandle;
inhandle=open(sname,O_RDONLY|O_BINARY);
outhandle=open(tname,O_CREAT|O_BINARY|O_WRONLY|S_IWRITE);
while(1)
{
bytes=read(inhandle,buffer,512);
if(bytes>0)
write(outhandle,buffer,bytes);
else
break;
}
close(inhandle);
close(outhandle);
}
```

