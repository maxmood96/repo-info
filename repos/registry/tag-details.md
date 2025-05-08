<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3`](#registry3)
-	[`registry:3.0`](#registry30)
-	[`registry:3.0.0`](#registry300)
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
		Last Modified: Fri, 14 Feb 2025 14:36:09 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbdd6c6894b7d41bab22098e3a0fff77de4a231f5b407224ead5b3f26cc4ff3`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
		Size: 295.7 KB (295684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e82f80af0de06ae95429a79d00ae7e98c0f5ded5555a06c024757d81371a742`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3493bf46cdec3b8ecbb96c0b1cd7fc5f90964306b7c55a0136dac0beeaa627f9`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d464ea18732475d5c3591f1eba3ee96a974808791a5fe103ea1c33199f2eb74`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:27 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a76c78501fbd32c96667efc8c07506d8a4b52d8ee80f1dd12c5184e92e7fdd`  
		Last Modified: Fri, 14 Feb 2025 22:38:27 GMT  
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
		Last Modified: Fri, 14 Feb 2025 19:25:11 GMT  
		Size: 3.2 MB (3160833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe8ee13420aca9cff4c4da8e0e5adde46e151e86f892da88833cfd617311a0`  
		Last Modified: Fri, 14 Feb 2025 22:38:40 GMT  
		Size: 296.2 KB (296177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a586eed463f7a84ba7e62c4e44890f66f66ec4177a3661b6ca216fb16a1197`  
		Last Modified: Fri, 14 Feb 2025 22:38:40 GMT  
		Size: 6.0 MB (6024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0401e68d47e3642ffa60c7b93765856dde64d801eeddec9d94c610200a9d50a5`  
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0878a23b07d0ff89c4aa4c2ccaf3c7bcf9c7f19b4a528eb0c1c5958a6b8bb780`  
		Last Modified: Fri, 14 Feb 2025 22:38:40 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:28 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:12 GMT  
		Size: 2.9 MB (2913220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb5ecea2df3f1350367f83ef9f25f66fca530c1d8418d0b67723052ab3c947`  
		Last Modified: Fri, 14 Feb 2025 23:00:52 GMT  
		Size: 295.2 KB (295166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b5de8c73453f44399c3c9ec4d1aa5cd5ddd4077e7b9a8a04c005470d5b28f`  
		Last Modified: Fri, 14 Feb 2025 23:00:54 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffef9a37654e4e40d3263a377e0cd650f8f574f025cb1da5e8aa2fd15a56cf1`  
		Last Modified: Fri, 14 Feb 2025 23:00:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc8021da8780644e7f2b30e8bb843962ea89c709644713b6d28055cbc2d854`  
		Last Modified: Fri, 14 Feb 2025 23:00:57 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1970e71b094e5b797deb75611d0a98cd09880f898ae91b4f82ba89fd57520d3d`  
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:47 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaad1488a8714e2cc69c2d60095bc20bf1b00df2cbd398f4dc6a36e1abf207`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
		Size: 297.8 KB (297838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6b3f59ebc2e050b970e37757f7a57120b76c52798fcf5aaf1dc6eb8d8e8b47`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd39ca3613a666408241996cb540196c3a89d30375c8f12b33b9cd4fd7530e6f`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb6d98388d2ab9e73e34a33bc0795566eefbdc2be62c3d8e63f8d44d21d6ec`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:41 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a5ce400b19e271e46772e9b6dbabc4a372acb92f7693cc032c465c94ee0a8d`  
		Last Modified: Fri, 14 Feb 2025 22:38:41 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:49 GMT  
		Size: 3.4 MB (3360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e98f03b75131dd03d21db367eeddeb8b5a826b435500169b442f32692ddcf`  
		Last Modified: Fri, 14 Feb 2025 23:01:27 GMT  
		Size: 298.3 KB (298257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc4c076544893d11b7abac2b20c9d950530832a23c7a68aa255c064b826dc84`  
		Last Modified: Fri, 14 Feb 2025 23:01:29 GMT  
		Size: 5.7 MB (5689220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608a80ad7912ecc5679a590cd4bb79e5b7d8272beba8224424a6dd6b86d4477`  
		Last Modified: Fri, 14 Feb 2025 23:01:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b996b58d4a65e936f55f8197b580b23338ef297fbd6b4f9a95776c4895a526b3`  
		Last Modified: Fri, 14 Feb 2025 23:01:32 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:32 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9fd8d94c257b5cfdd6dcb57c64d7a4431696c2074d2d0896ae36f18304c4d3`  
		Last Modified: Fri, 14 Feb 2025 22:38:32 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:37:23 GMT  
		Size: 3.2 MB (3232868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf189123ab9158cbdcedbc64afd064aab52289eb5972d4ee2757240c8328e6de`  
		Last Modified: Fri, 14 Feb 2025 23:01:43 GMT  
		Size: 296.2 KB (296182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88474e8748586491bd11b4a964ec89d87acd05c3d1282b9b2714d8f66e0e586d`  
		Last Modified: Fri, 14 Feb 2025 23:01:45 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a58d287f795ee0d5827b60357d1236ee5404f62efce6df39031dc0cc48138f6`  
		Last Modified: Fri, 14 Feb 2025 23:01:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eecc2312f415f0b8a833722640916a65420b40808aa0c7db2fe0877b1b65216`  
		Last Modified: Fri, 14 Feb 2025 23:01:49 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:33 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ee0fc123440180ad56dbb3639d50d42c8e882e7dcc1c662f421b4f7beaeda9`  
		Last Modified: Fri, 14 Feb 2025 22:38:33 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:09 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbdd6c6894b7d41bab22098e3a0fff77de4a231f5b407224ead5b3f26cc4ff3`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
		Size: 295.7 KB (295684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e82f80af0de06ae95429a79d00ae7e98c0f5ded5555a06c024757d81371a742`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3493bf46cdec3b8ecbb96c0b1cd7fc5f90964306b7c55a0136dac0beeaa627f9`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d464ea18732475d5c3591f1eba3ee96a974808791a5fe103ea1c33199f2eb74`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:27 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a76c78501fbd32c96667efc8c07506d8a4b52d8ee80f1dd12c5184e92e7fdd`  
		Last Modified: Fri, 14 Feb 2025 22:38:27 GMT  
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
		Last Modified: Fri, 14 Feb 2025 19:25:11 GMT  
		Size: 3.2 MB (3160833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe8ee13420aca9cff4c4da8e0e5adde46e151e86f892da88833cfd617311a0`  
		Last Modified: Fri, 14 Feb 2025 22:38:40 GMT  
		Size: 296.2 KB (296177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a586eed463f7a84ba7e62c4e44890f66f66ec4177a3661b6ca216fb16a1197`  
		Last Modified: Fri, 14 Feb 2025 22:38:40 GMT  
		Size: 6.0 MB (6024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0401e68d47e3642ffa60c7b93765856dde64d801eeddec9d94c610200a9d50a5`  
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0878a23b07d0ff89c4aa4c2ccaf3c7bcf9c7f19b4a528eb0c1c5958a6b8bb780`  
		Last Modified: Fri, 14 Feb 2025 22:38:40 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:28 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:12 GMT  
		Size: 2.9 MB (2913220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb5ecea2df3f1350367f83ef9f25f66fca530c1d8418d0b67723052ab3c947`  
		Last Modified: Fri, 14 Feb 2025 23:00:52 GMT  
		Size: 295.2 KB (295166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b5de8c73453f44399c3c9ec4d1aa5cd5ddd4077e7b9a8a04c005470d5b28f`  
		Last Modified: Fri, 14 Feb 2025 23:00:54 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffef9a37654e4e40d3263a377e0cd650f8f574f025cb1da5e8aa2fd15a56cf1`  
		Last Modified: Fri, 14 Feb 2025 23:00:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc8021da8780644e7f2b30e8bb843962ea89c709644713b6d28055cbc2d854`  
		Last Modified: Fri, 14 Feb 2025 23:00:57 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1970e71b094e5b797deb75611d0a98cd09880f898ae91b4f82ba89fd57520d3d`  
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:47 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaad1488a8714e2cc69c2d60095bc20bf1b00df2cbd398f4dc6a36e1abf207`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
		Size: 297.8 KB (297838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6b3f59ebc2e050b970e37757f7a57120b76c52798fcf5aaf1dc6eb8d8e8b47`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd39ca3613a666408241996cb540196c3a89d30375c8f12b33b9cd4fd7530e6f`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb6d98388d2ab9e73e34a33bc0795566eefbdc2be62c3d8e63f8d44d21d6ec`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:41 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a5ce400b19e271e46772e9b6dbabc4a372acb92f7693cc032c465c94ee0a8d`  
		Last Modified: Fri, 14 Feb 2025 22:38:41 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:49 GMT  
		Size: 3.4 MB (3360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e98f03b75131dd03d21db367eeddeb8b5a826b435500169b442f32692ddcf`  
		Last Modified: Fri, 14 Feb 2025 23:01:27 GMT  
		Size: 298.3 KB (298257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc4c076544893d11b7abac2b20c9d950530832a23c7a68aa255c064b826dc84`  
		Last Modified: Fri, 14 Feb 2025 23:01:29 GMT  
		Size: 5.7 MB (5689220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608a80ad7912ecc5679a590cd4bb79e5b7d8272beba8224424a6dd6b86d4477`  
		Last Modified: Fri, 14 Feb 2025 23:01:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b996b58d4a65e936f55f8197b580b23338ef297fbd6b4f9a95776c4895a526b3`  
		Last Modified: Fri, 14 Feb 2025 23:01:32 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:32 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9fd8d94c257b5cfdd6dcb57c64d7a4431696c2074d2d0896ae36f18304c4d3`  
		Last Modified: Fri, 14 Feb 2025 22:38:32 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:37:23 GMT  
		Size: 3.2 MB (3232868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf189123ab9158cbdcedbc64afd064aab52289eb5972d4ee2757240c8328e6de`  
		Last Modified: Fri, 14 Feb 2025 23:01:43 GMT  
		Size: 296.2 KB (296182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88474e8748586491bd11b4a964ec89d87acd05c3d1282b9b2714d8f66e0e586d`  
		Last Modified: Fri, 14 Feb 2025 23:01:45 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a58d287f795ee0d5827b60357d1236ee5404f62efce6df39031dc0cc48138f6`  
		Last Modified: Fri, 14 Feb 2025 23:01:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eecc2312f415f0b8a833722640916a65420b40808aa0c7db2fe0877b1b65216`  
		Last Modified: Fri, 14 Feb 2025 23:01:49 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:33 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ee0fc123440180ad56dbb3639d50d42c8e882e7dcc1c662f421b4f7beaeda9`  
		Last Modified: Fri, 14 Feb 2025 22:38:33 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:09 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbdd6c6894b7d41bab22098e3a0fff77de4a231f5b407224ead5b3f26cc4ff3`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
		Size: 295.7 KB (295684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e82f80af0de06ae95429a79d00ae7e98c0f5ded5555a06c024757d81371a742`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3493bf46cdec3b8ecbb96c0b1cd7fc5f90964306b7c55a0136dac0beeaa627f9`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d464ea18732475d5c3591f1eba3ee96a974808791a5fe103ea1c33199f2eb74`  
		Last Modified: Fri, 14 Feb 2025 22:38:23 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:27 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a76c78501fbd32c96667efc8c07506d8a4b52d8ee80f1dd12c5184e92e7fdd`  
		Last Modified: Fri, 14 Feb 2025 22:38:27 GMT  
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
		Last Modified: Fri, 14 Feb 2025 19:25:11 GMT  
		Size: 3.2 MB (3160833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe8ee13420aca9cff4c4da8e0e5adde46e151e86f892da88833cfd617311a0`  
		Last Modified: Fri, 14 Feb 2025 22:38:40 GMT  
		Size: 296.2 KB (296177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a586eed463f7a84ba7e62c4e44890f66f66ec4177a3661b6ca216fb16a1197`  
		Last Modified: Fri, 14 Feb 2025 22:38:40 GMT  
		Size: 6.0 MB (6024110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0401e68d47e3642ffa60c7b93765856dde64d801eeddec9d94c610200a9d50a5`  
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0878a23b07d0ff89c4aa4c2ccaf3c7bcf9c7f19b4a528eb0c1c5958a6b8bb780`  
		Last Modified: Fri, 14 Feb 2025 22:38:40 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:28 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:12 GMT  
		Size: 2.9 MB (2913220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb5ecea2df3f1350367f83ef9f25f66fca530c1d8418d0b67723052ab3c947`  
		Last Modified: Fri, 14 Feb 2025 23:00:52 GMT  
		Size: 295.2 KB (295166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b5de8c73453f44399c3c9ec4d1aa5cd5ddd4077e7b9a8a04c005470d5b28f`  
		Last Modified: Fri, 14 Feb 2025 23:00:54 GMT  
		Size: 6.0 MB (6017215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffef9a37654e4e40d3263a377e0cd650f8f574f025cb1da5e8aa2fd15a56cf1`  
		Last Modified: Fri, 14 Feb 2025 23:00:55 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc8021da8780644e7f2b30e8bb843962ea89c709644713b6d28055cbc2d854`  
		Last Modified: Fri, 14 Feb 2025 23:00:57 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1970e71b094e5b797deb75611d0a98cd09880f898ae91b4f82ba89fd57520d3d`  
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:47 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaad1488a8714e2cc69c2d60095bc20bf1b00df2cbd398f4dc6a36e1abf207`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
		Size: 297.8 KB (297838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6b3f59ebc2e050b970e37757f7a57120b76c52798fcf5aaf1dc6eb8d8e8b47`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd39ca3613a666408241996cb540196c3a89d30375c8f12b33b9cd4fd7530e6f`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb6d98388d2ab9e73e34a33bc0795566eefbdc2be62c3d8e63f8d44d21d6ec`  
		Last Modified: Fri, 14 Feb 2025 22:38:45 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:41 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a5ce400b19e271e46772e9b6dbabc4a372acb92f7693cc032c465c94ee0a8d`  
		Last Modified: Fri, 14 Feb 2025 22:38:41 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:49 GMT  
		Size: 3.4 MB (3360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2e98f03b75131dd03d21db367eeddeb8b5a826b435500169b442f32692ddcf`  
		Last Modified: Fri, 14 Feb 2025 23:01:27 GMT  
		Size: 298.3 KB (298257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc4c076544893d11b7abac2b20c9d950530832a23c7a68aa255c064b826dc84`  
		Last Modified: Fri, 14 Feb 2025 23:01:29 GMT  
		Size: 5.7 MB (5689220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608a80ad7912ecc5679a590cd4bb79e5b7d8272beba8224424a6dd6b86d4477`  
		Last Modified: Fri, 14 Feb 2025 23:01:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b996b58d4a65e936f55f8197b580b23338ef297fbd6b4f9a95776c4895a526b3`  
		Last Modified: Fri, 14 Feb 2025 23:01:32 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:32 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9fd8d94c257b5cfdd6dcb57c64d7a4431696c2074d2d0896ae36f18304c4d3`  
		Last Modified: Fri, 14 Feb 2025 22:38:32 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:37:23 GMT  
		Size: 3.2 MB (3232868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf189123ab9158cbdcedbc64afd064aab52289eb5972d4ee2757240c8328e6de`  
		Last Modified: Fri, 14 Feb 2025 23:01:43 GMT  
		Size: 296.2 KB (296182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88474e8748586491bd11b4a964ec89d87acd05c3d1282b9b2714d8f66e0e586d`  
		Last Modified: Fri, 14 Feb 2025 23:01:45 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a58d287f795ee0d5827b60357d1236ee5404f62efce6df39031dc0cc48138f6`  
		Last Modified: Fri, 14 Feb 2025 23:01:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eecc2312f415f0b8a833722640916a65420b40808aa0c7db2fe0877b1b65216`  
		Last Modified: Fri, 14 Feb 2025 23:01:49 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:33 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ee0fc123440180ad56dbb3639d50d42c8e882e7dcc1c662f421b4f7beaeda9`  
		Last Modified: Fri, 14 Feb 2025 22:38:33 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3`

```console
$ docker pull registry@sha256:1fc7de654f2ac1247f0b67e8a459e273b0993be7d2beda1f3f56fbf1001ed3e7
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

### `registry:3` - linux; amd64

```console
$ docker pull registry@sha256:61349442e9c3dc07fd06ffa6a4b622bc28960952b6b3adafcb58fa268ce92e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18551765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dec7d02aaeabc6faad1421be2570b4666be359853098ac7836ad0aa51b52d79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a9c19e7b9ded1170de9efd509fa08adaa16821aa7c17412b56416ffe0380f7`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 294.9 KB (294904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a894506e86bf28b556f2981f5bdbfee8e689c04f636f7586de1a1cf619023b`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 14.6 MB (14614003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1822bac1992d5c8ec6516886a75b7e6d3018ef07516b9e71fc2a6e1e53e709a`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5da7f963a9e69f979708ee8dd91417cd95926b746899f8f1962fd6fea44cb11`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:dbcfbb79febfd509882f7cb7c1c3459c39143692df9ebaacd9dc1d546af14464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f907df5af7bd030de05076c73dacf7cc8ef7550cc057530e6c685488c79aee21`

```dockerfile
```

-	Layers:
	-	`sha256:3aa6739dc80e343a49b1486b43f13b6f0d87dbaff910f3146efb1e70cebb43ef`  
		Last Modified: Thu, 08 May 2025 21:39:18 GMT  
		Size: 267.1 KB (267139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1bb4a6b1402fcc1731aa19dbce0a67b789c08e34b5928ff6138e71eae24662`  
		Last Modified: Thu, 08 May 2025 21:39:19 GMT  
		Size: 14.3 KB (14328 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; arm variant v6

```console
$ docker pull registry@sha256:b7f17db708eaa74f8d4d2b5ff58b8efbaccf94e972eb89a17b32aa6273d5d4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17385793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf959a051c4c1119dbdf5543f621aee0fb2ee15be53418462fc18b5b9e053d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581980cd7e455350d6aa347fdb0557ab19139b554f2eb4e902198755e72cf87`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 13.7 MB (13724200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f9db3d049e2b31b7b23120ce7e625a26a1ddbf1d50ba110c76f111df11083`  
		Last Modified: Thu, 08 May 2025 21:39:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71fe1d1ac1e449f7966e320190b416119d51de3aea11850bf490bfcae1593d8`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:cf5455cdc81bb49a947023f661d9b1ace7b0aa794f5b9f5aa0d346018fbea1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10aa550c2238c3ee39466e398ef637097ac8bbc60027a2d33d606baf024914e1`

```dockerfile
```

-	Layers:
	-	`sha256:0afd66928587230a35739d829e3e2503287e8141d6b6803b2e6bbf06fd0f05b1`  
		Last Modified: Thu, 08 May 2025 21:39:19 GMT  
		Size: 14.2 KB (14202 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; arm variant v7

```console
$ docker pull registry@sha256:4a685c7c549ca4cb45dd7f7fcd025adc3e708da1643e9bb5636ac61baadb9940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17099795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c03fce14d3a24b732a7f461fe6aa444030c8ea1b0d17f5d917731cb1cea1e08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 23:49:34 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143512d4fb1efe79e1c3e84f2b8990d7b156fc8e76e4d4cf27437d2f7249dc31`  
		Last Modified: Thu, 08 May 2025 21:34:11 GMT  
		Size: 13.7 MB (13705862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889ae642b115a5dea458049a6805d2e61e2951183f78ba7b769bbfe585132f9f`  
		Last Modified: Thu, 08 May 2025 21:34:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86712d9a840166a79062b237035504d7b3bed52d21cc41857bf456669d01766c`  
		Last Modified: Thu, 08 May 2025 21:34:12 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:f9a8d6912acef39a6b62f2466f96378fe53b46a6e907bd15f186dd7914daeddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef9d70079ca7408876f0355821a42e10b5549638e5d45bb3f1f0b538539e0a`

```dockerfile
```

-	Layers:
	-	`sha256:461152498186e16c914af6d05fda0150666d41ba53b152b895bf2c0f3dcc29bd`  
		Last Modified: Thu, 08 May 2025 21:39:20 GMT  
		Size: 266.4 KB (266411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbdaff0bf0e2267d5b6e47ce366e1d995e3ad6e6787e8be7798e25e11e93930`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 14.4 KB (14417 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:b8bf4b1d638d8733dd20e469c1e8c902f1f1bdfe5a9f6da70e164aa08bdf688a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17781033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3e98ee98fbbbb01a549a53426ef1ce639fad4dd2a92b05f05e6ec36ef0d516`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e33b27c9b76515e1154a131a67e2f0fe88ba9e9bc48a1a704c790a0561e068`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 297.9 KB (297871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d4f3945f82cb36f20759bd5e4d3ea8be7671f4f58be8fde14e12cccd9bfb0a`  
		Last Modified: Thu, 08 May 2025 17:07:22 GMT  
		Size: 13.5 MB (13489522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b82d7f2276a68e0a1064324f6d64909ee13fb144e62ff3c9582d2c7d4c19703`  
		Last Modified: Thu, 08 May 2025 17:07:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1666b4f592cf9c56455ed01e495240c7e03c00b239ef9a9a70b1a73f044205b7`  
		Last Modified: Thu, 08 May 2025 17:07:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:ad5a92ffa0aa4378228838161e4438ebdb40bfdd9410e51d1c50b5a89ee2fa72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 KB (281642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2ad8109cf484125829376ef68cde0a71374dcb59674f25a212b3ae45010f26`

```dockerfile
```

-	Layers:
	-	`sha256:6d02589dee8d283cfa66dd7808cd63cb5852fc971fda911f5206e17b7982934d`  
		Last Modified: Thu, 08 May 2025 21:39:22 GMT  
		Size: 267.2 KB (267195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e360e62c15eaf48115988eae5efdc603b2d8502da0965b24a4338cff515cbe93`  
		Last Modified: Thu, 08 May 2025 21:39:22 GMT  
		Size: 14.4 KB (14447 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; ppc64le

```console
$ docker pull registry@sha256:f173625ac28e24fbb1e4755873200d0df442002462afd86aeb3ca14003c74ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17041713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e599ea2922d2f2e1208c49f4a86aee794ad45b536ead49704c687e78662e8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27442ea8b4dc6fdf584c0b30a8e1943de4b659fd7ec220499d43ff5c7d4c1c8`  
		Last Modified: Thu, 08 May 2025 21:39:24 GMT  
		Size: 298.3 KB (298274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba782946e954b7993574b6d4fbd42bf789f17f9931a7d35396dccd56534ad30`  
		Last Modified: Thu, 08 May 2025 21:39:25 GMT  
		Size: 13.2 MB (13168484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e0cee1df6197dc8422353c954238a97db6bf6927326f8c7721cd770b43f609`  
		Last Modified: Thu, 08 May 2025 21:39:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5816d31b3612108b1ee52d324d9d54b8af0c1a8b145833ee2c96724afcb15172`  
		Last Modified: Thu, 08 May 2025 21:39:26 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:e7dff0d1725359a80c55558e1f7fdb8d7295b3fd65aef8a255ee8a647769fae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 KB (279596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25408cc7b38e5d22c9e74865c260b65a31fb5179d40f87029c05c2a1fc4417`

```dockerfile
```

-	Layers:
	-	`sha256:be79c05e6917674620c5ec307d8b1c57d952af01f3afbcef1e71028a9ba0205a`  
		Last Modified: Thu, 08 May 2025 21:39:23 GMT  
		Size: 265.2 KB (265222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f1c5c1874fbc1846d75b0df96b5e91dbab8ca2b2641c0291949c738b0dfd67`  
		Last Modified: Thu, 08 May 2025 21:39:24 GMT  
		Size: 14.4 KB (14374 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; riscv64

```console
$ docker pull registry@sha256:ccbed7fa29b70c17b41ade04dc137cf5201c6a67ded10c841a5060d8d91448ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17537511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ef966d24343fb41053dc6ad886204a91b958e313bdb1f4898eff3a32526f2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 09:31:14 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b7353e85f9f8ac0206684e4063270c05a00cd4d76172b167229744dc0ee090`  
		Last Modified: Thu, 08 May 2025 21:39:28 GMT  
		Size: 13.9 MB (13890117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324c7a7e2f398fc67985e8c0aa5aaedb16225779163b1e8540fe671a3bd4c66b`  
		Last Modified: Thu, 08 May 2025 21:39:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7cdfca9ab92a172e8e2d1ca853c9c5a69253cd4b4e29fd3b3ee10d5895c06d`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:dae75c7beac87098ef5289ed9d35b0427d269a4f38134f490c702941ec84b13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 KB (279592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162a4b96ddc6bfc8f86900ade67d99d782fc011d0dc357bf588b1a4465fe80fa`

```dockerfile
```

-	Layers:
	-	`sha256:4a8e462adc723873ce8ddf50a091b488c965663c0b97ade9bb594503f8c00459`  
		Last Modified: Thu, 08 May 2025 21:39:25 GMT  
		Size: 265.2 KB (265218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e28318ae55df529a5b2906c34a7c2e649a8f55e65af7bf6bdd97d4b47ee5c50`  
		Last Modified: Thu, 08 May 2025 21:39:27 GMT  
		Size: 14.4 KB (14374 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3` - linux; s390x

```console
$ docker pull registry@sha256:568befd308146d037135dee23a54555ddb0a2c0b9b8a77293403c36f92eeed01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17828305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b830b76ea9a73f4c882f771f3178c616506f53ca878ba4629eda7b310c00e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be80be2c55902add1c4b1f14066b1b4da724beaa2e355b53f8dd45b4887d9b9c`  
		Last Modified: Thu, 08 May 2025 20:29:45 GMT  
		Size: 296.2 KB (296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce32c938e0bce4c1726d2b421fa2169e9ad8d8cc7b03405bea7944f1ac40841d`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 14.1 MB (14063944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5ff26fb639a02f240d8adcb2df380a6a4e24dca5a803e98fa6b0210f6abc26`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51ea05070e17a1fe11d8fa1816b31d606454415d3c62e11363907f06173acb9`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3` - unknown; unknown

```console
$ docker pull registry@sha256:36d8e34b868e11078e746246f36717293796e7edc1fa6e52c561e29a66f32519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43dd18649be2b0176cfa2eb8ee48bea449c7c3f8b19e9ceadf6d42028221544f`

```dockerfile
```

-	Layers:
	-	`sha256:a0a29cd12b383eb04f8963993182974b7d8355c5e417efecf04711205e343623`  
		Last Modified: Thu, 08 May 2025 21:39:27 GMT  
		Size: 265.2 KB (265188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fe0b53d54f933f15c946fa5c09345bb45e37338f93d62f723ee7840c95d5c2`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 14.3 KB (14328 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0`

```console
$ docker pull registry@sha256:1fc7de654f2ac1247f0b67e8a459e273b0993be7d2beda1f3f56fbf1001ed3e7
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

### `registry:3.0` - linux; amd64

```console
$ docker pull registry@sha256:61349442e9c3dc07fd06ffa6a4b622bc28960952b6b3adafcb58fa268ce92e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18551765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dec7d02aaeabc6faad1421be2570b4666be359853098ac7836ad0aa51b52d79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a9c19e7b9ded1170de9efd509fa08adaa16821aa7c17412b56416ffe0380f7`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 294.9 KB (294904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a894506e86bf28b556f2981f5bdbfee8e689c04f636f7586de1a1cf619023b`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 14.6 MB (14614003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1822bac1992d5c8ec6516886a75b7e6d3018ef07516b9e71fc2a6e1e53e709a`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5da7f963a9e69f979708ee8dd91417cd95926b746899f8f1962fd6fea44cb11`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:dbcfbb79febfd509882f7cb7c1c3459c39143692df9ebaacd9dc1d546af14464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f907df5af7bd030de05076c73dacf7cc8ef7550cc057530e6c685488c79aee21`

```dockerfile
```

-	Layers:
	-	`sha256:3aa6739dc80e343a49b1486b43f13b6f0d87dbaff910f3146efb1e70cebb43ef`  
		Last Modified: Thu, 08 May 2025 21:39:18 GMT  
		Size: 267.1 KB (267139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1bb4a6b1402fcc1731aa19dbce0a67b789c08e34b5928ff6138e71eae24662`  
		Last Modified: Thu, 08 May 2025 21:39:19 GMT  
		Size: 14.3 KB (14328 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; arm variant v6

```console
$ docker pull registry@sha256:b7f17db708eaa74f8d4d2b5ff58b8efbaccf94e972eb89a17b32aa6273d5d4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17385793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf959a051c4c1119dbdf5543f621aee0fb2ee15be53418462fc18b5b9e053d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581980cd7e455350d6aa347fdb0557ab19139b554f2eb4e902198755e72cf87`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 13.7 MB (13724200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f9db3d049e2b31b7b23120ce7e625a26a1ddbf1d50ba110c76f111df11083`  
		Last Modified: Thu, 08 May 2025 21:39:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71fe1d1ac1e449f7966e320190b416119d51de3aea11850bf490bfcae1593d8`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:cf5455cdc81bb49a947023f661d9b1ace7b0aa794f5b9f5aa0d346018fbea1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10aa550c2238c3ee39466e398ef637097ac8bbc60027a2d33d606baf024914e1`

```dockerfile
```

-	Layers:
	-	`sha256:0afd66928587230a35739d829e3e2503287e8141d6b6803b2e6bbf06fd0f05b1`  
		Last Modified: Thu, 08 May 2025 21:39:19 GMT  
		Size: 14.2 KB (14202 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; arm variant v7

```console
$ docker pull registry@sha256:4a685c7c549ca4cb45dd7f7fcd025adc3e708da1643e9bb5636ac61baadb9940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17099795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c03fce14d3a24b732a7f461fe6aa444030c8ea1b0d17f5d917731cb1cea1e08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 23:49:34 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143512d4fb1efe79e1c3e84f2b8990d7b156fc8e76e4d4cf27437d2f7249dc31`  
		Last Modified: Thu, 08 May 2025 21:34:11 GMT  
		Size: 13.7 MB (13705862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889ae642b115a5dea458049a6805d2e61e2951183f78ba7b769bbfe585132f9f`  
		Last Modified: Thu, 08 May 2025 21:34:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86712d9a840166a79062b237035504d7b3bed52d21cc41857bf456669d01766c`  
		Last Modified: Thu, 08 May 2025 21:34:12 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:f9a8d6912acef39a6b62f2466f96378fe53b46a6e907bd15f186dd7914daeddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef9d70079ca7408876f0355821a42e10b5549638e5d45bb3f1f0b538539e0a`

```dockerfile
```

-	Layers:
	-	`sha256:461152498186e16c914af6d05fda0150666d41ba53b152b895bf2c0f3dcc29bd`  
		Last Modified: Thu, 08 May 2025 21:39:20 GMT  
		Size: 266.4 KB (266411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbdaff0bf0e2267d5b6e47ce366e1d995e3ad6e6787e8be7798e25e11e93930`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 14.4 KB (14417 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:b8bf4b1d638d8733dd20e469c1e8c902f1f1bdfe5a9f6da70e164aa08bdf688a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17781033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3e98ee98fbbbb01a549a53426ef1ce639fad4dd2a92b05f05e6ec36ef0d516`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e33b27c9b76515e1154a131a67e2f0fe88ba9e9bc48a1a704c790a0561e068`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 297.9 KB (297871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d4f3945f82cb36f20759bd5e4d3ea8be7671f4f58be8fde14e12cccd9bfb0a`  
		Last Modified: Thu, 08 May 2025 17:07:22 GMT  
		Size: 13.5 MB (13489522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b82d7f2276a68e0a1064324f6d64909ee13fb144e62ff3c9582d2c7d4c19703`  
		Last Modified: Thu, 08 May 2025 17:07:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1666b4f592cf9c56455ed01e495240c7e03c00b239ef9a9a70b1a73f044205b7`  
		Last Modified: Thu, 08 May 2025 17:07:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:ad5a92ffa0aa4378228838161e4438ebdb40bfdd9410e51d1c50b5a89ee2fa72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 KB (281642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2ad8109cf484125829376ef68cde0a71374dcb59674f25a212b3ae45010f26`

```dockerfile
```

-	Layers:
	-	`sha256:6d02589dee8d283cfa66dd7808cd63cb5852fc971fda911f5206e17b7982934d`  
		Last Modified: Thu, 08 May 2025 21:39:22 GMT  
		Size: 267.2 KB (267195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e360e62c15eaf48115988eae5efdc603b2d8502da0965b24a4338cff515cbe93`  
		Last Modified: Thu, 08 May 2025 21:39:22 GMT  
		Size: 14.4 KB (14447 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; ppc64le

```console
$ docker pull registry@sha256:f173625ac28e24fbb1e4755873200d0df442002462afd86aeb3ca14003c74ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17041713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e599ea2922d2f2e1208c49f4a86aee794ad45b536ead49704c687e78662e8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27442ea8b4dc6fdf584c0b30a8e1943de4b659fd7ec220499d43ff5c7d4c1c8`  
		Last Modified: Thu, 08 May 2025 21:39:24 GMT  
		Size: 298.3 KB (298274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba782946e954b7993574b6d4fbd42bf789f17f9931a7d35396dccd56534ad30`  
		Last Modified: Thu, 08 May 2025 21:39:25 GMT  
		Size: 13.2 MB (13168484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e0cee1df6197dc8422353c954238a97db6bf6927326f8c7721cd770b43f609`  
		Last Modified: Thu, 08 May 2025 21:39:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5816d31b3612108b1ee52d324d9d54b8af0c1a8b145833ee2c96724afcb15172`  
		Last Modified: Thu, 08 May 2025 21:39:26 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:e7dff0d1725359a80c55558e1f7fdb8d7295b3fd65aef8a255ee8a647769fae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 KB (279596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25408cc7b38e5d22c9e74865c260b65a31fb5179d40f87029c05c2a1fc4417`

```dockerfile
```

-	Layers:
	-	`sha256:be79c05e6917674620c5ec307d8b1c57d952af01f3afbcef1e71028a9ba0205a`  
		Last Modified: Thu, 08 May 2025 21:39:23 GMT  
		Size: 265.2 KB (265222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f1c5c1874fbc1846d75b0df96b5e91dbab8ca2b2641c0291949c738b0dfd67`  
		Last Modified: Thu, 08 May 2025 21:39:24 GMT  
		Size: 14.4 KB (14374 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; riscv64

```console
$ docker pull registry@sha256:ccbed7fa29b70c17b41ade04dc137cf5201c6a67ded10c841a5060d8d91448ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17537511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ef966d24343fb41053dc6ad886204a91b958e313bdb1f4898eff3a32526f2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 09:31:14 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b7353e85f9f8ac0206684e4063270c05a00cd4d76172b167229744dc0ee090`  
		Last Modified: Thu, 08 May 2025 21:39:28 GMT  
		Size: 13.9 MB (13890117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324c7a7e2f398fc67985e8c0aa5aaedb16225779163b1e8540fe671a3bd4c66b`  
		Last Modified: Thu, 08 May 2025 21:39:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7cdfca9ab92a172e8e2d1ca853c9c5a69253cd4b4e29fd3b3ee10d5895c06d`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:dae75c7beac87098ef5289ed9d35b0427d269a4f38134f490c702941ec84b13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 KB (279592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162a4b96ddc6bfc8f86900ade67d99d782fc011d0dc357bf588b1a4465fe80fa`

```dockerfile
```

-	Layers:
	-	`sha256:4a8e462adc723873ce8ddf50a091b488c965663c0b97ade9bb594503f8c00459`  
		Last Modified: Thu, 08 May 2025 21:39:25 GMT  
		Size: 265.2 KB (265218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e28318ae55df529a5b2906c34a7c2e649a8f55e65af7bf6bdd97d4b47ee5c50`  
		Last Modified: Thu, 08 May 2025 21:39:27 GMT  
		Size: 14.4 KB (14374 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0` - linux; s390x

```console
$ docker pull registry@sha256:568befd308146d037135dee23a54555ddb0a2c0b9b8a77293403c36f92eeed01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17828305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b830b76ea9a73f4c882f771f3178c616506f53ca878ba4629eda7b310c00e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be80be2c55902add1c4b1f14066b1b4da724beaa2e355b53f8dd45b4887d9b9c`  
		Last Modified: Thu, 08 May 2025 20:29:45 GMT  
		Size: 296.2 KB (296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce32c938e0bce4c1726d2b421fa2169e9ad8d8cc7b03405bea7944f1ac40841d`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 14.1 MB (14063944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5ff26fb639a02f240d8adcb2df380a6a4e24dca5a803e98fa6b0210f6abc26`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51ea05070e17a1fe11d8fa1816b31d606454415d3c62e11363907f06173acb9`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0` - unknown; unknown

```console
$ docker pull registry@sha256:36d8e34b868e11078e746246f36717293796e7edc1fa6e52c561e29a66f32519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43dd18649be2b0176cfa2eb8ee48bea449c7c3f8b19e9ceadf6d42028221544f`

```dockerfile
```

-	Layers:
	-	`sha256:a0a29cd12b383eb04f8963993182974b7d8355c5e417efecf04711205e343623`  
		Last Modified: Thu, 08 May 2025 21:39:27 GMT  
		Size: 265.2 KB (265188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fe0b53d54f933f15c946fa5c09345bb45e37338f93d62f723ee7840c95d5c2`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 14.3 KB (14328 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0`

```console
$ docker pull registry@sha256:1fc7de654f2ac1247f0b67e8a459e273b0993be7d2beda1f3f56fbf1001ed3e7
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

### `registry:3.0.0` - linux; amd64

```console
$ docker pull registry@sha256:61349442e9c3dc07fd06ffa6a4b622bc28960952b6b3adafcb58fa268ce92e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18551765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dec7d02aaeabc6faad1421be2570b4666be359853098ac7836ad0aa51b52d79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a9c19e7b9ded1170de9efd509fa08adaa16821aa7c17412b56416ffe0380f7`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 294.9 KB (294904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a894506e86bf28b556f2981f5bdbfee8e689c04f636f7586de1a1cf619023b`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 14.6 MB (14614003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1822bac1992d5c8ec6516886a75b7e6d3018ef07516b9e71fc2a6e1e53e709a`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5da7f963a9e69f979708ee8dd91417cd95926b746899f8f1962fd6fea44cb11`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:dbcfbb79febfd509882f7cb7c1c3459c39143692df9ebaacd9dc1d546af14464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f907df5af7bd030de05076c73dacf7cc8ef7550cc057530e6c685488c79aee21`

```dockerfile
```

-	Layers:
	-	`sha256:3aa6739dc80e343a49b1486b43f13b6f0d87dbaff910f3146efb1e70cebb43ef`  
		Last Modified: Thu, 08 May 2025 21:39:18 GMT  
		Size: 267.1 KB (267139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1bb4a6b1402fcc1731aa19dbce0a67b789c08e34b5928ff6138e71eae24662`  
		Last Modified: Thu, 08 May 2025 21:39:19 GMT  
		Size: 14.3 KB (14328 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; arm variant v6

```console
$ docker pull registry@sha256:b7f17db708eaa74f8d4d2b5ff58b8efbaccf94e972eb89a17b32aa6273d5d4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17385793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf959a051c4c1119dbdf5543f621aee0fb2ee15be53418462fc18b5b9e053d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581980cd7e455350d6aa347fdb0557ab19139b554f2eb4e902198755e72cf87`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 13.7 MB (13724200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f9db3d049e2b31b7b23120ce7e625a26a1ddbf1d50ba110c76f111df11083`  
		Last Modified: Thu, 08 May 2025 21:39:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71fe1d1ac1e449f7966e320190b416119d51de3aea11850bf490bfcae1593d8`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:cf5455cdc81bb49a947023f661d9b1ace7b0aa794f5b9f5aa0d346018fbea1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10aa550c2238c3ee39466e398ef637097ac8bbc60027a2d33d606baf024914e1`

```dockerfile
```

-	Layers:
	-	`sha256:0afd66928587230a35739d829e3e2503287e8141d6b6803b2e6bbf06fd0f05b1`  
		Last Modified: Thu, 08 May 2025 21:39:19 GMT  
		Size: 14.2 KB (14202 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; arm variant v7

```console
$ docker pull registry@sha256:4a685c7c549ca4cb45dd7f7fcd025adc3e708da1643e9bb5636ac61baadb9940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17099795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c03fce14d3a24b732a7f461fe6aa444030c8ea1b0d17f5d917731cb1cea1e08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 23:49:34 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143512d4fb1efe79e1c3e84f2b8990d7b156fc8e76e4d4cf27437d2f7249dc31`  
		Last Modified: Thu, 08 May 2025 21:34:11 GMT  
		Size: 13.7 MB (13705862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889ae642b115a5dea458049a6805d2e61e2951183f78ba7b769bbfe585132f9f`  
		Last Modified: Thu, 08 May 2025 21:34:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86712d9a840166a79062b237035504d7b3bed52d21cc41857bf456669d01766c`  
		Last Modified: Thu, 08 May 2025 21:34:12 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:f9a8d6912acef39a6b62f2466f96378fe53b46a6e907bd15f186dd7914daeddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef9d70079ca7408876f0355821a42e10b5549638e5d45bb3f1f0b538539e0a`

```dockerfile
```

-	Layers:
	-	`sha256:461152498186e16c914af6d05fda0150666d41ba53b152b895bf2c0f3dcc29bd`  
		Last Modified: Thu, 08 May 2025 21:39:20 GMT  
		Size: 266.4 KB (266411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbdaff0bf0e2267d5b6e47ce366e1d995e3ad6e6787e8be7798e25e11e93930`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 14.4 KB (14417 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:b8bf4b1d638d8733dd20e469c1e8c902f1f1bdfe5a9f6da70e164aa08bdf688a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17781033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3e98ee98fbbbb01a549a53426ef1ce639fad4dd2a92b05f05e6ec36ef0d516`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e33b27c9b76515e1154a131a67e2f0fe88ba9e9bc48a1a704c790a0561e068`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 297.9 KB (297871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d4f3945f82cb36f20759bd5e4d3ea8be7671f4f58be8fde14e12cccd9bfb0a`  
		Last Modified: Thu, 08 May 2025 17:07:22 GMT  
		Size: 13.5 MB (13489522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b82d7f2276a68e0a1064324f6d64909ee13fb144e62ff3c9582d2c7d4c19703`  
		Last Modified: Thu, 08 May 2025 17:07:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1666b4f592cf9c56455ed01e495240c7e03c00b239ef9a9a70b1a73f044205b7`  
		Last Modified: Thu, 08 May 2025 17:07:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:ad5a92ffa0aa4378228838161e4438ebdb40bfdd9410e51d1c50b5a89ee2fa72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 KB (281642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2ad8109cf484125829376ef68cde0a71374dcb59674f25a212b3ae45010f26`

```dockerfile
```

-	Layers:
	-	`sha256:6d02589dee8d283cfa66dd7808cd63cb5852fc971fda911f5206e17b7982934d`  
		Last Modified: Thu, 08 May 2025 21:39:22 GMT  
		Size: 267.2 KB (267195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e360e62c15eaf48115988eae5efdc603b2d8502da0965b24a4338cff515cbe93`  
		Last Modified: Thu, 08 May 2025 21:39:22 GMT  
		Size: 14.4 KB (14447 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; ppc64le

```console
$ docker pull registry@sha256:f173625ac28e24fbb1e4755873200d0df442002462afd86aeb3ca14003c74ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17041713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e599ea2922d2f2e1208c49f4a86aee794ad45b536ead49704c687e78662e8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27442ea8b4dc6fdf584c0b30a8e1943de4b659fd7ec220499d43ff5c7d4c1c8`  
		Last Modified: Thu, 08 May 2025 21:39:24 GMT  
		Size: 298.3 KB (298274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba782946e954b7993574b6d4fbd42bf789f17f9931a7d35396dccd56534ad30`  
		Last Modified: Thu, 08 May 2025 21:39:25 GMT  
		Size: 13.2 MB (13168484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e0cee1df6197dc8422353c954238a97db6bf6927326f8c7721cd770b43f609`  
		Last Modified: Thu, 08 May 2025 21:39:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5816d31b3612108b1ee52d324d9d54b8af0c1a8b145833ee2c96724afcb15172`  
		Last Modified: Thu, 08 May 2025 21:39:26 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:e7dff0d1725359a80c55558e1f7fdb8d7295b3fd65aef8a255ee8a647769fae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 KB (279596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25408cc7b38e5d22c9e74865c260b65a31fb5179d40f87029c05c2a1fc4417`

```dockerfile
```

-	Layers:
	-	`sha256:be79c05e6917674620c5ec307d8b1c57d952af01f3afbcef1e71028a9ba0205a`  
		Last Modified: Thu, 08 May 2025 21:39:23 GMT  
		Size: 265.2 KB (265222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f1c5c1874fbc1846d75b0df96b5e91dbab8ca2b2641c0291949c738b0dfd67`  
		Last Modified: Thu, 08 May 2025 21:39:24 GMT  
		Size: 14.4 KB (14374 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; riscv64

```console
$ docker pull registry@sha256:ccbed7fa29b70c17b41ade04dc137cf5201c6a67ded10c841a5060d8d91448ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17537511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ef966d24343fb41053dc6ad886204a91b958e313bdb1f4898eff3a32526f2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 09:31:14 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b7353e85f9f8ac0206684e4063270c05a00cd4d76172b167229744dc0ee090`  
		Last Modified: Thu, 08 May 2025 21:39:28 GMT  
		Size: 13.9 MB (13890117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324c7a7e2f398fc67985e8c0aa5aaedb16225779163b1e8540fe671a3bd4c66b`  
		Last Modified: Thu, 08 May 2025 21:39:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7cdfca9ab92a172e8e2d1ca853c9c5a69253cd4b4e29fd3b3ee10d5895c06d`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:dae75c7beac87098ef5289ed9d35b0427d269a4f38134f490c702941ec84b13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 KB (279592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162a4b96ddc6bfc8f86900ade67d99d782fc011d0dc357bf588b1a4465fe80fa`

```dockerfile
```

-	Layers:
	-	`sha256:4a8e462adc723873ce8ddf50a091b488c965663c0b97ade9bb594503f8c00459`  
		Last Modified: Thu, 08 May 2025 21:39:25 GMT  
		Size: 265.2 KB (265218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e28318ae55df529a5b2906c34a7c2e649a8f55e65af7bf6bdd97d4b47ee5c50`  
		Last Modified: Thu, 08 May 2025 21:39:27 GMT  
		Size: 14.4 KB (14374 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0` - linux; s390x

```console
$ docker pull registry@sha256:568befd308146d037135dee23a54555ddb0a2c0b9b8a77293403c36f92eeed01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17828305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b830b76ea9a73f4c882f771f3178c616506f53ca878ba4629eda7b310c00e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be80be2c55902add1c4b1f14066b1b4da724beaa2e355b53f8dd45b4887d9b9c`  
		Last Modified: Thu, 08 May 2025 20:29:45 GMT  
		Size: 296.2 KB (296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce32c938e0bce4c1726d2b421fa2169e9ad8d8cc7b03405bea7944f1ac40841d`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 14.1 MB (14063944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5ff26fb639a02f240d8adcb2df380a6a4e24dca5a803e98fa6b0210f6abc26`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51ea05070e17a1fe11d8fa1816b31d606454415d3c62e11363907f06173acb9`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0` - unknown; unknown

```console
$ docker pull registry@sha256:36d8e34b868e11078e746246f36717293796e7edc1fa6e52c561e29a66f32519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43dd18649be2b0176cfa2eb8ee48bea449c7c3f8b19e9ceadf6d42028221544f`

```dockerfile
```

-	Layers:
	-	`sha256:a0a29cd12b383eb04f8963993182974b7d8355c5e417efecf04711205e343623`  
		Last Modified: Thu, 08 May 2025 21:39:27 GMT  
		Size: 265.2 KB (265188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fe0b53d54f933f15c946fa5c09345bb45e37338f93d62f723ee7840c95d5c2`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 14.3 KB (14328 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:1fc7de654f2ac1247f0b67e8a459e273b0993be7d2beda1f3f56fbf1001ed3e7
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

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:61349442e9c3dc07fd06ffa6a4b622bc28960952b6b3adafcb58fa268ce92e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18551765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dec7d02aaeabc6faad1421be2570b4666be359853098ac7836ad0aa51b52d79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a9c19e7b9ded1170de9efd509fa08adaa16821aa7c17412b56416ffe0380f7`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 294.9 KB (294904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a894506e86bf28b556f2981f5bdbfee8e689c04f636f7586de1a1cf619023b`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 14.6 MB (14614003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1822bac1992d5c8ec6516886a75b7e6d3018ef07516b9e71fc2a6e1e53e709a`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5da7f963a9e69f979708ee8dd91417cd95926b746899f8f1962fd6fea44cb11`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:dbcfbb79febfd509882f7cb7c1c3459c39143692df9ebaacd9dc1d546af14464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 KB (281467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f907df5af7bd030de05076c73dacf7cc8ef7550cc057530e6c685488c79aee21`

```dockerfile
```

-	Layers:
	-	`sha256:3aa6739dc80e343a49b1486b43f13b6f0d87dbaff910f3146efb1e70cebb43ef`  
		Last Modified: Thu, 08 May 2025 21:39:18 GMT  
		Size: 267.1 KB (267139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1bb4a6b1402fcc1731aa19dbce0a67b789c08e34b5928ff6138e71eae24662`  
		Last Modified: Thu, 08 May 2025 21:39:19 GMT  
		Size: 14.3 KB (14328 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:b7f17db708eaa74f8d4d2b5ff58b8efbaccf94e972eb89a17b32aa6273d5d4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17385793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf959a051c4c1119dbdf5543f621aee0fb2ee15be53418462fc18b5b9e053d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581980cd7e455350d6aa347fdb0557ab19139b554f2eb4e902198755e72cf87`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 13.7 MB (13724200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f9db3d049e2b31b7b23120ce7e625a26a1ddbf1d50ba110c76f111df11083`  
		Last Modified: Thu, 08 May 2025 21:39:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71fe1d1ac1e449f7966e320190b416119d51de3aea11850bf490bfcae1593d8`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:cf5455cdc81bb49a947023f661d9b1ace7b0aa794f5b9f5aa0d346018fbea1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10aa550c2238c3ee39466e398ef637097ac8bbc60027a2d33d606baf024914e1`

```dockerfile
```

-	Layers:
	-	`sha256:0afd66928587230a35739d829e3e2503287e8141d6b6803b2e6bbf06fd0f05b1`  
		Last Modified: Thu, 08 May 2025 21:39:19 GMT  
		Size: 14.2 KB (14202 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:4a685c7c549ca4cb45dd7f7fcd025adc3e708da1643e9bb5636ac61baadb9940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17099795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c03fce14d3a24b732a7f461fe6aa444030c8ea1b0d17f5d917731cb1cea1e08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 23:49:34 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143512d4fb1efe79e1c3e84f2b8990d7b156fc8e76e4d4cf27437d2f7249dc31`  
		Last Modified: Thu, 08 May 2025 21:34:11 GMT  
		Size: 13.7 MB (13705862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889ae642b115a5dea458049a6805d2e61e2951183f78ba7b769bbfe585132f9f`  
		Last Modified: Thu, 08 May 2025 21:34:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86712d9a840166a79062b237035504d7b3bed52d21cc41857bf456669d01766c`  
		Last Modified: Thu, 08 May 2025 21:34:12 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:f9a8d6912acef39a6b62f2466f96378fe53b46a6e907bd15f186dd7914daeddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 KB (280828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef9d70079ca7408876f0355821a42e10b5549638e5d45bb3f1f0b538539e0a`

```dockerfile
```

-	Layers:
	-	`sha256:461152498186e16c914af6d05fda0150666d41ba53b152b895bf2c0f3dcc29bd`  
		Last Modified: Thu, 08 May 2025 21:39:20 GMT  
		Size: 266.4 KB (266411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbdaff0bf0e2267d5b6e47ce366e1d995e3ad6e6787e8be7798e25e11e93930`  
		Last Modified: Thu, 08 May 2025 21:39:21 GMT  
		Size: 14.4 KB (14417 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:b8bf4b1d638d8733dd20e469c1e8c902f1f1bdfe5a9f6da70e164aa08bdf688a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17781033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3e98ee98fbbbb01a549a53426ef1ce639fad4dd2a92b05f05e6ec36ef0d516`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e33b27c9b76515e1154a131a67e2f0fe88ba9e9bc48a1a704c790a0561e068`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 297.9 KB (297871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d4f3945f82cb36f20759bd5e4d3ea8be7671f4f58be8fde14e12cccd9bfb0a`  
		Last Modified: Thu, 08 May 2025 17:07:22 GMT  
		Size: 13.5 MB (13489522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b82d7f2276a68e0a1064324f6d64909ee13fb144e62ff3c9582d2c7d4c19703`  
		Last Modified: Thu, 08 May 2025 17:07:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1666b4f592cf9c56455ed01e495240c7e03c00b239ef9a9a70b1a73f044205b7`  
		Last Modified: Thu, 08 May 2025 17:07:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:ad5a92ffa0aa4378228838161e4438ebdb40bfdd9410e51d1c50b5a89ee2fa72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 KB (281642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2ad8109cf484125829376ef68cde0a71374dcb59674f25a212b3ae45010f26`

```dockerfile
```

-	Layers:
	-	`sha256:6d02589dee8d283cfa66dd7808cd63cb5852fc971fda911f5206e17b7982934d`  
		Last Modified: Thu, 08 May 2025 21:39:22 GMT  
		Size: 267.2 KB (267195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e360e62c15eaf48115988eae5efdc603b2d8502da0965b24a4338cff515cbe93`  
		Last Modified: Thu, 08 May 2025 21:39:22 GMT  
		Size: 14.4 KB (14447 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:f173625ac28e24fbb1e4755873200d0df442002462afd86aeb3ca14003c74ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17041713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e599ea2922d2f2e1208c49f4a86aee794ad45b536ead49704c687e78662e8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27442ea8b4dc6fdf584c0b30a8e1943de4b659fd7ec220499d43ff5c7d4c1c8`  
		Last Modified: Thu, 08 May 2025 21:39:24 GMT  
		Size: 298.3 KB (298274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba782946e954b7993574b6d4fbd42bf789f17f9931a7d35396dccd56534ad30`  
		Last Modified: Thu, 08 May 2025 21:39:25 GMT  
		Size: 13.2 MB (13168484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e0cee1df6197dc8422353c954238a97db6bf6927326f8c7721cd770b43f609`  
		Last Modified: Thu, 08 May 2025 21:39:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5816d31b3612108b1ee52d324d9d54b8af0c1a8b145833ee2c96724afcb15172`  
		Last Modified: Thu, 08 May 2025 21:39:26 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:e7dff0d1725359a80c55558e1f7fdb8d7295b3fd65aef8a255ee8a647769fae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 KB (279596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25408cc7b38e5d22c9e74865c260b65a31fb5179d40f87029c05c2a1fc4417`

```dockerfile
```

-	Layers:
	-	`sha256:be79c05e6917674620c5ec307d8b1c57d952af01f3afbcef1e71028a9ba0205a`  
		Last Modified: Thu, 08 May 2025 21:39:23 GMT  
		Size: 265.2 KB (265222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f1c5c1874fbc1846d75b0df96b5e91dbab8ca2b2641c0291949c738b0dfd67`  
		Last Modified: Thu, 08 May 2025 21:39:24 GMT  
		Size: 14.4 KB (14374 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; riscv64

```console
$ docker pull registry@sha256:ccbed7fa29b70c17b41ade04dc137cf5201c6a67ded10c841a5060d8d91448ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17537511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ef966d24343fb41053dc6ad886204a91b958e313bdb1f4898eff3a32526f2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 09:31:14 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b7353e85f9f8ac0206684e4063270c05a00cd4d76172b167229744dc0ee090`  
		Last Modified: Thu, 08 May 2025 21:39:28 GMT  
		Size: 13.9 MB (13890117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324c7a7e2f398fc67985e8c0aa5aaedb16225779163b1e8540fe671a3bd4c66b`  
		Last Modified: Thu, 08 May 2025 21:39:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7cdfca9ab92a172e8e2d1ca853c9c5a69253cd4b4e29fd3b3ee10d5895c06d`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:dae75c7beac87098ef5289ed9d35b0427d269a4f38134f490c702941ec84b13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 KB (279592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162a4b96ddc6bfc8f86900ade67d99d782fc011d0dc357bf588b1a4465fe80fa`

```dockerfile
```

-	Layers:
	-	`sha256:4a8e462adc723873ce8ddf50a091b488c965663c0b97ade9bb594503f8c00459`  
		Last Modified: Thu, 08 May 2025 21:39:25 GMT  
		Size: 265.2 KB (265218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e28318ae55df529a5b2906c34a7c2e649a8f55e65af7bf6bdd97d4b47ee5c50`  
		Last Modified: Thu, 08 May 2025 21:39:27 GMT  
		Size: 14.4 KB (14374 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:568befd308146d037135dee23a54555ddb0a2c0b9b8a77293403c36f92eeed01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17828305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b830b76ea9a73f4c882f771f3178c616506f53ca878ba4629eda7b310c00e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
RUN set -eux; 	version='3.0.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='61c9a2c0d5981a78482025b6b69728521fbc78506d68b223d4a2eb825de5ca3d' ;; 		aarch64) arch='arm64';   sha256='6c2ee1d135626fa42e0d6fb66a0e0f42e22439e5050087d04f4c5ff53655892e' ;; 		armhf)   arch='armv6';   sha256='e038bba14c573628407d9f5dfa6b6f9d782acda62abf52dbf24ab257bbeedfe7' ;; 		armv7)   arch='armv7';   sha256='147d617e604e2e7d11b055484493c6a20731f6ce252d2bc47c716d8c48258719' ;; 		ppc64le) arch='ppc64le'; sha256='5386e9811790616d5b3c4d5de2f449e6da99f03dd45f33ee3e3464e81a264e6e' ;; 		s390x)   arch='s390x';   sha256='c8645e6fcebde5a441e1050c673b3ffa38572f61c1d1b1605d2bf333d3760328' ;; 		riscv64) arch='riscv64'; sha256='99bfeef7c553bf7b9861435e6b55fa584ecca73704f4a71418e482cc2d9e013d' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
VOLUME [/var/lib/registry]
# Thu, 03 Apr 2025 13:26:51 GMT
EXPOSE map[5000/tcp:{}]
# Thu, 03 Apr 2025 13:26:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Apr 2025 13:26:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Apr 2025 13:26:51 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be80be2c55902add1c4b1f14066b1b4da724beaa2e355b53f8dd45b4887d9b9c`  
		Last Modified: Thu, 08 May 2025 20:29:45 GMT  
		Size: 296.2 KB (296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce32c938e0bce4c1726d2b421fa2169e9ad8d8cc7b03405bea7944f1ac40841d`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 14.1 MB (14063944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5ff26fb639a02f240d8adcb2df380a6a4e24dca5a803e98fa6b0210f6abc26`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51ea05070e17a1fe11d8fa1816b31d606454415d3c62e11363907f06173acb9`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:36d8e34b868e11078e746246f36717293796e7edc1fa6e52c561e29a66f32519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 KB (279516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43dd18649be2b0176cfa2eb8ee48bea449c7c3f8b19e9ceadf6d42028221544f`

```dockerfile
```

-	Layers:
	-	`sha256:a0a29cd12b383eb04f8963993182974b7d8355c5e417efecf04711205e343623`  
		Last Modified: Thu, 08 May 2025 21:39:27 GMT  
		Size: 265.2 KB (265188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fe0b53d54f933f15c946fa5c09345bb45e37338f93d62f723ee7840c95d5c2`  
		Last Modified: Thu, 08 May 2025 21:39:29 GMT  
		Size: 14.3 KB (14328 bytes)  
		MIME: application/vnd.in-toto+json
