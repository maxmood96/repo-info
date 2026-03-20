## `azul-zulu:26-jre-headless`

```console
$ docker pull azul-zulu@sha256:f68b375394318c100e3a3ec9f921c58bc460817009b560fb96a70c5b990ce401
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:7dda4bf51695286ffba404dff3ec4f42b8ac10bd40837466b194fc5789a82471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119837717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa73d69f551f585fb55af3168c4ecdd98696d19df47f130624ff1cfcb39ed24e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 17:27:35 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 20 Mar 2026 17:27:35 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 17:27:35 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 20 Mar 2026 17:27:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a7713fd122bbcbc967e5d7e6c70de54e2c3d049e1547a64538bdd227b1a811`  
		Last Modified: Fri, 20 Mar 2026 17:27:49 GMT  
		Size: 90.1 MB (90062217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:59238808258b1782444afb28f4c0abc8a173ba6bdbf28b7fe88d8133c60a73b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814a59b726b704311b6e36310e8bdc048b3875f3b7afa88d1ef703d99a21fbbb`

```dockerfile
```

-	Layers:
	-	`sha256:ff31d30349c16899b17730d455d44bb5fc4fae1b8fa85fb4bd19a2cbe26eb761`  
		Last Modified: Fri, 20 Mar 2026 17:27:47 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:92f23d8c7bd3037a2fa8b7ee885a38aa65d648e884b9b603ab4f1bdd0b5a5cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120131847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c6f0d267aa4ac3e3fb8ba4b3c2f368ac417adba3dfdba544be170f1cd11275`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 17:26:48 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 20 Mar 2026 17:26:48 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 17:26:48 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 20 Mar 2026 17:26:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a0a170d0cb47e45a3a3905125c49e4accf8198a3cd497c4a58db429a861cdb`  
		Last Modified: Fri, 20 Mar 2026 17:27:03 GMT  
		Size: 90.0 MB (89993431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4620e4d8ecac5334cdb8354a80883000b5bfc63ff476f4e63bc31d8157297192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f5a3e97d1b5185e381e817587dbedf82c135764bbfabc48345bc4c26b5b030`

```dockerfile
```

-	Layers:
	-	`sha256:9bb3183a4cd6e88cbb4be9c6a0f5e1333e7c4fe90baa410242f9abeb8f83a15e`  
		Last Modified: Fri, 20 Mar 2026 17:27:00 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.in-toto+json
