## `azul-zulu:11-jre-headless`

```console
$ docker pull azul-zulu@sha256:3fcfb1b0f7dda3dd6ae295823ffd0fb9ac8889b1a714ce9bf2aa4c043f6fa471
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:b74cdfe13a1bf9c928745c9544178ecbc4f592a280a81167b0655cdafb3a53db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683d88d0e8610dc92a4ce364b8f0a02dc33d731235894ed3d38603009ab1b129`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:38:57 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:38:57 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:38:57 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:38:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0224cd4b7ab973e7eb4f6515d32f09b441f0177002dec9d61b45631b2bc738a8`  
		Last Modified: Wed, 24 Jun 2026 01:39:08 GMT  
		Size: 65.0 MB (65044381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d274d13cb03700c1032f361b969487c3af737ec23c361d3d5ce4405caaa8ffb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b3230929d92e8198ef46e3c41cbf0249e13165cca982717b7b23160385a88f`

```dockerfile
```

-	Layers:
	-	`sha256:58c5ba14f0b9082533769e29daa5e3e725ca85a7454f17bc7f2f3d0608524384`  
		Last Modified: Wed, 24 Jun 2026 01:39:06 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:d61cc2cf30b748886778c4a88df21e8abb784e0eada66b4217c25dd6314db20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95032616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e5a35b5c30e0efd09e5a0cc0071df087a580d9278ca11f3fdba61799dfe23f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:25 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:41:25 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:41:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:41:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d7e1252357fa3bf8764e705dc81cdfd4af0010d02bed31db2a01d073cfb6c3`  
		Last Modified: Wed, 24 Jun 2026 01:41:36 GMT  
		Size: 64.9 MB (64884065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e3233c87d8364b735d567a00eca341ae559b7f3f755d9bafaeb6598c7e356e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e3d96b2dcb7ac0cdf4e9ef73481030a71604e8ed694a6950d2aee0f54100d2`

```dockerfile
```

-	Layers:
	-	`sha256:8e4fdf76b142257875e48e360f59ee9b6dc7ffa79c46cd940105f5fd8c46d8e1`  
		Last Modified: Wed, 24 Jun 2026 01:41:34 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
