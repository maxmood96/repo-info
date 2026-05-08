## `azul-zulu:11-headless-debian13`

```console
$ docker pull azul-zulu@sha256:5b555dbbf7fd92d8a59bd39aca3419ec7d5796bfec80af25673ab34f35d3298f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:36f071152a483a9c04d6b2a244fbbc0e39081d148a423cae627a50c267d21fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175980077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736d908a4e1e778a89c649b262891da5fb4145926256dd77c9b464e573c2d105`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:37:21 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:37:21 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:37:21 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:37:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Fri, 08 May 2026 19:37:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc65bd9807c2e37785173fa1b66394c8d8e93bdce5224c28712476b8c2c708`  
		Last Modified: Fri, 08 May 2026 19:37:36 GMT  
		Size: 146.2 MB (146199851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:310ceb0f4b0e818750c2b3f0fa3bc39e2cc17cbc95c506e53cb950083ff4f56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c236fd58c67ac9daa604e15de1f53a993ce1f400bcdb6a1e1abf9caa00e1a826`

```dockerfile
```

-	Layers:
	-	`sha256:7134ad79ba67f032bf6cbfdbd1e6346f431be86625ce630ecee75668742764db`  
		Last Modified: Fri, 08 May 2026 19:37:32 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:a72be232ff7e38826e3405e6a6e1ba0ffc2c4669a2ed0f2aae7c025039b8dc18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176053212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83ec0fcecf43360210b88f4b027b7a6cda1af923728e327caf327edffb9635`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:39:33 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:39:33 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:39:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:39:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Fri, 08 May 2026 19:39:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2358a9fd385cb8e45ab15ffad94b443924f5650e9375bce147c8c30247b2db65`  
		Last Modified: Fri, 08 May 2026 19:39:48 GMT  
		Size: 145.9 MB (145909570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f42bbbe1980aa493b96c24d975a8956897e74f1716b4f6fd1829e430c7c58293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10ffd1127f90865d13a25c46a00e7443289c27db289f47ae6ccc3291eb20e50`

```dockerfile
```

-	Layers:
	-	`sha256:8fb9a01f1c3458a0ea87b16780eeeb89b91e97f550759c4af038e37f506a8cb6`  
		Last Modified: Fri, 08 May 2026 19:39:45 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
