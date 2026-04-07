## `azul-zulu:21-jre-debian13`

```console
$ docker pull azul-zulu@sha256:ba6e24991722bf15575118bc249ef683a28a9a134c9c2a3bd1e7d9f27df25be4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:8edcaec8035f3b55496cd90062f8a52c494681b60bca8b7896c8794e78cbb42e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106551035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab04273d3272bbccc50b50020ac519fed43950cb2111ff6c5583d87c88574a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:40 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:45:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:45:40 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:45:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bfbc8343f51c53fef7ca863c38c86415128d7154088042db19a77938042222`  
		Last Modified: Tue, 07 Apr 2026 01:45:52 GMT  
		Size: 76.8 MB (76775395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:835ac833e299c11bbce7c6261f8dc67778974b9e0b1dde4eca2fec6a0e93de63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6f4c12f40cacb552eebb4d8aee22611ce29416241ed888a8727226ba279e23`

```dockerfile
```

-	Layers:
	-	`sha256:8dd1839bff2579844a1d359a9e1c592936d2a24e113fbc31fa84009d683f181c`  
		Last Modified: Tue, 07 Apr 2026 01:45:50 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c48a08282b97aa520383bc2a465e460e4284e63d514e7a29be244b8d56831b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106553089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781b33e9855e1a3f85c958d7e7c42d414a8682c13f79a99b21969d6417935d96`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:58 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:48:58 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:48:58 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:48:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bca1529527797fed0fb9b00f02045250a002f442f3ddd625c0034a23fe3aac3`  
		Last Modified: Tue, 07 Apr 2026 01:49:10 GMT  
		Size: 76.4 MB (76414538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:73cb644895d05a91221e4a7326ee203839743c40dc2c2434d70661a492ae2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba703425b6d3d48b8e9e54bc0cee884ab8f4c777839e937c0a592e2e69c2acb`

```dockerfile
```

-	Layers:
	-	`sha256:618e53ee145d07a95026f37f5cb77597fa72cc7de3dc43d31ac595a0189edec7`  
		Last Modified: Tue, 07 Apr 2026 01:49:08 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
