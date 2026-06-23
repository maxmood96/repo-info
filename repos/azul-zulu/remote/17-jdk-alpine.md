## `azul-zulu:17-jdk-alpine`

```console
$ docker pull azul-zulu@sha256:8f34902d50325375c720820c98ea27646ede5e988ffe467aa3bd937dd5d6da39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jdk-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:8e5c635e630e1f1e95f2817d6499c3a396a49a4683500c357bce7f51475f77b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152226542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6e99acb9a02821498b017891aab8d0d45d7d545779ef9d0ee880596160bb1d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:10 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:55:10 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:10 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jdk=17.0.19-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:55:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Mon, 22 Jun 2026 19:55:10 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:55:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7411355d120731146819e6c79223812c9ac9befc76d00e9caf1c70b59e549fc`  
		Last Modified: Mon, 22 Jun 2026 19:55:25 GMT  
		Size: 148.4 MB (148382121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:fa1ce1102b9a731e87245ae542ea9f112724e8ecd3930a024ff2c6e8d472a5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ff006e5663437e8609ba673e2933008c3145da71fb81abcdd024283fa205c7`

```dockerfile
```

-	Layers:
	-	`sha256:18d81705b6a21192531c40b498d12f2f4bae5a2ddddaa51d1a1b99e54688f49c`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 7.8 KB (7821 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:20c6908f83e2d6191a834f4e6e4ff2d1f79a25c13b026d267bff81d85d5c0a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150002018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e16e3d956c27984cf3ca80c7402854d1bf032a3c910b7ad25e5a5159a12520`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:48 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:56:48 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:56:48 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jdk=17.0.19-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:56:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Mon, 22 Jun 2026 19:56:48 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb589c43b31b714aec6d21d3c429bd331d702ccb15a6789abea0b7eceec0833`  
		Last Modified: Mon, 22 Jun 2026 19:57:03 GMT  
		Size: 145.8 MB (145820158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4f73f9029e1da55eac56390147cb593fd5e1c9efe3a5137b93d68e28b857b89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42cb8eae04cbaa82991b17991ae915525c74317ece3ad5d4e8ed73cf9e34d4a8`

```dockerfile
```

-	Layers:
	-	`sha256:8c9938f277556e6fa046d011d8e8e71daa6e7093e34e3a928745fbd6669283f1`  
		Last Modified: Mon, 22 Jun 2026 19:57:00 GMT  
		Size: 7.9 KB (7926 bytes)  
		MIME: application/vnd.in-toto+json
