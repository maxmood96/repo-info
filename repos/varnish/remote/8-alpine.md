## `varnish:8-alpine`

```console
$ docker pull varnish@sha256:0860b5e9f5535e373080f6921bdb68959dc93c300da569107cfedc45fe236e67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:8-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:41f3ee7e8f3a3a46657d7df7ddadd5eea49da1d7186284c299faf77f3cec2c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91658907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791bb19331c2b2bdffebd848babfd121a6021d9427e2c6f475f99a072a619ee8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:23 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_VERSION=8.0.1
# Wed, 15 Apr 2026 20:24:23 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 15 Apr 2026 20:24:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 15 Apr 2026 20:24:23 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VARNISH_SIZE=100M
# Wed, 15 Apr 2026 20:24:23 GMT
ENV VSM_NOPID=1
# Wed, 15 Apr 2026 20:24:23 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
WORKDIR /etc/varnish
# Wed, 15 Apr 2026 20:24:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 15 Apr 2026 20:24:24 GMT
USER varnish
# Wed, 15 Apr 2026 20:24:24 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 15 Apr 2026 20:24:24 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679d8a78a51fbc1e26e3a678fe492cb6f2332d4ee6ff65807916cefd5e7a4543`  
		Last Modified: Wed, 15 Apr 2026 20:24:37 GMT  
		Size: 87.8 MB (87791576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbbe98298180f5425cbd3529c155c99c4e2c43a390736a0524bb53683e88a1d`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94df06b538832a31a7961a6b753325a876258ed49ff0bebc40e9f1e3c04d0429`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0000b7ec6e0d633f66fbfb4778f222772737c21df487d6d648510fe7ebeca081`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:121924b23cede2872bba60cfc876f0b636157d3953b18b905da44259989aa0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b064587648707975a1acba9f70f37952c06481aa9895c4baafc8fc2393dfc3a5`

```dockerfile
```

-	Layers:
	-	`sha256:676e5180366d3c79d0802be63ad307362ab73fce89e51c60c4b2fb7c1b54c9e5`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:8-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:67be9e66cdb3ad84876f5dad5620896effd2e231ae6a997051af53eacb54e8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83419928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4d2863af766a3f848e4feb44e40779c7c6b89b6ce777ffeb9d0b7b73efab98`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:12 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_VERSION=8.0.1
# Wed, 15 Apr 2026 20:24:12 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Wed, 15 Apr 2026 20:24:12 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Wed, 15 Apr 2026 20:24:12 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VARNISH_SIZE=100M
# Wed, 15 Apr 2026 20:24:12 GMT
ENV VSM_NOPID=1
# Wed, 15 Apr 2026 20:24:12 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
WORKDIR /etc/varnish
# Wed, 15 Apr 2026 20:24:12 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
COPY index.html /etc/varnish/ # buildkit
# Wed, 15 Apr 2026 20:24:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 15 Apr 2026 20:24:12 GMT
USER varnish
# Wed, 15 Apr 2026 20:24:12 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 15 Apr 2026 20:24:12 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188f5b124ebe49de1164f7bc653185e82a76feb345a08196cf1a77b777bb7b78`  
		Last Modified: Wed, 15 Apr 2026 20:24:24 GMT  
		Size: 79.2 MB (79216922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da572ca168ae2da5fea13f3ded2448ea2dc618755043a2379de0eeeca56cba1d`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac44db7085a08eafc8087de7e0125e8bf2b440b3971135caf10aa92aebd550f`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191bd24e338faf457cdd8ab90dbc37ac634ed3b5562b7a77c422b9a2d2be6bf3`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:8-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:89d178943cec924648184dd343a5ac5570da6c4ec413e190b55be53a2a99fbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da0f9e255d495cc4139c0ffeacb61b4ca2e1599623537a29fb59707161221c2`

```dockerfile
```

-	Layers:
	-	`sha256:2cf9e1788fc9c92f38269c5e206e19918276f8c47b42d246a2d759dbe45e3da9`  
		Last Modified: Wed, 15 Apr 2026 20:24:22 GMT  
		Size: 20.6 KB (20572 bytes)  
		MIME: application/vnd.in-toto+json
