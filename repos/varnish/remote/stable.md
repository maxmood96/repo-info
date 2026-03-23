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
