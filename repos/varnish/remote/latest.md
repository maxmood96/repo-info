## `varnish:latest`

```console
$ docker pull varnish@sha256:62be997c135df33d10b9ca49cb599fbd836c5d8a3f96e2f8a2567db705f12e84
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

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:c97e31abb26c2a4bc80a60d0ca080f1e3a18e31ace60dbbaf4037ba29f9f3d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116466266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004bda53957dbb10230c7308b9596abf362bd6a0699bffa29463a7799274c2da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 16 Sep 2025 23:33:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefe861ac020fae87c9b3ce06a9bb9d050070b059d6c2a12c4ab7c81af27f4b2`  
		Last Modified: Tue, 30 Sep 2025 00:12:21 GMT  
		Size: 86.7 MB (86686458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998a2eafd8f6a49966509e8c6c54adeada7389ecb2bf14d232209ec99d6b78d7`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095bb281dc5a0973162db00f0de12ba6ac3f347e5c674d0a31052e2959ff96bf`  
		Last Modified: Tue, 30 Sep 2025 00:12:08 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:3968cd90f6dd9784b74ecd501fe63144337ecb3e3abdee2961ac95dc51fbf32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc82998fc1361929d6bd83b06965600e1bbdb0ff26200bdbab4a7850b941cca`

```dockerfile
```

-	Layers:
	-	`sha256:5ee38ca58b7551f252813868294b3e7bcf0cfa381fbe5256c7db0837747640f1`  
		Last Modified: Tue, 30 Sep 2025 21:32:26 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm variant v7

```console
$ docker pull varnish@sha256:063bfa59da18ebde7556850d2dd042faa80634d0c47c935c2cb9b5d64ed00782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87280727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c072bf4299e6aa4c5e571e09c7b1d469b54e8e6b6c2793d7c11b0825ea5751`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e026a2a65e9fa1cc228e59ba8c3ffbb23910fad5f080e6c175a700b483e60dae`  
		Last Modified: Tue, 16 Sep 2025 23:49:01 GMT  
		Size: 61.1 MB (61070835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9457b94e6a98f5a4404415fd9bb3496f25efbe22281e35e3bcd260bd0abfbf23`  
		Last Modified: Tue, 16 Sep 2025 23:48:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1904e3b9049e444d9afbd30608facf698c450abeab7dde6e1e723d06af61e71`  
		Last Modified: Tue, 16 Sep 2025 23:48:58 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:64edf2d4410ceb089e1baa1396d3e5d456751b0d3b4302077896d04f12a047f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85d7307c16cef587dc5c8f2ffe4f68e8299c2ed70b19f6770b605cda3d93972`

```dockerfile
```

-	Layers:
	-	`sha256:5dc3ca1c412aec1bf4c2684579ac0b165b712da2e6013dfc44a3232432537814`  
		Last Modified: Wed, 17 Sep 2025 00:19:41 GMT  
		Size: 19.7 KB (19681 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:73fe11222aca50a04268d31a887a1b7af868ae566401389f7dff44dfaabe4214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110649907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bba517d5adc51fa65d82ae98780532506c3dbadfb7a2f715d6788b3fdb7bfb0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e059c99dc2a0d0bf9e8d7594f9570dbb04201809d082d502ce2f418148703e8`  
		Last Modified: Tue, 16 Sep 2025 23:49:05 GMT  
		Size: 80.5 MB (80511231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207fdaf25d451b02d3f53eaf70cd42e5842ee1cc7c1d21e68de6dc6df29420c4`  
		Last Modified: Tue, 16 Sep 2025 23:48:48 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aacf596b97ca8cac4a574716332a01310fa9254f2978e0e0347a9d8022089e0`  
		Last Modified: Tue, 16 Sep 2025 23:48:48 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:fa73f3c17235dfe855a62a80028df70bb5d24e797210dee8377290b875ffc3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27409bdc5c9e070c186297d09edcbae5d6df1038d109cdbed76372317c318df9`

```dockerfile
```

-	Layers:
	-	`sha256:92f07d12babd1e201db985ec952d5ed63aedbf584fa1889698d4f25bfcf88c33`  
		Last Modified: Wed, 17 Sep 2025 00:19:44 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; 386

```console
$ docker pull varnish@sha256:e3856adc931fc6a28ddc25bc28e8445d68cf2c6ad4f23805e8d19eec1ea2c3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114618760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be701b669e9a2c4bf445335cc079c823b52b7545f5d6cb37b02a45211dc7b75`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96166455d32d943fbcecdba756986eb926e6a0fc11c34511c00d592762e00e71`  
		Last Modified: Tue, 16 Sep 2025 23:49:01 GMT  
		Size: 83.3 MB (83326931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1d206557279d39707fe934e71b7a7ca60759eed39a399831b9dbda82db34b7`  
		Last Modified: Tue, 16 Sep 2025 23:48:53 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c781e1094d98e5b0328e7520b4368e1956edc52c0bc6897d974828ddece1c4`  
		Last Modified: Tue, 16 Sep 2025 23:48:53 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:ed5de1977f4b38793d61e4de38852702d4f8373d3cef512a04fcaa9f30e19568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80715895144083c5434fb77a6c5f9daeecb25f14e61914b9b120ce1239f2d885`

```dockerfile
```

-	Layers:
	-	`sha256:d0f0c3b255b54ddbef74debeac45e7dbf3ead2dce9e5341ef9b3a8b21353f3be`  
		Last Modified: Wed, 17 Sep 2025 00:19:47 GMT  
		Size: 19.6 KB (19557 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; ppc64le

```console
$ docker pull varnish@sha256:65d4d016a355ede87506f11461bbeefcc7b3b9389c548f3a7034b6e3590a4510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111919411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bedfe585af5eff0eacaa576302b11abbbf86751723b4b06f0c53b4aa4b4238`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824991404ea7867a21a0879743ff7ccf095181ef538d252718104ab835946224`  
		Last Modified: Tue, 16 Sep 2025 23:56:02 GMT  
		Size: 78.3 MB (78323010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7393ce7cc69e43d87d032cb9d19b2f59a812a549e8d41f195d8bb4850e9c0d5`  
		Last Modified: Tue, 16 Sep 2025 23:55:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fed50c46d757203916dc966bb9a30ef6f6c3c0de2dee80d55a82870a293977`  
		Last Modified: Tue, 16 Sep 2025 23:55:55 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:0324eba5840c59482bf85c6fef3d2bc8eb89f5ea2002109bea43b8f0db82d4e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5378d005b70977315ce21055d85737f6837c43e8de9abffe6c9f96246e8bbddc`

```dockerfile
```

-	Layers:
	-	`sha256:55a48f40bdde1848b1ba475584fb503b2ad7a83a94186f63ab0c8a18529a4268`  
		Last Modified: Wed, 17 Sep 2025 00:19:51 GMT  
		Size: 19.6 KB (19644 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; s390x

```console
$ docker pull varnish@sha256:f4013b78e00ac31203fcd12d85aa0dfae1f5c670235c602948d655fb6c97f6dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93420608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef63697e145dce6624cd5d018317324e1aabb899ac5a5d73ea6a9a8bea85f21a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Tue, 16 Sep 2025 23:33:29 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_VERSION=8.0.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 16 Sep 2025 23:33:29 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 16 Sep 2025 23:33:29 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VARNISH_SIZE=100M
# Tue, 16 Sep 2025 23:33:29 GMT
ENV VSM_NOPID=1
# Tue, 16 Sep 2025 23:33:29 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot libgetdns-dev";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     mkdir -p /work/varnish /pkgs;     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS adduser libgetdns10t64 netbase;         adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         cd /work/varnish;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout $PKG_COMMIT;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     mv ../*dev*.deb /pkgs;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apt-mark hold varnish;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /work/ /usr/lib/varnish/vmods/libvmod_*.la;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
WORKDIR /etc/varnish
# Tue, 16 Sep 2025 23:33:29 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 16 Sep 2025 23:33:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 16 Sep 2025 23:33:29 GMT
USER varnish
# Tue, 16 Sep 2025 23:33:29 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 16 Sep 2025 23:33:29 GMT
CMD []
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd855b64576b66ab24943ed3775f49ac0b3ea420829fa32266838c87f74bea45`  
		Last Modified: Tue, 16 Sep 2025 23:48:42 GMT  
		Size: 63.6 MB (63585658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f476737a312af81574abec8edd9f01831dd7e11a3e4dbff61c0f54e342869a09`  
		Last Modified: Tue, 16 Sep 2025 23:48:34 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714ac4bf12ec9b7feadbdf85220f7a4a8df200aff798c72a4f6446b8fe784c3a`  
		Last Modified: Tue, 16 Sep 2025 23:48:34 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:96f637f9a46220e5cfb9fa91797b9c5debf776151f18eb612b7c3c453416f025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d797680456b78a67e2c1ea9fdbd1f48ef807575448f21bbf8a2e07f7a68dbae`

```dockerfile
```

-	Layers:
	-	`sha256:f1d4fefb15f21987ecb1f0ae2c6a123ffec8a29831381c8d8a819c54a6897155`  
		Last Modified: Wed, 17 Sep 2025 00:19:54 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json
