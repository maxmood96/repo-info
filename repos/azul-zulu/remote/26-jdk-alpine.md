## `azul-zulu:26-jdk-alpine`

```console
$ docker pull azul-zulu@sha256:a4a9fb0bc3c6808312522a523d4e4554d7abc63744a83cb73b38140bda6c6982
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jdk-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:52f55cdf3ff853c41fcfd1f1326c5d68f27ebd0fa7f408f222d5ea85de83f175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187902234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55a1b6dde94fcbece8f3b33274608f37dca830a6b4bad4d261794cebc8920e3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:58 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:55:58 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:58 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu26-jdk=26.0.1-r1;      java -version # buildkit
# Mon, 22 Jun 2026 19:55:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Mon, 22 Jun 2026 19:55:58 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:55:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d493e5a43cf07abf0eaaca731e6f29091f7d8959148845783f546a1b0178bf6`  
		Last Modified: Mon, 22 Jun 2026 19:56:16 GMT  
		Size: 184.1 MB (184057813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:de715e75bbea171e1dbdc0cea87fb73b3340ca81538dcdb2850487e094517840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f792e77b62e34cc03d93c8f66ce783d4a601ceba7997be363f022d22c7e745`

```dockerfile
```

-	Layers:
	-	`sha256:b9f433e97bde898119afe4d24de8e5a55c7d211b65dd0fae14f9763651fbf34f`  
		Last Modified: Mon, 22 Jun 2026 19:56:12 GMT  
		Size: 7.8 KB (7818 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:92e91f87fa30b12160def8f344f7f227c9f66baf0c739613032ad2674af4efda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185761315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d7b480a77ad52faec048086ffaf891a24e9a1d04c06da51346471d57d33fb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:36 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:57:36 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:57:36 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu26-jdk=26.0.1-r1;      java -version # buildkit
# Mon, 22 Jun 2026 19:57:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Mon, 22 Jun 2026 19:57:36 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae2df6f9b3c4c7cf96b4b0d95986a18e8e8f28f8adfef4617662c7547aa82d`  
		Last Modified: Mon, 22 Jun 2026 19:57:56 GMT  
		Size: 181.6 MB (181579455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6cdb9e13b6a7fc34d869f75e5e8d71a60e67b3f4a08a2ff674dd9337c569d91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea6add22633e265c526826155afb595dd0d0af60881c2457fd18c85f577fd5a`

```dockerfile
```

-	Layers:
	-	`sha256:ac479c3eb9aeb01e57eb6f65d3072ccfbacc25476e9dbddaa030e2f28af63197`  
		Last Modified: Mon, 22 Jun 2026 19:57:52 GMT  
		Size: 7.9 KB (7922 bytes)  
		MIME: application/vnd.in-toto+json
