## `azul-zulu:8-jre-headless-debian13`

```console
$ docker pull azul-zulu@sha256:4c2184f2f6d461345aec3f53fb3955f4fa8cdcec23cda5f2d8a728db5528e53d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:b25e519acf174104862e1800800724bbcbcf1bb51100c81d615b3a61ea864f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77507330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac4da6422ae8a08b9380dbffd776b0ae9380948b7a4c1fbe94e2ccb3d231d8c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:19:28 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:19:28 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:19:28 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:19:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913512984c422b878749e490f9e703c9653b0dcb3780d9689d9a0a3bb7385b53`  
		Last Modified: Tue, 19 May 2026 23:19:37 GMT  
		Size: 47.7 MB (47727404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f62ea78c3fad3e6773a75d178725407ba008b2079411e5dc136af771c8034aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453e74cc2726dca1a2060f919f5c83232867d1bc97e9919698ba6090db5239a7`

```dockerfile
```

-	Layers:
	-	`sha256:b5f050c220a049c5127a567ef029b367c949a5cd8f6387c58effd10e73330de0`  
		Last Modified: Tue, 19 May 2026 23:19:35 GMT  
		Size: 9.3 KB (9285 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:15feb64b8e322a1d7469db36c0dad1408dd5a81570327b3977f3d9a72c8c7114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78093736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01140bdaf2073c3242ad736978b07f916e52d446d7c08dd15e547af150d92d36`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:23:24 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:23:24 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:23:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638cde7520de075371f35a65b56db1ab45d14be96f8818fca69cd14c295d24d4`  
		Last Modified: Tue, 19 May 2026 23:23:33 GMT  
		Size: 48.0 MB (47951817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d184ff2e5894c9fecb102d4b7c6ce0b1ace106cd52af0db1bdc0b0b96c717a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e96a0a40dd840875959c2cfabdc843360d0b98a43cac49fd4bcf0c3f4d82eb4`

```dockerfile
```

-	Layers:
	-	`sha256:96e355f2353711f4535985668aa4fe25457c89d7b00cf4562f537b692287f031`  
		Last Modified: Tue, 19 May 2026 23:23:31 GMT  
		Size: 9.4 KB (9389 bytes)  
		MIME: application/vnd.in-toto+json
