# md-tst
<style>
.tst {
	font-family: serif;
	color: red;
}
</style>
<table>
<tr>
<td>Cell 1</td>
<td>Cell 2</td>
</tr>
<tr>
<td>Cell 3</td>
<td>Cell 4</td>
</tr>
</table>

## H2 <span class='tst'>Heading</span>

<a href='#h2'>### H3?</a>
<div id='content'></div>

<script>
let get = (filename)=> {
	let result = null;
	let xhr = new XMLHttpRequest();
	xhr.open('GET', filename, false);
	xhr.send();
	if (xhr.status == 200) {
		result = xhr.responseText;
	}
	return result;
}
let content = document.querySelector('#content');
let markdown = get('tst.md');
content.innerHTML = markdown;
</script>
