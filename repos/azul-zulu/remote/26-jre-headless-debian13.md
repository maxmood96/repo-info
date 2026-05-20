## `azul-zulu:26-jre-headless-debian13`

```console
$ docker pull azul-zulu@sha256:9e844868258edbb40d4a890cd4f515c32fd6bc0bef994b393e403cb31ae8c376
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:9bdafb02dfb1fe0d911f3f8222a760de2e9dc94d75cb181532ee097f0bca51bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119912799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84e703cffc0e064163cd1e44f028b31ad4c522870ce8606e2d8889912e86523`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:22:44 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:22:44 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:22:44 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:22:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d5d67613d94213965009b26c21c94d5fe413c9a90bdd0d2264f6128af84faf`  
		Last Modified: Tue, 19 May 2026 23:22:58 GMT  
		Size: 90.1 MB (90132873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a48b8e8c68d2cc37695b3eca37d7953932e78f264cf23d1eb86a5fa32dc9c1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf95aaec069ae50323ed8d003be4b0086ba51726bf261182d3c50a807419b86e`

```dockerfile
```

-	Layers:
	-	`sha256:1e6aca49c5f8e5a97486e32b6a1244c2b09de62d7d11f268a7ca3e7f98d8258a`  
		Last Modified: Tue, 19 May 2026 23:22:56 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:dcd596820d3d8cfb843cdc35a8878110ae9a539f07823878adfec50c2d0b076f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120201430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2e0608ae1016f211021e1ddfe7a198c647415fb2b834d45ea95edb569d47f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:33 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:26:33 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:26:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:26:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514f66ee83e65595e503120b18088e9f496d562b1c3d2cc56b92fa2f820b9beb`  
		Last Modified: Tue, 19 May 2026 23:26:47 GMT  
		Size: 90.1 MB (90059511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:acf692b7c1c1ca546255f142405ae424361ccd29d0633ecae466b419d867d882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b68bf6d9a2a583c96024f5eba33d2b2460d25e51fe81b13f8ee41c1dae63a0b`

```dockerfile
```

-	Layers:
	-	`sha256:c7c434dfcea686e50e98c7a421543c3bd584dffbdf7de9411b2fc8327555a1f0`  
		Last Modified: Tue, 19 May 2026 23:26:45 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
