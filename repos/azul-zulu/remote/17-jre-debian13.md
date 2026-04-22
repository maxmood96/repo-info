## `azul-zulu:17-jre-debian13`

```console
$ docker pull azul-zulu@sha256:598e07e3e3fd406181ce7339d441f04182441d1c97ac6dc26771bd6239a9ae4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:38844d2bf7fc7911ab358249079d4edbb55428779c91f35b5a7ebbf158001584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101404370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06e29643dcb847e47d799f056eaa81bd4dd46367e7690167ea4608de0671734`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:37:16 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:37:16 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:37:16 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:37:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75640f41820da31987ccc9a7853a435d6a9603c440ba70507c9683cdb2ddcea0`  
		Last Modified: Wed, 22 Apr 2026 01:37:29 GMT  
		Size: 71.6 MB (71624196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b9a18fec9baaddebf096b17fe6912f54c8c42bafc201ce04049597da134d48ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4420b2ad77766ad3859be37b42a65a9323731607d90ec1ae1cb97f19e2b48af4`

```dockerfile
```

-	Layers:
	-	`sha256:8800d980bb4357704372063caa4ea4dab7daddc2c848ded60261d31305196274`  
		Last Modified: Wed, 22 Apr 2026 01:37:27 GMT  
		Size: 9.2 KB (9189 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:a5042a532cc7bc73d6e58bbfb81f5e4b6450c0460fcb4e6be203b880c0a12bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101800403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4e36b6ca2b4a99b374d34a512cfe62e50f0159aa766a23788e5426df99f09f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:41:35 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:41:35 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:41:35 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:41:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec057a2b64808645c2b455c5bb03ad0b5bbf8c5a720d578aff7b64b399924f5`  
		Last Modified: Wed, 22 Apr 2026 01:41:48 GMT  
		Size: 71.7 MB (71656797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:71257c961fc62bad514033988b7da9cfa74ccc95a32ec525a486cf8d9f0095a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f990603a25b79b15c8122d80dba04256d5f2b93dc2cc2e7aa26bccb5ed83a905`

```dockerfile
```

-	Layers:
	-	`sha256:fdd5951909b8bf339ca716aae146da65c76488eb834fdc3728912806334ef6ab`  
		Last Modified: Wed, 22 Apr 2026 01:41:45 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
