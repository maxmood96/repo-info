## `azul-zulu:11-jre-headless-alpine`

```console
$ docker pull azul-zulu@sha256:c6df6044655505028e13f9c26386f815874bb18d2bb5bdf3ce407bdeb477c4ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-headless-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:9656a84d7b1f8156fbbafd39251766c50601581cf669a7de56ab5a30880368a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63052734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef4787f1a1fef182bda5329d99a238522050e8c8fcc3f00d4df481993ffcf46`
-	Default Command: `["\/bin\/sh"]`

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
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jre-headless=11.0.31-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:55:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Mon, 22 Jun 2026 19:55:02 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae4f7333e13164a4c04b6f7ad1ce96389762b84ecd14c042738ac1752701386`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 59.2 MB (59208313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:93ff445f533f93178be7bfe72e53d26da03f9f98ef5b287a6d4e89c8a294914b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058d6539a0495944ea0e307ebcb21af578cc33459adbaa6b69eae185dca674ce`

```dockerfile
```

-	Layers:
	-	`sha256:be223fbeac52fa2eea00a5e430c2c58484887115daf42c60ff4213a818b20d38`  
		Last Modified: Mon, 22 Jun 2026 19:55:11 GMT  
		Size: 7.6 KB (7576 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-headless-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:fee9b9c6cd128369e980ab1ae2e94f838446bd5e8c6ea2c523cdbeddc0ddd85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62127517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff74e421b5eaf1315b76215b7d5c12202dc6c75aaad868806b99581a55a6c93`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:44 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:56:44 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:56:44 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jre-headless=11.0.31-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:56:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Mon, 22 Jun 2026 19:56:44 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfea40c3ce19d3437f340e437e5b2e699f2f65edf77f44df3b732605c6d66df`  
		Last Modified: Mon, 22 Jun 2026 19:56:55 GMT  
		Size: 57.9 MB (57945657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4f2a815d31b1625badac01ce680b13ed58494290efc75670a55b979a8695601e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cb5e0cb3d46b02864ca280d56c180f2b5b3cd331d2164ffaa97bf949d38e3a`

```dockerfile
```

-	Layers:
	-	`sha256:552e88779e4a73a8886f7a387510d1ecdea0c9bb56f55fe0817c44d5ef1388dc`  
		Last Modified: Mon, 22 Jun 2026 19:56:53 GMT  
		Size: 7.7 KB (7668 bytes)  
		MIME: application/vnd.in-toto+json
