<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-rc.2`](#registry300-rc2)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:659d0b14276ef61b9ec46d6d07c77aaa714158312d83700199eed592359c3267
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:8e0f031915890a3b3c4e130babcc24f83acca94c8d43dd7d254c6595fc0f9a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10092123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf814567bb7f3c1bf8403122ed863fc982f4cf0e9869a9306a7def070601cf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512fd48e9ac56f4cf793d3f2fca031fe2b1a5d19e75fba2498a5b94b96ee89c8`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 280.1 KB (280124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669420efbe7e83652e9a4d88aef1138fd5a0f513356ab4a0336d83c9c8173eed`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcf3903ce8c5842c04532ba00a69ce19f238b03872154ad1e257d39a64933c6`  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1e60cf899f2ae517e502d7f8798722c6d0f61d2454862f2bd87172793a1c65`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:d55a9d4facd989a597c3e1e809923ef98e64559317e771493c300dea1a9e7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 KB (188249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f035dda176fcac1590363c5bc946b6086d26d924d50cf9980ea78c0382e57ec5`

```dockerfile
```

-	Layers:
	-	`sha256:cf52253b7ad6a8f47432a215ca190cc99ed6545211f6ffb9932ab20b6611f4fe`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 174.2 KB (174184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d9a80801cbfa2a2c6a6c3c07051d5e5cca7fef29eabd2c7d5c2058dfa6f3`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:b98f0fea3f7142eb5eb98424c6739f74dc3fb06cc4c5063b7250027ce559cef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9455059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acb56f5b6f35e3137bdea33caf1869721b57391e1373eb2d2f34cfb5bc0ca9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ed2887f4a78048b1f22f7f22125618370ad33bb137776b8f517a53e8b1b38f0d`  
		Last Modified: Tue, 07 Jan 2025 02:30:14 GMT  
		Size: 3.2 MB (3150100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c790e94d903071da79d816e6ec1ca41e3699e1920f692ff6a757e7905d0a19f3`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 280.3 KB (280273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6df2110c7bdc8eac0f1fca7ff7e0a2d394b02c1f72e06bb98d0146c319b346`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 6.0 MB (6024103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b81acb7724c9e10a243ca2ee58521426bfe9fb1e8f7f76282f5bc45ff36768`  
		Last Modified: Tue, 07 Jan 2025 06:42:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786e8db11e0fb9efe89d614a159662b1d4bb3bb45662b6b7ad6c05f439e8eed7`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:6c9f5f2789f4de52c26469f088906e1f8b2e6839bcb87e54d556abe8687cfda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb1acc3df04ae1ecd3dcc4fbbf1640eecf16277772999c2d95e04c5de5a6993`

```dockerfile
```

-	Layers:
	-	`sha256:8d1f998a5201ef14b4d2b928b9f1ca6f868f76755a0ab672ba55dcee4477e094`  
		Last Modified: Tue, 07 Jan 2025 06:42:16 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:47ef7710ba9f4fbd700872c21eab27a5dfa893a0e0911715852cdd2868ef21df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6200c959b354647eaf359eec9856aba78d2f961b1429c5cdcfa94c358192dbf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armv7.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7e2a8985a55f5e4f3b3ae472c5b93ce2792c73bcc72c5b6d704ccb5fb434a07b`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 2.9 MB (2911454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2862979d3b8c65bc60344e1997591bded8ed142bd7fd405120128eca7f49ca44`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 292.9 KB (292920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4518dd25cdc89f46b95212b0f8e670f000254dc3db5b67aade21b5b01391faa`  
		Last Modified: Tue, 12 Nov 2024 15:29:50 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f5962f66761865cdcee4ec702fda4f4dbe8fb126939f83ec2992209d0b66f`  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a61ee3ce5af7f700529f55881a97ca5cebdc8c11c768d681b35e4bd9860c1c`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:78b317756a86aa4c6aeb9088c93296bfaa48d4c4cbc06a0ca11c7fd65e62a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72878d323f86f97f5c0701a676fd961d4b6c6a25d2f67b24461e2aaa011a824d`

```dockerfile
```

-	Layers:
	-	`sha256:e791e9085d9badcc51e175cf9eb345929d3837ee061f19a89772b55d1009f974`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 179.0 KB (179043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898f7fdd08c3b472b4e5cff35cbe6e5139db5eb1bc94259a80e14b98868bac1b`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:86cdf44fa43a89e6031fc50e516d886c0b257f9f8463548218f7aa0cddca35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe03a1f8a043cc0d142b1dbfc0701eb12d5888e6714d95ef5de3ee3f66c3637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bf19dcb5e2f7e7518032e1f3abc91f7a0f014fc0f3a03de278aca2c9a523ea4f`  
		Last Modified: Tue, 12 Nov 2024 00:56:06 GMT  
		Size: 3.4 MB (3358858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792e3246e50751fd99db95bd81487f4ff267e527d2bdd744a8f15002029e84b`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 296.2 KB (296245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725d46af85c7a6abba2419cef1cd0a36956cf13a020d059ba8751a3a0687006`  
		Last Modified: Tue, 12 Nov 2024 08:06:05 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6f196c518d25b0537d6b92276855a0f837b6f99bc09e9cd2854e83070c872`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6030f6d937516639db015c42c56128b1c45f80405aa31d885d4e91fc8cd0ea17`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:63ebe77f6c587302b3a687db1d46b6b9e8b5d89b573cfc083d1f9dad199991b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e17de964dc185bfd1b49f65e7621e00c8c3a999513e31042bd22d6f293d26`

```dockerfile
```

-	Layers:
	-	`sha256:191655aad642e846fe9649b077d09cf1d11d1be5742cefe8be2036f8ceafe72f`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 177.1 KB (177087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47532ea0bac7cfc58e078cb792bdb9e1222186b96f8de6519bd95c04af4441b9`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8`

```console
$ docker pull registry@sha256:659d0b14276ef61b9ec46d6d07c77aaa714158312d83700199eed592359c3267
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:2.8` - linux; amd64

```console
$ docker pull registry@sha256:8e0f031915890a3b3c4e130babcc24f83acca94c8d43dd7d254c6595fc0f9a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10092123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf814567bb7f3c1bf8403122ed863fc982f4cf0e9869a9306a7def070601cf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512fd48e9ac56f4cf793d3f2fca031fe2b1a5d19e75fba2498a5b94b96ee89c8`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 280.1 KB (280124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669420efbe7e83652e9a4d88aef1138fd5a0f513356ab4a0336d83c9c8173eed`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcf3903ce8c5842c04532ba00a69ce19f238b03872154ad1e257d39a64933c6`  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1e60cf899f2ae517e502d7f8798722c6d0f61d2454862f2bd87172793a1c65`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:d55a9d4facd989a597c3e1e809923ef98e64559317e771493c300dea1a9e7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 KB (188249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f035dda176fcac1590363c5bc946b6086d26d924d50cf9980ea78c0382e57ec5`

```dockerfile
```

-	Layers:
	-	`sha256:cf52253b7ad6a8f47432a215ca190cc99ed6545211f6ffb9932ab20b6611f4fe`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 174.2 KB (174184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d9a80801cbfa2a2c6a6c3c07051d5e5cca7fef29eabd2c7d5c2058dfa6f3`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:b98f0fea3f7142eb5eb98424c6739f74dc3fb06cc4c5063b7250027ce559cef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9455059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acb56f5b6f35e3137bdea33caf1869721b57391e1373eb2d2f34cfb5bc0ca9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ed2887f4a78048b1f22f7f22125618370ad33bb137776b8f517a53e8b1b38f0d`  
		Last Modified: Tue, 07 Jan 2025 02:30:14 GMT  
		Size: 3.2 MB (3150100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c790e94d903071da79d816e6ec1ca41e3699e1920f692ff6a757e7905d0a19f3`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 280.3 KB (280273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6df2110c7bdc8eac0f1fca7ff7e0a2d394b02c1f72e06bb98d0146c319b346`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 6.0 MB (6024103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b81acb7724c9e10a243ca2ee58521426bfe9fb1e8f7f76282f5bc45ff36768`  
		Last Modified: Tue, 07 Jan 2025 06:42:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786e8db11e0fb9efe89d614a159662b1d4bb3bb45662b6b7ad6c05f439e8eed7`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:6c9f5f2789f4de52c26469f088906e1f8b2e6839bcb87e54d556abe8687cfda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb1acc3df04ae1ecd3dcc4fbbf1640eecf16277772999c2d95e04c5de5a6993`

```dockerfile
```

-	Layers:
	-	`sha256:8d1f998a5201ef14b4d2b928b9f1ca6f868f76755a0ab672ba55dcee4477e094`  
		Last Modified: Tue, 07 Jan 2025 06:42:16 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:47ef7710ba9f4fbd700872c21eab27a5dfa893a0e0911715852cdd2868ef21df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6200c959b354647eaf359eec9856aba78d2f961b1429c5cdcfa94c358192dbf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armv7.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7e2a8985a55f5e4f3b3ae472c5b93ce2792c73bcc72c5b6d704ccb5fb434a07b`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 2.9 MB (2911454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2862979d3b8c65bc60344e1997591bded8ed142bd7fd405120128eca7f49ca44`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 292.9 KB (292920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4518dd25cdc89f46b95212b0f8e670f000254dc3db5b67aade21b5b01391faa`  
		Last Modified: Tue, 12 Nov 2024 15:29:50 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f5962f66761865cdcee4ec702fda4f4dbe8fb126939f83ec2992209d0b66f`  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a61ee3ce5af7f700529f55881a97ca5cebdc8c11c768d681b35e4bd9860c1c`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:78b317756a86aa4c6aeb9088c93296bfaa48d4c4cbc06a0ca11c7fd65e62a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72878d323f86f97f5c0701a676fd961d4b6c6a25d2f67b24461e2aaa011a824d`

```dockerfile
```

-	Layers:
	-	`sha256:e791e9085d9badcc51e175cf9eb345929d3837ee061f19a89772b55d1009f974`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 179.0 KB (179043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898f7fdd08c3b472b4e5cff35cbe6e5139db5eb1bc94259a80e14b98868bac1b`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:86cdf44fa43a89e6031fc50e516d886c0b257f9f8463548218f7aa0cddca35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe03a1f8a043cc0d142b1dbfc0701eb12d5888e6714d95ef5de3ee3f66c3637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bf19dcb5e2f7e7518032e1f3abc91f7a0f014fc0f3a03de278aca2c9a523ea4f`  
		Last Modified: Tue, 12 Nov 2024 00:56:06 GMT  
		Size: 3.4 MB (3358858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792e3246e50751fd99db95bd81487f4ff267e527d2bdd744a8f15002029e84b`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 296.2 KB (296245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725d46af85c7a6abba2419cef1cd0a36956cf13a020d059ba8751a3a0687006`  
		Last Modified: Tue, 12 Nov 2024 08:06:05 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6f196c518d25b0537d6b92276855a0f837b6f99bc09e9cd2854e83070c872`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6030f6d937516639db015c42c56128b1c45f80405aa31d885d4e91fc8cd0ea17`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:63ebe77f6c587302b3a687db1d46b6b9e8b5d89b573cfc083d1f9dad199991b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e17de964dc185bfd1b49f65e7621e00c8c3a999513e31042bd22d6f293d26`

```dockerfile
```

-	Layers:
	-	`sha256:191655aad642e846fe9649b077d09cf1d11d1be5742cefe8be2036f8ceafe72f`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 177.1 KB (177087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47532ea0bac7cfc58e078cb792bdb9e1222186b96f8de6519bd95c04af4441b9`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8.3`

```console
$ docker pull registry@sha256:659d0b14276ef61b9ec46d6d07c77aaa714158312d83700199eed592359c3267
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:2.8.3` - linux; amd64

```console
$ docker pull registry@sha256:8e0f031915890a3b3c4e130babcc24f83acca94c8d43dd7d254c6595fc0f9a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10092123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf814567bb7f3c1bf8403122ed863fc982f4cf0e9869a9306a7def070601cf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512fd48e9ac56f4cf793d3f2fca031fe2b1a5d19e75fba2498a5b94b96ee89c8`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 280.1 KB (280124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669420efbe7e83652e9a4d88aef1138fd5a0f513356ab4a0336d83c9c8173eed`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcf3903ce8c5842c04532ba00a69ce19f238b03872154ad1e257d39a64933c6`  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1e60cf899f2ae517e502d7f8798722c6d0f61d2454862f2bd87172793a1c65`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:d55a9d4facd989a597c3e1e809923ef98e64559317e771493c300dea1a9e7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 KB (188249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f035dda176fcac1590363c5bc946b6086d26d924d50cf9980ea78c0382e57ec5`

```dockerfile
```

-	Layers:
	-	`sha256:cf52253b7ad6a8f47432a215ca190cc99ed6545211f6ffb9932ab20b6611f4fe`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 174.2 KB (174184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d9a80801cbfa2a2c6a6c3c07051d5e5cca7fef29eabd2c7d5c2058dfa6f3`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v6

```console
$ docker pull registry@sha256:b98f0fea3f7142eb5eb98424c6739f74dc3fb06cc4c5063b7250027ce559cef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9455059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acb56f5b6f35e3137bdea33caf1869721b57391e1373eb2d2f34cfb5bc0ca9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ed2887f4a78048b1f22f7f22125618370ad33bb137776b8f517a53e8b1b38f0d`  
		Last Modified: Tue, 07 Jan 2025 02:30:14 GMT  
		Size: 3.2 MB (3150100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c790e94d903071da79d816e6ec1ca41e3699e1920f692ff6a757e7905d0a19f3`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 280.3 KB (280273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6df2110c7bdc8eac0f1fca7ff7e0a2d394b02c1f72e06bb98d0146c319b346`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 6.0 MB (6024103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b81acb7724c9e10a243ca2ee58521426bfe9fb1e8f7f76282f5bc45ff36768`  
		Last Modified: Tue, 07 Jan 2025 06:42:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786e8db11e0fb9efe89d614a159662b1d4bb3bb45662b6b7ad6c05f439e8eed7`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:6c9f5f2789f4de52c26469f088906e1f8b2e6839bcb87e54d556abe8687cfda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb1acc3df04ae1ecd3dcc4fbbf1640eecf16277772999c2d95e04c5de5a6993`

```dockerfile
```

-	Layers:
	-	`sha256:8d1f998a5201ef14b4d2b928b9f1ca6f868f76755a0ab672ba55dcee4477e094`  
		Last Modified: Tue, 07 Jan 2025 06:42:16 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v7

```console
$ docker pull registry@sha256:47ef7710ba9f4fbd700872c21eab27a5dfa893a0e0911715852cdd2868ef21df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6200c959b354647eaf359eec9856aba78d2f961b1429c5cdcfa94c358192dbf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armv7.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7e2a8985a55f5e4f3b3ae472c5b93ce2792c73bcc72c5b6d704ccb5fb434a07b`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 2.9 MB (2911454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2862979d3b8c65bc60344e1997591bded8ed142bd7fd405120128eca7f49ca44`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 292.9 KB (292920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4518dd25cdc89f46b95212b0f8e670f000254dc3db5b67aade21b5b01391faa`  
		Last Modified: Tue, 12 Nov 2024 15:29:50 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f5962f66761865cdcee4ec702fda4f4dbe8fb126939f83ec2992209d0b66f`  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a61ee3ce5af7f700529f55881a97ca5cebdc8c11c768d681b35e4bd9860c1c`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:78b317756a86aa4c6aeb9088c93296bfaa48d4c4cbc06a0ca11c7fd65e62a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72878d323f86f97f5c0701a676fd961d4b6c6a25d2f67b24461e2aaa011a824d`

```dockerfile
```

-	Layers:
	-	`sha256:e791e9085d9badcc51e175cf9eb345929d3837ee061f19a89772b55d1009f974`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 179.0 KB (179043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898f7fdd08c3b472b4e5cff35cbe6e5139db5eb1bc94259a80e14b98868bac1b`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; ppc64le

```console
$ docker pull registry@sha256:86cdf44fa43a89e6031fc50e516d886c0b257f9f8463548218f7aa0cddca35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe03a1f8a043cc0d142b1dbfc0701eb12d5888e6714d95ef5de3ee3f66c3637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bf19dcb5e2f7e7518032e1f3abc91f7a0f014fc0f3a03de278aca2c9a523ea4f`  
		Last Modified: Tue, 12 Nov 2024 00:56:06 GMT  
		Size: 3.4 MB (3358858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792e3246e50751fd99db95bd81487f4ff267e527d2bdd744a8f15002029e84b`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 296.2 KB (296245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725d46af85c7a6abba2419cef1cd0a36956cf13a020d059ba8751a3a0687006`  
		Last Modified: Tue, 12 Nov 2024 08:06:05 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6f196c518d25b0537d6b92276855a0f837b6f99bc09e9cd2854e83070c872`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6030f6d937516639db015c42c56128b1c45f80405aa31d885d4e91fc8cd0ea17`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:63ebe77f6c587302b3a687db1d46b6b9e8b5d89b573cfc083d1f9dad199991b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e17de964dc185bfd1b49f65e7621e00c8c3a999513e31042bd22d6f293d26`

```dockerfile
```

-	Layers:
	-	`sha256:191655aad642e846fe9649b077d09cf1d11d1be5742cefe8be2036f8ceafe72f`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 177.1 KB (177087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47532ea0bac7cfc58e078cb792bdb9e1222186b96f8de6519bd95c04af4441b9`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0-rc.2`

```console
$ docker pull registry@sha256:eee5d904f0bb27619d920ac8a5d7989284ffceb888cd06dd02d3b3a1bd36b486
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:3.0.0-rc.2` - linux; amd64

```console
$ docker pull registry@sha256:16558ecf32fd47937890e8a3121a1d8eba127ada69897a4920742ec4277c36fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18294776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852f51fba12f990813c602a183b42ee1db252f65d7c00bf3c3d31500308dd263`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b25968f4d7d26f92a0453909fcdec270443fe4d57ce048f0ef8bec7d1fde2c`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 279.5 KB (279508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883225a24d675a596dd06542de134b202770bbce68ac14dc5878ba0c5c9fa3b7`  
		Last Modified: Tue, 07 Jan 2025 03:15:25 GMT  
		Size: 14.4 MB (14378435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d3cbfe0e97ec0383da5ad10702ba79d585dfe563d2612be87658e5dcf31f8b`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941106ea010761354c7c6f3da9f6ad9f8cd2fa8545dcb285b473b50a8dbad683`  
		Last Modified: Tue, 07 Jan 2025 03:15:25 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:b842ade9bada404071f5187db28f196d54e69a94dd5b1ae7bb0a82f8ea2b01a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 KB (274666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e350096153180101ef2fe794c538ae2c8a2e1fd76ae51e28d486e67c64a2e2`

```dockerfile
```

-	Layers:
	-	`sha256:e74cc19a035273a2a688bdd1781e4299d1175eb0eceaa62a7af6804c2d49c1a0`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 261.2 KB (261177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f5a029728f7852c931aa456fc3b596f80548dfc6eec52e5311e698fb2047bad`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 13.5 KB (13489 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; arm variant v6

```console
$ docker pull registry@sha256:1d8720148e30aa0ee50c45b82cb33ea42582ffc1b62943918622a3885bfe82da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17150611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c982f5ba76c4adfd6858a0654e4f9c62980e36f8e32fb66767e259981b4d437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a1a066ba01319a2a413a4b4e8495e18954e397883b57ded903afa9d7bd4a5d`  
		Size: 280.3 KB (280338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578b480e2a41b87ba4145aed70a4a30813e67b2b7c033cf1fc5575cf2272866d`  
		Last Modified: Tue, 07 Jan 2025 06:42:04 GMT  
		Size: 13.5 MB (13508626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0767c98b9e60aa404ec1339b5ab8f6433e7208b124047d04379ea82a128f77fd`  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4913fea00606a4171313c83c3292264df13ff04985d55057cbd8e560171b73a`  
		Last Modified: Thu, 19 Dec 2024 06:28:19 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:ff992a6747e3d6a5d92baf865c010e1ed7a9b5b2300eca60513985cac962c031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1e96040b8eaaa593938c55d82a3c084bc66de256cb53fa8cf89caa04956d06`

```dockerfile
```

-	Layers:
	-	`sha256:7f549f548f15c306390125acee36ce8190a22536e1c0b623375653ef3862c2a3`  
		Last Modified: Tue, 07 Jan 2025 06:42:03 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; arm variant v7

```console
$ docker pull registry@sha256:5d77e8a33bdb093947ad4395bc22b9faf7327b01254909bf431d1924a33fe131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16898074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c7574bba18f0dc9903f5189b98f881114656d29a639fbc65cb20c831854eaa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a49a2dc34dc55420bb1a7a53fe706b82cd56c9d5e3b8d9be9b00e726a3443a`  
		Last Modified: Fri, 06 Dec 2024 22:29:24 GMT  
		Size: 299.4 KB (299389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3d1b6e7c5eff08b57f093ce895c5c06cfc34e18516a6a69fed425e1449a2a`  
		Size: 13.5 MB (13498038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fbe80db628c0517ac90e1dd032aacae113fa4132d74b4afcd160051f89c0e3`  
		Last Modified: Thu, 19 Dec 2024 06:27:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2162874ad442d877f30944395e8ff817cbe6c725f7b8ea00becca50235ee163`  
		Last Modified: Thu, 19 Dec 2024 06:28:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:edf5d2fdfee9719479ee89eeb6db6466dc86b97274521f7f9f91667677773277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 KB (281942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea7ee060e35709d8dc500a81274a6f33db9af1404de7516a3768c68988fde40`

```dockerfile
```

-	Layers:
	-	`sha256:83f14b8cf903b56899c706e69d6e2c246693078a18815736f4784e6ea8aeb48d`  
		Last Modified: Thu, 19 Dec 2024 06:28:00 GMT  
		Size: 268.4 KB (268389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5c73ddf305fe520f99fe3805ce14320d00c3da8f6cd48451b4ffbd0b273604`  
		Last Modified: Thu, 19 Dec 2024 06:28:00 GMT  
		Size: 13.6 KB (13553 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:dc5d7af263c8aa4f99b622267dce9a4e569a6f358b83e3bdc5f5fcf3991bd1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17576687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9ca395c0880d6aa8c485168a06d7b774c172fcd53f40ef57426deee7babe29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76606b7c9c09596da9887e8bd5f49a569f68d0adba669c62de5ff3f3b5ff6cd0`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 301.8 KB (301793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6d58ea2e477c5f71842b1b0e9397dbde941e7f6c642be8c55c17d3a29dcef0`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 13.3 MB (13281097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98d3c33120bf4f8de8e4944dff7c4c7f0f358a9b0bac8af8c293368f2ef80e2`  
		Last Modified: Thu, 19 Dec 2024 06:28:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7134c60e6f98135f676bb48e534e4823b22c353d41ad5f68da3672634a7ec2c`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:eaff0147c8e5d8c62f0e21ed653e13148f93fc75323c6936750cdebd671f0f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.0 KB (281969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e9cdb4e2cc14e62231834ea289653320c986f3da5ecbbd125144ab7d247992`

```dockerfile
```

-	Layers:
	-	`sha256:7c03077250907f83ad65396dbd92877ae196d20bef3c3fdef0e1ef215bb96971`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 268.4 KB (268397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96ff30c6a5816d64055d960d81e0a3b1145c2f5febe3963353c297dee0f9cc08`  
		Size: 13.6 KB (13572 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; ppc64le

```console
$ docker pull registry@sha256:d069cd16aa5d0b943368ec949ca2267b58227cace6976ab50e7847afc0686973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16810040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4a4d4d26dbfae2dce577b1b4ba941c12271cece53fcf1559506086949b927e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60799cfa64278921df2cb5022a9b2506e24511fba4464615a66b4483fdd67cc1`  
		Last Modified: Tue, 07 Jan 2025 06:12:41 GMT  
		Size: 282.1 KB (282104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40354154bfb4591bfb0c1ba5d55be65d6bf734f3ed6057c5a055c19415bf4606`  
		Last Modified: Tue, 07 Jan 2025 06:12:41 GMT  
		Size: 13.0 MB (12959581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1444c672ee9241abe8014dba030259186cdbf58b2b6372aceb3b3b73ff2ab499`  
		Last Modified: Tue, 07 Jan 2025 06:12:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c160667d4ca60956a1995df3220b2ec52de1bdc2d24b65ba11dce51ee656567`  
		Last Modified: Tue, 07 Jan 2025 06:12:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:80b92939581f8a7f5fc66a604f5a2c97077b5d815240c5dfdcb059c02166d4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 KB (272759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57559374670a813c7fb28344e132723fcb18a4b791673f6f73bd835ac2184f8`

```dockerfile
```

-	Layers:
	-	`sha256:b95b258e962654bfc537b1e4e1ee302bebb37e256eeebedc6beb1c8371244a09`  
		Last Modified: Tue, 07 Jan 2025 06:12:41 GMT  
		Size: 259.2 KB (259242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38badef409d4f64dd3475840252823d55ec468804f963cf59be86a8e32e1330`  
		Last Modified: Tue, 07 Jan 2025 06:12:41 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; riscv64

```console
$ docker pull registry@sha256:14539ed2e75a71290875ecaafe5265c96e9fea788339fefbcb640b1dff1b0277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17320358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafb47fe39616521b03ac91bdf375de8b7a2dd179c50dd5053c21e89a2a84d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352d2aed11821bec39048fd95800ed8324f4ffbc936cc77681114832e36fdb97`  
		Size: 299.6 KB (299638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf63c2df3c6854583b64ea49993152004ff39f0c230370eca815fca6495d5649`  
		Last Modified: Thu, 19 Dec 2024 06:29:24 GMT  
		Size: 13.7 MB (13666087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd33c4db783cfc3577a8b0eb797331b8d9095e4880631797be76c2d8eff637b`  
		Last Modified: Thu, 19 Dec 2024 06:29:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3e3d9547781d9a3da6db638e7bc904ff603a35389168b11ffa27124122d339`  
		Last Modified: Thu, 19 Dec 2024 06:29:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:1c689ac0499ff5455e2af642ad38c01efd7dc3ec5226e057d53a64775edc7ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 KB (279955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe1c8660293640fc31cb59b91e26f79b0df0169438ccb905677efe30d8d9e50`

```dockerfile
```

-	Layers:
	-	`sha256:3c081ebdc1d1f64f2f33e219adfb72f319dc66e2fc10f4d9bad22b3ac570533e`  
		Last Modified: Thu, 19 Dec 2024 06:29:22 GMT  
		Size: 266.4 KB (266438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcc81fc93710c2acf4735c4c1f5e5f1a9f5b407023267abed377546ab9155df6`  
		Last Modified: Thu, 19 Dec 2024 06:29:22 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; s390x

```console
$ docker pull registry@sha256:7ae77b91df20b486f3ca052486d127073e310f98a521d8789d3b94bd00746d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17615138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6e3b86c235a5b614b0d08f55bc4c408dd5563f43bed09369ed3e78d781fae9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82495024d9a8579f15a17159de8fe1011aa2dc02d718c9ddede18ae591e4a8a`  
		Last Modified: Thu, 19 Dec 2024 06:28:38 GMT  
		Size: 300.4 KB (300390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9695dacfba9c5aebbe41878ddd1e83a5aff97ca1f7edbd634bb17eb90f26c4`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 13.8 MB (13844617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5fe3c3bc36f27b514a9c27430d2a137c4163e9267ed72f9a240f128bf81bbc`  
		Last Modified: Thu, 19 Dec 2024 06:28:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de77d6e77389c8d89456749cbb0f3b74478ed22f71c4f1969925d8ff14221a`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:1a041b7713caa35b4c53e3e81d812b120a2f0913409d5e09e101681454def0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 KB (279904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad162d25247e96868cae61476c38396bc278a30b0fc986d3010ff2738fd0f03c`

```dockerfile
```

-	Layers:
	-	`sha256:29bb371deb30ab893c2cc08e1b4471676ef9b65127e7787f700d13ded1b8b760`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 266.4 KB (266416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:983980c9b45a085848b82f115693301270502bd0d8a3f702b3116e5df119dadb`  
		Last Modified: Thu, 19 Dec 2024 06:28:38 GMT  
		Size: 13.5 KB (13488 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:2fc8a6fedb91029d2ab86f39c3b499280f369cf540bbff838423e05d93e75f99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:8e0f031915890a3b3c4e130babcc24f83acca94c8d43dd7d254c6595fc0f9a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10092123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf814567bb7f3c1bf8403122ed863fc982f4cf0e9869a9306a7def070601cf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512fd48e9ac56f4cf793d3f2fca031fe2b1a5d19e75fba2498a5b94b96ee89c8`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 280.1 KB (280124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669420efbe7e83652e9a4d88aef1138fd5a0f513356ab4a0336d83c9c8173eed`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcf3903ce8c5842c04532ba00a69ce19f238b03872154ad1e257d39a64933c6`  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1e60cf899f2ae517e502d7f8798722c6d0f61d2454862f2bd87172793a1c65`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:d55a9d4facd989a597c3e1e809923ef98e64559317e771493c300dea1a9e7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 KB (188249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f035dda176fcac1590363c5bc946b6086d26d924d50cf9980ea78c0382e57ec5`

```dockerfile
```

-	Layers:
	-	`sha256:cf52253b7ad6a8f47432a215ca190cc99ed6545211f6ffb9932ab20b6611f4fe`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 174.2 KB (174184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d9a80801cbfa2a2c6a6c3c07051d5e5cca7fef29eabd2c7d5c2058dfa6f3`  
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:b98f0fea3f7142eb5eb98424c6739f74dc3fb06cc4c5063b7250027ce559cef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9455059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acb56f5b6f35e3137bdea33caf1869721b57391e1373eb2d2f34cfb5bc0ca9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ed2887f4a78048b1f22f7f22125618370ad33bb137776b8f517a53e8b1b38f0d`  
		Last Modified: Tue, 07 Jan 2025 02:30:14 GMT  
		Size: 3.2 MB (3150100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c790e94d903071da79d816e6ec1ca41e3699e1920f692ff6a757e7905d0a19f3`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 280.3 KB (280273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6df2110c7bdc8eac0f1fca7ff7e0a2d394b02c1f72e06bb98d0146c319b346`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 6.0 MB (6024103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b81acb7724c9e10a243ca2ee58521426bfe9fb1e8f7f76282f5bc45ff36768`  
		Last Modified: Tue, 07 Jan 2025 06:42:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786e8db11e0fb9efe89d614a159662b1d4bb3bb45662b6b7ad6c05f439e8eed7`  
		Last Modified: Tue, 07 Jan 2025 06:42:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:6c9f5f2789f4de52c26469f088906e1f8b2e6839bcb87e54d556abe8687cfda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb1acc3df04ae1ecd3dcc4fbbf1640eecf16277772999c2d95e04c5de5a6993`

```dockerfile
```

-	Layers:
	-	`sha256:8d1f998a5201ef14b4d2b928b9f1ca6f868f76755a0ab672ba55dcee4477e094`  
		Last Modified: Tue, 07 Jan 2025 06:42:16 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:47ef7710ba9f4fbd700872c21eab27a5dfa893a0e0911715852cdd2868ef21df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6200c959b354647eaf359eec9856aba78d2f961b1429c5cdcfa94c358192dbf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armv7.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7e2a8985a55f5e4f3b3ae472c5b93ce2792c73bcc72c5b6d704ccb5fb434a07b`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 2.9 MB (2911454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2862979d3b8c65bc60344e1997591bded8ed142bd7fd405120128eca7f49ca44`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 292.9 KB (292920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4518dd25cdc89f46b95212b0f8e670f000254dc3db5b67aade21b5b01391faa`  
		Last Modified: Tue, 12 Nov 2024 15:29:50 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f5962f66761865cdcee4ec702fda4f4dbe8fb126939f83ec2992209d0b66f`  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a61ee3ce5af7f700529f55881a97ca5cebdc8c11c768d681b35e4bd9860c1c`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:78b317756a86aa4c6aeb9088c93296bfaa48d4c4cbc06a0ca11c7fd65e62a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72878d323f86f97f5c0701a676fd961d4b6c6a25d2f67b24461e2aaa011a824d`

```dockerfile
```

-	Layers:
	-	`sha256:e791e9085d9badcc51e175cf9eb345929d3837ee061f19a89772b55d1009f974`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 179.0 KB (179043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898f7fdd08c3b472b4e5cff35cbe6e5139db5eb1bc94259a80e14b98868bac1b`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:95c15c6a3e784c1b87bd2b03dfe279b83cd3b6ccce330ad6adb8f07e0720cb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9324664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f358fcd805fe6872590689e1a5f551bed07c3b59c5f163445e50273e43b6dcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5c877fdbcd847569c3edb3dc629e4db53a0f9f57223c60c49f8170fd4318dcc3`  
		Last Modified: Tue, 07 Jan 2025 02:32:59 GMT  
		Size: 3.4 MB (3352784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079368551e03dbfebff6c494bbbecf25822cea384fbea6642472638c45c02625`  
		Last Modified: Tue, 07 Jan 2025 06:13:13 GMT  
		Size: 282.1 KB (282083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf20f96a940953487c46a1c9baf778a210d310416efb77d636fa930da8bdeae`  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd024ed6200b5876a9fbac4bc327fc76555e3da1dd66feb73f348909da0ef3c5`  
		Last Modified: Tue, 07 Jan 2025 06:13:13 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f854332d4f080695784c5b296af84f05c416af996f04b7976d641e1924303a55`  
		Last Modified: Tue, 07 Jan 2025 06:13:13 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:4c53f4667d6d91bf033df9d18ceccf31eec8c36a6cb580d4cce2645636d30895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.4 KB (186378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c618c90431b3bd257d82e0b1a8273aa1af1176accfbda9322d5167ec5a6ff1`

```dockerfile
```

-	Layers:
	-	`sha256:766038e53fd3401c8b124e425a7412d4ac1b1d19a769d890ab57a049f738bd69`  
		Last Modified: Tue, 07 Jan 2025 06:13:13 GMT  
		Size: 172.3 KB (172267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e35566a60897fb71a0d00872e6560d4adcaed4c9db615a85aab2558ccdd0b41`  
		Last Modified: Tue, 07 Jan 2025 06:13:13 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json
