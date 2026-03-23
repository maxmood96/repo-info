## `varnish:stable`

```console
$ docker pull varnish@sha256:855d6c2d3b99ab239649829f016c29217dc4fcb7e0372a2555e236036eae5195
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:b0bb5130c045e4ed88893eeafbf6d8b1197d781605ae4f63a133c222bc95c838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103557925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c35d1f27f7233f4fa8eb5363593054e9aebb08d4e0587cac875afbaed15269`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:30 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 16 Mar 2026 22:38:30 GMT
ARG VARNISH_VERSION=6.0.16
# Mon, 16 Mar 2026 22:38:30 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Mon, 16 Mar 2026 22:38:30 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:38:30 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Mon, 16 Mar 2026 22:38:30 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:38:30 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:38:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:38:30 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:38:30 GMT
CMD []
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055a1df36dfed0fadbdc059ee421ee1ad6c7bf9251a1b2cc008471f8cfdf2654`  
		Last Modified: Mon, 16 Mar 2026 22:38:43 GMT  
		Size: 75.3 MB (75320945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee086c1915b7ed773532f3663341b2516d4cd1536daa434e814d08de2e61e7d`  
		Last Modified: Mon, 16 Mar 2026 22:38:41 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:9c96c92c25e84a14aa7c692bb557dd5f8809232fbd53b8e6490dc84b297becda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bdea2d2df2acb0efb583d102c2397b99556c9e7d0a3fd4205afc84c506430f`

```dockerfile
```

-	Layers:
	-	`sha256:00c2684bd4a8ab21306e221c438454b5d1290401d35d44f5654616b77c61fc3e`  
		Last Modified: Mon, 16 Mar 2026 22:38:41 GMT  
		Size: 12.7 KB (12657 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:0e0dd63b700b869e0d8fe8394a36082bbd43d587b1057f6d51e8397177a2bc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98416395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e62fbb2a951812f6565857d87cbac71a2ba90d6d6efb99f5a486edd6caab06`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Mon, 16 Mar 2026 22:40:36 GMT
ARG VARNISH_VERSION=6.0.16
# Mon, 16 Mar 2026 22:40:36 GMT
ARG DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
# Mon, 16 Mar 2026 22:40:36 GMT
ENV VARNISH_SIZE=100M
# Mon, 16 Mar 2026 22:40:36 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.16 DIST_SHA512=40bccbb024b7909af606220510efe68f6d1009cd678df1950ab6c1d16a0f12fb3cdb812f658825c45d071e1c5afc2561f8b56645da4bc396f5d20e27ed8bd0e2
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -L -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS varnish-dev;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Mon, 16 Mar 2026 22:40:36 GMT
WORKDIR /etc/varnish
# Mon, 16 Mar 2026 22:40:36 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:40:36 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 16 Mar 2026 22:40:36 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 16 Mar 2026 22:40:36 GMT
CMD []
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9d9907a53af5e00389e3eea54067d788145e7262bfa2582c47732b88600d50`  
		Last Modified: Mon, 16 Mar 2026 22:40:48 GMT  
		Size: 70.3 MB (70299576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6364eaea38f3f8be3bdb617f0a30b07b010d54213da9dff418bb7bd58f61215f`  
		Last Modified: Mon, 16 Mar 2026 22:40:46 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:76c67dc1e6b208fa6137cd91e0bd7a9d5913f85f5be2de3c148b277635b8479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6531325a26c3ec3b38e2b802d80ce7b5ab97311749cb9fbb84a6c535e984dd`

```dockerfile
```

-	Layers:
	-	`sha256:1ff656a98056e74c66c6382c20a86fa0b66bd4cddb489c765be5e878aa2c4f9a`  
		Last Modified: Mon, 16 Mar 2026 22:40:46 GMT  
		Size: 12.7 KB (12749 bytes)  
		MIME: application/vnd.in-toto+json
