## `varnish:fresh-alpine`

```console
$ docker pull varnish@sha256:d44658f3f59d7683cf163eb5ffe8b63676a38457578347069165d6d3374457c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh-alpine` - linux; amd64

```console
$ docker pull varnish@sha256:f0fb5a5274742a8bd2ebc0ada66d684cc7cd7038b4834c0bdd3a374f04ff7086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80677136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c87d2260c4e612e1984a3ab8fb61ad25fb3f50e69bbbfade33e9942b7397fe0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:48:04 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Thu, 11 Dec 2025 21:48:04 GMT
ARG VARNISH_VERSION=8.0.0
# Thu, 11 Dec 2025 21:48:04 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Thu, 11 Dec 2025 21:48:04 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Thu, 11 Dec 2025 21:48:04 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Thu, 11 Dec 2025 21:48:04 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Dec 2025 21:48:04 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Dec 2025 21:48:04 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Dec 2025 21:48:04 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 11 Dec 2025 21:48:04 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Dec 2025 21:48:04 GMT
ENV VSM_NOPID=1
# Thu, 11 Dec 2025 21:48:04 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Dec 2025 21:48:04 GMT
WORKDIR /etc/varnish
# Thu, 11 Dec 2025 21:48:04 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 21:48:04 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Dec 2025 21:48:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Dec 2025 21:48:04 GMT
USER varnish
# Thu, 11 Dec 2025 21:48:04 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Dec 2025 21:48:04 GMT
CMD []
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc230350bc7fb9b0c1da0dd3da8788eb1462912b6ef3aa94f2587b006dfc4660`  
		Last Modified: Thu, 11 Dec 2025 21:48:18 GMT  
		Size: 76.9 MB (76872624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c191716f4b9e56f4eacd6d99ad4f155a56374424b060949076d7fce8467005`  
		Last Modified: Thu, 11 Dec 2025 21:48:15 GMT  
		Size: 503.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472f9790da0dac7d0a220d14446b1b5fa5b02486742dbf074e4fc0a5bdac5971`  
		Last Modified: Thu, 11 Dec 2025 21:48:15 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:d235a8dea96bb618c6956847a875d3ec09d38e6b6dbfe78886aa80a64f51472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca6bf5093ff61765271da8d2cba11039b0ad357a7cd24730633a7c8b1b3c87e`

```dockerfile
```

-	Layers:
	-	`sha256:a1f4ba7bc4ce9fc762509238927ac3a080c276a64503078803b34ed5483d00f8`  
		Last Modified: Thu, 11 Dec 2025 21:48:15 GMT  
		Size: 19.3 KB (19308 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh-alpine` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:fb380d9020a96c0674e2c1b608424f488889fc8cb656b78f1ccfb87ffb738543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77675083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a525614ba55eed86375221f9e8283cd5a0ef32abd9fa84876077e3ccbe94d3f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:47:59 GMT
ARG PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595
# Thu, 11 Dec 2025 21:47:59 GMT
ARG VARNISH_VERSION=8.0.0
# Thu, 11 Dec 2025 21:47:59 GMT
ARG DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9
# Thu, 11 Dec 2025 21:47:59 GMT
ARG VARNISH_MODULES_VERSION=0.27.0
# Thu, 11 Dec 2025 21:47:59 GMT
ARG VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264
# Thu, 11 Dec 2025 21:47:59 GMT
ARG VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72
# Thu, 11 Dec 2025 21:47:59 GMT
ARG VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881
# Thu, 11 Dec 2025 21:47:59 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Thu, 11 Dec 2025 21:47:59 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkgconfig py3-sphinx
# Thu, 11 Dec 2025 21:47:59 GMT
ENV VARNISH_SIZE=100M
# Thu, 11 Dec 2025 21:47:59 GMT
ENV VSM_NOPID=1
# Thu, 11 Dec 2025 21:47:59 GMT
# ARGS: PKG_COMMIT=1f0d212dc45065f38bd80ac57fe22773a20a0595 VARNISH_VERSION=8.0.0 DIST_SHA512=c381928e23deaacb863dcf389a494f30a56d22a4e88fe0c5dc7d4a93828f3dc0595c7ae41837f3549795828aca1a30e08f4456d4a752a6d12c19b61943dd99e9 VARNISH_MODULES_VERSION=0.27.0 VARNISH_MODULES_SHA512SUM=bb8a55b3d665fe6de918f784a6f4276b2053f5b1cd0628d6b6c6c78c0042fd678736a2f48375cf356daa47a987175f52569c0b468ccd2b37ab55a32c25255264 VMOD_DYNAMIC_COMMIT=99f72bc4958dca3555dbfeeb43512f243b004a72 VMOD_DYNAMIC_SHA512SUM=6f7b635c3fd9b8acfff6130e4bbe88d0bb97dc0ac178918c2288670951dace70742d9c8d7d798fe885ef908707a21ba2e6ca15c1524d531a59c80d4fdc9c5881 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;    BASE_PKGS="tar alpine-sdk curl sudo py3-docutils python3 autoconf automake libtool";     apk add --virtual varnish-build-deps -q --no-progress --update $BASE_PKGS;         addgroup -g 1000 -S varnish;     adduser -u 1000 -S -D -H -s /sbin/nologin -G varnish -g varnish varnish;     adduser -u 1001 -S -D -H -s /sbin/nologin -G varnish -g varnish vcache;     adduser -u 1002 -S -D -H -s /sbin/nologin -G varnish -g varnish varnishlog;         adduser -D builder;     echo "builder ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/builder;     addgroup builder abuild;     su builder -c "abuild-keygen -nai";         git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache/alpine;     git checkout $PKG_COMMIT;     sed -i APKBUILD         -e "s/pkgver=@VERSION@/pkgver=$VARNISH_VERSION/" 	-e 's@^source=.*@source="http://varnish-cache.org/_downloads/varnish-$pkgver.tgz"@' 	-e "s/^sha512sums=.*/sha512sums=\"$DIST_SHA512  varnish-\$pkgver.tgz\"/";         chown builder -R .;     su builder -c "abuild -r";     apk add --allow-untrusted ~builder/packages/pkg-varnish-cache/*/*.apk;     echo -e 'vcl 4.1;\nbackend default none;' > /etc/varnish/default.vcl;         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         install-vmod https://github.com/varnish/varnish-modules/releases/download/$VARNISH_MODULES_VERSION/varnish-modules-$VARNISH_MODULES_VERSION.tar.gz $VARNISH_MODULES_SHA512SUM;         SKIP_CHECK=1 install-vmod https://github.com/gquintard/libvmod-dynamic/archive/$VMOD_DYNAMIC_COMMIT.tar.gz $VMOD_DYNAMIC_SHA512SUM;         apk del --no-network varnish-build-deps;     rm -rf ~builder /pkg-varnish-cache /varnish-modules /vmod-dynamic /etc/sudoers.d/builder;     deluser --remove-home builder;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Thu, 11 Dec 2025 21:47:59 GMT
WORKDIR /etc/varnish
# Thu, 11 Dec 2025 21:47:59 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 21:47:59 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Thu, 11 Dec 2025 21:47:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 11 Dec 2025 21:47:59 GMT
USER varnish
# Thu, 11 Dec 2025 21:47:59 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Thu, 11 Dec 2025 21:47:59 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030ee580ea382c941062b28967a1fefef20542361c07a2a69d374c17932f0b78`  
		Last Modified: Thu, 11 Dec 2025 21:48:12 GMT  
		Size: 73.5 MB (73534952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bffa1ab8a92c392f0d13b196efc82ca7ef9ead79f52eab994b1ba7e8a8cd88`  
		Last Modified: Thu, 11 Dec 2025 21:48:10 GMT  
		Size: 505.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0677c6d95f2b240df9947447e2ac6d5af788423763a1622601db5ad0b988271c`  
		Last Modified: Thu, 11 Dec 2025 21:48:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh-alpine` - unknown; unknown

```console
$ docker pull varnish@sha256:ca4659deccbc0fa676287b42aa5ee674ff8d8d28e8a22955c1478e8c43bad711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 KB (19424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eae7d5fd85fa1114d918f2a5cfa472ef8fd0511c8f1b3db581b2350495e013`

```dockerfile
```

-	Layers:
	-	`sha256:1d37497d5f254fe9b35b3cbd1587c80e187d4e040a75b969fb136a036800ae8a`  
		Last Modified: Thu, 11 Dec 2025 21:48:10 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.in-toto+json
