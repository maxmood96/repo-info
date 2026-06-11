## `azul-zulu:17-jre-debian13`

```console
$ docker pull azul-zulu@sha256:3b79b1293ed337ab57fe81bce5b3bbe4b8b011b736031e02fa6a51f43c681070
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:9a58b88cfbb70135e374415cd184e00df78ac3207cb6826c2d34a308bc991e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101409921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f5b7eaa65cbd720c403799ea1ab38f3d9474e0e675ed1df11d026b63c61c8f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:39:54 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:39:54 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:39:54 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:39:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde7d1f05fbb99820b664cdc34b0ceb23d2982d24756c1a79e4dac67bf009c05`  
		Last Modified: Thu, 11 Jun 2026 00:40:06 GMT  
		Size: 71.6 MB (71624506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2052649406c368b78bf5af2c252027a9a6d4e75afc21f8982516a2f8d2e35bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383f9579dd0e5138ebe3478d32d1d7808b3e03d476a65dc562361751a59879ba`

```dockerfile
```

-	Layers:
	-	`sha256:8cc686db8e6e3e42639e50ae55c60f44b4e4ca148e338cbf54f779be9a137d1d`  
		Last Modified: Thu, 11 Jun 2026 00:40:04 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:ff08584bae35b88241d167d9a1eee79d10e49f417313256755acf75e973d56ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101805630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0399cb72e492577decdf3a7442b29be0e0c639555a33cb6f7cdfbfee0916a7d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:41:52 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:41:52 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:41:52 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:41:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0602d7106e7b083f40220b726c6f284a2a75568bf5640d06329fea38126be78b`  
		Last Modified: Thu, 11 Jun 2026 00:42:05 GMT  
		Size: 71.7 MB (71657100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c52c6e4cc3818c973a5e5bec40e5a8ef95123fbf61d77ccc8459973ac31e98dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5eae0d621db86c779b3d1a61d3c7740fda764613f1026ee2c0c397cbc36b955`

```dockerfile
```

-	Layers:
	-	`sha256:6bb5a4789f19a8720aa138d803cd234198bff6b12a4557fbf55f32b9893d6b93`  
		Last Modified: Thu, 11 Jun 2026 00:42:02 GMT  
		Size: 9.3 KB (9292 bytes)  
		MIME: application/vnd.in-toto+json
