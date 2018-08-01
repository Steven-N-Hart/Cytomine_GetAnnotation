# Cytomine_GetAnnotation
This repo shows how can we export annotations(mask) and corrosponding images(patches of original slide images) from a Cytomine server.
You should have a Cytomine server and install the Cytomine python client package first. I have modified the official version, and made it capable for Python 3.

Q&A:
1. How can I get the enviroment variables, such as CYTOMINE_HOST and CYTOMINE_PUBLIC_KEY?
Ask your Cytomine server manager.
2. What's "url base address",and how can I know it?
"Url base address" is associate with your Cytomine server. Our code will use this url
address and some other information(image.fullPath) to piece together a full url to download an original image.
You can refer to the last couple of lines in export_annotations.py.
Login to your Cytomine server, open a project,and you will find a list of images. Find the download selection in the dropdown combbox, right click and save the link.
Run conn.fetch_url("link you just copied") in your code,you will get the "Url base address" in the console.
There might be more efficient ways to get it, tell me if you find it.

Contributors:
Jiang.Jun@mayo.edu
Hart.Steven@mayo.edu
