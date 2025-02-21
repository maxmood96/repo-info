## `varnish:old`

```console
$ docker pull varnish@sha256:bcb294ac95cb95dbe79d4496685076109ec8e38f9a1cd35ba74dfb8278199dcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `varnish:old` - linux; amd64

```console
$ docker pull varnish@sha256:9f8e5099ebe0d8c36e5275c92ac41941ac656b81ee99b2242f1bfd2eccf7a870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133947580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0ce3671cc93cda6b4fda1720db7d6f8f58c1f10ad062a16115db45009d2d8d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da20651324383642e77305fdc8e5ee80e40ed9110f7f7fa3a44ca0124caf6b`  
		Last Modified: Tue, 04 Feb 2025 04:26:04 GMT  
		Size: 105.7 MB (105733248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2958af66e2a26b4907cb4ac12a284d9c9037bb0675929e18c0684a07e175f3d4`  
		Last Modified: Tue, 04 Feb 2025 04:26:00 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18fc8b1264f71a4e5fc52f2bc6e74d64d699c1b0450cf6ce424accae804cc05`  
		Last Modified: Tue, 04 Feb 2025 04:26:03 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:1a5278c3c63de014ce017013bea0011b075c54752ff654276b6eab53026a8e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c3c464581b3f712bbb05dc82764f731c8f5c3ad4549e044e17ecaa7787d902`

```dockerfile
```

-	Layers:
	-	`sha256:b177209b0f766e9795f77d086a175574726188b79051e0e465987a5054710e81`  
		Last Modified: Tue, 04 Feb 2025 04:26:03 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7f00b98a92de69cd457912557de6eccf4b5f77a84aa7397cd379344ebb195f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104301206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4737fe407eed2498c6bc98e0e815bcbf9e6053167e439cdd8f1c03a9d3de4f16`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0334412056fcdb41bb87cb1c5f88e11f2fd9142febf8c4630223b5ea3d23d611`  
		Last Modified: Tue, 04 Feb 2025 10:38:43 GMT  
		Size: 80.4 MB (80384634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c455f50c99d6fd39c99189db47154c6a95c0e513352d0158d476fb31bbe1a5`  
		Last Modified: Tue, 04 Feb 2025 10:38:40 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec1263c72ce0184b3c076e3b96c4fe486aeda6066836298966e9c4eaa644d19`  
		Last Modified: Tue, 04 Feb 2025 10:38:41 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:56bdd5a66b1e8f70104346d0211d63e599b66d0402acb722b031f031d7dc699c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f25c88f3c45c959820d334d243f4f159e515a1e6e13fb0055691f1680eccadf`

```dockerfile
```

-	Layers:
	-	`sha256:be91b5c55be1d84912b05c54f316e9726f2cd6cd986bc250ea2222966cb41d87`  
		Last Modified: Tue, 04 Feb 2025 10:38:40 GMT  
		Size: 18.9 KB (18869 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c801be4e1a20b8e9339731e702da0da4e11f41ac7dd90f6f1bf28da481e854ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128229621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d37be3ebfe7fa3e9ef4bdc811cfcaf0b3286b60910174c89d8ba453edeb991d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64aace46cfd9caae7afaabd66dc21a83b16e8e44a1d596bab797297d7b9bbf54`  
		Last Modified: Tue, 04 Feb 2025 08:55:27 GMT  
		Size: 100.2 MB (100186706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeebc0efde50ade528714e6f2d8bdada5ed3a515c5a7bd9b69e067f5acfdb285`  
		Last Modified: Tue, 04 Feb 2025 08:55:24 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d59aa3d57786ece62d55c13f81cfa7e747079ec7df2a274b626f55dbde6f3b8`  
		Last Modified: Tue, 04 Feb 2025 08:55:24 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:6ea76fdf4edcf804b55138572f5c2f086913c0cbddfdf82ed5b9c8092448b642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638f6f181c95305f24938dfb630504812e79972ba4ffe9ba754b36d70fa3c3c8`

```dockerfile
```

-	Layers:
	-	`sha256:f3fc5809baa92223eed3288fb9105aa6a18e4124f8f38edb6278ff984fa8fa7f`  
		Last Modified: Tue, 04 Feb 2025 08:55:24 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; 386

```console
$ docker pull varnish@sha256:32961a84374f32ce335c3c2ddc6b9b654c8dceb2681ee77352fd1b1bf8c2a4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131058305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6590994ca1a7c60f38f951597dff1f567e90c921411c9d25f7ea0a2362a5e00`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31381739b1cf1d2013ab05495584256c14f70ff0690459179356fb415eaace20`  
		Last Modified: Tue, 04 Feb 2025 04:26:04 GMT  
		Size: 101.9 MB (101868816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22882845a4dd3b8960abc19f5cbbfbae10af74e6657d93ee64322171a1138aba`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63cfb1491d67d2f05f2d7991a2b1800d36bbda089293f6659a0b8b489e95c60`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:95bb88de67b2a8eafd754aad33701a7e7ebf11fa3ef9bc781b7ac22c3803bc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d057c2da4e156b6fee96bbbc7530fc6e4e5ec0e3cca758cd4ad56b383aa1c853`

```dockerfile
```

-	Layers:
	-	`sha256:bcf1cc90e51943acc8378004179404e8764fa3100f9da307356624fc646ac2e4`  
		Last Modified: Tue, 04 Feb 2025 04:26:01 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; ppc64le

```console
$ docker pull varnish@sha256:85be13e729f7f906682e94c595588e2e885c4f06e2e0192db93572b01144079d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136725152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4ce6bc7d2c87c66af78d8ad62792f76e4be85f8f058c0702ce1f3ece23c1ad`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5be896b554e305ce9876e38b680f5b6beadb99b1f0e05849caf16c75362a6eb`  
		Last Modified: Tue, 04 Feb 2025 07:19:25 GMT  
		Size: 104.7 MB (104678341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8abe61a6ee046cb87fece196f030318a2cb18915ffaa33eff25b39bdac3447`  
		Last Modified: Tue, 04 Feb 2025 07:19:18 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9147ea092c921f02dcd7acd28da634f45c389369e9fa2531659baa12814082`  
		Last Modified: Tue, 04 Feb 2025 07:19:18 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:ac40e8e229b09a1c6afb0236a0e1c0d5d2423c6059e32cbafe7fd497f33441d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230c556defdd7815cee8ee1eac83bca17d87ad94f626f9e60fba665e140c3557`

```dockerfile
```

-	Layers:
	-	`sha256:a019a7a0ab02e99006a2e095c17e6ca5e6c5beaae0eefc3d38890a8a9448d25c`  
		Last Modified: Tue, 04 Feb 2025 07:19:18 GMT  
		Size: 18.8 KB (18841 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old` - linux; s390x

```console
$ docker pull varnish@sha256:9308abcf7631383519d5a6ca5f02f2d4304f98c74d6d5b038e75ee22d6251617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111830926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5094488ac89b6f763b8dbfa26124b1f16c24e66d39530019e99171a94cecb8a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Sep 2024 20:20:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Mon, 16 Sep 2024 20:20:48 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_VERSION=7.5.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Mon, 16 Sep 2024 20:20:48 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Mon, 16 Sep 2024 20:20:48 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Mon, 16 Sep 2024 20:20:48 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Sep 2024 20:20:48 GMT
# ARGS: PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d VARNISH_VERSION=7.5.0 DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 VARNISH_MODULES_VERSION=0.24.0 VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VMOD_DYNAMIC_VERSION=2.8.0-1 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
WORKDIR /etc/varnish
# Mon, 16 Sep 2024 20:20:48 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 16 Sep 2024 20:20:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Sep 2024 20:20:48 GMT
USER varnish
# Mon, 16 Sep 2024 20:20:48 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Sep 2024 20:20:48 GMT
CMD []
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364ad64e026fa762ad2e2a60461d67dcd88dfba94cb5d7391714744909a3049e`  
		Last Modified: Tue, 04 Feb 2025 07:26:35 GMT  
		Size: 85.0 MB (84970267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78102bb9114e0acb6a8df6ea36ac58d198afc45f208c570d4e85cf4d6fe46d4`  
		Last Modified: Tue, 04 Feb 2025 07:26:33 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e52671a279afd65d319f7aa79aeb28a6d14f8f05fe7c49968cb745383c6f80`  
		Last Modified: Tue, 04 Feb 2025 07:26:34 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old` - unknown; unknown

```console
$ docker pull varnish@sha256:a236c3e9cc45ed66321d31d1bcd9198268dcdc8738606bc19d3ca4a8b3ed3141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a52f78ab1eb363fd7e44a1fd8a767b9225a465a2bd36b8539fa3443c2de1645`

```dockerfile
```

-	Layers:
	-	`sha256:262287fbe2a40af785d7294eef9d402afd7c52f95b73d185dd4d87772661f3e7`  
		Last Modified: Tue, 04 Feb 2025 07:26:33 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.in-toto+json
