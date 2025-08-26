## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:eb21e9f988be93f33ff9a0025d0a00617d49f3cc0cf59e0f2167bde7724eae6a
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

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:eb59c7c733b51c1b939cbf9ff520c263bc0c9299508d387e2c19d9df44ca052e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82842456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ba779d3e802e8d23096c4540664cc96d8536959d5b074aa304623851eb7b6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d21ba25e42c221c38da4178d142633a0f4b5df2ea8c3f3d106f42d0b10b443`  
		Last Modified: Tue, 26 Aug 2025 16:51:04 GMT  
		Size: 79.0 MB (79040710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da539f12306b86eb6f4852b5fc70b75a09cef49e31798ad611f63cc267c02be4`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4cd983d1fb0f0789a1a89e664b291a4a4661ccc517311755de1f6948133737`  
		Last Modified: Tue, 26 Aug 2025 16:50:56 GMT  
		Size: 1.5 KB (1522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:cca42d774f271c82579cabffc4db3bfc1035ac3771304e71f720aec531157efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b7b3c041668a547dc1bbb7950733445e113d810c45c9270e7a06ec1477f0bb`

```dockerfile
```

-	Layers:
	-	`sha256:352b25a10911cee1af8da5fbe36f12ae99a4566e98353faca1c19a1dba719b8a`  
		Last Modified: Tue, 26 Aug 2025 18:20:34 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:a45549c23c64999161d2144378f8972638bb135b9ae2a82f7a9c677827bf5ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64309206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2054d8cf53e95e19697765491d67a689b3bf8bbd4c17141d0793f38d883f13`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df002cf37151e7b0fa6b77dce491cac03f0f43e0787475b1164effafe412756`  
		Last Modified: Tue, 26 Aug 2025 16:52:10 GMT  
		Size: 61.1 MB (61088108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8f13ade0c407bc30c2d0943af75f6686574b0f26d379104e3c205bf45afc9a`  
		Last Modified: Tue, 26 Aug 2025 16:52:04 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1122e1df195890d89e2ce223091d4fdbf016c09a99097ad0d2800e51f1c1b614`  
		Last Modified: Tue, 26 Aug 2025 16:52:08 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:e2ab0e3e19ebf7c6ca62c6b44d5ebcf558dae64f334ad28c878643af087cdd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cf4ba26c47448e64139df64da0a0b9fe67159038b3408e9b09817f12aeef0e`

```dockerfile
```

-	Layers:
	-	`sha256:ce92da7aee86b3186c4df792b992aad5793b0bd68a2cf58e2c87edf2d1ca25c1`  
		Last Modified: Tue, 26 Aug 2025 18:20:39 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:cc7a4c790e15bf6bf5226b0d410417ec9f531d5a753110a66b5ab276c31d529f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80124371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcffa3fc8649cd6ecd6bf2901185697844222260efa02f05e99731db0afe6372`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61af1543a395f4ec8e503d693e122083a940bf2bb76d515063e5143006014daf`  
		Last Modified: Tue, 26 Aug 2025 18:21:12 GMT  
		Size: 76.0 MB (75991566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12d13ffdec5777bc9a087e7b6a7648c20098407baf88c27c9e7fe4aac7d8762`  
		Last Modified: Tue, 26 Aug 2025 17:10:48 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829db24f940156af11f84479793cc2a0a0cfe14343815b44983b6afde47268a1`  
		Last Modified: Tue, 26 Aug 2025 17:10:51 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:0ccbeff7dbfb12f5d18c9f0cd5717acfb9ad1edf5aa9e6b00ad5b3b40c42d048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb6f4dd4f15da4e733fba7d1e89c9f575efa966c077245df747443c718e3f9`

```dockerfile
```

-	Layers:
	-	`sha256:2a51627e99e6e144059176acd8432da0742e66b7680ad3e45c9b5b7b842abd83`  
		Last Modified: Tue, 26 Aug 2025 18:20:42 GMT  
		Size: 18.9 KB (18910 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; 386

```console
$ docker pull varnish@sha256:79de57822067c316205cf516f35730d9a48eba17a18438068b7f040a24ac3b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84867078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5504cbcd55267abd7eb20a78d9b5a7b750049aa4bc605904f43a56800e28e91b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8566fc257dd8fe62b706fceeac74d505c8d4f452f47443ab24c056b45d36a39`  
		Last Modified: Tue, 26 Aug 2025 16:51:00 GMT  
		Size: 81.3 MB (81250013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c902672d8239c81bbf78276bf948224102a95c14aa1c3425a2cd8d61ac8e72`  
		Last Modified: Tue, 26 Aug 2025 16:50:52 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b659f1d057b1bc172c204ef2be2e113d569f720ff55a3eede5412aa84a492b`  
		Last Modified: Tue, 26 Aug 2025 16:50:53 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:18c78749465acc21014ef75082ab645316c03195ac2240e39400c554dc25c080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745deeff47c188553c23284121381997db93b89c2f4f6a3ef25a5fde1cd3a4cc`

```dockerfile
```

-	Layers:
	-	`sha256:a0fa618125b27a4ad09d1553205573bf7cc3d05fe296ae1a5916418c2bef17b2`  
		Last Modified: Tue, 26 Aug 2025 18:20:46 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:edff5c8cf592568cd0c8a1791adb5a4c7038630e2396a74f30fbc286cc02d57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78817937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4e4f81bdc94adfb2b152c4986a786099e213c8872a0a447de1940eec8b36b9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41580bfa7bb549e94995896f5201eb9cea1494505ab84bd2126449b3a80d8788`  
		Last Modified: Tue, 26 Aug 2025 17:05:11 GMT  
		Size: 75.1 MB (75088762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf19c428ddd5472d5705df46e95a523161488ca0d2e70ca9bebd0089f1c233e`  
		Last Modified: Tue, 26 Aug 2025 17:05:02 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf0cd2ebebd5e2b3680f333eeeea9e24af8c1deab3442ac0419289d59b88528`  
		Last Modified: Tue, 26 Aug 2025 17:05:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:a97e2c5ce5f5ae8715cfb5aa54bd600ceda8d156a4d95fe1b69ffe7160544d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd36779ff7171b497584aecf1336f80b2271cbe770dfffecab9b37499691c10d`

```dockerfile
```

-	Layers:
	-	`sha256:4e868d107d4ec0f88f2515d8c0e461129f2d4c2412b6465284b4d66c9941ba81`  
		Last Modified: Tue, 26 Aug 2025 18:20:49 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:6bc7c34f4a8c82a84964269ceb7da23eadc1bfbc06e1dd164456a4a7c5a8f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73373120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7df50cfa2eacca4e44264105844791df8f7c91eb09af124a198445860554b81`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 15:45:37 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_VERSION=7.6.5
# Tue, 26 Aug 2025 15:45:37 GMT
ARG DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 26 Aug 2025 15:45:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 26 Aug 2025 15:45:37 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VARNISH_SIZE=100M
# Tue, 26 Aug 2025 15:45:37 GMT
ENV VSM_NOPID=1
# Tue, 26 Aug 2025 15:45:37 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=7.6.5 DIST_SHA512=b2bea5b64e0a17a821c97b22f34e1d1d5c403e6c8030aa7e3de3c814de117907d5341616ac2d86d1e85016b577b5243d3fe3c58db9edfbb021edae9cfae0ba3b VARNISH_MODULES_VERSION=0.25.0 VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VMOD_DYNAMIC_VERSION=7.6-master VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
WORKDIR /etc/varnish
# Tue, 26 Aug 2025 15:45:37 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 26 Aug 2025 15:45:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 26 Aug 2025 15:45:37 GMT
USER varnish
# Tue, 26 Aug 2025 15:45:37 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 26 Aug 2025 15:45:37 GMT
CMD []
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d347e847918994143d8709387f507640aec9549648f4ab8dd0dafaf35cda058`  
		Last Modified: Tue, 26 Aug 2025 17:17:15 GMT  
		Size: 69.7 MB (69726086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564bf67e3d60e0acd5d9612a5dc1bea2c8e30ed426161ea842a2c7203a7aa9f8`  
		Last Modified: Tue, 26 Aug 2025 17:17:08 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e8e125440740ba86e9c177b062cd9e2f77e2e8a5baecdf2b9627697318b17e`  
		Last Modified: Tue, 26 Aug 2025 17:17:08 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:2040c4c901971ec2aa62d7f20a30a283a3855e4e980e1567c742de35e05f9d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 KB (18818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb0b839668077db2d493c4e6f89335931c594587b4958d1d9f5c3171fab912c`

```dockerfile
```

-	Layers:
	-	`sha256:94a86035ec439c327f30139139dfafa0ae939c638319e9658f08da45c2eed1a3`  
		Last Modified: Tue, 26 Aug 2025 18:20:53 GMT  
		Size: 18.8 KB (18818 bytes)  
		MIME: application/vnd.in-toto+json
