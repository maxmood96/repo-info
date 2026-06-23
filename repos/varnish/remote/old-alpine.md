## `varnish:old-alpine`

```console
$ docker pull varnish@sha256:a44e33228e62b1da338b0de838e56ef0c49fc828e933b393a7ecf20a38121e60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:old-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:b05c774dc8e19360f9718835e98af8f4b94f73a5c945d2052a528958944b892e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93034595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c921eb4e0ed8f21795cc59b2fdde256911e14722157457c03969d4c9c52e5fa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:23 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 22 Jun 2026 19:54:23 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Mon, 22 Jun 2026 19:54:23 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Mon, 22 Jun 2026 19:54:23 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 22 Jun 2026 19:54:23 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 22 Jun 2026 19:54:23 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 22 Jun 2026 19:54:23 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 22 Jun 2026 19:54:23 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 22 Jun 2026 19:54:23 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jun 2026 19:54:23 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jun 2026 19:54:23 GMT
ENV VSM_NOPID=1
# Mon, 22 Jun 2026 19:54:23 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 22 Jun 2026 19:54:23 GMT
WORKDIR /etc/varnish
# Mon, 22 Jun 2026 19:54:23 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:23 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 22 Jun 2026 19:54:23 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 22 Jun 2026 19:54:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jun 2026 19:54:23 GMT
USER varnish
# Mon, 22 Jun 2026 19:54:23 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 22 Jun 2026 19:54:23 GMT
CMD []
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215620931a8076c266ac6fdd258edb15c83525809dcb96926865c9d0d95db873`  
		Last Modified: Mon, 22 Jun 2026 19:54:37 GMT  
		Size: 89.2 MB (89187040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4129b7be8a15877ab424531ef956ab4c80e6f51fd5abfb3d741a6cce3f0a889`  
		Last Modified: Mon, 22 Jun 2026 19:54:34 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb448c926c3dcc4a2493c5831b29af7223c531dc08cc287d7b606dd8f80b668`  
		Last Modified: Mon, 22 Jun 2026 19:54:34 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c6184f2532de9169714274a7a3be9b149c5ee07c1908ae7f6a28d571de3d54`  
		Last Modified: Mon, 22 Jun 2026 19:54:34 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:275987e296c2e6c9e630b67ac30987a57d563f891d63b116f79ad07278866d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e0caed73f581606a8bda3f1fc2ede415704844bddfda61a7015c634c9ef0aa`

```dockerfile
```

-	Layers:
	-	`sha256:af0ecf12dc5f1c5d3fadff66eccfc4468104a080d93f1d8fb67c7a010985c953`  
		Last Modified: Mon, 22 Jun 2026 19:54:35 GMT  
		Size: 20.5 KB (20498 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:old-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:786088462bfa11a9de63ee6860e3d4cd2582c896cfc30a06ef4adc12f9f1c08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84799141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a087cf9c812fac203b772e01ca99592cf7bf3fed1c3600113de1ac3ea4eeb838`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:50 GMT
ARG PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7
# Mon, 22 Jun 2026 19:55:50 GMT
ARG VARNISH_VERSION_NUMBER=8.0.2
# Mon, 22 Jun 2026 19:55:50 GMT
ARG DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1
# Mon, 22 Jun 2026 19:55:50 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Mon, 22 Jun 2026 19:55:50 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Mon, 22 Jun 2026 19:55:50 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Mon, 22 Jun 2026 19:55:50 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Mon, 22 Jun 2026 19:55:50 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Mon, 22 Jun 2026 19:55:50 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Mon, 22 Jun 2026 19:55:50 GMT
ENV VARNISH_SIZE=100M
# Mon, 22 Jun 2026 19:55:50 GMT
ENV VSM_NOPID=1
# Mon, 22 Jun 2026 19:55:50 GMT
# ARGS: PKG_COMMIT=eb692742c1a107cf3f896985271b35b125873bd7 VARNISH_VERSION_NUMBER=8.0.2 DIST_SHA512=0f349a8227644e3e1f640ad78d8ca04f3293920e53c6b5cd325f34e9dbe1d3a7d459808edff94f136428d7c5a6bd0159dac3ff2c8bb4268b72b6e8aabffbe0f1 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnish/all-packager.git;     cd all-packager;     git checkout $PKG_COMMIT;     cd varnish-cache/alpine;     ls;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION_NUMBER/" 	-e 's@^source=.*@source="https://github.com/varnish/varnish/releases/download/varnish-$pkgver/varnish-$pkgver.tar.gz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tar.gz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/varnish-cache/*/*.apk;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Mon, 22 Jun 2026 19:55:50 GMT
WORKDIR /etc/varnish
# Mon, 22 Jun 2026 19:55:50 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:55:50 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Mon, 22 Jun 2026 19:55:50 GMT
COPY index.html /etc/varnish/ # buildkit
# Mon, 22 Jun 2026 19:55:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Mon, 22 Jun 2026 19:55:50 GMT
USER varnish
# Mon, 22 Jun 2026 19:55:50 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Mon, 22 Jun 2026 19:55:50 GMT
CMD []
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7a4b4ecda678c3dbc222e0d4ec0c1d634527f0a96662609b7421a3f9346c72`  
		Last Modified: Mon, 22 Jun 2026 19:56:02 GMT  
		Size: 80.6 MB (80614146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6d96b8b3760e0d3ae66e00a8e33e9321cddc66151bc0834462e57d378357cf`  
		Last Modified: Mon, 22 Jun 2026 19:56:00 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a2c1e2fa77b64c9a6dacb353229adc80a0853661106bb263e5b97a96390844`  
		Last Modified: Mon, 22 Jun 2026 19:56:00 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e417791ac79c1e5b4c7986b86d151d8da6def0a7b8d3d8c57c2bdf39d31957d`  
		Last Modified: Mon, 22 Jun 2026 19:56:00 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:old-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:5b2cdda6fba2cebdf20b66c6b1bc3d0fef88adfcc0e5f99e3319ae92489b55ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3309acee5e9be0347b2916eae01d5ef83a2a67be67a68e661542d0db32df3247`

```dockerfile
```

-	Layers:
	-	`sha256:92cb663791962fc731364a0b3c0a61c0d1cdef7133cfe9edda21cca123656171`  
		Last Modified: Mon, 22 Jun 2026 19:56:00 GMT  
		Size: 20.6 KB (20602 bytes)  
		MIME: application/vnd.in-toto+json
