## `azul-zulu:11-jre-headless`

```console
$ docker pull azul-zulu@sha256:f4282f2121c5f8561304b0d0b8cc681bc70453ec5c402e6ca4c328b12f083d2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:421a6933724143c94f15ad0b904e7ac986660daa8b05e53b7ee65f9ac43415df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94762647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bad42a06f84d10819d101a67561c7da750e0c3b070dde7ee641a77d6dd7036`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:56 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:56 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d3c2b0d4e575b8817df04107c1f24b68321ba9d9bd22021e44c9c2f8893c05`  
		Last Modified: Tue, 17 Mar 2026 22:12:07 GMT  
		Size: 65.0 MB (64987147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:789511aac0a14ca88568aa1986c77d8dff1fac48d2e8a437ad67f5bc6ff844ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc58cb3e2785c1219422754fcf45bf10f3879a8c45aa7e9f0cf1c523fd2d4c8`

```dockerfile
```

-	Layers:
	-	`sha256:978b5ca9f55b7d8ac5e15bc1d63e73de64f78b7d8ae2581710cb2f85ab80a035`  
		Last Modified: Tue, 17 Mar 2026 22:12:05 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:4d26a5b6278eef17fd822204fef744bca5fdd729e42580a9dd814bc740f44859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94926274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2828dd5217ab1670b7c2eaf24949a923cbd4e7d5c188df6ad65fce33e96cb227`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:56 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:56 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9797bc5223ddc4007d828d48626739a02eadd4065cde51aee57f1001069adc`  
		Last Modified: Tue, 17 Mar 2026 22:12:07 GMT  
		Size: 64.8 MB (64787858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7407633ba9fc193c77e7798121f674577d07d5db81d8ddd810dfa17df769282a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4a703b617b461c562021b062bc81ce2052c04c1b0f625ecff1eb56c196fb10`

```dockerfile
```

-	Layers:
	-	`sha256:4f6c308a16edce7ae69f7caacdeea3e5d50ede2364fddad8810b9509135b1d0d`  
		Last Modified: Tue, 17 Mar 2026 22:12:05 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
