## `azul-zulu:11-jdk-debian13`

```console
$ docker pull azul-zulu@sha256:c7ffc5293d099826dd1cdca3b5b9258c855e4d872d3fd7ee2fdc433d5abfe68c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jdk-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:30c3a00dabca94dd376842d2d24742d2d89e127b7435d2c6ddb7990d7fb8de3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178385585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72470da57a4c1d3a5bb43dffcddc32933c9fa3a25098b1620d66a92b2acf4b9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:19:34 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:19:34 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:19:34 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:19:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 19 May 2026 23:19:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d9bb822b161da32307c31f46a44d4339cd40a99a0007b119ce518eab2ab641`  
		Last Modified: Tue, 19 May 2026 23:19:49 GMT  
		Size: 148.6 MB (148605659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:cb45f489dd67a2e6a39d7f3b1d88945956ebd75d6c37e76187b590beda672055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12c3233260b52b9e4d6fe97068a410d456b72c381c1cb121f77b58791065c57`

```dockerfile
```

-	Layers:
	-	`sha256:01120fa0e7095042e2ebe9832b576409ed84b7a63f4d6069f2a2e01fcb17c47b`  
		Last Modified: Tue, 19 May 2026 23:19:46 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jdk-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:707d62e90777973e23e7f9ff6997e635996287d2ff48549dafde520a37725d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178424731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2cc8aed5272adcd7b2e56822c9a9fb8f2dceaa00934e949a64fd8f31940f2d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:41 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:23:41 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:23:41 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:23:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 19 May 2026 23:23:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb986e1e26de61e2a8f97b62f4a4210ea85593937518a59f62b899177f90361b`  
		Last Modified: Tue, 19 May 2026 23:23:56 GMT  
		Size: 148.3 MB (148282812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f979e58cfb2608c2333141f20200bd6df6414f45f9cdadcab4b3ba10c7b54c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f28e50e970840a10362c8997b144aeec1a680e5a486efc6b50bb1e293303e02`

```dockerfile
```

-	Layers:
	-	`sha256:ed74d7563166042525f5dc0bb1b2d4c2db4c9a90659eeeaea2c981b3c4a55a3c`  
		Last Modified: Tue, 19 May 2026 23:23:52 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
