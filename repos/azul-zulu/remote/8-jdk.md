## `azul-zulu:8-jdk`

```console
$ docker pull azul-zulu@sha256:1d8daad03f7dcf9b079cdd2cf670a8b5e1318dea31f0d92166dbbfb83be1b603
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jdk` - linux; amd64

```console
$ docker pull azul-zulu@sha256:1f8f6dd6d112fb7a8504880e5a8ad786918800e7d46523a3ea861bcb6f58f9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91820444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07520ff1200a72c77d33ed313b500f40382314930cd0609fb3352e9939e99ae3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:45:58 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:45:58 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:45:58 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:45:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b15c843bb499ea2bd0111468ac4742e898ec5d3691f2dd21685559210cdd17`  
		Last Modified: Wed, 22 Apr 2026 01:46:08 GMT  
		Size: 62.0 MB (62040270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d57056c92b5aff1654a21af68cbea321161f03ffe0aa22d117386612db2b412a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc653625ddf910d4a97f09958f40ebfe37718862857af3c2876fcc2f070d602a`

```dockerfile
```

-	Layers:
	-	`sha256:dc36de998e4b241a26db60cd76853e2c32ac52dfa09420eeadec5578f814b42d`  
		Last Modified: Wed, 22 Apr 2026 01:46:06 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jdk` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:6ca4840810ec47e0e44f5329611af8b07d16db75b555793a89bdefa15dfb2e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92504408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3f9d7567ef02bfd7e055bc28e3cac9908f2f8ff05086484e788218039f47b0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:18 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:39:18 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:39:18 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:39:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936ef5866c1f75845a1098863dc16785ee18e76c0745ea3f1d8e853ce96dc5fc`  
		Last Modified: Wed, 22 Apr 2026 01:39:28 GMT  
		Size: 62.4 MB (62360802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8b90026904cb735c9e3dd500060032e48ea7a4ab84773a24b2581d43801e54ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4031a34cd4444fd65961c8bc83f2823792c17f4ad8c534a2ffcbaf9c7896bc`

```dockerfile
```

-	Layers:
	-	`sha256:0ae9e0af8ef19d2fc9c47718d88759fda5a11e242ed6e30475adaa945db47bd8`  
		Last Modified: Wed, 22 Apr 2026 01:39:26 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
