## `azul-zulu:21-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:821c25f36c7910eef2bdd99e402e713fec4829dd4b911d729fcdc3a8f699a114
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:0208f95e11b104e49a22991b91afb33540180ea6099af27e02b2433a62582a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104474204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d641dfe296451f57d32d21b0af4e2bd0b990e0687cc59fc3180c56eda5fcb150`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:12:01 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:12:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:12:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:12:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b37d60d1ff43bcfc47f7dbd3de6979b6b77c82564de649473263bcd73eda44`  
		Last Modified: Tue, 17 Mar 2026 22:12:14 GMT  
		Size: 74.7 MB (74698704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:5bda50e89caa6cfb46c74b7d45696cfc18472552184deb7af14717f86ed7c2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8846d196799ffc3df06cd99c2cb947b0e3374da2d38c2d884493883cb4b3793b`

```dockerfile
```

-	Layers:
	-	`sha256:154a05ab96e901b9ca3df8a84f2cd567f47781602111eb7e510bbf00153bd1a6`  
		Last Modified: Tue, 17 Mar 2026 22:12:12 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:1a829730a89edc7124e39903437106d18dc74dfe0150bde20c525594a228f035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104499377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc0c190c84da434b514b39e58e1a75b28afb79fc5bbfd9e461ceb5203d5cc00`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:59 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:59 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:59 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0425fe68df77b404c769093f93b090ee79b0ad8f6b2a24b80910d6b5f8818e`  
		Last Modified: Tue, 17 Mar 2026 22:12:12 GMT  
		Size: 74.4 MB (74360961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6a4ac56900307b5215f834e96fdfa6b202d5d36234f21332e1011cba578b7a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf98c6ecda2ca114e629b422f16260c519fae743b8310c1d59bffecb519de5c`

```dockerfile
```

-	Layers:
	-	`sha256:b7bb413439a9f8df3b684d6902773b10c384ffa22c654eb3ad80a956ccd103f7`  
		Last Modified: Tue, 17 Mar 2026 22:12:10 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
