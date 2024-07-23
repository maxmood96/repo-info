## `varnish:fresh`

```console
$ docker pull varnish@sha256:c73f3060bb27ba923973c83ad84c354b4b636469862ace996a3fb97973942c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:c6245b1f63629f17d20d1d309de3f04aedf929e0a4281c8cd3a6a620daf384c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134862254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d25f7e828ba6e722bb372cb9999fd138682017e0d0b82b4b09a62257f6a9d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:53:11 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:53:11 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:53:11 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:53:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:53:12 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:53:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:53:12 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:56:00 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:56:01 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:56:01 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:56:01 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:56:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:56:01 GMT
USER varnish
# Tue, 02 Jul 2024 04:56:01 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:56:01 GMT
CMD []
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16282c1add7c3baf6d62eb91f9434ef31e076bad8ac6529d2cbfd698fe683741`  
		Last Modified: Tue, 02 Jul 2024 05:08:45 GMT  
		Size: 105.7 MB (105733962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c568179d88274cbd7625ae74d29623d927c778a5f308ca67a42c6161e40344a1`  
		Last Modified: Tue, 02 Jul 2024 05:08:31 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d438f5bf9894896e1ddf61c4267996ae7846e743e09b3ec47e2d3dc15054f33`  
		Last Modified: Tue, 02 Jul 2024 05:08:31 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm variant v7

```console
$ docker pull varnish@sha256:5d42139183e4f47d78d822b9e4480b16ce595a41d57025f39f04c5592f404469
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105116485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95cda33b7f3565cc4e9bcb9a5d06ac54e46467226f4f535f1d1d8f7566d138e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:55:51 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 03:55:51 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 03:55:52 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 03:55:52 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 03:55:52 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 03:55:52 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 03:55:52 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 03:55:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 03:55:53 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 03:55:54 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 03:55:54 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 04:00:23 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 04:00:25 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 04:00:25 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 04:00:25 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 04:00:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 04:00:25 GMT
USER varnish
# Tue, 23 Jul 2024 04:00:26 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 04:00:26 GMT
CMD []
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd097c1c4415b1b3aae318c4db2859c71ecd21b4c9dbef64833e45dadaa55fb3`  
		Last Modified: Tue, 23 Jul 2024 04:19:12 GMT  
		Size: 80.4 MB (80396271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fef9d100de5ebc6fdeb7c8039234b68b4a5fea4610ff23551a8b07c73bc7f69`  
		Last Modified: Tue, 23 Jul 2024 04:18:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e55c6f0e570833bd4bc52f176994307220b30e6eae17bafcbfe9ae92388fa6`  
		Last Modified: Tue, 23 Jul 2024 04:18:54 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:944e5e7eedff373706f516f36571fcc31e190d2b7e8693ad6528e62a23ee4b1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129339124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b778778b32af3328bcc517f80f8d47dfc7f858dedff1babf6ce45657180fa805`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:12:06 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 02 Jul 2024 04:12:06 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 02 Jul 2024 04:12:06 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 02 Jul 2024 04:12:07 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 02 Jul 2024 04:12:07 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 02 Jul 2024 04:12:07 GMT
ENV VARNISH_SIZE=100M
# Tue, 02 Jul 2024 04:14:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 02 Jul 2024 04:14:29 GMT
WORKDIR /etc/varnish
# Tue, 02 Jul 2024 04:14:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:14:30 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 02 Jul 2024 04:14:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 02 Jul 2024 04:14:30 GMT
USER varnish
# Tue, 02 Jul 2024 04:14:30 GMT
EXPOSE 80 8443
# Tue, 02 Jul 2024 04:14:30 GMT
CMD []
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05fe21d9623c5387c391eec805dcd1526fb2ba19a3e0c4e632507c4f13e0dfd`  
		Last Modified: Tue, 02 Jul 2024 04:25:24 GMT  
		Size: 100.2 MB (100180549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7956d79257db29f3e1df4726e5423044d921f36494d042aca76d7b44cf787505`  
		Last Modified: Tue, 02 Jul 2024 04:25:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3165c0b54f641e6fa1b49d6d5236759255cf0c4362f3df5b3219ffd917aa7be`  
		Last Modified: Tue, 02 Jul 2024 04:25:14 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; 386

```console
$ docker pull varnish@sha256:678e6b56433c99ca3a7624e92d1954431eefb13e6877e8cf7f07cef5f14a5560
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132020330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e721c3a02b2cb585188e7580a66ed0bcee443bdc6f15d01bc4c5bac3f05637`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 03:54:13 GMT
ADD file:9b63a9d86a51a3d56d700d09e1152578d700ba4453d852325d8eb9896534f3ba in / 
# Tue, 23 Jul 2024 03:54:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:17:41 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 04:17:41 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 04:17:41 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 04:17:41 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 04:17:42 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 04:17:42 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 04:17:42 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 04:17:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 04:17:42 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 04:17:42 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 04:17:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 04:21:10 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 04:21:12 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 04:21:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 04:21:12 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 04:21:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 04:21:13 GMT
USER varnish
# Tue, 23 Jul 2024 04:21:13 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 04:21:13 GMT
CMD []
```

-	Layers:
	-	`sha256:7fa64a47f35cb425a1275bff76c45df3b76d3ff6b07911737090b82e4f221e93`  
		Last Modified: Tue, 23 Jul 2024 03:57:51 GMT  
		Size: 30.1 MB (30144309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce7b36b762d21d263f6e6fc649a61a97daa32a0cbd5c430176c94597156d2c`  
		Last Modified: Tue, 23 Jul 2024 04:36:25 GMT  
		Size: 101.9 MB (101874009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea5888fbac40b806da484653a180325897e23822bf1809dd7f0b007d7c77651`  
		Last Modified: Tue, 23 Jul 2024 04:36:05 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca46553d810eb9eb67ad175d87d38e09032a974c82428ccd808113a29d1473e`  
		Last Modified: Tue, 23 Jul 2024 04:36:06 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; ppc64le

```console
$ docker pull varnish@sha256:04a3896cf12d9c34ac580245d7479022e974248e7fc19c4738a299774f8ed323
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137791397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e094e8905c540f533e7ccd4b4714f49010f1dc5e8cd3da6a26c26e0afac51832`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 01:26:56 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Tue, 23 Jul 2024 01:26:58 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:58:42 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 01:58:42 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 01:58:43 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 01:58:43 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 01:58:43 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 01:58:44 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 01:58:45 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 01:58:45 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 01:58:45 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 02:03:04 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 02:03:08 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 02:03:08 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:03:09 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 02:03:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 02:03:09 GMT
USER varnish
# Tue, 23 Jul 2024 02:03:09 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 02:03:10 GMT
CMD []
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b4f270ca2ccef2786b50cdffe74b172b9f27330341d9a33af90d3f0015ca88`  
		Last Modified: Tue, 23 Jul 2024 02:23:35 GMT  
		Size: 104.7 MB (104667110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea004555eaacc47df18a7b2c1fb069f096fc3912fc586d9686ed12162c5ba47`  
		Last Modified: Tue, 23 Jul 2024 02:23:18 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d0aaf3a235a3b67bd395d526e0dab4d5c87bdac22b2038da3781d88fe2052`  
		Last Modified: Tue, 23 Jul 2024 02:23:18 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh` - linux; s390x

```console
$ docker pull varnish@sha256:a2ab708eed88d44d2e33921bc9673525c508f8baf93925ccba284e7c866eda01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112436029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729dc6a84568359196cc9893251e6d87091e64bc5771033db5ffbd598a7bc39`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 23 Jul 2024 02:27:49 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Tue, 23 Jul 2024 02:27:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:25:17 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 23 Jul 2024 03:25:17 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 23 Jul 2024 03:25:17 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 23 Jul 2024 03:25:18 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 23 Jul 2024 03:25:18 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 23 Jul 2024 03:25:18 GMT
ENV VARNISH_SIZE=100M
# Tue, 23 Jul 2024 03:27:41 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS libgetdns10;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 23 Jul 2024 03:27:45 GMT
WORKDIR /etc/varnish
# Tue, 23 Jul 2024 03:27:45 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:27:45 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 23 Jul 2024 03:27:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 23 Jul 2024 03:27:45 GMT
USER varnish
# Tue, 23 Jul 2024 03:27:45 GMT
EXPOSE 80 8443
# Tue, 23 Jul 2024 03:27:45 GMT
CMD []
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0f298f5ea636629583c7bb74172643b36a7b7fe33844a9645b1b77a757e043`  
		Last Modified: Tue, 23 Jul 2024 03:39:58 GMT  
		Size: 84.9 MB (84943920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728b95bcd97f9daaacbef71368158b0a2e3fc01d08fcd8f042c8ad4852e27ddb`  
		Last Modified: Tue, 23 Jul 2024 03:39:46 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63979c06f1ee7ecc8e2b43664c3594622babd6fc5ae9247cb17e9baf5e45c801`  
		Last Modified: Tue, 23 Jul 2024 03:39:46 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
