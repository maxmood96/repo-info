## `azul-zulu:8-jdk-debian13`

```console
$ docker pull azul-zulu@sha256:905ccac1b6bd9b246ff930e77a2af98555765569df52a5a880a75c84c6fd0812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jdk-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:96abc0523bf51dc400adc4cf5d52ef2a0d466d8a5cb092b8862f883a392006c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91820771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca61d6ae4c97c8c85d28f8b179871ae148f1db556132bd79bddc98d20fa94f05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:22 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:36:22 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:36:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:36:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd6a71e369495d2b33b59be56f151edc5969bdcc17725c4e66259b9763e1ba`  
		Last Modified: Fri, 08 May 2026 19:36:33 GMT  
		Size: 62.0 MB (62040545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7addfc1d5f04ccb28fc1ebd1940307f93d6e17f2599f36fd35833fcb763940c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d715fe1419e4a550932e430241e407e6855ad6e99c3c4a4d662a33c3e78cc1e`

```dockerfile
```

-	Layers:
	-	`sha256:6c6cc7156de32e2d42a563febcfdfcee1ff897ef706158e896eed47da895284a`  
		Last Modified: Fri, 08 May 2026 19:36:30 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jdk-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:6dc24abc7ec13491651f5ef2e15dba7cdc74d379a752cf9d63ab063507f8b1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92504071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5fd61dd0bd537ef71ad5a366b8e5af02ddb94c4c0b3d78c3f0a53f89f305e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:28 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:38:28 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:38:28 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:38:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcc212a03c2853e7529ac8de9c3b0a339bd25d74c5c041686b64d98a11b118d`  
		Last Modified: Fri, 08 May 2026 19:38:38 GMT  
		Size: 62.4 MB (62360429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d2d10b343ad77381d8873d3fc75b7a78937b40b555f42b2958c175cb44c3226e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884e4853362387d8a91cf0da50fa00290e7637c70d3c90691c3278aa8ea7a6fe`

```dockerfile
```

-	Layers:
	-	`sha256:c05ee65cd22278a07420ca3816ae02044fea8832073d44e1fb14e828959c1ae0`  
		Last Modified: Fri, 08 May 2026 19:38:36 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
