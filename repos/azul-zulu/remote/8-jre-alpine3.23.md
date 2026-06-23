## `azul-zulu:8-jre-alpine3.23`

```console
$ docker pull azul-zulu@sha256:b09b1aaf198f44350f2ef7bae421497147e8a3ebe71a469fd840d95f1221c9ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-alpine3.23` - linux; amd64

```console
$ docker pull azul-zulu@sha256:0aa6fb4878c12275e505df12cc818dec6a36cd153738116081b2ec18e5b75454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48511300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ddacee67924e9071d41102d53d79d13bfb314af33f0f32656be2491a144001`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:45 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:54:45 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:45 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu8-jre=8.0.492-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:54:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Mon, 22 Jun 2026 19:54:45 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ae34e7b7a79a98d0f71b901ff925c8ffbd7b8924d30736c0e09030295e6fc9`  
		Last Modified: Mon, 22 Jun 2026 19:54:53 GMT  
		Size: 44.7 MB (44666879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:49608825c2c0bbefe57054d92002fae9d92faf158bb6c357de4cc569e45399c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cef17b5e7915ac8006f21919b42baa17cbf4905f2b2e0e4f569cbebb49bf15e`

```dockerfile
```

-	Layers:
	-	`sha256:08e898f188d3e22c7854c2c86c71a0cd5b152cfbe438165e653024fbbb2c2eae`  
		Last Modified: Mon, 22 Jun 2026 19:54:52 GMT  
		Size: 7.5 KB (7474 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:2d88ea6980112cd1a726268f92fb720e5b500a01468c1ada2a0c67c7f1d54f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48038686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c52d0f7e54bbbbc039ded9fbd30d8ba8330733774fb1b819f1a8776b517abb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:29 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:56:29 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:56:29 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu8-jre=8.0.492-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:56:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Mon, 22 Jun 2026 19:56:29 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce5e5866b63d015a8fdbc8da26b5519038858ca2840ed32e2f73a6a96b26f3c`  
		Last Modified: Mon, 22 Jun 2026 19:56:37 GMT  
		Size: 43.9 MB (43856826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2445c6405ac16b8bb1162ad22aef276f93511b3288bb94b52885323566f78724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fbf32d07c361fa5e1e223708d688ea72482408a59348a07308df88babccc57`

```dockerfile
```

-	Layers:
	-	`sha256:885bd66fb0b864923e65b19cd926021ea6790013ed6ff710dcabb3088eb3a2a8`  
		Last Modified: Mon, 22 Jun 2026 19:56:36 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.in-toto+json
