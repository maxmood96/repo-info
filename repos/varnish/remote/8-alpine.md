## `varnish:8-alpine`

```console
$ docker pull varnish@sha256:edd2efd296a8bdb021841e8498a7cb61ded8bd5f3cb22ab542001a61cc750083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:1e7ed3f804951e43ed90c300bfabb5715b26a4514d119fe6d8dd43f82394adb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93035109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ea455493f4db66379e0f72bf70d9dded0fe1a84a6bc380c4a82f34325b7033`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 16:51:32 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Tue, 19 May 2026 16:51:32 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 19 May 2026 16:51:32 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 19 May 2026 16:51:32 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:32 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 May 2026 16:51:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:32 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:32 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:32 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:32 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:32 GMT
USER varnish
# Tue, 19 May 2026 16:51:32 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:32 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa485f15e897ed487ab343775f0ea4566f20ba9243dcf5e15d4be21c08e6631c`  
		Last Modified: Tue, 19 May 2026 16:51:46 GMT  
		Size: 89.2 MB (89167782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c9ee5c0f2ebc1aad93f89a4dfdf9d107fbae8bf00481a2decd2b78dbd1b2ad`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764fb603eb97ca18bc3b3c5ce407185d508a9671713605475c17d0d82a9323c`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e33232128fff25b6f01216c25ef9c69bc8ce41595b5ce57c613ef8321656a4`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:735b7f36f046328b55da201d60d548ee8362d91a4608b510b40c5c96c89bf4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d526de6586584e4a30351366b98a4360d074bc0f5f0c6642950aebfef0b761cd`

```dockerfile
```

-	Layers:
	-	`sha256:b40482caa22d698478f14b36e184f6f877cf75b72863e34c55b1075fcda74714`  
		Last Modified: Tue, 19 May 2026 16:51:44 GMT  
		Size: 20.5 KB (20498 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:22dcaac69b93b44cc9f776b336847b241613aad120ada8630428acb97281e56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84789676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f8b8675e0517fef28d057db82c312babdf17a2636bd43f2d2807a7f1c58945`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 16:51:24 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Tue, 19 May 2026 16:51:24 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Tue, 19 May 2026 16:51:24 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Tue, 19 May 2026 16:51:24 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Tue, 19 May 2026 16:51:24 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Tue, 19 May 2026 16:51:24 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 16:51:24 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 May 2026 16:51:24 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 16:51:24 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 16:51:24 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 16:51:24 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 16:51:24 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
COPY index.html /etc/varnish/ # buildkit
# Tue, 19 May 2026 16:51:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 16:51:24 GMT
USER varnish
# Tue, 19 May 2026 16:51:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 16:51:24 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7866c4e9b6bce00e744f1b2a14cdce2e24376dd037eae4280770a37130134`  
		Last Modified: Tue, 19 May 2026 16:51:37 GMT  
		Size: 80.6 MB (80586666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49261e403353c66e660d668215eb89e5a5bd2c2667bb602a221c18eed513eb81`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b81b6ea6f91c21f310bd64d939b83e6a6afe6dfbbb6d2cb5675d5a8be1d2f8c`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981e2b7b44dd078d913c48139d9ba5e706b8ceae5d8c3810c4aa4a5c52fc88cd`  
		Last Modified: Tue, 19 May 2026 16:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:4d820622217a8c5b08288f1e7f930bfd19cdd837a826628f419e111ac6f60971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2687331b117a35a869ac374c42ee5ffb2b98e39603c846eee668d7aa47f82ec`

```dockerfile
```

-	Layers:
	-	`sha256:cb5d188d7096c63fc9b8d2d3f404a5d4b2c1987915b922a2457e4945debb20bf`  
		Last Modified: Tue, 19 May 2026 16:51:34 GMT  
		Size: 20.6 KB (20602 bytes)  
		MIME: application/vnd.in-toto+json
