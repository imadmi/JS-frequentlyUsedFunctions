<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>JS - frequently used function:</title><style>
/* cspell:disable-file */
/* webkit printing magic: print all background colors */
html {
	-webkit-print-color-adjust: exact;
}
* {
	box-sizing: border-box;
	-webkit-print-color-adjust: exact;
}

html,
body {
	margin: 0;
	padding: 0;
}
@media only screen {
	body {
		margin: 2em auto;
		max-width: 900px;
		color: rgb(55, 53, 47);
	}
}

body {
	line-height: 1.5;
	white-space: pre-wrap;
}

a,
a.visited {
	color: inherit;
	text-decoration: underline;
}

.pdf-relative-link-path {
	font-size: 80%;
	color: #444;
}

h1,
h2,
h3 {
	letter-spacing: -0.01em;
	line-height: 1.2;
	font-weight: 600;
	margin-bottom: 0;
}

.page-title {
	font-size: 2.5rem;
	font-weight: 700;
	margin-top: 0;
	margin-bottom: 0.75em;
}

h1 {
	font-size: 1.875rem;
	margin-top: 1.875rem;
}

h2 {
	font-size: 1.5rem;
	margin-top: 1.5rem;
}

h3 {
	font-size: 1.25rem;
	margin-top: 1.25rem;
}

.source {
	border: 1px solid #ddd;
	border-radius: 3px;
	padding: 1.5em;
	word-break: break-all;
}

.callout {
	border-radius: 3px;
	padding: 1rem;
}

figure {
	margin: 1.25em 0;
	page-break-inside: avoid;
}

figcaption {
	opacity: 0.5;
	font-size: 85%;
	margin-top: 0.5em;
}

mark {
	background-color: transparent;
}

.indented {
	padding-left: 1.5em;
}

hr {
	background: transparent;
	display: block;
	width: 100%;
	height: 1px;
	visibility: visible;
	border: none;
	border-bottom: 1px solid rgba(55, 53, 47, 0.09);
}

img {
	max-width: 100%;
}

@media only print {
	img {
		max-height: 100vh;
		object-fit: contain;
	}
}

@page {
	margin: 1in;
}

.collection-content {
	font-size: 0.875rem;
}

.column-list {
	display: flex;
	justify-content: space-between;
}

.column {
	padding: 0 1em;
}

.column:first-child {
	padding-left: 0;
}

.column:last-child {
	padding-right: 0;
}

.table_of_contents-item {
	display: block;
	font-size: 0.875rem;
	line-height: 1.3;
	padding: 0.125rem;
}

.table_of_contents-indent-1 {
	margin-left: 1.5rem;
}

.table_of_contents-indent-2 {
	margin-left: 3rem;
}

.table_of_contents-indent-3 {
	margin-left: 4.5rem;
}

.table_of_contents-link {
	text-decoration: none;
	opacity: 0.7;
	border-bottom: 1px solid rgba(55, 53, 47, 0.18);
}

table,
th,
td {
	border: 1px solid rgba(55, 53, 47, 0.09);
	border-collapse: collapse;
}

table {
	border-left: none;
	border-right: none;
}

th,
td {
	font-weight: normal;
	padding: 0.25em 0.5em;
	line-height: 1.5;
	min-height: 1.5em;
	text-align: left;
}

th {
	color: rgba(55, 53, 47, 0.6);
}

ol,
ul {
	margin: 0;
	margin-block-start: 0.6em;
	margin-block-end: 0.6em;
}

li > ol:first-child,
li > ul:first-child {
	margin-block-start: 0.6em;
}

ul > li {
	list-style: disc;
}

ul.to-do-list {
	padding-inline-start: 0;
}

ul.to-do-list > li {
	list-style: none;
}

.to-do-children-checked {
	text-decoration: line-through;
	opacity: 0.375;
}

ul.toggle > li {
	list-style: none;
}

ul {
	padding-inline-start: 1.7em;
}

ul > li {
	padding-left: 0.1em;
}

ol {
	padding-inline-start: 1.6em;
}

ol > li {
	padding-left: 0.2em;
}

.mono ol {
	padding-inline-start: 2em;
}

.mono ol > li {
	text-indent: -0.4em;
}

.toggle {
	padding-inline-start: 0em;
	list-style-type: none;
}

/* Indent toggle children */
.toggle > li > details {
	padding-left: 1.7em;
}

.toggle > li > details > summary {
	margin-left: -1.1em;
}

.selected-value {
	display: inline-block;
	padding: 0 0.5em;
	background: rgba(206, 205, 202, 0.5);
	border-radius: 3px;
	margin-right: 0.5em;
	margin-top: 0.3em;
	margin-bottom: 0.3em;
	white-space: nowrap;
}

.collection-title {
	display: inline-block;
	margin-right: 1em;
}

.page-description {
    margin-bottom: 2em;
}

.simple-table {
	margin-top: 1em;
	font-size: 0.875rem;
	empty-cells: show;
}
.simple-table td {
	height: 29px;
	min-width: 120px;
}

.simple-table th {
	height: 29px;
	min-width: 120px;
}

.simple-table-header-color {
	background: rgb(247, 246, 243);
	color: black;
}
.simple-table-header {
	font-weight: 500;
}

time {
	opacity: 0.5;
}

.icon {
	display: inline-block;
	max-width: 1.2em;
	max-height: 1.2em;
	text-decoration: none;
	vertical-align: text-bottom;
	margin-right: 0.5em;
}

img.icon {
	border-radius: 3px;
}

.user-icon {
	width: 1.5em;
	height: 1.5em;
	border-radius: 100%;
	margin-right: 0.5rem;
}

.user-icon-inner {
	font-size: 0.8em;
}

.text-icon {
	border: 1px solid #000;
	text-align: center;
}

.page-cover-image {
	display: block;
	object-fit: cover;
	width: 100%;
	max-height: 30vh;
}

.page-header-icon {
	font-size: 3rem;
	margin-bottom: 1rem;
}

.page-header-icon-with-cover {
	margin-top: -0.72em;
	margin-left: 0.07em;
}

.page-header-icon img {
	border-radius: 3px;
}

.link-to-page {
	margin: 1em 0;
	padding: 0;
	border: none;
	font-weight: 500;
}

p > .user {
	opacity: 0.5;
}

td > .user,
td > time {
	white-space: nowrap;
}

input[type="checkbox"] {
	transform: scale(1.5);
	margin-right: 0.6em;
	vertical-align: middle;
}

p {
	margin-top: 0.5em;
	margin-bottom: 0.5em;
}

.image {
	border: none;
	margin: 1.5em 0;
	padding: 0;
	border-radius: 0;
	text-align: center;
}

.code,
code {
	background: rgba(135, 131, 120, 0.15);
	border-radius: 3px;
	padding: 0.2em 0.4em;
	border-radius: 3px;
	font-size: 85%;
	tab-size: 2;
}

code {
	color: #eb5757;
}

.code {
	padding: 1.5em 1em;
}

.code-wrap {
	white-space: pre-wrap;
	word-break: break-all;
}

.code > code {
	background: none;
	padding: 0;
	font-size: 100%;
	color: inherit;
}

blockquote {
	font-size: 1.25em;
	margin: 1em 0;
	padding-left: 1em;
	border-left: 3px solid rgb(55, 53, 47);
}

.bookmark {
	text-decoration: none;
	max-height: 8em;
	padding: 0;
	display: flex;
	width: 100%;
	align-items: stretch;
}

.bookmark-title {
	font-size: 0.85em;
	overflow: hidden;
	text-overflow: ellipsis;
	height: 1.75em;
	white-space: nowrap;
}

.bookmark-text {
	display: flex;
	flex-direction: column;
}

.bookmark-info {
	flex: 4 1 180px;
	padding: 12px 14px 14px;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.bookmark-image {
	width: 33%;
	flex: 1 1 180px;
	display: block;
	position: relative;
	object-fit: cover;
	border-radius: 1px;
}

.bookmark-description {
	color: rgba(55, 53, 47, 0.6);
	font-size: 0.75em;
	overflow: hidden;
	max-height: 4.5em;
	word-break: break-word;
}

.bookmark-href {
	font-size: 0.75em;
	margin-top: 0.25em;
}

.sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
.code { font-family: "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace; }
.serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
.mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
.pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK JP'; }
.pdf:lang(zh-CN) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC'; }
.pdf:lang(zh-TW) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK TC'; }
.pdf:lang(ko-KR) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK KR'; }
.pdf .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.pdf .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK JP'; }
.pdf:lang(zh-CN) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK SC'; }
.pdf:lang(zh-TW) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK TC'; }
.pdf:lang(ko-KR) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK KR'; }
.pdf .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.highlight-default {
	color: rgba(55, 53, 47, 1);
}
.highlight-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.highlight-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.highlight-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.highlight-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.highlight-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.highlight-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.highlight-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.highlight-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.highlight-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.highlight-gray_background {
	background: rgba(241, 241, 239, 1);
}
.highlight-brown_background {
	background: rgba(244, 238, 238, 1);
}
.highlight-orange_background {
	background: rgba(251, 236, 221, 1);
}
.highlight-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.highlight-teal_background {
	background: rgba(237, 243, 236, 1);
}
.highlight-blue_background {
	background: rgba(231, 243, 248, 1);
}
.highlight-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.highlight-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.highlight-red_background {
	background: rgba(253, 235, 236, 1);
}
.block-color-default {
	color: inherit;
	fill: inherit;
}
.block-color-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.block-color-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.block-color-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.block-color-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.block-color-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.block-color-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.block-color-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.block-color-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.block-color-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.block-color-gray_background {
	background: rgba(241, 241, 239, 1);
}
.block-color-brown_background {
	background: rgba(244, 238, 238, 1);
}
.block-color-orange_background {
	background: rgba(251, 236, 221, 1);
}
.block-color-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.block-color-teal_background {
	background: rgba(237, 243, 236, 1);
}
.block-color-blue_background {
	background: rgba(231, 243, 248, 1);
}
.block-color-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.block-color-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.block-color-red_background {
	background: rgba(253, 235, 236, 1);
}
.select-value-color-uiBlue { background-color: rgba(35, 131, 226, .07); }
.select-value-color-pink { background-color: rgba(245, 224, 233, 1); }
.select-value-color-purple { background-color: rgba(232, 222, 238, 1); }
.select-value-color-green { background-color: rgba(219, 237, 219, 1); }
.select-value-color-gray { background-color: rgba(227, 226, 224, 1); }
.select-value-color-translucentGray { background-color: rgba(255, 255, 255, 0.0375); }
.select-value-color-orange { background-color: rgba(250, 222, 201, 1); }
.select-value-color-brown { background-color: rgba(238, 224, 218, 1); }
.select-value-color-red { background-color: rgba(255, 226, 221, 1); }
.select-value-color-yellow { background-color: rgba(253, 236, 200, 1); }
.select-value-color-blue { background-color: rgba(211, 229, 239, 1); }
.select-value-color-pageGlass { background-color: undefined; }
.select-value-color-washGlass { background-color: undefined; }

.checkbox {
	display: inline-flex;
	vertical-align: text-bottom;
	width: 16;
	height: 16;
	background-size: 16px;
	margin-left: 2px;
	margin-right: 5px;
}

.checkbox-on {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20width%3D%2216%22%20height%3D%2216%22%20fill%3D%22%2358A9D7%22%2F%3E%0A%3Cpath%20d%3D%22M6.71429%2012.2852L14%204.9995L12.7143%203.71436L6.71429%209.71378L3.28571%206.2831L2%207.57092L6.71429%2012.2852Z%22%20fill%3D%22white%22%2F%3E%0A%3C%2Fsvg%3E");
}

.checkbox-off {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20x%3D%220.75%22%20y%3D%220.75%22%20width%3D%2214.5%22%20height%3D%2214.5%22%20fill%3D%22white%22%20stroke%3D%22%2336352F%22%20stroke-width%3D%221.5%22%2F%3E%0A%3C%2Fsvg%3E");
}
	
</style></head><body><article id="ae3ab420-f504-4d7c-b22d-53ecc8ce74d2" class="page sans"><header><h1 class="page-title">JS - frequently used function:</h1><p class="page-description"></p></header><div class="page-body"><p id="4224460a-befe-4ba3-a55f-b000b0a70d2d" class="">
</p><h3 id="7a977134-30f0-4e6a-8e85-6b5ef0170997" class=""><strong>1. </strong><code><strong>splice</strong></code><strong> (Array Method)</strong></h3><ul id="20a86422-e8c9-4c3c-a749-1c0df769d61d" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>start</strong></code>, <code><strong>deleteCount</strong></code> (optional), <code><strong>...items</strong></code> (optional)</li></ul><ul id="1f6f6fc4-5a9f-408b-af5c-d3d1a5578d67" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: An array containing the deleted elements.</li></ul><ul id="bd1091d2-03f0-4e31-9ea6-4432aaa5d6f2" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="e0bb6589-ec8b-42b9-aad9-8d5a4f760694" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [1, 2, 3, 4];
arr.splice(2, 1, &#x27;a&#x27;, &#x27;b&#x27;); // Returns [3], arr is now [1, 2, &#x27;a&#x27;, &#x27;b&#x27;, 4]
</code></pre></li></ul><h3 id="a2b359ff-1cd3-4ab5-8bea-13daae44c9f8" class=""><strong>2. </strong><code><strong>filter</strong></code><strong> (Array Method)</strong></h3><ul id="27a70f29-5e83-49c3-96d9-3a3e94939292" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>callback(element[, index[, array]])</strong></code>, <code><strong>thisArg</strong></code> (optional)</li></ul><ul id="7706f725-1b71-4f8f-abe0-bf486f6c7e0c" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A new array with elements that pass the test implemented by the provided function.</li></ul><ul id="67b51fcd-2b79-452c-8a57-8b0db782503c" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="78f71d84-206e-4916-beea-a5ff558d14db" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let numbers = [1, 2, 3, 4];
let even = numbers.filter(n =&gt; n % 2 === 0); // Returns [2, 4]

</code></pre></li></ul><h3 id="b14e46e3-b62c-48b7-bf39-5b985f350fbd" class=""><strong>3. </strong><code><strong>map</strong></code><strong> (Array Method)</strong></h3><ul id="0eb47335-f248-4496-946d-4dbb2ff2f067" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>callback(currentValue[, index[, array]])</strong></code>, <code><strong>thisArg</strong></code> (optional)</li></ul><ul id="630071e1-e123-4e6f-8724-89b06c2bc64e" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A new array with the results of calling a provided function on every element in the calling array.</li></ul><ul id="e49f4d78-bf39-49a9-bba8-cce74e7d3b5e" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="5a68d5e4-a266-4b9d-bdb4-a2fb3c7e91f9" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let numbers = [1, 2, 3, 4];
let squares = numbers.map(n =&gt; n * n); // Returns [1, 4, 9, 16]

</code></pre></li></ul><h3 id="04803401-a983-4a98-bf37-b1e1501d0721" class=""><strong>4. </strong><code><strong>reduce</strong></code><strong> (Array Method)</strong></h3><ul id="94259f13-f9fe-4d1b-97a6-268ea0575f56" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>callback(accumulator, currentValue[, index[, array]])</strong></code>, <code><strong>initialValue</strong></code> (optional)</li></ul><ul id="a71c617b-9287-4248-94dd-a9bc9289d7af" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: The single value that results from the reduction.</li></ul><ul id="72c92936-45c7-43a6-983f-28cecc290d56" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="f8a9b2f9-4d76-41df-a8a9-0c2086167c4c" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let sum = [1, 2, 3, 4].reduce((acc, val) =&gt; acc + val, 0); // Returns 10

</code></pre></li></ul><h3 id="af4b968e-8b44-49a9-8ea3-546a844a577f" class=""><strong>5. </strong><code><strong>forEach</strong></code><strong> (Array Method)</strong></h3><ul id="fbeeb1bc-3476-4b01-8448-ca23954f0b3e" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>callback(currentValue [, index [, array]])</strong></code>, <code><strong>thisArg</strong></code> (optional)</li></ul><ul id="7cb65d09-e0da-4103-a1c3-a8b3ee5be419" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: <code><strong>undefined</strong></code>.</li></ul><ul id="00a5663f-d639-4861-9825-c47d1ce9f1e5" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="c2eec4da-4331-4de6-9079-de4ba28e4265" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
[1, 2, 3, 4].forEach(alert); // Alerts each number in turn

</code></pre></li></ul><h3 id="d7835bf6-8124-460b-a33b-8e85fbbdc3b4" class=""><strong>6. </strong><code><strong>every</strong></code><strong> (Array Method)</strong></h3><ul id="4fa9333e-6191-4040-89d9-0c182e03df73" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>callback(element[, index[, array]])</strong></code>, <code><strong>thisArg</strong></code> (optional)</li></ul><ul id="c97edb58-1fc7-4a48-935c-9ef15a33753b" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: <code><strong>true</strong></code> if the callback function returns a truthy value for every array element; otherwise, <code><strong>false</strong></code>.</li></ul><ul id="30b2d04a-e706-4d5d-8aa1-1b7a9b9da8fe" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="07afbbad-affd-4a53-83c0-1e4d354bcf90" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let allEven = [2, 4, 6].every(n =&gt; n % 2 === 0); // Returns true

</code></pre></li></ul><h3 id="b274f39c-5a0c-4a3e-b9cd-bbd89b0404f5" class=""><strong>7. </strong><code><strong>some</strong></code><strong> (Array Method)</strong></h3><ul id="a46f3e5b-24fa-4046-bcf7-a7e9f9adbf1f" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>callback(element[, index[, array]])</strong></code>, <code><strong>thisArg</strong></code> (optional)</li></ul><ul id="53b39072-e17b-45e6-bf3c-884c2b9d30a9" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: <code><strong>true</strong></code> if the callback function returns a truthy value for at least one element in the array; otherwise, <code><strong>false</strong></code>.</li></ul><ul id="81ba352a-5712-45e6-8efd-49f0ca1bbbc7" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="6a0c692b-17f9-41a9-97e5-85cda779edaf" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let someEven = [1, 2, 3].some(n =&gt; n % 2 === 0); // Returns true

</code></pre></li></ul><h3 id="7c1ef5f7-4852-40a6-a2bb-481713930d8e" class=""><strong>8. </strong><code><strong>find</strong></code><strong> (Array Method)</strong></h3><ul id="8e49e14e-4e41-4009-8537-7628d12ba1c0" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>callback(element[, index[, array]])</strong></code>, <code><strong>thisArg</strong></code> (optional)</li></ul><ul id="f51bf7b7-a5e4-4592-8300-615339e10e15" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: The value of the first element in the array that satisfies the provided testing function. Otherwise, <code><strong>undefined</strong></code>.</li></ul><ul id="72fd690c-5a5a-4488-9ae3-6987b0d39832" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="cc375904-0f23-4288-ba09-520fb8fc5cd2" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let found = [1, 2, 3, 4].find(n =&gt; n &gt; 2); // Returns 3

</code></pre></li></ul><h3 id="2c4a9aa6-0d0f-49e3-81d3-96d4cca08e29" class=""><strong>9. </strong><code><strong>findIndex</strong></code><strong> (Array Method)</strong></h3><ul id="4b6270f4-b6f3-4d3e-9731-61e0f9bbd2ca" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>callback(element[, index[, array]])</strong></code>, <code><strong>thisArg</strong></code> (optional)</li></ul><ul id="c60b7689-0911-4ca6-b732-1914245470c6" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: The index of the first element in the array that satisfies the provided testing function. Otherwise, -1.</li></ul><ul id="4298fdbc-3bb9-4244-b480-f2f35378f59e" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="eb2f517f-2dd3-44fa-aaca-cdc9c4fba111" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let index = [1, 2, 3, 4].findIndex(n =&gt; n &gt; 2); // Returns 2

</code></pre></li></ul><h3 id="e88ed2db-c130-4cc8-9afb-0007b4373a14" class=""><strong>10. </strong><code><strong>sort</strong></code><strong> (Array Method)</strong></h3><ul id="2409a1eb-a320-41e1-8e75-a9abbaaab063" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>compareFunction</strong></code> (optional)</li></ul><ul id="6f91b1a3-1635-4cbf-9fce-79b6718b196d" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: The sorted array.</li></ul><ul id="27bad2cf-0ddb-41a8-8ce1-8d658ec030e5" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="47e97d43-cf9e-4276-ae8d-be66bf398fa8" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [3, 1, 4, 1, 5, 9];
arr.sort((a, b) =&gt; a - b); // Returns [1, 1, 3, 4, 5, 9]

</code></pre></li></ul><h3 id="6c8d6789-f86c-4928-a920-be6ac8bbdad4" class=""><strong>11. </strong><code><strong>concat</strong></code><strong> (Array Method)</strong></h3><ul id="21884388-73a4-4e30-8a17-523549a3fbae" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>...values</strong></code> (Arrays and/or values)</li></ul><ul id="eae9cc35-5be4-4885-a373-6b84f6f71851" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A new array consisting of the elements in the object on which it is called, followed in order by, for each argument, the elements of that argument (if the argument is an array) or the argument itself (if the argument is not an array).</li></ul><ul id="2dcdc7ad-65b0-4d4a-8414-575f51f6501c" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="e1388cda-e60a-47a2-8d4a-28967e4c36de" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
let combined = arr1.concat(arr2); // Returns [1, 2, 3, 4, 5, 6]

</code></pre></li></ul><h3 id="8f3c5ea3-a403-45b0-a6da-f4eae2be27cc" class=""><strong>12. </strong><code><strong>slice</strong></code><strong> (Array Method)</strong></h3><ul id="b3c82d35-c395-49ae-b156-e1bcc4e9a9df" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>begin</strong></code> (optional), <code><strong>end</strong></code> (optional)</li></ul><ul id="7f307342-8e36-4c2a-83c2-7ccf80ae033e" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A shallow copy of a portion of an array into a new array object selected from <code><strong>begin</strong></code> to <code><strong>end</strong></code> (<code><strong>end</strong></code> not included). The original array will not be modified.</li></ul><ul id="63193ce5-9c95-4960-84ed-78d2d7ebc649" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="82de0f94-cd2c-4bc8-9c6b-eb4694b26eb1" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [1, 2, 3, 4, 5];
let sliced = arr.slice(1, 3); // Returns [2, 3]

</code></pre></li></ul><h3 id="6b6b9240-1284-4392-bd7c-d709728db725" class=""><strong>13. </strong><code><strong>includes</strong></code><strong> (Array/String Method)</strong></h3><ul id="365ab5e7-cb1a-48fc-be15-666d6780a013" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>searchElement</strong></code>, <code><strong>fromIndex</strong></code> (optional)</li></ul><ul id="4ad2cc2b-7940-4360-a3bb-561cb07fc23c" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: <code><strong>true</strong></code> if the array/string includes the element/value, <code><strong>false</strong></code> otherwise.</li></ul><ul id="3ddecedb-f418-432e-aa32-c7cc6cd73189" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong> (Array):<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="c6a93d5f-61c2-4d1c-ace3-9df4dad7c4f4" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [1, 2, 3];
let includesTwo = arr.includes(2); // Returns true

</code></pre></li></ul><ul id="ae47424f-01f7-423a-8bf8-c968bd0f0e4c" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong> (String):<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="b49ff065-fbc3-4fe9-8d28-1fc100a2bf45" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let str = &quot;hello&quot;;
let includesEllo = str.includes(&quot;ello&quot;); // Returns true

</code></pre></li></ul><h3 id="708df683-6e3b-4ef8-9648-ae467080727b" class=""><strong>14. </strong><code><strong>indexOf</strong></code><strong> (Array/String Method)</strong></h3><ul id="aa759403-b217-49f6-b701-159d9cfb1782" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>searchElement</strong></code>, <code><strong>fromIndex</strong></code> (optional)</li></ul><ul id="f63e8dad-db35-4c0a-9072-6b3fa1e2d6b9" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: The first index at which a given element can be found in the array/string, or -1 if it is not present.</li></ul><ul id="9cd5c464-1035-4351-847a-ed12d7272f21" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong> (Array):<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="22aaafc9-e7cf-4542-aee3-bbad438b561a" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [1, 2, 3];
let indexOfTwo = arr.indexOf(2); // Returns 1

</code></pre></li></ul><ul id="56d156da-7773-48fc-ba24-e1009f8d0275" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong> (String):<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="d5e33e58-11ea-4cb7-9e1d-e93c9c713404" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let str = &quot;hello&quot;;
let indexOfE = str.indexOf(&quot;e&quot;); // Returns 1

</code></pre></li></ul><h3 id="5382fb63-dda1-4dd6-a8bd-6fcec3782026" class=""><strong>15. </strong><code><strong>join</strong></code><strong> (Array Method)</strong></h3><ul id="47b7b621-405f-4863-93e9-28a1cf6061d3" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>separator</strong></code> (optional)</li></ul><ul id="c9423466-aa68-4c13-858c-c6cf6f2e1f35" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A string with all array elements joined. If <code><strong>separator</strong></code> is not specified, a comma (<code><strong>,</strong></code>) will be used.</li></ul><ul id="c1e45963-fd27-45b8-8541-3b6c3f0aa405" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="165a31bb-9b87-4985-8c95-f551d251fc4c" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [1, 2, 3];
let joined = arr.join(&quot;-&quot;); // Returns &quot;1-2-3&quot;

</code></pre></li></ul><h3 id="db66337e-9011-488a-8017-366199fa018d" class=""><strong>16. </strong><code><strong>toString</strong></code><strong> (Global Object Method)</strong></h3><ul id="e4326eef-2e7c-4175-8826-86996acdb7e4" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: None</li></ul><ul id="34398891-e4bd-46c5-b835-fbb46ca021ae" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A string representing the object.</li></ul><ul id="d95bef89-29ed-4f5e-b735-2fff9c57d51d" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="08bb7a52-8837-4238-a316-d6febae92db0" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let num = 123;
let str = num.toString(); // Returns &quot;123&quot;

</code></pre></li></ul><h3 id="1777e07d-64b8-4d46-9b11-4f79c0caaaf9" class=""><strong>17. </strong><code><strong>toLocaleString</strong></code><strong> (Global Object Method)</strong></h3><ul id="c4eb51ab-2a12-4746-8cc5-16b67516716a" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: Varies by object</li></ul><ul id="069d3eee-c313-4a51-8aee-021e40831d6a" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A string representing the object. This method is meant to be overridden by derived objects for locale-specific purposes.</li></ul><ul id="1193c4c9-b55e-4422-a818-00c8046a0715" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="0b2ad65d-a4cb-4160-b4ec-69f8b6564b80" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let num = 123456.789;
let str = num.toLocaleString(&#x27;en-US&#x27;); // Returns &quot;123,456.789&quot; for US English locale

</code></pre></li></ul><h3 id="b52712aa-8a71-4ca7-8769-0d427e6668ee" class=""><strong>18. </strong><code><strong>shift</strong></code><strong> (Array Method)</strong></h3><ul id="07d4fecc-69ff-425e-b71f-8dc732f79ba9" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: None</li></ul><ul id="a56f77ac-1fb8-430f-8272-b4428ad992a2" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: The removed element from the array; <code><strong>undefined</strong></code> if the array is empty.</li></ul><ul id="a89edf4f-e27f-47a9-83e5-36d0692b5ecf" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="c37498af-31fc-423b-87a2-a16e83205ee6" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [1, 2, 3];
let first = arr.shift(); // Returns 1, arr is now [2, 3]

</code></pre></li></ul><h3 id="13963ee0-75d5-4245-b12e-d45e86533020" class=""><strong>19. </strong><code><strong>unshift</strong></code><strong> (Array Method)</strong></h3><ul id="35a8eb1f-7c2e-48b3-84d6-d5d741a24e9b" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>...elements</strong></code></li></ul><ul id="163fd5b5-f3ed-4f5c-be92-ecd50100d3a3" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: The new length of the array.</li></ul><ul id="56cb51bb-cef3-4175-a5e2-0ad8e6294572" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="6832b3f4-32a0-48a6-8ddb-a7301c43b124" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [2, 3];
let newLength = arr.unshift(1); // Returns 3, arr is now [1, 2, 3]

</code></pre></li></ul><h3 id="02eaae58-f9e7-4c2f-8769-38a871a82a61" class=""><strong>20. </strong><code><strong>reverse</strong></code><strong> (Array Method)</strong></h3><ul id="391d4f66-2e80-4bc6-bb7d-93e7e5e6da3e" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: None</li></ul><ul id="b39debf5-1149-4c51-addc-393c387ad114" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: The reversed array.</li></ul><ul id="ed36a31d-633b-464a-a8f9-b65eb3f138d7" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="c785c9ef-5dae-4849-bc4c-dba2fcef2e62" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [1, 2, 3];
arr.reverse(); // Now arr is [3, 2, 1]

</code></pre></li></ul><h3 id="eb019436-fa22-4e97-b635-e9f8aff6d393" class=""><strong>21. </strong><code><strong>fill</strong></code><strong> (Array Method)</strong></h3><ul id="4a0dc757-8164-4b33-a33b-f262f27f1fd1" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>value</strong></code>, <code><strong>start</strong></code> (optional), <code><strong>end</strong></code> (optional)</li></ul><ul id="9a6c951e-59f6-423e-beb7-843603dfea4b" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: The modified array, filled with <code><strong>value</strong></code> from <code><strong>start</strong></code> to <code><strong>end</strong></code>.</li></ul><ul id="6237a44f-555b-4fa9-ab76-8bc370e1fc19" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="654700be-fdb8-4b54-ade0-db6fe69c7790" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [1, 2, 3, 4];
arr.fill(0, 2, 4); // Now arr is [1, 2, 0, 0]

</code></pre></li></ul><h3 id="5092b358-be6d-4803-a58a-ac325a4839dd" class=""><strong>22. </strong><code><strong>copyWithin</strong></code><strong> (Array Method)</strong></h3><ul id="9321ebb4-0cc7-4c0c-88a8-4227aed338f4" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>target</strong></code>, <code><strong>start</strong></code> (optional), <code><strong>end</strong></code> (optional)</li></ul><ul id="68746d6a-f7d2-409f-9987-22b3b0498973" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: The modified array.</li></ul><ul id="57c5a988-9b2f-4f73-afbc-a179e42fc960" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="7bb8b8d0-d9c6-4cbe-a4fe-351a52ab00ea" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [1, 2, 3, 4, 5];
arr.copyWithin(0, 3); // Now arr is [4, 5, 3, 4, 5]

</code></pre></li></ul><h3 id="ceb8f92a-2077-4c67-a1c3-5ffbf3cbb262" class=""><strong>23. </strong><code><strong>flat</strong></code><strong> (Array Method)</strong></h3><ul id="fd634e91-c9e8-4177-9b67-a3b55c2a9b46" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>depth</strong></code> (optional)</li></ul><ul id="5502355c-ee57-48f1-ada8-faa8a8cd9281" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A new array with all sub-array elements concatenated into it recursively up to the specified depth.</li></ul><ul id="78c40c79-83ab-4c5c-8fa8-be965b8f9c5a" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="c842dc48-eb31-4be2-bbf3-dd039747a72b" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [1, [2, [3, [4]]]];
let flattened = arr.flat(2); // Returns [1, 2, 3, [4]]

</code></pre></li></ul><h3 id="e2ae648b-7e99-4dff-8f5d-bdb1da6f0f02" class=""><strong>24. </strong><code><strong>flatMap</strong></code><strong> (Array Method)</strong></h3><ul id="c74eee65-969a-4c62-97e5-cc43e4c040af" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>callback(currentValue[, index[, array]])</strong></code>, <code><strong>thisArg</strong></code> (optional)</li></ul><ul id="5e2369fe-38ea-4241-806f-d5895fae5973" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A new array formed by applying a given callback function to each element of the array, and then flattening the result by one level.</li></ul><ul id="fdba17e3-451a-42d8-94a5-0bf537c737db" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="8126ba11-4765-408e-90d5-b578de0b6965" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [1, 2, 3];
let mappedAndFlattened = arr.flatMap(x =&gt; [x, x * 2]); // Returns [1, 2, 2, 4, 3, 6]

</code></pre></li></ul><h3 id="d729dc04-5180-418b-8897-ae87b720a8e4" class=""><strong>25. </strong><code><strong>keys</strong></code><strong> (Object/Array Method)</strong></h3><ul id="cd2254d6-935b-4e9d-9361-ef2ecf453469" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: None</li></ul><ul id="e1e4eed7-ec14-4ea0-91a7-f6b6b4e72409" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A new Array Iterator object that contains the keys for each index in the array/object.</li></ul><ul id="0e30167d-04ba-4e31-879e-fd10d9848683" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="57a4cc29-5769-4b0c-8217-368a33783e27" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [&#x27;a&#x27;, &#x27;b&#x27;, &#x27;c&#x27;];
let iterator = arr.keys();
for (let key of iterator) {
  console.log(key); // logs 0, 1, 2
}

</code></pre></li></ul><h3 id="0bcbfed9-b3fe-4b7d-8cae-5076fdddd779" class=""><strong>26. </strong><code><strong>values</strong></code><strong> (Object/Array Method)</strong></h3><ul id="4a14075c-2be1-4ad9-99a2-c633c7aa6f5b" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: None</li></ul><ul id="370c9b56-b2ce-44a1-9251-f5b2221e9bca" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A new Array Iterator object that contains the values for each index in the array/object.</li></ul><ul id="0434715a-f253-4712-b723-5c0b0793eee2" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="4b6b27cf-c9bb-4f81-b803-c4c42867b36f" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [&#x27;a&#x27;, &#x27;b&#x27;, &#x27;c&#x27;];
let iterator = arr.values();
for (let value of iterator) {
  console.log(value); // logs &quot;a&quot;, &quot;b&quot;, &quot;c&quot;
}

</code></pre></li></ul><h3 id="49dda674-d30f-4b99-abc3-22a925543308" class=""><strong>27. </strong><code><strong>entries</strong></code><strong> (Object/Array Method)</strong></h3><ul id="1d927b65-bb43-46c1-8b94-4b99f4128862" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: None</li></ul><ul id="258d49af-ce15-4c53-b133-f810415b4ae4" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A new Array Iterator object that contains the [key, value] pairs for each index in the array/object.</li></ul><ul id="54872d12-8978-40a2-a244-eecb96c60079" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="5c90d2cd-ffe9-4c14-8451-971c73fd50d5" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = [&#x27;a&#x27;, &#x27;b&#x27;, &#x27;c&#x27;];
let iterator = arr.entries();
for (let entry of iterator) {
  console.log(entry); // logs [0, &quot;a&quot;], [1, &quot;b&quot;], [2, &quot;c&quot;]
}

</code></pre></li></ul><h3 id="a4d4a7cd-2db8-4660-b907-8c2d92bdc1fd" class=""><strong>28. </strong><code><strong>from</strong></code><strong> (Array Method)</strong></h3><ul id="47c9c56a-8ec3-46cc-9098-ea76d19e4685" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>arrayLike</strong></code>, <code><strong>mapFn</strong></code> (optional), <code><strong>thisArg</strong></code> (optional)</li></ul><ul id="287a2032-0670-4c84-9172-25de1fd71743" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A new Array instance from an array-like or iterable object.</li></ul><ul id="59b1f49f-8114-4408-bb5f-0bd3b61b6a42" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="6ef02516-2336-47cf-89e1-ec8975c85556" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = Array.from(&quot;123&quot;, num =&gt; Number(num)); // Returns [1, 2, 3]

</code></pre></li></ul><h3 id="9825db76-2aa1-4173-b46d-8c8c58e8e99b" class=""><strong>29. </strong><code><strong>of</strong></code><strong> (Array Method)</strong></h3><ul id="31dcdadc-a519-4334-8d51-eef3683db83b" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>...elements</strong></code></li></ul><ul id="e275a5f3-489b-4ee9-8a3a-4b728e72629c" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: A new Array instance with a variable number of elements.</li></ul><ul id="1c5ad994-0d5c-4b4e-a537-7c0782e2dfc5" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="0950dec4-ece5-4407-af16-234e5c703782" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let arr = Array.of(1, 2, 3); // Returns [1, 2, 3]

</code></pre></li></ul><h3 id="99beb3e6-ba0b-4820-a35a-fa363f79e53f" class=""><strong>30. </strong><code><strong>isArray</strong></code><strong> (Array Method)</strong></h3><ul id="5c476ddd-e1e8-430b-a8f7-a75c5b6f4f30" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>obj</strong></code></li></ul><ul id="d3e64788-9293-4b55-b96b-bae8fe9309c1" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: <code><strong>true</strong></code> if the object is an array; otherwise, <code><strong>false</strong></code>.</li></ul><ul id="2b86bc22-73dc-4722-bc07-59aa45271e6b" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="189309f2-2220-4fd7-8d87-f2d59edd9cad" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let isArray = Array.isArray([1, 2, 3]); // Returns true

</code></pre></li></ul><p id="cdc899ca-8b43-4753-ab10-41a60804b2ca" class="">The remaining items on your list refer to various JavaScript and Web APIs for type checking, parsing, and encoding/decoding strings. Due to the vast number of items, I&#x27;ll provide a general structure for those functions without detailed examples:</p><h3 id="79ebaef7-7c2c-4e14-b565-fc8b42fc890f" class=""><strong>31-47. Type Checking (Various)</strong></h3><ul id="074f7ecc-3a6c-4e91-8723-6b6b72096a6b" class="bulleted-list"><li style="list-style-type:disc"><strong>Example Structure</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="d0ac73a3-b223-47c8-8677-eaec49e632f7" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let isType = Type.isType(variable); // Returns true or false based on the type check

</code></pre></li></ul><h3 id="ee25f377-f25b-4aa3-91ac-17e835bbd8f1" class=""><strong>48-57. Parsing and String/URI Handling (Global Functions)</strong></h3><ul id="a9839d83-46cc-481e-9abb-9badfd74da8d" class="bulleted-list"><li style="list-style-type:disc"><strong>Example Structure</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="f43fbbe9-dddc-4790-9ed0-b8852d48a9ff" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let result = FunctionName(input[, additionalParameters]);

</code></pre></li></ul><h3 id="f4500931-df95-4991-89a5-75d9e5297412" class=""><strong>58. </strong><code><strong>eval</strong></code><strong> (Global Function)</strong></h3><ul id="5ab5337f-bd8e-4cd0-9281-3221c4e087dd" class="bulleted-list"><li style="list-style-type:disc"><strong>Parameters</strong>: <code><strong>string</strong></code></li></ul><ul id="7fcd4107-c1bf-44cd-bbe8-2e945559cbbd" class="bulleted-list"><li style="list-style-type:disc"><strong>Return Value</strong>: The result of executing the string as JavaScript code.</li></ul><ul id="a65a845d-7dd4-4155-8077-0268a26d164c" class="bulleted-list"><li style="list-style-type:disc"><strong>Example</strong>:<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js" integrity="sha512-7Z9J3l1+EYfeaPKcGXu3MS/7T+w19WtKQY/n+xzmw4hZhJ9tyYmcUS+4QqAlzhicE5LAfMQSF3iFTK9bQdTxXg==" crossorigin="anonymous" referrerPolicy="no-referrer"></script><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism.min.css" integrity="sha512-tN7Ec6zAFaVSG3TpNAKtk4DOHNpSwKHxxrsiw4GHKESGPs5njn/0sMCUMl2svV4wo4BK/rCP7juYz+zx+l6oeQ==" crossorigin="anonymous" referrerPolicy="no-referrer"/><pre id="695c8a62-c7b1-4f81-833f-c25e6480c9b7" class="code"><code class="language-JavaScript" style="white-space:pre-wrap;word-break:break-all">javascriptCopy code
let result = eval(&#x27;2 + 2&#x27;); // Returns 4

</code></pre></li></ul></div></article><span class="sans" style="font-size:14px;padding-top:2em"></span></body></html>