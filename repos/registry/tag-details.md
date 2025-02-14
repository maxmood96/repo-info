<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-rc.3`](#registry300-rc3)
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
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:51:05 GMT  
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
		Last Modified: Tue, 14 Jan 2025 21:04:09 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:51 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:17 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:51:05 GMT  
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
		Last Modified: Tue, 14 Jan 2025 21:04:09 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:51 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:17 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:51:05 GMT  
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
		Last Modified: Tue, 14 Jan 2025 21:04:09 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:51 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:17 GMT  
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

## `registry:3.0.0-rc.3`

```console
$ docker pull registry@sha256:2890fabe4c5e62ed3f05661f14ce699401b6bf4542e5e11f08dd8cd848b4ab04
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

### `registry:3.0.0-rc.3` - linux; amd64

```console
$ docker pull registry@sha256:36017b736232e1f973b5ed9380e0284463ed36e9f4819d287b9191f42e09934b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18321279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc13184ff7bf13650659d390a6d86a715f84d54dff306851729f4c8980fd6ca6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
RUN set -eux; 	version='3.0.0-rc.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='e4412fbc7b010432e64dca3f02140d608912ec3aa91554ff3b67700891bb3a12' ;; 		aarch64) arch='arm64';   sha256='393eb2fff43d93a362a3ec417ec07d4304b81bee9276d1a589951467c4a49bf3' ;; 		armhf)   arch='armv6';   sha256='a4f25dc7eaed798523c045afbef5e9416c7810904777e92fc4797321cdfd2a24' ;; 		armv7)   arch='armv7';   sha256='7fdf37749bf9b7692ecd419779cd0d298cc54a7b32b5cb838a71bb3c3b126272' ;; 		ppc64le) arch='ppc64le'; sha256='7d1c58daa3ba9373d5ce12b7e235795a62951ed9afd91aad0280a1cc115bf060' ;; 		s390x)   arch='s390x';   sha256='d99a60587451f6daa9a67ea1ebe55982f7a967834926830b7463dcdd739ab01b' ;; 		riscv64) arch='riscv64'; sha256='46a24d55f2efbbcfbc97aee9962c61c76a3be7aa6f7b76faaa9513e8866d20d4' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
VOLUME [/var/lib/registry]
# Tue, 11 Feb 2025 22:14:46 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 11 Feb 2025 22:14:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efd6bab0646f81727e12905f00c9ad1d42f1f0768b89c6d0efc3e0088787947`  
		Last Modified: Wed, 12 Feb 2025 09:46:04 GMT  
		Size: 294.9 KB (294892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e6af0ee16c47b452c128912d17401586932ecca9dcf11091e5c21cd64075d`  
		Last Modified: Wed, 12 Feb 2025 01:39:21 GMT  
		Size: 14.4 MB (14384063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dfbe072dbbdc64d919e240b752f9564cff3167733332ec9788e4bf7d44896b`  
		Last Modified: Tue, 11 Feb 2025 23:30:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a8c729390ee95faee970a62bb1495322beb8307fc469a4fcac0fdd8c24ab25`  
		Last Modified: Tue, 11 Feb 2025 23:30:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:f5f0ed160a8566f9707d41c1577505c0773c10e8229f0647ebb8fa56acfc101f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 KB (280512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31edf516199f84a76f436f8c0c59bf294babeba4b4cf742351856e97a68b63f9`

```dockerfile
```

-	Layers:
	-	`sha256:6a4abfede73e765d16a68714c1e970f86dde7f60f202569f7dda639d596ef6df`  
		Last Modified: Wed, 12 Feb 2025 20:01:06 GMT  
		Size: 267.1 KB (267055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e6c0bc10e5ce812d13e93a4158cd03af668c4da08f487d5329b36061078a2b`  
		Last Modified: Wed, 12 Feb 2025 02:23:20 GMT  
		Size: 13.5 KB (13457 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; arm variant v6

```console
$ docker pull registry@sha256:71a5035ae86479ca386b6c8f8d7d9ca1a1644b8119e9a487821c46a5e06cd9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17178024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efac3fc886c5669b1298e47842725d79f70fc4183f9ca3a411fdfc1972e998b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
RUN set -eux; 	version='3.0.0-rc.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='e4412fbc7b010432e64dca3f02140d608912ec3aa91554ff3b67700891bb3a12' ;; 		aarch64) arch='arm64';   sha256='393eb2fff43d93a362a3ec417ec07d4304b81bee9276d1a589951467c4a49bf3' ;; 		armhf)   arch='armv6';   sha256='a4f25dc7eaed798523c045afbef5e9416c7810904777e92fc4797321cdfd2a24' ;; 		armv7)   arch='armv7';   sha256='7fdf37749bf9b7692ecd419779cd0d298cc54a7b32b5cb838a71bb3c3b126272' ;; 		ppc64le) arch='ppc64le'; sha256='7d1c58daa3ba9373d5ce12b7e235795a62951ed9afd91aad0280a1cc115bf060' ;; 		s390x)   arch='s390x';   sha256='d99a60587451f6daa9a67ea1ebe55982f7a967834926830b7463dcdd739ab01b' ;; 		riscv64) arch='riscv64'; sha256='46a24d55f2efbbcfbc97aee9962c61c76a3be7aa6f7b76faaa9513e8866d20d4' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
VOLUME [/var/lib/registry]
# Tue, 11 Feb 2025 22:14:46 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 11 Feb 2025 22:14:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f03f69a8f388ed7361ffb2b4247b3a48f246dac506cf30e7f01c792fb81bc18`  
		Last Modified: Tue, 14 Jan 2025 20:47:26 GMT  
		Size: 296.2 KB (296242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfff766b5cf6c3053370be650a38acb1d4e6e8cac359358766f115ae067f0f1`  
		Last Modified: Wed, 12 Feb 2025 02:23:30 GMT  
		Size: 13.5 MB (13517294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925999b7d99b781aafc6079f76e30e0eb4cfd01fde32aae87e1d0f505148fa85`  
		Last Modified: Tue, 11 Feb 2025 23:30:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6f66f98998e68c79f8a3b6ec414f388ad98e97bcbec20eb4ab69b775bab484`  
		Last Modified: Tue, 11 Feb 2025 23:30:15 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:a892e116c0ac5fb1234b39d345210e29223ff7c4dee5979ae8082fddf3b984a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0f896d7d6ba435195234760bc6f81ce99c5c39ec9f14e0bbc8af153911fcb1`

```dockerfile
```

-	Layers:
	-	`sha256:d0578980dcb19682ec7554751f1a804eed7c330359a40252aa6bff0860794c63`  
		Last Modified: Wed, 12 Feb 2025 09:01:54 GMT  
		Size: 13.3 KB (13305 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; arm variant v7

```console
$ docker pull registry@sha256:3117b0eb58365366c8886e3c26a2dceb5e43cabe3ea6fafbfc4ab9de2723f754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16896975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c0a5ccf83c4453e1ecf04cdc6f2e9835acd4ce1a97d89b2e0dca2cccae1028`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
RUN set -eux; 	version='3.0.0-rc.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='e4412fbc7b010432e64dca3f02140d608912ec3aa91554ff3b67700891bb3a12' ;; 		aarch64) arch='arm64';   sha256='393eb2fff43d93a362a3ec417ec07d4304b81bee9276d1a589951467c4a49bf3' ;; 		armhf)   arch='armv6';   sha256='a4f25dc7eaed798523c045afbef5e9416c7810904777e92fc4797321cdfd2a24' ;; 		armv7)   arch='armv7';   sha256='7fdf37749bf9b7692ecd419779cd0d298cc54a7b32b5cb838a71bb3c3b126272' ;; 		ppc64le) arch='ppc64le'; sha256='7d1c58daa3ba9373d5ce12b7e235795a62951ed9afd91aad0280a1cc115bf060' ;; 		s390x)   arch='s390x';   sha256='d99a60587451f6daa9a67ea1ebe55982f7a967834926830b7463dcdd739ab01b' ;; 		riscv64) arch='riscv64'; sha256='46a24d55f2efbbcfbc97aee9962c61c76a3be7aa6f7b76faaa9513e8866d20d4' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
VOLUME [/var/lib/registry]
# Tue, 11 Feb 2025 22:14:46 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 11 Feb 2025 22:14:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
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
	-	`sha256:e27fb74418b16cc41b41fe0851e4b0f62b9c78c66f0393200529d3557a7a8b13`  
		Last Modified: Wed, 12 Feb 2025 02:23:50 GMT  
		Size: 13.5 MB (13504072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0383031952a7755d65d0e4a3b756ecef5faae11e2acd4c08e2bdece5e3eba9`  
		Last Modified: Tue, 11 Feb 2025 23:30:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be349fde7273f645bc1c5369b64010d25aafaadd794335d80bd6429bfa66188e`  
		Last Modified: Wed, 12 Feb 2025 09:01:55 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:6bed89f0a5bd1c82855631b5bf2c8adf752f7c9b4dd56e13fe59acb0cfb7e704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 KB (280589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7039651c736bbdbdf7c6da0c498f0f639a345387b8d500dcaf8ea12d7afd74e`

```dockerfile
```

-	Layers:
	-	`sha256:c06c83591de161f9f8c721d088d1fe625a2d46c80ecc2412515d262fa214db63`  
		Last Modified: Wed, 12 Feb 2025 09:01:54 GMT  
		Size: 267.1 KB (267067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f7726b40d1c48e7f1799cd004257463581f24ae51f278dfc0abfd86eb8cb24`  
		Last Modified: Wed, 12 Feb 2025 02:24:03 GMT  
		Size: 13.5 KB (13522 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:243451e7a3d1f50351da412949a0af67d7f0a8faf5978af22bcf5bb194975baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17577815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaeb70aa2fb1d297c40509134065393f319c6997af23dc807b36626c55ceace`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
RUN set -eux; 	version='3.0.0-rc.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='e4412fbc7b010432e64dca3f02140d608912ec3aa91554ff3b67700891bb3a12' ;; 		aarch64) arch='arm64';   sha256='393eb2fff43d93a362a3ec417ec07d4304b81bee9276d1a589951467c4a49bf3' ;; 		armhf)   arch='armv6';   sha256='a4f25dc7eaed798523c045afbef5e9416c7810904777e92fc4797321cdfd2a24' ;; 		armv7)   arch='armv7';   sha256='7fdf37749bf9b7692ecd419779cd0d298cc54a7b32b5cb838a71bb3c3b126272' ;; 		ppc64le) arch='ppc64le'; sha256='7d1c58daa3ba9373d5ce12b7e235795a62951ed9afd91aad0280a1cc115bf060' ;; 		s390x)   arch='s390x';   sha256='d99a60587451f6daa9a67ea1ebe55982f7a967834926830b7463dcdd739ab01b' ;; 		riscv64) arch='riscv64'; sha256='46a24d55f2efbbcfbc97aee9962c61c76a3be7aa6f7b76faaa9513e8866d20d4' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
VOLUME [/var/lib/registry]
# Tue, 11 Feb 2025 22:14:46 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 11 Feb 2025 22:14:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1868c9f11e67c6a569d83fd91d32a555c8f736e46d134152ae38157607d910`  
		Last Modified: Wed, 05 Feb 2025 03:24:10 GMT  
		Size: 297.9 KB (297860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a3ef8d8ca950987e0cccb7b1a6425ab3b1de1391e02e6429039ebabea4c280`  
		Last Modified: Wed, 12 Feb 2025 01:39:20 GMT  
		Size: 13.3 MB (13286986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a174290a050ce40328a9070a052bdbcb4c793e5b66132f4fc2774cb20c99e93`  
		Last Modified: Tue, 11 Feb 2025 23:30:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95296fb8a1115984ec8a5e4f4484d4a68e6d37236224ac58608ecbe0cd16c892`  
		Last Modified: Tue, 11 Feb 2025 23:30:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:e253b5ca632e92e1916e98238b531adc01ea5428f06c301a05faf3e776a5b417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 KB (280615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc843ae7418afcdfcc503558aee8c110cf181b51f7cc8c3514a3869b3bdaf177`

```dockerfile
```

-	Layers:
	-	`sha256:ebef9bf97e018e3e20f637ac7ebf73ff60b5a2eae75096502fde9c4970f92878`  
		Last Modified: Wed, 12 Feb 2025 02:24:24 GMT  
		Size: 267.1 KB (267075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:572290ebc2ecd3aeefacb53daf59fe7fd16e95c78cbad8a2cab4dd3790b1214c`  
		Last Modified: Fri, 14 Feb 2025 08:59:01 GMT  
		Size: 13.5 KB (13540 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; ppc64le

```console
$ docker pull registry@sha256:6ec304b7d830cb062c6f209223b32d2b845fc45b995792107949551897ce66ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16837145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1df8df8d54b7b8bbdcc3dbe835da42956d1befb9d1395403c2138677c9a9c8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
RUN set -eux; 	version='3.0.0-rc.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='e4412fbc7b010432e64dca3f02140d608912ec3aa91554ff3b67700891bb3a12' ;; 		aarch64) arch='arm64';   sha256='393eb2fff43d93a362a3ec417ec07d4304b81bee9276d1a589951467c4a49bf3' ;; 		armhf)   arch='armv6';   sha256='a4f25dc7eaed798523c045afbef5e9416c7810904777e92fc4797321cdfd2a24' ;; 		armv7)   arch='armv7';   sha256='7fdf37749bf9b7692ecd419779cd0d298cc54a7b32b5cb838a71bb3c3b126272' ;; 		ppc64le) arch='ppc64le'; sha256='7d1c58daa3ba9373d5ce12b7e235795a62951ed9afd91aad0280a1cc115bf060' ;; 		s390x)   arch='s390x';   sha256='d99a60587451f6daa9a67ea1ebe55982f7a967834926830b7463dcdd739ab01b' ;; 		riscv64) arch='riscv64'; sha256='46a24d55f2efbbcfbc97aee9962c61c76a3be7aa6f7b76faaa9513e8866d20d4' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
VOLUME [/var/lib/registry]
# Tue, 11 Feb 2025 22:14:46 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 11 Feb 2025 22:14:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd68bfd3ee8de54b2fbc691d541267c5e55c57c253f41c0bd40aa2b5f9f17e9b`  
		Last Modified: Wed, 05 Feb 2025 00:31:28 GMT  
		Size: 298.3 KB (298275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa3de66648657e60baa73b7a22803e81b482e0bbbf9ceddd56b5d7b827a85d8`  
		Last Modified: Wed, 12 Feb 2025 02:24:38 GMT  
		Size: 13.0 MB (12964659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9faf3ae17a03d74033b9a236475c08eac33c7c69642f8221769fa14b27c9fbc`  
		Last Modified: Wed, 12 Feb 2025 20:01:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f07aaff603dc72323ed2333efc8d4e5c250c49a40a55aa375b9d8a9357f7716`  
		Last Modified: Tue, 11 Feb 2025 23:30:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:d7a0485c9eec4234e613457f2627981393b586de587bae23f9ff42cde62f9fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71cae37ba63e5d1e64fdc9c906e0977cfad54968bf0a95bff3cca7b7749d3e0`

```dockerfile
```

-	Layers:
	-	`sha256:d71b49f0f51ed1e2aa2b0d7a51d9a251cc967057d43b1479df076fb3ccf00c0c`  
		Last Modified: Wed, 12 Feb 2025 02:24:48 GMT  
		Size: 265.1 KB (265120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7131044f07e1e7f8192bcefdfc783cea11c1aaa881b0b47c48fa53251ed5ea0f`  
		Last Modified: Wed, 12 Feb 2025 02:24:51 GMT  
		Size: 13.5 KB (13485 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; riscv64

```console
$ docker pull registry@sha256:b4b6c0d668346a7b0ea66a4e4232f76b163afd996ca05fa80199f7c34cdc06ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17318241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c0f00befda7f73401724fddebb395c2ae39181837c21ec9176aea5335321c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
RUN set -eux; 	version='3.0.0-rc.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='e4412fbc7b010432e64dca3f02140d608912ec3aa91554ff3b67700891bb3a12' ;; 		aarch64) arch='arm64';   sha256='393eb2fff43d93a362a3ec417ec07d4304b81bee9276d1a589951467c4a49bf3' ;; 		armhf)   arch='armv6';   sha256='a4f25dc7eaed798523c045afbef5e9416c7810904777e92fc4797321cdfd2a24' ;; 		armv7)   arch='armv7';   sha256='7fdf37749bf9b7692ecd419779cd0d298cc54a7b32b5cb838a71bb3c3b126272' ;; 		ppc64le) arch='ppc64le'; sha256='7d1c58daa3ba9373d5ce12b7e235795a62951ed9afd91aad0280a1cc115bf060' ;; 		s390x)   arch='s390x';   sha256='d99a60587451f6daa9a67ea1ebe55982f7a967834926830b7463dcdd739ab01b' ;; 		riscv64) arch='riscv64'; sha256='46a24d55f2efbbcfbc97aee9962c61c76a3be7aa6f7b76faaa9513e8866d20d4' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
VOLUME [/var/lib/registry]
# Tue, 11 Feb 2025 22:14:46 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 11 Feb 2025 22:14:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d26d7d7362ba90a5c2912b455128da725e739b7dbd70f75dc1091bfed8ea2d6`  
		Last Modified: Tue, 14 Jan 2025 21:23:59 GMT  
		Size: 295.4 KB (295361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36671c22063792968120b23f6004e6e0d50527fbefa44d49ccdec88d0380e349`  
		Last Modified: Wed, 12 Feb 2025 02:25:00 GMT  
		Size: 13.7 MB (13672014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373fbec3e2ee01b1a2772ba421ca08518458d86f18a2eb4bc7faae2b033f96c6`  
		Last Modified: Tue, 11 Feb 2025 23:32:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35026c07e384bd603f3e574c02b8070c60808766ecedb39fb71c18e8d8f6fc6`  
		Last Modified: Tue, 11 Feb 2025 23:32:09 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:1f350384a58f481939ea2c45d3505a81e16485ae94b2e8b0f33772146b0f82ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fc3b42f38c48ecd0c2cb9f0aa373dcb3cadccb0203e3e07827d8ef34831480`

```dockerfile
```

-	Layers:
	-	`sha256:f41f99a255abb90d92d34d84254bca27ad246250388eae4edf2acecffc592c43`  
		Last Modified: Wed, 12 Feb 2025 02:25:13 GMT  
		Size: 265.1 KB (265116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31cacdb0b46f4e1d21ac2b8ffb1f2cb825e3b9cf1b0f88e4f1d54a9b0a7b235a`  
		Last Modified: Wed, 12 Feb 2025 09:01:58 GMT  
		Size: 13.5 KB (13485 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; s390x

```console
$ docker pull registry@sha256:5960ca523b949fa4a1d7180e265c85f34c0674b307028ae967428a13ce71454b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17615911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef72b6f77e34460a44c3f6f536753722bf5cf5af2ecc7471e44a9e527a2e59f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
RUN set -eux; 	version='3.0.0-rc.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='e4412fbc7b010432e64dca3f02140d608912ec3aa91554ff3b67700891bb3a12' ;; 		aarch64) arch='arm64';   sha256='393eb2fff43d93a362a3ec417ec07d4304b81bee9276d1a589951467c4a49bf3' ;; 		armhf)   arch='armv6';   sha256='a4f25dc7eaed798523c045afbef5e9416c7810904777e92fc4797321cdfd2a24' ;; 		armv7)   arch='armv7';   sha256='7fdf37749bf9b7692ecd419779cd0d298cc54a7b32b5cb838a71bb3c3b126272' ;; 		ppc64le) arch='ppc64le'; sha256='7d1c58daa3ba9373d5ce12b7e235795a62951ed9afd91aad0280a1cc115bf060' ;; 		s390x)   arch='s390x';   sha256='d99a60587451f6daa9a67ea1ebe55982f7a967834926830b7463dcdd739ab01b' ;; 		riscv64) arch='riscv64'; sha256='46a24d55f2efbbcfbc97aee9962c61c76a3be7aa6f7b76faaa9513e8866d20d4' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
VOLUME [/var/lib/registry]
# Tue, 11 Feb 2025 22:14:46 GMT
EXPOSE map[5000/tcp:{}]
# Tue, 11 Feb 2025 22:14:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Feb 2025 22:14:46 GMT
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
	-	`sha256:3f5812ac6350d30af5c05496139df2f5241d69d8ac3444e577c1b7fbc530cab0`  
		Last Modified: Wed, 12 Feb 2025 09:01:57 GMT  
		Size: 13.9 MB (13852275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2703a3ad7258e2d15ad11e1d94b04d6c4427ba95038b0358a45338d97863993`  
		Last Modified: Wed, 12 Feb 2025 02:25:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65f2e7925dcaf65110adc1eebf6b6c5c97dc105324eb3d09950b0a144a378ad`  
		Last Modified: Tue, 11 Feb 2025 23:30:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:654b69c9e5505a8fe5975dc5deab60b405ea343129a6cdadc9a5480d234b8dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b017894f11d9f00531da722672dab36d48e1fc019157d5026422b0936d69e24e`

```dockerfile
```

-	Layers:
	-	`sha256:9ca0ed832112fbc1b428969f5a864847cf8bf5e9ae1cd0f9b603edf9e17b306a`  
		Last Modified: Wed, 12 Feb 2025 02:25:35 GMT  
		Size: 265.1 KB (265094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fdb5639f9027c289afb029fcc252dd1fdd28cf04d4209af54d754ed87545440`  
		Last Modified: Wed, 12 Feb 2025 02:25:37 GMT  
		Size: 13.5 KB (13457 bytes)  
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
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:51:05 GMT  
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
		Last Modified: Tue, 14 Jan 2025 21:04:09 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:51 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:44:17 GMT  
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
