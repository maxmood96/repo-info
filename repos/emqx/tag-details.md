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
$ docker pull emqx@sha256:a4198adf5aa4ff207131c9ea9f2d4273c5d03db1d05010eac796a193e5d5f835
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:8e2bfdc3e7a5b34ca4de77f33753f313eb408fe31a5d519864526d2b38a71db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105462134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4543f20e9b7061d572ed7e9cb889b906e6d473a3f170dfeb38d5aa51b219fbc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e54478d76cb26be89195325246b71120e537470a900e575f05745d64fa027f`  
		Last Modified: Mon, 17 Mar 2025 23:12:32 GMT  
		Size: 77.3 MB (77256208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a05e78475e00caa1853725f2e3a7709df919a6a30aaf32bb7eaa8dbf808dc`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:5b2b9f1594ffef5f1442e1683ab1842885a42c5a57e04c047757b5ab28fca42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2291c049078b0bb04b3e8c5c956fb6cf33ee5364baa4ca1f921a4cb7021f746e`

```dockerfile
```

-	Layers:
	-	`sha256:a9f8808066765e582d149ad0b40fc53bc11f7c3513b8e38be07a8765def4ac70`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 2.6 MB (2614515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e96ae50fc2db336889bab96ffe2c6a88fec66ac8fbf7b0090283339f807d0363`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
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
$ docker pull emqx@sha256:17c2c685f6ea381daed635b4d2413ba2772148035f10581e89bfa99b5df236fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:3a3c7b620559ce83c17ba4fae6ce0ff24026b26ea831a160a6c36cfbbd7ded02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125353882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed69cbffdb51187de2b2cd07c4f99ee213df9d0c2ecaee0dd9c170ecc13e2f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a9952e19ffe8de7b43dee788754c3e7aa7e006bc48a2020ed20e137bf284a`  
		Last Modified: Mon, 17 Mar 2025 23:12:36 GMT  
		Size: 97.1 MB (97147955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65f3af15e5991942024404577817f290093c6cc73c306b9b5457f2e02b74b93`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:1850adedac86f3aaefac09cea3a9bf16e6d3faaf143e6df5a12f8c54b4ba63e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49132a604e0a3fbf56b6e41f5f2cb3693d6d59293956a829115ae05fda234a5c`

```dockerfile
```

-	Layers:
	-	`sha256:befe33bf1c163a3f2dda4585fe0106984a68e38ad4a383afdfa27b52ce198b3e`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 2.6 MB (2623911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcc2a157ead6fa4ad55697a82730fb68e1dae6fd5969bd09d71803b77270723`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 12.0 KB (11951 bytes)  
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
$ docker pull emqx@sha256:17c2c685f6ea381daed635b4d2413ba2772148035f10581e89bfa99b5df236fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:3a3c7b620559ce83c17ba4fae6ce0ff24026b26ea831a160a6c36cfbbd7ded02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125353882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed69cbffdb51187de2b2cd07c4f99ee213df9d0c2ecaee0dd9c170ecc13e2f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a9952e19ffe8de7b43dee788754c3e7aa7e006bc48a2020ed20e137bf284a`  
		Last Modified: Mon, 17 Mar 2025 23:12:36 GMT  
		Size: 97.1 MB (97147955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65f3af15e5991942024404577817f290093c6cc73c306b9b5457f2e02b74b93`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:1850adedac86f3aaefac09cea3a9bf16e6d3faaf143e6df5a12f8c54b4ba63e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49132a604e0a3fbf56b6e41f5f2cb3693d6d59293956a829115ae05fda234a5c`

```dockerfile
```

-	Layers:
	-	`sha256:befe33bf1c163a3f2dda4585fe0106984a68e38ad4a383afdfa27b52ce198b3e`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 2.6 MB (2623911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcc2a157ead6fa4ad55697a82730fb68e1dae6fd5969bd09d71803b77270723`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 12.0 KB (11951 bytes)  
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
$ docker pull emqx@sha256:a4198adf5aa4ff207131c9ea9f2d4273c5d03db1d05010eac796a193e5d5f835
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:8e2bfdc3e7a5b34ca4de77f33753f313eb408fe31a5d519864526d2b38a71db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105462134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4543f20e9b7061d572ed7e9cb889b906e6d473a3f170dfeb38d5aa51b219fbc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e54478d76cb26be89195325246b71120e537470a900e575f05745d64fa027f`  
		Last Modified: Mon, 17 Mar 2025 23:12:32 GMT  
		Size: 77.3 MB (77256208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a05e78475e00caa1853725f2e3a7709df919a6a30aaf32bb7eaa8dbf808dc`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:5b2b9f1594ffef5f1442e1683ab1842885a42c5a57e04c047757b5ab28fca42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2291c049078b0bb04b3e8c5c956fb6cf33ee5364baa4ca1f921a4cb7021f746e`

```dockerfile
```

-	Layers:
	-	`sha256:a9f8808066765e582d149ad0b40fc53bc11f7c3513b8e38be07a8765def4ac70`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 2.6 MB (2614515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e96ae50fc2db336889bab96ffe2c6a88fec66ac8fbf7b0090283339f807d0363`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
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
$ docker pull emqx@sha256:a4198adf5aa4ff207131c9ea9f2d4273c5d03db1d05010eac796a193e5d5f835
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.5` - linux; amd64

```console
$ docker pull emqx@sha256:8e2bfdc3e7a5b34ca4de77f33753f313eb408fe31a5d519864526d2b38a71db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105462134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4543f20e9b7061d572ed7e9cb889b906e6d473a3f170dfeb38d5aa51b219fbc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e54478d76cb26be89195325246b71120e537470a900e575f05745d64fa027f`  
		Last Modified: Mon, 17 Mar 2025 23:12:32 GMT  
		Size: 77.3 MB (77256208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a05e78475e00caa1853725f2e3a7709df919a6a30aaf32bb7eaa8dbf808dc`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.5` - unknown; unknown

```console
$ docker pull emqx@sha256:5b2b9f1594ffef5f1442e1683ab1842885a42c5a57e04c047757b5ab28fca42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2291c049078b0bb04b3e8c5c956fb6cf33ee5364baa4ca1f921a4cb7021f746e`

```dockerfile
```

-	Layers:
	-	`sha256:a9f8808066765e582d149ad0b40fc53bc11f7c3513b8e38be07a8765def4ac70`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 2.6 MB (2614515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e96ae50fc2db336889bab96ffe2c6a88fec66ac8fbf7b0090283339f807d0363`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
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
$ docker pull emqx@sha256:a4198adf5aa4ff207131c9ea9f2d4273c5d03db1d05010eac796a193e5d5f835
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:8e2bfdc3e7a5b34ca4de77f33753f313eb408fe31a5d519864526d2b38a71db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105462134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4543f20e9b7061d572ed7e9cb889b906e6d473a3f170dfeb38d5aa51b219fbc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e54478d76cb26be89195325246b71120e537470a900e575f05745d64fa027f`  
		Last Modified: Mon, 17 Mar 2025 23:12:32 GMT  
		Size: 77.3 MB (77256208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a05e78475e00caa1853725f2e3a7709df919a6a30aaf32bb7eaa8dbf808dc`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:5b2b9f1594ffef5f1442e1683ab1842885a42c5a57e04c047757b5ab28fca42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2291c049078b0bb04b3e8c5c956fb6cf33ee5364baa4ca1f921a4cb7021f746e`

```dockerfile
```

-	Layers:
	-	`sha256:a9f8808066765e582d149ad0b40fc53bc11f7c3513b8e38be07a8765def4ac70`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 2.6 MB (2614515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e96ae50fc2db336889bab96ffe2c6a88fec66ac8fbf7b0090283339f807d0363`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
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
