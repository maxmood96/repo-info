## `azul-zulu:25-headless`

```console
$ docker pull azul-zulu@sha256:949e74f7d7e56618808bf9f53747da6ae5b13bf73831f78ab61aaa34a27a8471
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:7ec3aa2ee7cdb5784bbbc5b681c198bed88f2f68f124c99e1c99730d643c583a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfa1229eba4740f4d8846e2caf46c9f7bc2ce8d221b4e7f15e54af04068256f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:12:27 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:12:27 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:12:27 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:12:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 17 Mar 2026 22:12:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41849ac281c06523772e70c3d7f8e7e042f8aa52ad1000c21b05e0e1decee4b`  
		Last Modified: Tue, 17 Mar 2026 22:12:44 GMT  
		Size: 182.6 MB (182608202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:17196b1935efdc6540cbbb81b27077e4ff631c295bfa2f7fa2756811fefd2b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e3b6a58e555c1a6d3c3f551e32fe7f9d18700f7bf0a2e58b03ea8354f2ac6c`

```dockerfile
```

-	Layers:
	-	`sha256:bf5481588b24f2e99594542207134ed02c8e7515ef942bab867c9612fa39d18f`  
		Last Modified: Tue, 17 Mar 2026 22:12:39 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:7c168c21a690fc74a418ecfca8e7d0ebf70ba9bde5acdddf3f4646e4c96ebe61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211895745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b9b4ff2fd4ee5cb90fb27eaf96a18b9e849962904159c0e346e72130ba6bf5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:12:07 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:12:07 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:12:07 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:12:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 17 Mar 2026 22:12:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da507ed725442b6906593e9bc6295fcad8ed5edae0b6a53ade1d744d87d67a2`  
		Last Modified: Tue, 17 Mar 2026 22:12:27 GMT  
		Size: 181.8 MB (181757329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:87ef1cb141f07f67de7a3140b4901c06dcfc564bf3eaa00fcf7373fa11956a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775cff6d3b779bfc7db6b54ff3a6f148741fbf9ef4498c0f53eea7ff60079955`

```dockerfile
```

-	Layers:
	-	`sha256:86a90663cfd1682a9c0dc55fa5a10cfa8b8fd5d1e3a81de2d29d4903b2eb2f41`  
		Last Modified: Tue, 17 Mar 2026 22:12:23 GMT  
		Size: 9.4 KB (9399 bytes)  
		MIME: application/vnd.in-toto+json
