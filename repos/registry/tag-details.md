<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-rc.2`](#registry300-rc2)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:319881be2ee9e345d5837d15842a04268de6a139e23be42654fc7664fc6eaf52
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
$ docker pull registry@sha256:57350583fba19eaab4b4632aafa1537483a390dfd29c5b37c9d59e2467ce1b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282bd1664cf1fccccf9f225118e31f9352f1f93e4d0ad485c92e74ec6b11ebd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
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
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6afea20d55c46e60901e594cad0651da46b7437cf42a3c27e52d5bd37320165`  
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 295.7 KB (295665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f4e00e7d3c5ea061e25a18ba6127f79930efbbd3f3deb59c272ca0d6de23c3`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 6.4 MB (6403790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665375f3730237f2109d398104a2072e38166ecf5d8316b1464f8a005146384e`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9959184a302f6f95d8be97229fb31def6700b1895b1ee92090129b60e6567820`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:2ed78d67c727bcce149533b0ac69e59a62b8c16edd0f113f0b81d8cad414adf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 KB (194126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7686a99322a57149ff0aab40827d9abaf011fdbda972d8817e04f5d98530d01`

```dockerfile
```

-	Layers:
	-	`sha256:a7f9721296093c0999458f91d6176f8cbf9ad755f89877da06031de4b3e9cb69`  
		Last Modified: Wed, 15 Jan 2025 00:10:17 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c800ea38a09dbe46c3cb07f4498fcb316134e44440ee5941a2374c41d0eac9d`  
		Last Modified: Wed, 15 Jan 2025 03:19:35 GMT  
		Size: 14.1 KB (14064 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:7f9dcbf2fb5296dacd3c0113fbbd5ab2d5e5a95900060c7b1fdbd4001713ade0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9480838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd9a6e975ec81b8ae82571e63e99f4a8775c1f2e1c78e382d1ad786b4ac1fe7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-armhf.tar.gz / # buildkit
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
	-	`sha256:803cf02755db9f4dbb0d52a3ff280052dd523cdfdb9e9be6494b4edd548d6dc6`  
		Last Modified: Wed, 08 Jan 2025 17:24:20 GMT  
		Size: 3.2 MB (3159977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7840dcb6e03dd1709b54c0be0dd05dab1e1332a39708dee9eaaf7dbb8820ce9`  
		Last Modified: Wed, 15 Jan 2025 02:37:53 GMT  
		Size: 296.2 KB (296164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551f60a571f5e22a678c2812142fcecb7a4ca62e3bdb99e32bc8962583208349`  
		Last Modified: Wed, 15 Jan 2025 02:37:54 GMT  
		Size: 6.0 MB (6024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad6dfdda7a01c82c1ae649bbf1f80fe5126a5c22559167fe5975356c7949341`  
		Last Modified: Wed, 15 Jan 2025 02:37:53 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786e8db11e0fb9efe89d614a159662b1d4bb3bb45662b6b7ad6c05f439e8eed7`  
		Last Modified: Tue, 07 Jan 2025 07:43:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:087a16847794451af13a9f72c4eb87727c0f690e715bc2cab96758309ce3bca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bdb2f6d7b8b7e511805bbf68d57fe69ec8922ff6d64628aff9a1ed11c9d790`

```dockerfile
```

-	Layers:
	-	`sha256:5fb180ceda25c616d72b29cbf15eed44aedc427e6b45c16b7b83c1f9ede99b15`  
		Last Modified: Wed, 15 Jan 2025 02:37:54 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:574610c8eafc5c3961b7fc8229597d5ae88733a8283fc835d32d41d396f8f546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9225758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f9c806796de21a52dbafc030a4dfa0e913746772b85686d43eb796402fef29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-armv7.tar.gz / # buildkit
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
	-	`sha256:e1b4e22e09e012565a243e582da1a0c5d1de7318c191f19a95a4e6e5e8535be8`  
		Last Modified: Wed, 08 Jan 2025 17:34:42 GMT  
		Size: 2.9 MB (2912794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7361fdbbdb9dd007424891fe5603438ddf1db7c562c4e853d78827f54a26f257`  
		Last Modified: Tue, 14 Jan 2025 21:31:26 GMT  
		Size: 295.2 KB (295165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca4f35222130d5ce0cc4968ce9ecfbb0e1f3988a0db13c95fa0b7a6a2876df4`  
		Last Modified: Tue, 14 Jan 2025 21:31:26 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8c2cb058a9769352b2455ed4001792d88acd516960469d0092b7c126eebdec`  
		Last Modified: Tue, 14 Jan 2025 21:31:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34401837030ebc7227878bae338335617113254bf4208048748a38326150786`  
		Last Modified: Wed, 15 Jan 2025 00:10:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:6d9590249cd4a04e2c96c7451ec5fbfc2cd5ce5dfcaf4f54d27a6d4fe846333d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6f0f8b0819f6d3a9963ca63d53ea51adc9629f0eb7b9b7ca73f0ac5dd2350f`

```dockerfile
```

-	Layers:
	-	`sha256:a3661c5da3fdd2b47d824fe3bda6c618a50daff424f25ece3c38d7c376f6d9a0`  
		Last Modified: Wed, 15 Jan 2025 03:19:18 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d73d4b6eaf8501e4340b60842355e671fe7ced474835e36951c93ff327af82`  
		Last Modified: Wed, 15 Jan 2025 02:37:55 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1674a8dd758ef390d16fdb58be6646005a0154606bba8bb41e5ddf2b40b3fcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8876582179f0fe21dad0d58f5cf820017819161bb786ea43e9863beeef95f70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
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
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Wed, 08 Jan 2025 17:24:31 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0726ca172d8b26fcb657230174e78246e0d10a453d5eb068720f3e309c422a04`  
		Last Modified: Tue, 14 Jan 2025 20:38:59 GMT  
		Size: 297.8 KB (297823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b7b7187cb358b4974cf0245aecab9fb00f528bbdebf66fb63e8da2a74456e7`  
		Last Modified: Tue, 14 Jan 2025 20:37:00 GMT  
		Size: 5.8 MB (5824731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14fe80572add96e41c3ef0b859c81f81c9662078baba85162bf121af0337176`  
		Last Modified: Tue, 14 Jan 2025 20:39:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa909d97427642d4f9aa7249f3c06087e667e40b74753a4cf27ab3005250c970`  
		Last Modified: Tue, 14 Jan 2025 20:37:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:f98e543c1aced03689c60d626e1b8501c1568f43156afe7930902e2f006de0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3212b1b26d5836c0dec2c1d174a74b0aacc40a44767d5a706fbb4fb89c14358`

```dockerfile
```

-	Layers:
	-	`sha256:d19202c96c707295b0022d580dd5187da04580f93059ed006d1cf32e415eef49`  
		Last Modified: Wed, 15 Jan 2025 10:46:15 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682fd9916c4c71c5c7c15151a03509a7346c9efc018d7c2a67251b8ff095072b`  
		Last Modified: Wed, 15 Jan 2025 00:10:18 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:60619ec298638d377e8631927d55b84c9ea86ac2e1303de28a65b2e20ae4ec85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9347330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f8f1595a0733b662963c070cd0c8c3d594720b77ae00d099913b1f37110ea7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-ppc64le.tar.gz / # buildkit
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
	-	`sha256:6259f25643973acaf5182679ac24f10e7bcb8be462646ba81a87b013ec80c9ed`  
		Last Modified: Wed, 08 Jan 2025 17:25:55 GMT  
		Size: 3.4 MB (3359277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b59fd69e39afe9b69b4ed12982c3fcc9b36a7453cf9ae8e34edbea633db64c`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 298.3 KB (298253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84815ad061a37d997ef0467524fb1782e217752eb2017f61101df2d66fc508ad`  
		Last Modified: Wed, 15 Jan 2025 03:19:20 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e108bb20672a34158c362d7a824852b67b1055b96032e540cd8aeebae409356`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9bb1e1a56c8509c23cf94332c160707790aaaa8d1cddd92182964da536c538`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:0d21931696fa83e2e6e170f48375ad62ea48db603439ac45034b84568b5c2d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 KB (192255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf187220c58e23bd5f1b27074abc712ca3e537a502ea51a55675d6601175ae3`

```dockerfile
```

-	Layers:
	-	`sha256:129c8dd66a4381ad34fac5989711b1a956eddd716be30f64e5b2ea3c1074d767`  
		Last Modified: Wed, 15 Jan 2025 02:37:56 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7be9132674cb879c894e8b20f9735919f07228698009969b9d40db2a7d2a2f`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 14.1 KB (14110 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:126b6d230d49f8167af80d517a2e407ef5fdd44a5409ff3bf6612b0072f44054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9688649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5c6a4a61291d9496e34bac48ab1dacebd4739321c6cfea44f57bf7d70d0ec4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-s390x.tar.gz / # buildkit
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
	-	`sha256:552c3aaa08429935d8dfef69ca747244fe854badcb537563677169e2f2ebdde8`  
		Last Modified: Wed, 08 Jan 2025 17:27:28 GMT  
		Size: 3.2 MB (3231849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088de0189be3b501d83cd78bb736e152eb9c879fee282f9dbc136e3d59ea1ee5`  
		Last Modified: Wed, 15 Jan 2025 02:37:57 GMT  
		Size: 296.2 KB (296168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95abefa83c834e15d00de84079607a49184ee2125795798f287f955f45d84d`  
		Last Modified: Wed, 15 Jan 2025 00:10:20 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a765923fab0e8bd0e0e5273d4883d868210b55d31fa8e102409189f093e461b8`  
		Last Modified: Wed, 15 Jan 2025 10:41:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea1c9c51d488f6c8ef15fdc1c88881262a91a6c731e4397e4402b158a52b107`  
		Last Modified: Wed, 15 Jan 2025 00:10:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:ac84eda0399f81593ee60869efeeafd4c44aeb92e4d4f8aff7d74c9e5338f9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 KB (192176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4cf9615766470533a5207df9fcbfafdce5121030d02d0c7d5db4ecb7c3bbc3`

```dockerfile
```

-	Layers:
	-	`sha256:4f5fbbf076e745d22a8e41a999227a6b751adda40e7a3e98afa1abac119c787a`  
		Last Modified: Wed, 15 Jan 2025 02:37:57 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae1a54ed652d75d520f8eb65aebea6ab6549b447255c286084e321dc29cc126`  
		Last Modified: Wed, 15 Jan 2025 00:10:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8`

```console
$ docker pull registry@sha256:319881be2ee9e345d5837d15842a04268de6a139e23be42654fc7664fc6eaf52
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
$ docker pull registry@sha256:57350583fba19eaab4b4632aafa1537483a390dfd29c5b37c9d59e2467ce1b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282bd1664cf1fccccf9f225118e31f9352f1f93e4d0ad485c92e74ec6b11ebd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
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
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6afea20d55c46e60901e594cad0651da46b7437cf42a3c27e52d5bd37320165`  
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 295.7 KB (295665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f4e00e7d3c5ea061e25a18ba6127f79930efbbd3f3deb59c272ca0d6de23c3`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 6.4 MB (6403790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665375f3730237f2109d398104a2072e38166ecf5d8316b1464f8a005146384e`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9959184a302f6f95d8be97229fb31def6700b1895b1ee92090129b60e6567820`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:2ed78d67c727bcce149533b0ac69e59a62b8c16edd0f113f0b81d8cad414adf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 KB (194126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7686a99322a57149ff0aab40827d9abaf011fdbda972d8817e04f5d98530d01`

```dockerfile
```

-	Layers:
	-	`sha256:a7f9721296093c0999458f91d6176f8cbf9ad755f89877da06031de4b3e9cb69`  
		Last Modified: Wed, 15 Jan 2025 00:10:17 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c800ea38a09dbe46c3cb07f4498fcb316134e44440ee5941a2374c41d0eac9d`  
		Last Modified: Wed, 15 Jan 2025 03:19:35 GMT  
		Size: 14.1 KB (14064 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:7f9dcbf2fb5296dacd3c0113fbbd5ab2d5e5a95900060c7b1fdbd4001713ade0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9480838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd9a6e975ec81b8ae82571e63e99f4a8775c1f2e1c78e382d1ad786b4ac1fe7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-armhf.tar.gz / # buildkit
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
	-	`sha256:803cf02755db9f4dbb0d52a3ff280052dd523cdfdb9e9be6494b4edd548d6dc6`  
		Last Modified: Wed, 08 Jan 2025 17:24:20 GMT  
		Size: 3.2 MB (3159977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7840dcb6e03dd1709b54c0be0dd05dab1e1332a39708dee9eaaf7dbb8820ce9`  
		Last Modified: Wed, 15 Jan 2025 02:37:53 GMT  
		Size: 296.2 KB (296164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551f60a571f5e22a678c2812142fcecb7a4ca62e3bdb99e32bc8962583208349`  
		Last Modified: Wed, 15 Jan 2025 02:37:54 GMT  
		Size: 6.0 MB (6024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad6dfdda7a01c82c1ae649bbf1f80fe5126a5c22559167fe5975356c7949341`  
		Last Modified: Wed, 15 Jan 2025 02:37:53 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786e8db11e0fb9efe89d614a159662b1d4bb3bb45662b6b7ad6c05f439e8eed7`  
		Last Modified: Tue, 07 Jan 2025 07:43:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:087a16847794451af13a9f72c4eb87727c0f690e715bc2cab96758309ce3bca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bdb2f6d7b8b7e511805bbf68d57fe69ec8922ff6d64628aff9a1ed11c9d790`

```dockerfile
```

-	Layers:
	-	`sha256:5fb180ceda25c616d72b29cbf15eed44aedc427e6b45c16b7b83c1f9ede99b15`  
		Last Modified: Wed, 15 Jan 2025 02:37:54 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:574610c8eafc5c3961b7fc8229597d5ae88733a8283fc835d32d41d396f8f546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9225758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f9c806796de21a52dbafc030a4dfa0e913746772b85686d43eb796402fef29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-armv7.tar.gz / # buildkit
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
	-	`sha256:e1b4e22e09e012565a243e582da1a0c5d1de7318c191f19a95a4e6e5e8535be8`  
		Last Modified: Wed, 08 Jan 2025 17:34:42 GMT  
		Size: 2.9 MB (2912794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7361fdbbdb9dd007424891fe5603438ddf1db7c562c4e853d78827f54a26f257`  
		Last Modified: Tue, 14 Jan 2025 21:31:26 GMT  
		Size: 295.2 KB (295165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca4f35222130d5ce0cc4968ce9ecfbb0e1f3988a0db13c95fa0b7a6a2876df4`  
		Last Modified: Tue, 14 Jan 2025 21:31:26 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8c2cb058a9769352b2455ed4001792d88acd516960469d0092b7c126eebdec`  
		Last Modified: Tue, 14 Jan 2025 21:31:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34401837030ebc7227878bae338335617113254bf4208048748a38326150786`  
		Last Modified: Wed, 15 Jan 2025 00:10:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:6d9590249cd4a04e2c96c7451ec5fbfc2cd5ce5dfcaf4f54d27a6d4fe846333d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6f0f8b0819f6d3a9963ca63d53ea51adc9629f0eb7b9b7ca73f0ac5dd2350f`

```dockerfile
```

-	Layers:
	-	`sha256:a3661c5da3fdd2b47d824fe3bda6c618a50daff424f25ece3c38d7c376f6d9a0`  
		Last Modified: Wed, 15 Jan 2025 03:19:18 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d73d4b6eaf8501e4340b60842355e671fe7ced474835e36951c93ff327af82`  
		Last Modified: Wed, 15 Jan 2025 02:37:55 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1674a8dd758ef390d16fdb58be6646005a0154606bba8bb41e5ddf2b40b3fcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8876582179f0fe21dad0d58f5cf820017819161bb786ea43e9863beeef95f70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
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
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Wed, 08 Jan 2025 17:24:31 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0726ca172d8b26fcb657230174e78246e0d10a453d5eb068720f3e309c422a04`  
		Last Modified: Tue, 14 Jan 2025 20:38:59 GMT  
		Size: 297.8 KB (297823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b7b7187cb358b4974cf0245aecab9fb00f528bbdebf66fb63e8da2a74456e7`  
		Last Modified: Tue, 14 Jan 2025 20:37:00 GMT  
		Size: 5.8 MB (5824731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14fe80572add96e41c3ef0b859c81f81c9662078baba85162bf121af0337176`  
		Last Modified: Tue, 14 Jan 2025 20:39:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa909d97427642d4f9aa7249f3c06087e667e40b74753a4cf27ab3005250c970`  
		Last Modified: Tue, 14 Jan 2025 20:37:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:f98e543c1aced03689c60d626e1b8501c1568f43156afe7930902e2f006de0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3212b1b26d5836c0dec2c1d174a74b0aacc40a44767d5a706fbb4fb89c14358`

```dockerfile
```

-	Layers:
	-	`sha256:d19202c96c707295b0022d580dd5187da04580f93059ed006d1cf32e415eef49`  
		Last Modified: Wed, 15 Jan 2025 10:46:15 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682fd9916c4c71c5c7c15151a03509a7346c9efc018d7c2a67251b8ff095072b`  
		Last Modified: Wed, 15 Jan 2025 00:10:18 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:60619ec298638d377e8631927d55b84c9ea86ac2e1303de28a65b2e20ae4ec85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9347330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f8f1595a0733b662963c070cd0c8c3d594720b77ae00d099913b1f37110ea7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-ppc64le.tar.gz / # buildkit
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
	-	`sha256:6259f25643973acaf5182679ac24f10e7bcb8be462646ba81a87b013ec80c9ed`  
		Last Modified: Wed, 08 Jan 2025 17:25:55 GMT  
		Size: 3.4 MB (3359277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b59fd69e39afe9b69b4ed12982c3fcc9b36a7453cf9ae8e34edbea633db64c`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 298.3 KB (298253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84815ad061a37d997ef0467524fb1782e217752eb2017f61101df2d66fc508ad`  
		Last Modified: Wed, 15 Jan 2025 03:19:20 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e108bb20672a34158c362d7a824852b67b1055b96032e540cd8aeebae409356`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9bb1e1a56c8509c23cf94332c160707790aaaa8d1cddd92182964da536c538`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:0d21931696fa83e2e6e170f48375ad62ea48db603439ac45034b84568b5c2d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 KB (192255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf187220c58e23bd5f1b27074abc712ca3e537a502ea51a55675d6601175ae3`

```dockerfile
```

-	Layers:
	-	`sha256:129c8dd66a4381ad34fac5989711b1a956eddd716be30f64e5b2ea3c1074d767`  
		Last Modified: Wed, 15 Jan 2025 02:37:56 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7be9132674cb879c894e8b20f9735919f07228698009969b9d40db2a7d2a2f`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 14.1 KB (14110 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:126b6d230d49f8167af80d517a2e407ef5fdd44a5409ff3bf6612b0072f44054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9688649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5c6a4a61291d9496e34bac48ab1dacebd4739321c6cfea44f57bf7d70d0ec4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-s390x.tar.gz / # buildkit
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
	-	`sha256:552c3aaa08429935d8dfef69ca747244fe854badcb537563677169e2f2ebdde8`  
		Last Modified: Wed, 08 Jan 2025 17:27:28 GMT  
		Size: 3.2 MB (3231849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088de0189be3b501d83cd78bb736e152eb9c879fee282f9dbc136e3d59ea1ee5`  
		Last Modified: Wed, 15 Jan 2025 02:37:57 GMT  
		Size: 296.2 KB (296168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95abefa83c834e15d00de84079607a49184ee2125795798f287f955f45d84d`  
		Last Modified: Wed, 15 Jan 2025 00:10:20 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a765923fab0e8bd0e0e5273d4883d868210b55d31fa8e102409189f093e461b8`  
		Last Modified: Wed, 15 Jan 2025 10:41:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea1c9c51d488f6c8ef15fdc1c88881262a91a6c731e4397e4402b158a52b107`  
		Last Modified: Wed, 15 Jan 2025 00:10:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:ac84eda0399f81593ee60869efeeafd4c44aeb92e4d4f8aff7d74c9e5338f9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 KB (192176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4cf9615766470533a5207df9fcbfafdce5121030d02d0c7d5db4ecb7c3bbc3`

```dockerfile
```

-	Layers:
	-	`sha256:4f5fbbf076e745d22a8e41a999227a6b751adda40e7a3e98afa1abac119c787a`  
		Last Modified: Wed, 15 Jan 2025 02:37:57 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae1a54ed652d75d520f8eb65aebea6ab6549b447255c286084e321dc29cc126`  
		Last Modified: Wed, 15 Jan 2025 00:10:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8.3`

```console
$ docker pull registry@sha256:319881be2ee9e345d5837d15842a04268de6a139e23be42654fc7664fc6eaf52
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
$ docker pull registry@sha256:57350583fba19eaab4b4632aafa1537483a390dfd29c5b37c9d59e2467ce1b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282bd1664cf1fccccf9f225118e31f9352f1f93e4d0ad485c92e74ec6b11ebd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
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
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6afea20d55c46e60901e594cad0651da46b7437cf42a3c27e52d5bd37320165`  
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 295.7 KB (295665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f4e00e7d3c5ea061e25a18ba6127f79930efbbd3f3deb59c272ca0d6de23c3`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 6.4 MB (6403790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665375f3730237f2109d398104a2072e38166ecf5d8316b1464f8a005146384e`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9959184a302f6f95d8be97229fb31def6700b1895b1ee92090129b60e6567820`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:2ed78d67c727bcce149533b0ac69e59a62b8c16edd0f113f0b81d8cad414adf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 KB (194126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7686a99322a57149ff0aab40827d9abaf011fdbda972d8817e04f5d98530d01`

```dockerfile
```

-	Layers:
	-	`sha256:a7f9721296093c0999458f91d6176f8cbf9ad755f89877da06031de4b3e9cb69`  
		Last Modified: Wed, 15 Jan 2025 00:10:17 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c800ea38a09dbe46c3cb07f4498fcb316134e44440ee5941a2374c41d0eac9d`  
		Last Modified: Wed, 15 Jan 2025 03:19:35 GMT  
		Size: 14.1 KB (14064 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v6

```console
$ docker pull registry@sha256:7f9dcbf2fb5296dacd3c0113fbbd5ab2d5e5a95900060c7b1fdbd4001713ade0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9480838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd9a6e975ec81b8ae82571e63e99f4a8775c1f2e1c78e382d1ad786b4ac1fe7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-armhf.tar.gz / # buildkit
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
	-	`sha256:803cf02755db9f4dbb0d52a3ff280052dd523cdfdb9e9be6494b4edd548d6dc6`  
		Last Modified: Wed, 08 Jan 2025 17:24:20 GMT  
		Size: 3.2 MB (3159977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7840dcb6e03dd1709b54c0be0dd05dab1e1332a39708dee9eaaf7dbb8820ce9`  
		Last Modified: Wed, 15 Jan 2025 02:37:53 GMT  
		Size: 296.2 KB (296164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551f60a571f5e22a678c2812142fcecb7a4ca62e3bdb99e32bc8962583208349`  
		Last Modified: Wed, 15 Jan 2025 02:37:54 GMT  
		Size: 6.0 MB (6024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad6dfdda7a01c82c1ae649bbf1f80fe5126a5c22559167fe5975356c7949341`  
		Last Modified: Wed, 15 Jan 2025 02:37:53 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786e8db11e0fb9efe89d614a159662b1d4bb3bb45662b6b7ad6c05f439e8eed7`  
		Last Modified: Tue, 07 Jan 2025 07:43:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:087a16847794451af13a9f72c4eb87727c0f690e715bc2cab96758309ce3bca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bdb2f6d7b8b7e511805bbf68d57fe69ec8922ff6d64628aff9a1ed11c9d790`

```dockerfile
```

-	Layers:
	-	`sha256:5fb180ceda25c616d72b29cbf15eed44aedc427e6b45c16b7b83c1f9ede99b15`  
		Last Modified: Wed, 15 Jan 2025 02:37:54 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v7

```console
$ docker pull registry@sha256:574610c8eafc5c3961b7fc8229597d5ae88733a8283fc835d32d41d396f8f546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9225758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f9c806796de21a52dbafc030a4dfa0e913746772b85686d43eb796402fef29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-armv7.tar.gz / # buildkit
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
	-	`sha256:e1b4e22e09e012565a243e582da1a0c5d1de7318c191f19a95a4e6e5e8535be8`  
		Last Modified: Wed, 08 Jan 2025 17:34:42 GMT  
		Size: 2.9 MB (2912794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7361fdbbdb9dd007424891fe5603438ddf1db7c562c4e853d78827f54a26f257`  
		Last Modified: Tue, 14 Jan 2025 21:31:26 GMT  
		Size: 295.2 KB (295165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca4f35222130d5ce0cc4968ce9ecfbb0e1f3988a0db13c95fa0b7a6a2876df4`  
		Last Modified: Tue, 14 Jan 2025 21:31:26 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8c2cb058a9769352b2455ed4001792d88acd516960469d0092b7c126eebdec`  
		Last Modified: Tue, 14 Jan 2025 21:31:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34401837030ebc7227878bae338335617113254bf4208048748a38326150786`  
		Last Modified: Wed, 15 Jan 2025 00:10:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:6d9590249cd4a04e2c96c7451ec5fbfc2cd5ce5dfcaf4f54d27a6d4fe846333d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6f0f8b0819f6d3a9963ca63d53ea51adc9629f0eb7b9b7ca73f0ac5dd2350f`

```dockerfile
```

-	Layers:
	-	`sha256:a3661c5da3fdd2b47d824fe3bda6c618a50daff424f25ece3c38d7c376f6d9a0`  
		Last Modified: Wed, 15 Jan 2025 03:19:18 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d73d4b6eaf8501e4340b60842355e671fe7ced474835e36951c93ff327af82`  
		Last Modified: Wed, 15 Jan 2025 02:37:55 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1674a8dd758ef390d16fdb58be6646005a0154606bba8bb41e5ddf2b40b3fcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8876582179f0fe21dad0d58f5cf820017819161bb786ea43e9863beeef95f70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
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
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Wed, 08 Jan 2025 17:24:31 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0726ca172d8b26fcb657230174e78246e0d10a453d5eb068720f3e309c422a04`  
		Last Modified: Tue, 14 Jan 2025 20:38:59 GMT  
		Size: 297.8 KB (297823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b7b7187cb358b4974cf0245aecab9fb00f528bbdebf66fb63e8da2a74456e7`  
		Last Modified: Tue, 14 Jan 2025 20:37:00 GMT  
		Size: 5.8 MB (5824731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14fe80572add96e41c3ef0b859c81f81c9662078baba85162bf121af0337176`  
		Last Modified: Tue, 14 Jan 2025 20:39:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa909d97427642d4f9aa7249f3c06087e667e40b74753a4cf27ab3005250c970`  
		Last Modified: Tue, 14 Jan 2025 20:37:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:f98e543c1aced03689c60d626e1b8501c1568f43156afe7930902e2f006de0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3212b1b26d5836c0dec2c1d174a74b0aacc40a44767d5a706fbb4fb89c14358`

```dockerfile
```

-	Layers:
	-	`sha256:d19202c96c707295b0022d580dd5187da04580f93059ed006d1cf32e415eef49`  
		Last Modified: Wed, 15 Jan 2025 10:46:15 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682fd9916c4c71c5c7c15151a03509a7346c9efc018d7c2a67251b8ff095072b`  
		Last Modified: Wed, 15 Jan 2025 00:10:18 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; ppc64le

```console
$ docker pull registry@sha256:60619ec298638d377e8631927d55b84c9ea86ac2e1303de28a65b2e20ae4ec85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9347330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f8f1595a0733b662963c070cd0c8c3d594720b77ae00d099913b1f37110ea7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-ppc64le.tar.gz / # buildkit
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
	-	`sha256:6259f25643973acaf5182679ac24f10e7bcb8be462646ba81a87b013ec80c9ed`  
		Last Modified: Wed, 08 Jan 2025 17:25:55 GMT  
		Size: 3.4 MB (3359277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b59fd69e39afe9b69b4ed12982c3fcc9b36a7453cf9ae8e34edbea633db64c`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 298.3 KB (298253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84815ad061a37d997ef0467524fb1782e217752eb2017f61101df2d66fc508ad`  
		Last Modified: Wed, 15 Jan 2025 03:19:20 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e108bb20672a34158c362d7a824852b67b1055b96032e540cd8aeebae409356`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9bb1e1a56c8509c23cf94332c160707790aaaa8d1cddd92182964da536c538`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:0d21931696fa83e2e6e170f48375ad62ea48db603439ac45034b84568b5c2d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 KB (192255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf187220c58e23bd5f1b27074abc712ca3e537a502ea51a55675d6601175ae3`

```dockerfile
```

-	Layers:
	-	`sha256:129c8dd66a4381ad34fac5989711b1a956eddd716be30f64e5b2ea3c1074d767`  
		Last Modified: Wed, 15 Jan 2025 02:37:56 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7be9132674cb879c894e8b20f9735919f07228698009969b9d40db2a7d2a2f`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 14.1 KB (14110 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:126b6d230d49f8167af80d517a2e407ef5fdd44a5409ff3bf6612b0072f44054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9688649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5c6a4a61291d9496e34bac48ab1dacebd4739321c6cfea44f57bf7d70d0ec4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-s390x.tar.gz / # buildkit
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
	-	`sha256:552c3aaa08429935d8dfef69ca747244fe854badcb537563677169e2f2ebdde8`  
		Last Modified: Wed, 08 Jan 2025 17:27:28 GMT  
		Size: 3.2 MB (3231849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088de0189be3b501d83cd78bb736e152eb9c879fee282f9dbc136e3d59ea1ee5`  
		Last Modified: Wed, 15 Jan 2025 02:37:57 GMT  
		Size: 296.2 KB (296168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95abefa83c834e15d00de84079607a49184ee2125795798f287f955f45d84d`  
		Last Modified: Wed, 15 Jan 2025 00:10:20 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a765923fab0e8bd0e0e5273d4883d868210b55d31fa8e102409189f093e461b8`  
		Last Modified: Wed, 15 Jan 2025 10:41:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea1c9c51d488f6c8ef15fdc1c88881262a91a6c731e4397e4402b158a52b107`  
		Last Modified: Wed, 15 Jan 2025 00:10:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:ac84eda0399f81593ee60869efeeafd4c44aeb92e4d4f8aff7d74c9e5338f9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 KB (192176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4cf9615766470533a5207df9fcbfafdce5121030d02d0c7d5db4ecb7c3bbc3`

```dockerfile
```

-	Layers:
	-	`sha256:4f5fbbf076e745d22a8e41a999227a6b751adda40e7a3e98afa1abac119c787a`  
		Last Modified: Wed, 15 Jan 2025 02:37:57 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae1a54ed652d75d520f8eb65aebea6ab6549b447255c286084e321dc29cc126`  
		Last Modified: Wed, 15 Jan 2025 00:10:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0-rc.2`

```console
$ docker pull registry@sha256:41c6924baf8b3c075f0bef84b885d36b9c7af271fd799d39f03a6b06695e80ec
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
$ docker pull registry@sha256:9ee5a51ee9a04e9ca8f8d57efd68d35d01a2c26fb7193b48af6cfcd56522b0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18315637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e2464438b36d1f685f3dd7e8d05f43c8ea36cecefe66f43c15d0201fce654a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cf40876cec3283678dcc892717e8b535313897d77f7008a4e1a76f6d971787`  
		Last Modified: Tue, 14 Jan 2025 20:44:37 GMT  
		Size: 294.9 KB (294876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280cf0325da76eb3f673f4d5c3254ead5119a2dfc6c98181379d0bb852aff11a`  
		Last Modified: Tue, 14 Jan 2025 20:34:11 GMT  
		Size: 14.4 MB (14378436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd193f29b6741853f108fde76c8e1ea993cbe86420ca718ae249ea54fb7798d`  
		Last Modified: Tue, 14 Jan 2025 20:34:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce6170d59039c467caa2ddf6f80211398fe0f24cb0636140ab6b262f581f27f`  
		Last Modified: Tue, 14 Jan 2025 20:34:09 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:4b8f74be0d31780f8437c2b1659b26ffc1c04f9a953a92d8eadc29ac29f27e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 KB (280544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b05466004c03f389adacb000a3c6b52738ee80b388bf40c345fdc6d4cf95a2`

```dockerfile
```

-	Layers:
	-	`sha256:5d5a9be4a6fe050c2e538140d7302b85783782d90208ffc41bea3ae570210f4f`  
		Last Modified: Wed, 08 Jan 2025 18:11:33 GMT  
		Size: 267.1 KB (267055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d17ad5d62d21418e98421cb16ab87d7a2b3010c889c7b18c8ee6fb4eedeb3a`  
		Last Modified: Wed, 08 Jan 2025 18:11:33 GMT  
		Size: 13.5 KB (13489 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; arm variant v6

```console
$ docker pull registry@sha256:1c4e386b7bd684dbc6c704c2680eec1ccf87f1047a2a87edceac84ba87d6157f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17169362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b51b468e216154be3b3cd103ee2cf36eacc2fd74b729970b8ae86376b8369b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f03f69a8f388ed7361ffb2b4247b3a48f246dac506cf30e7f01c792fb81bc18`  
		Last Modified: Tue, 14 Jan 2025 20:47:26 GMT  
		Size: 296.2 KB (296242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a9f77784bd51d41e68ba465a1b60c16aa42b69e6c5a7022cc6c6ea2669af20`  
		Last Modified: Wed, 08 Jan 2025 21:49:42 GMT  
		Size: 13.5 MB (13508627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fed0d7c0374b93d8e268831c26c1fd57f535548c959ce0e9bb4612dad98f939`  
		Last Modified: Wed, 08 Jan 2025 21:49:41 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4913fea00606a4171313c83c3292264df13ff04985d55057cbd8e560171b73a`  
		Last Modified: Thu, 19 Dec 2024 08:08:14 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:fe7d1232a3550f0c29dcb409acd360c5ab8f726ec7f968057632341433397b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3c9ff16e0ce9981468b1e7ca1de7e876cb5d2826031710e350c2c784ff3172`

```dockerfile
```

-	Layers:
	-	`sha256:9712fd1f8c12f10865adf5c012eb3a0c130f1d3d8864015106e84a8a86775f4c`  
		Last Modified: Wed, 08 Jan 2025 21:49:41 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; arm variant v7

```console
$ docker pull registry@sha256:b9ea647996c5bcb35d2e4255d9641f437fd8fbaea619e0665cb41268e568a25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16890946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18159640300f416928fa0d2c4a25e982ded053f3e17aea241bcf8abec45a8e13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0001409a747749230c7a654e2687c0848bbc83674d48cdc49a7ace1ecdd14`  
		Last Modified: Tue, 14 Jan 2025 20:39:05 GMT  
		Size: 295.2 KB (295180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c70dfde2c82a9760b64b64677a9e4d6a5b85290c6a0a6579f230d4e7aaf9cb3`  
		Last Modified: Wed, 08 Jan 2025 21:54:51 GMT  
		Size: 13.5 MB (13498045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed403ad487a1ff442a0802144aaa0a62fd948185faedf50564093f66b5bb342e`  
		Last Modified: Wed, 08 Jan 2025 21:54:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4d824ecec0d7444d822dd474d8b73f7390ef32cfbf147cf5d945afe80607d8`  
		Last Modified: Wed, 08 Jan 2025 21:54:50 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:4f599589099feb78d00ab49d281770dab44cef05751fc640443b126b9232a867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 KB (280621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17aee387891b65307e96915a1d48ecfce90e2db501e15e16ea122e4d530a54d0`

```dockerfile
```

-	Layers:
	-	`sha256:00865c5c1ad4cd8cbbbf4025e129fac176acbb1184a24e9a6e5a8b0ce61efb25`  
		Last Modified: Wed, 08 Jan 2025 21:54:50 GMT  
		Size: 267.1 KB (267067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4f284a4514a973149fc88b14aa8727e78ac7bd1ab4db809f68cc02bdaa947ae`  
		Last Modified: Wed, 08 Jan 2025 21:54:50 GMT  
		Size: 13.6 KB (13554 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:03869b3a898f31865cc76345159bd0117dd51d0a8495e3ebe9dc3982f38743c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17571923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87882d78068c9094f147ba85fa71f00650546cb6e3ddbce4b83d1ac23795552`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60c5244e6e0746968690ea87cc54b1e6431555cbe0d64cfe4914d06ca5f3587`  
		Last Modified: Tue, 14 Jan 2025 20:35:08 GMT  
		Size: 297.9 KB (297856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d19fa519fd1681280a394a326d25ed73877bde8ac081fe1023b03a9a0e1e4fa`  
		Last Modified: Tue, 14 Jan 2025 21:56:21 GMT  
		Size: 13.3 MB (13281098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c520dd78e75edba3c80d4838e6ff1c495402b108d2b9d8b6e29a28d67091da4`  
		Last Modified: Tue, 14 Jan 2025 21:56:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d491ceda2c0ed2a524a78bc569b08b1526562f805f2ce5c091c52abde51333b5`  
		Last Modified: Wed, 15 Jan 2025 08:57:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:97786bb0b7a0d764e7addce1298a2664a5e6ca299f663ca4fed7b832c60ac333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 KB (280647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f08610a3955e52798fa34f666833aa37a6f01784ca6842cda99555c40ae79bc`

```dockerfile
```

-	Layers:
	-	`sha256:18c0988c0d9c2e97f91ceda86b18d3283d6e1eff758f19c8830a4d4098eb14aa`  
		Last Modified: Wed, 08 Jan 2025 22:06:12 GMT  
		Size: 267.1 KB (267075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e695af7d88239da26a3702052592ef71fcb9bfe875a9bf2d62e0dd4dcfce39a1`  
		Last Modified: Wed, 08 Jan 2025 22:06:12 GMT  
		Size: 13.6 KB (13572 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; ppc64le

```console
$ docker pull registry@sha256:125a508e7e255076939d38c9927115bfb7d4588b30add4f9294306a5998464f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16832068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ad6d2e0394f5e0595882b75760d4d7fd81078e9a9eb85b04e8f89a8f5bbb4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a042ebf699b611e6e58aca079ac36bcffe2b6f4192af8e600a7562a6c7df55`  
		Last Modified: Wed, 08 Jan 2025 21:28:16 GMT  
		Size: 298.3 KB (298270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31db74a4453143a71be4e37a6f11a650f82e7cd719070afed3df9c2c662c012a`  
		Last Modified: Wed, 08 Jan 2025 21:28:16 GMT  
		Size: 13.0 MB (12959587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56b45defd09ab85f4490d9632fed3ff8d245c94f9bacb42e902dfc246b57cb2`  
		Last Modified: Wed, 08 Jan 2025 21:28:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b2e010837b9b6ca0a3e1cdcfd96f3bc279e0cd5dde8a2ca463122950d5ee19`  
		Last Modified: Wed, 08 Jan 2025 21:28:15 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:e49247c5124e86d8a4712ee6b5e4c29d0e3e8bec9b70e205811d9ef23cc8346a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b99fe57c2996be435629c74838782836ada5d8b3da1f724c0051996d49e27a2`

```dockerfile
```

-	Layers:
	-	`sha256:dbe4d8154dc837fab37914a65c00d5af9c54d84b33b9a281833fea2fb9b0897c`  
		Last Modified: Wed, 08 Jan 2025 21:28:16 GMT  
		Size: 265.1 KB (265120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda3bf9af70b788581c700c1b1caf72aed65e416a035cbeaf6915a1f5a871c3d`  
		Last Modified: Wed, 08 Jan 2025 21:28:15 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; riscv64

```console
$ docker pull registry@sha256:16daa80c70f40e721b9fd8b2943e26ed1910f8ffb7944a9e5b04679dc7c8b00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17312312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a0bae7bbf30e51aa47b43a1bcb27a1e129d32cf4b9aa63229b143a3fac5905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d26d7d7362ba90a5c2912b455128da725e739b7dbd70f75dc1091bfed8ea2d6`  
		Last Modified: Tue, 14 Jan 2025 21:23:59 GMT  
		Size: 295.4 KB (295361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8fdcb2f2b2a5ef02dc5384848001c83ffe5ca8922b7e3ba02904a6c50d2ceb`  
		Last Modified: Tue, 14 Jan 2025 21:20:48 GMT  
		Size: 13.7 MB (13666086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6ef0185480aa76f1fc639da17cf9d0a589228cac9c2acf2cba7f8d43865355`  
		Last Modified: Fri, 10 Jan 2025 16:32:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6033d72f0e4bc56fff111848436d6561f122dd0decf408eda030cf7be8bc6bc3`  
		Last Modified: Fri, 10 Jan 2025 16:32:59 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:bb1931cb2e01feee860bc6bbd8b9336be025680aec0117923ae6955dbb6016bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5f1da55990b1f9f3390270b84be3d643bf45b1ad21c0b0d10d06db7dc95fcc`

```dockerfile
```

-	Layers:
	-	`sha256:322ba432988cbf896512b8d34ce7ecd86ac0fcfec4c199fe86951cff1023dc9b`  
		Last Modified: Tue, 14 Jan 2025 21:20:47 GMT  
		Size: 265.1 KB (265116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af4f3204e7f8cf59ed13db32ef7afe351d4ba69665a0ead80b79560f6778ec0`  
		Last Modified: Tue, 14 Jan 2025 21:20:47 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; s390x

```console
$ docker pull registry@sha256:7324db875f30306d125e689ab1134b602eb4f6d2606d4431d154b892406a0535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17608250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea34606cdca75abc5f0537663709de42177ebdd6e4b523e087f50df4cfeb8397`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 18 Dec 2024 15:37:50 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891798c8b7f45ed9fd4734da8ad75c1f6667b239c599c11f3cdab494a7a8406d`  
		Last Modified: Tue, 14 Jan 2025 23:35:19 GMT  
		Size: 296.2 KB (296160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d597c4250fcb51a1f4e9bf6ad882b5966b0fc95d74d7637c3cc452a44787e4`  
		Last Modified: Wed, 08 Jan 2025 22:06:35 GMT  
		Size: 13.8 MB (13844614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40ce435b7c95d1c8a9c6469020c2229075f18e443d87ff21fc05fa00600774a`  
		Last Modified: Wed, 08 Jan 2025 22:06:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7584221c2a737083c8d82300f01bb39978328b8142879b2183d34b21e81475`  
		Last Modified: Wed, 08 Jan 2025 22:06:35 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:ae83d4c22b4d34c94c7901a64e54b691339b07b685ae449a950648677807de30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9fe6bd143bd7e18ebaf891fcf33db1bc4b2e0345e51f3d50f4da3197e59a8c`

```dockerfile
```

-	Layers:
	-	`sha256:a3636f8a3fc7f71297d9ed5c836d8dbb2db2fd00e823eb91d3a32da190601960`  
		Last Modified: Wed, 08 Jan 2025 22:06:35 GMT  
		Size: 265.1 KB (265094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca43a18929509def657a9ec1930d5fb84ea59262280c020b87ad034a65aa36fb`  
		Last Modified: Wed, 08 Jan 2025 22:06:35 GMT  
		Size: 13.5 KB (13488 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:319881be2ee9e345d5837d15842a04268de6a139e23be42654fc7664fc6eaf52
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
$ docker pull registry@sha256:57350583fba19eaab4b4632aafa1537483a390dfd29c5b37c9d59e2467ce1b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282bd1664cf1fccccf9f225118e31f9352f1f93e4d0ad485c92e74ec6b11ebd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
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
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6afea20d55c46e60901e594cad0651da46b7437cf42a3c27e52d5bd37320165`  
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 295.7 KB (295665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f4e00e7d3c5ea061e25a18ba6127f79930efbbd3f3deb59c272ca0d6de23c3`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 6.4 MB (6403790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665375f3730237f2109d398104a2072e38166ecf5d8316b1464f8a005146384e`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9959184a302f6f95d8be97229fb31def6700b1895b1ee92090129b60e6567820`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:2ed78d67c727bcce149533b0ac69e59a62b8c16edd0f113f0b81d8cad414adf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 KB (194126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7686a99322a57149ff0aab40827d9abaf011fdbda972d8817e04f5d98530d01`

```dockerfile
```

-	Layers:
	-	`sha256:a7f9721296093c0999458f91d6176f8cbf9ad755f89877da06031de4b3e9cb69`  
		Last Modified: Wed, 15 Jan 2025 00:10:17 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c800ea38a09dbe46c3cb07f4498fcb316134e44440ee5941a2374c41d0eac9d`  
		Last Modified: Wed, 15 Jan 2025 03:19:35 GMT  
		Size: 14.1 KB (14064 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:7f9dcbf2fb5296dacd3c0113fbbd5ab2d5e5a95900060c7b1fdbd4001713ade0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9480838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd9a6e975ec81b8ae82571e63e99f4a8775c1f2e1c78e382d1ad786b4ac1fe7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-armhf.tar.gz / # buildkit
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
	-	`sha256:803cf02755db9f4dbb0d52a3ff280052dd523cdfdb9e9be6494b4edd548d6dc6`  
		Last Modified: Wed, 08 Jan 2025 17:24:20 GMT  
		Size: 3.2 MB (3159977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7840dcb6e03dd1709b54c0be0dd05dab1e1332a39708dee9eaaf7dbb8820ce9`  
		Last Modified: Wed, 15 Jan 2025 02:37:53 GMT  
		Size: 296.2 KB (296164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551f60a571f5e22a678c2812142fcecb7a4ca62e3bdb99e32bc8962583208349`  
		Last Modified: Wed, 15 Jan 2025 02:37:54 GMT  
		Size: 6.0 MB (6024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad6dfdda7a01c82c1ae649bbf1f80fe5126a5c22559167fe5975356c7949341`  
		Last Modified: Wed, 15 Jan 2025 02:37:53 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786e8db11e0fb9efe89d614a159662b1d4bb3bb45662b6b7ad6c05f439e8eed7`  
		Last Modified: Tue, 07 Jan 2025 07:43:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:087a16847794451af13a9f72c4eb87727c0f690e715bc2cab96758309ce3bca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bdb2f6d7b8b7e511805bbf68d57fe69ec8922ff6d64628aff9a1ed11c9d790`

```dockerfile
```

-	Layers:
	-	`sha256:5fb180ceda25c616d72b29cbf15eed44aedc427e6b45c16b7b83c1f9ede99b15`  
		Last Modified: Wed, 15 Jan 2025 02:37:54 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:574610c8eafc5c3961b7fc8229597d5ae88733a8283fc835d32d41d396f8f546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9225758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f9c806796de21a52dbafc030a4dfa0e913746772b85686d43eb796402fef29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-armv7.tar.gz / # buildkit
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
	-	`sha256:e1b4e22e09e012565a243e582da1a0c5d1de7318c191f19a95a4e6e5e8535be8`  
		Last Modified: Wed, 08 Jan 2025 17:34:42 GMT  
		Size: 2.9 MB (2912794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7361fdbbdb9dd007424891fe5603438ddf1db7c562c4e853d78827f54a26f257`  
		Last Modified: Tue, 14 Jan 2025 21:31:26 GMT  
		Size: 295.2 KB (295165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca4f35222130d5ce0cc4968ce9ecfbb0e1f3988a0db13c95fa0b7a6a2876df4`  
		Last Modified: Tue, 14 Jan 2025 21:31:26 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8c2cb058a9769352b2455ed4001792d88acd516960469d0092b7c126eebdec`  
		Last Modified: Tue, 14 Jan 2025 21:31:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34401837030ebc7227878bae338335617113254bf4208048748a38326150786`  
		Last Modified: Wed, 15 Jan 2025 00:10:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:6d9590249cd4a04e2c96c7451ec5fbfc2cd5ce5dfcaf4f54d27a6d4fe846333d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6f0f8b0819f6d3a9963ca63d53ea51adc9629f0eb7b9b7ca73f0ac5dd2350f`

```dockerfile
```

-	Layers:
	-	`sha256:a3661c5da3fdd2b47d824fe3bda6c618a50daff424f25ece3c38d7c376f6d9a0`  
		Last Modified: Wed, 15 Jan 2025 03:19:18 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d73d4b6eaf8501e4340b60842355e671fe7ced474835e36951c93ff327af82`  
		Last Modified: Wed, 15 Jan 2025 02:37:55 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1674a8dd758ef390d16fdb58be6646005a0154606bba8bb41e5ddf2b40b3fcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8876582179f0fe21dad0d58f5cf820017819161bb786ea43e9863beeef95f70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
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
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Wed, 08 Jan 2025 17:24:31 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0726ca172d8b26fcb657230174e78246e0d10a453d5eb068720f3e309c422a04`  
		Last Modified: Tue, 14 Jan 2025 20:38:59 GMT  
		Size: 297.8 KB (297823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b7b7187cb358b4974cf0245aecab9fb00f528bbdebf66fb63e8da2a74456e7`  
		Last Modified: Tue, 14 Jan 2025 20:37:00 GMT  
		Size: 5.8 MB (5824731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14fe80572add96e41c3ef0b859c81f81c9662078baba85162bf121af0337176`  
		Last Modified: Tue, 14 Jan 2025 20:39:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa909d97427642d4f9aa7249f3c06087e667e40b74753a4cf27ab3005250c970`  
		Last Modified: Tue, 14 Jan 2025 20:37:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:f98e543c1aced03689c60d626e1b8501c1568f43156afe7930902e2f006de0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3212b1b26d5836c0dec2c1d174a74b0aacc40a44767d5a706fbb4fb89c14358`

```dockerfile
```

-	Layers:
	-	`sha256:d19202c96c707295b0022d580dd5187da04580f93059ed006d1cf32e415eef49`  
		Last Modified: Wed, 15 Jan 2025 10:46:15 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682fd9916c4c71c5c7c15151a03509a7346c9efc018d7c2a67251b8ff095072b`  
		Last Modified: Wed, 15 Jan 2025 00:10:18 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:60619ec298638d377e8631927d55b84c9ea86ac2e1303de28a65b2e20ae4ec85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9347330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f8f1595a0733b662963c070cd0c8c3d594720b77ae00d099913b1f37110ea7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-ppc64le.tar.gz / # buildkit
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
	-	`sha256:6259f25643973acaf5182679ac24f10e7bcb8be462646ba81a87b013ec80c9ed`  
		Last Modified: Wed, 08 Jan 2025 17:25:55 GMT  
		Size: 3.4 MB (3359277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b59fd69e39afe9b69b4ed12982c3fcc9b36a7453cf9ae8e34edbea633db64c`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 298.3 KB (298253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84815ad061a37d997ef0467524fb1782e217752eb2017f61101df2d66fc508ad`  
		Last Modified: Wed, 15 Jan 2025 03:19:20 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e108bb20672a34158c362d7a824852b67b1055b96032e540cd8aeebae409356`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9bb1e1a56c8509c23cf94332c160707790aaaa8d1cddd92182964da536c538`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:0d21931696fa83e2e6e170f48375ad62ea48db603439ac45034b84568b5c2d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 KB (192255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf187220c58e23bd5f1b27074abc712ca3e537a502ea51a55675d6601175ae3`

```dockerfile
```

-	Layers:
	-	`sha256:129c8dd66a4381ad34fac5989711b1a956eddd716be30f64e5b2ea3c1074d767`  
		Last Modified: Wed, 15 Jan 2025 02:37:56 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7be9132674cb879c894e8b20f9735919f07228698009969b9d40db2a7d2a2f`  
		Last Modified: Wed, 15 Jan 2025 00:10:19 GMT  
		Size: 14.1 KB (14110 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:126b6d230d49f8167af80d517a2e407ef5fdd44a5409ff3bf6612b0072f44054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9688649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5c6a4a61291d9496e34bac48ab1dacebd4739321c6cfea44f57bf7d70d0ec4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.11-s390x.tar.gz / # buildkit
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
	-	`sha256:552c3aaa08429935d8dfef69ca747244fe854badcb537563677169e2f2ebdde8`  
		Last Modified: Wed, 08 Jan 2025 17:27:28 GMT  
		Size: 3.2 MB (3231849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088de0189be3b501d83cd78bb736e152eb9c879fee282f9dbc136e3d59ea1ee5`  
		Last Modified: Wed, 15 Jan 2025 02:37:57 GMT  
		Size: 296.2 KB (296168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95abefa83c834e15d00de84079607a49184ee2125795798f287f955f45d84d`  
		Last Modified: Wed, 15 Jan 2025 00:10:20 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a765923fab0e8bd0e0e5273d4883d868210b55d31fa8e102409189f093e461b8`  
		Last Modified: Wed, 15 Jan 2025 10:41:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea1c9c51d488f6c8ef15fdc1c88881262a91a6c731e4397e4402b158a52b107`  
		Last Modified: Wed, 15 Jan 2025 00:10:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:ac84eda0399f81593ee60869efeeafd4c44aeb92e4d4f8aff7d74c9e5338f9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 KB (192176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4cf9615766470533a5207df9fcbfafdce5121030d02d0c7d5db4ecb7c3bbc3`

```dockerfile
```

-	Layers:
	-	`sha256:4f5fbbf076e745d22a8e41a999227a6b751adda40e7a3e98afa1abac119c787a`  
		Last Modified: Wed, 15 Jan 2025 02:37:57 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae1a54ed652d75d520f8eb65aebea6ab6549b447255c286084e321dc29cc126`  
		Last Modified: Wed, 15 Jan 2025 00:10:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json
