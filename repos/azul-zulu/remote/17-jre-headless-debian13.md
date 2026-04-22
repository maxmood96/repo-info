## `azul-zulu:17-jre-headless-debian13`

```console
$ docker pull azul-zulu@sha256:2e18e88f209e7b5238dd42990ef101bd6d5fd82fbfb020b8657329b40b95e846
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6418b17d1f66b21456bbf94a4bd15328a4deb894d1160b0d3ec39beb41b0db1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99308592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ea064a1d9563aca4a4ac7abaa0675dda5a272c4c84a0c12d89c15b0bfa97cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:37:22 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:37:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:37:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:37:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55df8b3cb7ee4c05ae1ff90424c001f7125a4b47bb4b73b562a726fd66a28e0`  
		Last Modified: Wed, 22 Apr 2026 01:37:33 GMT  
		Size: 69.5 MB (69528418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b791915766aa2519ca58a16959fad41f9e06cb5f5b82e26d071115eaaeb2ed2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bdeb5b6f996372a2c08dd165aeec39d8e372d0ee307ba47571b906ad599977`

```dockerfile
```

-	Layers:
	-	`sha256:21443ff9b4ee1439763171f06f4fe977aaaf53d31d8a788682f8fe3e6bb400b0`  
		Last Modified: Wed, 22 Apr 2026 01:37:31 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:2971cf350a3505670a8f7b8fd6557b1d6ad9c7dcfd1a15fcd573b6490001ac98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99728075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716029a20f715dcd9e445aac6667ffe8b1d5cf9fe77d1458cdf082d81e654fad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:41:40 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:41:40 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:41:40 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:41:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a565ae04eb7b1a15c3bffa05851772a330062b96f9e27f187294422c34aa2`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 69.6 MB (69584469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3159bc3a928bb1030c43e5ddd2077ed45548ff4cd600c2ef0fb61882689ca018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6166e1ba7ce0821072844a033c8cf2ee7551076e9c0c1d16a916ad5edb48b099`

```dockerfile
```

-	Layers:
	-	`sha256:3e53cd1dd59fabfb47485c17693badbe9042b4e9df4bb532f008949777a14938`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
