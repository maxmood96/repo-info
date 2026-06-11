## `azul-zulu:17-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:90e388fa75488846a5b092ecf061435496d4eedf04a5b7001d5f674d7bf9096b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:f30f5f8c708f3ae1e528fc3ea2cb56ff5ff1de8f479b42f7090820f81a731825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99314371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee28c84259a848cb07356fc9e4e1285fb158eacbb07228fececb4a538de7ff4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:40:00 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:40:00 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:40:00 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:40:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43b7876dff26fb08c0755900ce459cdafc3d3a8774d1a269953abdd407e4025`  
		Last Modified: Thu, 11 Jun 2026 00:40:12 GMT  
		Size: 69.5 MB (69528956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3cf04a11e9b815fb55fb1abc99a5ba6fcb4347fd76804d463da77d45d41673e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4f9d7193a1717a2dd5236321870271a43d44f4ec72920c003440484a742863`

```dockerfile
```

-	Layers:
	-	`sha256:8780341d42cb4fdd2ca536116e20470031a7b4b0f562c453d1fd2724951fa591`  
		Last Modified: Thu, 11 Jun 2026 00:40:10 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:db7ee525d00f584b8fbf151070e1a1f47e3a568f889e42194c8733bf742ef760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99733263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9184c98e24a4303b131ff3e534c55a9795751423d9c682526822d9d6322ddc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:41:54 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:41:54 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:41:54 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:41:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b15c180c519e6bf832bddf31cd1aed665b2b9d49b72b0637f5e1adc2056e059`  
		Last Modified: Thu, 11 Jun 2026 00:42:06 GMT  
		Size: 69.6 MB (69584733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ef9afba134ad97929b5add935c63ee04c8703ac327a36715c7bff6b676ddd6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71002eb6e528babe999173eefe647fdf0afec2e12536e509d3f37bbec7b9d2ac`

```dockerfile
```

-	Layers:
	-	`sha256:ac69a6bd7e33df2fd915ee3eb7cf79a33769cb4e97f897bc7c9a74b50db21a39`  
		Last Modified: Thu, 11 Jun 2026 00:42:04 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json
