<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.5`](#emqx585)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:fccbdab89b862e7209ffcac51d8e6beb9e64d531cb12e32d69a94a72aa9fb6bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:0094eee4d86d36762069a4e7c7eef6c443edd7cb4ab8febfd5f752c2b596250b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105476470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc4150a5c55d39550a68bbdf316f5d14c82e699323c2e09c3e994d18b1a5835`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d6aa382eb37c556af8a1616111cb063f5008d82cffa29947108fe44c402ddf`  
		Last Modified: Wed, 26 Feb 2025 20:27:44 GMT  
		Size: 77.3 MB (77256105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb866a131069cecc8734486908a29cb7bdeabd26b7c09f7807a7989a17b60a`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:a67f4b17370a795e3c4612564c5b6a1065285945f30a4e6ca5545815552cb148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54824ff2fb8301c5d8ae430daa6a6263589c6fc815c27e2e35fcd6140f91a5e9`

```dockerfile
```

-	Layers:
	-	`sha256:4d1d33c3adb9b0116037c8d32e71e3617a9cc2ae2ffcb8030c85427aae63a0ea`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 2.5 MB (2470564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8250407e5883ffb41db5e0ad13ac5f4dfc2bdd970fe13a743dcac6d0656c5b89`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:690bdff01d850e9447cd1b314f182257b29e1081302011e46e02cc8860e70bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102571566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a9eee581576607160f2b3b8e1f2ccbb00a6a5292de276aafb2fd08a0156583`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22049b5f099b581c5d16958b6a9ac3ad2fa169c6881b17d6f4536fd98d029acd`  
		Last Modified: Wed, 26 Feb 2025 20:27:46 GMT  
		Size: 74.5 MB (74522077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28ed9900e76432cbf3370c5774efc0cb4bec1a4d2f31216d0335c988fbd8533`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:f0bde9085f1f5e482b45e2a79746b5d0e99dd6bd0f19218a5526ce2621b7e21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12bf22ce007e78bc7dbc15e842578209f11fa7c1ebe68880fc5857c457cb2be`

```dockerfile
```

-	Layers:
	-	`sha256:edd0eb711d4470018468532661425c836441840845eee8514556ed44592400e5`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 2.6 MB (2614783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08c04ef24aa37d12e3c0a54c3528e185a208c1dcfb43ed2d0ff173adeedf79a8`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:f1db05edcec99e0c811c79257582d103844d2668cfeddafe2aeee1bb64dc4747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:19bef65c58a9d80e7b16532682048499386b2a97443f32e338ba4f593904f45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125368143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfa6e4d932249862f18693d6c17e5d44f9266c019fd0189fb33a43af4df8c5e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06295ae8c5f311aab004684137a401206e103b1223d50549de5f51e490d63a91`  
		Last Modified: Tue, 25 Feb 2025 02:11:55 GMT  
		Size: 97.1 MB (97147780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1623c54f375602bb851b2a56ee34806ffa1adc91313f7db32597491d62718b8`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:4a223a603e47ea2970b3f59a55a22985ef320f5fda9ce3428a00b65a3d7ecdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b8b1f5b8be3bf3db841d6559d69549fdaa3c34ae5baf30942af16cc8c263ad`

```dockerfile
```

-	Layers:
	-	`sha256:e7d29a56f2a5dce372bd688ebfcc912c47457df63f8002a5e74e20270dbec5ab`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 2.5 MB (2469986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361431caf86526d1b02a2a1132ff3efc67a3b5bc697709731838ca1eaf8465b5`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 11.9 KB (11950 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fc1f0bc72480373cb6026e537271120d66f5427ac865d2da3ffcff7f73a5d5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121745136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b464c6dcfc92f136330077d779362fb41087d4c6c4fc26fa9f59708f25960c3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b75f0ae6ae2f3d7a07935e2e953a9049f63039114decfe8ccf4ff4ce987b69`  
		Last Modified: Tue, 25 Feb 2025 02:18:37 GMT  
		Size: 93.7 MB (93695648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a672a2c5d502e4285088b479ad1934c813f4ca20c43001bbce878b5280609cf`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:95ee8343bc0b25fd940a40884b66c2bc621e8bf24aa36e413f9bf92e1cdd1e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e166d78a7d069dc27968deff9034284ccf029123ce40b9d3c1d7327c89d140c`

```dockerfile
```

-	Layers:
	-	`sha256:3600e2fee9d3ba1ffbe41bc43ebb773cf8787a74c9a03b19eba34b807b12c693`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 2.6 MB (2624155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598f302a8cb26e3042885c9f04bc95a726d89ee978c4b495d7c546f524e08942`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:f1db05edcec99e0c811c79257582d103844d2668cfeddafe2aeee1bb64dc4747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:19bef65c58a9d80e7b16532682048499386b2a97443f32e338ba4f593904f45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125368143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfa6e4d932249862f18693d6c17e5d44f9266c019fd0189fb33a43af4df8c5e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06295ae8c5f311aab004684137a401206e103b1223d50549de5f51e490d63a91`  
		Last Modified: Tue, 25 Feb 2025 02:11:55 GMT  
		Size: 97.1 MB (97147780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1623c54f375602bb851b2a56ee34806ffa1adc91313f7db32597491d62718b8`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:4a223a603e47ea2970b3f59a55a22985ef320f5fda9ce3428a00b65a3d7ecdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b8b1f5b8be3bf3db841d6559d69549fdaa3c34ae5baf30942af16cc8c263ad`

```dockerfile
```

-	Layers:
	-	`sha256:e7d29a56f2a5dce372bd688ebfcc912c47457df63f8002a5e74e20270dbec5ab`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 2.5 MB (2469986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361431caf86526d1b02a2a1132ff3efc67a3b5bc697709731838ca1eaf8465b5`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 11.9 KB (11950 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fc1f0bc72480373cb6026e537271120d66f5427ac865d2da3ffcff7f73a5d5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121745136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b464c6dcfc92f136330077d779362fb41087d4c6c4fc26fa9f59708f25960c3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b75f0ae6ae2f3d7a07935e2e953a9049f63039114decfe8ccf4ff4ce987b69`  
		Last Modified: Tue, 25 Feb 2025 02:18:37 GMT  
		Size: 93.7 MB (93695648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a672a2c5d502e4285088b479ad1934c813f4ca20c43001bbce878b5280609cf`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:95ee8343bc0b25fd940a40884b66c2bc621e8bf24aa36e413f9bf92e1cdd1e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e166d78a7d069dc27968deff9034284ccf029123ce40b9d3c1d7327c89d140c`

```dockerfile
```

-	Layers:
	-	`sha256:3600e2fee9d3ba1ffbe41bc43ebb773cf8787a74c9a03b19eba34b807b12c693`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 2.6 MB (2624155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598f302a8cb26e3042885c9f04bc95a726d89ee978c4b495d7c546f524e08942`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:fccbdab89b862e7209ffcac51d8e6beb9e64d531cb12e32d69a94a72aa9fb6bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:0094eee4d86d36762069a4e7c7eef6c443edd7cb4ab8febfd5f752c2b596250b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105476470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc4150a5c55d39550a68bbdf316f5d14c82e699323c2e09c3e994d18b1a5835`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d6aa382eb37c556af8a1616111cb063f5008d82cffa29947108fe44c402ddf`  
		Last Modified: Wed, 26 Feb 2025 20:27:44 GMT  
		Size: 77.3 MB (77256105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb866a131069cecc8734486908a29cb7bdeabd26b7c09f7807a7989a17b60a`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:a67f4b17370a795e3c4612564c5b6a1065285945f30a4e6ca5545815552cb148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54824ff2fb8301c5d8ae430daa6a6263589c6fc815c27e2e35fcd6140f91a5e9`

```dockerfile
```

-	Layers:
	-	`sha256:4d1d33c3adb9b0116037c8d32e71e3617a9cc2ae2ffcb8030c85427aae63a0ea`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 2.5 MB (2470564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8250407e5883ffb41db5e0ad13ac5f4dfc2bdd970fe13a743dcac6d0656c5b89`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:690bdff01d850e9447cd1b314f182257b29e1081302011e46e02cc8860e70bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102571566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a9eee581576607160f2b3b8e1f2ccbb00a6a5292de276aafb2fd08a0156583`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22049b5f099b581c5d16958b6a9ac3ad2fa169c6881b17d6f4536fd98d029acd`  
		Last Modified: Wed, 26 Feb 2025 20:27:46 GMT  
		Size: 74.5 MB (74522077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28ed9900e76432cbf3370c5774efc0cb4bec1a4d2f31216d0335c988fbd8533`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:f0bde9085f1f5e482b45e2a79746b5d0e99dd6bd0f19218a5526ce2621b7e21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12bf22ce007e78bc7dbc15e842578209f11fa7c1ebe68880fc5857c457cb2be`

```dockerfile
```

-	Layers:
	-	`sha256:edd0eb711d4470018468532661425c836441840845eee8514556ed44592400e5`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 2.6 MB (2614783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08c04ef24aa37d12e3c0a54c3528e185a208c1dcfb43ed2d0ff173adeedf79a8`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.5`

```console
$ docker pull emqx@sha256:fccbdab89b862e7209ffcac51d8e6beb9e64d531cb12e32d69a94a72aa9fb6bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.5` - linux; amd64

```console
$ docker pull emqx@sha256:0094eee4d86d36762069a4e7c7eef6c443edd7cb4ab8febfd5f752c2b596250b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105476470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc4150a5c55d39550a68bbdf316f5d14c82e699323c2e09c3e994d18b1a5835`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d6aa382eb37c556af8a1616111cb063f5008d82cffa29947108fe44c402ddf`  
		Last Modified: Wed, 26 Feb 2025 20:27:44 GMT  
		Size: 77.3 MB (77256105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb866a131069cecc8734486908a29cb7bdeabd26b7c09f7807a7989a17b60a`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.5` - unknown; unknown

```console
$ docker pull emqx@sha256:a67f4b17370a795e3c4612564c5b6a1065285945f30a4e6ca5545815552cb148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54824ff2fb8301c5d8ae430daa6a6263589c6fc815c27e2e35fcd6140f91a5e9`

```dockerfile
```

-	Layers:
	-	`sha256:4d1d33c3adb9b0116037c8d32e71e3617a9cc2ae2ffcb8030c85427aae63a0ea`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 2.5 MB (2470564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8250407e5883ffb41db5e0ad13ac5f4dfc2bdd970fe13a743dcac6d0656c5b89`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:690bdff01d850e9447cd1b314f182257b29e1081302011e46e02cc8860e70bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102571566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a9eee581576607160f2b3b8e1f2ccbb00a6a5292de276aafb2fd08a0156583`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22049b5f099b581c5d16958b6a9ac3ad2fa169c6881b17d6f4536fd98d029acd`  
		Last Modified: Wed, 26 Feb 2025 20:27:46 GMT  
		Size: 74.5 MB (74522077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28ed9900e76432cbf3370c5774efc0cb4bec1a4d2f31216d0335c988fbd8533`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.5` - unknown; unknown

```console
$ docker pull emqx@sha256:f0bde9085f1f5e482b45e2a79746b5d0e99dd6bd0f19218a5526ce2621b7e21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12bf22ce007e78bc7dbc15e842578209f11fa7c1ebe68880fc5857c457cb2be`

```dockerfile
```

-	Layers:
	-	`sha256:edd0eb711d4470018468532661425c836441840845eee8514556ed44592400e5`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 2.6 MB (2614783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08c04ef24aa37d12e3c0a54c3528e185a208c1dcfb43ed2d0ff173adeedf79a8`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:fccbdab89b862e7209ffcac51d8e6beb9e64d531cb12e32d69a94a72aa9fb6bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:0094eee4d86d36762069a4e7c7eef6c443edd7cb4ab8febfd5f752c2b596250b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105476470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc4150a5c55d39550a68bbdf316f5d14c82e699323c2e09c3e994d18b1a5835`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d6aa382eb37c556af8a1616111cb063f5008d82cffa29947108fe44c402ddf`  
		Last Modified: Wed, 26 Feb 2025 20:27:44 GMT  
		Size: 77.3 MB (77256105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb866a131069cecc8734486908a29cb7bdeabd26b7c09f7807a7989a17b60a`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:a67f4b17370a795e3c4612564c5b6a1065285945f30a4e6ca5545815552cb148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54824ff2fb8301c5d8ae430daa6a6263589c6fc815c27e2e35fcd6140f91a5e9`

```dockerfile
```

-	Layers:
	-	`sha256:4d1d33c3adb9b0116037c8d32e71e3617a9cc2ae2ffcb8030c85427aae63a0ea`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 2.5 MB (2470564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8250407e5883ffb41db5e0ad13ac5f4dfc2bdd970fe13a743dcac6d0656c5b89`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:690bdff01d850e9447cd1b314f182257b29e1081302011e46e02cc8860e70bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102571566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a9eee581576607160f2b3b8e1f2ccbb00a6a5292de276aafb2fd08a0156583`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22049b5f099b581c5d16958b6a9ac3ad2fa169c6881b17d6f4536fd98d029acd`  
		Last Modified: Wed, 26 Feb 2025 20:27:46 GMT  
		Size: 74.5 MB (74522077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28ed9900e76432cbf3370c5774efc0cb4bec1a4d2f31216d0335c988fbd8533`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:f0bde9085f1f5e482b45e2a79746b5d0e99dd6bd0f19218a5526ce2621b7e21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12bf22ce007e78bc7dbc15e842578209f11fa7c1ebe68880fc5857c457cb2be`

```dockerfile
```

-	Layers:
	-	`sha256:edd0eb711d4470018468532661425c836441840845eee8514556ed44592400e5`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 2.6 MB (2614783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08c04ef24aa37d12e3c0a54c3528e185a208c1dcfb43ed2d0ff173adeedf79a8`  
		Last Modified: Wed, 26 Feb 2025 20:27:43 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
