## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:062c4ab1b637b9e9a5d9250ce8508ee167cc45f370f4d2d1f1d1b7991ce845c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:fresh-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:a3574e3b2bd944073722b876c29cf09702b6375036db42f908e4650bf23dbd0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73337749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bacdaeae6793680cab791ebe1361728b7eb083a1facf2a497f7a1ea4cf18d4f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:23:25 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:23:25 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:23:25 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:23:26 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:23:26 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:23:26 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:24:40 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:24:40 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:24:40 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:24:40 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:24:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:24:41 GMT
USER varnish
# Tue, 17 Sep 2024 21:24:41 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:24:41 GMT
CMD []
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e644d68d0bbf715e3aaf103a5de4694aabfd642ca037acec5cd9747bbd9db1e`  
		Last Modified: Tue, 17 Sep 2024 21:25:45 GMT  
		Size: 69.9 MB (69916017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce8bff1fbb90cba56a245cd68096d687f98a03b64a2b1b2681cb21b58ad0035`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6388e5f21c3b90a3870f1d6f8d66c507911dd575681cde25bc1a04550effb8`  
		Last Modified: Tue, 17 Sep 2024 21:25:37 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm variant v7

```console
$ docker pull varnish@sha256:354deab8a503dc8e31a8850bef8b20fa344a9b0a15d14933ae7b5094d4a8c4ec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57533950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a17a406fb78972e5809fdbe52daa99b4e69883753a1179b956a1132227c941`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 22:00:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 22:00:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 22:00:47 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 22:00:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 22:00:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 22:02:14 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 22:02:14 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 22:02:14 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 22:02:14 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 22:02:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 22:02:14 GMT
USER varnish
# Tue, 17 Sep 2024 22:02:14 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 22:02:15 GMT
CMD []
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8813ea3938ff81df50007e31b76067340c1758667bdfd7179d32551ad0bcfa2d`  
		Last Modified: Tue, 17 Sep 2024 22:03:10 GMT  
		Size: 54.6 MB (54604264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05417369d263b7c8d8b315666096d9bab56febfc2a86595bd211969ebe18ad`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba7ded2285f89b8b64eb163a5f0ed74aaeec188161b3bf7fd0aaccae6788a1`  
		Last Modified: Tue, 17 Sep 2024 22:03:04 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:dfe1aee4c184e7663ae040322c0c31b35cd0b8d728f3865de30a67122a3b6f0d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70044444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21780c1110170fc966cb4748ff00e2f7a188c43db1b48811bfecc073ecb4c9e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:46 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:46 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:47 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:47 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:43:48 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:43:49 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:43:49 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:43:49 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:43:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:43:49 GMT
USER varnish
# Tue, 17 Sep 2024 21:43:49 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:43:49 GMT
CMD []
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28ba5a4402255fdab74468444d26ba5a450bb3bf85308c8bfa037ff0d2e4481`  
		Last Modified: Tue, 17 Sep 2024 21:44:39 GMT  
		Size: 66.7 MB (66683314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c872d5a9b252a340d0656fdcf4b6e90d931d11f137f0b44b4444ff273873a2`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2c1c538a2d3a1c5c004361f6a4b125a2483e3a3dc1816c7ea8775f6c7c7f9`  
		Last Modified: Tue, 17 Sep 2024 21:44:33 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; 386

```console
$ docker pull varnish@sha256:3da50e3f81938d063b7849dd4d8f83dc09552bc13b68a0788b2bdaeb5e8966be
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75354425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30579799344622ba130f6df5e174e986f75c31937b2056a74c7c6fb36422fccb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:42:27 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:42:27 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:42:28 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:42:28 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:42:28 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:44:36 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:44:37 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:44:37 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:44:37 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:44:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:44:37 GMT
USER varnish
# Tue, 17 Sep 2024 21:44:37 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:44:37 GMT
CMD []
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cf3a67921019e12988f9ad85476068512edd6a81f7f1f8ff550e83621a3d5b`  
		Last Modified: Tue, 17 Sep 2024 21:45:52 GMT  
		Size: 72.1 MB (72098793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084453347407e41595c52dccc0c96066e579395b163b8855f44de0467535b488`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f056ae9a1c7699ea5fdc01d3dc561774699e1aa2129eb8e22bbd0390ccb475`  
		Last Modified: Tue, 17 Sep 2024 21:45:40 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; ppc64le

```console
$ docker pull varnish@sha256:b33c3bf2263e07743fc34db1e1fd476bca5279d0e472948dcb4caa483dd3e079
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70852146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf71f4aa39c3d3f9cc25e091e2c80279768b5bd3188357306804ada74fe4555`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:21:40 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:21:41 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:21:41 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:21:42 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:21:43 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:21:44 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:21:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:21:45 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:23:09 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:23:11 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:23:12 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:23:12 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:23:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:23:13 GMT
USER varnish
# Tue, 17 Sep 2024 21:23:13 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:23:13 GMT
CMD []
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08064ec4ae5f41f092978faf6983b834979aee5a429e973da86446bcdcfc102a`  
		Last Modified: Tue, 17 Sep 2024 21:24:27 GMT  
		Size: 67.5 MB (67485653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b5dc4a106ffaa87b00a0f8fe0dd74ee249a01a15d621662d178fe13c079e71`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e905a8c021e2e7c34ba3ca625b2f1f36542c7334dfb60820e908c40d94b5678`  
		Last Modified: Tue, 17 Sep 2024 21:24:16 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:fresh-alpine` - linux; s390x

```console
$ docker pull varnish@sha256:db93041e4e4775e3d4159fa1b5b7c65545a3c0dbdc12de978cded0fc36515740
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65242016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af743e848584bd94e6cf9c19729927521a094bfc5207e0be3a21a8aef0830a4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 21:46:31 GMT
ARG PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_VERSION=7.6.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_VERSION=0.25.0
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_VERSION=7.6-master
# Tue, 17 Sep 2024 21:46:31 GMT
ARG VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95
# Tue, 17 Sep 2024 21:46:32 GMT
ARG VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182
# Tue, 17 Sep 2024 21:46:32 GMT
ARG TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VARNISH_SIZE=100M
# Tue, 17 Sep 2024 21:46:32 GMT
ENV VSM_NOPID=1
# Tue, 17 Sep 2024 21:47:54 GMT
# ARGS: DIST_SHA512=11ca965837ef38aa52487f388555dd56a33faaff61d6662e9df647891cf444309323c665fd353c49c69ba327beeba131730b397d1849b8cff721f0d8257b9f48 PKG_COMMIT=7d90347be31891b338dededb318594cebb668ba7 TOOLBOX_COMMIT=cfa9ec43a47429ef94f7e04e4abc58c67ad50add VARNISH_MODULES_SHA512SUM=2ad8ebeab165002d1bfba9a2088951fb10ff573f0205d3f04e68921f191441f4026450f3a0b78f2aa96f40c82838a2d4d5f0688141fa7b8241ae7b7a5f507c10 VARNISH_MODULES_VERSION=0.25.0 VARNISH_VERSION=7.6.0 VMOD_DYNAMIC_COMMIT=5e01fb2176911d68c82c5bafec1ae8dc53da1e95 VMOD_DYNAMIC_SHA512SUM=e25ba047dcee58173901c2742afc36e79bc2b501c1bb7210d69297db031d749179bcde322f0bc9b83224688857e594e2cc64d7995aa7b66ab4936ffc70a50182 VMOD_DYNAMIC_VERSION=7.6-master
RUN set -ex;    BASE_PKGS="tar alpine-sdk sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/nigoroll/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd
# Tue, 17 Sep 2024 21:47:56 GMT
WORKDIR /etc/varnish
# Tue, 17 Sep 2024 21:47:56 GMT
COPY dir:6dcb75fa0bc26d4afaf5dc722b0827803ad6d52fba8af98ee9fcd0dd74a868f3 in /usr/local/bin/ 
# Tue, 17 Sep 2024 21:47:56 GMT
COPY file:687620bda1f16ee1ee6d594345197f41c40d140752af05a628fe7eba7ab8d9bd in /etc/varnish/ 
# Tue, 17 Sep 2024 21:47:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 17 Sep 2024 21:47:57 GMT
USER varnish
# Tue, 17 Sep 2024 21:47:57 GMT
EXPOSE 80 8443
# Tue, 17 Sep 2024 21:47:57 GMT
CMD []
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6d1365d833d5e91a3423b89a361a19152c440c149cd7d12c26e57e64b3069`  
		Last Modified: Tue, 17 Sep 2024 21:49:17 GMT  
		Size: 62.0 MB (61986636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75daf6d5dfbb1c97cf59aa4a63c806056b36c721839e21899802891464a067a6`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85307912e9b6db6d28beb66a825b1bbaaafe821d0bc5b7156ff36f607b7b94c2`  
		Last Modified: Tue, 17 Sep 2024 21:49:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
