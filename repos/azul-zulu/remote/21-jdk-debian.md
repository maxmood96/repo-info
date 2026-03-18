## `azul-zulu:21-jdk-debian`

```console
$ docker pull azul-zulu@sha256:cd5b1898a9ba0d8c8d73627d35097e142aea1445ab245fec46c9d1b3858301cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jdk-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c16064967f70beac246f6700003b73b5783a493f2bf08dd99cff3bf8a424d3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195620576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac058b43cf8ecbadb349f9df6ca2e9405a4956d22f817285ed1d03773742ca9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:12:02 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:12:02 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:12:02 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:12:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 17 Mar 2026 22:12:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5836a46ed08e704eb541745d273b69ca19a189d0577871f3a2bcaf7d5ef4c2c9`  
		Last Modified: Tue, 17 Mar 2026 22:12:18 GMT  
		Size: 165.8 MB (165845076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:77ffc7ad2d13c14ac843d8c0bcf0b6462cc3e446cf1956ea096d5d3fccc46916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8d8856422087aa41948963b0e6733237b62287a3d73f42643bce71c41ec102`

```dockerfile
```

-	Layers:
	-	`sha256:1e5b6427c2e806a369554a09854fc0e999501808b6a5fd8d880c989f83220be8`  
		Last Modified: Tue, 17 Mar 2026 22:12:14 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jdk-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:360c44a04b443a921b2c11b478f58777476163ac9ab859d5d37a356401761615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195267174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d558a5a646f3806d2199f6fb11ac5138a0ef38e1cdc96f014a6f83f0a8687ba1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:55 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:55 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:55 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 17 Mar 2026 22:11:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420bfb8507395b4a0edbaa54d2eb895c1f7a2991c3dfcadf46943d1f35553741`  
		Last Modified: Tue, 17 Mar 2026 22:12:12 GMT  
		Size: 165.1 MB (165128758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9c427fc896a7a444a18705db9f19ff5092706d4144ba6a8c17c32f010f632a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa47ddc0a999785e69fe02b332553102f9e328afd56dd6aa8658891535f9ca0b`

```dockerfile
```

-	Layers:
	-	`sha256:6996148d006d0d530aae46bcaa1a1c646f37613892306328adc9c9272f9f2e83`  
		Last Modified: Tue, 17 Mar 2026 22:12:08 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
