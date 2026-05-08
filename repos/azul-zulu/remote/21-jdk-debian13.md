## `azul-zulu:21-jdk-debian13`

```console
$ docker pull azul-zulu@sha256:3fe84ca596668bdc34c36099eea93eb47b53152cc58e68febd97adcc34da9450
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jdk-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:605fee4bf967c7d64c440dba06b652b4b8d4c91b6144c580355ce9b2a8bf6ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195875124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cebea932c1ab6aeeb0eb06d0357c7a6d90c66404f76dd04eb42e3e8b5ee33d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:46 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:38:46 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:38:46 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:38:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Fri, 08 May 2026 19:38:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f17f64193521f3f5e56c0c04c072a00229e9099c56cb2db0892d91a71add7e0`  
		Last Modified: Fri, 08 May 2026 19:39:03 GMT  
		Size: 166.1 MB (166094898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:bcab27d19abc5bcbdb221eb4d3179a56b667fcfeaf3e2eec36697a6bc13c43db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51aba8d95ba207a9ed2c0aa7253e813b68cb799583f561bd1267a24b750af1db`

```dockerfile
```

-	Layers:
	-	`sha256:151bc0a3e861de8eaf265000f3ce4850bc0c4f37ea83b3d24efab7ab7a732663`  
		Last Modified: Fri, 08 May 2026 19:38:59 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jdk-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:15717a4c8171fba079a53b5a5ecb54f74850ac081a3ac972c89a377ad1b44ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195543173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4336fff5c8dc829d2276da34a7a0d73f11df1cc0a53cdaf682b2170a47329c64`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:02 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:41:02 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:41:02 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:41:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Fri, 08 May 2026 19:41:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5ccdd6631c7ce9cbc861473ce090035d924be95a85283011710724b77da3c`  
		Last Modified: Fri, 08 May 2026 19:41:20 GMT  
		Size: 165.4 MB (165399531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a4af6f39bc496445b58a972b2e2adf8bf80441bdcc2f57490901298b08d40f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ab601ba6728c097a73f88c851bc39978f41c5c03a5e5e3a7e5f863dcd069ff`

```dockerfile
```

-	Layers:
	-	`sha256:5a7ddbd91af900528229cc1e2b9fd2987269ec2590e036e237340525e2b4c9ed`  
		Last Modified: Fri, 08 May 2026 19:41:16 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
