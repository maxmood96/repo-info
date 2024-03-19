## `varnish:alpine`

```console
$ docker pull varnish@sha256:84dc0fb0667bfbc164e61dece65ce47703d8fadfaff8d26795888a9952cb80c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:alpine` - linux; amd64

```console
$ docker pull varnish@sha256:5fbc1bc3e84cd3ac60979a9481a85f5f52ff1cc67faf8947829a7bd7b9b9754b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73097019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11907c4ede7c51a7cc8003a8ebe7e9a0609cfd2fada1ca510e2874ba75b7e1db`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:58:03 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 16 Mar 2024 08:58:03 GMT
ARG VARNISH_VERSION=7.4.2
# Sat, 16 Mar 2024 08:58:04 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Sat, 16 Mar 2024 08:58:04 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 08:58:04 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 08:58:04 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 16 Mar 2024 08:58:04 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Sat, 16 Mar 2024 08:58:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Sat, 16 Mar 2024 08:58:04 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 08:58:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 08:58:04 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 08:59:25 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 08:59:25 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 08:59:25 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 08:59:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 08:59:26 GMT
USER varnish
# Sat, 16 Mar 2024 08:59:26 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 08:59:26 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae58533547796615774c41bafb56460bad4877888565bfc9a1ec6c16f52f6b4`  
		Last Modified: Sat, 16 Mar 2024 09:01:31 GMT  
		Size: 69.7 MB (69687794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99819e92fc3b92e368ea5ea98755d4e3030786570497598bd4e522ba1ac33a56`  
		Last Modified: Sat, 16 Mar 2024 09:01:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:ae15d877b16a9eca5c1c41f757d89ed297cc8f443c69fa711759a93eb37ce6ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57294962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d2c8f3854f037f951775e00013e99cec1267081a8ec3dc3571de8417211882`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:04:36 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 16 Mar 2024 06:04:36 GMT
ARG VARNISH_VERSION=7.4.2
# Sat, 16 Mar 2024 06:04:36 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Sat, 16 Mar 2024 06:04:37 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 06:04:37 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 06:04:37 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 16 Mar 2024 06:04:37 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Sat, 16 Mar 2024 06:04:37 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Sat, 16 Mar 2024 06:04:37 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 06:04:37 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 06:04:37 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 06:06:12 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 06:06:12 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 06:06:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:06:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 06:06:13 GMT
USER varnish
# Sat, 16 Mar 2024 06:06:13 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 06:06:13 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ab5ecb2d1ed8f3c2aae1ab9bd751055e5d7650e89828ea44f142bfcac65fb`  
		Last Modified: Sat, 16 Mar 2024 06:08:44 GMT  
		Size: 54.4 MB (54375566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9005365c96e93c96392277b12692c41855b1ee092d79721e614ea7fa36110f`  
		Last Modified: Sat, 16 Mar 2024 06:08:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:ec98b2eb6b8667b460891865e7efac5ff91a27f865fc4c36b6b1fd734bbc8cd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69908650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1d1ec26a3258c847ab32434c2b7bde64ac4beeabc8748d1801080c01ab7dc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:44:35 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:53:31 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 18:53:31 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 18:53:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 18:53:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:53:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:53:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 18:54:32 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 18:54:33 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 18:54:33 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 18:54:33 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 18:54:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 18:54:33 GMT
USER varnish
# Tue, 19 Mar 2024 18:54:33 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 18:54:33 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d0b6d2fd6cff808b366da93f873d055ce0419948d3444a1bb58808ea47fb3f`  
		Last Modified: Tue, 19 Mar 2024 19:00:52 GMT  
		Size: 66.6 MB (66558909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44994d724b8545ce35ad86ea63237c741cdc823b438f0d6bd598c894642c8179`  
		Last Modified: Tue, 19 Mar 2024 19:00:45 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e930cce73c948215a5db7660fc238edfe4246ba4765a2962c4719e153abc60d`  
		Last Modified: Tue, 19 Mar 2024 19:00:46 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; 386

```console
$ docker pull varnish@sha256:271cfe5af6514984ccd097b3cce731d5a9c032bc99b52cc47110dbc556768d57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75228860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb431a34bb6cdb93a0f5f2e356b8c965ce3a1fc82f8161532b21fa9bd1145809`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:10:49 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_VERSION=7.5.0
# Tue, 19 Mar 2024 18:58:27 GMT
ARG DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_MODULES_VERSION=0.24.0
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6
# Tue, 19 Mar 2024 18:58:27 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Tue, 19 Mar 2024 18:58:28 GMT
ARG VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f
# Tue, 19 Mar 2024 18:58:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292
# Tue, 19 Mar 2024 18:58:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 19 Mar 2024 18:58:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 19 Mar 2024 18:58:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 Mar 2024 19:00:28 GMT
# ARGS: DIST_SHA512=ca77abcb21299942b2bfd433e5f964d2e974cdae92d6a8889217fcd81933a3b7bc1e70ba87d7e842a4f90b59d7948242155380054d67ad49aab8dcea343055a2 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=fd1b1b7ff61654e568df208229eb1af0086c98726592d1269ca5e13b24ce292a4ec6aeea52a5469f465ca426019629ef5db5a54dfed7f1fd2f0a4b50c92503a6 VARNISH_MODULES_VERSION=0.24.0 VARNISH_VERSION=7.5.0 VMOD_DYNAMIC_COMMIT=5dc09f52cd8eeed77d879b0313bd8ad9a749477f VMOD_DYNAMIC_SHA512SUM=0f57c1ca2d85acb4dce86f241a709486fc14dae03af4c6f9a4c59471e4ed2fe776c6a07ed24b898624025b52ed08a051340bc89ce539f25844a0b3650d14c292 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 19 Mar 2024 19:00:28 GMT
WORKDIR /etc/varnish
# Tue, 19 Mar 2024 19:00:29 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 19 Mar 2024 19:00:29 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 19 Mar 2024 19:00:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 Mar 2024 19:00:29 GMT
USER varnish
# Tue, 19 Mar 2024 19:00:29 GMT
EXPOSE 80 8443
# Tue, 19 Mar 2024 19:00:29 GMT
CMD []
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113db18c4e7963ab8ca76533a0c77b2c708d3810e54641faa7945eca0c252dcf`  
		Last Modified: Tue, 19 Mar 2024 19:10:14 GMT  
		Size: 72.0 MB (71982747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4e877b2d115d0c129cc6f97774e825110e4e6bd3931b8c5f04ce7182ffcba6`  
		Last Modified: Tue, 19 Mar 2024 19:10:00 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25f3f77beb119cded24ad4aab6c67e0513920007e46e9354bc1d57d452efdfb`  
		Last Modified: Tue, 19 Mar 2024 19:10:00 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:1ca80c297a6636bef9e676941eadbbd2ae4a9883046c66082eb9962960cccd9e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70612414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39f9f04fdcb24570df2135e595128bbf3a7367d913a0f5bb08e313ef5db2cd8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:04:51 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 16 Mar 2024 07:04:51 GMT
ARG VARNISH_VERSION=7.4.2
# Sat, 16 Mar 2024 07:04:51 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Sat, 16 Mar 2024 07:04:52 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 07:04:52 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 07:04:52 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 16 Mar 2024 07:04:53 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Sat, 16 Mar 2024 07:04:53 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Sat, 16 Mar 2024 07:04:54 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 07:04:54 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 07:04:54 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 07:06:30 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 07:06:32 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 07:06:33 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:06:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 07:06:34 GMT
USER varnish
# Sat, 16 Mar 2024 07:06:34 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 07:06:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53da8af833a2063e7469eca5acf43f5089262962457c9e0c3fa2dd70a25e90e5`  
		Last Modified: Sat, 16 Mar 2024 07:08:52 GMT  
		Size: 67.3 MB (67253562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be6baa01e0aa1ca71e452b7d8f4fdb9481e761b24a79f0236c1162c333219c`  
		Last Modified: Sat, 16 Mar 2024 07:08:42 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:alpine` - linux; s390x

```console
$ docker pull varnish@sha256:658c619e1c5888e359b4e6993de98b842e60f83a216e0e385524ceec95a8214c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64981125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c25a5086d9e97839e0738a7ab23141fdcc358c417980cbd7036347af18b3c0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 23:02:20 GMT
ARG PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d
# Sat, 16 Mar 2024 23:02:20 GMT
ARG VARNISH_VERSION=7.4.2
# Sat, 16 Mar 2024 23:02:20 GMT
ARG DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971
# Sat, 16 Mar 2024 23:02:20 GMT
ARG VARNISH_MODULES_VERSION=0.22.0
# Sat, 16 Mar 2024 23:02:20 GMT
ARG VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a
# Sat, 16 Mar 2024 23:02:21 GMT
ARG VMOD_DYNAMIC_VERSION=2.8.0-1
# Sat, 16 Mar 2024 23:02:21 GMT
ARG VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9
# Sat, 16 Mar 2024 23:02:21 GMT
ARG VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1
# Sat, 16 Mar 2024 23:02:21 GMT
ARG TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55
# Sat, 16 Mar 2024 23:02:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Sat, 16 Mar 2024 23:02:21 GMT
ENV VARNISH_SIZE=100M
# Sat, 16 Mar 2024 23:03:57 GMT
# ARGS: DIST_SHA512=acd61a852ac7d66b268ab831d3a771d7a063a6a257b5e7c25c5a2ec9bccefa845279b9bd5fc85dd0b4f1d56da59164a13149355d1e6187e71ad76463687f7971 PKG_COMMIT=cfa8cb3724e4ca6398f60b09157715bcb99d189d TOOLBOX_COMMIT=01ff3ec18a955f93880afe18167f17d0bc36cd55 VARNISH_MODULES_SHA512SUM=597ac1161224a25c11183fbaaf25412c8f8e0af3bf58fa76161328d8ae97aa7c485cfa6ed50e9f24ce73eca9ddeeb87ee4998427382c0fce633bf43eaf08068a VARNISH_MODULES_VERSION=0.22.0 VARNISH_VERSION=7.4.2 VMOD_DYNAMIC_COMMIT=15e32fb8cf96752c90d895b0ca31451bd05d92d9 VMOD_DYNAMIC_SHA512SUM=d62d7af87770ef370c2e78e5b464f4f7712ebb50281728ca157ff38303f5455f1afdc0f8efaf0040febdf2d0aedbfa4c3369fe0f9d634ed34f185b54876cb4d1 VMOD_DYNAMIC_VERSION=2.8.0-1
RUN set -e;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;
# Sat, 16 Mar 2024 23:03:59 GMT
WORKDIR /etc/varnish
# Sat, 16 Mar 2024 23:03:59 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Sat, 16 Mar 2024 23:03:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 16 Mar 2024 23:03:59 GMT
USER varnish
# Sat, 16 Mar 2024 23:03:59 GMT
EXPOSE 80 8443
# Sat, 16 Mar 2024 23:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e0e3c7f56cc2089f64535150ddab85f53e7531b873d39685447626588bb835`  
		Last Modified: Sat, 16 Mar 2024 23:10:56 GMT  
		Size: 61.7 MB (61737992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caffa1f3451ac4491205f6e354cc93f52b906c40e9f65d8fe5944e999a5ac963`  
		Last Modified: Sat, 16 Mar 2024 23:10:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
