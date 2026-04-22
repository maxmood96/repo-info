<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.17`](#varnish6017)
-	[`varnish:8`](#varnish8)
-	[`varnish:8-alpine`](#varnish8-alpine)
-	[`varnish:8.0`](#varnish80)
-	[`varnish:8.0-alpine`](#varnish80-alpine)
-	[`varnish:8.0.1`](#varnish801)
-	[`varnish:8.0.1-alpine`](#varnish801-alpine)
-	[`varnish:9`](#varnish9)
-	[`varnish:9.0`](#varnish90)
-	[`varnish:9.0.1`](#varnish901)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:5a330531aed44556cb3945541e545ee72883e95c02004a90e0de9d9d4095c2e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:d7470c7890e171e9d092e0341de3f0b816224fce30c7d4c5d938f77da4f9ab56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121845786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45d675741188122757da0f492460259a71a0b8ef0e0fed186d26d238ed46449`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:35:24 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:35:24 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Wed, 22 Apr 2026 01:35:24 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:35:24 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:35:24 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:35:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:35:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:35:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:35:24 GMT
CMD []
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428831b534d63ea84ae32b63b89352efb0090a51ec53adca52c20daf8c61ed5`  
		Last Modified: Wed, 22 Apr 2026 01:35:38 GMT  
		Size: 93.6 MB (93608783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ed50d38925630e1365fcfc59ae9af553ee92efeba5b5fddb0f619da147e21`  
		Last Modified: Wed, 22 Apr 2026 01:35:35 GMT  
		Size: 719.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:4d8885d15e8ad327757cc9af7d9d19d1ffb9054cfb6fcf9aec1e2095f0130e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b9f24314d0f95ed439d9dd32076f2f77751396474725ee8461d7334ddab706`

```dockerfile
```

-	Layers:
	-	`sha256:b5efb2061b3a5a62abd9b670bc433fea46b64575de786bb82ca8c623a58174cf`  
		Last Modified: Wed, 22 Apr 2026 01:35:35 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:51aab920607f22b9b4b92e2a4263397ed679206af6280dd5eec0ba6128e4642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116282023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758f6baa0188670ac0cca26ad29c5cd562de377f21f4f41b9813aa5e859063e9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:38:30 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:30 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Wed, 22 Apr 2026 01:38:30 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:30 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:30 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:30 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:30 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:30 GMT
CMD []
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522c865a1a54eb735fca6d3bf5028dadb14227f8380fe813af1385c80230d29a`  
		Last Modified: Wed, 22 Apr 2026 01:38:44 GMT  
		Size: 88.2 MB (88165156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66318508b57a6194c6e839ff16e5796d0fb09317a44ad26663f4635ace80808f`  
		Last Modified: Wed, 22 Apr 2026 01:38:42 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:a1d5e941f4f75457809893d805774755e6ec4665c5175a3e589c488b6ce07e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77747cb1d135fd70a706bc5e1d64b09bca10c685f35ed9a958fa1a591fe37875`

```dockerfile
```

-	Layers:
	-	`sha256:ee8295a66738c6a3e8f816c3738eab8d8cc432f2a11934f3bc47824084752f3f`  
		Last Modified: Wed, 22 Apr 2026 01:38:42 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.17`

```console
$ docker pull varnish@sha256:5a330531aed44556cb3945541e545ee72883e95c02004a90e0de9d9d4095c2e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0.17` - linux; amd64

```console
$ docker pull varnish@sha256:d7470c7890e171e9d092e0341de3f0b816224fce30c7d4c5d938f77da4f9ab56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121845786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45d675741188122757da0f492460259a71a0b8ef0e0fed186d26d238ed46449`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:35:24 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:35:24 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Wed, 22 Apr 2026 01:35:24 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:35:24 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:35:24 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:35:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:35:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:35:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:35:24 GMT
CMD []
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428831b534d63ea84ae32b63b89352efb0090a51ec53adca52c20daf8c61ed5`  
		Last Modified: Wed, 22 Apr 2026 01:35:38 GMT  
		Size: 93.6 MB (93608783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ed50d38925630e1365fcfc59ae9af553ee92efeba5b5fddb0f619da147e21`  
		Last Modified: Wed, 22 Apr 2026 01:35:35 GMT  
		Size: 719.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.17` - unknown; unknown

```console
$ docker pull varnish@sha256:4d8885d15e8ad327757cc9af7d9d19d1ffb9054cfb6fcf9aec1e2095f0130e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b9f24314d0f95ed439d9dd32076f2f77751396474725ee8461d7334ddab706`

```dockerfile
```

-	Layers:
	-	`sha256:b5efb2061b3a5a62abd9b670bc433fea46b64575de786bb82ca8c623a58174cf`  
		Last Modified: Wed, 22 Apr 2026 01:35:35 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.17` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:51aab920607f22b9b4b92e2a4263397ed679206af6280dd5eec0ba6128e4642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116282023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758f6baa0188670ac0cca26ad29c5cd562de377f21f4f41b9813aa5e859063e9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:38:30 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:30 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Wed, 22 Apr 2026 01:38:30 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:30 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:30 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:30 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:30 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:30 GMT
CMD []
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522c865a1a54eb735fca6d3bf5028dadb14227f8380fe813af1385c80230d29a`  
		Last Modified: Wed, 22 Apr 2026 01:38:44 GMT  
		Size: 88.2 MB (88165156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66318508b57a6194c6e839ff16e5796d0fb09317a44ad26663f4635ace80808f`  
		Last Modified: Wed, 22 Apr 2026 01:38:42 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.17` - unknown; unknown

```console
$ docker pull varnish@sha256:a1d5e941f4f75457809893d805774755e6ec4665c5175a3e589c488b6ce07e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77747cb1d135fd70a706bc5e1d64b09bca10c685f35ed9a958fa1a591fe37875`

```dockerfile
```

-	Layers:
	-	`sha256:ee8295a66738c6a3e8f816c3738eab8d8cc432f2a11934f3bc47824084752f3f`  
		Last Modified: Wed, 22 Apr 2026 01:38:42 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8`

```console
$ docker pull varnish@sha256:7fa8dd2fcdbeaefc29efb96c92dac505eb76ff194593db28632f687ad20ec230
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8` - linux; amd64

```console
$ docker pull varnish@sha256:0d7c333016f4d2b3a66bc5be6307ae235c6f20b0a5d71169c404e475acea82ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120223887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb157507910bf77f5197f4da860b15ce00571331d6d9e4b128ff9559976caa94`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:04 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 22 Apr 2026 01:36:04 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:36:04 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:36:04 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:36:04 GMT
USER varnish
# Wed, 22 Apr 2026 01:36:04 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:36:04 GMT
CMD []
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13fe021ce98fc3e43723e7d6eac15fa7e57c09454bcdbf055816cd8f0eb3f66`  
		Last Modified: Wed, 22 Apr 2026 01:36:18 GMT  
		Size: 90.4 MB (90440595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd665091af05d185e797f0e25cfa2c7ebba7303f69cbb1071e23ac0f13e97f32`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1b61c9f2264ebe42547ca72098767d2bd98eb008dd8603043987576a7b32f1`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4694eb4d823ed6d46fda0ed742c60b52221d9f1dd3c2ba7ec9fa67d1bf2ac1`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:5a0509b660617508db280d9b212d0bcb97434d5ab67ec8c52791555324fa7141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0653a73fecbd756b34b5b735f68d7667a88c3e199c91c378f582d19f7d6fde1`

```dockerfile
```

-	Layers:
	-	`sha256:d7f20852d018cab3bd1ebc3f8946cd01956a95d2e24b1e765ee2afa53355c228`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 20.6 KB (20566 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:52862dbab6a067932694258f3537003d531fbdb83ecb57d6bd3fc23a1e6133f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114223681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f56b3f99a36d1369fc3e9f67daab174f101df81ef42245cdcf1373ed7e536`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:51 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 22 Apr 2026 01:38:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:38:51 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:51 GMT
USER varnish
# Wed, 22 Apr 2026 01:38:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:51 GMT
CMD []
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafd7766e5127767b5b73b02696b18df5e05c79c066ca1ba3dd03f8c184766ef`  
		Last Modified: Wed, 22 Apr 2026 01:39:05 GMT  
		Size: 84.1 MB (84076958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a7d79f36816eb049aa66034af5058439fe387ba9fc3fc951f1c729ae61e54`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d79a8a35d70caadc22937595fd60dcb0e856079b34513fbc53e15c5597733`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d82b935e13bb0df346909afb500e111a6054f6c92294df2b3a1026e77ce7db`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:e267c9e599c04d4449f03ae59c502a07ec2d8388a8c0689e85f8ac1c7ee74ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1497c254c5a9d6ced5afadcf08a8f169b34f428363334beb851beada8ab08a37`

```dockerfile
```

-	Layers:
	-	`sha256:772a91d4e68d1310789627a9d789cdd14a324d171027ae540dadd8d4523509c8`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 20.7 KB (20671 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8-alpine`

```console
$ docker pull varnish@sha256:0860b5e9f5535e373080f6921bdb68959dc93c300da569107cfedc45fe236e67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:41f3ee7e8f3a3a46657d7df7ddadd5eea49da1d7186284c299faf77f3cec2c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91658907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791bb19331c2b2bdffebd848babfd121a6021d9427e2c6f475f99a072a619ee8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:23 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_VERSION=8.0.1
# Wed, 15 Apr 2026 20:24:23 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 15 Apr 2026 20:24:23 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VARNISH_SIZE=100M
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VSM_NOPID=1
# Wed, 15 Apr 2026 20:24:23 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
WORKDIR /etc/varnish
# Wed, 15 Apr 2026 20:24:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 15 Apr 2026 20:24:24 GMT
USER varnish
# Wed, 15 Apr 2026 20:24:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 15 Apr 2026 20:24:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679d8a78a51fbc1e26e3a678fe492cb6f2332d4ee6ff65807916cefd5e7a4543`  
		Last Modified: Wed, 15 Apr 2026 20:24:37 GMT  
		Size: 87.8 MB (87791576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbbe98298180f5425cbd3529c155c99c4e2c43a390736a0524bb53683e88a1d`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94df06b538832a31a7961a6b753325a876258ed49ff0bebc40e9f1e3c04d0429`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0000b7ec6e0d633f66fbfb4778f222772737c21df487d6d648510fe7ebeca081`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:121924b23cede2872bba60cfc876f0b636157d3953b18b905da44259989aa0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b064587648707975a1acba9f70f37952c06481aa9895c4baafc8fc2393dfc3a5`

```dockerfile
```

-	Layers:
	-	`sha256:676e5180366d3c79d0802be63ad307362ab73fce89e51c60c4b2fb7c1b54c9e5`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:67be9e66cdb3ad84876f5dad5620896effd2e231ae6a997051af53eacb54e8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83419928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4d2863af766a3f848e4feb44e40779c7c6b89b6ce777ffeb9d0b7b73efab98`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:12 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_VERSION=8.0.1
# Wed, 15 Apr 2026 20:24:12 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 15 Apr 2026 20:24:12 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VARNISH_SIZE=100M
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VSM_NOPID=1
# Wed, 15 Apr 2026 20:24:12 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
WORKDIR /etc/varnish
# Wed, 15 Apr 2026 20:24:12 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 15 Apr 2026 20:24:12 GMT
USER varnish
# Wed, 15 Apr 2026 20:24:12 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 15 Apr 2026 20:24:12 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188f5b124ebe49de1164f7bc653185e82a76feb345a08196cf1a77b777bb7b78`  
		Last Modified: Wed, 15 Apr 2026 20:24:24 GMT  
		Size: 79.2 MB (79216922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da572ca168ae2da5fea13f3ded2448ea2dc618755043a2379de0eeeca56cba1d`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac44db7085a08eafc8087de7e0125e8bf2b440b3971135caf10aa92aebd550f`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191bd24e338faf457cdd8ab90dbc37ac634ed3b5562b7a77c422b9a2d2be6bf3`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:89d178943cec924648184dd343a5ac5570da6c4ec413e190b55be53a2a99fbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da0f9e255d495cc4139c0ffeacb61b4ca2e1599623537a29fb59707161221c2`

```dockerfile
```

-	Layers:
	-	`sha256:2cf9e1788fc9c92f38269c5e206e19918276f8c47b42d246a2d759dbe45e3da9`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0`

```console
$ docker pull varnish@sha256:7fa8dd2fcdbeaefc29efb96c92dac505eb76ff194593db28632f687ad20ec230
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0` - linux; amd64

```console
$ docker pull varnish@sha256:0d7c333016f4d2b3a66bc5be6307ae235c6f20b0a5d71169c404e475acea82ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120223887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb157507910bf77f5197f4da860b15ce00571331d6d9e4b128ff9559976caa94`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:04 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 22 Apr 2026 01:36:04 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:36:04 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:36:04 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:36:04 GMT
USER varnish
# Wed, 22 Apr 2026 01:36:04 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:36:04 GMT
CMD []
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13fe021ce98fc3e43723e7d6eac15fa7e57c09454bcdbf055816cd8f0eb3f66`  
		Last Modified: Wed, 22 Apr 2026 01:36:18 GMT  
		Size: 90.4 MB (90440595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd665091af05d185e797f0e25cfa2c7ebba7303f69cbb1071e23ac0f13e97f32`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1b61c9f2264ebe42547ca72098767d2bd98eb008dd8603043987576a7b32f1`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4694eb4d823ed6d46fda0ed742c60b52221d9f1dd3c2ba7ec9fa67d1bf2ac1`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:5a0509b660617508db280d9b212d0bcb97434d5ab67ec8c52791555324fa7141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0653a73fecbd756b34b5b735f68d7667a88c3e199c91c378f582d19f7d6fde1`

```dockerfile
```

-	Layers:
	-	`sha256:d7f20852d018cab3bd1ebc3f8946cd01956a95d2e24b1e765ee2afa53355c228`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 20.6 KB (20566 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:52862dbab6a067932694258f3537003d531fbdb83ecb57d6bd3fc23a1e6133f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114223681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f56b3f99a36d1369fc3e9f67daab174f101df81ef42245cdcf1373ed7e536`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:51 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 22 Apr 2026 01:38:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:38:51 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:51 GMT
USER varnish
# Wed, 22 Apr 2026 01:38:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:51 GMT
CMD []
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafd7766e5127767b5b73b02696b18df5e05c79c066ca1ba3dd03f8c184766ef`  
		Last Modified: Wed, 22 Apr 2026 01:39:05 GMT  
		Size: 84.1 MB (84076958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a7d79f36816eb049aa66034af5058439fe387ba9fc3fc951f1c729ae61e54`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d79a8a35d70caadc22937595fd60dcb0e856079b34513fbc53e15c5597733`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d82b935e13bb0df346909afb500e111a6054f6c92294df2b3a1026e77ce7db`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:e267c9e599c04d4449f03ae59c502a07ec2d8388a8c0689e85f8ac1c7ee74ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1497c254c5a9d6ced5afadcf08a8f169b34f428363334beb851beada8ab08a37`

```dockerfile
```

-	Layers:
	-	`sha256:772a91d4e68d1310789627a9d789cdd14a324d171027ae540dadd8d4523509c8`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 20.7 KB (20671 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0-alpine`

```console
$ docker pull varnish@sha256:0860b5e9f5535e373080f6921bdb68959dc93c300da569107cfedc45fe236e67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:41f3ee7e8f3a3a46657d7df7ddadd5eea49da1d7186284c299faf77f3cec2c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91658907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791bb19331c2b2bdffebd848babfd121a6021d9427e2c6f475f99a072a619ee8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:23 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_VERSION=8.0.1
# Wed, 15 Apr 2026 20:24:23 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 15 Apr 2026 20:24:23 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VARNISH_SIZE=100M
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VSM_NOPID=1
# Wed, 15 Apr 2026 20:24:23 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
WORKDIR /etc/varnish
# Wed, 15 Apr 2026 20:24:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 15 Apr 2026 20:24:24 GMT
USER varnish
# Wed, 15 Apr 2026 20:24:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 15 Apr 2026 20:24:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679d8a78a51fbc1e26e3a678fe492cb6f2332d4ee6ff65807916cefd5e7a4543`  
		Last Modified: Wed, 15 Apr 2026 20:24:37 GMT  
		Size: 87.8 MB (87791576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbbe98298180f5425cbd3529c155c99c4e2c43a390736a0524bb53683e88a1d`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94df06b538832a31a7961a6b753325a876258ed49ff0bebc40e9f1e3c04d0429`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0000b7ec6e0d633f66fbfb4778f222772737c21df487d6d648510fe7ebeca081`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:121924b23cede2872bba60cfc876f0b636157d3953b18b905da44259989aa0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b064587648707975a1acba9f70f37952c06481aa9895c4baafc8fc2393dfc3a5`

```dockerfile
```

-	Layers:
	-	`sha256:676e5180366d3c79d0802be63ad307362ab73fce89e51c60c4b2fb7c1b54c9e5`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:67be9e66cdb3ad84876f5dad5620896effd2e231ae6a997051af53eacb54e8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83419928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4d2863af766a3f848e4feb44e40779c7c6b89b6ce777ffeb9d0b7b73efab98`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:12 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_VERSION=8.0.1
# Wed, 15 Apr 2026 20:24:12 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 15 Apr 2026 20:24:12 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VARNISH_SIZE=100M
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VSM_NOPID=1
# Wed, 15 Apr 2026 20:24:12 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
WORKDIR /etc/varnish
# Wed, 15 Apr 2026 20:24:12 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 15 Apr 2026 20:24:12 GMT
USER varnish
# Wed, 15 Apr 2026 20:24:12 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 15 Apr 2026 20:24:12 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188f5b124ebe49de1164f7bc653185e82a76feb345a08196cf1a77b777bb7b78`  
		Last Modified: Wed, 15 Apr 2026 20:24:24 GMT  
		Size: 79.2 MB (79216922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da572ca168ae2da5fea13f3ded2448ea2dc618755043a2379de0eeeca56cba1d`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac44db7085a08eafc8087de7e0125e8bf2b440b3971135caf10aa92aebd550f`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191bd24e338faf457cdd8ab90dbc37ac634ed3b5562b7a77c422b9a2d2be6bf3`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:89d178943cec924648184dd343a5ac5570da6c4ec413e190b55be53a2a99fbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da0f9e255d495cc4139c0ffeacb61b4ca2e1599623537a29fb59707161221c2`

```dockerfile
```

-	Layers:
	-	`sha256:2cf9e1788fc9c92f38269c5e206e19918276f8c47b42d246a2d759dbe45e3da9`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.1`

```console
$ docker pull varnish@sha256:7fa8dd2fcdbeaefc29efb96c92dac505eb76ff194593db28632f687ad20ec230
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.1` - linux; amd64

```console
$ docker pull varnish@sha256:0d7c333016f4d2b3a66bc5be6307ae235c6f20b0a5d71169c404e475acea82ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120223887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb157507910bf77f5197f4da860b15ce00571331d6d9e4b128ff9559976caa94`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:04 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 22 Apr 2026 01:36:04 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:36:04 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:36:04 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:36:04 GMT
USER varnish
# Wed, 22 Apr 2026 01:36:04 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:36:04 GMT
CMD []
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13fe021ce98fc3e43723e7d6eac15fa7e57c09454bcdbf055816cd8f0eb3f66`  
		Last Modified: Wed, 22 Apr 2026 01:36:18 GMT  
		Size: 90.4 MB (90440595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd665091af05d185e797f0e25cfa2c7ebba7303f69cbb1071e23ac0f13e97f32`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1b61c9f2264ebe42547ca72098767d2bd98eb008dd8603043987576a7b32f1`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4694eb4d823ed6d46fda0ed742c60b52221d9f1dd3c2ba7ec9fa67d1bf2ac1`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:5a0509b660617508db280d9b212d0bcb97434d5ab67ec8c52791555324fa7141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0653a73fecbd756b34b5b735f68d7667a88c3e199c91c378f582d19f7d6fde1`

```dockerfile
```

-	Layers:
	-	`sha256:d7f20852d018cab3bd1ebc3f8946cd01956a95d2e24b1e765ee2afa53355c228`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 20.6 KB (20566 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:52862dbab6a067932694258f3537003d531fbdb83ecb57d6bd3fc23a1e6133f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114223681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f56b3f99a36d1369fc3e9f67daab174f101df81ef42245cdcf1373ed7e536`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:51 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 22 Apr 2026 01:38:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:38:51 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:51 GMT
USER varnish
# Wed, 22 Apr 2026 01:38:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:51 GMT
CMD []
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafd7766e5127767b5b73b02696b18df5e05c79c066ca1ba3dd03f8c184766ef`  
		Last Modified: Wed, 22 Apr 2026 01:39:05 GMT  
		Size: 84.1 MB (84076958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a7d79f36816eb049aa66034af5058439fe387ba9fc3fc951f1c729ae61e54`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d79a8a35d70caadc22937595fd60dcb0e856079b34513fbc53e15c5597733`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d82b935e13bb0df346909afb500e111a6054f6c92294df2b3a1026e77ce7db`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:e267c9e599c04d4449f03ae59c502a07ec2d8388a8c0689e85f8ac1c7ee74ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1497c254c5a9d6ced5afadcf08a8f169b34f428363334beb851beada8ab08a37`

```dockerfile
```

-	Layers:
	-	`sha256:772a91d4e68d1310789627a9d789cdd14a324d171027ae540dadd8d4523509c8`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 20.7 KB (20671 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.1-alpine`

```console
$ docker pull varnish@sha256:0860b5e9f5535e373080f6921bdb68959dc93c300da569107cfedc45fe236e67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:41f3ee7e8f3a3a46657d7df7ddadd5eea49da1d7186284c299faf77f3cec2c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91658907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791bb19331c2b2bdffebd848babfd121a6021d9427e2c6f475f99a072a619ee8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:23 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_VERSION=8.0.1
# Wed, 15 Apr 2026 20:24:23 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 15 Apr 2026 20:24:23 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VARNISH_SIZE=100M
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VSM_NOPID=1
# Wed, 15 Apr 2026 20:24:23 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
WORKDIR /etc/varnish
# Wed, 15 Apr 2026 20:24:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 15 Apr 2026 20:24:24 GMT
USER varnish
# Wed, 15 Apr 2026 20:24:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 15 Apr 2026 20:24:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679d8a78a51fbc1e26e3a678fe492cb6f2332d4ee6ff65807916cefd5e7a4543`  
		Last Modified: Wed, 15 Apr 2026 20:24:37 GMT  
		Size: 87.8 MB (87791576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbbe98298180f5425cbd3529c155c99c4e2c43a390736a0524bb53683e88a1d`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94df06b538832a31a7961a6b753325a876258ed49ff0bebc40e9f1e3c04d0429`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0000b7ec6e0d633f66fbfb4778f222772737c21df487d6d648510fe7ebeca081`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:121924b23cede2872bba60cfc876f0b636157d3953b18b905da44259989aa0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b064587648707975a1acba9f70f37952c06481aa9895c4baafc8fc2393dfc3a5`

```dockerfile
```

-	Layers:
	-	`sha256:676e5180366d3c79d0802be63ad307362ab73fce89e51c60c4b2fb7c1b54c9e5`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:67be9e66cdb3ad84876f5dad5620896effd2e231ae6a997051af53eacb54e8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83419928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4d2863af766a3f848e4feb44e40779c7c6b89b6ce777ffeb9d0b7b73efab98`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:12 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_VERSION=8.0.1
# Wed, 15 Apr 2026 20:24:12 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 15 Apr 2026 20:24:12 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VARNISH_SIZE=100M
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VSM_NOPID=1
# Wed, 15 Apr 2026 20:24:12 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
WORKDIR /etc/varnish
# Wed, 15 Apr 2026 20:24:12 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 15 Apr 2026 20:24:12 GMT
USER varnish
# Wed, 15 Apr 2026 20:24:12 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 15 Apr 2026 20:24:12 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188f5b124ebe49de1164f7bc653185e82a76feb345a08196cf1a77b777bb7b78`  
		Last Modified: Wed, 15 Apr 2026 20:24:24 GMT  
		Size: 79.2 MB (79216922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da572ca168ae2da5fea13f3ded2448ea2dc618755043a2379de0eeeca56cba1d`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac44db7085a08eafc8087de7e0125e8bf2b440b3971135caf10aa92aebd550f`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191bd24e338faf457cdd8ab90dbc37ac634ed3b5562b7a77c422b9a2d2be6bf3`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:89d178943cec924648184dd343a5ac5570da6c4ec413e190b55be53a2a99fbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da0f9e255d495cc4139c0ffeacb61b4ca2e1599623537a29fb59707161221c2`

```dockerfile
```

-	Layers:
	-	`sha256:2cf9e1788fc9c92f38269c5e206e19918276f8c47b42d246a2d759dbe45e3da9`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9`

```console
$ docker pull varnish@sha256:f0608bcfcfe658eafd2241d95dded61cc69bf955fb0e695a88ca4dee1d662b50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9` - linux; amd64

```console
$ docker pull varnish@sha256:d4e2856f159f4c4cf380fb893cd36f4d6937205f29d62ec34453d8eea44cd99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122267345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fd2d91023cd1c8273d3ce26b2185bffa2dd0f069f7e935d87e9e73745fd82e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:00 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:36:00 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:36:00 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:36:00 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:36:00 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:36:00 GMT
USER varnish
# Wed, 22 Apr 2026 01:36:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:36:00 GMT
CMD []
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601edb7781b9274ac218e7930845a6538310653cb711636fb099263596f2eefd`  
		Last Modified: Wed, 22 Apr 2026 01:36:14 GMT  
		Size: 92.5 MB (92484290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd4de00aad0b69ff3b2f72326caaba6ad41c6a04f12cfa2122fddb510db7baa`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5241f96ed347e1a16d4c2dd38d9c05cd97a5b7df5bf5dccb0b878d3ef53f08d2`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afff8b7ee9ba14e5e92004e2887f23bbd72fd4c8812ad936c6997bb800ad083`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:0f867c8b714583d85915287708a1045ffc825382f0c7eb80797baec76f655d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc38cb393f19bd840c6efe114f940ef1a46984c21d55481be6ffc2d3248fb70`

```dockerfile
```

-	Layers:
	-	`sha256:85f810513181db83064f6da83400d25791193783208a0d85fd84e46477a169e5`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:524b3a703e7fd2a5febff47a18e8c1e4c18b6b10e5231bf05cf52b19c6d70951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116258574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1949bf4e4687183b516beb39d13e89c5bd4ac5b44a00e95cd1a446fce4d47aa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:46 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:46 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:38:46 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:38:46 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:46 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:46 GMT
USER varnish
# Wed, 22 Apr 2026 01:38:46 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:46 GMT
CMD []
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51e88dbbba69d1c081d800c779001a16460d26a17170ac0a926d081e292c6a`  
		Last Modified: Wed, 22 Apr 2026 01:39:02 GMT  
		Size: 86.1 MB (86112080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac720f2cf45b018f15fa42faa7bf3de6f7e70e58ad120a611fba4206ec1570`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93078a388f3f282e7f7420d845ce957923734469a1862dea242eeea169aa9a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebf17e0159fd56e4d39430fbaf0dc5da21e0b7938aa5708aeaf1154024c742`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:e522aa6de935cab70ba77619d50c4fa66cd433443ed1dbba1231019b1a8729fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0e15384eb987ccfb5ba098e98cd04b6b153c719907962d33a0d0e1b4154a6b`

```dockerfile
```

-	Layers:
	-	`sha256:b0504082c9211a3de2803311791e2ccac9179ee556df15d8ccd8b04e5496181a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0`

```console
$ docker pull varnish@sha256:f0608bcfcfe658eafd2241d95dded61cc69bf955fb0e695a88ca4dee1d662b50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0` - linux; amd64

```console
$ docker pull varnish@sha256:d4e2856f159f4c4cf380fb893cd36f4d6937205f29d62ec34453d8eea44cd99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122267345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fd2d91023cd1c8273d3ce26b2185bffa2dd0f069f7e935d87e9e73745fd82e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:00 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:36:00 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:36:00 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:36:00 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:36:00 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:36:00 GMT
USER varnish
# Wed, 22 Apr 2026 01:36:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:36:00 GMT
CMD []
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601edb7781b9274ac218e7930845a6538310653cb711636fb099263596f2eefd`  
		Last Modified: Wed, 22 Apr 2026 01:36:14 GMT  
		Size: 92.5 MB (92484290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd4de00aad0b69ff3b2f72326caaba6ad41c6a04f12cfa2122fddb510db7baa`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5241f96ed347e1a16d4c2dd38d9c05cd97a5b7df5bf5dccb0b878d3ef53f08d2`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afff8b7ee9ba14e5e92004e2887f23bbd72fd4c8812ad936c6997bb800ad083`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:0f867c8b714583d85915287708a1045ffc825382f0c7eb80797baec76f655d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc38cb393f19bd840c6efe114f940ef1a46984c21d55481be6ffc2d3248fb70`

```dockerfile
```

-	Layers:
	-	`sha256:85f810513181db83064f6da83400d25791193783208a0d85fd84e46477a169e5`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:524b3a703e7fd2a5febff47a18e8c1e4c18b6b10e5231bf05cf52b19c6d70951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116258574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1949bf4e4687183b516beb39d13e89c5bd4ac5b44a00e95cd1a446fce4d47aa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:46 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:46 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:38:46 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:38:46 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:46 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:46 GMT
USER varnish
# Wed, 22 Apr 2026 01:38:46 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:46 GMT
CMD []
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51e88dbbba69d1c081d800c779001a16460d26a17170ac0a926d081e292c6a`  
		Last Modified: Wed, 22 Apr 2026 01:39:02 GMT  
		Size: 86.1 MB (86112080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac720f2cf45b018f15fa42faa7bf3de6f7e70e58ad120a611fba4206ec1570`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93078a388f3f282e7f7420d845ce957923734469a1862dea242eeea169aa9a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebf17e0159fd56e4d39430fbaf0dc5da21e0b7938aa5708aeaf1154024c742`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:e522aa6de935cab70ba77619d50c4fa66cd433443ed1dbba1231019b1a8729fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0e15384eb987ccfb5ba098e98cd04b6b153c719907962d33a0d0e1b4154a6b`

```dockerfile
```

-	Layers:
	-	`sha256:b0504082c9211a3de2803311791e2ccac9179ee556df15d8ccd8b04e5496181a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0.1`

```console
$ docker pull varnish@sha256:f0608bcfcfe658eafd2241d95dded61cc69bf955fb0e695a88ca4dee1d662b50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0.1` - linux; amd64

```console
$ docker pull varnish@sha256:d4e2856f159f4c4cf380fb893cd36f4d6937205f29d62ec34453d8eea44cd99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122267345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fd2d91023cd1c8273d3ce26b2185bffa2dd0f069f7e935d87e9e73745fd82e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:00 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:36:00 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:36:00 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:36:00 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:36:00 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:36:00 GMT
USER varnish
# Wed, 22 Apr 2026 01:36:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:36:00 GMT
CMD []
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601edb7781b9274ac218e7930845a6538310653cb711636fb099263596f2eefd`  
		Last Modified: Wed, 22 Apr 2026 01:36:14 GMT  
		Size: 92.5 MB (92484290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd4de00aad0b69ff3b2f72326caaba6ad41c6a04f12cfa2122fddb510db7baa`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5241f96ed347e1a16d4c2dd38d9c05cd97a5b7df5bf5dccb0b878d3ef53f08d2`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afff8b7ee9ba14e5e92004e2887f23bbd72fd4c8812ad936c6997bb800ad083`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:0f867c8b714583d85915287708a1045ffc825382f0c7eb80797baec76f655d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc38cb393f19bd840c6efe114f940ef1a46984c21d55481be6ffc2d3248fb70`

```dockerfile
```

-	Layers:
	-	`sha256:85f810513181db83064f6da83400d25791193783208a0d85fd84e46477a169e5`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:524b3a703e7fd2a5febff47a18e8c1e4c18b6b10e5231bf05cf52b19c6d70951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116258574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1949bf4e4687183b516beb39d13e89c5bd4ac5b44a00e95cd1a446fce4d47aa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:46 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:46 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:38:46 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:38:46 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:46 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:46 GMT
USER varnish
# Wed, 22 Apr 2026 01:38:46 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:46 GMT
CMD []
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51e88dbbba69d1c081d800c779001a16460d26a17170ac0a926d081e292c6a`  
		Last Modified: Wed, 22 Apr 2026 01:39:02 GMT  
		Size: 86.1 MB (86112080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac720f2cf45b018f15fa42faa7bf3de6f7e70e58ad120a611fba4206ec1570`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93078a388f3f282e7f7420d845ce957923734469a1862dea242eeea169aa9a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebf17e0159fd56e4d39430fbaf0dc5da21e0b7938aa5708aeaf1154024c742`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:e522aa6de935cab70ba77619d50c4fa66cd433443ed1dbba1231019b1a8729fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0e15384eb987ccfb5ba098e98cd04b6b153c719907962d33a0d0e1b4154a6b`

```dockerfile
```

-	Layers:
	-	`sha256:b0504082c9211a3de2803311791e2ccac9179ee556df15d8ccd8b04e5496181a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:f0608bcfcfe658eafd2241d95dded61cc69bf955fb0e695a88ca4dee1d662b50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:d4e2856f159f4c4cf380fb893cd36f4d6937205f29d62ec34453d8eea44cd99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122267345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fd2d91023cd1c8273d3ce26b2185bffa2dd0f069f7e935d87e9e73745fd82e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:00 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:36:00 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:36:00 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:36:00 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:36:00 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:36:00 GMT
USER varnish
# Wed, 22 Apr 2026 01:36:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:36:00 GMT
CMD []
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601edb7781b9274ac218e7930845a6538310653cb711636fb099263596f2eefd`  
		Last Modified: Wed, 22 Apr 2026 01:36:14 GMT  
		Size: 92.5 MB (92484290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd4de00aad0b69ff3b2f72326caaba6ad41c6a04f12cfa2122fddb510db7baa`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5241f96ed347e1a16d4c2dd38d9c05cd97a5b7df5bf5dccb0b878d3ef53f08d2`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afff8b7ee9ba14e5e92004e2887f23bbd72fd4c8812ad936c6997bb800ad083`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:0f867c8b714583d85915287708a1045ffc825382f0c7eb80797baec76f655d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc38cb393f19bd840c6efe114f940ef1a46984c21d55481be6ffc2d3248fb70`

```dockerfile
```

-	Layers:
	-	`sha256:85f810513181db83064f6da83400d25791193783208a0d85fd84e46477a169e5`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:524b3a703e7fd2a5febff47a18e8c1e4c18b6b10e5231bf05cf52b19c6d70951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116258574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1949bf4e4687183b516beb39d13e89c5bd4ac5b44a00e95cd1a446fce4d47aa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:46 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:46 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:38:46 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:38:46 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:46 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:46 GMT
USER varnish
# Wed, 22 Apr 2026 01:38:46 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:46 GMT
CMD []
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51e88dbbba69d1c081d800c779001a16460d26a17170ac0a926d081e292c6a`  
		Last Modified: Wed, 22 Apr 2026 01:39:02 GMT  
		Size: 86.1 MB (86112080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac720f2cf45b018f15fa42faa7bf3de6f7e70e58ad120a611fba4206ec1570`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93078a388f3f282e7f7420d845ce957923734469a1862dea242eeea169aa9a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebf17e0159fd56e4d39430fbaf0dc5da21e0b7938aa5708aeaf1154024c742`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:e522aa6de935cab70ba77619d50c4fa66cd433443ed1dbba1231019b1a8729fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0e15384eb987ccfb5ba098e98cd04b6b153c719907962d33a0d0e1b4154a6b`

```dockerfile
```

-	Layers:
	-	`sha256:b0504082c9211a3de2803311791e2ccac9179ee556df15d8ccd8b04e5496181a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:f0608bcfcfe658eafd2241d95dded61cc69bf955fb0e695a88ca4dee1d662b50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:d4e2856f159f4c4cf380fb893cd36f4d6937205f29d62ec34453d8eea44cd99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122267345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fd2d91023cd1c8273d3ce26b2185bffa2dd0f069f7e935d87e9e73745fd82e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:00 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:36:00 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:36:00 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:36:00 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:36:00 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:36:00 GMT
USER varnish
# Wed, 22 Apr 2026 01:36:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:36:00 GMT
CMD []
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601edb7781b9274ac218e7930845a6538310653cb711636fb099263596f2eefd`  
		Last Modified: Wed, 22 Apr 2026 01:36:14 GMT  
		Size: 92.5 MB (92484290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd4de00aad0b69ff3b2f72326caaba6ad41c6a04f12cfa2122fddb510db7baa`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5241f96ed347e1a16d4c2dd38d9c05cd97a5b7df5bf5dccb0b878d3ef53f08d2`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afff8b7ee9ba14e5e92004e2887f23bbd72fd4c8812ad936c6997bb800ad083`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:0f867c8b714583d85915287708a1045ffc825382f0c7eb80797baec76f655d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc38cb393f19bd840c6efe114f940ef1a46984c21d55481be6ffc2d3248fb70`

```dockerfile
```

-	Layers:
	-	`sha256:85f810513181db83064f6da83400d25791193783208a0d85fd84e46477a169e5`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:524b3a703e7fd2a5febff47a18e8c1e4c18b6b10e5231bf05cf52b19c6d70951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116258574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1949bf4e4687183b516beb39d13e89c5bd4ac5b44a00e95cd1a446fce4d47aa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:46 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:46 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:38:46 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:38:46 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:46 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:46 GMT
USER varnish
# Wed, 22 Apr 2026 01:38:46 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:46 GMT
CMD []
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51e88dbbba69d1c081d800c779001a16460d26a17170ac0a926d081e292c6a`  
		Last Modified: Wed, 22 Apr 2026 01:39:02 GMT  
		Size: 86.1 MB (86112080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac720f2cf45b018f15fa42faa7bf3de6f7e70e58ad120a611fba4206ec1570`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93078a388f3f282e7f7420d845ce957923734469a1862dea242eeea169aa9a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebf17e0159fd56e4d39430fbaf0dc5da21e0b7938aa5708aeaf1154024c742`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:e522aa6de935cab70ba77619d50c4fa66cd433443ed1dbba1231019b1a8729fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0e15384eb987ccfb5ba098e98cd04b6b153c719907962d33a0d0e1b4154a6b`

```dockerfile
```

-	Layers:
	-	`sha256:b0504082c9211a3de2803311791e2ccac9179ee556df15d8ccd8b04e5496181a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:7fa8dd2fcdbeaefc29efb96c92dac505eb76ff194593db28632f687ad20ec230
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:0d7c333016f4d2b3a66bc5be6307ae235c6f20b0a5d71169c404e475acea82ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120223887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb157507910bf77f5197f4da860b15ce00571331d6d9e4b128ff9559976caa94`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:04 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 22 Apr 2026 01:36:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 22 Apr 2026 01:36:04 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:36:04 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:36:04 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:36:04 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:36:04 GMT
USER varnish
# Wed, 22 Apr 2026 01:36:04 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:36:04 GMT
CMD []
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13fe021ce98fc3e43723e7d6eac15fa7e57c09454bcdbf055816cd8f0eb3f66`  
		Last Modified: Wed, 22 Apr 2026 01:36:18 GMT  
		Size: 90.4 MB (90440595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd665091af05d185e797f0e25cfa2c7ebba7303f69cbb1071e23ac0f13e97f32`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1b61c9f2264ebe42547ca72098767d2bd98eb008dd8603043987576a7b32f1`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4694eb4d823ed6d46fda0ed742c60b52221d9f1dd3c2ba7ec9fa67d1bf2ac1`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:5a0509b660617508db280d9b212d0bcb97434d5ab67ec8c52791555324fa7141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0653a73fecbd756b34b5b735f68d7667a88c3e199c91c378f582d19f7d6fde1`

```dockerfile
```

-	Layers:
	-	`sha256:d7f20852d018cab3bd1ebc3f8946cd01956a95d2e24b1e765ee2afa53355c228`  
		Last Modified: Wed, 22 Apr 2026 01:36:16 GMT  
		Size: 20.6 KB (20566 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:52862dbab6a067932694258f3537003d531fbdb83ecb57d6bd3fc23a1e6133f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114223681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f56b3f99a36d1369fc3e9f67daab174f101df81ef42245cdcf1373ed7e536`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:51 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 22 Apr 2026 01:38:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 22 Apr 2026 01:38:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:51 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:38:51 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:51 GMT
USER varnish
# Wed, 22 Apr 2026 01:38:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:51 GMT
CMD []
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafd7766e5127767b5b73b02696b18df5e05c79c066ca1ba3dd03f8c184766ef`  
		Last Modified: Wed, 22 Apr 2026 01:39:05 GMT  
		Size: 84.1 MB (84076958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a7d79f36816eb049aa66034af5058439fe387ba9fc3fc951f1c729ae61e54`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d79a8a35d70caadc22937595fd60dcb0e856079b34513fbc53e15c5597733`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d82b935e13bb0df346909afb500e111a6054f6c92294df2b3a1026e77ce7db`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:e267c9e599c04d4449f03ae59c502a07ec2d8388a8c0689e85f8ac1c7ee74ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1497c254c5a9d6ced5afadcf08a8f169b34f428363334beb851beada8ab08a37`

```dockerfile
```

-	Layers:
	-	`sha256:772a91d4e68d1310789627a9d789cdd14a324d171027ae540dadd8d4523509c8`  
		Last Modified: Wed, 22 Apr 2026 01:39:03 GMT  
		Size: 20.7 KB (20671 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:0860b5e9f5535e373080f6921bdb68959dc93c300da569107cfedc45fe236e67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:41f3ee7e8f3a3a46657d7df7ddadd5eea49da1d7186284c299faf77f3cec2c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91658907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791bb19331c2b2bdffebd848babfd121a6021d9427e2c6f475f99a072a619ee8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:23 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_VERSION=8.0.1
# Wed, 15 Apr 2026 20:24:23 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 15 Apr 2026 20:24:23 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VARNISH_SIZE=100M
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VSM_NOPID=1
# Wed, 15 Apr 2026 20:24:23 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
WORKDIR /etc/varnish
# Wed, 15 Apr 2026 20:24:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 15 Apr 2026 20:24:24 GMT
USER varnish
# Wed, 15 Apr 2026 20:24:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 15 Apr 2026 20:24:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679d8a78a51fbc1e26e3a678fe492cb6f2332d4ee6ff65807916cefd5e7a4543`  
		Last Modified: Wed, 15 Apr 2026 20:24:37 GMT  
		Size: 87.8 MB (87791576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbbe98298180f5425cbd3529c155c99c4e2c43a390736a0524bb53683e88a1d`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94df06b538832a31a7961a6b753325a876258ed49ff0bebc40e9f1e3c04d0429`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0000b7ec6e0d633f66fbfb4778f222772737c21df487d6d648510fe7ebeca081`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:121924b23cede2872bba60cfc876f0b636157d3953b18b905da44259989aa0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b064587648707975a1acba9f70f37952c06481aa9895c4baafc8fc2393dfc3a5`

```dockerfile
```

-	Layers:
	-	`sha256:676e5180366d3c79d0802be63ad307362ab73fce89e51c60c4b2fb7c1b54c9e5`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:67be9e66cdb3ad84876f5dad5620896effd2e231ae6a997051af53eacb54e8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83419928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4d2863af766a3f848e4feb44e40779c7c6b89b6ce777ffeb9d0b7b73efab98`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:12 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_VERSION=8.0.1
# Wed, 15 Apr 2026 20:24:12 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 15 Apr 2026 20:24:12 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VARNISH_SIZE=100M
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VSM_NOPID=1
# Wed, 15 Apr 2026 20:24:12 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
WORKDIR /etc/varnish
# Wed, 15 Apr 2026 20:24:12 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 15 Apr 2026 20:24:12 GMT
USER varnish
# Wed, 15 Apr 2026 20:24:12 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 15 Apr 2026 20:24:12 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188f5b124ebe49de1164f7bc653185e82a76feb345a08196cf1a77b777bb7b78`  
		Last Modified: Wed, 15 Apr 2026 20:24:24 GMT  
		Size: 79.2 MB (79216922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da572ca168ae2da5fea13f3ded2448ea2dc618755043a2379de0eeeca56cba1d`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac44db7085a08eafc8087de7e0125e8bf2b440b3971135caf10aa92aebd550f`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191bd24e338faf457cdd8ab90dbc37ac634ed3b5562b7a77c422b9a2d2be6bf3`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:89d178943cec924648184dd343a5ac5570da6c4ec413e190b55be53a2a99fbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da0f9e255d495cc4139c0ffeacb61b4ca2e1599623537a29fb59707161221c2`

```dockerfile
```

-	Layers:
	-	`sha256:2cf9e1788fc9c92f38269c5e206e19918276f8c47b42d246a2d759dbe45e3da9`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:5a330531aed44556cb3945541e545ee72883e95c02004a90e0de9d9d4095c2e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:d7470c7890e171e9d092e0341de3f0b816224fce30c7d4c5d938f77da4f9ab56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121845786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45d675741188122757da0f492460259a71a0b8ef0e0fed186d26d238ed46449`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:35:24 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:35:24 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Wed, 22 Apr 2026 01:35:24 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:35:24 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:35:24 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:35:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:35:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:35:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:35:24 GMT
CMD []
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428831b534d63ea84ae32b63b89352efb0090a51ec53adca52c20daf8c61ed5`  
		Last Modified: Wed, 22 Apr 2026 01:35:38 GMT  
		Size: 93.6 MB (93608783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ed50d38925630e1365fcfc59ae9af553ee92efeba5b5fddb0f619da147e21`  
		Last Modified: Wed, 22 Apr 2026 01:35:35 GMT  
		Size: 719.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:4d8885d15e8ad327757cc9af7d9d19d1ffb9054cfb6fcf9aec1e2095f0130e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b9f24314d0f95ed439d9dd32076f2f77751396474725ee8461d7334ddab706`

```dockerfile
```

-	Layers:
	-	`sha256:b5efb2061b3a5a62abd9b670bc433fea46b64575de786bb82ca8c623a58174cf`  
		Last Modified: Wed, 22 Apr 2026 01:35:35 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:51aab920607f22b9b4b92e2a4263397ed679206af6280dd5eec0ba6128e4642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116282023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758f6baa0188670ac0cca26ad29c5cd562de377f21f4f41b9813aa5e859063e9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:38:30 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:30 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Wed, 22 Apr 2026 01:38:30 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:30 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:30 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:30 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:30 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:30 GMT
CMD []
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522c865a1a54eb735fca6d3bf5028dadb14227f8380fe813af1385c80230d29a`  
		Last Modified: Wed, 22 Apr 2026 01:38:44 GMT  
		Size: 88.2 MB (88165156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66318508b57a6194c6e839ff16e5796d0fb09317a44ad26663f4635ace80808f`  
		Last Modified: Wed, 22 Apr 2026 01:38:42 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:a1d5e941f4f75457809893d805774755e6ec4665c5175a3e589c488b6ce07e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77747cb1d135fd70a706bc5e1d64b09bca10c685f35ed9a958fa1a591fe37875`

```dockerfile
```

-	Layers:
	-	`sha256:ee8295a66738c6a3e8f816c3738eab8d8cc432f2a11934f3bc47824084752f3f`  
		Last Modified: Wed, 22 Apr 2026 01:38:42 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json
