## `azul-zulu:21-jre-debian13`

```console
$ docker pull azul-zulu@sha256:7f2d6de0598c9ff1aac5790f759eae144a4528892461f5bfa3f851390d498abd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c25a577175e4189b948afe750bf5c6f20b212f448993e57b1f7c6f28ab0c5a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106675941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df3da61d037cd541256e9f1f8a1a28d8b98408bb0f617acb5ea11c7fcb611d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:37:55 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:37:55 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:37:55 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:37:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7540a4b1fde08e591db41b6b9f1db69e8aec122bb642959a572e8caca97af7f`  
		Last Modified: Wed, 22 Apr 2026 01:38:07 GMT  
		Size: 76.9 MB (76895767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:cd77bed7e658c096a3bbaebd056da73ebfd753284d6772d5645c6772ba237eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cd8940de83cd16cce10a8a30fa3a582cfd36fa0c58988ec48c463cd18c0b78`

```dockerfile
```

-	Layers:
	-	`sha256:72d2be779dd1b18953064077ab4c21072bc635c445b1c698a196f6320e647d84`  
		Last Modified: Wed, 22 Apr 2026 01:38:05 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:5afcfc9c55f3f354d85ff7172ac4e18ed4e5d6cc79da0ad15498494d6074dbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106690973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba7a098f082d47ef7266516dc855b1bd79296dcdd36c73e350b9347b1f0c9cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:02 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:42:02 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:42:02 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:42:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37076a3a4e4abfbe752598a5fd9c1ecdd822964ce3bcf6ca0012cf080b52193`  
		Last Modified: Wed, 22 Apr 2026 01:42:16 GMT  
		Size: 76.5 MB (76547367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:fc367c47558ab2572a58e5d5edbbb688e4611d3581d23fad16b547f27f41235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c72cf41055ed379b850031941560aeb5e1f8dc40acb93c70dd195744e11780`

```dockerfile
```

-	Layers:
	-	`sha256:7880d6ab365707d160bb9041aabf8ee67cb150196c56f7446099ec92d552ada0`  
		Last Modified: Wed, 22 Apr 2026 01:42:12 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
