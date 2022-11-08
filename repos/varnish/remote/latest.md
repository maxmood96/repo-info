## `varnish:latest`

```console
$ docker pull varnish@sha256:ec9915981892e41bb2f7b3fb4c656cee08a518517dd04f6095cc2bd6b086f9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:e313fa4401f2854e04eeaa6910137a0056b1456b7b0fa7457c527e682a73e33b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106849216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e82dd14490d6738f10f02600cfc820167851226ba7393bcfd1e5e561fd0a30`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:03:55 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Tue, 08 Nov 2022 18:53:28 GMT
ARG VARNISH_VERSION=7.2.1
# Tue, 08 Nov 2022 18:53:29 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Tue, 08 Nov 2022 18:53:29 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Tue, 08 Nov 2022 18:53:29 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Tue, 08 Nov 2022 18:53:29 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 08 Nov 2022 18:53:29 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Tue, 08 Nov 2022 18:53:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Tue, 08 Nov 2022 18:53:29 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Tue, 08 Nov 2022 18:53:29 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Tue, 08 Nov 2022 18:53:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 08 Nov 2022 18:56:54 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 08 Nov 2022 18:56:55 GMT
WORKDIR /etc/varnish
# Tue, 08 Nov 2022 18:56:55 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 08 Nov 2022 18:56:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 08 Nov 2022 18:56:55 GMT
USER varnish
# Tue, 08 Nov 2022 18:56:55 GMT
EXPOSE 80 8443
# Tue, 08 Nov 2022 18:56:55 GMT
CMD []
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bae733ac90afc06f167fbfb3e3e5d36a1cf9516d71449dfc3cfaa83cc6db2b`  
		Last Modified: Tue, 08 Nov 2022 19:05:52 GMT  
		Size: 75.4 MB (75428685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624b5d92e6f3cd8c14eb61df8556209ab15b692d56a0bcb1c12468cd643b3517`  
		Last Modified: Tue, 08 Nov 2022 19:05:42 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:3f8f4f88f2b9ffafd1905421125971c63a0b9a27ece9b074e05cc0a692a3c70d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83187801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3c3ebd163c397c7362d37616c25fc371718b4c8147078cacb83ebe6772c9ce`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 03:14:27 GMT
ADD file:0d2a17d07f391dfbf63c00d2b826373c98aaf6ab777481e33d4bee6d57c4a0b0 in / 
# Tue, 25 Oct 2022 03:14:27 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:18:32 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Wed, 26 Oct 2022 04:18:32 GMT
ARG VARNISH_VERSION=7.2.0
# Wed, 26 Oct 2022 04:18:32 GMT
ARG DIST_SHA512=d9a57d644d1b1456ee96ee84182f816b3b693fe2d9cc4b1859b62a836ee8c7d51025bb96efbc0ebc82349f60b2f186335436d76c12a5257c0560572db9d01133
# Wed, 26 Oct 2022 04:18:32 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Wed, 26 Oct 2022 04:18:32 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Wed, 26 Oct 2022 04:18:32 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Wed, 26 Oct 2022 04:18:32 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Wed, 26 Oct 2022 04:18:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Wed, 26 Oct 2022 04:18:32 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Wed, 26 Oct 2022 04:18:32 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Wed, 26 Oct 2022 04:18:33 GMT
ENV VARNISH_SIZE=100M
# Wed, 26 Oct 2022 04:21:34 GMT
# ARGS: DIST_SHA512=d9a57d644d1b1456ee96ee84182f816b3b693fe2d9cc4b1859b62a836ee8c7d51025bb96efbc0ebc82349f60b2f186335436d76c12a5257c0560572db9d01133 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.0 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.0.tgz -o $tmpdir/orig.tgz;     echo "d9a57d644d1b1456ee96ee84182f816b3b693fe2d9cc4b1859b62a836ee8c7d51025bb96efbc0ebc82349f60b2f186335436d76c12a5257c0560572db9d01133  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Wed, 26 Oct 2022 04:21:34 GMT
WORKDIR /etc/varnish
# Wed, 26 Oct 2022 04:21:35 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Wed, 26 Oct 2022 04:21:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 26 Oct 2022 04:21:35 GMT
USER varnish
# Wed, 26 Oct 2022 04:21:35 GMT
EXPOSE 80 8443
# Wed, 26 Oct 2022 04:21:35 GMT
CMD []
```

-	Layers:
	-	`sha256:e96255deabf6ae29e08aa044ffd2843f7a10c579cc8207bf0ddf13a90d192020`  
		Last Modified: Tue, 25 Oct 2022 03:21:16 GMT  
		Size: 26.6 MB (26579293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1779b43ed8c042b7cb5f0a415a22456a7833818b171ab793e1cd3c30e4555639`  
		Last Modified: Wed, 26 Oct 2022 04:31:04 GMT  
		Size: 56.6 MB (56608016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b94df6002528cbfafb48bc1bfb8db6a8d254b7e668a686e0ce9cfe84437ea4`  
		Last Modified: Wed, 26 Oct 2022 04:30:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:07bbbdb43cac6d60fa13d7f99a2960dfc7e29fea102984539e603067c51f15e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99412516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2938bfd77b00a8f5dc79537b75c6f9302fc1008081483716398c168b536e5fcc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:47:36 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 13 Sep 2022 13:47:37 GMT
ARG VARNISH_VERSION=7.1.1
# Tue, 13 Sep 2022 13:47:38 GMT
ARG DIST_SHA512=7c3c081bd37c63b429337a25ebc0c14d780b0c4fd235d18b9ac1004e0bb2f65e70664c5bd25c5d941deeb6bc078f344fa2629cf0d641a0149fe29dcfa07ffcd2
# Tue, 13 Sep 2022 13:47:39 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 13 Sep 2022 13:47:40 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 13 Sep 2022 13:47:41 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 13 Sep 2022 13:47:42 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Tue, 13 Sep 2022 13:47:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Tue, 13 Sep 2022 13:47:44 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Tue, 13 Sep 2022 13:47:45 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Tue, 13 Sep 2022 13:47:46 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 Sep 2022 13:50:44 GMT
# ARGS: DIST_SHA512=7c3c081bd37c63b429337a25ebc0c14d780b0c4fd235d18b9ac1004e0bb2f65e70664c5bd25c5d941deeb6bc078f344fa2629cf0d641a0149fe29dcfa07ffcd2 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.1 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.1.tgz -o $tmpdir/orig.tgz;     echo "7c3c081bd37c63b429337a25ebc0c14d780b0c4fd235d18b9ac1004e0bb2f65e70664c5bd25c5d941deeb6bc078f344fa2629cf0d641a0149fe29dcfa07ffcd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 13 Sep 2022 13:50:45 GMT
WORKDIR /etc/varnish
# Tue, 13 Sep 2022 13:50:46 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 13 Sep 2022 13:50:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 Sep 2022 13:50:47 GMT
USER varnish
# Tue, 13 Sep 2022 13:50:48 GMT
EXPOSE 80 8443
# Tue, 13 Sep 2022 13:50:49 GMT
CMD []
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc53de5761eead687d57c6833225c1b27e8f0fbafb9bde67ecfb7cd0ca0034c`  
		Last Modified: Tue, 13 Sep 2022 13:56:50 GMT  
		Size: 69.4 MB (69357802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371c28164205f4cb5ff1c3f63c3e8091ab05bde41b7cb9333d92eb92d73b7b10`  
		Last Modified: Tue, 13 Sep 2022 13:56:41 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:667692149b0ab73abdd422de941d82dd61b9055e23677bd03d694b76136aee6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108219869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f732a497f9c6b43f1a35f8c7da3cfd0e3d425ce59cdf6a139b3630b529e4179`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 25 Oct 2022 02:22:34 GMT
ADD file:14adaece72e410cf04ac21a101e5b530aab1d5e5a189a2be72d195ec0ac5e6d4 in / 
# Tue, 25 Oct 2022 02:22:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 11:36:20 GMT
ARG PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2
# Tue, 08 Nov 2022 18:38:57 GMT
ARG VARNISH_VERSION=7.2.1
# Tue, 08 Nov 2022 18:38:58 GMT
ARG DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089
# Tue, 08 Nov 2022 18:38:59 GMT
ARG VARNISH_MODULES_VERSION=0.21.0
# Tue, 08 Nov 2022 18:39:00 GMT
ARG VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35
# Tue, 08 Nov 2022 18:39:01 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 08 Nov 2022 18:39:02 GMT
ARG VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597
# Tue, 08 Nov 2022 18:39:03 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5
# Tue, 08 Nov 2022 18:39:04 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Tue, 08 Nov 2022 18:39:05 GMT
ENV VMOD_DEPS=automake curl libtool make pkg-config python3-sphinx
# Tue, 08 Nov 2022 18:39:06 GMT
ENV VARNISH_SIZE=100M
# Tue, 08 Nov 2022 18:41:58 GMT
# ARGS: DIST_SHA512=7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089 PKG_COMMIT=ffc59a345217b599fd49f7f0442b5f653fbe6fc2 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=a442f58968b471d713c99a94e5b80302c07ea163d3d5022d768eb0b39ab081f18744fd529b04283b0c6ec942f362197935d8ef1aa04f26eff10a81425a63bd35 VARNISH_MODULES_VERSION=0.21.0 VARNISH_VERSION=7.2.1 VMOD_DYNAMIC_COMMIT=9666973952f62110c872d720af3dae0b85b4b597 VMOD_DYNAMIC_SHA512SUM=e62f1ee801ab2c9e22f5554bbe40c239257e2c46ea3d2ae19b465b1c82edad6f675417be8f7351d4f9eddafc9ad6c0149f88edc44dd0b922ad82e5d75b6b15a5 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS libgetdns10;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout ffc59a345217b599fd49f7f0442b5f653fbe6fc2;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.2.1.tgz -o $tmpdir/orig.tgz;     echo "7b9b837a8bafdf5798e81bc38163457b3bca16d933a9492800cdd2cde35c9b524a10b7e5ec931217e11d72f32feb05157a7eecfd9cf2c5856e717b634e51d089  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 08 Nov 2022 18:41:59 GMT
WORKDIR /etc/varnish
# Tue, 08 Nov 2022 18:42:00 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 08 Nov 2022 18:42:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 08 Nov 2022 18:42:01 GMT
USER varnish
# Tue, 08 Nov 2022 18:42:02 GMT
EXPOSE 80 8443
# Tue, 08 Nov 2022 18:42:03 GMT
CMD []
```

-	Layers:
	-	`sha256:3c83067056c0f1bc4e162249831ac686f3a9a9c64c5366b903581580de8fcac2`  
		Last Modified: Tue, 25 Oct 2022 02:28:26 GMT  
		Size: 32.4 MB (32396384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b3573e3b9b071bcc3987475972d0a1ad264c4ec0c174a8bdcf886a90aae24b`  
		Last Modified: Tue, 08 Nov 2022 18:47:22 GMT  
		Size: 75.8 MB (75822991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffbb8e4de18e6dccd32bae54f6f0805773126cc6511a673d54387947b3c10b7`  
		Last Modified: Tue, 08 Nov 2022 18:47:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:387cd6794baf021e9362961e2384acbdb25e98fe9a1a394bb6ca859c3c0d3c29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104492792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884a34f4825b0e2e99e750df9c6eb4d44c28ff0a026a3d8932d446f01665b1f3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Sep 2022 02:07:56 GMT
ADD file:8b05dcf5f16a2ae9169b27aa848b812e07cd30414e51e4d53df9a5f01cd4c1a4 in / 
# Tue, 13 Sep 2022 02:07:58 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 10:48:48 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 13 Sep 2022 10:48:48 GMT
ARG VARNISH_VERSION=7.1.1
# Tue, 13 Sep 2022 10:48:48 GMT
ARG DIST_SHA512=7c3c081bd37c63b429337a25ebc0c14d780b0c4fd235d18b9ac1004e0bb2f65e70664c5bd25c5d941deeb6bc078f344fa2629cf0d641a0149fe29dcfa07ffcd2
# Tue, 13 Sep 2022 10:48:49 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 13 Sep 2022 10:48:49 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 13 Sep 2022 10:48:49 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 13 Sep 2022 10:48:50 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Tue, 13 Sep 2022 10:48:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Tue, 13 Sep 2022 10:48:50 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Tue, 13 Sep 2022 10:48:51 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Tue, 13 Sep 2022 10:48:51 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 Sep 2022 10:54:43 GMT
# ARGS: DIST_SHA512=7c3c081bd37c63b429337a25ebc0c14d780b0c4fd235d18b9ac1004e0bb2f65e70664c5bd25c5d941deeb6bc078f344fa2629cf0d641a0149fe29dcfa07ffcd2 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.1 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.1.tgz -o $tmpdir/orig.tgz;     echo "7c3c081bd37c63b429337a25ebc0c14d780b0c4fd235d18b9ac1004e0bb2f65e70664c5bd25c5d941deeb6bc078f344fa2629cf0d641a0149fe29dcfa07ffcd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 13 Sep 2022 10:54:46 GMT
WORKDIR /etc/varnish
# Tue, 13 Sep 2022 10:54:46 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 13 Sep 2022 10:54:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 Sep 2022 10:54:47 GMT
USER varnish
# Tue, 13 Sep 2022 10:54:47 GMT
EXPOSE 80 8443
# Tue, 13 Sep 2022 10:54:48 GMT
CMD []
```

-	Layers:
	-	`sha256:9716ed411387b5ba1ec8278e9fb108a44d8a09ffbbbfd1639f06c63f20364b45`  
		Last Modified: Tue, 13 Sep 2022 02:13:40 GMT  
		Size: 35.3 MB (35277392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4e8423909e32907c374b40534ee89da2efcdb5bb4761bad98dbc593e3aa29e`  
		Last Modified: Tue, 13 Sep 2022 11:06:10 GMT  
		Size: 69.2 MB (69214925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caeee3ea66d867696a8db281c80b7caa089b11024d1e616add57c163aebb4ad8`  
		Last Modified: Tue, 13 Sep 2022 11:05:53 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:94533056a29ed197fe0a3b8d7e3267730a8b9550a81604729665a744362ec716
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85727466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024c8b5a25f9e560b63b1bb14f3a0c93d14354a7ac3b3a849c93566bab34ccd3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Sep 2022 00:48:07 GMT
ADD file:e8a6c2e8be5d9d1f83c1e280419014489438391a9feb7c77b6c21adbf0ec062b in / 
# Tue, 13 Sep 2022 00:48:08 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:42 GMT
ARG PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83
# Tue, 13 Sep 2022 06:53:42 GMT
ARG VARNISH_VERSION=7.1.1
# Tue, 13 Sep 2022 06:53:42 GMT
ARG DIST_SHA512=7c3c081bd37c63b429337a25ebc0c14d780b0c4fd235d18b9ac1004e0bb2f65e70664c5bd25c5d941deeb6bc078f344fa2629cf0d641a0149fe29dcfa07ffcd2
# Tue, 13 Sep 2022 06:53:43 GMT
ARG VARNISH_MODULES_VERSION=0.20.0
# Tue, 13 Sep 2022 06:53:43 GMT
ARG VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36
# Tue, 13 Sep 2022 06:53:43 GMT
ARG VMOD_DYNAMIC_VERSION=2.6.0
# Tue, 13 Sep 2022 06:53:43 GMT
ARG VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a
# Tue, 13 Sep 2022 06:53:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816
# Tue, 13 Sep 2022 06:53:43 GMT
ARG TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04
# Tue, 13 Sep 2022 06:53:43 GMT
ENV VMOD_DEPS=automake curl gcc libtool make pkg-config python3-sphinx
# Tue, 13 Sep 2022 06:53:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 Sep 2022 06:56:13 GMT
# ARGS: DIST_SHA512=7c3c081bd37c63b429337a25ebc0c14d780b0c4fd235d18b9ac1004e0bb2f65e70664c5bd25c5d941deeb6bc078f344fa2629cf0d641a0149fe29dcfa07ffcd2 PKG_COMMIT=3ba24a8eee8cc5c082714034145b907402bbdb83 TOOLBOX_COMMIT=96bab07cf58b6e04824ffec608199f1780ff0d04 VARNISH_MODULES_SHA512SUM=e63d6da8f63a5ce56bc7a5a1dd1a908e4ab0f6a36b5bdc5709dca2aa9c0b474bd8a06491ed3dee23636d335241ced4c7ef017b57413b05792ad382f6306a0b36 VARNISH_MODULES_VERSION=0.20.0 VARNISH_VERSION=7.1.1 VMOD_DYNAMIC_COMMIT=025e9918f6cba33135e16e0fb0d86b4c34b6dd5a VMOD_DYNAMIC_SHA512SUM=89b7251529c4c63c408b83c59e32b54b94b0f31f83614a34b3ffc4fb96ebdac5b6f8b5fe5b95056d5952a3c0a0217c935c5073c38415f7680af748e58c041816 VMOD_DYNAMIC_VERSION=2.6.0
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot sbuild";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y $BASE_PKGS;     cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 3ba24a8eee8cc5c082714034145b907402bbdb83;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-7.1.1.tgz -o $tmpdir/orig.tgz;     echo "7c3c081bd37c63b429337a25ebc0c14d780b0c4fd235d18b9ac1004e0bb2f65e70664c5bd25c5d941deeb6bc078f344fa2629cf0d641a0149fe29dcfa07ffcd2  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;
# Tue, 13 Sep 2022 06:56:15 GMT
WORKDIR /etc/varnish
# Tue, 13 Sep 2022 06:56:15 GMT
COPY dir:846b8f8975487ee292d565d7ea945a1a79fb5f0e418fec900574091bb0a7cffc in /usr/local/bin/ 
# Tue, 13 Sep 2022 06:56:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 Sep 2022 06:56:16 GMT
USER varnish
# Tue, 13 Sep 2022 06:56:16 GMT
EXPOSE 80 8443
# Tue, 13 Sep 2022 06:56:16 GMT
CMD []
```

-	Layers:
	-	`sha256:c64715e5ebd39975a39b5cf2535772544c27713cbed678b0a21e73680fffaf72`  
		Last Modified: Tue, 13 Sep 2022 00:52:39 GMT  
		Size: 29.6 MB (29635080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04976f863b25f9dbf72873d6cdbccf813a5d2db0ca7818d68284fc6d588ed2ac`  
		Last Modified: Tue, 13 Sep 2022 07:00:20 GMT  
		Size: 56.1 MB (56091911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dcdef6310d5d684296de769c6877cf4dbf99739f5b1af7dfe9555972fef90a`  
		Last Modified: Tue, 13 Sep 2022 07:00:13 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
