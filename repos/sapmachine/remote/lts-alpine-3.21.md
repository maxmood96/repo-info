## `sapmachine:lts-alpine-3.21`

```console
$ docker pull sapmachine@sha256:6907507d06654007701b4db4b2487cd9e2482d894249e304470f01d667e1045e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:6ce0e2300a6c8e3d348fbcf3444243047e644f4354484d35aa1e33fdeff2c038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225145567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff501ecefd50776b6dfde61da041fb705e6a1d9ccb6fba9c6e5b0557f9f358a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.1-r0 # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb83bd2d303375859773f471a66e3444c5cda0d8b4df25cb5350dd9ccfb7b2c`  
		Last Modified: Mon, 22 Dec 2025 16:00:51 GMT  
		Size: 221.5 MB (221502998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0a41b9c055b7c01baf5190deff5e87a5ae2b9c9f99282a3ad0dc49acc60e4f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.5 KB (510480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437f2396d445623d578c785e6ff55ea756b39da3b6fbc5f7cd6006367aaadb04`

```dockerfile
```

-	Layers:
	-	`sha256:188aab6d33e0a570a935a7098c3c30ea52f15f35ce790fe6a9bfe132068bbac3`  
		Last Modified: Wed, 22 Oct 2025 02:42:27 GMT  
		Size: 501.5 KB (501527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09650e0868c72511f60f58a9c50ebf78deb4bc8c4bc91fc81d8da63db98b330d`  
		Last Modified: Wed, 22 Oct 2025 02:42:27 GMT  
		Size: 9.0 KB (8953 bytes)  
		MIME: application/vnd.in-toto+json
