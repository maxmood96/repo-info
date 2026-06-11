## `azul-zulu:21-jdk-debian`

```console
$ docker pull azul-zulu@sha256:f1874fa30db9e8b9cc59bd9283562bb200c73fe4a4a917907cc8a1b9cc107650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jdk-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:cf13fb2b34743007a620d7d210da8694a4236fb8916915d60aa2a21ec1395391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195881062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad5d3bd69a2a7bdc1c5c6bff7509a3e3f8ec5ef536782a5b7d9c095a5bd207b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:40:23 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:40:23 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:40:23 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:40:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Thu, 11 Jun 2026 00:40:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adf416c06a3633075dc955f5e39a6b14c14cb34146cb122c9110960311ff7bc`  
		Last Modified: Thu, 11 Jun 2026 00:40:39 GMT  
		Size: 166.1 MB (166095647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d550110c91f58f36053cb727a97a1d23a89712b38fdc7c322805f8cf6d6aeaee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6984d55cd0cb79a63bda92f5bdeed1a42112c28d187bf7da5bb5dcc506d42cf0`

```dockerfile
```

-	Layers:
	-	`sha256:78fb5a6e43a109f62864055581ccdaa462572d62c98ac18446c414367c771298`  
		Last Modified: Thu, 11 Jun 2026 00:40:35 GMT  
		Size: 9.5 KB (9506 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jdk-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:b946f4c1e321662e25513d8d9e81ee632c7eb191b8bdb7395202dcbc8d9f6fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195548751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639419bd7ed5de56b5cd1918250ccad5fa905972acca9a51fc58c6d3f6ea3bb0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:16 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:42:16 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:42:16 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:42:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Thu, 11 Jun 2026 00:42:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c5644d54cf3e3a0f5a44e7576d632485629c2914ff98c73cfd97537e82541`  
		Last Modified: Thu, 11 Jun 2026 00:42:35 GMT  
		Size: 165.4 MB (165400221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b65e764abde5c5efcd6b9081a006b12a365584a1608baa99eac46b28ad09f4c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f0bf5ff4465490b2422e1dceea08c344585bee1b8014f1794164c132575874`

```dockerfile
```

-	Layers:
	-	`sha256:51472d31790a1f367914471d7d98636f63489e005694b89c905ac1408a3a452e`  
		Last Modified: Thu, 11 Jun 2026 00:42:30 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
