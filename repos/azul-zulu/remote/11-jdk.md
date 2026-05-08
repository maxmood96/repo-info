## `azul-zulu:11-jdk`

```console
$ docker pull azul-zulu@sha256:bba53c3d3c0e98ff0113078689700733bc7ae27b82c9af056368bb237ab62534
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jdk` - linux; amd64

```console
$ docker pull azul-zulu@sha256:577a6e02bee375aa4097cfa9e035ada56e9382a8e0bac52b0da541feea9762a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178386387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767a5785bcc841ac3c4e68b49577599fedab48753898a12d023011e5ae22366d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:37:25 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:37:25 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:37:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:37:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Fri, 08 May 2026 19:37:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237f072723e382c03caa867f012a5b8fc6b9485b2742438adcdc70a043cd7082`  
		Last Modified: Fri, 08 May 2026 19:37:39 GMT  
		Size: 148.6 MB (148606161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d70796a235f0210e4b920df0aa3937a119437fe51272b398125681360853ded3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37efae952e63bff16d4d1a209ff9cb9c835ade4bfed813b61c5123b2bac0fff`

```dockerfile
```

-	Layers:
	-	`sha256:221532cc6bebbd778d69df32b2010e242e36dd84de3f3a3404ed79c2c36a49b5`  
		Last Modified: Fri, 08 May 2026 19:37:35 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jdk` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:9462089ce4447bcfcd2c821d0b422ea01fcaf536220402c0d5966d228eafa90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178426136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414a156c5479a2af9c45ecfde5868d1c66a819eca80d5bf68417072de861df8e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:39:22 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:39:22 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:39:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Fri, 08 May 2026 19:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae03e82f806f79cf800b5955642aac67f07dc3ac0244f182cc1c856deed79544`  
		Last Modified: Fri, 08 May 2026 19:39:38 GMT  
		Size: 148.3 MB (148282494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:54b86ff102e6325bcc765b24ec3fc7f5ab447dd0ceb0a27820125d87570c4a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d862b4ca525839f80863b16eba05b23bc3211077f47f55b76de25032effe77`

```dockerfile
```

-	Layers:
	-	`sha256:8e2ef7668a9b19a02f8200835ac2c5f9f9c304e9d2c7a789aa2413948cb0e44a`  
		Last Modified: Fri, 08 May 2026 19:39:35 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.in-toto+json
