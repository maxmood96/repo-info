## `azul-zulu:25-jdk-debian13`

```console
$ docker pull azul-zulu@sha256:8a49de48fa5f213181c1060a03241ba969e4c1df53732d54f555478b27aee962
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jdk-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c4c04ef0c76025d7bf608f7282da5cdc9eca0fe349b4b2e29ba9374ec1ce7ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214948232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e624b670a56b4379e7e5f96cf26b372a56be85560a21db24e612d49cafc6df0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:39:30 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:39:30 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:39:30 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:39:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Fri, 08 May 2026 19:39:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2e42df414b150ce1ec508d5049ce1fae696a7dbc8f747dcad7d80cd3679474`  
		Last Modified: Fri, 08 May 2026 19:39:48 GMT  
		Size: 185.2 MB (185168006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:066062c5a65ed6d0e32c43f9cf45c39a996d6ab856d2cfa0ff2f4d45d2319827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a6261e8965ce43af8a231e75bb3fd864388cd6516d9f8a2e28c77e086acbc5`

```dockerfile
```

-	Layers:
	-	`sha256:dc495a01f7f299d4c82c76d20958e8ee6a568b6b0c5ac6f34429f3cdc90c7b62`  
		Last Modified: Fri, 08 May 2026 19:39:43 GMT  
		Size: 9.5 KB (9504 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jdk-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:0db43c3da8f07a9e926404ffb2cdc8f331e5a2ab0ea4b93b05df64c14a7304b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214449164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ce7560398021f4c08c9a2b56c4cbe665b96064954350724ad209c87da44b76`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:49 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:41:49 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:41:49 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:41:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Fri, 08 May 2026 19:41:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e72e8a9576f65875f373a2f585ccfac7486a707afafae4c610de60d9cd022e8`  
		Last Modified: Fri, 08 May 2026 19:42:10 GMT  
		Size: 184.3 MB (184305522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d239c6dab06d4904fa3f921a4e938011013478d881beb1b0fd980cc818746c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3d7b1abf14249fcc8c9ba6bdd5e36accc557f5efc49e833e374e5644d60340`

```dockerfile
```

-	Layers:
	-	`sha256:00f745ba135772990a7432d669605ccbad25157db5e012f80a45ef578d1a673d`  
		Last Modified: Fri, 08 May 2026 19:42:05 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json
