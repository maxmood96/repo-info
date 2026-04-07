## `azul-zulu:26-jre-debian13`

```console
$ docker pull azul-zulu@sha256:85b9ccc5602ff008cda937504e5aacd4e6809699c5273c7d9d2ba074d887606d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6d4508995d86a45ed495ac62338225226c0aea08941bb81d0c55987f577d80a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121839537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929acc3fd88eebf8896cbd4ccc6f1a05b7a5ec87f965110c89e6745973e0be06`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:37 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:46:37 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:46:37 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:46:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc5ba9524cac933cb7e4051ec84973746a21b9921390fcdf397897336882abe`  
		Last Modified: Tue, 07 Apr 2026 01:46:51 GMT  
		Size: 92.1 MB (92063897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1bab971b67eb75cde8c79f2e6c20ad43a137d2361e70f0b56fbccdbf6bf7a794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce0a8b1a0960f6abb617aa33eaee2c9c6363974199a70878cf5a3cfcbf4b360`

```dockerfile
```

-	Layers:
	-	`sha256:acbde349412346a0eb43b1a450848612ffdc4f0a5446836691ff3b962d8e4774`  
		Last Modified: Tue, 07 Apr 2026 01:46:49 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:e957b80778df0a436368c1fa51ef3b8a6bedc50bfad3e68a8b2c45266b8fb100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122112193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7640260d7fd0c7ffa146bf2ff61e64a116e7e2f8b5fc62cd53d5f55266c5ed9c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:49:49 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:49:49 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:49:49 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:49:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e184966d5e660f5b27ac29ec3313b9ef53326cd44dd31c298627cff824d85ad1`  
		Last Modified: Tue, 07 Apr 2026 01:50:03 GMT  
		Size: 92.0 MB (91973642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7da0ac20f62abdeaf79c1804c475edd78b01442fa3abc2204ff86a1b244fa98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04f32947b2020f274d0cbc050066c58a393e7a03f5ad48154718b9c12783d3d`

```dockerfile
```

-	Layers:
	-	`sha256:a8c0a2cdedd18f918c136d5afd4ea6d162e4bd038bc21c579ebe2b57786c0504`  
		Last Modified: Tue, 07 Apr 2026 01:50:01 GMT  
		Size: 9.3 KB (9283 bytes)  
		MIME: application/vnd.in-toto+json
