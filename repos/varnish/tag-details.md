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
-	[`varnish:9.0.0`](#varnish900)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:old`](#varnishold)
-	[`varnish:old-alpine`](#varnishold-alpine)
-	[`varnish:stable`](#varnishstable)

## `varnish:6.0`

```console
$ docker pull varnish@sha256:0d15a35db7861a1405c663c3698661ab48d44c62033d1de01f4b179bd67bfea5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:c615a265cfab1c818ac433e143023312e8b8eb8d84a95f010d04ec26f6a90db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121834260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76909c248e91d721b1c79c9888765a713a3f8999282b8111bf2187bd6551650c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 23 Mar 2026 21:13:07 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:07 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Mon, 23 Mar 2026 21:13:07 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:07 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:07 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:07 GMT
CMD []
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a8200ce1afc03bd4213cda0f93efae1d9fa6d153693d93ba296691f764e6bd`  
		Last Modified: Mon, 23 Mar 2026 21:13:21 GMT  
		Size: 93.6 MB (93597279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43fc935c97cdcaf115ea63f731159a6804a7625c965b264d8aedd4e999bf06b`  
		Last Modified: Mon, 23 Mar 2026 21:13:19 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:d0494c2a51aaeae230225429494430c80a28e6c81d75f339922d60438c41ea4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b993d22883433982f51b1afbcc4dbd49084ce07b675631c5ed51064c4e67057`

```dockerfile
```

-	Layers:
	-	`sha256:577aaac6979eee466ed802d68e3e891ab613d13fb8df461281c8352dcda85ff0`  
		Last Modified: Mon, 23 Mar 2026 21:13:19 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e9715b366f3455ea91be0a94011100f40eb9b029ef83d37583aade7dbe2967d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116272694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbf98f80b6b8de49b3e19f78848bcd65b2c7bfbcd99528237507d189f8df99a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 23 Mar 2026 21:13:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:13 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Mon, 23 Mar 2026 21:13:13 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:13 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:13 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:13 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:13 GMT
CMD []
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2708264724e9892a90b168ac157338e36dad9a162a59bf9d43620b1215166a0`  
		Last Modified: Mon, 23 Mar 2026 21:13:27 GMT  
		Size: 88.2 MB (88155873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecba3d0b9410b0a4540bb613f7db73f9b2dbbb6fdebde8b3ec81443aca83014`  
		Last Modified: Mon, 23 Mar 2026 21:13:25 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:1923d8f6527eb359e44de59e310740d46580cc067c429512933dce48efe391c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a4ccdc8dca405b4e766c7416f611cab838d04cb53efd0d7a85eaea1dba546d`

```dockerfile
```

-	Layers:
	-	`sha256:6a276baefac7277c9183fd696a455d1d4d303238d8672202e5aaee20bdce02ff`  
		Last Modified: Mon, 23 Mar 2026 21:13:25 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.17`

```console
$ docker pull varnish@sha256:0d15a35db7861a1405c663c3698661ab48d44c62033d1de01f4b179bd67bfea5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0.17` - linux; amd64

```console
$ docker pull varnish@sha256:c615a265cfab1c818ac433e143023312e8b8eb8d84a95f010d04ec26f6a90db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121834260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76909c248e91d721b1c79c9888765a713a3f8999282b8111bf2187bd6551650c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 23 Mar 2026 21:13:07 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:07 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Mon, 23 Mar 2026 21:13:07 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:07 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:07 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:07 GMT
CMD []
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a8200ce1afc03bd4213cda0f93efae1d9fa6d153693d93ba296691f764e6bd`  
		Last Modified: Mon, 23 Mar 2026 21:13:21 GMT  
		Size: 93.6 MB (93597279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43fc935c97cdcaf115ea63f731159a6804a7625c965b264d8aedd4e999bf06b`  
		Last Modified: Mon, 23 Mar 2026 21:13:19 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.17` - unknown; unknown

```console
$ docker pull varnish@sha256:d0494c2a51aaeae230225429494430c80a28e6c81d75f339922d60438c41ea4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b993d22883433982f51b1afbcc4dbd49084ce07b675631c5ed51064c4e67057`

```dockerfile
```

-	Layers:
	-	`sha256:577aaac6979eee466ed802d68e3e891ab613d13fb8df461281c8352dcda85ff0`  
		Last Modified: Mon, 23 Mar 2026 21:13:19 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.17` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e9715b366f3455ea91be0a94011100f40eb9b029ef83d37583aade7dbe2967d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116272694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbf98f80b6b8de49b3e19f78848bcd65b2c7bfbcd99528237507d189f8df99a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 23 Mar 2026 21:13:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:13 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Mon, 23 Mar 2026 21:13:13 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:13 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:13 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:13 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:13 GMT
CMD []
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2708264724e9892a90b168ac157338e36dad9a162a59bf9d43620b1215166a0`  
		Last Modified: Mon, 23 Mar 2026 21:13:27 GMT  
		Size: 88.2 MB (88155873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecba3d0b9410b0a4540bb613f7db73f9b2dbbb6fdebde8b3ec81443aca83014`  
		Last Modified: Mon, 23 Mar 2026 21:13:25 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.17` - unknown; unknown

```console
$ docker pull varnish@sha256:1923d8f6527eb359e44de59e310740d46580cc067c429512933dce48efe391c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a4ccdc8dca405b4e766c7416f611cab838d04cb53efd0d7a85eaea1dba546d`

```dockerfile
```

-	Layers:
	-	`sha256:6a276baefac7277c9183fd696a455d1d4d303238d8672202e5aaee20bdce02ff`  
		Last Modified: Mon, 23 Mar 2026 21:13:25 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8`

```console
$ docker pull varnish@sha256:27fe28746312f82899ef3641365858cfd057ed177db6e986ecfc9896868b59eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8` - linux; amd64

```console
$ docker pull varnish@sha256:9a8e05ecd244feec8d38b7c9ec13b6ff50473f995a99f145c81ec4c0c4651a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118969795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9816e9caeff0309576e279a3a52a06f249bb1b23f6464c995ef6ba7b5f2022`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:13:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:39 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:39 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:39 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:39 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f975bb7529e7812049c30fdeb2287d6a601f3a13dbdbcc12ad554cfc065b3`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 89.2 MB (89191176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92de269be7dcff60a0a7dcb234c98e27736105551e913be612f18c46fbe17eda`  
		Last Modified: Mon, 23 Mar 2026 21:13:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ff401e2d3f450d97c4ff16bfa13ca6eae3b4dd544db95b843be43e091c87f3`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8846f3613a686868ecbe8f7bd14ba27849d74b8cf462059876fd1b379ee5e`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:774ca949ecd7fc78b6d9dfbb34be68675c2a5e4f70be3a8f06358b8b49383fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b22837ddba04dd9c5ba05a18fe3f9f8d8bd97ef0372605f1b3c292edad969c7`

```dockerfile
```

-	Layers:
	-	`sha256:13ef1e2c8a016d78decab0ce3c2b2bfb42ce16c81a4d3ec5cc1028460d02f066`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 20.6 KB (20567 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7545f1e899d41503707e183811da9211bc08752ac539057666d8ccb069e5ef97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112980406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3567afa5746e3ae986b003e711b9d2dd9dbc1b8343136ce5fd259f11b58cbe4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:13:20 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:20 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:20 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:20 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:20 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36624dda4d4a5f22031a8ecf277784dba0a51791c09f194e02d3cb8e06eac4b`  
		Last Modified: Mon, 23 Mar 2026 21:13:34 GMT  
		Size: 82.8 MB (82838865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c73e6ee3d4b1dd4430becaf9a71332ce89a3147e95eec7c67b10a20cb61da2b`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4f0f61b58654e60852827d3f5fe2ee63024ba878f113d7e86bc39df02efe71`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad10485b0ebb7a62b63fe02901a382d88a869cbb0599215a489305de05248cc`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:5875d10850c185d6faeb313433894e9d90761acfeb0796b2606d7d0d546dab43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e262802a35234b84b6651ee519ddcfafe9b29ac25e87e07089b677902dc17145`

```dockerfile
```

-	Layers:
	-	`sha256:1d8871e49a96b450a0c5008c1edcbe6fc9154433a1c395498603d002c955dc4b`  
		Last Modified: Mon, 23 Mar 2026 21:13:31 GMT  
		Size: 20.7 KB (20670 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8-alpine`

```console
$ docker pull varnish@sha256:6951946bb82d7cd8e9e1c866ecfe25ae95aa4200c4a88ebd9c49f4dcdf3b26da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:ff7b8e557befb88a7e32161e502dc17f1c390148eb4b5aa40fbf430f42bda3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91704851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c51e3ad6c57540b305abc5e2395c4592823be6b68377dcdbe05bc25b3fffdff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 21:13:42 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_VERSION=8.0.1
# Mon, 23 Mar 2026 21:13:42 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:42 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:42 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:42 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:42 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:43 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:43 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:43 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:43 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206097f4181c9fa4590a2371688ec2119bc36496d8af7eb109bddfc3ac66c60`  
		Last Modified: Mon, 23 Mar 2026 21:13:57 GMT  
		Size: 87.8 MB (87839887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bd9f173e9285143c2c21f2e29a944cec96b4c6e290d39f6b21582c33c73b2f`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3156a7bc99ed24b11f65d33cdad0ff7f1f005429c1cfd8506dd7e2628286cead`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c026f4d3ee5aa5de156c6f42e55ce767006671ded719b46e12df05e035b4d686`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:58e15d7406750f2fd2729d1d4487d270c336a37a4b4dcb2df4fb7603f3d2a339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed36101bbde00452cde137596a63f8061b17f73f5c47fabfb0b44d53ee8feafd`

```dockerfile
```

-	Layers:
	-	`sha256:d6d20eb725eb2633b8a25b87ec89de83be31d4ff6586ec371fe168d896ce0a59`  
		Last Modified: Mon, 23 Mar 2026 21:13:55 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:82ebd7b638c190b9377c18fe6521eb82c55b238f7e891c91efaea21089032b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83462349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d42b11254a33f07217d43166bd040f1006dbaf25dc40680801ebeda1051fc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 21:13:51 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_VERSION=8.0.1
# Mon, 23 Mar 2026 21:13:51 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:51 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:51 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:51 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9ad70109afe8d82eaaa011549528d090df0d5d0d9cecbc4cc2bfe54457c3c1`  
		Last Modified: Mon, 23 Mar 2026 21:14:05 GMT  
		Size: 79.3 MB (79262120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be347025ff924b1e32d83d731c5d87b0dacb89c1d3de796e1441afa3a336d031`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1258fa3292dfb4cfc41530b03a50383b81ae32873f76c10e06aec2377fcc24f5`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63020009814ee7a38c936c50f5115cfe979cb9163ed0c9a203b3a2e9cdaf58df`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:bd8fd92b77b84b16579b46155bd2bb60bb945c516913ed1414c15aaa38ece413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98d8cf1665d32e833346bf8e61262a7b5a8ec24c8b1eccd24798eecedfa099f`

```dockerfile
```

-	Layers:
	-	`sha256:41c749bc136cb406afc5928735cad6d77e080fb04d426517944569b98caabad1`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 20.6 KB (20571 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0`

```console
$ docker pull varnish@sha256:27fe28746312f82899ef3641365858cfd057ed177db6e986ecfc9896868b59eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0` - linux; amd64

```console
$ docker pull varnish@sha256:9a8e05ecd244feec8d38b7c9ec13b6ff50473f995a99f145c81ec4c0c4651a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118969795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9816e9caeff0309576e279a3a52a06f249bb1b23f6464c995ef6ba7b5f2022`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:13:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:39 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:39 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:39 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:39 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f975bb7529e7812049c30fdeb2287d6a601f3a13dbdbcc12ad554cfc065b3`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 89.2 MB (89191176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92de269be7dcff60a0a7dcb234c98e27736105551e913be612f18c46fbe17eda`  
		Last Modified: Mon, 23 Mar 2026 21:13:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ff401e2d3f450d97c4ff16bfa13ca6eae3b4dd544db95b843be43e091c87f3`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8846f3613a686868ecbe8f7bd14ba27849d74b8cf462059876fd1b379ee5e`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:774ca949ecd7fc78b6d9dfbb34be68675c2a5e4f70be3a8f06358b8b49383fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b22837ddba04dd9c5ba05a18fe3f9f8d8bd97ef0372605f1b3c292edad969c7`

```dockerfile
```

-	Layers:
	-	`sha256:13ef1e2c8a016d78decab0ce3c2b2bfb42ce16c81a4d3ec5cc1028460d02f066`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 20.6 KB (20567 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7545f1e899d41503707e183811da9211bc08752ac539057666d8ccb069e5ef97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112980406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3567afa5746e3ae986b003e711b9d2dd9dbc1b8343136ce5fd259f11b58cbe4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:13:20 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:20 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:20 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:20 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:20 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36624dda4d4a5f22031a8ecf277784dba0a51791c09f194e02d3cb8e06eac4b`  
		Last Modified: Mon, 23 Mar 2026 21:13:34 GMT  
		Size: 82.8 MB (82838865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c73e6ee3d4b1dd4430becaf9a71332ce89a3147e95eec7c67b10a20cb61da2b`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4f0f61b58654e60852827d3f5fe2ee63024ba878f113d7e86bc39df02efe71`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad10485b0ebb7a62b63fe02901a382d88a869cbb0599215a489305de05248cc`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:5875d10850c185d6faeb313433894e9d90761acfeb0796b2606d7d0d546dab43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e262802a35234b84b6651ee519ddcfafe9b29ac25e87e07089b677902dc17145`

```dockerfile
```

-	Layers:
	-	`sha256:1d8871e49a96b450a0c5008c1edcbe6fc9154433a1c395498603d002c955dc4b`  
		Last Modified: Mon, 23 Mar 2026 21:13:31 GMT  
		Size: 20.7 KB (20670 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0-alpine`

```console
$ docker pull varnish@sha256:6951946bb82d7cd8e9e1c866ecfe25ae95aa4200c4a88ebd9c49f4dcdf3b26da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:ff7b8e557befb88a7e32161e502dc17f1c390148eb4b5aa40fbf430f42bda3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91704851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c51e3ad6c57540b305abc5e2395c4592823be6b68377dcdbe05bc25b3fffdff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 21:13:42 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_VERSION=8.0.1
# Mon, 23 Mar 2026 21:13:42 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:42 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:42 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:42 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:42 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:43 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:43 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:43 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:43 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206097f4181c9fa4590a2371688ec2119bc36496d8af7eb109bddfc3ac66c60`  
		Last Modified: Mon, 23 Mar 2026 21:13:57 GMT  
		Size: 87.8 MB (87839887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bd9f173e9285143c2c21f2e29a944cec96b4c6e290d39f6b21582c33c73b2f`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3156a7bc99ed24b11f65d33cdad0ff7f1f005429c1cfd8506dd7e2628286cead`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c026f4d3ee5aa5de156c6f42e55ce767006671ded719b46e12df05e035b4d686`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:58e15d7406750f2fd2729d1d4487d270c336a37a4b4dcb2df4fb7603f3d2a339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed36101bbde00452cde137596a63f8061b17f73f5c47fabfb0b44d53ee8feafd`

```dockerfile
```

-	Layers:
	-	`sha256:d6d20eb725eb2633b8a25b87ec89de83be31d4ff6586ec371fe168d896ce0a59`  
		Last Modified: Mon, 23 Mar 2026 21:13:55 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:82ebd7b638c190b9377c18fe6521eb82c55b238f7e891c91efaea21089032b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83462349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d42b11254a33f07217d43166bd040f1006dbaf25dc40680801ebeda1051fc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 21:13:51 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_VERSION=8.0.1
# Mon, 23 Mar 2026 21:13:51 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:51 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:51 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:51 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9ad70109afe8d82eaaa011549528d090df0d5d0d9cecbc4cc2bfe54457c3c1`  
		Last Modified: Mon, 23 Mar 2026 21:14:05 GMT  
		Size: 79.3 MB (79262120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be347025ff924b1e32d83d731c5d87b0dacb89c1d3de796e1441afa3a336d031`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1258fa3292dfb4cfc41530b03a50383b81ae32873f76c10e06aec2377fcc24f5`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63020009814ee7a38c936c50f5115cfe979cb9163ed0c9a203b3a2e9cdaf58df`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:bd8fd92b77b84b16579b46155bd2bb60bb945c516913ed1414c15aaa38ece413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98d8cf1665d32e833346bf8e61262a7b5a8ec24c8b1eccd24798eecedfa099f`

```dockerfile
```

-	Layers:
	-	`sha256:41c749bc136cb406afc5928735cad6d77e080fb04d426517944569b98caabad1`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 20.6 KB (20571 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.1`

```console
$ docker pull varnish@sha256:27fe28746312f82899ef3641365858cfd057ed177db6e986ecfc9896868b59eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.1` - linux; amd64

```console
$ docker pull varnish@sha256:9a8e05ecd244feec8d38b7c9ec13b6ff50473f995a99f145c81ec4c0c4651a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118969795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9816e9caeff0309576e279a3a52a06f249bb1b23f6464c995ef6ba7b5f2022`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:13:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:39 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:39 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:39 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:39 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f975bb7529e7812049c30fdeb2287d6a601f3a13dbdbcc12ad554cfc065b3`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 89.2 MB (89191176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92de269be7dcff60a0a7dcb234c98e27736105551e913be612f18c46fbe17eda`  
		Last Modified: Mon, 23 Mar 2026 21:13:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ff401e2d3f450d97c4ff16bfa13ca6eae3b4dd544db95b843be43e091c87f3`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8846f3613a686868ecbe8f7bd14ba27849d74b8cf462059876fd1b379ee5e`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:774ca949ecd7fc78b6d9dfbb34be68675c2a5e4f70be3a8f06358b8b49383fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b22837ddba04dd9c5ba05a18fe3f9f8d8bd97ef0372605f1b3c292edad969c7`

```dockerfile
```

-	Layers:
	-	`sha256:13ef1e2c8a016d78decab0ce3c2b2bfb42ce16c81a4d3ec5cc1028460d02f066`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 20.6 KB (20567 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7545f1e899d41503707e183811da9211bc08752ac539057666d8ccb069e5ef97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112980406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3567afa5746e3ae986b003e711b9d2dd9dbc1b8343136ce5fd259f11b58cbe4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:13:20 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:20 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:20 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:20 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:20 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36624dda4d4a5f22031a8ecf277784dba0a51791c09f194e02d3cb8e06eac4b`  
		Last Modified: Mon, 23 Mar 2026 21:13:34 GMT  
		Size: 82.8 MB (82838865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c73e6ee3d4b1dd4430becaf9a71332ce89a3147e95eec7c67b10a20cb61da2b`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4f0f61b58654e60852827d3f5fe2ee63024ba878f113d7e86bc39df02efe71`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad10485b0ebb7a62b63fe02901a382d88a869cbb0599215a489305de05248cc`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:5875d10850c185d6faeb313433894e9d90761acfeb0796b2606d7d0d546dab43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e262802a35234b84b6651ee519ddcfafe9b29ac25e87e07089b677902dc17145`

```dockerfile
```

-	Layers:
	-	`sha256:1d8871e49a96b450a0c5008c1edcbe6fc9154433a1c395498603d002c955dc4b`  
		Last Modified: Mon, 23 Mar 2026 21:13:31 GMT  
		Size: 20.7 KB (20670 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8.0.1-alpine`

```console
$ docker pull varnish@sha256:6951946bb82d7cd8e9e1c866ecfe25ae95aa4200c4a88ebd9c49f4dcdf3b26da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.1-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:ff7b8e557befb88a7e32161e502dc17f1c390148eb4b5aa40fbf430f42bda3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91704851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c51e3ad6c57540b305abc5e2395c4592823be6b68377dcdbe05bc25b3fffdff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 21:13:42 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_VERSION=8.0.1
# Mon, 23 Mar 2026 21:13:42 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:42 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:42 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:42 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:42 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:43 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:43 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:43 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:43 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206097f4181c9fa4590a2371688ec2119bc36496d8af7eb109bddfc3ac66c60`  
		Last Modified: Mon, 23 Mar 2026 21:13:57 GMT  
		Size: 87.8 MB (87839887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bd9f173e9285143c2c21f2e29a944cec96b4c6e290d39f6b21582c33c73b2f`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3156a7bc99ed24b11f65d33cdad0ff7f1f005429c1cfd8506dd7e2628286cead`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c026f4d3ee5aa5de156c6f42e55ce767006671ded719b46e12df05e035b4d686`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:58e15d7406750f2fd2729d1d4487d270c336a37a4b4dcb2df4fb7603f3d2a339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed36101bbde00452cde137596a63f8061b17f73f5c47fabfb0b44d53ee8feafd`

```dockerfile
```

-	Layers:
	-	`sha256:d6d20eb725eb2633b8a25b87ec89de83be31d4ff6586ec371fe168d896ce0a59`  
		Last Modified: Mon, 23 Mar 2026 21:13:55 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.1-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:82ebd7b638c190b9377c18fe6521eb82c55b238f7e891c91efaea21089032b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83462349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d42b11254a33f07217d43166bd040f1006dbaf25dc40680801ebeda1051fc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 21:13:51 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_VERSION=8.0.1
# Mon, 23 Mar 2026 21:13:51 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:51 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:51 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:51 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9ad70109afe8d82eaaa011549528d090df0d5d0d9cecbc4cc2bfe54457c3c1`  
		Last Modified: Mon, 23 Mar 2026 21:14:05 GMT  
		Size: 79.3 MB (79262120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be347025ff924b1e32d83d731c5d87b0dacb89c1d3de796e1441afa3a336d031`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1258fa3292dfb4cfc41530b03a50383b81ae32873f76c10e06aec2377fcc24f5`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63020009814ee7a38c936c50f5115cfe979cb9163ed0c9a203b3a2e9cdaf58df`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:bd8fd92b77b84b16579b46155bd2bb60bb945c516913ed1414c15aaa38ece413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98d8cf1665d32e833346bf8e61262a7b5a8ec24c8b1eccd24798eecedfa099f`

```dockerfile
```

-	Layers:
	-	`sha256:41c749bc136cb406afc5928735cad6d77e080fb04d426517944569b98caabad1`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 20.6 KB (20571 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9`

```console
$ docker pull varnish@sha256:7146c8185a24b42d2233bb669b86fea12c1623dc922cc950efee17ba3a9b8921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9` - linux; amd64

```console
$ docker pull varnish@sha256:2f459717bad8b2b08fbf29c8b74f2c22a056c3ee69f17ca2678bccf411339c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (121020566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa9537475cb0751c7bec4b57410e6276d332e4106b2cbc9a867b497c190b0a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:25 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:25 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:25 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:25 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:25 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:25 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:25 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956defc67a0580f9fd9ee9407db7c652c7ae707204582808de58228c8154abdd`  
		Last Modified: Mon, 23 Mar 2026 21:12:41 GMT  
		Size: 91.2 MB (91242179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bdea834e2af1aac140374d19b13f1fede3f60320c6365d7b7f5c55a0496c47`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb43ba12a60fced427e2753efaaf818565598fc7b189b0e4c718d8c32fd2a0c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc71a769554ee2326e001a2f67c5e49424a5debd7c04b516967a29caf40a855`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:59feb0220565bbedaec23456b16c70c5403706af9c750a9c2bd165c38b49bbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab06dee630f531bf1ff657b84ea07c794fd29b65a1621ef4fcad646d20f8f6`

```dockerfile
```

-	Layers:
	-	`sha256:f10bdae9217fdc56afbf0f3fb942d0bd47c6fab87b3b92f83a7ab736aaad812e`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a50418e84d3a7744da85152619b0babca188f19eccd3354552dde8cdecd98f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115018223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb34cdfd366eb7d518256e6b50ae5a6af0bbcb45a9d3948d8aff09008633650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:34 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:34 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:34 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:34 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:34 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:34 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:34 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ef81572ab25406c274dcdf5f919e59349d81a2ca4799bc60f6c1245e9b4e8`  
		Last Modified: Mon, 23 Mar 2026 21:12:47 GMT  
		Size: 84.9 MB (84876921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ecea7934d0b71ae0729994a89929966fc2a9852f06c121fcb5ed212068cd5e`  
		Last Modified: Mon, 23 Mar 2026 21:12:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaf1775d15b64385d723efebe785407fab2d9711d03b62e45625f1f0aad37c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb348ae1c19f498939a0eea32a13b1a3133e6a4d9d3861f043b9de89e36ed34`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:1b8dd378d06ce571a5f031d9d126933149a1af5d3a5fc61af35b00ce4fc5deec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553cc8148a431217ceddfce685ea8faec17906db96d1cee2e69d89f141db92ec`

```dockerfile
```

-	Layers:
	-	`sha256:b2edf9e74c2fffe31f33d731559e82ad854cb1494fb777a76ddb4dac28cf9e0e`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0`

```console
$ docker pull varnish@sha256:7146c8185a24b42d2233bb669b86fea12c1623dc922cc950efee17ba3a9b8921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0` - linux; amd64

```console
$ docker pull varnish@sha256:2f459717bad8b2b08fbf29c8b74f2c22a056c3ee69f17ca2678bccf411339c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (121020566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa9537475cb0751c7bec4b57410e6276d332e4106b2cbc9a867b497c190b0a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:25 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:25 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:25 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:25 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:25 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:25 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:25 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956defc67a0580f9fd9ee9407db7c652c7ae707204582808de58228c8154abdd`  
		Last Modified: Mon, 23 Mar 2026 21:12:41 GMT  
		Size: 91.2 MB (91242179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bdea834e2af1aac140374d19b13f1fede3f60320c6365d7b7f5c55a0496c47`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb43ba12a60fced427e2753efaaf818565598fc7b189b0e4c718d8c32fd2a0c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc71a769554ee2326e001a2f67c5e49424a5debd7c04b516967a29caf40a855`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:59feb0220565bbedaec23456b16c70c5403706af9c750a9c2bd165c38b49bbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab06dee630f531bf1ff657b84ea07c794fd29b65a1621ef4fcad646d20f8f6`

```dockerfile
```

-	Layers:
	-	`sha256:f10bdae9217fdc56afbf0f3fb942d0bd47c6fab87b3b92f83a7ab736aaad812e`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a50418e84d3a7744da85152619b0babca188f19eccd3354552dde8cdecd98f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115018223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb34cdfd366eb7d518256e6b50ae5a6af0bbcb45a9d3948d8aff09008633650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:34 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:34 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:34 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:34 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:34 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:34 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:34 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ef81572ab25406c274dcdf5f919e59349d81a2ca4799bc60f6c1245e9b4e8`  
		Last Modified: Mon, 23 Mar 2026 21:12:47 GMT  
		Size: 84.9 MB (84876921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ecea7934d0b71ae0729994a89929966fc2a9852f06c121fcb5ed212068cd5e`  
		Last Modified: Mon, 23 Mar 2026 21:12:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaf1775d15b64385d723efebe785407fab2d9711d03b62e45625f1f0aad37c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb348ae1c19f498939a0eea32a13b1a3133e6a4d9d3861f043b9de89e36ed34`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:1b8dd378d06ce571a5f031d9d126933149a1af5d3a5fc61af35b00ce4fc5deec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553cc8148a431217ceddfce685ea8faec17906db96d1cee2e69d89f141db92ec`

```dockerfile
```

-	Layers:
	-	`sha256:b2edf9e74c2fffe31f33d731559e82ad854cb1494fb777a76ddb4dac28cf9e0e`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0.0`

```console
$ docker pull varnish@sha256:7146c8185a24b42d2233bb669b86fea12c1623dc922cc950efee17ba3a9b8921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0.0` - linux; amd64

```console
$ docker pull varnish@sha256:2f459717bad8b2b08fbf29c8b74f2c22a056c3ee69f17ca2678bccf411339c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (121020566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa9537475cb0751c7bec4b57410e6276d332e4106b2cbc9a867b497c190b0a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:25 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:25 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:25 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:25 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:25 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:25 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:25 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956defc67a0580f9fd9ee9407db7c652c7ae707204582808de58228c8154abdd`  
		Last Modified: Mon, 23 Mar 2026 21:12:41 GMT  
		Size: 91.2 MB (91242179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bdea834e2af1aac140374d19b13f1fede3f60320c6365d7b7f5c55a0496c47`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb43ba12a60fced427e2753efaaf818565598fc7b189b0e4c718d8c32fd2a0c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc71a769554ee2326e001a2f67c5e49424a5debd7c04b516967a29caf40a855`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:59feb0220565bbedaec23456b16c70c5403706af9c750a9c2bd165c38b49bbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab06dee630f531bf1ff657b84ea07c794fd29b65a1621ef4fcad646d20f8f6`

```dockerfile
```

-	Layers:
	-	`sha256:f10bdae9217fdc56afbf0f3fb942d0bd47c6fab87b3b92f83a7ab736aaad812e`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a50418e84d3a7744da85152619b0babca188f19eccd3354552dde8cdecd98f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115018223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb34cdfd366eb7d518256e6b50ae5a6af0bbcb45a9d3948d8aff09008633650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:34 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:34 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:34 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:34 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:34 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:34 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:34 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ef81572ab25406c274dcdf5f919e59349d81a2ca4799bc60f6c1245e9b4e8`  
		Last Modified: Mon, 23 Mar 2026 21:12:47 GMT  
		Size: 84.9 MB (84876921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ecea7934d0b71ae0729994a89929966fc2a9852f06c121fcb5ed212068cd5e`  
		Last Modified: Mon, 23 Mar 2026 21:12:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaf1775d15b64385d723efebe785407fab2d9711d03b62e45625f1f0aad37c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb348ae1c19f498939a0eea32a13b1a3133e6a4d9d3861f043b9de89e36ed34`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.0` - unknown; unknown

```console
$ docker pull varnish@sha256:1b8dd378d06ce571a5f031d9d126933149a1af5d3a5fc61af35b00ce4fc5deec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553cc8148a431217ceddfce685ea8faec17906db96d1cee2e69d89f141db92ec`

```dockerfile
```

-	Layers:
	-	`sha256:b2edf9e74c2fffe31f33d731559e82ad854cb1494fb777a76ddb4dac28cf9e0e`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:7146c8185a24b42d2233bb669b86fea12c1623dc922cc950efee17ba3a9b8921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:2f459717bad8b2b08fbf29c8b74f2c22a056c3ee69f17ca2678bccf411339c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (121020566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa9537475cb0751c7bec4b57410e6276d332e4106b2cbc9a867b497c190b0a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:25 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:25 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:25 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:25 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:25 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:25 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:25 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956defc67a0580f9fd9ee9407db7c652c7ae707204582808de58228c8154abdd`  
		Last Modified: Mon, 23 Mar 2026 21:12:41 GMT  
		Size: 91.2 MB (91242179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bdea834e2af1aac140374d19b13f1fede3f60320c6365d7b7f5c55a0496c47`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb43ba12a60fced427e2753efaaf818565598fc7b189b0e4c718d8c32fd2a0c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc71a769554ee2326e001a2f67c5e49424a5debd7c04b516967a29caf40a855`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:59feb0220565bbedaec23456b16c70c5403706af9c750a9c2bd165c38b49bbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab06dee630f531bf1ff657b84ea07c794fd29b65a1621ef4fcad646d20f8f6`

```dockerfile
```

-	Layers:
	-	`sha256:f10bdae9217fdc56afbf0f3fb942d0bd47c6fab87b3b92f83a7ab736aaad812e`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a50418e84d3a7744da85152619b0babca188f19eccd3354552dde8cdecd98f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115018223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb34cdfd366eb7d518256e6b50ae5a6af0bbcb45a9d3948d8aff09008633650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:34 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:34 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:34 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:34 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:34 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:34 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:34 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ef81572ab25406c274dcdf5f919e59349d81a2ca4799bc60f6c1245e9b4e8`  
		Last Modified: Mon, 23 Mar 2026 21:12:47 GMT  
		Size: 84.9 MB (84876921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ecea7934d0b71ae0729994a89929966fc2a9852f06c121fcb5ed212068cd5e`  
		Last Modified: Mon, 23 Mar 2026 21:12:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaf1775d15b64385d723efebe785407fab2d9711d03b62e45625f1f0aad37c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb348ae1c19f498939a0eea32a13b1a3133e6a4d9d3861f043b9de89e36ed34`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:1b8dd378d06ce571a5f031d9d126933149a1af5d3a5fc61af35b00ce4fc5deec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553cc8148a431217ceddfce685ea8faec17906db96d1cee2e69d89f141db92ec`

```dockerfile
```

-	Layers:
	-	`sha256:b2edf9e74c2fffe31f33d731559e82ad854cb1494fb777a76ddb4dac28cf9e0e`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:7146c8185a24b42d2233bb669b86fea12c1623dc922cc950efee17ba3a9b8921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:2f459717bad8b2b08fbf29c8b74f2c22a056c3ee69f17ca2678bccf411339c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (121020566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa9537475cb0751c7bec4b57410e6276d332e4106b2cbc9a867b497c190b0a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:25 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:25 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:25 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:25 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:25 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:25 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:25 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:25 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956defc67a0580f9fd9ee9407db7c652c7ae707204582808de58228c8154abdd`  
		Last Modified: Mon, 23 Mar 2026 21:12:41 GMT  
		Size: 91.2 MB (91242179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bdea834e2af1aac140374d19b13f1fede3f60320c6365d7b7f5c55a0496c47`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb43ba12a60fced427e2753efaaf818565598fc7b189b0e4c718d8c32fd2a0c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc71a769554ee2326e001a2f67c5e49424a5debd7c04b516967a29caf40a855`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:59feb0220565bbedaec23456b16c70c5403706af9c750a9c2bd165c38b49bbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab06dee630f531bf1ff657b84ea07c794fd29b65a1621ef4fcad646d20f8f6`

```dockerfile
```

-	Layers:
	-	`sha256:f10bdae9217fdc56afbf0f3fb942d0bd47c6fab87b3b92f83a7ab736aaad812e`  
		Last Modified: Mon, 23 Mar 2026 21:12:38 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a50418e84d3a7744da85152619b0babca188f19eccd3354552dde8cdecd98f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115018223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb34cdfd366eb7d518256e6b50ae5a6af0bbcb45a9d3948d8aff09008633650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:12:34 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:12:34 GMT
ARG VARNISH_VERSION_NUMBER=9.0.0-1
# Mon, 23 Mar 2026 21:12:34 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:12:34 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:12:34 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.0-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:12:34 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
COPY index.html /var/www/html/ # buildkit
# Mon, 23 Mar 2026 21:12:34 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:12:34 GMT
USER varnish
# Mon, 23 Mar 2026 21:12:34 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:12:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ef81572ab25406c274dcdf5f919e59349d81a2ca4799bc60f6c1245e9b4e8`  
		Last Modified: Mon, 23 Mar 2026 21:12:47 GMT  
		Size: 84.9 MB (84876921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ecea7934d0b71ae0729994a89929966fc2a9852f06c121fcb5ed212068cd5e`  
		Last Modified: Mon, 23 Mar 2026 21:12:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaf1775d15b64385d723efebe785407fab2d9711d03b62e45625f1f0aad37c2`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb348ae1c19f498939a0eea32a13b1a3133e6a4d9d3861f043b9de89e36ed34`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:1b8dd378d06ce571a5f031d9d126933149a1af5d3a5fc61af35b00ce4fc5deec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553cc8148a431217ceddfce685ea8faec17906db96d1cee2e69d89f141db92ec`

```dockerfile
```

-	Layers:
	-	`sha256:b2edf9e74c2fffe31f33d731559e82ad854cb1494fb777a76ddb4dac28cf9e0e`  
		Last Modified: Mon, 23 Mar 2026 21:12:46 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:27fe28746312f82899ef3641365858cfd057ed177db6e986ecfc9896868b59eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:9a8e05ecd244feec8d38b7c9ec13b6ff50473f995a99f145c81ec4c0c4651a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118969795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9816e9caeff0309576e279a3a52a06f249bb1b23f6464c995ef6ba7b5f2022`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:13:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:39 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:39 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:39 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:39 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:39 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:39 GMT
CMD []
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f975bb7529e7812049c30fdeb2287d6a601f3a13dbdbcc12ad554cfc065b3`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 89.2 MB (89191176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92de269be7dcff60a0a7dcb234c98e27736105551e913be612f18c46fbe17eda`  
		Last Modified: Mon, 23 Mar 2026 21:13:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ff401e2d3f450d97c4ff16bfa13ca6eae3b4dd544db95b843be43e091c87f3`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8846f3613a686868ecbe8f7bd14ba27849d74b8cf462059876fd1b379ee5e`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:774ca949ecd7fc78b6d9dfbb34be68675c2a5e4f70be3a8f06358b8b49383fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b22837ddba04dd9c5ba05a18fe3f9f8d8bd97ef0372605f1b3c292edad969c7`

```dockerfile
```

-	Layers:
	-	`sha256:13ef1e2c8a016d78decab0ce3c2b2bfb42ce16c81a4d3ec5cc1028460d02f066`  
		Last Modified: Mon, 23 Mar 2026 21:13:52 GMT  
		Size: 20.6 KB (20567 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:7545f1e899d41503707e183811da9211bc08752ac539057666d8ccb069e5ef97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112980406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3567afa5746e3ae986b003e711b9d2dd9dbc1b8343136ce5fd259f11b58cbe4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 21:13:20 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:20 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:20 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:20 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:20 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:20 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:20 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:20 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:20 GMT
CMD []
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36624dda4d4a5f22031a8ecf277784dba0a51791c09f194e02d3cb8e06eac4b`  
		Last Modified: Mon, 23 Mar 2026 21:13:34 GMT  
		Size: 82.8 MB (82838865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c73e6ee3d4b1dd4430becaf9a71332ce89a3147e95eec7c67b10a20cb61da2b`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4f0f61b58654e60852827d3f5fe2ee63024ba878f113d7e86bc39df02efe71`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad10485b0ebb7a62b63fe02901a382d88a869cbb0599215a489305de05248cc`  
		Last Modified: Mon, 23 Mar 2026 21:13:32 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:5875d10850c185d6faeb313433894e9d90761acfeb0796b2606d7d0d546dab43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e262802a35234b84b6651ee519ddcfafe9b29ac25e87e07089b677902dc17145`

```dockerfile
```

-	Layers:
	-	`sha256:1d8871e49a96b450a0c5008c1edcbe6fc9154433a1c395498603d002c955dc4b`  
		Last Modified: Mon, 23 Mar 2026 21:13:31 GMT  
		Size: 20.7 KB (20670 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:6951946bb82d7cd8e9e1c866ecfe25ae95aa4200c4a88ebd9c49f4dcdf3b26da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:ff7b8e557befb88a7e32161e502dc17f1c390148eb4b5aa40fbf430f42bda3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91704851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c51e3ad6c57540b305abc5e2395c4592823be6b68377dcdbe05bc25b3fffdff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 21:13:42 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_VERSION=8.0.1
# Mon, 23 Mar 2026 21:13:42 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:42 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:42 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:42 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:42 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:43 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:43 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:43 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:43 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206097f4181c9fa4590a2371688ec2119bc36496d8af7eb109bddfc3ac66c60`  
		Last Modified: Mon, 23 Mar 2026 21:13:57 GMT  
		Size: 87.8 MB (87839887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bd9f173e9285143c2c21f2e29a944cec96b4c6e290d39f6b21582c33c73b2f`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3156a7bc99ed24b11f65d33cdad0ff7f1f005429c1cfd8506dd7e2628286cead`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c026f4d3ee5aa5de156c6f42e55ce767006671ded719b46e12df05e035b4d686`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:58e15d7406750f2fd2729d1d4487d270c336a37a4b4dcb2df4fb7603f3d2a339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed36101bbde00452cde137596a63f8061b17f73f5c47fabfb0b44d53ee8feafd`

```dockerfile
```

-	Layers:
	-	`sha256:d6d20eb725eb2633b8a25b87ec89de83be31d4ff6586ec371fe168d896ce0a59`  
		Last Modified: Mon, 23 Mar 2026 21:13:55 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:82ebd7b638c190b9377c18fe6521eb82c55b238f7e891c91efaea21089032b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83462349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d42b11254a33f07217d43166bd040f1006dbaf25dc40680801ebeda1051fc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 21:13:51 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_VERSION=8.0.1
# Mon, 23 Mar 2026 21:13:51 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:51 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:51 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:51 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9ad70109afe8d82eaaa011549528d090df0d5d0d9cecbc4cc2bfe54457c3c1`  
		Last Modified: Mon, 23 Mar 2026 21:14:05 GMT  
		Size: 79.3 MB (79262120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be347025ff924b1e32d83d731c5d87b0dacb89c1d3de796e1441afa3a336d031`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1258fa3292dfb4cfc41530b03a50383b81ae32873f76c10e06aec2377fcc24f5`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63020009814ee7a38c936c50f5115cfe979cb9163ed0c9a203b3a2e9cdaf58df`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:bd8fd92b77b84b16579b46155bd2bb60bb945c516913ed1414c15aaa38ece413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98d8cf1665d32e833346bf8e61262a7b5a8ec24c8b1eccd24798eecedfa099f`

```dockerfile
```

-	Layers:
	-	`sha256:41c749bc136cb406afc5928735cad6d77e080fb04d426517944569b98caabad1`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 20.6 KB (20571 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:stable`

```console
$ docker pull varnish@sha256:0d15a35db7861a1405c663c3698661ab48d44c62033d1de01f4b179bd67bfea5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:c615a265cfab1c818ac433e143023312e8b8eb8d84a95f010d04ec26f6a90db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121834260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76909c248e91d721b1c79c9888765a713a3f8999282b8111bf2187bd6551650c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 23 Mar 2026 21:13:07 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:07 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Mon, 23 Mar 2026 21:13:07 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:07 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:07 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:07 GMT
CMD []
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a8200ce1afc03bd4213cda0f93efae1d9fa6d153693d93ba296691f764e6bd`  
		Last Modified: Mon, 23 Mar 2026 21:13:21 GMT  
		Size: 93.6 MB (93597279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43fc935c97cdcaf115ea63f731159a6804a7625c965b264d8aedd4e999bf06b`  
		Last Modified: Mon, 23 Mar 2026 21:13:19 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:d0494c2a51aaeae230225429494430c80a28e6c81d75f339922d60438c41ea4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b993d22883433982f51b1afbcc4dbd49084ce07b675631c5ed51064c4e67057`

```dockerfile
```

-	Layers:
	-	`sha256:577aaac6979eee466ed802d68e3e891ab613d13fb8df461281c8352dcda85ff0`  
		Last Modified: Mon, 23 Mar 2026 21:13:19 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:e9715b366f3455ea91be0a94011100f40eb9b029ef83d37583aade7dbe2967d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116272694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbf98f80b6b8de49b3e19f78848bcd65b2c7bfbcd99528237507d189f8df99a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 23 Mar 2026 21:13:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Mon, 23 Mar 2026 21:13:13 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Mon, 23 Mar 2026 21:13:13 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:13 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:13 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:13 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:13 GMT
CMD []
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2708264724e9892a90b168ac157338e36dad9a162a59bf9d43620b1215166a0`  
		Last Modified: Mon, 23 Mar 2026 21:13:27 GMT  
		Size: 88.2 MB (88155873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecba3d0b9410b0a4540bb613f7db73f9b2dbbb6fdebde8b3ec81443aca83014`  
		Last Modified: Mon, 23 Mar 2026 21:13:25 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:1923d8f6527eb359e44de59e310740d46580cc067c429512933dce48efe391c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a4ccdc8dca405b4e766c7416f611cab838d04cb53efd0d7a85eaea1dba546d`

```dockerfile
```

-	Layers:
	-	`sha256:6a276baefac7277c9183fd696a455d1d4d303238d8672202e5aaee20bdce02ff`  
		Last Modified: Mon, 23 Mar 2026 21:13:25 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json
