## `azul-zulu:21-headless`

```console
$ docker pull azul-zulu@sha256:3f7ce43b5971c76a8de1b744f60f3550b775b5286304255eabc60a0861292f28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:3a1fb95f8ce16102c036d65ae1fd617c082b244e959c2362785299593a064baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193616909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8667d6e5609843599f025d51887d2e174f873638fb2b582b72fb73e19871f87c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:45 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:38:45 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:38:45 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:38:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Fri, 08 May 2026 19:38:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27417baf57a6a850c8d7570d3870fd65e7d2b9f40649c9daaf98d82a8c5dd4f`  
		Last Modified: Fri, 08 May 2026 19:39:01 GMT  
		Size: 163.8 MB (163836683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d6d0979d315bc4e43bed9f2119ab3082f8844f5f2c8fc35efac85d9e31eb12b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadcb893cf10eeb1b51b0e37442a68e24796a5923d9749af6c6cb3df6ee7093f`

```dockerfile
```

-	Layers:
	-	`sha256:a75ccc5a94c39122409d701ad7b463329c87afea84afa295591fcadf25a933f5`  
		Last Modified: Fri, 08 May 2026 19:38:57 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:dc1d39c180df3e7b447f801cc5696c19ea483eec63a4bbe8aacc758db037e673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193292821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266a4224958e5213eebf139b52072117494799c89ff21c9156e37f386fdd9a61`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:09 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:41:09 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:41:09 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:41:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Fri, 08 May 2026 19:41:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9aac66a4cb8cf48bcfbbbee772b39fe179569420a1c08955388fb07ce2b42b`  
		Last Modified: Fri, 08 May 2026 19:41:27 GMT  
		Size: 163.1 MB (163149179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d76b2abd40d2e6c6403900afa1cccee7a094872d7d02bedd64dfe5921e10e3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1479ba92ca548a66c138ebbe1d4a210ef1d5e4051b0eb02e1d9b1cc53d648e4e`

```dockerfile
```

-	Layers:
	-	`sha256:86ba423821279eff041b88201891f1ff3d3e2e3ee27ef44c734393b76b5a2bd4`  
		Last Modified: Fri, 08 May 2026 19:41:23 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
