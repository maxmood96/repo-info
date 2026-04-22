## `azul-zulu:11-jre-headless`

```console
$ docker pull azul-zulu@sha256:6200a32b69e1481eb1a12a338fc43cee4cb5d75f8de8741710b154a8e01bec02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:97101d8e0aaf89ea644fe92e87978913c0f924fda9becb7b577c29c4291d6bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94823961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c0d1a4f22017aa5994e54f04aa81477f9f22ffcc14fe37154b02ee63c137cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:41 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:36:41 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:36:41 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:36:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86700b002d205db43166dd90b29ad003328d1b66d1934b4e299ca00a220bbdf9`  
		Last Modified: Wed, 22 Apr 2026 01:36:52 GMT  
		Size: 65.0 MB (65043787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:5ddf4874ce708d4f83c7e52a6538090c653237b97071eb78b547db279be7a7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef83c6eccb855c9a116675dd2029a53ae90ffa82e703610b07a2f7a1b722f639`

```dockerfile
```

-	Layers:
	-	`sha256:a4d1c94bada533cdabed1daeea3e297fc94c423d7f90818f6be04444a2be45fd`  
		Last Modified: Wed, 22 Apr 2026 01:36:50 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:59899518a560c94a2fd8e4a3d831199d3cc9afc94531b73d68e80f94258fef31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95027412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1c40a60fa8c1e2c98ffaad7d72d7f6fc47574bc69cca1aee8da9921fb93773`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:41:06 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:41:06 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:41:06 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:41:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65faab5979fd6b621b905f798a3cf77fd2a4fdaadd910b8bf77eefd785b2246`  
		Last Modified: Wed, 22 Apr 2026 01:41:18 GMT  
		Size: 64.9 MB (64883806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8ea60b417b1d0bcaaa5f1d39aa0f3d24d90ffcb6710bd85f6f4e2d2f2adfc6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9768aa8f334a4cc2b27f117c264af9510b9b04695ea3c69ea6d56d8983d3d874`

```dockerfile
```

-	Layers:
	-	`sha256:c01bd498599cc8bb4ab8c9c5ee027e29f801cd9a1b6b3f02aac9f085fc5160b3`  
		Last Modified: Wed, 22 Apr 2026 01:41:14 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
