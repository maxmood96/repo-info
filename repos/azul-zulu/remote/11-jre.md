## `azul-zulu:11-jre`

```console
$ docker pull azul-zulu@sha256:2590df32d71ae559259dc055fef850129d8f7654687c4f67850ec70c2ae4933d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre` - linux; amd64

```console
$ docker pull azul-zulu@sha256:2d86d346e60d35d0ca0a40891a4332495b16691f368c0b4e0d2ea99b2813deb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96832639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be2a1b64db1f4193a33ce2346a78e3dcde040284c84b099ba6ab8d4ffd789ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:44:27 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:44:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:44:27 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:44:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7e75c7c6c68d15d9cfc89f1add2e158e648e42a28459746ed962982703ef0f`  
		Last Modified: Tue, 07 Apr 2026 01:44:39 GMT  
		Size: 67.1 MB (67056999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:abf76eb4c5fab2056f6bdb10a71524c72ddb8011e2f0ccc5893fe78a2b187e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2b9c0be3812e47b7d5c28c58fdc289188808030e7976b76336068d7f893105`

```dockerfile
```

-	Layers:
	-	`sha256:966ffb8ce90a7ba50541d331e1aed3d3af02853bfe5e33412e0f53fa3dadf702`  
		Last Modified: Tue, 07 Apr 2026 01:44:37 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:12cddabffcd76dc0aa77002970d6458dfd4b748d8cc812ebf6cc9e09fa98063b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96967402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71781ccef92694615a19e584b32f4dea56ee37f3d90f2ed1cfa7d62643fa47de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:36 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:47:36 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:47:36 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:47:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5eefd7d1c23e818e84a1c85db927c2d16e18f3d44f54d5ec309d1ffff0de65`  
		Last Modified: Tue, 07 Apr 2026 01:47:47 GMT  
		Size: 66.8 MB (66828851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3cc89543f0d13865be50882688cb8defc1e13e8f33701a44970f0f6d394357a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3681bb4f2cbb0ccf90161b8f6d14e3fa64c79ccc0dc1e6ce6e3d0772681343e1`

```dockerfile
```

-	Layers:
	-	`sha256:ac169e4023961689fac0faf630ea2d07a9fad8867f5104ac18d0168a5fe01103`  
		Last Modified: Tue, 07 Apr 2026 01:47:45 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
