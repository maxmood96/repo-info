## `azul-zulu:17-jre-headless-alpine3.23`

```console
$ docker pull azul-zulu@sha256:83a4df164fd6cea7a0661665e100aa540bef05e59580b2ad78fb653de95f644b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-headless-alpine3.23` - linux; amd64

```console
$ docker pull azul-zulu@sha256:7fc0620249bcadf57271ebc52d3ec238dfe9ae4935e8aad242e961f621f8f248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67524182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90880405a446673a9e6c0326b352dad2a0b58de4a1147e49a1bba677880eae1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:22 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:55:22 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jre-headless=17.0.19-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:55:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Mon, 22 Jun 2026 19:55:22 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba97d3d6d0948a3752b17741a2e3908a81f83b261f90ca0da45e3e097c764ca`  
		Last Modified: Mon, 22 Jun 2026 19:55:33 GMT  
		Size: 63.7 MB (63679761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d9b79153c94fd6598fbd7c2f950bd47063f386a028edd0fdd80535df870bcba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4efe47221b83eb60ba72b6caa6a52e82c5ae21ccd36ce1a230eed001ac75656`

```dockerfile
```

-	Layers:
	-	`sha256:be8b28787ec636317acc208ef7f2468aca13d4cce1da370640a68b34ed11a3f8`  
		Last Modified: Mon, 22 Jun 2026 19:55:31 GMT  
		Size: 7.6 KB (7575 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-headless-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:0116fe3bd3510d23c5d36d5b0050482aaf9e6b2121fbb98f0a9b5682ba7078af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66697043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c51d5966f0ca316c3a87be557a083146732e5b77e17f754b97ef6a253fd9e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:01 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:57:01 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:57:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jre-headless=17.0.19-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:57:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Mon, 22 Jun 2026 19:57:01 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f0ffd65db17e05c5e05dc69f863bc7a82e1e6dc0fb0530af75481a623bea3a`  
		Last Modified: Mon, 22 Jun 2026 19:57:13 GMT  
		Size: 62.5 MB (62515183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:55ed8d232aa82d75c666c2a84448f5d46bd8ab9bfb5f8eabaae7084c7073e5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e078239ce48fb49c67fb146a125d78663de8a466bf92ab086a8b502795e02a`

```dockerfile
```

-	Layers:
	-	`sha256:6b3a67b771c00ce532593d9dcebc36077242bdc6460db44885d39484e4f280e0`  
		Last Modified: Mon, 22 Jun 2026 19:57:11 GMT  
		Size: 7.7 KB (7668 bytes)  
		MIME: application/vnd.in-toto+json
