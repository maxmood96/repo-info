## `azul-zulu:25-jre`

```console
$ docker pull azul-zulu@sha256:c3a0e82963c576c3d670298ca3069582f4ac8adee0faa120d902f2955e01efbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c8373aa04e847f5e05373545e2cee174d3848358640dbb9644e15af7a8b7fb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120829062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094c06a853c4039adf3cd8a29df192de17b1330e0fb60e607c98444d46a0ae14`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:21:59 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:21:59 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:21:59 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:21:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8dd3b330dc5c59e1401d02cc195fb7b811c0c1b35777861e362798bfbeda1b`  
		Last Modified: Tue, 19 May 2026 23:22:13 GMT  
		Size: 91.0 MB (91049136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ae13689f2d6aaf730a760ad1d3a4f422f5d13183ca889b1afeb469b341354e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d577dc3c2cbda2e43ca3dc2265a809b089652d3c36075f24311d6dd0ff2f870`

```dockerfile
```

-	Layers:
	-	`sha256:40a5fc29e55a417ee179247d33b36cbc3af994db314c626c83de5afdcb632db2`  
		Last Modified: Tue, 19 May 2026 23:22:11 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:98b835f4d44b4b684e988622eae56e314ac1b887f823d89e6a0aac1e0e2d47ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120778282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e258974db3751868aac8fea006c9c5772da5b3ab675d5bb35a6e568945dbd43`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:51 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:25:51 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:25:51 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:25:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461e07fe719d0df34533c7ef379d84ddf7f747d48f3def058e45d3139c3b5e36`  
		Last Modified: Tue, 19 May 2026 23:26:06 GMT  
		Size: 90.6 MB (90636363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e81042b00f6156c1def747ce083d521322026a9d99bf1d104ee3e813139b0658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3701242038f5a4e1004c32b420bb53c830f263aed4767ecbf0a7c29bd0fe38c6`

```dockerfile
```

-	Layers:
	-	`sha256:f6c356d4808afff9064ed6ee43ab5a545bd3c2f931fc17832e8ac8a0417e0d4b`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 9.3 KB (9290 bytes)  
		MIME: application/vnd.in-toto+json
