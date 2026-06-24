## `azul-zulu:8-jdk-debian`

```console
$ docker pull azul-zulu@sha256:f05bb3a7197552933edf57d9da0f017acc9b699bff4e9fe41c6db92e841315b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jdk-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:4f2b55556355aa3b903dcfc560d966f604f597bb8792904698b568a5dd6fa875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91825928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423fc4d693fdd5b52bcd3303b0ce18edcb9e9abe7f6fb214eea2c6cfa3c98b77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:36:42 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:36:42 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:36:42 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:36:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd0e3d93a625721a3c5530f155650368215ae2c3394621ce7b4e3d93a340040`  
		Last Modified: Wed, 24 Jun 2026 01:36:52 GMT  
		Size: 62.0 MB (62040509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f3620c50b35dd9cbcd509294706db1eee526ba974116f393ab5f4a539b996b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fcde3f69b2f9e167befa9f8b246cd1b1a314ec513b3028ee50d562db73b292`

```dockerfile
```

-	Layers:
	-	`sha256:674e3b8057a481d57d1e942876dcfa3f35cfd5d2cd8544a27b739af6dfe6dd7c`  
		Last Modified: Wed, 24 Jun 2026 01:36:50 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jdk-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:408309ba1b3bae39550fae30f4306fbc4dc2ce5460af5f84885004c176b08182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92509662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9bedaac5c26bfd41d867fa31033caa30ef75fc08ec0282ca70331011943b82`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:39:11 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:39:11 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:39:11 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:39:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f5aaffee2b22c322eeaa75c70e48258c1e4d23fdfcaa59c9e7285ba899b805`  
		Last Modified: Wed, 24 Jun 2026 01:39:21 GMT  
		Size: 62.4 MB (62361111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:af1d448c9e81c6251fbb08780dfdabd69a01b23f98b79fbe73585a40bc0c8fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343d1f65eaca02fa5d3b84c3b68c5ffd34c9da5322b13a880691724c29844dbd`

```dockerfile
```

-	Layers:
	-	`sha256:6bcc5e5dc7365cea84b83edd4e0dac8c20ffff79a8a807251c8841cefb96e9c2`  
		Last Modified: Wed, 24 Jun 2026 01:39:20 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
