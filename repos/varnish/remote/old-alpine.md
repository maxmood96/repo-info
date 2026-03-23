## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:6951946bb82d7cd8e9e1c866ecfe25ae95aa4200c4a88ebd9c49f4dcdf3b26da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:ff7b8e557befb88a7e32161e502dc17f1c390148eb4b5aa40fbf430f42bda3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91704851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c51e3ad6c57540b305abc5e2395c4592823be6b68377dcdbe05bc25b3fffdff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 21:13:42 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_VERSION=8.0.1
# Mon, 23 Mar 2026 21:13:42 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:42 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:42 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:42 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:42 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:42 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:42 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:42 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:43 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:43 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:43 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:43 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206097f4181c9fa4590a2371688ec2119bc36496d8af7eb109bddfc3ac66c60`  
		Last Modified: Mon, 23 Mar 2026 21:13:57 GMT  
		Size: 87.8 MB (87839887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bd9f173e9285143c2c21f2e29a944cec96b4c6e290d39f6b21582c33c73b2f`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 504.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3156a7bc99ed24b11f65d33cdad0ff7f1f005429c1cfd8506dd7e2628286cead`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c026f4d3ee5aa5de156c6f42e55ce767006671ded719b46e12df05e035b4d686`  
		Last Modified: Mon, 23 Mar 2026 21:13:54 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:58e15d7406750f2fd2729d1d4487d270c336a37a4b4dcb2df4fb7603f3d2a339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed36101bbde00452cde137596a63f8061b17f73f5c47fabfb0b44d53ee8feafd`

```dockerfile
```

-	Layers:
	-	`sha256:d6d20eb725eb2633b8a25b87ec89de83be31d4ff6586ec371fe168d896ce0a59`  
		Last Modified: Mon, 23 Mar 2026 21:13:55 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:82ebd7b638c190b9377c18fe6521eb82c55b238f7e891c91efaea21089032b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83462349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d42b11254a33f07217d43166bd040f1006dbaf25dc40680801ebeda1051fc1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 21:13:51 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_VERSION=8.0.1
# Mon, 23 Mar 2026 21:13:51 GMT
ARG DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 23 Mar 2026 21:13:51 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 23 Mar 2026 21:13:51 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VARNISH_SIZE=100M
# Mon, 23 Mar 2026 21:13:51 GMT
ENV VSM_NOPID=1
# Mon, 23 Mar 2026 21:13:51 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION=8.0.1 DIST_SHA512=6f75a135298048f4ee767ec24805e00b30b78c4011768e4828c9893c56379641a404bfb3bf597f7348ca7471833b7791a7e135de3146b6f2fd7b217cceccc971 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
WORKDIR /etc/varnish
# Mon, 23 Mar 2026 21:13:51 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 23 Mar 2026 21:13:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 23 Mar 2026 21:13:51 GMT
USER varnish
# Mon, 23 Mar 2026 21:13:51 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 23 Mar 2026 21:13:51 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9ad70109afe8d82eaaa011549528d090df0d5d0d9cecbc4cc2bfe54457c3c1`  
		Last Modified: Mon, 23 Mar 2026 21:14:05 GMT  
		Size: 79.3 MB (79262120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be347025ff924b1e32d83d731c5d87b0dacb89c1d3de796e1441afa3a336d031`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1258fa3292dfb4cfc41530b03a50383b81ae32873f76c10e06aec2377fcc24f5`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63020009814ee7a38c936c50f5115cfe979cb9163ed0c9a203b3a2e9cdaf58df`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:bd8fd92b77b84b16579b46155bd2bb60bb945c516913ed1414c15aaa38ece413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98d8cf1665d32e833346bf8e61262a7b5a8ec24c8b1eccd24798eecedfa099f`

```dockerfile
```

-	Layers:
	-	`sha256:41c749bc136cb406afc5928735cad6d77e080fb04d426517944569b98caabad1`  
		Last Modified: Mon, 23 Mar 2026 21:14:02 GMT  
		Size: 20.6 KB (20571 bytes)  
		MIME: application/vnd.in-toto+json
