## `azul-zulu:21-jre`

```console
$ docker pull azul-zulu@sha256:333718f8913fc0b79ec5f367f3f5f1f1c2602fe8efa9f0f2477106d61361594d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c2579723215a12b52ba3b8776670bcc2611c50d8874714987de4276ceb9b71fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106676132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76573e2d7859280e087b63af4ac347759ab325f80710b93288bbd3263a1cccd3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:39:01 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:39:01 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:39:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:39:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f7c3787ca9b2bc58134c0e2655372157baf818d42afda2761e0233a6144cb1`  
		Last Modified: Fri, 08 May 2026 19:39:14 GMT  
		Size: 76.9 MB (76895906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8125670f536df94589b19fb43fb5538e18f7b91a7a2151fc9c862f79dda9c60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3444012847a4037528d6f3900991726cfdbadeada6934f0969f6a4ccad5724b`

```dockerfile
```

-	Layers:
	-	`sha256:8574d910daeb16a2d5868dfad6b1d369cdcd3a74104c9b14494bd356560e165d`  
		Last Modified: Fri, 08 May 2026 19:39:11 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c69c533012736114b3d12db5a8e66a2aecc6c255dec20bfd34bcb667fe212d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106690822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9091012938e5e8d6f47691ccd15d5b6213640030856e45f52d4cf72ded485103`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:11 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:41:11 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:41:11 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:41:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14240a9f7aad7472ed7c156fbc0cb2f0df6a4879afd76b00b3e2819ad5612bf`  
		Last Modified: Fri, 08 May 2026 19:41:24 GMT  
		Size: 76.5 MB (76547180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7c1672198dcb4e4bb28094e872804b894f6b76f605e4cf7f4452f8a501dc865b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a973b6a4696d214ef97cdfada7299235321c7e1a9f9700978f563ee5d963e6c5`

```dockerfile
```

-	Layers:
	-	`sha256:dec76f7d72fcc0f8f30616e3ddbb39742bf98b49e0a2c109bbdfcbcc2f600cff`  
		Last Modified: Fri, 08 May 2026 19:41:22 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
