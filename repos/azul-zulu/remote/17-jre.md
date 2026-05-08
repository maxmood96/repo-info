## `azul-zulu:17-jre`

```console
$ docker pull azul-zulu@sha256:d757847aad74a1bb4bb2f8ccf74fac089a26bcf8f8e00527f3e86e3d564922ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre` - linux; amd64

```console
$ docker pull azul-zulu@sha256:963e39002adbff65ad7977d1d5fae8c73646f10208a5aa5b21a014a8ff564daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101404582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ba4415362a86d160b570427ad6a04ec0eb4b5448ee6bdbe676fe2581592f69`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:05 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:38:05 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:38:05 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:38:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f76cd9cda8149e6fa9697a9a4b9296bfec2429db37823b8c17a499bce55ace`  
		Last Modified: Fri, 08 May 2026 19:38:17 GMT  
		Size: 71.6 MB (71624356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e7ac015f3485a53f4eb5462d640443986e757aaf5b29b1776e6d16fdbbafd42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfe4f813103ec0463b5822423ce7abe9098f45740eb47cc9548fe88133d2928`

```dockerfile
```

-	Layers:
	-	`sha256:a7feec4aebc778725c8bb9a05448cc35a898b427c375a0af208cef33f141457f`  
		Last Modified: Fri, 08 May 2026 19:38:15 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:8e8deb56aafbc6c7c8aa4be6f2f9cedda299a6cce9b06136c1ae872238558719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101800522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0539cd1e64ca0d71921bc4543c26a3da81d857a369fa67271a6b35883c239c22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:32 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:40:32 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:40:32 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:40:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b90587159cc7671ec2c5025658b0d13b5413dd1a7c179819c4581e334cce3`  
		Last Modified: Fri, 08 May 2026 19:40:44 GMT  
		Size: 71.7 MB (71656880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:08d8c7488edf7c2f781c44c619886d46dd0cb8e1ea02dd2684c1d57ca5eeb058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f64dbbd0037ca5985a774e01bf41fdb4896bea7d6f11ae80cb329c001d131d`

```dockerfile
```

-	Layers:
	-	`sha256:57814bc387d089e993c4d0249b7d336a4b50746dbb42eeb5652117777702a848`  
		Last Modified: Fri, 08 May 2026 19:40:42 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
