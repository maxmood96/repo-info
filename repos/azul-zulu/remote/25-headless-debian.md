## `azul-zulu:25-headless-debian`

```console
$ docker pull azul-zulu@sha256:8b06780da840cb9e56f173035c3f25315ef88817a533661673eb64a5da04ea2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:5564df379d55c67d284f1d41a69ee08ec3eb6cc8825971f3e0dcd4f1e7b17f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212689358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4275c1721bf0974d6769f3c086aff7c30f00119f589642318dcd7fa8b4616c7e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:41:22 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:41:22 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:41:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:41:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Thu, 11 Jun 2026 00:41:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316f9e69ee1563ad0b2ba8bc9467fab1b87ad768df364fa1ff0702824688bdda`  
		Last Modified: Thu, 11 Jun 2026 00:41:41 GMT  
		Size: 182.9 MB (182903943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0c4942e5b5953ffd3c154c13e46e3e5ea5700f96c4f0f769be398682fa4dbe3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59eb9326ef7248f5fa6a4a4ff9ece897889c52a109638dc698fb5f47eb842a2`

```dockerfile
```

-	Layers:
	-	`sha256:11c1cda08d96138ab1793005e496413a8c870d3641f92ef420c0d8a84910aa7a`  
		Last Modified: Thu, 11 Jun 2026 00:41:36 GMT  
		Size: 9.3 KB (9295 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:22ae1141ae8b15f2e88a7b62e06bdced54d202388e4bc3b706cd3e357339e79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212203478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ae272124eeb3fbc621d8e32ca43ef8ab3fce949f90b3ec0dd92da565120a18`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:43:07 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:43:07 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:43:07 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:43:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Thu, 11 Jun 2026 00:43:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a067acb5f974b1db340ee2c4b43fe2b3c6d395494ef6016d01d7cb017290a`  
		Last Modified: Thu, 11 Jun 2026 00:43:25 GMT  
		Size: 182.1 MB (182054948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e8fe365f1f5ae027cba8459654cbf6075c96429b3987318802ea113e5c654e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6d382be7df33b90b7e97be25f8a892dc0b61d813148461a6f5300b0ecac3e3`

```dockerfile
```

-	Layers:
	-	`sha256:9014e130f9781eea765098cfcf70afdda1d2efa75f12d60fe66cb9299a650897`  
		Last Modified: Thu, 11 Jun 2026 00:43:21 GMT  
		Size: 9.4 KB (9399 bytes)  
		MIME: application/vnd.in-toto+json
