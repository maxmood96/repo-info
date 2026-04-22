## `azul-zulu:25-headless`

```console
$ docker pull azul-zulu@sha256:337e7fcba9934ba7957b478baa390903dbe0f5f103416569a792fb5f99b499ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6f80f6adecf79b39a0cdd31e7380f960e3ee3d8e936d9a5c05d4f3e20375c5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212683567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ec7a4b01f39f082e02b5b88f9def1e4ad4bd24a9c01a0eb978ce1c11cbbc52`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:34 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:38:34 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:38:34 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:38:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 22 Apr 2026 01:38:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78fea3bd1fea525677a5852628e35cad1e66bb0ceef957a4526f71b0753030a`  
		Last Modified: Wed, 22 Apr 2026 01:38:51 GMT  
		Size: 182.9 MB (182903393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9bb15ad5a8999c7f7edbb6620f7f1fbff9762fe81f92cd561829ace421f9a226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3708a247765dc521fdbd121c0f618b2b7aac7bd54cb5668f5970cc7b707ea3`

```dockerfile
```

-	Layers:
	-	`sha256:e7126f89cd53881ee72431a0a8c2abe54d9589f39b85ed7936f24b81bfa9b314`  
		Last Modified: Wed, 22 Apr 2026 01:38:47 GMT  
		Size: 9.3 KB (9295 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:d5a5ffef343b1f50c9ccf5d53288fdc5950c96cfe110ddd0e28b6ca02eb217b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212197276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb28f30ef2b1943e4c48e2f653af7e1a29a39c4d4fa92173764005d586baecb6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:23 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:42:23 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:42:23 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:42:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 22 Apr 2026 01:42:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71e8ce69badb031ed0dec8f622e27236371ccab72370e6312170b8537632b4e`  
		Last Modified: Wed, 22 Apr 2026 01:42:43 GMT  
		Size: 182.1 MB (182053670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:27592560c71a49b7fe9162c9270e77656121728c681406e5bdb541934124cfe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c084a6084a6d373988f4b744bd7e78b72c5c20f21a9ac8d57baba02db860e4`

```dockerfile
```

-	Layers:
	-	`sha256:320cadcf9f204a3b687f53ca4bc0e65f24c8932b86d6ee1e12a8dcb2af441736`  
		Last Modified: Wed, 22 Apr 2026 01:42:39 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json
