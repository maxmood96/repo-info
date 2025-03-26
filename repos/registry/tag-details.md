<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-rc.4`](#registry300-rc4)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:a3d8aaa63ed8681a604f1dea0aa03f100d5895b6a58ace528858a7b332415373
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
$ docker pull registry@sha256:46faa9a1ae6813194b53921a370f2f4f8c5e1aae228a89bceafef5847a6a3278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b2eb03618e749084668eaff68cff8f81dda12d06ac641be7a6398b82a6f25b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
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
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbdd6c6894b7d41bab22098e3a0fff77de4a231f5b407224ead5b3f26cc4ff3`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 295.7 KB (295684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e82f80af0de06ae95429a79d00ae7e98c0f5ded5555a06c024757d81371a742`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3493bf46cdec3b8ecbb96c0b1cd7fc5f90964306b7c55a0136dac0beeaa627f9`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d464ea18732475d5c3591f1eba3ee96a974808791a5fe103ea1c33199f2eb74`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:b79491fc7716809e3eb28bb866c952b670ec72edc28ac84dd423d28b94e22f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 KB (194127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a15a454b11b760c2f0143e9b2a8155c43f2bab9bf68ff9d023e769472c91c`

```dockerfile
```

-	Layers:
	-	`sha256:b537bf6d11468f33bfdeccc0adb9faeb2e73fec56f0760658e759a143e6876fb`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a76c78501fbd32c96667efc8c07506d8a4b52d8ee80f1dd12c5184e92e7fdd`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:dae8f4fff8ee8c708720c295f15d74bd7cc45a4334c7a7ed14a5ee3570d492e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9481704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4766864f845629917a8e179a204f361b52567e1c616e9a218c2658dd864a2a7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-armhf.tar.gz / # buildkit
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
	-	`sha256:0f01aea641831b6eaaa7bf504034e5dae031ca857cca80964061df5ea6eea1fd`  
		Last Modified: Fri, 14 Feb 2025 18:28:36 GMT  
		Size: 3.2 MB (3160833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe8ee13420aca9cff4c4da8e0e5adde46e151e86f892da88833cfd617311a0`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 296.2 KB (296177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a586eed463f7a84ba7e62c4e44890f66f66ec4177a3661b6ca216fb16a1197`  
		Last Modified: Fri, 14 Feb 2025 22:09:34 GMT  
		Size: 6.0 MB (6024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0401e68d47e3642ffa60c7b93765856dde64d801eeddec9d94c610200a9d50a5`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0878a23b07d0ff89c4aa4c2ccaf3c7bcf9c7f19b4a528eb0c1c5958a6b8bb780`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:3f34b7b055647d4dbd573edcb91fe341c32636863b0a46f62512ee8f2e95f2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61e1507da9470450f1dd13a5b5292be362a92d813598a0c425a3eba1e1498ef`

```dockerfile
```

-	Layers:
	-	`sha256:66fa3fe4df8aeb5c7a907d6f5a37df3843b547af92231416c14b6c6180eb86a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:6f67febdf3bc889a0177cfe053932d8aab43069501e20d1238e5998dc0b0c9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9226183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85b451c0fb857aca5abed4025f5bd717867768bb3583532cf934fb766921b6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-armv7.tar.gz / # buildkit
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
	-	`sha256:add8bf880239c61df6b8fb5468202d0c151ada0960cd3c2691007322655b41a7`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 2.9 MB (2913220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb5ecea2df3f1350367f83ef9f25f66fca530c1d8418d0b67723052ab3c947`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 295.2 KB (295166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b5de8c73453f44399c3c9ec4d1aa5cd5ddd4077e7b9a8a04c005470d5b28f`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffef9a37654e4e40d3263a377e0cd650f8f574f025cb1da5e8aa2fd15a56cf1`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc8021da8780644e7f2b30e8bb843962ea89c709644713b6d28055cbc2d854`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:aab2a2c3f62aab7fdbb4386626f0918ac34c6f28f770c5e4b910894a19dbefbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9aa8661937173c75d9d5dc7a6486fc7707cbed342f389082c312af6a728d1cd`

```dockerfile
```

-	Layers:
	-	`sha256:59133632b395d7351d3c0bb3aedc980dd89dd2610c19efa7fc25da239d673609`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1970e71b094e5b797deb75611d0a98cd09880f898ae91b4f82ba89fd57520d3d`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 14.2 KB (14153 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:fa647fc1e5d5df7d8d923fb6332aab8e78783f8fca1a1394efb4011f68f5a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9465812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33eeff39e0aaabe61ca826fd7502396183462451be0783133e1a8fa944fc7350`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
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
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 12:05:04 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaad1488a8714e2cc69c2d60095bc20bf1b00df2cbd398f4dc6a36e1abf207`  
		Last Modified: Fri, 14 Feb 2025 22:23:25 GMT  
		Size: 297.8 KB (297838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6b3f59ebc2e050b970e37757f7a57120b76c52798fcf5aaf1dc6eb8d8e8b47`  
		Last Modified: Fri, 14 Feb 2025 22:23:25 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd39ca3613a666408241996cb540196c3a89d30375c8f12b33b9cd4fd7530e6f`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb6d98388d2ab9e73e34a33bc0795566eefbdc2be62c3d8e63f8d44d21d6ec`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:1aa1079885b640a7fb6c01d680c6b50b7cbc9d0ef4905bf34d5099d8fa74dc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdc6b7dae415da31a28825768e58ec52e16959bf5db56ce9b32a5feeef03767`

```dockerfile
```

-	Layers:
	-	`sha256:c4472e68032e1ca292888794e317e1ea0b892cc834999c96b4acf159c1355b94`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a5ce400b19e271e46772e9b6dbabc4a372acb92f7693cc032c465c94ee0a8d`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 14.2 KB (14183 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:10606c79c136c19a8d0e69acb08932b0de4bfdad8fa5e0fb193033f89afb718e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9348229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dd9882a38a66fc185011f804fac82027e193389da7256cd460141db48b27cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-ppc64le.tar.gz / # buildkit
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
	-	`sha256:3328e3c235e7d1731238778d35cdabc664a01e783c0ffd0faa9e6a0c759c4646`  
		Last Modified: Fri, 14 Feb 2025 12:05:06 GMT  
		Size: 3.4 MB (3360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e98f03b75131dd03d21db367eeddeb8b5a826b435500169b442f32692ddcf`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 298.3 KB (298257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc4c076544893d11b7abac2b20c9d950530832a23c7a68aa255c064b826dc84`  
		Last Modified: Fri, 14 Feb 2025 21:51:26 GMT  
		Size: 5.7 MB (5689220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608a80ad7912ecc5679a590cd4bb79e5b7d8272beba8224424a6dd6b86d4477`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b996b58d4a65e936f55f8197b580b23338ef297fbd6b4f9a95776c4895a526b3`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:8f4deb927eecce4f8f7b6a93a7c8a3d9bdf419b4be5cd17caa0ffbd9ff8cc715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 KB (192256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f82b70af3810d530b51e44e29b5ac9bd824be602c7460457722237b7c1c0a55`

```dockerfile
```

-	Layers:
	-	`sha256:81a881e7c0c9c46a4c2fa2c8426890c7e138d079df030b8d58573002c07e25e4`  
		Last Modified: Fri, 14 Feb 2025 21:51:26 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9fd8d94c257b5cfdd6dcb57c64d7a4431696c2074d2d0896ae36f18304c4d3`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:d57627e6eaff3c9acbb1af5a889f9c04ebab46d4018b269e106b64f086aa6103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9689682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b1b5a3a1cec14d181b92df3357798ad62c589cc85ec2ef5d4d2c8dd7c66344`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-s390x.tar.gz / # buildkit
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
	-	`sha256:9d66a7fc8569c55ed7be55ca8d841e62d7dc7948a5b9d3ac10d7d462a706d48c`  
		Last Modified: Fri, 14 Feb 2025 12:05:07 GMT  
		Size: 3.2 MB (3232868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf189123ab9158cbdcedbc64afd064aab52289eb5972d4ee2757240c8328e6de`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 296.2 KB (296182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88474e8748586491bd11b4a964ec89d87acd05c3d1282b9b2714d8f66e0e586d`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a58d287f795ee0d5827b60357d1236ee5404f62efce6df39031dc0cc48138f6`  
		Last Modified: Fri, 14 Feb 2025 22:25:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eecc2312f415f0b8a833722640916a65420b40808aa0c7db2fe0877b1b65216`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:5733c871d98809734f3473fdf8543af2296a21460091120831358b706e0c2a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 KB (192176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccedbb86e1fab22893d32d3f992003b21f6772e6795e01ab7611a6bbf81103a6`

```dockerfile
```

-	Layers:
	-	`sha256:8617fa9130c4db3c616aac7abbbfc44207d7387a43973ba965cc538aee9f617b`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ee0fc123440180ad56dbb3639d50d42c8e882e7dcc1c662f421b4f7beaeda9`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8`

```console
$ docker pull registry@sha256:a3d8aaa63ed8681a604f1dea0aa03f100d5895b6a58ace528858a7b332415373
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
$ docker pull registry@sha256:46faa9a1ae6813194b53921a370f2f4f8c5e1aae228a89bceafef5847a6a3278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b2eb03618e749084668eaff68cff8f81dda12d06ac641be7a6398b82a6f25b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
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
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbdd6c6894b7d41bab22098e3a0fff77de4a231f5b407224ead5b3f26cc4ff3`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 295.7 KB (295684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e82f80af0de06ae95429a79d00ae7e98c0f5ded5555a06c024757d81371a742`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3493bf46cdec3b8ecbb96c0b1cd7fc5f90964306b7c55a0136dac0beeaa627f9`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d464ea18732475d5c3591f1eba3ee96a974808791a5fe103ea1c33199f2eb74`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:b79491fc7716809e3eb28bb866c952b670ec72edc28ac84dd423d28b94e22f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 KB (194127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a15a454b11b760c2f0143e9b2a8155c43f2bab9bf68ff9d023e769472c91c`

```dockerfile
```

-	Layers:
	-	`sha256:b537bf6d11468f33bfdeccc0adb9faeb2e73fec56f0760658e759a143e6876fb`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a76c78501fbd32c96667efc8c07506d8a4b52d8ee80f1dd12c5184e92e7fdd`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:dae8f4fff8ee8c708720c295f15d74bd7cc45a4334c7a7ed14a5ee3570d492e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9481704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4766864f845629917a8e179a204f361b52567e1c616e9a218c2658dd864a2a7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-armhf.tar.gz / # buildkit
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
	-	`sha256:0f01aea641831b6eaaa7bf504034e5dae031ca857cca80964061df5ea6eea1fd`  
		Last Modified: Fri, 14 Feb 2025 18:28:36 GMT  
		Size: 3.2 MB (3160833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe8ee13420aca9cff4c4da8e0e5adde46e151e86f892da88833cfd617311a0`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 296.2 KB (296177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a586eed463f7a84ba7e62c4e44890f66f66ec4177a3661b6ca216fb16a1197`  
		Last Modified: Fri, 14 Feb 2025 22:09:34 GMT  
		Size: 6.0 MB (6024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0401e68d47e3642ffa60c7b93765856dde64d801eeddec9d94c610200a9d50a5`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0878a23b07d0ff89c4aa4c2ccaf3c7bcf9c7f19b4a528eb0c1c5958a6b8bb780`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:3f34b7b055647d4dbd573edcb91fe341c32636863b0a46f62512ee8f2e95f2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61e1507da9470450f1dd13a5b5292be362a92d813598a0c425a3eba1e1498ef`

```dockerfile
```

-	Layers:
	-	`sha256:66fa3fe4df8aeb5c7a907d6f5a37df3843b547af92231416c14b6c6180eb86a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:6f67febdf3bc889a0177cfe053932d8aab43069501e20d1238e5998dc0b0c9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9226183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85b451c0fb857aca5abed4025f5bd717867768bb3583532cf934fb766921b6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-armv7.tar.gz / # buildkit
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
	-	`sha256:add8bf880239c61df6b8fb5468202d0c151ada0960cd3c2691007322655b41a7`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 2.9 MB (2913220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb5ecea2df3f1350367f83ef9f25f66fca530c1d8418d0b67723052ab3c947`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 295.2 KB (295166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b5de8c73453f44399c3c9ec4d1aa5cd5ddd4077e7b9a8a04c005470d5b28f`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffef9a37654e4e40d3263a377e0cd650f8f574f025cb1da5e8aa2fd15a56cf1`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc8021da8780644e7f2b30e8bb843962ea89c709644713b6d28055cbc2d854`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:aab2a2c3f62aab7fdbb4386626f0918ac34c6f28f770c5e4b910894a19dbefbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9aa8661937173c75d9d5dc7a6486fc7707cbed342f389082c312af6a728d1cd`

```dockerfile
```

-	Layers:
	-	`sha256:59133632b395d7351d3c0bb3aedc980dd89dd2610c19efa7fc25da239d673609`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1970e71b094e5b797deb75611d0a98cd09880f898ae91b4f82ba89fd57520d3d`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 14.2 KB (14153 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:fa647fc1e5d5df7d8d923fb6332aab8e78783f8fca1a1394efb4011f68f5a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9465812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33eeff39e0aaabe61ca826fd7502396183462451be0783133e1a8fa944fc7350`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
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
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 12:05:04 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaad1488a8714e2cc69c2d60095bc20bf1b00df2cbd398f4dc6a36e1abf207`  
		Last Modified: Fri, 14 Feb 2025 22:23:25 GMT  
		Size: 297.8 KB (297838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6b3f59ebc2e050b970e37757f7a57120b76c52798fcf5aaf1dc6eb8d8e8b47`  
		Last Modified: Fri, 14 Feb 2025 22:23:25 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd39ca3613a666408241996cb540196c3a89d30375c8f12b33b9cd4fd7530e6f`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb6d98388d2ab9e73e34a33bc0795566eefbdc2be62c3d8e63f8d44d21d6ec`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:1aa1079885b640a7fb6c01d680c6b50b7cbc9d0ef4905bf34d5099d8fa74dc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdc6b7dae415da31a28825768e58ec52e16959bf5db56ce9b32a5feeef03767`

```dockerfile
```

-	Layers:
	-	`sha256:c4472e68032e1ca292888794e317e1ea0b892cc834999c96b4acf159c1355b94`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a5ce400b19e271e46772e9b6dbabc4a372acb92f7693cc032c465c94ee0a8d`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 14.2 KB (14183 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:10606c79c136c19a8d0e69acb08932b0de4bfdad8fa5e0fb193033f89afb718e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9348229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dd9882a38a66fc185011f804fac82027e193389da7256cd460141db48b27cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-ppc64le.tar.gz / # buildkit
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
	-	`sha256:3328e3c235e7d1731238778d35cdabc664a01e783c0ffd0faa9e6a0c759c4646`  
		Last Modified: Fri, 14 Feb 2025 12:05:06 GMT  
		Size: 3.4 MB (3360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e98f03b75131dd03d21db367eeddeb8b5a826b435500169b442f32692ddcf`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 298.3 KB (298257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc4c076544893d11b7abac2b20c9d950530832a23c7a68aa255c064b826dc84`  
		Last Modified: Fri, 14 Feb 2025 21:51:26 GMT  
		Size: 5.7 MB (5689220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608a80ad7912ecc5679a590cd4bb79e5b7d8272beba8224424a6dd6b86d4477`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b996b58d4a65e936f55f8197b580b23338ef297fbd6b4f9a95776c4895a526b3`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:8f4deb927eecce4f8f7b6a93a7c8a3d9bdf419b4be5cd17caa0ffbd9ff8cc715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 KB (192256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f82b70af3810d530b51e44e29b5ac9bd824be602c7460457722237b7c1c0a55`

```dockerfile
```

-	Layers:
	-	`sha256:81a881e7c0c9c46a4c2fa2c8426890c7e138d079df030b8d58573002c07e25e4`  
		Last Modified: Fri, 14 Feb 2025 21:51:26 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9fd8d94c257b5cfdd6dcb57c64d7a4431696c2074d2d0896ae36f18304c4d3`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:d57627e6eaff3c9acbb1af5a889f9c04ebab46d4018b269e106b64f086aa6103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9689682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b1b5a3a1cec14d181b92df3357798ad62c589cc85ec2ef5d4d2c8dd7c66344`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-s390x.tar.gz / # buildkit
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
	-	`sha256:9d66a7fc8569c55ed7be55ca8d841e62d7dc7948a5b9d3ac10d7d462a706d48c`  
		Last Modified: Fri, 14 Feb 2025 12:05:07 GMT  
		Size: 3.2 MB (3232868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf189123ab9158cbdcedbc64afd064aab52289eb5972d4ee2757240c8328e6de`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 296.2 KB (296182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88474e8748586491bd11b4a964ec89d87acd05c3d1282b9b2714d8f66e0e586d`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a58d287f795ee0d5827b60357d1236ee5404f62efce6df39031dc0cc48138f6`  
		Last Modified: Fri, 14 Feb 2025 22:25:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eecc2312f415f0b8a833722640916a65420b40808aa0c7db2fe0877b1b65216`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:5733c871d98809734f3473fdf8543af2296a21460091120831358b706e0c2a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 KB (192176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccedbb86e1fab22893d32d3f992003b21f6772e6795e01ab7611a6bbf81103a6`

```dockerfile
```

-	Layers:
	-	`sha256:8617fa9130c4db3c616aac7abbbfc44207d7387a43973ba965cc538aee9f617b`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ee0fc123440180ad56dbb3639d50d42c8e882e7dcc1c662f421b4f7beaeda9`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8.3`

```console
$ docker pull registry@sha256:a3d8aaa63ed8681a604f1dea0aa03f100d5895b6a58ace528858a7b332415373
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
$ docker pull registry@sha256:46faa9a1ae6813194b53921a370f2f4f8c5e1aae228a89bceafef5847a6a3278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b2eb03618e749084668eaff68cff8f81dda12d06ac641be7a6398b82a6f25b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
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
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbdd6c6894b7d41bab22098e3a0fff77de4a231f5b407224ead5b3f26cc4ff3`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 295.7 KB (295684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e82f80af0de06ae95429a79d00ae7e98c0f5ded5555a06c024757d81371a742`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3493bf46cdec3b8ecbb96c0b1cd7fc5f90964306b7c55a0136dac0beeaa627f9`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d464ea18732475d5c3591f1eba3ee96a974808791a5fe103ea1c33199f2eb74`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:b79491fc7716809e3eb28bb866c952b670ec72edc28ac84dd423d28b94e22f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 KB (194127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a15a454b11b760c2f0143e9b2a8155c43f2bab9bf68ff9d023e769472c91c`

```dockerfile
```

-	Layers:
	-	`sha256:b537bf6d11468f33bfdeccc0adb9faeb2e73fec56f0760658e759a143e6876fb`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a76c78501fbd32c96667efc8c07506d8a4b52d8ee80f1dd12c5184e92e7fdd`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v6

```console
$ docker pull registry@sha256:dae8f4fff8ee8c708720c295f15d74bd7cc45a4334c7a7ed14a5ee3570d492e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9481704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4766864f845629917a8e179a204f361b52567e1c616e9a218c2658dd864a2a7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-armhf.tar.gz / # buildkit
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
	-	`sha256:0f01aea641831b6eaaa7bf504034e5dae031ca857cca80964061df5ea6eea1fd`  
		Last Modified: Fri, 14 Feb 2025 18:28:36 GMT  
		Size: 3.2 MB (3160833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe8ee13420aca9cff4c4da8e0e5adde46e151e86f892da88833cfd617311a0`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 296.2 KB (296177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a586eed463f7a84ba7e62c4e44890f66f66ec4177a3661b6ca216fb16a1197`  
		Last Modified: Fri, 14 Feb 2025 22:09:34 GMT  
		Size: 6.0 MB (6024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0401e68d47e3642ffa60c7b93765856dde64d801eeddec9d94c610200a9d50a5`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0878a23b07d0ff89c4aa4c2ccaf3c7bcf9c7f19b4a528eb0c1c5958a6b8bb780`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:3f34b7b055647d4dbd573edcb91fe341c32636863b0a46f62512ee8f2e95f2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61e1507da9470450f1dd13a5b5292be362a92d813598a0c425a3eba1e1498ef`

```dockerfile
```

-	Layers:
	-	`sha256:66fa3fe4df8aeb5c7a907d6f5a37df3843b547af92231416c14b6c6180eb86a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v7

```console
$ docker pull registry@sha256:6f67febdf3bc889a0177cfe053932d8aab43069501e20d1238e5998dc0b0c9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9226183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85b451c0fb857aca5abed4025f5bd717867768bb3583532cf934fb766921b6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-armv7.tar.gz / # buildkit
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
	-	`sha256:add8bf880239c61df6b8fb5468202d0c151ada0960cd3c2691007322655b41a7`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 2.9 MB (2913220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb5ecea2df3f1350367f83ef9f25f66fca530c1d8418d0b67723052ab3c947`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 295.2 KB (295166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b5de8c73453f44399c3c9ec4d1aa5cd5ddd4077e7b9a8a04c005470d5b28f`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffef9a37654e4e40d3263a377e0cd650f8f574f025cb1da5e8aa2fd15a56cf1`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc8021da8780644e7f2b30e8bb843962ea89c709644713b6d28055cbc2d854`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:aab2a2c3f62aab7fdbb4386626f0918ac34c6f28f770c5e4b910894a19dbefbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9aa8661937173c75d9d5dc7a6486fc7707cbed342f389082c312af6a728d1cd`

```dockerfile
```

-	Layers:
	-	`sha256:59133632b395d7351d3c0bb3aedc980dd89dd2610c19efa7fc25da239d673609`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1970e71b094e5b797deb75611d0a98cd09880f898ae91b4f82ba89fd57520d3d`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 14.2 KB (14153 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:fa647fc1e5d5df7d8d923fb6332aab8e78783f8fca1a1394efb4011f68f5a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9465812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33eeff39e0aaabe61ca826fd7502396183462451be0783133e1a8fa944fc7350`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
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
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 12:05:04 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaad1488a8714e2cc69c2d60095bc20bf1b00df2cbd398f4dc6a36e1abf207`  
		Last Modified: Fri, 14 Feb 2025 22:23:25 GMT  
		Size: 297.8 KB (297838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6b3f59ebc2e050b970e37757f7a57120b76c52798fcf5aaf1dc6eb8d8e8b47`  
		Last Modified: Fri, 14 Feb 2025 22:23:25 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd39ca3613a666408241996cb540196c3a89d30375c8f12b33b9cd4fd7530e6f`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb6d98388d2ab9e73e34a33bc0795566eefbdc2be62c3d8e63f8d44d21d6ec`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:1aa1079885b640a7fb6c01d680c6b50b7cbc9d0ef4905bf34d5099d8fa74dc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdc6b7dae415da31a28825768e58ec52e16959bf5db56ce9b32a5feeef03767`

```dockerfile
```

-	Layers:
	-	`sha256:c4472e68032e1ca292888794e317e1ea0b892cc834999c96b4acf159c1355b94`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a5ce400b19e271e46772e9b6dbabc4a372acb92f7693cc032c465c94ee0a8d`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 14.2 KB (14183 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; ppc64le

```console
$ docker pull registry@sha256:10606c79c136c19a8d0e69acb08932b0de4bfdad8fa5e0fb193033f89afb718e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9348229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dd9882a38a66fc185011f804fac82027e193389da7256cd460141db48b27cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-ppc64le.tar.gz / # buildkit
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
	-	`sha256:3328e3c235e7d1731238778d35cdabc664a01e783c0ffd0faa9e6a0c759c4646`  
		Last Modified: Fri, 14 Feb 2025 12:05:06 GMT  
		Size: 3.4 MB (3360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e98f03b75131dd03d21db367eeddeb8b5a826b435500169b442f32692ddcf`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 298.3 KB (298257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc4c076544893d11b7abac2b20c9d950530832a23c7a68aa255c064b826dc84`  
		Last Modified: Fri, 14 Feb 2025 21:51:26 GMT  
		Size: 5.7 MB (5689220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608a80ad7912ecc5679a590cd4bb79e5b7d8272beba8224424a6dd6b86d4477`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b996b58d4a65e936f55f8197b580b23338ef297fbd6b4f9a95776c4895a526b3`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:8f4deb927eecce4f8f7b6a93a7c8a3d9bdf419b4be5cd17caa0ffbd9ff8cc715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 KB (192256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f82b70af3810d530b51e44e29b5ac9bd824be602c7460457722237b7c1c0a55`

```dockerfile
```

-	Layers:
	-	`sha256:81a881e7c0c9c46a4c2fa2c8426890c7e138d079df030b8d58573002c07e25e4`  
		Last Modified: Fri, 14 Feb 2025 21:51:26 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9fd8d94c257b5cfdd6dcb57c64d7a4431696c2074d2d0896ae36f18304c4d3`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:d57627e6eaff3c9acbb1af5a889f9c04ebab46d4018b269e106b64f086aa6103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9689682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b1b5a3a1cec14d181b92df3357798ad62c589cc85ec2ef5d4d2c8dd7c66344`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-s390x.tar.gz / # buildkit
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
	-	`sha256:9d66a7fc8569c55ed7be55ca8d841e62d7dc7948a5b9d3ac10d7d462a706d48c`  
		Last Modified: Fri, 14 Feb 2025 12:05:07 GMT  
		Size: 3.2 MB (3232868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf189123ab9158cbdcedbc64afd064aab52289eb5972d4ee2757240c8328e6de`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 296.2 KB (296182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88474e8748586491bd11b4a964ec89d87acd05c3d1282b9b2714d8f66e0e586d`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a58d287f795ee0d5827b60357d1236ee5404f62efce6df39031dc0cc48138f6`  
		Last Modified: Fri, 14 Feb 2025 22:25:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eecc2312f415f0b8a833722640916a65420b40808aa0c7db2fe0877b1b65216`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:5733c871d98809734f3473fdf8543af2296a21460091120831358b706e0c2a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 KB (192176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccedbb86e1fab22893d32d3f992003b21f6772e6795e01ab7611a6bbf81103a6`

```dockerfile
```

-	Layers:
	-	`sha256:8617fa9130c4db3c616aac7abbbfc44207d7387a43973ba965cc538aee9f617b`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ee0fc123440180ad56dbb3639d50d42c8e882e7dcc1c662f421b4f7beaeda9`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0-rc.4`

```console
$ docker pull registry@sha256:3f48c732a2fc34a32c5ae3c1cdce1b8d5021b462bc7aaefd771fd5bda4538506
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

### `registry:3.0.0-rc.4` - linux; amd64

```console
$ docker pull registry@sha256:9d1ffb8b1b83ed483ecd931be0e34c30dc028d2682b3fe08aad471b117483b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18333399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad06d4347c62eaa826eb1743ded71d8a2605c778d707fee127c3859456e4439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
RUN set -eux; 	version='3.0.0-rc.4'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='bdd57a6c9fa802bb72407936045b323aadc61abfd7fac6e55364dee8a1d18d50' ;; 		aarch64) arch='arm64';   sha256='94bdf16a7813a7a501cc23bf7c8a40625456cbe1b9863b4626caddc801b7071b' ;; 		armhf)   arch='armv6';   sha256='f9d7928264c05d4d5b55e270d9f49eca1376d7aeade34ea80513f82bac4ea3ae' ;; 		armv7)   arch='armv7';   sha256='ce384d85cfd260245e7845d9512a89fe1d790d5b6c09c5fc6907326251cd2db2' ;; 		ppc64le) arch='ppc64le'; sha256='e15a7883883bc054f04c88e99ea8b80e7bb36eed86bc5dc3a5604e138339fa08' ;; 		s390x)   arch='s390x';   sha256='7d3879657f7184bd4315fcf05154dd87f3045ce256380fdfd6a9bc34a094296b' ;; 		riscv64) arch='riscv64'; sha256='94cc989b4e16b86abe221c2cc8adc67199d824dbff891d7da87f981dd9353409' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
VOLUME [/var/lib/registry]
# Mon, 24 Mar 2025 18:51:47 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 24 Mar 2025 18:51:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ee046e3c25c1f5a165fb73e6fd804eb63dac25c3e2f1fac76e87171e79610e`  
		Last Modified: Wed, 26 Mar 2025 16:23:05 GMT  
		Size: 294.9 KB (294893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef9f7f5fcf0f6115c6910cced88bcf754d2b05245e3c3a7bfbf8a9c3d89c5f3`  
		Last Modified: Wed, 26 Mar 2025 16:23:06 GMT  
		Size: 14.4 MB (14395649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e5eb710f9fddd01fae1551df1addf851f0716a7e1f8e9c3c9d41a0354146e`  
		Last Modified: Wed, 26 Mar 2025 16:23:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de524212e4780edea609fbf800a7ac70281f0241ad1bedc874f94c09090683a1`  
		Last Modified: Wed, 26 Mar 2025 16:23:05 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.4` - unknown; unknown

```console
$ docker pull registry@sha256:1ec2cae07f3a492cfca8bf7f5d9dddea1cea701d267a880aad296d197b36a44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 KB (280518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fff03dd110a0bedfbd5259018a55b21dda9f50f85c0583866098e943e992b8`

```dockerfile
```

-	Layers:
	-	`sha256:42223ba22358f2936df00a13ecd14810fec1637563327d9a8c68f6c790da117d`  
		Last Modified: Wed, 26 Mar 2025 16:23:05 GMT  
		Size: 267.1 KB (267061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0c0f5f55d604d5b5fb97ee7c335c218af6c2953cbaeb3890d0c5824f4fba65`  
		Last Modified: Wed, 26 Mar 2025 16:23:05 GMT  
		Size: 13.5 KB (13457 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.4` - linux; arm variant v6

```console
$ docker pull registry@sha256:b6463b802854ee8274fd9354b2bba0b2ce1a8031fcc18cc2ce5c4aca1131b7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17185185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbb7937fb739c5cf51c47943e9bbe121bfc7a7435cb271e27973209c554d977`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
RUN set -eux; 	version='3.0.0-rc.4'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='bdd57a6c9fa802bb72407936045b323aadc61abfd7fac6e55364dee8a1d18d50' ;; 		aarch64) arch='arm64';   sha256='94bdf16a7813a7a501cc23bf7c8a40625456cbe1b9863b4626caddc801b7071b' ;; 		armhf)   arch='armv6';   sha256='f9d7928264c05d4d5b55e270d9f49eca1376d7aeade34ea80513f82bac4ea3ae' ;; 		armv7)   arch='armv7';   sha256='ce384d85cfd260245e7845d9512a89fe1d790d5b6c09c5fc6907326251cd2db2' ;; 		ppc64le) arch='ppc64le'; sha256='e15a7883883bc054f04c88e99ea8b80e7bb36eed86bc5dc3a5604e138339fa08' ;; 		s390x)   arch='s390x';   sha256='7d3879657f7184bd4315fcf05154dd87f3045ce256380fdfd6a9bc34a094296b' ;; 		riscv64) arch='riscv64'; sha256='94cc989b4e16b86abe221c2cc8adc67199d824dbff891d7da87f981dd9353409' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
VOLUME [/var/lib/registry]
# Mon, 24 Mar 2025 18:51:47 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 24 Mar 2025 18:51:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:20 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbd41fa3c306c34258201875bf8cfa650a363196fdb1d9cf1244a62d3c8dfe4`  
		Last Modified: Wed, 26 Mar 2025 16:22:07 GMT  
		Size: 13.5 MB (13523591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cac6e530a2beae008e8dfe34ec1ac2af6b640400fb5a9cf7ca489a8bc95cfd2`  
		Last Modified: Wed, 26 Mar 2025 16:22:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f5946ed032165751ddf2e3e9ba3d53be8d23e2222229e197619117bf22f174`  
		Last Modified: Wed, 26 Mar 2025 16:22:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.4` - unknown; unknown

```console
$ docker pull registry@sha256:5cc96405c54d711255f102d1b4b4d127437834691e7f10f4c0044dd66249224a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99faaeefa4e990b199b87325fb5adbd8c668da473bfb3013a1d4009e0bfaf133`

```dockerfile
```

-	Layers:
	-	`sha256:b8214ac291c4e1453d505e731bcee9087b257f6ab800f2388e14be63c09e7047`  
		Last Modified: Wed, 26 Mar 2025 16:22:06 GMT  
		Size: 13.3 KB (13307 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.4` - linux; arm variant v7

```console
$ docker pull registry@sha256:849a67e2f6d3a9685fe8bbaa98d7cf50ed2527b8c49c385bbbbe76cc5a48efd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16908579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc5325b871f332cb64eaf8b85a54313c0de3a1951c7776ed56ca328d474ab3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
RUN set -eux; 	version='3.0.0-rc.4'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='bdd57a6c9fa802bb72407936045b323aadc61abfd7fac6e55364dee8a1d18d50' ;; 		aarch64) arch='arm64';   sha256='94bdf16a7813a7a501cc23bf7c8a40625456cbe1b9863b4626caddc801b7071b' ;; 		armhf)   arch='armv6';   sha256='f9d7928264c05d4d5b55e270d9f49eca1376d7aeade34ea80513f82bac4ea3ae' ;; 		armv7)   arch='armv7';   sha256='ce384d85cfd260245e7845d9512a89fe1d790d5b6c09c5fc6907326251cd2db2' ;; 		ppc64le) arch='ppc64le'; sha256='e15a7883883bc054f04c88e99ea8b80e7bb36eed86bc5dc3a5604e138339fa08' ;; 		s390x)   arch='s390x';   sha256='7d3879657f7184bd4315fcf05154dd87f3045ce256380fdfd6a9bc34a094296b' ;; 		riscv64) arch='riscv64'; sha256='94cc989b4e16b86abe221c2cc8adc67199d824dbff891d7da87f981dd9353409' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
VOLUME [/var/lib/registry]
# Mon, 24 Mar 2025 18:51:47 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 24 Mar 2025 18:51:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 21:47:46 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ce722db79e60a4cff9152581ae51e916521b21956e8944545f6600e7ff98a1`  
		Last Modified: Wed, 26 Mar 2025 16:21:55 GMT  
		Size: 13.5 MB (13514648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091e07f0dcc2931acd8ed38931c2a699619780d6d39badc2625f9c805ff6a6ae`  
		Last Modified: Wed, 26 Mar 2025 16:21:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591e3fb2ef8415923815d4edb2ee63e9f2d5015dcfdfd9da508b243a6b88f964`  
		Last Modified: Wed, 26 Mar 2025 16:21:55 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.4` - unknown; unknown

```console
$ docker pull registry@sha256:a19f065162be9626385c12615827f15cf3685ddcdb1ba1863713d2dbc6ed088c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 KB (280594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f6338acefd0433ae20c81f237de77c6aafb9f747767b691d19f197c43f06fb`

```dockerfile
```

-	Layers:
	-	`sha256:5c68f6402ef8b5cca776eabeffb6b032807152dba2693788d5d5076a80e41b18`  
		Last Modified: Wed, 26 Mar 2025 16:21:55 GMT  
		Size: 267.1 KB (267073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc4437fb9b7a78265ab4747ef00d6bcb957137ab78ad924e1a37bdcbc4a2cdc`  
		Last Modified: Wed, 26 Mar 2025 16:21:55 GMT  
		Size: 13.5 KB (13521 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.4` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:d09099f317d70f2b5ad78f19f55825a5b72e418bdf8ee82744fcf393dacbd796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17589392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71894c13d895e8c2a7c2ad780aa5909e03d70bc57c486f1e6afc9b0693fe249b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
RUN set -eux; 	version='3.0.0-rc.4'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='bdd57a6c9fa802bb72407936045b323aadc61abfd7fac6e55364dee8a1d18d50' ;; 		aarch64) arch='arm64';   sha256='94bdf16a7813a7a501cc23bf7c8a40625456cbe1b9863b4626caddc801b7071b' ;; 		armhf)   arch='armv6';   sha256='f9d7928264c05d4d5b55e270d9f49eca1376d7aeade34ea80513f82bac4ea3ae' ;; 		armv7)   arch='armv7';   sha256='ce384d85cfd260245e7845d9512a89fe1d790d5b6c09c5fc6907326251cd2db2' ;; 		ppc64le) arch='ppc64le'; sha256='e15a7883883bc054f04c88e99ea8b80e7bb36eed86bc5dc3a5604e138339fa08' ;; 		s390x)   arch='s390x';   sha256='7d3879657f7184bd4315fcf05154dd87f3045ce256380fdfd6a9bc34a094296b' ;; 		riscv64) arch='riscv64'; sha256='94cc989b4e16b86abe221c2cc8adc67199d824dbff891d7da87f981dd9353409' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
VOLUME [/var/lib/registry]
# Mon, 24 Mar 2025 18:51:47 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 24 Mar 2025 18:51:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e33b27c9b76515e1154a131a67e2f0fe88ba9e9bc48a1a704c790a0561e068`  
		Last Modified: Mon, 24 Mar 2025 21:29:27 GMT  
		Size: 297.9 KB (297871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a6d2c80d624e2c1407936c1b5c376e3ccb8bf7c65b457cd0ff007527672c5e`  
		Last Modified: Wed, 26 Mar 2025 16:21:52 GMT  
		Size: 13.3 MB (13297881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb400489e0fbab4eac6892fd188e6028d689e7c77f1588a788429e9b931b9cb`  
		Last Modified: Wed, 26 Mar 2025 16:21:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7b9d95485442198489a8de9d22b6ffc99fc985168dd00e7e85e41df852c2ae`  
		Last Modified: Wed, 26 Mar 2025 16:21:52 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.4` - unknown; unknown

```console
$ docker pull registry@sha256:432f29cce605ae4001ba87a626865eb5732aa1ba76420097beb4a85d85c734ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 KB (280621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa3829065d4ca55025fd560f612e80e48a2ef2c4a9048720fa2b0f143da0371`

```dockerfile
```

-	Layers:
	-	`sha256:b34a91b41d09e20a08fc0123873987a7ef04e970405948b6d3ffe4b7e6a342ac`  
		Last Modified: Wed, 26 Mar 2025 16:21:52 GMT  
		Size: 267.1 KB (267081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43e04b5d32efd98bf8efc67c039bb9eb3453dd2ae12079f1a32101fa3de6e6d6`  
		Last Modified: Wed, 26 Mar 2025 16:21:52 GMT  
		Size: 13.5 KB (13540 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.4` - linux; ppc64le

```console
$ docker pull registry@sha256:e76418cb7a0cb2943929296bbf8f76114541e07c23fbf590967eddf5b324fec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16846102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7501dd01401950db08dbd8b0473f7de4b0913ecfde771d542a0e0b09b799af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
RUN set -eux; 	version='3.0.0-rc.4'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='bdd57a6c9fa802bb72407936045b323aadc61abfd7fac6e55364dee8a1d18d50' ;; 		aarch64) arch='arm64';   sha256='94bdf16a7813a7a501cc23bf7c8a40625456cbe1b9863b4626caddc801b7071b' ;; 		armhf)   arch='armv6';   sha256='f9d7928264c05d4d5b55e270d9f49eca1376d7aeade34ea80513f82bac4ea3ae' ;; 		armv7)   arch='armv7';   sha256='ce384d85cfd260245e7845d9512a89fe1d790d5b6c09c5fc6907326251cd2db2' ;; 		ppc64le) arch='ppc64le'; sha256='e15a7883883bc054f04c88e99ea8b80e7bb36eed86bc5dc3a5604e138339fa08' ;; 		s390x)   arch='s390x';   sha256='7d3879657f7184bd4315fcf05154dd87f3045ce256380fdfd6a9bc34a094296b' ;; 		riscv64) arch='riscv64'; sha256='94cc989b4e16b86abe221c2cc8adc67199d824dbff891d7da87f981dd9353409' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
VOLUME [/var/lib/registry]
# Mon, 24 Mar 2025 18:51:47 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 24 Mar 2025 18:51:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27442ea8b4dc6fdf584c0b30a8e1943de4b659fd7ec220499d43ff5c7d4c1c8`  
		Last Modified: Mon, 24 Mar 2025 21:48:27 GMT  
		Size: 298.3 KB (298274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffbd14757fef9c090e2fc488f223c935f73b3e47b7c6c40caac48ddd53452b0`  
		Last Modified: Wed, 26 Mar 2025 16:22:49 GMT  
		Size: 13.0 MB (12972873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204ebff256b7ba8c9796cbc16ce2984996210165b32d08ac84006fac9667111`  
		Last Modified: Wed, 26 Mar 2025 16:22:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e29f927a3b4e7824dddb0770760044005da74de88e8ad9de03dcb2e03490fc5`  
		Last Modified: Wed, 26 Mar 2025 16:22:49 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.4` - unknown; unknown

```console
$ docker pull registry@sha256:369f9a85f1da979c7e410adc25fb1585d49aedf3a0812e80498d5849d628bac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc035136a11764ee86d2733ed9f5f4b24cccd22eecd547a3412fa08ccbd3ed49`

```dockerfile
```

-	Layers:
	-	`sha256:38e2ae9745f48c5d4e20a3ebee60664dbdcae801879ce396ce9bc6313cdb6512`  
		Last Modified: Wed, 26 Mar 2025 16:22:49 GMT  
		Size: 265.1 KB (265126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0e0f31f72b5494b8be37405d9595012803edaa788791c946ad34e7519396aa5`  
		Last Modified: Wed, 26 Mar 2025 16:22:49 GMT  
		Size: 13.5 KB (13485 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.4` - linux; riscv64

```console
$ docker pull registry@sha256:974d987b61946f8f7fc37a5f93b939c9d045539ec8d45995a1274fa268fc57e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17329387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b236a6733eb4df1033413e793f58f54941978f20cd43820f6e3cfd40fb208667`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
RUN set -eux; 	version='3.0.0-rc.4'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='bdd57a6c9fa802bb72407936045b323aadc61abfd7fac6e55364dee8a1d18d50' ;; 		aarch64) arch='arm64';   sha256='94bdf16a7813a7a501cc23bf7c8a40625456cbe1b9863b4626caddc801b7071b' ;; 		armhf)   arch='armv6';   sha256='f9d7928264c05d4d5b55e270d9f49eca1376d7aeade34ea80513f82bac4ea3ae' ;; 		armv7)   arch='armv7';   sha256='ce384d85cfd260245e7845d9512a89fe1d790d5b6c09c5fc6907326251cd2db2' ;; 		ppc64le) arch='ppc64le'; sha256='e15a7883883bc054f04c88e99ea8b80e7bb36eed86bc5dc3a5604e138339fa08' ;; 		s390x)   arch='s390x';   sha256='7d3879657f7184bd4315fcf05154dd87f3045ce256380fdfd6a9bc34a094296b' ;; 		riscv64) arch='riscv64'; sha256='94cc989b4e16b86abe221c2cc8adc67199d824dbff891d7da87f981dd9353409' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
VOLUME [/var/lib/registry]
# Mon, 24 Mar 2025 18:51:47 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 24 Mar 2025 18:51:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 05:52:00 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94da5d35721951125f064f866b8d9f4791cd555c6e2ccb1cb0243b1d171a87d`  
		Last Modified: Wed, 26 Mar 2025 16:23:47 GMT  
		Size: 13.7 MB (13681992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3481871cd928b4349783fb166c20b765523439b43c4ad5f6e99ec9e5fd23b53f`  
		Last Modified: Wed, 26 Mar 2025 16:23:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdc1f953820c862b85ba2a0568196dca9c407caf7b48bf27396a11a44d0b8f0`  
		Last Modified: Wed, 26 Mar 2025 16:23:45 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.4` - unknown; unknown

```console
$ docker pull registry@sha256:34670f421f90b64d2134f78b41eb9da0a642ece699d4729360df507d2b188d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16145d6cd4f2ba60a7219e406bebb1083d51bc64596e8d62b1927914132f735c`

```dockerfile
```

-	Layers:
	-	`sha256:8a669662261d1003c19c57d1dd977de216c2519b5292218bcd8e5d541de171ca`  
		Last Modified: Wed, 26 Mar 2025 16:23:45 GMT  
		Size: 265.1 KB (265122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1c506d985faee3374c2a8b89f0b57380794577da437e0cbaf998a123b4c975`  
		Last Modified: Wed, 26 Mar 2025 16:23:45 GMT  
		Size: 13.5 KB (13485 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.4` - linux; s390x

```console
$ docker pull registry@sha256:3884800dd444223a0e337fd56c3d929a8376e5adfb0095283c1b22ac9b50f077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17621871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41268c6c62a91ada4e6cd79ed9aad20d6c48757cbb593320d5afcd6655b5d545`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
RUN set -eux; 	version='3.0.0-rc.4'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='bdd57a6c9fa802bb72407936045b323aadc61abfd7fac6e55364dee8a1d18d50' ;; 		aarch64) arch='arm64';   sha256='94bdf16a7813a7a501cc23bf7c8a40625456cbe1b9863b4626caddc801b7071b' ;; 		armhf)   arch='armv6';   sha256='f9d7928264c05d4d5b55e270d9f49eca1376d7aeade34ea80513f82bac4ea3ae' ;; 		armv7)   arch='armv7';   sha256='ce384d85cfd260245e7845d9512a89fe1d790d5b6c09c5fc6907326251cd2db2' ;; 		ppc64le) arch='ppc64le'; sha256='e15a7883883bc054f04c88e99ea8b80e7bb36eed86bc5dc3a5604e138339fa08' ;; 		s390x)   arch='s390x';   sha256='7d3879657f7184bd4315fcf05154dd87f3045ce256380fdfd6a9bc34a094296b' ;; 		riscv64) arch='riscv64'; sha256='94cc989b4e16b86abe221c2cc8adc67199d824dbff891d7da87f981dd9353409' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
VOLUME [/var/lib/registry]
# Mon, 24 Mar 2025 18:51:47 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 24 Mar 2025 18:51:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 18:51:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 18:51:47 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be80be2c55902add1c4b1f14066b1b4da724beaa2e355b53f8dd45b4887d9b9c`  
		Last Modified: Mon, 24 Mar 2025 21:26:52 GMT  
		Size: 296.2 KB (296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67110b659907af94a6bd3ab16d3103a4bf97016f66d1cf8ed5821112472ff1c`  
		Last Modified: Wed, 26 Mar 2025 16:23:16 GMT  
		Size: 13.9 MB (13857512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acfe137e15f106dcf3943788d3387e748b71c1cc16b486c78e9e8d581b08cad`  
		Last Modified: Wed, 26 Mar 2025 16:23:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d44d3cec11a8541a5cb0c416b0bc120f9e55573d33bfb628cca66be13eb067e`  
		Last Modified: Wed, 26 Mar 2025 16:23:16 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.4` - unknown; unknown

```console
$ docker pull registry@sha256:c0cafd689c119f8451a07aacde3742b08274d587ceb51cd94dea3d3228c9325b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4644746b4b708847a8c4be426ff96238d8dd2b8b2b9254e172a110ab68c1d199`

```dockerfile
```

-	Layers:
	-	`sha256:b006841f7e61575a5555f848464bd607c463906aeab8af513134ccbe0e5de38f`  
		Last Modified: Wed, 26 Mar 2025 16:23:16 GMT  
		Size: 265.1 KB (265100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdc76a2f9c304a54f50a9c96393b63d97fe9687a22e470ff424763e8e4f279f0`  
		Last Modified: Wed, 26 Mar 2025 16:23:15 GMT  
		Size: 13.5 KB (13457 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:a3d8aaa63ed8681a604f1dea0aa03f100d5895b6a58ace528858a7b332415373
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
$ docker pull registry@sha256:46faa9a1ae6813194b53921a370f2f4f8c5e1aae228a89bceafef5847a6a3278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b2eb03618e749084668eaff68cff8f81dda12d06ac641be7a6398b82a6f25b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
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
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbdd6c6894b7d41bab22098e3a0fff77de4a231f5b407224ead5b3f26cc4ff3`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 295.7 KB (295684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e82f80af0de06ae95429a79d00ae7e98c0f5ded5555a06c024757d81371a742`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3493bf46cdec3b8ecbb96c0b1cd7fc5f90964306b7c55a0136dac0beeaa627f9`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d464ea18732475d5c3591f1eba3ee96a974808791a5fe103ea1c33199f2eb74`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:b79491fc7716809e3eb28bb866c952b670ec72edc28ac84dd423d28b94e22f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 KB (194127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a15a454b11b760c2f0143e9b2a8155c43f2bab9bf68ff9d023e769472c91c`

```dockerfile
```

-	Layers:
	-	`sha256:b537bf6d11468f33bfdeccc0adb9faeb2e73fec56f0760658e759a143e6876fb`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a76c78501fbd32c96667efc8c07506d8a4b52d8ee80f1dd12c5184e92e7fdd`  
		Last Modified: Fri, 14 Feb 2025 19:23:58 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:dae8f4fff8ee8c708720c295f15d74bd7cc45a4334c7a7ed14a5ee3570d492e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9481704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4766864f845629917a8e179a204f361b52567e1c616e9a218c2658dd864a2a7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-armhf.tar.gz / # buildkit
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
	-	`sha256:0f01aea641831b6eaaa7bf504034e5dae031ca857cca80964061df5ea6eea1fd`  
		Last Modified: Fri, 14 Feb 2025 18:28:36 GMT  
		Size: 3.2 MB (3160833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe8ee13420aca9cff4c4da8e0e5adde46e151e86f892da88833cfd617311a0`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 296.2 KB (296177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a586eed463f7a84ba7e62c4e44890f66f66ec4177a3661b6ca216fb16a1197`  
		Last Modified: Fri, 14 Feb 2025 22:09:34 GMT  
		Size: 6.0 MB (6024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0401e68d47e3642ffa60c7b93765856dde64d801eeddec9d94c610200a9d50a5`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0878a23b07d0ff89c4aa4c2ccaf3c7bcf9c7f19b4a528eb0c1c5958a6b8bb780`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:3f34b7b055647d4dbd573edcb91fe341c32636863b0a46f62512ee8f2e95f2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61e1507da9470450f1dd13a5b5292be362a92d813598a0c425a3eba1e1498ef`

```dockerfile
```

-	Layers:
	-	`sha256:66fa3fe4df8aeb5c7a907d6f5a37df3843b547af92231416c14b6c6180eb86a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:33 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:6f67febdf3bc889a0177cfe053932d8aab43069501e20d1238e5998dc0b0c9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9226183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85b451c0fb857aca5abed4025f5bd717867768bb3583532cf934fb766921b6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-armv7.tar.gz / # buildkit
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
	-	`sha256:add8bf880239c61df6b8fb5468202d0c151ada0960cd3c2691007322655b41a7`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 2.9 MB (2913220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb5ecea2df3f1350367f83ef9f25f66fca530c1d8418d0b67723052ab3c947`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 295.2 KB (295166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b5de8c73453f44399c3c9ec4d1aa5cd5ddd4077e7b9a8a04c005470d5b28f`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffef9a37654e4e40d3263a377e0cd650f8f574f025cb1da5e8aa2fd15a56cf1`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc8021da8780644e7f2b30e8bb843962ea89c709644713b6d28055cbc2d854`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:aab2a2c3f62aab7fdbb4386626f0918ac34c6f28f770c5e4b910894a19dbefbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9aa8661937173c75d9d5dc7a6486fc7707cbed342f389082c312af6a728d1cd`

```dockerfile
```

-	Layers:
	-	`sha256:59133632b395d7351d3c0bb3aedc980dd89dd2610c19efa7fc25da239d673609`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1970e71b094e5b797deb75611d0a98cd09880f898ae91b4f82ba89fd57520d3d`  
		Last Modified: Fri, 14 Feb 2025 21:48:03 GMT  
		Size: 14.2 KB (14153 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:fa647fc1e5d5df7d8d923fb6332aab8e78783f8fca1a1394efb4011f68f5a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9465812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33eeff39e0aaabe61ca826fd7502396183462451be0783133e1a8fa944fc7350`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
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
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 12:05:04 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaad1488a8714e2cc69c2d60095bc20bf1b00df2cbd398f4dc6a36e1abf207`  
		Last Modified: Fri, 14 Feb 2025 22:23:25 GMT  
		Size: 297.8 KB (297838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6b3f59ebc2e050b970e37757f7a57120b76c52798fcf5aaf1dc6eb8d8e8b47`  
		Last Modified: Fri, 14 Feb 2025 22:23:25 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd39ca3613a666408241996cb540196c3a89d30375c8f12b33b9cd4fd7530e6f`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb6d98388d2ab9e73e34a33bc0795566eefbdc2be62c3d8e63f8d44d21d6ec`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:1aa1079885b640a7fb6c01d680c6b50b7cbc9d0ef4905bf34d5099d8fa74dc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdc6b7dae415da31a28825768e58ec52e16959bf5db56ce9b32a5feeef03767`

```dockerfile
```

-	Layers:
	-	`sha256:c4472e68032e1ca292888794e317e1ea0b892cc834999c96b4acf159c1355b94`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a5ce400b19e271e46772e9b6dbabc4a372acb92f7693cc032c465c94ee0a8d`  
		Last Modified: Fri, 14 Feb 2025 22:23:24 GMT  
		Size: 14.2 KB (14183 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:10606c79c136c19a8d0e69acb08932b0de4bfdad8fa5e0fb193033f89afb718e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9348229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dd9882a38a66fc185011f804fac82027e193389da7256cd460141db48b27cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-ppc64le.tar.gz / # buildkit
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
	-	`sha256:3328e3c235e7d1731238778d35cdabc664a01e783c0ffd0faa9e6a0c759c4646`  
		Last Modified: Fri, 14 Feb 2025 12:05:06 GMT  
		Size: 3.4 MB (3360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e98f03b75131dd03d21db367eeddeb8b5a826b435500169b442f32692ddcf`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 298.3 KB (298257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc4c076544893d11b7abac2b20c9d950530832a23c7a68aa255c064b826dc84`  
		Last Modified: Fri, 14 Feb 2025 21:51:26 GMT  
		Size: 5.7 MB (5689220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608a80ad7912ecc5679a590cd4bb79e5b7d8272beba8224424a6dd6b86d4477`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b996b58d4a65e936f55f8197b580b23338ef297fbd6b4f9a95776c4895a526b3`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:8f4deb927eecce4f8f7b6a93a7c8a3d9bdf419b4be5cd17caa0ffbd9ff8cc715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 KB (192256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f82b70af3810d530b51e44e29b5ac9bd824be602c7460457722237b7c1c0a55`

```dockerfile
```

-	Layers:
	-	`sha256:81a881e7c0c9c46a4c2fa2c8426890c7e138d079df030b8d58573002c07e25e4`  
		Last Modified: Fri, 14 Feb 2025 21:51:26 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9fd8d94c257b5cfdd6dcb57c64d7a4431696c2074d2d0896ae36f18304c4d3`  
		Last Modified: Fri, 14 Feb 2025 21:51:25 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:d57627e6eaff3c9acbb1af5a889f9c04ebab46d4018b269e106b64f086aa6103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9689682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b1b5a3a1cec14d181b92df3357798ad62c589cc85ec2ef5d4d2c8dd7c66344`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.12-s390x.tar.gz / # buildkit
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
	-	`sha256:9d66a7fc8569c55ed7be55ca8d841e62d7dc7948a5b9d3ac10d7d462a706d48c`  
		Last Modified: Fri, 14 Feb 2025 12:05:07 GMT  
		Size: 3.2 MB (3232868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf189123ab9158cbdcedbc64afd064aab52289eb5972d4ee2757240c8328e6de`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 296.2 KB (296182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88474e8748586491bd11b4a964ec89d87acd05c3d1282b9b2714d8f66e0e586d`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a58d287f795ee0d5827b60357d1236ee5404f62efce6df39031dc0cc48138f6`  
		Last Modified: Fri, 14 Feb 2025 22:25:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eecc2312f415f0b8a833722640916a65420b40808aa0c7db2fe0877b1b65216`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:5733c871d98809734f3473fdf8543af2296a21460091120831358b706e0c2a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 KB (192176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccedbb86e1fab22893d32d3f992003b21f6772e6795e01ab7611a6bbf81103a6`

```dockerfile
```

-	Layers:
	-	`sha256:8617fa9130c4db3c616aac7abbbfc44207d7387a43973ba965cc538aee9f617b`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ee0fc123440180ad56dbb3639d50d42c8e882e7dcc1c662f421b4f7beaeda9`  
		Last Modified: Fri, 14 Feb 2025 22:25:27 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json
