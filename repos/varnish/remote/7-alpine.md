## `varnish:7-alpine`

```console
$ docker pull varnish@sha256:cc0a7aad884e7e86b751fbb031c56ebee7bef90fe3b05b3272aa58322bfe0af6
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

### `varnish:7-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:e68dc9857076551f8a67225317a95f345ad91e1f11c46c34210a7291adca6967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80315725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f9095c515e21eb54100068f9a2ecfb3955655c2ee88fef95f72e3ccb6db24e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e37e905a5b0a7e3887b2a91c8327b24129284a0d4f3951d3d9c1bc2c311a62d`  
		Last Modified: Tue, 03 Jun 2025 13:50:17 GMT  
		Size: 76.7 MB (76671419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deacc4f5ce53935aa92bcf316166edecb88d737a471b0c6ca0bf48473cc100e`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719d05040e8ab5a7400a08463a05466ce025243a468968194a57f9d867ed71c4`  
		Last Modified: Tue, 03 Jun 2025 13:50:11 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:073fbd63633e8cfd353e4ec52c591ba2ac33e0e754cfb31912e3e78c8c0e2ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23415dee6df89120996803f92b9564456f2f811d2762c918a334bafcdec5278`

```dockerfile
```

-	Layers:
	-	`sha256:018e7686fef92c81e6d79fd1f1bd13969950d4398f0435fad294561c8af9547a`  
		Last Modified: Wed, 04 Jun 2025 22:50:23 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:00ac6b75c1690c74500ec45b30a46a8760a81a908c866bff46a826f6d6d46a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62366095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6240af100b3925d63c86bcc69ff57620fcbc327ba2ba5ace25bb0e38926a2fdd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3277c43e2a6e7ca8224b892d8251fd2f8944eb81fd376d90c5240f7816a0f083`  
		Last Modified: Tue, 27 May 2025 19:00:58 GMT  
		Size: 59.3 MB (59265914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd3f2d2fac3ed373219e2f04eb8c553a4b9cd07f49822a348cd6bd0ba0bf03`  
		Last Modified: Tue, 27 May 2025 19:00:56 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3107ef22442871d82b7ec5388ec01e3e2959a9e0e457bb531af8f317f1835928`  
		Last Modified: Tue, 27 May 2025 19:00:56 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:7350079942c472339e1816bfd7c6aedd38cc60d56c537313b4dd72db0413bc42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a141db0e280fa2f137f3bd523ff5c2742c2efe54f70ea8fc5b7b2ed71f6168`

```dockerfile
```

-	Layers:
	-	`sha256:ca90931822ce458bc12a86e23a88bd82f7c8417c72e440a288c63ba1980187de`  
		Last Modified: Tue, 27 May 2025 19:00:56 GMT  
		Size: 19.6 KB (19553 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:8e0f90786ecfa0f4e952a8bfcd7cf90ffb65f55afe12a1038b44d230554da349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77317664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a8e20c8b0476e94c93500537b71b2d6c9be6fbf759d39ebf428c5825cdf764`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e84cd3f100e7a4987c9955b88d2ef87afc93a0e64cd6d8aa10263812165fe27`  
		Last Modified: Tue, 03 Jun 2025 14:12:57 GMT  
		Size: 73.3 MB (73322572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4f9e26ec65432a8efe09f77a816bf77b643748294604f7eeedb1601897d54`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204ee6311ecdf7dd9255ffe86d6389a3da94408d715faa19f1d7c770750e654`  
		Last Modified: Tue, 03 Jun 2025 14:12:50 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:1fc387008de696d9c88f44df0d8657685c27996c772c00f3d72fbf60635b7557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c364243c247b5f5a8019e10d2800233ed9c74c18cda92e040fcae27072732a`

```dockerfile
```

-	Layers:
	-	`sha256:9886a9295fbfcfb2c559ef20677457a21cea3b439be5bb62329e04ff2d942936`  
		Last Modified: Tue, 27 May 2025 19:20:57 GMT  
		Size: 19.6 KB (19585 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; 386

```console
$ docker pull varnish@sha256:b121f54ac7f5b5c56b4247fd3a89f5eaa87edb49536a78080a31283009af079c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82508852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e09ad2b11367485e00ad4bfd5a72c959b265f7da89c593cb821cd1bd3a31f35`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c61829aa639dff24aad65e1a82bc8d02bf867875e2d4c5e53137c5276cb2d1`  
		Last Modified: Tue, 27 May 2025 18:58:49 GMT  
		Size: 79.0 MB (79043172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4960eea97cf4f85503b6f86d972a55d352d8befc1bb5ce313e3afd030bde0419`  
		Last Modified: Tue, 27 May 2025 18:58:46 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f18cbf086639292a7cf6ea4ef41ea5008005b3aaad98bac0c1e90b1d31838a`  
		Last Modified: Tue, 27 May 2025 18:58:46 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d1466d9b377d819bd92e5f57939cb0c6d678cbfeda41f7364e267c23ad3635d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb75d8d35091397ece88fcbfedf8015f162f250dfa08ba6c4d34d51e129502f7`

```dockerfile
```

-	Layers:
	-	`sha256:1acecb9b3a5cda019c5227afed2ea18570ffeaeb102971e5262e9ae248497b27`  
		Last Modified: Tue, 27 May 2025 18:58:46 GMT  
		Size: 19.4 KB (19432 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:71d583672fd210f53a87283c6cd7d8f0724cb438133803dcc2efddc983a4b8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76438752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9699c43a7e79fb04a4be6186b24690ad97f4e62825ee80eff8b1c7d7e0f210`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbab925e54587cbf4497c7970617c093c097ad8c8130f3f3683fca36278df31`  
		Last Modified: Tue, 27 May 2025 19:02:45 GMT  
		Size: 72.9 MB (72862344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb5bd15cbeac020aacb495032517a81a030115e97271921f08eb49865f0045`  
		Last Modified: Tue, 27 May 2025 19:02:40 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9b52ba2323f2f33051b67003e5f5ccb783f00ff3b7aa934e8d32dbea2c1860`  
		Last Modified: Tue, 27 May 2025 19:02:41 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d94a917abc20ae0e4c8bc4e8f7f1d2945a698b16383f1f33a790aad4876148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c61ed2fadd3eb862006a0a17f29ccc99948148d5f87e0a3ee70403c5c3616c`

```dockerfile
```

-	Layers:
	-	`sha256:1d1a360fb74bcf4bac9f6756708403acf376b869d1fb1bab0b248394b4b0fcfb`  
		Last Modified: Tue, 27 May 2025 19:02:40 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:7-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:d11e359e354542668965c74d14c43927f83784083bff1786e638ab48d378112c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71034509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73df919373dc10e0f84e083bf120e846c130d92fffa1442e1f8bc4441b7a7c3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 26 May 2025 12:40:55 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_VERSION=7.7.1
# Mon, 26 May 2025 12:40:55 GMT
ARG DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_VERSION=0.26.0
# Mon, 26 May 2025 12:40:55 GMT
ARG VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_VERSION=7.7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7
# Mon, 26 May 2025 12:40:55 GMT
ARG VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b
# Mon, 26 May 2025 12:40:55 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Mon, 26 May 2025 12:40:55 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 26 May 2025 12:40:55 GMT
ENV VARNISH_SIZE=100M
# Mon, 26 May 2025 12:40:55 GMT
ENV VSM_NOPID=1
# Mon, 26 May 2025 12:40:55 GMT
# ARGS: PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 VARNISH_VERSION=7.7.1 DIST_SHA512=4a15ff23dc07cb19959031be5070e7da46a2be2d1a1d2e3950966ca593849d3f8be4f41bd35dae75876bbc121bf268345b47aa35764645362aa42b822b634ad9 VARNISH_MODULES_VERSION=0.26.0 VARNISH_MODULES_SHA512SUM=2050ec65ae731bddc74743c9aa6246e41ffba8017c404c32e50d45f72f5a02dd3eb2290f8b8e43e25a385a06819836fb19f8540f1cdae394083729ff6b6aed35 VMOD_DYNAMIC_VERSION=7.7 VMOD_DYNAMIC_COMMIT=490068ba146c48fd7201c8d19cdb37f6d7d932c7 VMOD_DYNAMIC_SHA512SUM=3ff84710d4d9c4fd956cc27c41ae8b3d0bed4db7a2ca70d61e3900cd1f77ff293e2be3551d044a644ec76c6678517d788511e61c803dda2fe75bd5c286d5901b TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         varnishd -V;     install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 26 May 2025 12:40:55 GMT
WORKDIR /etc/varnish
# Mon, 26 May 2025 12:40:55 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 26 May 2025 12:40:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 26 May 2025 12:40:55 GMT
USER varnish
# Mon, 26 May 2025 12:40:55 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 26 May 2025 12:40:55 GMT
CMD []
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03b83f7ad8b83b5dcd56c2bd88b05dac6dbb70832ec12eecc3357cf097f7557`  
		Last Modified: Tue, 27 May 2025 19:01:49 GMT  
		Size: 67.6 MB (67564885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcacd333e5c4954b9a8d9f90265c801e8336cd7c6961afdc4b95da8145104dec`  
		Last Modified: Tue, 27 May 2025 19:01:47 GMT  
		Size: 502.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2611d5ee154f2c95fdcb474c498be2f8f0689c6c70cc4fa28acb770361e34fc`  
		Last Modified: Tue, 27 May 2025 19:01:47 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:7-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:f1c5fa2662bf90956b5c270950cf6d6f2f8a1e3cf0aef9716aaa47400cc6afa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188aab5b4924a51bfbd764a58d62bd7339a56f5b27faa5f8079ca6b60cf58257`

```dockerfile
```

-	Layers:
	-	`sha256:705f3871102b5aba5628f7eabccfed1d5bc984c5e7197744e5d5633ae2f279d5`  
		Last Modified: Tue, 27 May 2025 19:01:47 GMT  
		Size: 19.5 KB (19469 bytes)  
		MIME: application/vnd.in-toto+json
