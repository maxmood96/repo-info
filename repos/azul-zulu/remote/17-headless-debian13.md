## `azul-zulu:17-headless-debian13`

```console
$ docker pull azul-zulu@sha256:a4279fa09517fec7938cf53a01e6a3f8dc6ca9a795cb75dade85c88e2093750d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:202c93427676f421cdac7096d20a6f958223671a8a8737e2493adc91e354e8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180303310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7502f7154fbc0e38063353e7f31b2823817f499d1b20db0cfa625749cea94c2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:47 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:39:47 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:39:47 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:39:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Thu, 11 Jun 2026 00:39:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec6a0be7a2c2026fb5f4a5da8cfd29155f05d8f6bd3f44513cbd07a436e0721`  
		Last Modified: Thu, 11 Jun 2026 00:40:03 GMT  
		Size: 150.5 MB (150517895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7a57a4bd7700eb774df24f1b68f4688e9e24f92eff9b5e853dcba11482f36abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0240e02c2f083b7a409bb52d9186ded13768f4fdb066214c0f7fe86b72dfc3c`

```dockerfile
```

-	Layers:
	-	`sha256:9a220944be83ec0fb0f977741d648753b7d36e73fc41ec5725c433481ec0472e`  
		Last Modified: Thu, 11 Jun 2026 00:40:00 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:2aa6438c2dd0800dc484283f6181624fab3057b4f7b6136467f3eebecf00974c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180706993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77496a18472e7b194715d053c55a4e1ca3a6a4d5c4f271bf81601398f6268fc9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:41:24 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:41:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:41:24 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:41:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Thu, 11 Jun 2026 00:41:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2c5d64ffc2073af65c9c3301e7f3992fb7091f2e4e680e051d574397520851`  
		Last Modified: Thu, 11 Jun 2026 00:41:40 GMT  
		Size: 150.6 MB (150558463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a72b2896062597ae979f3dd15e8207d0c0ee821b652cf3766836782ceef7079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b18d513a78bfe3bdf4101fad9267e0c9c435b0e9fda71c04bdf152e941fa8f`

```dockerfile
```

-	Layers:
	-	`sha256:19ff798ae4e72c3ab5e931eae1b1ef541f79ca4e8c33bb8ad1f864641804c71c`  
		Last Modified: Thu, 11 Jun 2026 00:41:36 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
