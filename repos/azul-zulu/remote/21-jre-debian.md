## `azul-zulu:21-jre-debian`

```console
$ docker pull azul-zulu@sha256:8dd60ece58c96e525992d756eeb90d18102a2cb5b71508b1a8845c9f1ea864ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:d26d30608452b7456a859820f0683057bedd7e89b48b598070a90d3c3d8343db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106676631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f617a15217889e25833b6881203d33536f3a125764c5cae990afe8c8908a3393`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:21:19 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:21:19 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:21:19 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:21:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcbc9638c565c46b5e242a18d8817ec1b222c49f2c00c69d187b145b30a1d4f`  
		Last Modified: Tue, 19 May 2026 23:21:32 GMT  
		Size: 76.9 MB (76896705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:03bf7b3e8ba2173c36ebe999db59baf03166ed1f76dd4f21515ce9865e5e2d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b426d4b1f7be5da748bb71f92d3b90924aa370a91e61018eb4bbe3e49fd08ee`

```dockerfile
```

-	Layers:
	-	`sha256:1fcb089d5f32a3dc5575a1ff4f11fb3e5d8e1a76abb94b8b6232d8f1f2618aed`  
		Last Modified: Tue, 19 May 2026 23:21:29 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:34e99eaeb771cba35e93b74eda09e01329fe16874ec5316f01ab1942dd06bce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106690717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a4efdd88ab9ed3bfe813b098a84bc2c49de271f28a611dd1b30b25a30b2f1d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:09 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:25:09 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:25:09 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:25:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997d811dd6832182496a3256bb51c0daf268c2846d984126efdc64049cf0fc1d`  
		Last Modified: Tue, 19 May 2026 23:25:23 GMT  
		Size: 76.5 MB (76548798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c1492dfde606967f61c25f5a9539de1e82d29ecfc654f58a2a422a60a3c9200b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5570f493f34ab8b0d7836c90cd892c32b84b3a7ad517a33f4cb4e2e63a08d58c`

```dockerfile
```

-	Layers:
	-	`sha256:7ea8d7c8ebd4790b4503cbf4c5c6a86dde9b7e00dd17e3e978e885d9837c2c49`  
		Last Modified: Tue, 19 May 2026 23:25:21 GMT  
		Size: 9.3 KB (9293 bytes)  
		MIME: application/vnd.in-toto+json
