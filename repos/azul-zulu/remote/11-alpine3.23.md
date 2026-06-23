## `azul-zulu:11-alpine3.23`

```console
$ docker pull azul-zulu@sha256:334e08e6e9f91691aa6739750ec64962ebf0f7f03fb6a715b9cc4a9fa6891017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-alpine3.23` - linux; amd64

```console
$ docker pull azul-zulu@sha256:9da1adcf0c9878abed65ca98dd02a0f32df1c1d3ab553d91de9b62328b796740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147935029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181ffed2b2c249ce1e1f376139a4da3069ae4ba991affc7b4ff746bd2e0394a0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:02 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:55:02 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:02 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jdk=11.0.31-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:55:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Mon, 22 Jun 2026 19:55:02 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:55:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1d3d26c21487a24ca6c7178f8228e74a7472ed71814109c7a1be26cf2e6c66`  
		Last Modified: Mon, 22 Jun 2026 19:55:16 GMT  
		Size: 144.1 MB (144090608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9d3820ba7a465adb337df2291a27783ffd258b51bb22048f3b85c2aa4cdf2c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8221937784976e74063ba8b3327946ff57e634c067794bea5169370f8a20802`

```dockerfile
```

-	Layers:
	-	`sha256:7314f0b72fa3a94163871496fe2b3c5429b4d727e24039210f778f0a245dfad2`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 7.8 KB (7822 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:b97b05e9bd159ddacfe5de49d00c7774837195298305a09c476a7bc7eba7fae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145615049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27228d977a03b9767938cc99a2b5b38faa08c2a0c696ffe48603b9df2a66531`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:37 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:56:37 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:56:37 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jdk=11.0.31-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:56:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Mon, 22 Jun 2026 19:56:37 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416013a204c8a24a9cfd1e5060c70daf40f9d2159b4121e7b085abee7ff755fc`  
		Last Modified: Mon, 22 Jun 2026 19:56:51 GMT  
		Size: 141.4 MB (141433189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d796376da07a82ba471bb44178540e9f6f545fe33150b97dd960fd6e091a6882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a650a44fe78eec4efcf21aecfcc4b122ca96420dbdf2fffe257c54df5d10b097`

```dockerfile
```

-	Layers:
	-	`sha256:4e3f0c21b683f0658b6df0681bf2370972430fd8581da1fb3ae42e28420ea3ee`  
		Last Modified: Mon, 22 Jun 2026 19:56:48 GMT  
		Size: 7.9 KB (7926 bytes)  
		MIME: application/vnd.in-toto+json
