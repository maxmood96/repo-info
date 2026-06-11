## `azul-zulu:25-jre-debian`

```console
$ docker pull azul-zulu@sha256:74a6fc65dbc209cb5819533a8c89291952211c1757f30fd2a91a2dadb88027eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:9cb45380edccf167487e6ed2fca6a80be1a55d12522ea5dcf2f59b3728252e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120834525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94597473eca34e7cb9fca33490f46749b96ee68838f254ea6984a7d47acbc40`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:41:19 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:41:19 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:41:19 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:41:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7554c8741a9294d36d12ae401560d42572e704c419a2a4c0d8c8d2eb2d5496e0`  
		Last Modified: Thu, 11 Jun 2026 00:41:33 GMT  
		Size: 91.0 MB (91049110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e0d72a663a11d47eebf47fec252d124646bdd1e0587f5a8a0b491879c2e26a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c42504734679f52bb572cdd6818d28e102309abf93017064dfc9cf1cb9c72e4`

```dockerfile
```

-	Layers:
	-	`sha256:ea1e1d0170841dc2bef77489c6c7bcc1f5659f2a3a6bb78ef183c6bcd52d5455`  
		Last Modified: Thu, 11 Jun 2026 00:41:31 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:6f459b5f7e3be017b8c034c96af777e8029421eee72eee010132031be1dc2ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120784796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0bb1cab03fe23e5ba2b6324cf48314615b3c915692b015b05758a85d85a283`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:43:11 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:43:11 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:43:11 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:43:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8f7326474506416cdabd7a457a1bd2b60df795a4ce863a31f8f88fdd19977`  
		Last Modified: Thu, 11 Jun 2026 00:43:25 GMT  
		Size: 90.6 MB (90636266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f91085f919de3d0ab5d05dae3d663fe53bae8096acf558731b9ef1e6f0b7283c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc953f6368039cdc27068502613adc751b29847969c50fdd93bc8dcdbb61398`

```dockerfile
```

-	Layers:
	-	`sha256:7fb0058a0a9b4a04c577e0c7406200e4f7ecc15561b102efcd73b2860aa08123`  
		Last Modified: Thu, 11 Jun 2026 00:43:23 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
