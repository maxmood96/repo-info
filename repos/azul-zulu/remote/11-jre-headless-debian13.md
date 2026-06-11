## `azul-zulu:11-jre-headless-debian13`

```console
$ docker pull azul-zulu@sha256:e8d1525cfec9c85b25483ce91f122f099e9113862162c8272be9c362131af6e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:b8f547772414433aef67bb1ee91f9c57e006dea08817c815bca8f3e9e0eeb490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94830242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e64c1b565a676b16767cfff2704d9943c192e7b4b63f4c512dc62c5316fe55`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:24 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:39:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:39:24 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:39:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6bf6bc7e0a0940c7bc04d956ff2fd45a6ab06beb20e3966453b235c62bdbdf`  
		Last Modified: Thu, 11 Jun 2026 00:39:36 GMT  
		Size: 65.0 MB (65044827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d7f1a42a2d4598d05e6e5cadef918f9336ce0b538d682d5c222735194974a2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97ebc5ad6b12c18858c38c7e3837a2c9cfdec609b8c025cf9c570cf0741a563`

```dockerfile
```

-	Layers:
	-	`sha256:70e32e0ff6b272348a1073b47a4f28faa887d8145d53d82b0849526b8cb4fcd0`  
		Last Modified: Thu, 11 Jun 2026 00:39:33 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:23417df7b1ed8cf209ed8a567f1b1929d74c5d9a1696567f439cf411a02a822d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95032542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ec6fb5726fa884aaa94c111e14919a30f62c5dd9dcf8cb875f4eee7ae385bf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:41:14 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:41:14 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:41:14 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:41:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdc3571f32bdeb39010f0a37df3b50d112308c52323ed2b298269f1e39839e1`  
		Last Modified: Thu, 11 Jun 2026 00:41:25 GMT  
		Size: 64.9 MB (64884012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:36c7e46d63b2d4a3b6d06b5e490f7949098b97981e2e25b05a5f6cc1e66eebb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c610e14c2d033a80970f4a518d382c2b0472d4a37e5b3093ede45870a2f50698`

```dockerfile
```

-	Layers:
	-	`sha256:0803a335ed7c73f5c95afcb68aae578d0a8dac0f8fff7e01236905c6acec3155`  
		Last Modified: Thu, 11 Jun 2026 00:41:23 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
