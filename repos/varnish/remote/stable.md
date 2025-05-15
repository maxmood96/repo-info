## `varnish:stable`

```console
$ docker pull varnish@sha256:868fb40f8f2146aa746a330e1cdd7dfc97a99bcc03460feb10750159c9872445
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
$ docker pull varnish@sha256:66bdc6469d0d61f2b355c849f35c4c2f2f8ebf80d046b22f30368fc456c0e29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127751801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6218ac31f8051cfabf6efe690a3505c95c87c9710d386dbb2836eb85b413a3ff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a07b08b0f89755e76c50dfbbaf61079d65bea9a9d5c38f0cb4859b55d62d4f`  
		Last Modified: Tue, 13 May 2025 23:47:53 GMT  
		Size: 99.5 MB (99523403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43955ffb5f4280a0c57b3302d076f3a87a85f81a8f040e27afad2988f3075f09`  
		Last Modified: Tue, 13 May 2025 23:47:51 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:463dfeabc3c4d2a02d09ce73e56dda5e09b0c28c233d5fdaba61373fc5a9bc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218637f9e1fa5e00b79f187d32b62b0d413edfbeaf79e37b3bcdb9799528d4d7`

```dockerfile
```

-	Layers:
	-	`sha256:299d041706a61a5bf715815a2ec0c22d9a9a041aa86f7b73980a650a223f375a`  
		Last Modified: Tue, 13 May 2025 23:47:51 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:7f96db009b0666538ae164aeb5cdbe64033d267fbc006ab265eff09a72c27e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98301122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621050906300e858484a6dd4231164ce57655d7ee893d70dee91f360c40e65ad`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c83ffdb2996fd1ae71febab56e2d2b25994fea29e5d877eee7f40d82da34a73`  
		Last Modified: Tue, 13 May 2025 23:56:44 GMT  
		Size: 74.4 MB (74362294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0bef30fd770d593f576d5b924997130cfc8e352c3a5faa47ed69b321831d88`  
		Last Modified: Tue, 13 May 2025 23:56:41 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:77776b658734f4655f6aacd7dc896728e2ca22f45d26866fba053d728039d915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc5f2771889fe96fa2a51021fffdc3d02a16d67e94030e6428eec3f3d3d4ab9`

```dockerfile
```

-	Layers:
	-	`sha256:23578b6aa6cfc04957eee0b62ee6a08ec716fc223f84f5f2bb2ba33d60c3dc98`  
		Last Modified: Tue, 13 May 2025 23:56:41 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:31c226d0e1da086bbb14e4a8a60cc9ccd7c01a4a2cf8b2c6ee3e6bd4262341bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122368914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139811ae510fad3a9e8144604e9d7771bfa586ef2ffe362092797e70e55466f9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5508cfcb77ac7f17fc088f0f0e52579241730d1d650f04332a5acb49e7aef427`  
		Last Modified: Tue, 13 May 2025 23:55:42 GMT  
		Size: 94.3 MB (94301537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65b2634581085261d26bd2238962df0010003010557cea4bcedf086645a81d0`  
		Last Modified: Tue, 13 May 2025 23:55:39 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:8b6c9c65e14771bcdbd53f061f404a2699d042844b00144fc9d95dd9a4e57797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c83280f2bf9797d435757456f17ec4d9a533af1efaa7ea503d333a578f36e8`

```dockerfile
```

-	Layers:
	-	`sha256:ae4402b0587fc9b35ac330e0b5f0cfba3fa250c3a9d9d815593467851f1f5953`  
		Last Modified: Tue, 13 May 2025 23:55:39 GMT  
		Size: 12.8 KB (12757 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:26d8e467c18988751c97e240a61f52521addaf5dfd810db7bb266236fa33f8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124908238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68e553cc4fd48c3da7473a29fe8067adc172029a1918bba1a24f9a1e937b8ed`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Thu, 08 May 2025 17:08:57 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7060f02e2aa9a584ce329eab0127d728d2f492b7efe47b1092adcf0ae0ed7c33`  
		Last Modified: Tue, 13 May 2025 23:48:02 GMT  
		Size: 95.7 MB (95696616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d3781afbad69eefcf42238c1dfa70e6321c80bde89662bd9e95cc1ed54d37c`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 724.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:13fdc49ed43cc6409ebf5bf0d4c5b8c244c4d2f26bd2e9d2a2398cc0fb66513d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 KB (12636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed80704c6e2c4a4b282f80e85515f0726514956b9422dd61ebde5b5fe4e94d01`

```dockerfile
```

-	Layers:
	-	`sha256:450e45ba03f9bdb4b1d3719ce3df477b164c70dd6e9c6935f3b51d4c8f1dc7a9`  
		Last Modified: Tue, 13 May 2025 23:47:59 GMT  
		Size: 12.6 KB (12636 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:34447fca426a5d5fe08b9f8e9a1ecde2c4ec456200349bd81af272776473daf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130417116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a33d29837032baae03a73cdef6f3cdeebf2b023e209d1362ba70d2feb8ab45e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Thu, 08 May 2025 17:09:00 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073ddc7fd38cef02cc6c6fc6a5fc5c32d3b3b93dff5dd6e58a4ae35db96d93eb`  
		Last Modified: Wed, 14 May 2025 00:05:05 GMT  
		Size: 98.3 MB (98347918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31a65db2dd65a79300357dbea9a209652f91fdaeabd0861156cbb96fb53bd81`  
		Last Modified: Wed, 14 May 2025 00:05:02 GMT  
		Size: 723.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:b73ca8ea1d6d380fba641683fcc179d9ad1a94b69ba76e2051d50aeae0318bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fb8cec5bb9a7fa54d8fdb676a975e2740ccf004d4601bafb4bbf5bcb239a26`

```dockerfile
```

-	Layers:
	-	`sha256:c6bf3f06141a8df1e36083cb4dd00321da8372b285a3647953a8dfcfcf75fa78`  
		Last Modified: Wed, 14 May 2025 00:05:02 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:09a0dbbee17f636c0c0b9093399608278800fa8e1ed19c31e2666eef6a5ff9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105646551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7621b78da40966c8501bcb704e28029fab38204fad7b79b9f5099e674e45e58d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 22:18:23 GMT
ARG PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b
# Tue, 13 May 2025 22:18:23 GMT
ARG VARNISH_VERSION=6.0.14
# Tue, 13 May 2025 22:18:23 GMT
ARG DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
# Tue, 13 May 2025 22:18:23 GMT
ENV VARNISH_SIZE=100M
# Tue, 13 May 2025 22:18:23 GMT
# ARGS: PKG_COMMIT=10da6a585eb7d8defe9d273a51df5b133500eb6b VARNISH_VERSION=6.0.14 DIST_SHA512=60c51ef71f8da11cdc862c257b6ce3970501af3ffc20199a6230f93f092657e2a5ddc37994acc25acc4ce2e50e1f4c69606aa0c92cb5d546e4f4244cfc473e91
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y --no-install-recommends $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout "$PKG_COMMIT";     rm -rf .git;     curl -f "https://varnish-cache.org/downloads/varnish-$VARNISH_VERSION.tgz" -o $tmpdir/orig.tgz;     echo "$DIST_SHA512  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|$VARNISH_VERSION|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y --no-install-recommends install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir"; # buildkit
# Tue, 13 May 2025 22:18:23 GMT
WORKDIR /etc/varnish
# Tue, 13 May 2025 22:18:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 13 May 2025 22:18:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 13 May 2025 22:18:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 13 May 2025 22:18:23 GMT
CMD []
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db18e1950ca47b8e9fce1f44435ffcedc2f0a789a648f41801efc1d97fda81a`  
		Last Modified: Tue, 13 May 2025 23:58:14 GMT  
		Size: 78.8 MB (78760930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e14d69023dc6c7ba0d87a0a1354e9f2dd77b313fd6dc0abaf63e753195def1d`  
		Last Modified: Tue, 13 May 2025 23:58:12 GMT  
		Size: 722.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:stable` - unknown; unknown

```console
$ docker pull varnish@sha256:ba3f2584bbc08a5ce7008a5132a81c4894044e989b0095c4d2e25d36df4fbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a31d7f2c49f555233725c42ad9d603c4980870c356e30693c5027911f32ff0c`

```dockerfile
```

-	Layers:
	-	`sha256:101edce10cd755c6bc713a14125c6358a1f4473aa2459de1fa89a3b72f27ceac`  
		Last Modified: Tue, 13 May 2025 23:58:12 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json
