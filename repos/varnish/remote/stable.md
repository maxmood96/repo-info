## `varnish:stable`

```console
$ docker pull varnish@sha256:5b1d9eec715ce8cec54825b7fdf2d8e4629bfeca8bd2544ed49fc460a3050351
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

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:edbcf0cd549f53684fc336b974b1c3fe89cb9a2af5a5a2f136777a226581e3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103549394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69a36386db13b384d7adf8030bd4311732d4338a012187246d7fe640abcef87`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021bd6671d3c11349807a74fa9eed35c5ab7ae0b1861bdbad9e0c1f3bb0836c5`  
		Last Modified: Tue, 30 Sep 2025 21:32:34 GMT  
		Size: 75.3 MB (75320304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283d977df10b07fad39caa773e480b85b2316bb0210df4529286f9e3f64071df`  
		Last Modified: Tue, 30 Sep 2025 20:32:52 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:fdaad8c93b08a3788a9b33f4ad7ea9f826c4629f41078677b7d301d48a4a63d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db71b02b550e84775078b00b1c320ba9a498e132b71f30dea306cc2e8262af21`

```dockerfile
```

-	Layers:
	-	`sha256:fa7091d13984269be7930011aabfc70e936efb08c9c46386147647138e188614`  
		Last Modified: Tue, 30 Sep 2025 21:32:14 GMT  
		Size: 12.7 KB (12692 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:83d0eb092587fb5442cfdbd0359adf6882ca26c5fa9e5957c2aa9997f7bf8fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75967394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca5d3d8e50e1364c4b1de38f7a093ed938e5b162b5c7c87a5651993f42ca6c7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a96e3e9f59bc14457ad942b973f0d57ab12afaff6dc14cb34cb73d85b3ffd4`  
		Last Modified: Mon, 08 Sep 2025 22:49:28 GMT  
		Size: 52.0 MB (52032733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2319aebd117135eff4658d33b156b6b2a9d49f00ad83a96a75352f08061c664`  
		Last Modified: Mon, 08 Sep 2025 22:39:51 GMT  
		Size: 725.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:761cb4d694b8df422a48c010a217c18afca4cb7b51be9d4573e99562c98d080e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dd6497965803a8eda5b5e176c760ebf0c549a405b5127e071dd297beff09b2`

```dockerfile
```

-	Layers:
	-	`sha256:533d2079eacc98d46a2c79d10c8af512dcc0ffb6699d73c883e1b7b2bd750c9a`  
		Last Modified: Tue, 09 Sep 2025 00:19:29 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:a2aac0559b353cb60b49686e387cc2369c4fe84952783f965980c226fdc77207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98404617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda087f571e171269283c9c4e691e2a8d665240031fbd46506953c181f299498`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1a9b5f2ef0a48e29a325995aaa014a02ee8e27a2d6b6c7f1eae706c5e6e5a4`  
		Last Modified: Tue, 30 Sep 2025 00:15:26 GMT  
		Size: 70.3 MB (70301719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62acb4a8b52242bb4d121dca852e3cdee447dd87cddb494c3ec202454bdee7a`  
		Last Modified: Tue, 30 Sep 2025 00:15:08 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:94e57ecd1d41808eb3bc924d4c61c2571da38d126a5a21a235927117d40e3f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5269aab6856b2cce907b5896eedda8a0baf058f610e832b67fdf302adc2f2b17`

```dockerfile
```

-	Layers:
	-	`sha256:fb18672428481ccd161b086f4a89f40e1684dbc5a7129fa72cca8c9981cdc789`  
		Last Modified: Tue, 30 Sep 2025 12:19:44 GMT  
		Size: 12.8 KB (12784 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:770c31fec1c0d1e8bb18b3f73130aa7d7b9cedbd371f68718c46015db8093d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101009937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7369af1ac997223f89a186307d3cf0ad66d6c7483d96e030e3d2bf70e54178d5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac062943d6dbf85d9967efb33f240d7174233498ecefeae11fc3e752e4b701a6`  
		Last Modified: Tue, 30 Sep 2025 15:11:14 GMT  
		Size: 71.8 MB (71799554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acb1e036848264770a871e40dbc8f57b501eaa6a3973e6d6002bd0469ae1eac`  
		Last Modified: Tue, 30 Sep 2025 01:11:00 GMT  
		Size: 721.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:0540529c49b2c9cf0341f115c4e4de158e14ccd3eeb46eecf643fcd720a151c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612d547d40a94907dee9f043de061252f518a847f289ed29eea07e8b3e42a9f5`

```dockerfile
```

-	Layers:
	-	`sha256:284ab7a9bc5e80ab20f48608dfda7f7e25be01c46c4bd04faa1880a3d4647191`  
		Last Modified: Tue, 30 Sep 2025 15:21:15 GMT  
		Size: 12.7 KB (12666 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:cda3f84a524ce26496944326d0fa01b70d036a03b5ebd533158d74dc771b5ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105448760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0ebeaf1ed77e48a4d1cb9ebfbec5334b02381b14c832f80f7ae2620a39e90c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc374f61690bfbde05777b216808ef4ca55da9b385772d1e11c2582cce8eea1`  
		Last Modified: Tue, 09 Sep 2025 03:19:41 GMT  
		Size: 73.4 MB (73379243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fb0210a0c4003e5d22dcdff1d2f4adacc7333b8cc018962cd478e2c4cb4f25`  
		Last Modified: Tue, 09 Sep 2025 02:16:19 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:95b564b7811b2f0940e19273c3edbbcba8d048ad314ab12e20cf69838b5b29e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8848e40fc40a9cbda6e721d532704562057c11768aeb759a7461dc43e80eabd7`

```dockerfile
```

-	Layers:
	-	`sha256:413e97a38d767932bdc61c06dfeca8574b71e5e3e907123b2318bf18298d3ae1`  
		Last Modified: Tue, 09 Sep 2025 03:19:28 GMT  
		Size: 12.7 KB (12731 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:dd816940571162d6ee1e989f9c9952bae13cf153bcea3e5e5fa9654f6d81d3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81335071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e39171b878b614da5e82f45d179d7fde3eb76ff4017254c2e737115caa4513f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 26 Aug 2025 14:45:42 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Tue, 26 Aug 2025 14:45:42 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 26 Aug 2025 14:45:42 GMT
ARG VARNISH_VERSION=6.0.16
# Tue, 26 Aug 2025 14:45:42 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Tue, 26 Aug 2025 14:45:42 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 14:45:42 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 14:45:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 14:45:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 14:45:42 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 14:45:42 GMT
CMD []
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e5a4571b8763222bc9df6252308856a003d945316511f14da7b7c397cbbcfa`  
		Last Modified: Wed, 01 Oct 2025 00:30:47 GMT  
		Size: 54.4 MB (54449997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d87403c37cdba5b295b8dd02cb3c9a68249c1ca86a8658955712801fc9edd1`  
		Last Modified: Tue, 30 Sep 2025 03:57:19 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:67fbf88ebd64cd482b3ba39fb4aa2617c9d8e90112d0a7220dc93a23b0ca31d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382986cfda5f76f4c8b9ff355bf4142f88e49fc7f32b7e0462c284caae2ca060`

```dockerfile
```

-	Layers:
	-	`sha256:7c98189558027159262d622199a4fa7eed6df5488f9ea32417c53665e9081ff5`  
		Last Modified: Wed, 01 Oct 2025 00:30:26 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json
