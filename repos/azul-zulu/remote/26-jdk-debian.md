## `azul-zulu:26-jdk-debian`

```console
$ docker pull azul-zulu@sha256:fdc4e5febbb7836f00e5f84276000eba1e230f18eeaab690d869fca173124b19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jdk-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:bb66a5fd643995c81c8b248a9d20a6f3c813ce0d6784dddd1a03c2e8b6124933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217092988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1066ceb02b3e84dc3a8f258b7aef10493a075a0b9b8c514be1119dd29ed060`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 17:24:54 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 20 Mar 2026 17:24:54 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 17:24:54 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 20 Mar 2026 17:24:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Fri, 20 Mar 2026 17:24:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e2e10da2f6b19835927ae9344c9f67ddf12bc8eb20d63fa010a8e67189f89a`  
		Last Modified: Fri, 20 Mar 2026 17:25:12 GMT  
		Size: 187.3 MB (187317488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:93039599732e91efee4575e8023d0c401fa5a688edfc2efc2328a1ae3db4e9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4cad873743e903eae6187fbd6431a2249e3daa1cc7050b06ceda673989d40a`

```dockerfile
```

-	Layers:
	-	`sha256:65f59dd201d2ae8ee03627f7d8f25a2c89e35a6c021461dd1a68bdc9e46bcf86`  
		Last Modified: Fri, 20 Mar 2026 17:25:08 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jdk-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:3de1d17246043ea6d74edb134f7e7763554f2812fa7ee12ed50b7ca6d07ed1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217129228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b72349d39dca33e57f6085b30b741ec9aab86ff288ed77c4c1225b4d7cf2e34`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 17:24:44 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 20 Mar 2026 17:24:44 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 17:24:44 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 20 Mar 2026 17:24:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Fri, 20 Mar 2026 17:24:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ad47da874b06e7df50fbdc25f836330c3987880a02ca5c60e34bd035e82770`  
		Last Modified: Fri, 20 Mar 2026 17:25:04 GMT  
		Size: 187.0 MB (186990812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d6dddce03efb9f5bdd6e9df18f395064228ef8c7c69c83b9b682e03b343f6c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cf3d8f2c754c6c2a0b0ec913d5adba79ded65fe462e3fb30e8ae527811b17f`

```dockerfile
```

-	Layers:
	-	`sha256:6c9ca440c9c7e4de4bd3a67913a805664a35e6a2abb6346dca5cbc54de4cff4b`  
		Last Modified: Fri, 20 Mar 2026 17:25:00 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json
