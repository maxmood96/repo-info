## `azul-zulu:21-jre-alpine`

```console
$ docker pull azul-zulu@sha256:a5caf78213f2ccc1e7e29d5b75a14722005a99f6b4e8ca5d4e814f46ca1834ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:72fb4d773709f3811cc4abeb6ea2b0c98af6a214c0c0cd318b3b9752f5d299da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75798192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600f5e2c0be6fe36e286c44ef48fc80515d59f53ae3ca6d0634daabc227a0865`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:33 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:55:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jre=21.0.11-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:55:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Mon, 22 Jun 2026 19:55:33 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39976cce6e53d24575aa1f571afdcd7c29665d24311a192e1c6f389b88fa9892`  
		Last Modified: Mon, 22 Jun 2026 19:55:46 GMT  
		Size: 72.0 MB (71953771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8497abb4624dd23f878961f4b55a2ca48cc22ec797ba8c40a4378f856ab0a75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6fdcf831dc1620f9ffea7b7f6f18096d1f90ffdf61a19c3855a9ed43082c6e`

```dockerfile
```

-	Layers:
	-	`sha256:ddd1a7456a58f93e9c2641092aaede12ee1a7a6af1dfc91cf9aeb1a5e497d527`  
		Last Modified: Mon, 22 Jun 2026 19:55:43 GMT  
		Size: 7.5 KB (7483 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:6dab53c59657f24d4c124c85265d8870bb5c63e09039a7d2c33f1aec022e379c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74896028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ab10d7478218b83eb7453c3ad17203b2cfd23666d93214f381542f1f77af65`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:12 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:57:12 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:57:12 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jre=21.0.11-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:57:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Mon, 22 Jun 2026 19:57:12 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57ef096833487a7e882c156887f8743cb4913d8b5977fa116b079700f2448c7`  
		Last Modified: Mon, 22 Jun 2026 19:57:24 GMT  
		Size: 70.7 MB (70714168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9aa638c2c50cb857d58605d0fc510e4e97793d529d358f5749f0c8821fe90141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc189c1de96c0907cfe9d59cc2122c594890eb806530a2cdddf0b8d064eb995e`

```dockerfile
```

-	Layers:
	-	`sha256:26d8e2e783038f2e900661bef521f12f6a8ffa208aa3107c23c1f0f0be7eb974`  
		Last Modified: Mon, 22 Jun 2026 19:57:22 GMT  
		Size: 7.6 KB (7575 bytes)  
		MIME: application/vnd.in-toto+json
