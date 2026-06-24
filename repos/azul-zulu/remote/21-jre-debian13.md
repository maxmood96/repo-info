## `azul-zulu:21-jre-debian13`

```console
$ docker pull azul-zulu@sha256:89f0dd716cfb76c210f228aca42b788fa5a6f4a943af8f59eecf0eeb94e2decb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:9af21e6e206f1f657cc505333aef34fba23c28a3bee78626a729bc857c1e3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106682002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9cc489de5c1a93070c4b6f6caead0cf6bb1b7f634de5ce1ff6fd2caeb150fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:39:58 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:39:58 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:39:58 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:39:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797a220a4954867273216c65379a168211c938015571dcacc0b7f4cf6d2a7a68`  
		Last Modified: Wed, 24 Jun 2026 01:40:10 GMT  
		Size: 76.9 MB (76896583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2ced39935ea0e26e04173ba43d863fb6a0c5a57055a518ac674f9eebf4fe4ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fde87a17dae3f634d4259b833d1dc542d3d968ff23d197eb0a1c0117404bbf3`

```dockerfile
```

-	Layers:
	-	`sha256:f9fbeb4aa60a79119845bedf053d3f6fa78c7039f8472bf4c7214e12fbf8f517`  
		Last Modified: Wed, 24 Jun 2026 01:40:08 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:8aadc9dddd953df403d1c9dea20f3dd1808d2ed6bd2645a318aa911720b75724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106697322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194aaca7725ea6585fa98cf27b175faecea8c9340c35a95b2f1bf32f730fb0bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:43:11 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:43:11 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:43:11 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:43:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72737315687980c8fd56f96f9fc9ad07a2569d945d9f878a62081b6b03edc753`  
		Last Modified: Wed, 24 Jun 2026 01:43:23 GMT  
		Size: 76.5 MB (76548771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:670c200c460cebdbfa54ef670787527008c2cd883ae492b38412244b4fb6a494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d47a1b84a5c759f830f2a078d7d5666c24835b81ee9a82b1a972b20ed96812`

```dockerfile
```

-	Layers:
	-	`sha256:69654220386ba11557d43c28bdae644f5b67a05dbb4ad27c4cb4cf0db007a95c`  
		Last Modified: Wed, 24 Jun 2026 01:43:21 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
