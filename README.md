<div align="center">

## Dual Scrollbars in IE When using IFrames


</div>

### Description

Anyone who has used IFRAMES in IE may have noticed several problems with them. One big one, is that if you were to include an iframe that extends to the side of your parent page, and the iframe has a scroll bar, then both the iframe and the parent would have a scroll bar. Very confusing. This script resizes the iframe so that it doesn't have a scroll bar. Problem solved...
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Josh C](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/josh-c.md)
**Level**          |Intermediate
**User Rating**    |3.7 (11 globes from 3 users)
**Compatibility**  |
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__2-57.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/josh-c-dual-scrollbars-in-ie-when-using-iframes__2-2195/archive/master.zip)





### Source Code

```
stick this on your page....
<script language="javascript">
function checkiFrame() {
  if ((document.all('imain').readyState=="complete")) {
		if (document.frames('imain',0).document.body.scrollHeight > 500) {
		document.all('imain').style.height = document.frames('imain',0).document.body.scrollHeight;
		}else{
		document.all('imain').style.height = 500
		}
	}
}
</script>
it's fired by this in your iframe...
<iframe.... onreadystatechange="checkiFrame()">
```

