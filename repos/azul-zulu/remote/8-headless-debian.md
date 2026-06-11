## `azul-zulu:8-headless-debian`

```console
$ docker pull azul-zulu@sha256:0b29b564c802ef6c9d8c3baa511e13b86d9af963874706d2d880ca86fe8c4262
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:8d27d738a9182962c72ba0b5d174e630ff78391efdc97d38493d12f5a2cea33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88933823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0ab1ea40af857f334c656615f444fae903dc8c96d6a9f5edb116662fa8b0bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:18 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:38:18 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:38:18 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:38:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e399c76780c2377c30ea3d7fd7af58a116323f2ab616af0f71ae0b81fed24b`  
		Last Modified: Thu, 11 Jun 2026 00:38:27 GMT  
		Size: 59.1 MB (59148408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:37c10e0514b407c6e63abfea5e9b85dafd18bb6f3c9e305c649af88fdcb4dba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5021a6e7c5bb78ae1253195e9ad10d0fcd0185ff98701815316366ceebd07047`

```dockerfile
```

-	Layers:
	-	`sha256:6ef753cc4f894905deffcb325e0567bf01314d65dd0dbac486efde0511d5ab76`  
		Last Modified: Thu, 11 Jun 2026 00:38:26 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:bd61352247a89229dc7f6ab8f2f39913fc3e38a01ebd1820b542932e0bf9ca48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89626892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2746145a0913f54ddbeb294108a5b63395397ca6540b0f7fa6bd8a70260e0e8f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:53 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:39:53 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:39:53 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:39:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed38c133b8e8eb581632d2fbfb50b790e3ab4e68dd9618e283d9cf82780d24`  
		Last Modified: Thu, 11 Jun 2026 00:40:03 GMT  
		Size: 59.5 MB (59478362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b97e3d6098d72f1be00c62aaae0864607bb31b20bbaf3dbff7b1f859ea3dea80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45f673f91ec457322a3c77835d7e1cb85019c26ddd43403a92f6d3b994e2e2f`

```dockerfile
```

-	Layers:
	-	`sha256:b583704d94a1754e5fa3f135832d600d0e82ecf71a4f6f1a62333f06adee4162`  
		Last Modified: Thu, 11 Jun 2026 00:40:01 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json
