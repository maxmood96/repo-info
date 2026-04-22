## `azul-zulu:21-jre-headless`

```console
$ docker pull azul-zulu@sha256:e33168ebc538b9660170a182869689ed05c373bf20c6cd33b639e8b9b720db03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:de76745f16f0616efd2762af95714e06898481c849c8b37f44c1c0d32973ca06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104604668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963b4827eaa16483180bbcfa39503028cc9320123d7517bb7534cf7b4f8b99a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:37:56 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:37:56 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:37:56 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c704f2182ff851e0b096facaed323327a58cb8b1c33e14eb58215894786445`  
		Last Modified: Wed, 22 Apr 2026 01:38:08 GMT  
		Size: 74.8 MB (74824494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9e2df799d8c79afddc4579969514fedbf82e6136bda31121c5852a143e44fd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0159b60ff2124f227ef24f51c6e2b9c997ba95d298a062b823e9424e43956538`

```dockerfile
```

-	Layers:
	-	`sha256:a01218eb43e45156b7fe2a1668d94162eabef08133a16906f0c2485a1bad2e9f`  
		Last Modified: Wed, 22 Apr 2026 01:38:06 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:9c76120668f7c3dc684d57d6956266dde318d30009873988cd48f9c9ced3e04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104636158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a529807e8c76749088e0380a8f3a0c6a67a2208568c1b5cac1fe60d812e9e92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:10 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:42:10 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:42:10 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:42:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c4e747ba48e8fd85012c32fec98305d2b64506af2c3af8a89c0fca4d102f5b`  
		Last Modified: Wed, 22 Apr 2026 01:42:22 GMT  
		Size: 74.5 MB (74492552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:88f6d4ef7ba65ca40a4a5c8e941e93305aefc3fc911f2447f4cbbd2c4b18820e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31828d735d87069d9421d52d791536d751f913ed5db338330bd6683773f04c55`

```dockerfile
```

-	Layers:
	-	`sha256:295b382bec7e932c410547bf1a2dfe910a620a53d51cc7413bb066fd6f7e11bc`  
		Last Modified: Wed, 22 Apr 2026 01:42:20 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
