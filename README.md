<div align="center">

## String Replacement \(str\_replace\)


</div>

### Description

This gives you the ability to use str_replace in C. str_replace is a very powerful function with many applications.
 
### More Info
 
First parameter is string to replace.

Second parameter is what to replace with.

Third parameter is the string to do it in.

Returns the new string with all occurences of first parameter replaced with second parameter.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Brian Folts](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/brian-folts.md)
**Level**          |Advanced
**User Rating**    |2.8 (14 globes from 5 users)
**Compatibility**  |C
**Category**       |[Strings](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/strings__3-26.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/brian-folts-string-replacement-str-replace__3-10890/archive/master.zip)

### API Declarations

```
#include &lt;stdlib.h&gt;
#include &lt;string.h&gt;
#include &lt;stdio.h&gt;
```


### Source Code

```
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
//replaces all occurences with another occurence
char *str_replace(char * t1, char * t2, char * t6){
	char*t4;
	char*t5=malloc(0);
	while(strstr(t6,t1)){
		t4=strstr(t6,t1);
		strncpy(t5+strlen(t5),t6,t4-t6);
		strcat(t5,t2);
		t4+=strlen(t1);
		t6=t4;
	}
	return strcat(t5,t4);
}
int main(){
	printf("%s",str_replace("hello","goodbye","hello worldhello hello hello helloworld hello hello hello hello hellohello worldhello hello hello helloworld hello hello hello hello hellohello worldhello hello hello helloworld hello hello hello hello hello,and then it gets to the new line?\n"));
	return 0;
}
```

