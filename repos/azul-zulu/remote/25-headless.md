## `azul-zulu:25-headless`

```console
$ docker pull azul-zulu@sha256:bfcae7e8b9f697776f3a1fb4e0b7bb66b175abbb6ce880564217beb4fb94b7ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:e9374fe09a6ed95bb96757827ec5b29ab05dbe5ae861299536c879d460f6d777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212684005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdce87e42c349e944c3045dc5c0bd9f499fd91d4fe32af1f3a3aa640758c02b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:22:01 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:22:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:22:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:22:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 19 May 2026 23:22:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8d6fa1982494c34feff34d776965bf8dbab2d6aad863be605e71b575f552b6`  
		Last Modified: Tue, 19 May 2026 23:22:19 GMT  
		Size: 182.9 MB (182904079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:990afc68327a7e853d6bf8ee65b5bd02968e717ebe08826e82719c95a0b246a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc80b8934012ca3b505cd533eefb3443048aaea56c90f66555be42673dbf1956`

```dockerfile
```

-	Layers:
	-	`sha256:fdcfde0ff1c3ab92ef98c72ef00ee159f25ead4607de062a263b827cefb16803`  
		Last Modified: Tue, 19 May 2026 23:22:14 GMT  
		Size: 9.3 KB (9295 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:bf80bdb10677c84c1fb19558f5e76760829873187b64caa439ad4652bc532bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212197092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0cefff06c6bc184acc083de1cd7ac52b497da868393cc8506b8087837e9455`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:54 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:25:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:25:54 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:25:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 19 May 2026 23:25:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2be2268d9482be0365872788d43c0e1df40b3890ee223481b26b0c203e5d3a9`  
		Last Modified: Tue, 19 May 2026 23:26:12 GMT  
		Size: 182.1 MB (182055173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:34eb303d49f0aaa4ac050fe99313f6f22ea2495bd995f8aad6bebf1fb40a3238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695488d5cee8f757f6f47559440340eb38cab07bd05f106b1a7670f4dc09a86e`

```dockerfile
```

-	Layers:
	-	`sha256:4e4d21df7c293c2d8467f06739e17e3d26ce5c38b8bf28070216a678fa1781ca`  
		Last Modified: Tue, 19 May 2026 23:26:08 GMT  
		Size: 9.4 KB (9399 bytes)  
		MIME: application/vnd.in-toto+json
