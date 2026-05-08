## `azul-zulu:21-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:a8b4ebc4d017e4532fde6fae4c4c8adb2ecb26926b21521f31c35fb36a1f2c54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:2e94e9a52deaebc3754a65b122e5b58ffd8bda8cb127b097e02ae3e45d2a2cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104604887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c76cb1d579bfc1f251163c6522a95a857162d41c21c0bcb77145dfcf7001e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:53 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:38:53 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:38:53 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:38:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2a044eb4608d651d1f2ea1f474e7967639b383a8420b15ba32ab663d5fa264`  
		Last Modified: Fri, 08 May 2026 19:39:06 GMT  
		Size: 74.8 MB (74824661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:758d44e1612c57853d845e0cbbc23403bdfc3d26df42d6a5f30a28ba31487203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca94c03a6266da1a945473beb4329d3921dc992f8e402ad67f25f79eb82a212f`

```dockerfile
```

-	Layers:
	-	`sha256:7182ca4ff4e1801c02ac403c75e42ba187876a58b56948d1b1f4851c092059d5`  
		Last Modified: Fri, 08 May 2026 19:39:03 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:8fa78609c1ece74442e93ee433d8457606414ebbda5ef22f8e700d9b16089700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104636095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b79d70745cfbf2d252402c88a3054c9479cb9424036bc64e28e89f1ab0a2246`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:16 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:41:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:41:16 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:41:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da410aace126290dee959c96ba7233f277afd228f4f3a1f3a52550d772f3c457`  
		Last Modified: Fri, 08 May 2026 19:41:29 GMT  
		Size: 74.5 MB (74492453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:fcf7b0ac4a61fbae1217204cbfee762381c9099f3934d004d79079d48c736e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67bd3324ff80e22d0d4ec92879db38f6c20ea7622540493f6b7b9eac36215f2`

```dockerfile
```

-	Layers:
	-	`sha256:aea37b04001aebf67ab269c8210b0050a4b0b64532defcc2f6ca1754069e6741`  
		Last Modified: Fri, 08 May 2026 19:41:26 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
