## `azul-zulu:26-headless-debian`

```console
$ docker pull azul-zulu@sha256:4fdc0d3a590c19c5f868b8a45e27c91b11e9cd8c670d52db94e605875c36ae53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:9c2c8d9dc2b2ad35b9977a58619ee58fd2a3cf363e28d06deb79d55b71579f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215021091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bb18c837bd6f94c2c8a33ec4d40e4ae141998591c494fcbfd7b6cf67128722`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:12 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:40:12 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:40:12 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:40:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Fri, 08 May 2026 19:40:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07551ba2ebd9ab2f6d4fce04915e970060aef237e142f0bdaeafa43f82af5b45`  
		Last Modified: Fri, 08 May 2026 19:40:30 GMT  
		Size: 185.2 MB (185240865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2efb15ee55c6ceefaf0e84401b84f8780c731a1aa13e63d5320bf9d67dd0b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029be369155c8d3ee6d1aa12a7ccef6f677708f2d98da1054e51a5fe3f6c8a7f`

```dockerfile
```

-	Layers:
	-	`sha256:561a978e8b43626d45d9a2af09ecad0df3ce209f01a018b7490232297db809e9`  
		Last Modified: Fri, 08 May 2026 19:40:26 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:65e461ac7693ced7031b4a139b9a1ae8218ab3081d525c1a3c5676ed31e64bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215090347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0790da1ed0cbd9ea964a489be8fc9a3335c71adf8af9cf4ad53cef69312f34b9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:59 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:41:59 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:41:59 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:41:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Fri, 08 May 2026 19:41:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50befee9ce61dd700bb6dcd31eade474b248386e99a433c4a92933d9a7d5f46`  
		Last Modified: Fri, 08 May 2026 19:42:19 GMT  
		Size: 184.9 MB (184946705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0efa446a7e494215c7fe434cf6f089085a2323d378284b5aa7b949d3c1af7c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06e86190b945181199afbdee5388e5d2c0f8e0924845c41ad955356bef3d054`

```dockerfile
```

-	Layers:
	-	`sha256:22a7f3b9170d07dbb36190a8f9249718fe76b5adcc6fa38e903d128f87e759b4`  
		Last Modified: Fri, 08 May 2026 19:42:15 GMT  
		Size: 9.4 KB (9399 bytes)  
		MIME: application/vnd.in-toto+json
