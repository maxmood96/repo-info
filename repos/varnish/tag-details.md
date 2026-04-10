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
$ docker pull varnish@sha256:a327469c847044adad0f29d2912abe3ee2078efcc70fa723233a0e2ff033e602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:aa13c718b3982e4703770030f0580d33facdb64dacce0e0d2d9beafc0056c118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121834627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6ed23c3cd7206c4759f32f8f685765ea45fc9b8860284c84ec9474588e8f93`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:42:42 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:42:42 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Tue, 07 Apr 2026 01:42:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:42:42 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:42:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:42:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:42:42 GMT
CMD []
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087951f710c0e407d30ec37397fe6623bd8a28d5ae98e14136b127c1103d6892`  
		Last Modified: Tue, 07 Apr 2026 01:42:56 GMT  
		Size: 93.6 MB (93597541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775f4ea95a4fc2b7ecb083439230ef0ab1ec7982665f91453f2cd99452fab27`  
		Last Modified: Tue, 07 Apr 2026 01:42:53 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:7a23731bb440cce975699313750c73c44e6d0229375395f0d3b8159140bc5f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c10318cf4c437876c0adca974e1fc38ea38cc60fdf40cc9b8e8d7a025715f4`

```dockerfile
```

-	Layers:
	-	`sha256:7b6f06ce63a86598ef0e95017b8b79f76704c4d71fcf265d532738858740686f`  
		Last Modified: Tue, 07 Apr 2026 01:42:53 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b63827ce50d83b7b23ab61469cf692b214329f10793f7430a9f6ed4aadaa5a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116273321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b9384b2bf421a7cee583bbbe7063fa7dc2ac315e2829ae48a6af6b1f5e0ada`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:19 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:45:19 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Tue, 07 Apr 2026 01:45:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:45:19 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:45:19 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:45:19 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:45:19 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:45:19 GMT
CMD []
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3bfba1c260932e5c73ff6752352b937a92fe90b8ae47d9bc29cfd1a10e94b1`  
		Last Modified: Tue, 07 Apr 2026 01:45:34 GMT  
		Size: 88.2 MB (88156398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72a069d1e21a3e7d3243080102b18b514c3033cb9ea379e60a0fa900525f138`  
		Last Modified: Tue, 07 Apr 2026 01:45:30 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:539afa52fed34b062e5f9ab496680ac55d2c7316fa541dfdfe0fc0281a189dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf52ef98d2b789a12c45714447cc4459b6046269d42905a3473b4a140f629bc`

```dockerfile
```

-	Layers:
	-	`sha256:0c635b48d71db522c557d9ab44c311c4b75f322ff537d583b44db50c4c37fdd2`  
		Last Modified: Tue, 07 Apr 2026 01:45:30 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.17`

```console
$ docker pull varnish@sha256:a327469c847044adad0f29d2912abe3ee2078efcc70fa723233a0e2ff033e602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0.17` - linux; amd64

```console
$ docker pull varnish@sha256:aa13c718b3982e4703770030f0580d33facdb64dacce0e0d2d9beafc0056c118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121834627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6ed23c3cd7206c4759f32f8f685765ea45fc9b8860284c84ec9474588e8f93`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:42:42 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:42:42 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Tue, 07 Apr 2026 01:42:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:42:42 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:42:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:42:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:42:42 GMT
CMD []
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087951f710c0e407d30ec37397fe6623bd8a28d5ae98e14136b127c1103d6892`  
		Last Modified: Tue, 07 Apr 2026 01:42:56 GMT  
		Size: 93.6 MB (93597541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775f4ea95a4fc2b7ecb083439230ef0ab1ec7982665f91453f2cd99452fab27`  
		Last Modified: Tue, 07 Apr 2026 01:42:53 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.17` - unknown; unknown

```console
$ docker pull varnish@sha256:7a23731bb440cce975699313750c73c44e6d0229375395f0d3b8159140bc5f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c10318cf4c437876c0adca974e1fc38ea38cc60fdf40cc9b8e8d7a025715f4`

```dockerfile
```

-	Layers:
	-	`sha256:7b6f06ce63a86598ef0e95017b8b79f76704c4d71fcf265d532738858740686f`  
		Last Modified: Tue, 07 Apr 2026 01:42:53 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.17` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b63827ce50d83b7b23ab61469cf692b214329f10793f7430a9f6ed4aadaa5a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116273321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b9384b2bf421a7cee583bbbe7063fa7dc2ac315e2829ae48a6af6b1f5e0ada`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:19 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:45:19 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Tue, 07 Apr 2026 01:45:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:45:19 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:45:19 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:45:19 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:45:19 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:45:19 GMT
CMD []
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3bfba1c260932e5c73ff6752352b937a92fe90b8ae47d9bc29cfd1a10e94b1`  
		Last Modified: Tue, 07 Apr 2026 01:45:34 GMT  
		Size: 88.2 MB (88156398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72a069d1e21a3e7d3243080102b18b514c3033cb9ea379e60a0fa900525f138`  
		Last Modified: Tue, 07 Apr 2026 01:45:30 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.17` - unknown; unknown

```console
$ docker pull varnish@sha256:539afa52fed34b062e5f9ab496680ac55d2c7316fa541dfdfe0fc0281a189dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf52ef98d2b789a12c45714447cc4459b6046269d42905a3473b4a140f629bc`

```dockerfile
```

-	Layers:
	-	`sha256:0c635b48d71db522c557d9ab44c311c4b75f322ff537d583b44db50c4c37fdd2`  
		Last Modified: Tue, 07 Apr 2026 01:45:30 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8`

```console
$ docker pull varnish@sha256:5a858bdf9f58f3594068561a83c0118bbac4d33115fdcfe696b9848ac00fb874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8` - linux; amd64

```console
$ docker pull varnish@sha256:1d3f3e1488bdb098172a83e7a0945366aaf4758b24b546cd6228d0788ac0acbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118969785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704910fdf8acb521b137eb1c582d117bf276fc9cdbcb63924cec65ad82d42cea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:43:16 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 07 Apr 2026 01:43:16 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:43:16 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:43:16 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:43:16 GMT
USER varnish
# Tue, 07 Apr 2026 01:43:16 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:43:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1c95874e0f344466754391b7814d464fefdc4ab8c4b1cd8b7212eaf12501a6`  
		Last Modified: Tue, 07 Apr 2026 01:43:30 GMT  
		Size: 89.2 MB (89191026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0100e77b0565c2bd21409eb5e342f7f50b720ef2a14c69445c1568676b2a40e8`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f764fdc9687224de301a170cc8e83dea71e5a3cf3a409e55af1498ad2eca9f58`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5307540174c82b00c0ec9143fcd4a145e229bd752f225bc799c6e17b3aefd819`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:774b08e1fc8028fbe42b005ee640a70e1dfc8e39dd767b5767888bb2ed69b9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38f3dfa0f2f39666f75096a358de1673426ae8aa1947a3c848d1cc844ddf585`

```dockerfile
```

-	Layers:
	-	`sha256:3a275ad839eb9f637c806e0f07c2997954fca97d77056c69f76e3b7f0d8b1aaa`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 20.6 KB (20566 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:de8b7f4ac8eb159c3a54e4da0433e4738814f03d9ad2766f97bfd7572c2d578b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112980461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1d09b8db52da7ec70bdb708f0b250878dfe56901e65ccdc1f23fa01506706b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:51 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 07 Apr 2026 01:45:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:45:51 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:45:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:45:51 GMT
USER varnish
# Tue, 07 Apr 2026 01:45:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:45:51 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6827838a7494d352d3517a378420f6f240e1c2836595174a325b46e7bbafed`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 82.8 MB (82838785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415602245747d85c3f67217d8bd9aea878af889fe3a3d428b9c52ec7a31d1edf`  
		Last Modified: Tue, 07 Apr 2026 01:45:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60023cc98fb7529f68b7666443a15ea520e1e03ff0aae66a991639dba65b691d`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92c13a3e89c80bf3a497d8d05e31e98b647ce2f0b9e3c9aa5b637a0dc483de`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:261c213a261f10f93f4fb7a95462b9228b67e9e57bfc6da5fb7504943a55d127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d2b5d729ed8071c671bde7dbe22e970e06717c24b3aff9eac3d95ff99387e6`

```dockerfile
```

-	Layers:
	-	`sha256:126cad36bd2a7055aaca0c9b6d346d2a079533d11cafd4c5cef693c7b32a46cd`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 20.7 KB (20671 bytes)  
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
$ docker pull varnish@sha256:5a858bdf9f58f3594068561a83c0118bbac4d33115fdcfe696b9848ac00fb874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0` - linux; amd64

```console
$ docker pull varnish@sha256:1d3f3e1488bdb098172a83e7a0945366aaf4758b24b546cd6228d0788ac0acbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118969785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704910fdf8acb521b137eb1c582d117bf276fc9cdbcb63924cec65ad82d42cea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:43:16 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 07 Apr 2026 01:43:16 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:43:16 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:43:16 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:43:16 GMT
USER varnish
# Tue, 07 Apr 2026 01:43:16 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:43:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1c95874e0f344466754391b7814d464fefdc4ab8c4b1cd8b7212eaf12501a6`  
		Last Modified: Tue, 07 Apr 2026 01:43:30 GMT  
		Size: 89.2 MB (89191026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0100e77b0565c2bd21409eb5e342f7f50b720ef2a14c69445c1568676b2a40e8`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f764fdc9687224de301a170cc8e83dea71e5a3cf3a409e55af1498ad2eca9f58`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5307540174c82b00c0ec9143fcd4a145e229bd752f225bc799c6e17b3aefd819`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:774b08e1fc8028fbe42b005ee640a70e1dfc8e39dd767b5767888bb2ed69b9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38f3dfa0f2f39666f75096a358de1673426ae8aa1947a3c848d1cc844ddf585`

```dockerfile
```

-	Layers:
	-	`sha256:3a275ad839eb9f637c806e0f07c2997954fca97d77056c69f76e3b7f0d8b1aaa`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 20.6 KB (20566 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:de8b7f4ac8eb159c3a54e4da0433e4738814f03d9ad2766f97bfd7572c2d578b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112980461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1d09b8db52da7ec70bdb708f0b250878dfe56901e65ccdc1f23fa01506706b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:51 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 07 Apr 2026 01:45:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:45:51 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:45:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:45:51 GMT
USER varnish
# Tue, 07 Apr 2026 01:45:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:45:51 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6827838a7494d352d3517a378420f6f240e1c2836595174a325b46e7bbafed`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 82.8 MB (82838785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415602245747d85c3f67217d8bd9aea878af889fe3a3d428b9c52ec7a31d1edf`  
		Last Modified: Tue, 07 Apr 2026 01:45:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60023cc98fb7529f68b7666443a15ea520e1e03ff0aae66a991639dba65b691d`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92c13a3e89c80bf3a497d8d05e31e98b647ce2f0b9e3c9aa5b637a0dc483de`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:261c213a261f10f93f4fb7a95462b9228b67e9e57bfc6da5fb7504943a55d127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d2b5d729ed8071c671bde7dbe22e970e06717c24b3aff9eac3d95ff99387e6`

```dockerfile
```

-	Layers:
	-	`sha256:126cad36bd2a7055aaca0c9b6d346d2a079533d11cafd4c5cef693c7b32a46cd`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 20.7 KB (20671 bytes)  
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
$ docker pull varnish@sha256:5a858bdf9f58f3594068561a83c0118bbac4d33115fdcfe696b9848ac00fb874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.1` - linux; amd64

```console
$ docker pull varnish@sha256:1d3f3e1488bdb098172a83e7a0945366aaf4758b24b546cd6228d0788ac0acbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118969785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704910fdf8acb521b137eb1c582d117bf276fc9cdbcb63924cec65ad82d42cea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:43:16 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 07 Apr 2026 01:43:16 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:43:16 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:43:16 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:43:16 GMT
USER varnish
# Tue, 07 Apr 2026 01:43:16 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:43:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1c95874e0f344466754391b7814d464fefdc4ab8c4b1cd8b7212eaf12501a6`  
		Last Modified: Tue, 07 Apr 2026 01:43:30 GMT  
		Size: 89.2 MB (89191026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0100e77b0565c2bd21409eb5e342f7f50b720ef2a14c69445c1568676b2a40e8`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f764fdc9687224de301a170cc8e83dea71e5a3cf3a409e55af1498ad2eca9f58`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5307540174c82b00c0ec9143fcd4a145e229bd752f225bc799c6e17b3aefd819`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:774b08e1fc8028fbe42b005ee640a70e1dfc8e39dd767b5767888bb2ed69b9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38f3dfa0f2f39666f75096a358de1673426ae8aa1947a3c848d1cc844ddf585`

```dockerfile
```

-	Layers:
	-	`sha256:3a275ad839eb9f637c806e0f07c2997954fca97d77056c69f76e3b7f0d8b1aaa`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 20.6 KB (20566 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:de8b7f4ac8eb159c3a54e4da0433e4738814f03d9ad2766f97bfd7572c2d578b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112980461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1d09b8db52da7ec70bdb708f0b250878dfe56901e65ccdc1f23fa01506706b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:51 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 07 Apr 2026 01:45:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:45:51 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:45:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:45:51 GMT
USER varnish
# Tue, 07 Apr 2026 01:45:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:45:51 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6827838a7494d352d3517a378420f6f240e1c2836595174a325b46e7bbafed`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 82.8 MB (82838785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415602245747d85c3f67217d8bd9aea878af889fe3a3d428b9c52ec7a31d1edf`  
		Last Modified: Tue, 07 Apr 2026 01:45:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60023cc98fb7529f68b7666443a15ea520e1e03ff0aae66a991639dba65b691d`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92c13a3e89c80bf3a497d8d05e31e98b647ce2f0b9e3c9aa5b637a0dc483de`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:261c213a261f10f93f4fb7a95462b9228b67e9e57bfc6da5fb7504943a55d127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d2b5d729ed8071c671bde7dbe22e970e06717c24b3aff9eac3d95ff99387e6`

```dockerfile
```

-	Layers:
	-	`sha256:126cad36bd2a7055aaca0c9b6d346d2a079533d11cafd4c5cef693c7b32a46cd`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 20.7 KB (20671 bytes)  
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
$ docker pull varnish@sha256:91cd10d2aa08f293054a75db600b7093ee1b8a7e413b6c9435015c890575d6a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9` - linux; amd64

```console
$ docker pull varnish@sha256:a633196ce5f4abc0746be632c7a30073fe191860b4881353c326f47f42381f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123984303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb10adaa2e06f0fdcd8c3579392ebc669af212d8a6d90a8b1a3f1aaec04dcf1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:47:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:47:39 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:47:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:47:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:47:39 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:47:39 GMT
USER varnish
# Fri, 10 Apr 2026 17:47:39 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:47:39 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edb459dc695b9ed55dc9d57d42fe814817dff184d4eaff0f36ef9301b9a508a`  
		Last Modified: Fri, 10 Apr 2026 17:47:55 GMT  
		Size: 94.2 MB (94205783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e81bb3cf144ca0a88f8fa0d1bfaa98e66c19c4d21cddc52ba6c9643a6a026aa`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2abd877ddaceccbfa26d173d45cebe74a8ab9aedca64142400c31d05813662`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760a134477850f33d57d335e741110ad0633eb6ae64cd3edc62f8bb355518530`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:8b5764c5ce75e8a002bbb573534efc73ad65880efa608d7d3fd8cc3dc4d786a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364d0bdf5fe043ed4dfb0872e56f83e6be572c5e8a3bb2a9aee34b697d5a935a`

```dockerfile
```

-	Layers:
	-	`sha256:e2d648c6c09dcef4353d46af054a1b1d4b5528ecdd7967e9e3972c69ba6c2f16`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f9cd1a697def9d65f20a3a3334d47159cd2ad63aec6bce78d6d8f885adcc052b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118349593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ac8463ddfbad01e0651f120580f18d99b3fb4c7ec04a88e01b5c921b4e3aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:11:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:11:33 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:11:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:11:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:11:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:11:33 GMT
USER varnish
# Fri, 10 Apr 2026 17:11:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:11:33 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3af3bca1472f9f298828fce4d29fa27c20acaf5822194ff32e4125fe8fcb31`  
		Last Modified: Fri, 10 Apr 2026 17:11:47 GMT  
		Size: 88.2 MB (88208151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89383f887ad181889cb93db922142949358a7dc9965d5ee382ed751fb78dd39`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e00dc83ad7bf1fff59acff685454469c3130a9106f07f4afa39272b96eb7ae5`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bd7a322abd7119444c3a9289524ffe41f6570522ecdb1f02510688b36391f2`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:d96ae547aadc8aa0e2f5194b5dad6311f9eaadfb2681b4891d37c204b70f1c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac038aa58b7c7e03b15a8363daa3c33cab1d8d6a63740d5bb691edf8e68245c5`

```dockerfile
```

-	Layers:
	-	`sha256:608227b037937cd986038e26304d6c5f4326b3fd14b8e1846cae3118b3db6278`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0`

```console
$ docker pull varnish@sha256:91cd10d2aa08f293054a75db600b7093ee1b8a7e413b6c9435015c890575d6a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0` - linux; amd64

```console
$ docker pull varnish@sha256:a633196ce5f4abc0746be632c7a30073fe191860b4881353c326f47f42381f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123984303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb10adaa2e06f0fdcd8c3579392ebc669af212d8a6d90a8b1a3f1aaec04dcf1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:47:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:47:39 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:47:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:47:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:47:39 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:47:39 GMT
USER varnish
# Fri, 10 Apr 2026 17:47:39 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:47:39 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edb459dc695b9ed55dc9d57d42fe814817dff184d4eaff0f36ef9301b9a508a`  
		Last Modified: Fri, 10 Apr 2026 17:47:55 GMT  
		Size: 94.2 MB (94205783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e81bb3cf144ca0a88f8fa0d1bfaa98e66c19c4d21cddc52ba6c9643a6a026aa`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2abd877ddaceccbfa26d173d45cebe74a8ab9aedca64142400c31d05813662`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760a134477850f33d57d335e741110ad0633eb6ae64cd3edc62f8bb355518530`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:8b5764c5ce75e8a002bbb573534efc73ad65880efa608d7d3fd8cc3dc4d786a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364d0bdf5fe043ed4dfb0872e56f83e6be572c5e8a3bb2a9aee34b697d5a935a`

```dockerfile
```

-	Layers:
	-	`sha256:e2d648c6c09dcef4353d46af054a1b1d4b5528ecdd7967e9e3972c69ba6c2f16`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f9cd1a697def9d65f20a3a3334d47159cd2ad63aec6bce78d6d8f885adcc052b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118349593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ac8463ddfbad01e0651f120580f18d99b3fb4c7ec04a88e01b5c921b4e3aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:11:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:11:33 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:11:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:11:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:11:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:11:33 GMT
USER varnish
# Fri, 10 Apr 2026 17:11:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:11:33 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3af3bca1472f9f298828fce4d29fa27c20acaf5822194ff32e4125fe8fcb31`  
		Last Modified: Fri, 10 Apr 2026 17:11:47 GMT  
		Size: 88.2 MB (88208151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89383f887ad181889cb93db922142949358a7dc9965d5ee382ed751fb78dd39`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e00dc83ad7bf1fff59acff685454469c3130a9106f07f4afa39272b96eb7ae5`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bd7a322abd7119444c3a9289524ffe41f6570522ecdb1f02510688b36391f2`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:d96ae547aadc8aa0e2f5194b5dad6311f9eaadfb2681b4891d37c204b70f1c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac038aa58b7c7e03b15a8363daa3c33cab1d8d6a63740d5bb691edf8e68245c5`

```dockerfile
```

-	Layers:
	-	`sha256:608227b037937cd986038e26304d6c5f4326b3fd14b8e1846cae3118b3db6278`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0.1`

```console
$ docker pull varnish@sha256:91cd10d2aa08f293054a75db600b7093ee1b8a7e413b6c9435015c890575d6a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0.1` - linux; amd64

```console
$ docker pull varnish@sha256:a633196ce5f4abc0746be632c7a30073fe191860b4881353c326f47f42381f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123984303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb10adaa2e06f0fdcd8c3579392ebc669af212d8a6d90a8b1a3f1aaec04dcf1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:47:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:47:39 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:47:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:47:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:47:39 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:47:39 GMT
USER varnish
# Fri, 10 Apr 2026 17:47:39 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:47:39 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edb459dc695b9ed55dc9d57d42fe814817dff184d4eaff0f36ef9301b9a508a`  
		Last Modified: Fri, 10 Apr 2026 17:47:55 GMT  
		Size: 94.2 MB (94205783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e81bb3cf144ca0a88f8fa0d1bfaa98e66c19c4d21cddc52ba6c9643a6a026aa`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2abd877ddaceccbfa26d173d45cebe74a8ab9aedca64142400c31d05813662`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760a134477850f33d57d335e741110ad0633eb6ae64cd3edc62f8bb355518530`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:8b5764c5ce75e8a002bbb573534efc73ad65880efa608d7d3fd8cc3dc4d786a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364d0bdf5fe043ed4dfb0872e56f83e6be572c5e8a3bb2a9aee34b697d5a935a`

```dockerfile
```

-	Layers:
	-	`sha256:e2d648c6c09dcef4353d46af054a1b1d4b5528ecdd7967e9e3972c69ba6c2f16`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f9cd1a697def9d65f20a3a3334d47159cd2ad63aec6bce78d6d8f885adcc052b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118349593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ac8463ddfbad01e0651f120580f18d99b3fb4c7ec04a88e01b5c921b4e3aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:11:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:11:33 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:11:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:11:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:11:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:11:33 GMT
USER varnish
# Fri, 10 Apr 2026 17:11:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:11:33 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3af3bca1472f9f298828fce4d29fa27c20acaf5822194ff32e4125fe8fcb31`  
		Last Modified: Fri, 10 Apr 2026 17:11:47 GMT  
		Size: 88.2 MB (88208151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89383f887ad181889cb93db922142949358a7dc9965d5ee382ed751fb78dd39`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e00dc83ad7bf1fff59acff685454469c3130a9106f07f4afa39272b96eb7ae5`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bd7a322abd7119444c3a9289524ffe41f6570522ecdb1f02510688b36391f2`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:d96ae547aadc8aa0e2f5194b5dad6311f9eaadfb2681b4891d37c204b70f1c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac038aa58b7c7e03b15a8363daa3c33cab1d8d6a63740d5bb691edf8e68245c5`

```dockerfile
```

-	Layers:
	-	`sha256:608227b037937cd986038e26304d6c5f4326b3fd14b8e1846cae3118b3db6278`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:91cd10d2aa08f293054a75db600b7093ee1b8a7e413b6c9435015c890575d6a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:a633196ce5f4abc0746be632c7a30073fe191860b4881353c326f47f42381f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123984303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb10adaa2e06f0fdcd8c3579392ebc669af212d8a6d90a8b1a3f1aaec04dcf1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:47:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:47:39 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:47:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:47:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:47:39 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:47:39 GMT
USER varnish
# Fri, 10 Apr 2026 17:47:39 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:47:39 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edb459dc695b9ed55dc9d57d42fe814817dff184d4eaff0f36ef9301b9a508a`  
		Last Modified: Fri, 10 Apr 2026 17:47:55 GMT  
		Size: 94.2 MB (94205783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e81bb3cf144ca0a88f8fa0d1bfaa98e66c19c4d21cddc52ba6c9643a6a026aa`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2abd877ddaceccbfa26d173d45cebe74a8ab9aedca64142400c31d05813662`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760a134477850f33d57d335e741110ad0633eb6ae64cd3edc62f8bb355518530`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:8b5764c5ce75e8a002bbb573534efc73ad65880efa608d7d3fd8cc3dc4d786a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364d0bdf5fe043ed4dfb0872e56f83e6be572c5e8a3bb2a9aee34b697d5a935a`

```dockerfile
```

-	Layers:
	-	`sha256:e2d648c6c09dcef4353d46af054a1b1d4b5528ecdd7967e9e3972c69ba6c2f16`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f9cd1a697def9d65f20a3a3334d47159cd2ad63aec6bce78d6d8f885adcc052b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118349593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ac8463ddfbad01e0651f120580f18d99b3fb4c7ec04a88e01b5c921b4e3aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:11:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:11:33 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:11:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:11:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:11:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:11:33 GMT
USER varnish
# Fri, 10 Apr 2026 17:11:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:11:33 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3af3bca1472f9f298828fce4d29fa27c20acaf5822194ff32e4125fe8fcb31`  
		Last Modified: Fri, 10 Apr 2026 17:11:47 GMT  
		Size: 88.2 MB (88208151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89383f887ad181889cb93db922142949358a7dc9965d5ee382ed751fb78dd39`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e00dc83ad7bf1fff59acff685454469c3130a9106f07f4afa39272b96eb7ae5`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bd7a322abd7119444c3a9289524ffe41f6570522ecdb1f02510688b36391f2`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:d96ae547aadc8aa0e2f5194b5dad6311f9eaadfb2681b4891d37c204b70f1c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac038aa58b7c7e03b15a8363daa3c33cab1d8d6a63740d5bb691edf8e68245c5`

```dockerfile
```

-	Layers:
	-	`sha256:608227b037937cd986038e26304d6c5f4326b3fd14b8e1846cae3118b3db6278`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:91cd10d2aa08f293054a75db600b7093ee1b8a7e413b6c9435015c890575d6a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:a633196ce5f4abc0746be632c7a30073fe191860b4881353c326f47f42381f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123984303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb10adaa2e06f0fdcd8c3579392ebc669af212d8a6d90a8b1a3f1aaec04dcf1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:47:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:47:39 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:47:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:47:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:47:39 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:47:39 GMT
USER varnish
# Fri, 10 Apr 2026 17:47:39 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:47:39 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edb459dc695b9ed55dc9d57d42fe814817dff184d4eaff0f36ef9301b9a508a`  
		Last Modified: Fri, 10 Apr 2026 17:47:55 GMT  
		Size: 94.2 MB (94205783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e81bb3cf144ca0a88f8fa0d1bfaa98e66c19c4d21cddc52ba6c9643a6a026aa`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2abd877ddaceccbfa26d173d45cebe74a8ab9aedca64142400c31d05813662`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760a134477850f33d57d335e741110ad0633eb6ae64cd3edc62f8bb355518530`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:8b5764c5ce75e8a002bbb573534efc73ad65880efa608d7d3fd8cc3dc4d786a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364d0bdf5fe043ed4dfb0872e56f83e6be572c5e8a3bb2a9aee34b697d5a935a`

```dockerfile
```

-	Layers:
	-	`sha256:e2d648c6c09dcef4353d46af054a1b1d4b5528ecdd7967e9e3972c69ba6c2f16`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f9cd1a697def9d65f20a3a3334d47159cd2ad63aec6bce78d6d8f885adcc052b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118349593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ac8463ddfbad01e0651f120580f18d99b3fb4c7ec04a88e01b5c921b4e3aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:11:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:11:33 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:11:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:11:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:11:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:11:33 GMT
USER varnish
# Fri, 10 Apr 2026 17:11:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:11:33 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3af3bca1472f9f298828fce4d29fa27c20acaf5822194ff32e4125fe8fcb31`  
		Last Modified: Fri, 10 Apr 2026 17:11:47 GMT  
		Size: 88.2 MB (88208151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89383f887ad181889cb93db922142949358a7dc9965d5ee382ed751fb78dd39`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e00dc83ad7bf1fff59acff685454469c3130a9106f07f4afa39272b96eb7ae5`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bd7a322abd7119444c3a9289524ffe41f6570522ecdb1f02510688b36391f2`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:d96ae547aadc8aa0e2f5194b5dad6311f9eaadfb2681b4891d37c204b70f1c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac038aa58b7c7e03b15a8363daa3c33cab1d8d6a63740d5bb691edf8e68245c5`

```dockerfile
```

-	Layers:
	-	`sha256:608227b037937cd986038e26304d6c5f4326b3fd14b8e1846cae3118b3db6278`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:5a858bdf9f58f3594068561a83c0118bbac4d33115fdcfe696b9848ac00fb874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:1d3f3e1488bdb098172a83e7a0945366aaf4758b24b546cd6228d0788ac0acbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118969785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704910fdf8acb521b137eb1c582d117bf276fc9cdbcb63924cec65ad82d42cea`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:43:16 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 07 Apr 2026 01:43:16 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 07 Apr 2026 01:43:16 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:43:16 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:43:16 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:43:16 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:43:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:43:16 GMT
USER varnish
# Tue, 07 Apr 2026 01:43:16 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:43:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1c95874e0f344466754391b7814d464fefdc4ab8c4b1cd8b7212eaf12501a6`  
		Last Modified: Tue, 07 Apr 2026 01:43:30 GMT  
		Size: 89.2 MB (89191026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0100e77b0565c2bd21409eb5e342f7f50b720ef2a14c69445c1568676b2a40e8`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f764fdc9687224de301a170cc8e83dea71e5a3cf3a409e55af1498ad2eca9f58`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5307540174c82b00c0ec9143fcd4a145e229bd752f225bc799c6e17b3aefd819`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:774b08e1fc8028fbe42b005ee640a70e1dfc8e39dd767b5767888bb2ed69b9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38f3dfa0f2f39666f75096a358de1673426ae8aa1947a3c848d1cc844ddf585`

```dockerfile
```

-	Layers:
	-	`sha256:3a275ad839eb9f637c806e0f07c2997954fca97d77056c69f76e3b7f0d8b1aaa`  
		Last Modified: Tue, 07 Apr 2026 01:43:28 GMT  
		Size: 20.6 KB (20566 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:de8b7f4ac8eb159c3a54e4da0433e4738814f03d9ad2766f97bfd7572c2d578b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112980461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1d09b8db52da7ec70bdb708f0b250878dfe56901e65ccdc1f23fa01506706b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:51 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 07 Apr 2026 01:45:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 07 Apr 2026 01:45:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:45:51 GMT
ENV VSM_NOPID=1
# Tue, 07 Apr 2026 01:45:51 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:45:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:45:51 GMT
USER varnish
# Tue, 07 Apr 2026 01:45:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:45:51 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6827838a7494d352d3517a378420f6f240e1c2836595174a325b46e7bbafed`  
		Last Modified: Tue, 07 Apr 2026 01:46:04 GMT  
		Size: 82.8 MB (82838785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415602245747d85c3f67217d8bd9aea878af889fe3a3d428b9c52ec7a31d1edf`  
		Last Modified: Tue, 07 Apr 2026 01:45:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60023cc98fb7529f68b7666443a15ea520e1e03ff0aae66a991639dba65b691d`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de92c13a3e89c80bf3a497d8d05e31e98b647ce2f0b9e3c9aa5b637a0dc483de`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:261c213a261f10f93f4fb7a95462b9228b67e9e57bfc6da5fb7504943a55d127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d2b5d729ed8071c671bde7dbe22e970e06717c24b3aff9eac3d95ff99387e6`

```dockerfile
```

-	Layers:
	-	`sha256:126cad36bd2a7055aaca0c9b6d346d2a079533d11cafd4c5cef693c7b32a46cd`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 20.7 KB (20671 bytes)  
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
$ docker pull varnish@sha256:a327469c847044adad0f29d2912abe3ee2078efcc70fa723233a0e2ff033e602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:aa13c718b3982e4703770030f0580d33facdb64dacce0e0d2d9beafc0056c118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121834627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6ed23c3cd7206c4759f32f8f685765ea45fc9b8860284c84ec9474588e8f93`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:42:42 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:42:42 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Tue, 07 Apr 2026 01:42:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:42:42 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:42:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:42:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:42:42 GMT
CMD []
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087951f710c0e407d30ec37397fe6623bd8a28d5ae98e14136b127c1103d6892`  
		Last Modified: Tue, 07 Apr 2026 01:42:56 GMT  
		Size: 93.6 MB (93597541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775f4ea95a4fc2b7ecb083439230ef0ab1ec7982665f91453f2cd99452fab27`  
		Last Modified: Tue, 07 Apr 2026 01:42:53 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:7a23731bb440cce975699313750c73c44e6d0229375395f0d3b8159140bc5f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c10318cf4c437876c0adca974e1fc38ea38cc60fdf40cc9b8e8d7a025715f4`

```dockerfile
```

-	Layers:
	-	`sha256:7b6f06ce63a86598ef0e95017b8b79f76704c4d71fcf265d532738858740686f`  
		Last Modified: Tue, 07 Apr 2026 01:42:53 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:b63827ce50d83b7b23ab61469cf692b214329f10793f7430a9f6ed4aadaa5a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116273321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b9384b2bf421a7cee583bbbe7063fa7dc2ac315e2829ae48a6af6b1f5e0ada`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:19 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 07 Apr 2026 01:45:19 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Tue, 07 Apr 2026 01:45:19 GMT
ENV VARNISH_SIZE=100M
# Tue, 07 Apr 2026 01:45:19 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 07 Apr 2026 01:45:19 GMT
WORKDIR /etc/varnish
# Tue, 07 Apr 2026 01:45:19 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:45:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 07 Apr 2026 01:45:19 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 07 Apr 2026 01:45:19 GMT
CMD []
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3bfba1c260932e5c73ff6752352b937a92fe90b8ae47d9bc29cfd1a10e94b1`  
		Last Modified: Tue, 07 Apr 2026 01:45:34 GMT  
		Size: 88.2 MB (88156398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72a069d1e21a3e7d3243080102b18b514c3033cb9ea379e60a0fa900525f138`  
		Last Modified: Tue, 07 Apr 2026 01:45:30 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:539afa52fed34b062e5f9ab496680ac55d2c7316fa541dfdfe0fc0281a189dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf52ef98d2b789a12c45714447cc4459b6046269d42905a3473b4a140f629bc`

```dockerfile
```

-	Layers:
	-	`sha256:0c635b48d71db522c557d9ab44c311c4b75f322ff537d583b44db50c4c37fdd2`  
		Last Modified: Tue, 07 Apr 2026 01:45:30 GMT  
		Size: 12.8 KB (12761 bytes)  
		MIME: application/vnd.in-toto+json
