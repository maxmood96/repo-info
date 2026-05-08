## `azul-zulu:8-jre-debian13`

```console
$ docker pull azul-zulu@sha256:16302e469e76eba684c3afa81b4febf0f189b96313acea98a8fdf5bed40e1dd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:cd9c9d814772a58dc1fad93ba018e5c98e38e53669de7dd981f0786b3a66edd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79612325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e973bad859f8199510c028a09e665362daa79abd192f11c82808a162e1fa5089`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:56 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:36:56 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:36:56 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:36:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a1e7dda96d5bdf74958aaa6a8f7408941a8f152b76ac8e3fe94b59289b4df4`  
		Last Modified: Fri, 08 May 2026 19:37:05 GMT  
		Size: 49.8 MB (49832099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:85d6968d64c0c80dcdaa6a2d412d4d431c2dff897e4869284346474f1f56d2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd2e322855c7cbba99a22dd6b1e1412e2eb8b479f72a198bef67d2a2ef053f4`

```dockerfile
```

-	Layers:
	-	`sha256:afed44d8e2737f6daad08f5d1df11d1212211da7ffdf518e0b44bba8592ad594`  
		Last Modified: Fri, 08 May 2026 19:37:03 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:f2147598fece9cd8a9bc5a2c232b44034a02c7c63aa1151331ea069a60c7f200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80197506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8be5176e61cb45aa47232c02d842054cda9d8344fbafa97d0a9cc4f40b984d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:54 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:38:54 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:38:54 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:38:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949f9e5861709fe0cb78dc094d495f0737931adc3b612ce9dba04761ced80f3a`  
		Last Modified: Fri, 08 May 2026 19:39:03 GMT  
		Size: 50.1 MB (50053864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:453669315818d8b90af2e74afb0ae9e631b86948a1f67ca102cc228591e207cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96948fb09360aaac102b94ce4769a9a94c6a10dfa74d0f8c0dfef25eeea653a`

```dockerfile
```

-	Layers:
	-	`sha256:8af365cf99d6758bbd69fdba5c7fcfd2a8be0182d42a61ecdda767b618cb9177`  
		Last Modified: Fri, 08 May 2026 19:39:01 GMT  
		Size: 9.3 KB (9278 bytes)  
		MIME: application/vnd.in-toto+json
