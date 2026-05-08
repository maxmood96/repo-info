## `azul-zulu:8-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:54689ed1c082e1e63d3f39fd6f70b5dbf51c6a9f6f381a9f3dc8cf6646faa92f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:2b4195736a3e7d07a0f3aa9601cf9dbc2bcdb7ffb5d96af4f432908acd3bc195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77507181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e11941883b6578ebc18e4db1ac2f265b439b8514e2b13fcf27c63533628bf35`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:37:10 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:37:10 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:37:10 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:37:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279677c69582e541ce6545a7a7fceaa65fc0701b96af357d1200618f10380998`  
		Last Modified: Fri, 08 May 2026 19:37:19 GMT  
		Size: 47.7 MB (47726955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2b827f851870f3d3176061a4786f9b7790b499bc00e9cc2fdf7fdd25f719a660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee13295ecbd528d1a824c97ced6e5e608903371ff649b86fbf1fa081f81b22c4`

```dockerfile
```

-	Layers:
	-	`sha256:8e691933efc28e069555d7e2223813ea0245c78b54fae1788c2735041831ccc8`  
		Last Modified: Fri, 08 May 2026 19:37:17 GMT  
		Size: 9.3 KB (9285 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:5547b7c339b5467069c8380e826b5eba4aeac5c17654d4132f39b330a251b63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78094797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a2bf87976e655949a6814679433b0afb0b1fa7ebfb7b53d31112da9ca4757c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:39:01 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:39:01 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:39:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:39:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9383d7ee41ae26004f2df392eac9c45668c48a4e8a031b16be69b47aa9f2e18`  
		Last Modified: Fri, 08 May 2026 19:39:09 GMT  
		Size: 48.0 MB (47951155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6423b6f7e6a4e59d68acfb2578de203fcf58fecda5e54cf57aa36813b8281f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1e9aa9c6c346c880872ec1605a9152959a48b51a9f87274fde7073445dbc2a`

```dockerfile
```

-	Layers:
	-	`sha256:57fc25a063241c52120a0365cd6f10ca549988e4d0e9551df115a0d86fc0a590`  
		Last Modified: Fri, 08 May 2026 19:39:07 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json
