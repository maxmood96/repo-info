## `azul-zulu:8-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:0a0d976cae9d43649b000caa413d6886d2800a760d253a18629495ded7b25f6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:ffae44e9cb8ab5fd9fbdd20de318d2031cacf29268de6b41081fb75f13f83efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77512880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e005eb0be6553a7b98a1da2e475fd242f3efb7cd576e625daf56dd921f73a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:38:51 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:38:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:38:51 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:38:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0d135dbc474e4075845c22bc730dcf5494e6cc3c790d299f00c2f29249510d`  
		Last Modified: Thu, 11 Jun 2026 00:39:00 GMT  
		Size: 47.7 MB (47727465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:776bcf1af0a3523a69ec62cb0278bbbf2ff2033e6868fcebc6940b26764f2ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8d045e5d7c0dceca1c86600f43e561b7896de5d683fb3290959b4336625855`

```dockerfile
```

-	Layers:
	-	`sha256:f7b926173fb4827b03bfd9571491d650f75215d10cf079ec82b117c105089a63`  
		Last Modified: Thu, 11 Jun 2026 00:38:57 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:b4f64e495b3bc88075e00c625d905836c299daea92b84ca39e2d3067b66f9459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78100295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043b6451bc13f7eb30d9af4ae7949025991917efd4bdfd722a3dd4bfd08c716`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:40:16 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:40:16 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:40:16 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:40:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9d9417004b9d940cdec856fca8a877b55d7c8d9b214e026eec15a8fe6d0adb`  
		Last Modified: Thu, 11 Jun 2026 00:40:24 GMT  
		Size: 48.0 MB (47951765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ed1cf32c9768d52ad18d7f9e8fcafb2a6d8cb11bb8320e465f54e67e124af765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1084c6e5d8ecbaa241cb711226c6de68803894b89b250a5d15dcfba29c81e0e9`

```dockerfile
```

-	Layers:
	-	`sha256:5419458090ccc196d09f5a5bdca5ef0d0e56f3bd0955a150401359a7a7fa1adf`  
		Last Modified: Thu, 11 Jun 2026 00:40:23 GMT  
		Size: 9.4 KB (9389 bytes)  
		MIME: application/vnd.in-toto+json
