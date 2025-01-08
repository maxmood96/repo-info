<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-rc.2`](#registry300-rc2)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:26f7266535a3a1dae81e137ba4935c59d96e7bb4b700f64e4af8959ca5ab0419
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
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
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
$ docker pull registry@sha256:9126ddb9b38b2265550e19f0240941a7118b5c620b7561338830de10f9963db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9201788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44abcbb25e569ce7af153a0dacc3e8071eee28693c2f5cae1be010ae314a7aff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-armv7.tar.gz / # buildkit
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
	-	`sha256:52e1a0d0bc554ff1294b79e52982946141f0dbe774dd603e745e91fa95cbdcc0`  
		Size: 2.9 MB (2904510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00e99f059306c5402b4ded95e14a270a824d4046c3afce7ddf45e4eee26102a`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 279.5 KB (279477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a29bd9d7fda548e4391ecbf347c7005f5d6bf0924f75cf1e9db23fd9ffb372d`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf2211f7dd108ea925e6711fb7c6eb5b5d585daba27d80e0959797ef413bd6d`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90dcac0c0f3a1067c4e16107f6b510984601b4d0fc54416356fe6146b745b13`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:318421972eaee19efeda0906a3aee9306fac431b3f50064b33f118dc18771ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 KB (188374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a335c7e70e90b941d4c2ae8df80a015fbf11300b06ba6648736b76227d2917c`

```dockerfile
```

-	Layers:
	-	`sha256:fd7824ae74a43ef109d829b530d3f102c52e1b383289db4d500989c60673d068`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 174.2 KB (174220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392edc5795705d1b0fa57d8865fe41531ca9467fd9ae58f6ad3f23545649c8df`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:9c833162b2eece5355ceb22acd599d2524cc6486f59c545583f4958816da0657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9444451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f5db491c361ca1e645859af99f3b172a2ac3ac1b9896dcf3ef352036deaf96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
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
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de214b2e86deccd7ec891d7639ec311ffe0367fb8514cbac3837f5ef085f774e`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 281.7 KB (281703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9b3e296f121ec56f918ca09de97ee071efc86ad29dcc854d0549d2697e9b18`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 5.8 MB (5824732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203af9cbfb3f6d2622303f23f9c4eedb0ebef36e84f0b5eda69bc69f03cb5c24`  
		Last Modified: Tue, 07 Jan 2025 07:09:14 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1ddda351657531159618bf230a5095d1db2a3ab53a8ef428f3c97a24168783`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:b56f57d3c345198d50b4f417b5a2cf570f28c1af31c0689cc9564b9a0e4267af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 KB (188424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64436b8673609b7502ac0cde578248704a53a2f342e3fe7d3a9c280ca0a16e43`

```dockerfile
```

-	Layers:
	-	`sha256:c51cf8033267067c13ee1ad51fda4b7233f140962f2432a72592909a84e3a2f5`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 174.2 KB (174240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcf56cf60418af47370ec7e6e57b3227568605665e3680e9e3a3c9c6e4e62cba`  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; ppc64le

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
		Last Modified: Tue, 07 Jan 2025 06:13:14 GMT  
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

### `registry:2` - unknown; unknown

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
		Size: 172.3 KB (172267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e35566a60897fb71a0d00872e6560d4adcaed4c9db615a85aab2558ccdd0b41`  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:51e058f2ed6c99da7f064e2edd532a25f4e131452d3c38753e3f70c1abeab583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9662898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d323e8994059f531daad4e5b537ab4686d057a5e1ce7048a9a3a7a03cd45030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-s390x.tar.gz / # buildkit
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
	-	`sha256:3f361b0906ea16e3dece69ee08f2757263eec429d79816947474341b7bb78cda`  
		Last Modified: Tue, 07 Jan 2025 02:33:55 GMT  
		Size: 3.2 MB (3221764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa30bcca2667fd92ed4f05b233be5f3923c7bf4068e427e55e80c69accae8cc7`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 280.5 KB (280502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d01416ada54fdf42e0f8038487e81d3ca6644e614aec672200df5b19fff00b`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d403d2dd580732e316a0e33a62b41c5d9cf37426bac4861e6fdfee7b666318`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe06d437b66f6a4cc177bb0d90eb1b42a6dc4eb63c63ff204588f61dd53c06a`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:b8e44d226fbf5a75f7f57602fe57366f47830fd02d3059763c84e569b07f1875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 KB (186298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a5de63d743bd096ef313f0e864cc7468613a4d657916edb2d9bce42a1c9030`

```dockerfile
```

-	Layers:
	-	`sha256:292f3c534f05732a64699849e73e36e51a2f31666c23e5ce7ce7352efcb992a9`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 172.2 KB (172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90cd775f6b7a08fefd088bdf59a7baa32f9431356a7b99503e3bc9b0707ff855`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8`

```console
$ docker pull registry@sha256:26f7266535a3a1dae81e137ba4935c59d96e7bb4b700f64e4af8959ca5ab0419
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
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
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
$ docker pull registry@sha256:9126ddb9b38b2265550e19f0240941a7118b5c620b7561338830de10f9963db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9201788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44abcbb25e569ce7af153a0dacc3e8071eee28693c2f5cae1be010ae314a7aff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-armv7.tar.gz / # buildkit
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
	-	`sha256:52e1a0d0bc554ff1294b79e52982946141f0dbe774dd603e745e91fa95cbdcc0`  
		Size: 2.9 MB (2904510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00e99f059306c5402b4ded95e14a270a824d4046c3afce7ddf45e4eee26102a`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 279.5 KB (279477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a29bd9d7fda548e4391ecbf347c7005f5d6bf0924f75cf1e9db23fd9ffb372d`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf2211f7dd108ea925e6711fb7c6eb5b5d585daba27d80e0959797ef413bd6d`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90dcac0c0f3a1067c4e16107f6b510984601b4d0fc54416356fe6146b745b13`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:318421972eaee19efeda0906a3aee9306fac431b3f50064b33f118dc18771ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 KB (188374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a335c7e70e90b941d4c2ae8df80a015fbf11300b06ba6648736b76227d2917c`

```dockerfile
```

-	Layers:
	-	`sha256:fd7824ae74a43ef109d829b530d3f102c52e1b383289db4d500989c60673d068`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 174.2 KB (174220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392edc5795705d1b0fa57d8865fe41531ca9467fd9ae58f6ad3f23545649c8df`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:9c833162b2eece5355ceb22acd599d2524cc6486f59c545583f4958816da0657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9444451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f5db491c361ca1e645859af99f3b172a2ac3ac1b9896dcf3ef352036deaf96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
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
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de214b2e86deccd7ec891d7639ec311ffe0367fb8514cbac3837f5ef085f774e`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 281.7 KB (281703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9b3e296f121ec56f918ca09de97ee071efc86ad29dcc854d0549d2697e9b18`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 5.8 MB (5824732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203af9cbfb3f6d2622303f23f9c4eedb0ebef36e84f0b5eda69bc69f03cb5c24`  
		Last Modified: Tue, 07 Jan 2025 07:09:14 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1ddda351657531159618bf230a5095d1db2a3ab53a8ef428f3c97a24168783`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:b56f57d3c345198d50b4f417b5a2cf570f28c1af31c0689cc9564b9a0e4267af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 KB (188424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64436b8673609b7502ac0cde578248704a53a2f342e3fe7d3a9c280ca0a16e43`

```dockerfile
```

-	Layers:
	-	`sha256:c51cf8033267067c13ee1ad51fda4b7233f140962f2432a72592909a84e3a2f5`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 174.2 KB (174240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcf56cf60418af47370ec7e6e57b3227568605665e3680e9e3a3c9c6e4e62cba`  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; ppc64le

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
		Last Modified: Tue, 07 Jan 2025 06:13:14 GMT  
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

### `registry:2.8` - unknown; unknown

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
		Size: 172.3 KB (172267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e35566a60897fb71a0d00872e6560d4adcaed4c9db615a85aab2558ccdd0b41`  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:51e058f2ed6c99da7f064e2edd532a25f4e131452d3c38753e3f70c1abeab583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9662898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d323e8994059f531daad4e5b537ab4686d057a5e1ce7048a9a3a7a03cd45030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-s390x.tar.gz / # buildkit
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
	-	`sha256:3f361b0906ea16e3dece69ee08f2757263eec429d79816947474341b7bb78cda`  
		Last Modified: Tue, 07 Jan 2025 02:33:55 GMT  
		Size: 3.2 MB (3221764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa30bcca2667fd92ed4f05b233be5f3923c7bf4068e427e55e80c69accae8cc7`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 280.5 KB (280502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d01416ada54fdf42e0f8038487e81d3ca6644e614aec672200df5b19fff00b`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d403d2dd580732e316a0e33a62b41c5d9cf37426bac4861e6fdfee7b666318`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe06d437b66f6a4cc177bb0d90eb1b42a6dc4eb63c63ff204588f61dd53c06a`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:b8e44d226fbf5a75f7f57602fe57366f47830fd02d3059763c84e569b07f1875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 KB (186298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a5de63d743bd096ef313f0e864cc7468613a4d657916edb2d9bce42a1c9030`

```dockerfile
```

-	Layers:
	-	`sha256:292f3c534f05732a64699849e73e36e51a2f31666c23e5ce7ce7352efcb992a9`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 172.2 KB (172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90cd775f6b7a08fefd088bdf59a7baa32f9431356a7b99503e3bc9b0707ff855`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8.3`

```console
$ docker pull registry@sha256:26f7266535a3a1dae81e137ba4935c59d96e7bb4b700f64e4af8959ca5ab0419
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
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
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
$ docker pull registry@sha256:9126ddb9b38b2265550e19f0240941a7118b5c620b7561338830de10f9963db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9201788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44abcbb25e569ce7af153a0dacc3e8071eee28693c2f5cae1be010ae314a7aff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-armv7.tar.gz / # buildkit
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
	-	`sha256:52e1a0d0bc554ff1294b79e52982946141f0dbe774dd603e745e91fa95cbdcc0`  
		Size: 2.9 MB (2904510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00e99f059306c5402b4ded95e14a270a824d4046c3afce7ddf45e4eee26102a`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 279.5 KB (279477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a29bd9d7fda548e4391ecbf347c7005f5d6bf0924f75cf1e9db23fd9ffb372d`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf2211f7dd108ea925e6711fb7c6eb5b5d585daba27d80e0959797ef413bd6d`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90dcac0c0f3a1067c4e16107f6b510984601b4d0fc54416356fe6146b745b13`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:318421972eaee19efeda0906a3aee9306fac431b3f50064b33f118dc18771ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 KB (188374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a335c7e70e90b941d4c2ae8df80a015fbf11300b06ba6648736b76227d2917c`

```dockerfile
```

-	Layers:
	-	`sha256:fd7824ae74a43ef109d829b530d3f102c52e1b383289db4d500989c60673d068`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 174.2 KB (174220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392edc5795705d1b0fa57d8865fe41531ca9467fd9ae58f6ad3f23545649c8df`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:9c833162b2eece5355ceb22acd599d2524cc6486f59c545583f4958816da0657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9444451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f5db491c361ca1e645859af99f3b172a2ac3ac1b9896dcf3ef352036deaf96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
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
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de214b2e86deccd7ec891d7639ec311ffe0367fb8514cbac3837f5ef085f774e`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 281.7 KB (281703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9b3e296f121ec56f918ca09de97ee071efc86ad29dcc854d0549d2697e9b18`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 5.8 MB (5824732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203af9cbfb3f6d2622303f23f9c4eedb0ebef36e84f0b5eda69bc69f03cb5c24`  
		Last Modified: Tue, 07 Jan 2025 07:09:14 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1ddda351657531159618bf230a5095d1db2a3ab53a8ef428f3c97a24168783`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:b56f57d3c345198d50b4f417b5a2cf570f28c1af31c0689cc9564b9a0e4267af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 KB (188424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64436b8673609b7502ac0cde578248704a53a2f342e3fe7d3a9c280ca0a16e43`

```dockerfile
```

-	Layers:
	-	`sha256:c51cf8033267067c13ee1ad51fda4b7233f140962f2432a72592909a84e3a2f5`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 174.2 KB (174240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcf56cf60418af47370ec7e6e57b3227568605665e3680e9e3a3c9c6e4e62cba`  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; ppc64le

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
		Last Modified: Tue, 07 Jan 2025 06:13:14 GMT  
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

### `registry:2.8.3` - unknown; unknown

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
		Size: 172.3 KB (172267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e35566a60897fb71a0d00872e6560d4adcaed4c9db615a85aab2558ccdd0b41`  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:51e058f2ed6c99da7f064e2edd532a25f4e131452d3c38753e3f70c1abeab583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9662898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d323e8994059f531daad4e5b537ab4686d057a5e1ce7048a9a3a7a03cd45030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-s390x.tar.gz / # buildkit
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
	-	`sha256:3f361b0906ea16e3dece69ee08f2757263eec429d79816947474341b7bb78cda`  
		Last Modified: Tue, 07 Jan 2025 02:33:55 GMT  
		Size: 3.2 MB (3221764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa30bcca2667fd92ed4f05b233be5f3923c7bf4068e427e55e80c69accae8cc7`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 280.5 KB (280502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d01416ada54fdf42e0f8038487e81d3ca6644e614aec672200df5b19fff00b`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d403d2dd580732e316a0e33a62b41c5d9cf37426bac4861e6fdfee7b666318`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe06d437b66f6a4cc177bb0d90eb1b42a6dc4eb63c63ff204588f61dd53c06a`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:b8e44d226fbf5a75f7f57602fe57366f47830fd02d3059763c84e569b07f1875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 KB (186298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a5de63d743bd096ef313f0e864cc7468613a4d657916edb2d9bce42a1c9030`

```dockerfile
```

-	Layers:
	-	`sha256:292f3c534f05732a64699849e73e36e51a2f31666c23e5ce7ce7352efcb992a9`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 172.2 KB (172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90cd775f6b7a08fefd088bdf59a7baa32f9431356a7b99503e3bc9b0707ff855`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0-rc.2`

```console
$ docker pull registry@sha256:9bfb6bf1c817f0c835206fbaed11ced7754587abe40bff738ba9c3ca7f6dd25b
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
		Last Modified: Tue, 07 Jan 2025 06:42:03 GMT  
		Size: 280.3 KB (280338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578b480e2a41b87ba4145aed70a4a30813e67b2b7c033cf1fc5575cf2272866d`  
		Size: 13.5 MB (13508626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0767c98b9e60aa404ec1339b5ab8f6433e7208b124047d04379ea82a128f77fd`  
		Last Modified: Tue, 07 Jan 2025 06:42:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4913fea00606a4171313c83c3292264df13ff04985d55057cbd8e560171b73a`  
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
$ docker pull registry@sha256:25e4484525fde220e2e0217265a057ecbcddcd88e99f39070ae16db17531c726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16871399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff681a69e111e7d7eb2eb8e071a30f1db23a6e319237ab6da906f9d76f2fcd3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
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
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53369145b61506ac256a77458c81613de9e873072eb9392b09431243ceb0de89`  
		Last Modified: Tue, 07 Jan 2025 06:19:28 GMT  
		Size: 279.5 KB (279502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747afaf017f5320f544b2069bb60f50a6459524a26f08bcce1d5bd3826c7ebb3`  
		Last Modified: Tue, 07 Jan 2025 06:19:28 GMT  
		Size: 13.5 MB (13498045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb56ad63f294f10b1ce125707ea1a5246682ddd2a115eb0076b160b3624b44be`  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7a4b72f7ffcf308aac14e81916b961ee83b33ce45b23de6072cf032b2d9647`  
		Last Modified: Tue, 07 Jan 2025 06:19:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:9716a073904a91dfa301fb8fdf7c160620c1ede50c949c5d2b49ab8125c825f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 KB (274743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9e72b7a75473dc9a1f97c55bdb51dfb89221190fce5bbca609bdef1be74e81`

```dockerfile
```

-	Layers:
	-	`sha256:7bcd04f956e6b1cb1dbe1160173e84bf31d234dd7d712a9e1a6ab2657c53e0be`  
		Last Modified: Tue, 07 Jan 2025 06:19:28 GMT  
		Size: 261.2 KB (261189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47863c5368857c1bf9cc4a60e3585fa35d282be1cfff14ed8e52e366d4802937`  
		Last Modified: Tue, 07 Jan 2025 06:19:27 GMT  
		Size: 13.6 KB (13554 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:3b7e980e32555ffdd19040cd1e51d7ebed77cc79197b88b6a1d24b1ef5dd9dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17546408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecbda0de7b1e0a1f6a64c2d5e02c42466f55e45711c152d11c4ed409e547915`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712339dc7afde33ea8162a86ca2a257bb3cf6faa8436da4b8d6f01a8dad2e745`  
		Last Modified: Tue, 07 Jan 2025 07:09:01 GMT  
		Size: 281.7 KB (281695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ea0f3aa45e9b6c11c43a0437d60e7dd9dabba85bd164acf9b2db4a404b7b4c`  
		Last Modified: Tue, 07 Jan 2025 07:09:01 GMT  
		Size: 13.3 MB (13281097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4405d8886c89239930e757081cda16404e54131a53a584a7be36aca909f1d672`  
		Last Modified: Tue, 07 Jan 2025 07:09:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f6925b2654835f68386bea05b65272058412fee4ac90ed4dcbd66c450a4c0c`  
		Last Modified: Tue, 07 Jan 2025 07:09:00 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:419ded70e1f3b50b0eaf4c75409a3739ad6cb0eb09342a2bf5a32e35d684527a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 KB (274769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2cac0bc0563a3ac141646d6a997d66b3bb862b7a1313095db293a6e56fba97`

```dockerfile
```

-	Layers:
	-	`sha256:248515f7066f5f5591c03c4c76f84d142c4a08f07b0c52289fa0006d9f105b3f`  
		Last Modified: Tue, 07 Jan 2025 07:09:01 GMT  
		Size: 261.2 KB (261197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e47200d5394ef91114a64cf644ed78e8c842b3fd9a1d4cd9f4077c3001ae33`  
		Last Modified: Tue, 07 Jan 2025 07:09:00 GMT  
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
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
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
		Last Modified: Fri, 06 Dec 2024 22:31:00 GMT  
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
$ docker pull registry@sha256:b9bc3a1fc0bb29a6b00f6448e3cc4aefa153f4500387c14b2e00507c4cec7982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17585172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e929d8f2157f9e27a56c96b4a00a9668d5229ef55ca17126f046be7ead64279`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c80aba2f3c52b257c2a9bd1f1926ff778f3cdf5ace50a9adf1eaed5a22d7a96`  
		Last Modified: Tue, 07 Jan 2025 06:18:07 GMT  
		Size: 280.5 KB (280499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400d7250a11f8f61411a06aac67fa57a749e06fa2c6568cf32e8b261e1997642`  
		Last Modified: Tue, 07 Jan 2025 06:18:07 GMT  
		Size: 13.8 MB (13844614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db684da2708360cb692657477e8a078a1861cb49e8a1546652e4c55cfe6bb6b9`  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645c05e7c60f63466b570b2d36350651fbabda9443caca005404d399887de535`  
		Last Modified: Tue, 07 Jan 2025 06:18:07 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:0054769c9f41b6ff3362c806c7872663a160192e5e8ece37987b1a2c063fb11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 KB (272705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead178280c57710781b7a6ddf7dd6436f8cca09c24c48525372378376c73c72f`

```dockerfile
```

-	Layers:
	-	`sha256:84a4fd0e17a8bd21ab1d51ea2b3fbe74f6f2bdae33bc4f2450cffd9d4272dd69`  
		Last Modified: Tue, 07 Jan 2025 06:18:07 GMT  
		Size: 259.2 KB (259216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b139f9214e3701ec0176750467773e30d02cca470456a6d3063535ba8610045f`  
		Size: 13.5 KB (13489 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:26f7266535a3a1dae81e137ba4935c59d96e7bb4b700f64e4af8959ca5ab0419
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
		Last Modified: Tue, 07 Jan 2025 03:15:27 GMT  
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
$ docker pull registry@sha256:9126ddb9b38b2265550e19f0240941a7118b5c620b7561338830de10f9963db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9201788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44abcbb25e569ce7af153a0dacc3e8071eee28693c2f5cae1be010ae314a7aff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-armv7.tar.gz / # buildkit
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
	-	`sha256:52e1a0d0bc554ff1294b79e52982946141f0dbe774dd603e745e91fa95cbdcc0`  
		Size: 2.9 MB (2904510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00e99f059306c5402b4ded95e14a270a824d4046c3afce7ddf45e4eee26102a`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 279.5 KB (279477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a29bd9d7fda548e4391ecbf347c7005f5d6bf0924f75cf1e9db23fd9ffb372d`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf2211f7dd108ea925e6711fb7c6eb5b5d585daba27d80e0959797ef413bd6d`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90dcac0c0f3a1067c4e16107f6b510984601b4d0fc54416356fe6146b745b13`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:318421972eaee19efeda0906a3aee9306fac431b3f50064b33f118dc18771ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 KB (188374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a335c7e70e90b941d4c2ae8df80a015fbf11300b06ba6648736b76227d2917c`

```dockerfile
```

-	Layers:
	-	`sha256:fd7824ae74a43ef109d829b530d3f102c52e1b383289db4d500989c60673d068`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 174.2 KB (174220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392edc5795705d1b0fa57d8865fe41531ca9467fd9ae58f6ad3f23545649c8df`  
		Last Modified: Tue, 07 Jan 2025 06:19:46 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:9c833162b2eece5355ceb22acd599d2524cc6486f59c545583f4958816da0657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9444451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f5db491c361ca1e645859af99f3b172a2ac3ac1b9896dcf3ef352036deaf96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
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
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de214b2e86deccd7ec891d7639ec311ffe0367fb8514cbac3837f5ef085f774e`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 281.7 KB (281703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9b3e296f121ec56f918ca09de97ee071efc86ad29dcc854d0549d2697e9b18`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 5.8 MB (5824732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203af9cbfb3f6d2622303f23f9c4eedb0ebef36e84f0b5eda69bc69f03cb5c24`  
		Last Modified: Tue, 07 Jan 2025 07:09:14 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1ddda351657531159618bf230a5095d1db2a3ab53a8ef428f3c97a24168783`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:b56f57d3c345198d50b4f417b5a2cf570f28c1af31c0689cc9564b9a0e4267af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 KB (188424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64436b8673609b7502ac0cde578248704a53a2f342e3fe7d3a9c280ca0a16e43`

```dockerfile
```

-	Layers:
	-	`sha256:c51cf8033267067c13ee1ad51fda4b7233f140962f2432a72592909a84e3a2f5`  
		Last Modified: Tue, 07 Jan 2025 07:09:15 GMT  
		Size: 174.2 KB (174240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcf56cf60418af47370ec7e6e57b3227568605665e3680e9e3a3c9c6e4e62cba`  
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
		Last Modified: Tue, 07 Jan 2025 06:13:14 GMT  
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
		Size: 172.3 KB (172267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e35566a60897fb71a0d00872e6560d4adcaed4c9db615a85aab2558ccdd0b41`  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:51e058f2ed6c99da7f064e2edd532a25f4e131452d3c38753e3f70c1abeab583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9662898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d323e8994059f531daad4e5b537ab4686d057a5e1ce7048a9a3a7a03cd45030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.10-s390x.tar.gz / # buildkit
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
	-	`sha256:3f361b0906ea16e3dece69ee08f2757263eec429d79816947474341b7bb78cda`  
		Last Modified: Tue, 07 Jan 2025 02:33:55 GMT  
		Size: 3.2 MB (3221764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa30bcca2667fd92ed4f05b233be5f3923c7bf4068e427e55e80c69accae8cc7`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 280.5 KB (280502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d01416ada54fdf42e0f8038487e81d3ca6644e614aec672200df5b19fff00b`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d403d2dd580732e316a0e33a62b41c5d9cf37426bac4861e6fdfee7b666318`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe06d437b66f6a4cc177bb0d90eb1b42a6dc4eb63c63ff204588f61dd53c06a`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:b8e44d226fbf5a75f7f57602fe57366f47830fd02d3059763c84e569b07f1875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 KB (186298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a5de63d743bd096ef313f0e864cc7468613a4d657916edb2d9bce42a1c9030`

```dockerfile
```

-	Layers:
	-	`sha256:292f3c534f05732a64699849e73e36e51a2f31666c23e5ce7ce7352efcb992a9`  
		Last Modified: Tue, 07 Jan 2025 06:18:40 GMT  
		Size: 172.2 KB (172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90cd775f6b7a08fefd088bdf59a7baa32f9431356a7b99503e3bc9b0707ff855`  
		Last Modified: Tue, 07 Jan 2025 06:18:41 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json
