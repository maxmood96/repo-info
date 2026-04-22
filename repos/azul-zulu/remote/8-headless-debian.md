## `azul-zulu:8-headless-debian`

```console
$ docker pull azul-zulu@sha256:04dabc2f139df4df3d25d8b7efb210cf62349bfaa3ba9f980f5bc05286068dca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:2f4fe8fa8a3de28374e4083fc9ba1a2a895d8473550e42f9ee948ec9c832fdcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88928100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150ae575f7c3d701a9e1930f419fb79fb2ad078ccdc8a2fa483dc07e7f47b534`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:35:30 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:35:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:35:30 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:35:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d241626a81c7b4da3dd663843353be326748725d2072cc3ffaaa906bd1c195`  
		Last Modified: Wed, 22 Apr 2026 01:35:40 GMT  
		Size: 59.1 MB (59147926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ae92d678060933f8420cedafcc31dd44b05bcd4419a3c9a32cb26fee113d1394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a1f07c0725b76f44be4217a2be67ffb5a51e49adc873282d151d3ee8b59e24`

```dockerfile
```

-	Layers:
	-	`sha256:bc38760070eaa12346283d6d995eecd52759ba6ec8300d5977e7531dca9a00d3`  
		Last Modified: Wed, 22 Apr 2026 01:35:37 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:3ea1ec2109be43d5efcec6ecfb6c9b3541e5f737ed428c0afa4ff0a95bd1ab22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89620134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f53513665e472fc8c7468804ce3c253e4265cd56c926a1c57e47891152a801e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:58 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:39:58 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:39:58 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:39:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62b7237694bd01dee543840ac51c0d0d8465bf9ebbf62dac30061fe9919f347`  
		Last Modified: Wed, 22 Apr 2026 01:40:08 GMT  
		Size: 59.5 MB (59476528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:438bdeb52b2e25363cc4f3d5f98b5f703f9c2adc30a4c3aecbf82f870370bce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95199458f1783c561dc07a84d0c88c46c150ec595be97151f80f7896679ee93f`

```dockerfile
```

-	Layers:
	-	`sha256:4030f5d356c553822ec94d318503888196f1c03541e5b4fba510e071e4b37c0f`  
		Last Modified: Wed, 22 Apr 2026 01:40:06 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json
