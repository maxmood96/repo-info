## `azul-zulu:17-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:737bc2fcafe6b41a643f146c3b42b0cf4f6c3c22a14eb39072514c4df405c130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:8d206acc3a30567381e844d71480b5bb4a736257f42d2adf0b1574cd50ff1715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99308642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d24086448516e451cbfa4740228c9b1c4ebe2a435fc199ee422e6a31cbac68d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:17 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:38:17 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:38:17 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:38:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e08524ebd4078f8528cf8bdc37c062171a776e1a50d5f95a156da8e03c5e03`  
		Last Modified: Fri, 08 May 2026 19:38:29 GMT  
		Size: 69.5 MB (69528416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6eeb91ba5335583277172e9869bc11777a0b40303ee1fb09fd6367528855e91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db942038eb97180b6eed5b4d05ff9c92535ad0b31618b86d3045714efaf8e47d`

```dockerfile
```

-	Layers:
	-	`sha256:5444eb656dc735211bf8ad5fa4e7574ad4973730651b6a39c5f0200a0485fd6c`  
		Last Modified: Fri, 08 May 2026 19:38:27 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:7614b5e1d765aa3b74b85b0c77ba6a8aba6e06718bb3faf873bd0e027a1c2de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99728097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9df142cb2d32c4c3317407a3a58ac5114b0ae8278f758efccfc32d8c491c3de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:39 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:40:39 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:40:39 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:40:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43022d1e1b3ff95b56617566242d6dea90fd93526015fafe4974cfea189df8b5`  
		Last Modified: Fri, 08 May 2026 19:40:52 GMT  
		Size: 69.6 MB (69584455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d5fd5c806fdc1818da65e391051939cf8ac355f0463f26ce64f12ba3a4d44843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0af3463cc5d42147dfc0a3dad1c3c6806604d8d3e7c2f71c9db51f75ee07885`

```dockerfile
```

-	Layers:
	-	`sha256:c7ef91050d8b7d18cde1a48563edea31569330282667e716775a309659eaac5f`  
		Last Modified: Fri, 08 May 2026 19:40:50 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
