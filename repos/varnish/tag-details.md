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
$ docker pull varnish@sha256:ec99f528eb409789d6b2d01178a36388f21d5a19faab7f695e39ad5e23eca5ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:f319003ae2e7f71186f5577c29ea2a8eaee3fb9840e9d6e12235f44fe11b8e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121850316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c112f173adbd5ccc82a3d685d20bd6a1b68379e28ec47ffb95b7b877dacb5fb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:36:07 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:07 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Fri, 08 May 2026 19:36:07 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:07 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:07 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:07 GMT
CMD []
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc62d7f7ac1905a4537698365a041b779630457cf204f14d41d3c0343befaa75`  
		Last Modified: Fri, 08 May 2026 19:36:21 GMT  
		Size: 93.6 MB (93613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f806ed6a57a7942d1867a26edb91b295bed9dc11ea50e0800d3d10f259a1f2f`  
		Last Modified: Fri, 08 May 2026 19:36:19 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:af5f6161c930c6e00468d5b2e9edeffed9506e572adf6064af08b6e037280a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825723351a505a8866775871508482db3d7ec94960c07eaf60894476631c5997`

```dockerfile
```

-	Layers:
	-	`sha256:2adfa1ab1b5d353f8b22c4a047c806f633f5a024c3463d068a8f00fe790fb1dd`  
		Last Modified: Fri, 08 May 2026 19:36:19 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:44575916983ffb89251685ed9f6cc4162f4a7406933eb193c894f51c27805b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116285686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88d535d8298265194ebdb4873ea88475db031f9a7c73fcbad57052543cb5d23`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:37:47 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:37:47 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Fri, 08 May 2026 19:37:47 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:37:47 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:37:47 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:37:47 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:37:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:37:47 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:37:47 GMT
CMD []
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd1683cbe057ee5d4edda621a71a46b2442071426c7494653340127d1d7e59c`  
		Last Modified: Fri, 08 May 2026 19:38:01 GMT  
		Size: 88.2 MB (88168766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088683e2f67788e0a35e995abee66f97048da5c83cc71661a3aafa6be018c5c6`  
		Last Modified: Fri, 08 May 2026 19:37:59 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0` - unknown; unknown

```console
$ docker pull varnish@sha256:0023c08ac49f87eb5cf42dd4e14e19f3727fe157d3513dd5d030f39a072103c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a56a8f34ffaba5ece5035ff54335c52a5fe49bb4868bcd9f8c0995a8adc58b9`

```dockerfile
```

-	Layers:
	-	`sha256:768dea45adb67a07408f99f9eec95b7c0a03b5f81376de6c6c4c28f4f3457f55`  
		Last Modified: Fri, 08 May 2026 19:37:59 GMT  
		Size: 12.8 KB (12760 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:6.0.17`

```console
$ docker pull varnish@sha256:ec99f528eb409789d6b2d01178a36388f21d5a19faab7f695e39ad5e23eca5ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:6.0.17` - linux; amd64

```console
$ docker pull varnish@sha256:f319003ae2e7f71186f5577c29ea2a8eaee3fb9840e9d6e12235f44fe11b8e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121850316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c112f173adbd5ccc82a3d685d20bd6a1b68379e28ec47ffb95b7b877dacb5fb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:36:07 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:07 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Fri, 08 May 2026 19:36:07 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:07 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:07 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:07 GMT
CMD []
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc62d7f7ac1905a4537698365a041b779630457cf204f14d41d3c0343befaa75`  
		Last Modified: Fri, 08 May 2026 19:36:21 GMT  
		Size: 93.6 MB (93613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f806ed6a57a7942d1867a26edb91b295bed9dc11ea50e0800d3d10f259a1f2f`  
		Last Modified: Fri, 08 May 2026 19:36:19 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.17` - unknown; unknown

```console
$ docker pull varnish@sha256:af5f6161c930c6e00468d5b2e9edeffed9506e572adf6064af08b6e037280a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825723351a505a8866775871508482db3d7ec94960c07eaf60894476631c5997`

```dockerfile
```

-	Layers:
	-	`sha256:2adfa1ab1b5d353f8b22c4a047c806f633f5a024c3463d068a8f00fe790fb1dd`  
		Last Modified: Fri, 08 May 2026 19:36:19 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:6.0.17` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:44575916983ffb89251685ed9f6cc4162f4a7406933eb193c894f51c27805b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116285686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88d535d8298265194ebdb4873ea88475db031f9a7c73fcbad57052543cb5d23`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:37:47 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:37:47 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Fri, 08 May 2026 19:37:47 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:37:47 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:37:47 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:37:47 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:37:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:37:47 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:37:47 GMT
CMD []
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd1683cbe057ee5d4edda621a71a46b2442071426c7494653340127d1d7e59c`  
		Last Modified: Fri, 08 May 2026 19:38:01 GMT  
		Size: 88.2 MB (88168766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088683e2f67788e0a35e995abee66f97048da5c83cc71661a3aafa6be018c5c6`  
		Last Modified: Fri, 08 May 2026 19:37:59 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:6.0.17` - unknown; unknown

```console
$ docker pull varnish@sha256:0023c08ac49f87eb5cf42dd4e14e19f3727fe157d3513dd5d030f39a072103c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a56a8f34ffaba5ece5035ff54335c52a5fe49bb4868bcd9f8c0995a8adc58b9`

```dockerfile
```

-	Layers:
	-	`sha256:768dea45adb67a07408f99f9eec95b7c0a03b5f81376de6c6c4c28f4f3457f55`  
		Last Modified: Fri, 08 May 2026 19:37:59 GMT  
		Size: 12.8 KB (12760 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:8`

```console
$ docker pull varnish@sha256:8b618ce555c65ff1c3ff32fb2e03c0e45105c6f8e001cfa372e4ed47a5722744
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8` - linux; amd64

```console
$ docker pull varnish@sha256:6c13f546e900db1c5b45166cec3fdfb2d1d02d6166c6c2122ff4ad57fdbb13a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120238661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b268ab5d396ab64e0352f63a0bbb11beb2e266caf06b6aec8666ead792ec97`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:41 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:41 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Fri, 08 May 2026 19:36:41 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Fri, 08 May 2026 19:36:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Fri, 08 May 2026 19:36:41 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:36:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:36:41 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:41 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:36:41 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:41 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:41 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
COPY index.html /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:41 GMT
USER varnish
# Fri, 08 May 2026 19:36:41 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:41 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7365b8d155025cf0b3a8eeea351689542d7bd64582e909dac84553d0bb1134`  
		Last Modified: Fri, 08 May 2026 19:36:55 GMT  
		Size: 90.5 MB (90455320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e7eef1eb5f8e9691ab443fd2945693f755baa9ac07eb2aaa68121baebf45f1`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdefd778b717d91f169c1fae86e25549dedeed932149a459653d173cbd9c4e6b`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949cc04440888046d9dc6651d062e77d6a22c54151b79c29c6c9a4b28986f3af`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:a05cd40db5df192b41a87d288c98780daeba7665e52b02c9ddb14ac2bef84fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb8f78923fc858b5b19e2b3239aad1f2bff989beb74b9fd9b5becb941aa687e`

```dockerfile
```

-	Layers:
	-	`sha256:03a66b0f14f02f9d3de77a48ebc4bf1484c80c475ebe8a47215063766c6cdc4b`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 20.6 KB (20567 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3a60b23d57a0a5945a63b3ee14b6c8fa5d82b11278f3ecd5d52fa999850b22fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114245888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371bfffc933532ead58b49dd77c659fa770b07de0898baa61fd9aa0fcf29d2c6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:38:13 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Fri, 08 May 2026 19:38:13 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Fri, 08 May 2026 19:38:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Fri, 08 May 2026 19:38:13 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:38:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:38:13 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:38:13 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:38:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:38:13 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:38:13 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
COPY index.html /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:38:13 GMT
USER varnish
# Fri, 08 May 2026 19:38:13 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:38:13 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62f5e803ffd19caa42da395fbdad66e0d1e57df08278891de44d133e257d743`  
		Last Modified: Fri, 08 May 2026 19:38:27 GMT  
		Size: 84.1 MB (84099127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e0e771f75f8b71c0be9f4bf566a9b3e76194ce490738638695f97842636dbe`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f1cf2b419f37c73aee1126aaab7a5ac5fcdc08981affbe8d26383fef3dfc83`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42817c86f5b88de25c323ba5dcf6d7a3a852ebafc0dc9855cdf9746e1808c222`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8` - unknown; unknown

```console
$ docker pull varnish@sha256:ec3a17e688bc14a3fad5b5665bf5663c2a676b14d4af4871e195bb0b77161d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06d0a8881fd6f40d0454d5539045bfcdf230ed0c58213069d857f1c52c14f2c`

```dockerfile
```

-	Layers:
	-	`sha256:b6e9c99dff33245e656bfac655440da9a15e79bd3612bf23ac75a0511370583a`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
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
$ docker pull varnish@sha256:8b618ce555c65ff1c3ff32fb2e03c0e45105c6f8e001cfa372e4ed47a5722744
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0` - linux; amd64

```console
$ docker pull varnish@sha256:6c13f546e900db1c5b45166cec3fdfb2d1d02d6166c6c2122ff4ad57fdbb13a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120238661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b268ab5d396ab64e0352f63a0bbb11beb2e266caf06b6aec8666ead792ec97`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:41 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:41 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Fri, 08 May 2026 19:36:41 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Fri, 08 May 2026 19:36:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Fri, 08 May 2026 19:36:41 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:36:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:36:41 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:41 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:36:41 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:41 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:41 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
COPY index.html /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:41 GMT
USER varnish
# Fri, 08 May 2026 19:36:41 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:41 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7365b8d155025cf0b3a8eeea351689542d7bd64582e909dac84553d0bb1134`  
		Last Modified: Fri, 08 May 2026 19:36:55 GMT  
		Size: 90.5 MB (90455320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e7eef1eb5f8e9691ab443fd2945693f755baa9ac07eb2aaa68121baebf45f1`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdefd778b717d91f169c1fae86e25549dedeed932149a459653d173cbd9c4e6b`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949cc04440888046d9dc6651d062e77d6a22c54151b79c29c6c9a4b28986f3af`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:a05cd40db5df192b41a87d288c98780daeba7665e52b02c9ddb14ac2bef84fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb8f78923fc858b5b19e2b3239aad1f2bff989beb74b9fd9b5becb941aa687e`

```dockerfile
```

-	Layers:
	-	`sha256:03a66b0f14f02f9d3de77a48ebc4bf1484c80c475ebe8a47215063766c6cdc4b`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 20.6 KB (20567 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3a60b23d57a0a5945a63b3ee14b6c8fa5d82b11278f3ecd5d52fa999850b22fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114245888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371bfffc933532ead58b49dd77c659fa770b07de0898baa61fd9aa0fcf29d2c6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:38:13 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Fri, 08 May 2026 19:38:13 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Fri, 08 May 2026 19:38:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Fri, 08 May 2026 19:38:13 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:38:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:38:13 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:38:13 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:38:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:38:13 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:38:13 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
COPY index.html /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:38:13 GMT
USER varnish
# Fri, 08 May 2026 19:38:13 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:38:13 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62f5e803ffd19caa42da395fbdad66e0d1e57df08278891de44d133e257d743`  
		Last Modified: Fri, 08 May 2026 19:38:27 GMT  
		Size: 84.1 MB (84099127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e0e771f75f8b71c0be9f4bf566a9b3e76194ce490738638695f97842636dbe`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f1cf2b419f37c73aee1126aaab7a5ac5fcdc08981affbe8d26383fef3dfc83`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42817c86f5b88de25c323ba5dcf6d7a3a852ebafc0dc9855cdf9746e1808c222`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0` - unknown; unknown

```console
$ docker pull varnish@sha256:ec3a17e688bc14a3fad5b5665bf5663c2a676b14d4af4871e195bb0b77161d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06d0a8881fd6f40d0454d5539045bfcdf230ed0c58213069d857f1c52c14f2c`

```dockerfile
```

-	Layers:
	-	`sha256:b6e9c99dff33245e656bfac655440da9a15e79bd3612bf23ac75a0511370583a`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
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
$ docker pull varnish@sha256:8b618ce555c65ff1c3ff32fb2e03c0e45105c6f8e001cfa372e4ed47a5722744
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8.0.1` - linux; amd64

```console
$ docker pull varnish@sha256:6c13f546e900db1c5b45166cec3fdfb2d1d02d6166c6c2122ff4ad57fdbb13a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120238661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b268ab5d396ab64e0352f63a0bbb11beb2e266caf06b6aec8666ead792ec97`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:41 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:41 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Fri, 08 May 2026 19:36:41 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Fri, 08 May 2026 19:36:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Fri, 08 May 2026 19:36:41 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:36:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:36:41 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:41 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:36:41 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:41 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:41 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
COPY index.html /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:41 GMT
USER varnish
# Fri, 08 May 2026 19:36:41 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:41 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7365b8d155025cf0b3a8eeea351689542d7bd64582e909dac84553d0bb1134`  
		Last Modified: Fri, 08 May 2026 19:36:55 GMT  
		Size: 90.5 MB (90455320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e7eef1eb5f8e9691ab443fd2945693f755baa9ac07eb2aaa68121baebf45f1`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdefd778b717d91f169c1fae86e25549dedeed932149a459653d173cbd9c4e6b`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949cc04440888046d9dc6651d062e77d6a22c54151b79c29c6c9a4b28986f3af`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:a05cd40db5df192b41a87d288c98780daeba7665e52b02c9ddb14ac2bef84fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb8f78923fc858b5b19e2b3239aad1f2bff989beb74b9fd9b5becb941aa687e`

```dockerfile
```

-	Layers:
	-	`sha256:03a66b0f14f02f9d3de77a48ebc4bf1484c80c475ebe8a47215063766c6cdc4b`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 20.6 KB (20567 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8.0.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3a60b23d57a0a5945a63b3ee14b6c8fa5d82b11278f3ecd5d52fa999850b22fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114245888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371bfffc933532ead58b49dd77c659fa770b07de0898baa61fd9aa0fcf29d2c6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:38:13 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Fri, 08 May 2026 19:38:13 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Fri, 08 May 2026 19:38:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Fri, 08 May 2026 19:38:13 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:38:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:38:13 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:38:13 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:38:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:38:13 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:38:13 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
COPY index.html /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:38:13 GMT
USER varnish
# Fri, 08 May 2026 19:38:13 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:38:13 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62f5e803ffd19caa42da395fbdad66e0d1e57df08278891de44d133e257d743`  
		Last Modified: Fri, 08 May 2026 19:38:27 GMT  
		Size: 84.1 MB (84099127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e0e771f75f8b71c0be9f4bf566a9b3e76194ce490738638695f97842636dbe`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f1cf2b419f37c73aee1126aaab7a5ac5fcdc08981affbe8d26383fef3dfc83`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42817c86f5b88de25c323ba5dcf6d7a3a852ebafc0dc9855cdf9746e1808c222`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:ec3a17e688bc14a3fad5b5665bf5663c2a676b14d4af4871e195bb0b77161d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06d0a8881fd6f40d0454d5539045bfcdf230ed0c58213069d857f1c52c14f2c`

```dockerfile
```

-	Layers:
	-	`sha256:b6e9c99dff33245e656bfac655440da9a15e79bd3612bf23ac75a0511370583a`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
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
$ docker pull varnish@sha256:bb507a9c6b769c0bd5c43636ce4856b34bf6c4cdab9eb3f3642691b6c7b046cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9` - linux; amd64

```console
$ docker pull varnish@sha256:1821196fb9c9aa0b056d0d3394d85689a955705d0689ccc6ebdd8400d09db3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122289599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3bb3d6735c2b379e7f54f8198e10646a1d7c3b67deb93ec78653d3c2bdcd62`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:33 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 08 May 2026 19:36:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:36:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:36:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:33 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:36:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:33 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:33 GMT
USER varnish
# Fri, 08 May 2026 19:36:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:33 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c91c7abba5d319edc994cdbc9ee025cf097a0d326ce29d39d55cc39dc4bd57`  
		Last Modified: Fri, 08 May 2026 19:36:48 GMT  
		Size: 92.5 MB (92506489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e44e5a59f31b828040391fdad8b30537e0aeb356823881cdd527303b0773a`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c65346bdff8a0cf80ebfa8b46f05ffceb32305f260842196db5a25c326991e2`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037e71ec53b0a2895d978f7c96347e505f972ffaa858a3e49f806e3aa1595590`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:c95f04b77e6122f92631d8d82b74952933d5d11dda2e05a8fd11219f3a936f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b0310013cfe1a89a0c5f164e31a8bd3f3069b56ca8c1a545fe6ece8895c7ee`

```dockerfile
```

-	Layers:
	-	`sha256:07a6cbd4ea26d001da1e6968a6b7c0a9b1a0cd88b2436de2006e1c9c7c3afef4`  
		Last Modified: Fri, 08 May 2026 19:36:45 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fde4d6fa8e59786ca723ded32bfd39568b9024200a831a9004402c190885ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116279646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25776b366fe3813d4e39b9241c7dd793a8759f42c7615b8961839222c876b126`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:02 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:38:02 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 08 May 2026 19:38:02 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:38:02 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:38:02 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:38:02 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:38:02 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:38:02 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:38:02 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:38:02 GMT
USER varnish
# Fri, 08 May 2026 19:38:02 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:38:02 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63db5efe7e3cebee83d627b2bbae2e4533b6a0d552a3c923c442ebbbda7c013d`  
		Last Modified: Fri, 08 May 2026 19:38:16 GMT  
		Size: 86.1 MB (86133117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533278927ec1bdc0f2a79287974128713507865b5c43f492ba8dd0ce17419a9f`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b1567b21859c67ad54ffb11d72f9a1e6ab83620931b6f08296ccf5a593ebf`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4776f4e16d65904f664b9c241564ba75ed82f8949480ab1fc14df951d55eb373`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9` - unknown; unknown

```console
$ docker pull varnish@sha256:3e46b0fb8e88d93bc06a7970e34f419a65d9d25edb4439f57924db09728c343e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b6df8064b4c281891c8ea91f2d30f66e3c084de0c3866942a9be2607493187`

```dockerfile
```

-	Layers:
	-	`sha256:189656c0076e991c23d39a25816bbccb40449661ae72e6842a8ae989dff3dc0c`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0`

```console
$ docker pull varnish@sha256:bb507a9c6b769c0bd5c43636ce4856b34bf6c4cdab9eb3f3642691b6c7b046cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0` - linux; amd64

```console
$ docker pull varnish@sha256:1821196fb9c9aa0b056d0d3394d85689a955705d0689ccc6ebdd8400d09db3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122289599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3bb3d6735c2b379e7f54f8198e10646a1d7c3b67deb93ec78653d3c2bdcd62`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:33 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 08 May 2026 19:36:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:36:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:36:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:33 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:36:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:33 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:33 GMT
USER varnish
# Fri, 08 May 2026 19:36:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:33 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c91c7abba5d319edc994cdbc9ee025cf097a0d326ce29d39d55cc39dc4bd57`  
		Last Modified: Fri, 08 May 2026 19:36:48 GMT  
		Size: 92.5 MB (92506489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e44e5a59f31b828040391fdad8b30537e0aeb356823881cdd527303b0773a`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c65346bdff8a0cf80ebfa8b46f05ffceb32305f260842196db5a25c326991e2`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037e71ec53b0a2895d978f7c96347e505f972ffaa858a3e49f806e3aa1595590`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:c95f04b77e6122f92631d8d82b74952933d5d11dda2e05a8fd11219f3a936f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b0310013cfe1a89a0c5f164e31a8bd3f3069b56ca8c1a545fe6ece8895c7ee`

```dockerfile
```

-	Layers:
	-	`sha256:07a6cbd4ea26d001da1e6968a6b7c0a9b1a0cd88b2436de2006e1c9c7c3afef4`  
		Last Modified: Fri, 08 May 2026 19:36:45 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fde4d6fa8e59786ca723ded32bfd39568b9024200a831a9004402c190885ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116279646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25776b366fe3813d4e39b9241c7dd793a8759f42c7615b8961839222c876b126`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:02 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:38:02 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 08 May 2026 19:38:02 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:38:02 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:38:02 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:38:02 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:38:02 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:38:02 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:38:02 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:38:02 GMT
USER varnish
# Fri, 08 May 2026 19:38:02 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:38:02 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63db5efe7e3cebee83d627b2bbae2e4533b6a0d552a3c923c442ebbbda7c013d`  
		Last Modified: Fri, 08 May 2026 19:38:16 GMT  
		Size: 86.1 MB (86133117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533278927ec1bdc0f2a79287974128713507865b5c43f492ba8dd0ce17419a9f`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b1567b21859c67ad54ffb11d72f9a1e6ab83620931b6f08296ccf5a593ebf`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4776f4e16d65904f664b9c241564ba75ed82f8949480ab1fc14df951d55eb373`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0` - unknown; unknown

```console
$ docker pull varnish@sha256:3e46b0fb8e88d93bc06a7970e34f419a65d9d25edb4439f57924db09728c343e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b6df8064b4c281891c8ea91f2d30f66e3c084de0c3866942a9be2607493187`

```dockerfile
```

-	Layers:
	-	`sha256:189656c0076e991c23d39a25816bbccb40449661ae72e6842a8ae989dff3dc0c`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:9.0.1`

```console
$ docker pull varnish@sha256:bb507a9c6b769c0bd5c43636ce4856b34bf6c4cdab9eb3f3642691b6c7b046cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:9.0.1` - linux; amd64

```console
$ docker pull varnish@sha256:1821196fb9c9aa0b056d0d3394d85689a955705d0689ccc6ebdd8400d09db3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122289599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3bb3d6735c2b379e7f54f8198e10646a1d7c3b67deb93ec78653d3c2bdcd62`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:33 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 08 May 2026 19:36:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:36:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:36:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:33 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:36:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:33 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:33 GMT
USER varnish
# Fri, 08 May 2026 19:36:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:33 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c91c7abba5d319edc994cdbc9ee025cf097a0d326ce29d39d55cc39dc4bd57`  
		Last Modified: Fri, 08 May 2026 19:36:48 GMT  
		Size: 92.5 MB (92506489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e44e5a59f31b828040391fdad8b30537e0aeb356823881cdd527303b0773a`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c65346bdff8a0cf80ebfa8b46f05ffceb32305f260842196db5a25c326991e2`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037e71ec53b0a2895d978f7c96347e505f972ffaa858a3e49f806e3aa1595590`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:c95f04b77e6122f92631d8d82b74952933d5d11dda2e05a8fd11219f3a936f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b0310013cfe1a89a0c5f164e31a8bd3f3069b56ca8c1a545fe6ece8895c7ee`

```dockerfile
```

-	Layers:
	-	`sha256:07a6cbd4ea26d001da1e6968a6b7c0a9b1a0cd88b2436de2006e1c9c7c3afef4`  
		Last Modified: Fri, 08 May 2026 19:36:45 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:9.0.1` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fde4d6fa8e59786ca723ded32bfd39568b9024200a831a9004402c190885ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116279646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25776b366fe3813d4e39b9241c7dd793a8759f42c7615b8961839222c876b126`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:02 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:38:02 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 08 May 2026 19:38:02 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:38:02 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:38:02 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:38:02 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:38:02 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:38:02 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:38:02 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:38:02 GMT
USER varnish
# Fri, 08 May 2026 19:38:02 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:38:02 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63db5efe7e3cebee83d627b2bbae2e4533b6a0d552a3c923c442ebbbda7c013d`  
		Last Modified: Fri, 08 May 2026 19:38:16 GMT  
		Size: 86.1 MB (86133117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533278927ec1bdc0f2a79287974128713507865b5c43f492ba8dd0ce17419a9f`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b1567b21859c67ad54ffb11d72f9a1e6ab83620931b6f08296ccf5a593ebf`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4776f4e16d65904f664b9c241564ba75ed82f8949480ab1fc14df951d55eb373`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:9.0.1` - unknown; unknown

```console
$ docker pull varnish@sha256:3e46b0fb8e88d93bc06a7970e34f419a65d9d25edb4439f57924db09728c343e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b6df8064b4c281891c8ea91f2d30f66e3c084de0c3866942a9be2607493187`

```dockerfile
```

-	Layers:
	-	`sha256:189656c0076e991c23d39a25816bbccb40449661ae72e6842a8ae989dff3dc0c`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:fresh`

```console
$ docker pull varnish@sha256:bb507a9c6b769c0bd5c43636ce4856b34bf6c4cdab9eb3f3642691b6c7b046cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:1821196fb9c9aa0b056d0d3394d85689a955705d0689ccc6ebdd8400d09db3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122289599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3bb3d6735c2b379e7f54f8198e10646a1d7c3b67deb93ec78653d3c2bdcd62`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:33 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 08 May 2026 19:36:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:36:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:36:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:33 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:36:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:33 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:33 GMT
USER varnish
# Fri, 08 May 2026 19:36:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:33 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c91c7abba5d319edc994cdbc9ee025cf097a0d326ce29d39d55cc39dc4bd57`  
		Last Modified: Fri, 08 May 2026 19:36:48 GMT  
		Size: 92.5 MB (92506489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e44e5a59f31b828040391fdad8b30537e0aeb356823881cdd527303b0773a`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c65346bdff8a0cf80ebfa8b46f05ffceb32305f260842196db5a25c326991e2`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037e71ec53b0a2895d978f7c96347e505f972ffaa858a3e49f806e3aa1595590`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:c95f04b77e6122f92631d8d82b74952933d5d11dda2e05a8fd11219f3a936f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b0310013cfe1a89a0c5f164e31a8bd3f3069b56ca8c1a545fe6ece8895c7ee`

```dockerfile
```

-	Layers:
	-	`sha256:07a6cbd4ea26d001da1e6968a6b7c0a9b1a0cd88b2436de2006e1c9c7c3afef4`  
		Last Modified: Fri, 08 May 2026 19:36:45 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fde4d6fa8e59786ca723ded32bfd39568b9024200a831a9004402c190885ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116279646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25776b366fe3813d4e39b9241c7dd793a8759f42c7615b8961839222c876b126`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:02 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:38:02 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 08 May 2026 19:38:02 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:38:02 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:38:02 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:38:02 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:38:02 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:38:02 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:38:02 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:38:02 GMT
USER varnish
# Fri, 08 May 2026 19:38:02 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:38:02 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63db5efe7e3cebee83d627b2bbae2e4533b6a0d552a3c923c442ebbbda7c013d`  
		Last Modified: Fri, 08 May 2026 19:38:16 GMT  
		Size: 86.1 MB (86133117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533278927ec1bdc0f2a79287974128713507865b5c43f492ba8dd0ce17419a9f`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b1567b21859c67ad54ffb11d72f9a1e6ab83620931b6f08296ccf5a593ebf`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4776f4e16d65904f664b9c241564ba75ed82f8949480ab1fc14df951d55eb373`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:3e46b0fb8e88d93bc06a7970e34f419a65d9d25edb4439f57924db09728c343e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b6df8064b4c281891c8ea91f2d30f66e3c084de0c3866942a9be2607493187`

```dockerfile
```

-	Layers:
	-	`sha256:189656c0076e991c23d39a25816bbccb40449661ae72e6842a8ae989dff3dc0c`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:latest`

```console
$ docker pull varnish@sha256:bb507a9c6b769c0bd5c43636ce4856b34bf6c4cdab9eb3f3642691b6c7b046cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:1821196fb9c9aa0b056d0d3394d85689a955705d0689ccc6ebdd8400d09db3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122289599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3bb3d6735c2b379e7f54f8198e10646a1d7c3b67deb93ec78653d3c2bdcd62`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:33 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 08 May 2026 19:36:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:36:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:36:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:33 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:36:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:33 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 08 May 2026 19:36:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:33 GMT
USER varnish
# Fri, 08 May 2026 19:36:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:33 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c91c7abba5d319edc994cdbc9ee025cf097a0d326ce29d39d55cc39dc4bd57`  
		Last Modified: Fri, 08 May 2026 19:36:48 GMT  
		Size: 92.5 MB (92506489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e44e5a59f31b828040391fdad8b30537e0aeb356823881cdd527303b0773a`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c65346bdff8a0cf80ebfa8b46f05ffceb32305f260842196db5a25c326991e2`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037e71ec53b0a2895d978f7c96347e505f972ffaa858a3e49f806e3aa1595590`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:c95f04b77e6122f92631d8d82b74952933d5d11dda2e05a8fd11219f3a936f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b0310013cfe1a89a0c5f164e31a8bd3f3069b56ca8c1a545fe6ece8895c7ee`

```dockerfile
```

-	Layers:
	-	`sha256:07a6cbd4ea26d001da1e6968a6b7c0a9b1a0cd88b2436de2006e1c9c7c3afef4`  
		Last Modified: Fri, 08 May 2026 19:36:45 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fde4d6fa8e59786ca723ded32bfd39568b9024200a831a9004402c190885ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116279646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25776b366fe3813d4e39b9241c7dd793a8759f42c7615b8961839222c876b126`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:02 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:38:02 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 08 May 2026 19:38:02 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:38:02 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:38:02 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:38:02 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:38:02 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:38:02 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:38:02 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 08 May 2026 19:38:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:38:02 GMT
USER varnish
# Fri, 08 May 2026 19:38:02 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:38:02 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63db5efe7e3cebee83d627b2bbae2e4533b6a0d552a3c923c442ebbbda7c013d`  
		Last Modified: Fri, 08 May 2026 19:38:16 GMT  
		Size: 86.1 MB (86133117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533278927ec1bdc0f2a79287974128713507865b5c43f492ba8dd0ce17419a9f`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b1567b21859c67ad54ffb11d72f9a1e6ab83620931b6f08296ccf5a593ebf`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4776f4e16d65904f664b9c241564ba75ed82f8949480ab1fc14df951d55eb373`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:3e46b0fb8e88d93bc06a7970e34f419a65d9d25edb4439f57924db09728c343e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b6df8064b4c281891c8ea91f2d30f66e3c084de0c3866942a9be2607493187`

```dockerfile
```

-	Layers:
	-	`sha256:189656c0076e991c23d39a25816bbccb40449661ae72e6842a8ae989dff3dc0c`  
		Last Modified: Fri, 08 May 2026 19:38:13 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json

## `varnish:old`

```console
$ docker pull varnish@sha256:8b618ce555c65ff1c3ff32fb2e03c0e45105c6f8e001cfa372e4ed47a5722744
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:6c13f546e900db1c5b45166cec3fdfb2d1d02d6166c6c2122ff4ad57fdbb13a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120238661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b268ab5d396ab64e0352f63a0bbb11beb2e266caf06b6aec8666ead792ec97`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:36:41 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:41 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Fri, 08 May 2026 19:36:41 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Fri, 08 May 2026 19:36:41 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Fri, 08 May 2026 19:36:41 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:36:41 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:36:41 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:41 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:36:41 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:41 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:41 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
COPY index.html /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:36:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:41 GMT
USER varnish
# Fri, 08 May 2026 19:36:41 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:41 GMT
CMD []
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7365b8d155025cf0b3a8eeea351689542d7bd64582e909dac84553d0bb1134`  
		Last Modified: Fri, 08 May 2026 19:36:55 GMT  
		Size: 90.5 MB (90455320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e7eef1eb5f8e9691ab443fd2945693f755baa9ac07eb2aaa68121baebf45f1`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdefd778b717d91f169c1fae86e25549dedeed932149a459653d173cbd9c4e6b`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949cc04440888046d9dc6651d062e77d6a22c54151b79c29c6c9a4b28986f3af`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:a05cd40db5df192b41a87d288c98780daeba7665e52b02c9ddb14ac2bef84fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb8f78923fc858b5b19e2b3239aad1f2bff989beb74b9fd9b5becb941aa687e`

```dockerfile
```

-	Layers:
	-	`sha256:03a66b0f14f02f9d3de77a48ebc4bf1484c80c475ebe8a47215063766c6cdc4b`  
		Last Modified: Fri, 08 May 2026 19:36:52 GMT  
		Size: 20.6 KB (20567 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:3a60b23d57a0a5945a63b3ee14b6c8fa5d82b11278f3ecd5d52fa999850b22fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114245888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371bfffc933532ead58b49dd77c659fa770b07de0898baa61fd9aa0fcf29d2c6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:13 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:38:13 GMT
ARG VARNISH_VERSION_NUMBER=8.0.1-1
# Fri, 08 May 2026 19:38:13 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Fri, 08 May 2026 19:38:13 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Fri, 08 May 2026 19:38:13 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 08 May 2026 19:38:13 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 08 May 2026 19:38:13 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:38:13 GMT
ENV VSM_NOPID=1
# Fri, 08 May 2026 19:38:13 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=8.0.1-1 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION} 				libgetdns10t64 				netbase;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:38:13 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:38:13 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
COPY index.html /etc/varnish/ # buildkit
# Fri, 08 May 2026 19:38:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:38:13 GMT
USER varnish
# Fri, 08 May 2026 19:38:13 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:38:13 GMT
CMD []
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62f5e803ffd19caa42da395fbdad66e0d1e57df08278891de44d133e257d743`  
		Last Modified: Fri, 08 May 2026 19:38:27 GMT  
		Size: 84.1 MB (84099127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e0e771f75f8b71c0be9f4bf566a9b3e76194ce490738638695f97842636dbe`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f1cf2b419f37c73aee1126aaab7a5ac5fcdc08981affbe8d26383fef3dfc83`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42817c86f5b88de25c323ba5dcf6d7a3a852ebafc0dc9855cdf9746e1808c222`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:ec3a17e688bc14a3fad5b5665bf5663c2a676b14d4af4871e195bb0b77161d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06d0a8881fd6f40d0454d5539045bfcdf230ed0c58213069d857f1c52c14f2c`

```dockerfile
```

-	Layers:
	-	`sha256:b6e9c99dff33245e656bfac655440da9a15e79bd3612bf23ac75a0511370583a`  
		Last Modified: Fri, 08 May 2026 19:38:25 GMT  
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
$ docker pull varnish@sha256:ec99f528eb409789d6b2d01178a36388f21d5a19faab7f695e39ad5e23eca5ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:f319003ae2e7f71186f5577c29ea2a8eaee3fb9840e9d6e12235f44fe11b8e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121850316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c112f173adbd5ccc82a3d685d20bd6a1b68379e28ec47ffb95b7b877dacb5fb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:36:07 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:36:07 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Fri, 08 May 2026 19:36:07 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:36:07 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:36:07 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:36:07 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:36:07 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:36:07 GMT
CMD []
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc62d7f7ac1905a4537698365a041b779630457cf204f14d41d3c0343befaa75`  
		Last Modified: Fri, 08 May 2026 19:36:21 GMT  
		Size: 93.6 MB (93613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f806ed6a57a7942d1867a26edb91b295bed9dc11ea50e0800d3d10f259a1f2f`  
		Last Modified: Fri, 08 May 2026 19:36:19 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:af5f6161c930c6e00468d5b2e9edeffed9506e572adf6064af08b6e037280a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825723351a505a8866775871508482db3d7ec94960c07eaf60894476631c5997`

```dockerfile
```

-	Layers:
	-	`sha256:2adfa1ab1b5d353f8b22c4a047c806f633f5a024c3463d068a8f00fe790fb1dd`  
		Last Modified: Fri, 08 May 2026 19:36:19 GMT  
		Size: 12.7 KB (12669 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:44575916983ffb89251685ed9f6cc4162f4a7406933eb193c894f51c27805b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116285686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88d535d8298265194ebdb4873ea88475db031f9a7c73fcbad57052543cb5d23`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:37:47 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 08 May 2026 19:37:47 GMT
ARG VARNISH_VERSION_NUMBER=6.0.17-1
# Fri, 08 May 2026 19:37:47 GMT
ENV VARNISH_SIZE=100M
# Fri, 08 May 2026 19:37:47 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=6.0.17-1
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="curl gpg";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION};     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 08 May 2026 19:37:47 GMT
WORKDIR /etc/varnish
# Fri, 08 May 2026 19:37:47 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:37:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 08 May 2026 19:37:47 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 08 May 2026 19:37:47 GMT
CMD []
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd1683cbe057ee5d4edda621a71a46b2442071426c7494653340127d1d7e59c`  
		Last Modified: Fri, 08 May 2026 19:38:01 GMT  
		Size: 88.2 MB (88168766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088683e2f67788e0a35e995abee66f97048da5c83cc71661a3aafa6be018c5c6`  
		Last Modified: Fri, 08 May 2026 19:37:59 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:0023c08ac49f87eb5cf42dd4e14e19f3727fe157d3513dd5d030f39a072103c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a56a8f34ffaba5ece5035ff54335c52a5fe49bb4868bcd9f8c0995a8adc58b9`

```dockerfile
```

-	Layers:
	-	`sha256:768dea45adb67a07408f99f9eec95b7c0a03b5f81376de6c6c4c28f4f3457f55`  
		Last Modified: Fri, 08 May 2026 19:37:59 GMT  
		Size: 12.8 KB (12760 bytes)  
		MIME: application/vnd.in-toto+json
