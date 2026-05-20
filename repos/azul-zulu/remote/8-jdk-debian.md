## `azul-zulu:8-jdk-debian`

```console
$ docker pull azul-zulu@sha256:b7961a16e8251b0286bf04575047b5db164765c22e93df5cc25651589405c86d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jdk-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:42b62fc03b88eb57115a3c35c3c82a2c56f096fdf5eb5c014691c4d3cc73d448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91820459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0392b8ad46f879471967e5cb1dbde6eeba2aff8e17a5522da210eb248c50da1e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:18:52 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:18:52 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:18:52 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:18:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520eecfb2201da643ff3194430f89868d7b3870131e72539cd0f347c07cad007`  
		Last Modified: Tue, 19 May 2026 23:19:02 GMT  
		Size: 62.0 MB (62040533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:985cef2e4d3f08ff3a614682e2d9726fde5dc36fba869620e3fe8f924a86760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b4bfd81209cecb4a81cffabfed330c3b643de43676c282202c8327059193d6`

```dockerfile
```

-	Layers:
	-	`sha256:802025eb7d476696ae7d096b0b75ffa7848fb15a83c4eed992bb657161ef715c`  
		Last Modified: Tue, 19 May 2026 23:19:00 GMT  
		Size: 9.5 KB (9467 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jdk-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:3ebf580b721df950a73b088f4617e7276b06c78aac79ded3c8bf8e423f33e615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92502951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e874821df107a50e0b002f1ea49e760155595f97955d014f65c09302832225dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:22:58 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:22:58 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:22:58 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:22:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede09bc84e91173cf440bd5751fad87acf88c264b53ce24952a2dab506f17bb4`  
		Last Modified: Tue, 19 May 2026 23:23:08 GMT  
		Size: 62.4 MB (62361032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6ef50aa62e9c8da4dc7d22cf880077225dd465ef48504243aa57ad11da0027f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53e5c87fce946731b0ae09fe428251c785a505c752945910774d2109807d17a`

```dockerfile
```

-	Layers:
	-	`sha256:509b69e04593c157f6eb809805fdaecc5e56b68478204ae086b54a642a1dc823`  
		Last Modified: Tue, 19 May 2026 23:23:06 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
