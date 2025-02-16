<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-rc.3`](#registry300-rc3)
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

## `registry:3.0.0-rc.3`

```console
$ docker pull registry@sha256:baec50202770e4b0d9e017efdffc84bfe82f01998d80dfe9027f6294dfb6a814
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
$ docker pull registry@sha256:b430c590f513ec94749aea9cdfba6df81fcfdc189f0eb5b665cc9aa7e7ad1787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18321792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b7b9a0c309072e61aedad8278f696020009550ebd2d4d18901a0ecaebb3762`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Tue, 11 Feb 2025 22:14:46 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d8eebd466837c50e329b3eef32769635e8514ae41ad3232677d1da2b8c2c03`  
		Last Modified: Fri, 14 Feb 2025 22:42:32 GMT  
		Size: 294.9 KB (294868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd975e0eb2c920c206cbe1c24ef4c28fb5d1b62e389207bc5373552e60bbd3e0`  
		Last Modified: Fri, 14 Feb 2025 22:42:47 GMT  
		Size: 14.4 MB (14384066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084eeef1c707a26a2cf9f4f10e02d2468f92e6406d255c728cea0469424c9436`  
		Last Modified: Fri, 14 Feb 2025 22:42:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165265c642eab4e27ce65c4e3313ebc5596b0345ca33c620241943fe39f8d62c`  
		Last Modified: Fri, 14 Feb 2025 22:42:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:198718179a77f0cde27c7ab4831c133a0b12cb622baa4dcfe4cda4f27eecab73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 KB (280518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52a684dfc681d1dbcc16850e7839a97db1bb9ff8290a4f948c9ad16f17ac18a`

```dockerfile
```

-	Layers:
	-	`sha256:5e0855dd905f90d974d68a3273868b7a0e78194f66d11e66826267a01ce97e68`  
		Last Modified: Fri, 14 Feb 2025 22:38:56 GMT  
		Size: 267.1 KB (267061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4383778017e8d0715aabc154839f5a0de6ca72003de4ab9a3507eeb223d2ec93`  
		Last Modified: Fri, 14 Feb 2025 22:38:56 GMT  
		Size: 13.5 KB (13457 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; arm variant v6

```console
$ docker pull registry@sha256:456a83cc0d82713843cf36e2b67373e23536950db76f593308c4e8e64f1f5f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17178892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c46cae6f7e2b67b03d0b80fd23e227667f50935816abe5e0cc88faf7d15b19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Tue, 11 Feb 2025 22:14:46 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8610ff7eba13dc9df45a4eeb7069fcc134debe5b39c76be1018face7677fa`  
		Last Modified: Fri, 14 Feb 2025 22:39:13 GMT  
		Size: 13.5 MB (13517296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6a7a5d67e8b801a8e949b942369b1a549ea0eb0c7f3141fbab84880a88b6df`  
		Last Modified: Fri, 14 Feb 2025 22:39:12 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6f66f98998e68c79f8a3b6ec414f388ad98e97bcbec20eb4ab69b775bab484`  
		Last Modified: Tue, 11 Feb 2025 23:30:15 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:7ce94b347b64fe5b580113cc713a9ee523da06d0b0e80636a67e1f6f56ed1553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63504a50bc88179c5b4935950e66493ec1d3550dc9f01a373fb56ac80e9906f9`

```dockerfile
```

-	Layers:
	-	`sha256:a7d7c9078da29828f4b3b535edf0e052e3e12de71b53e5a131562dfa23654c3e`  
		Last Modified: Fri, 14 Feb 2025 22:38:58 GMT  
		Size: 13.3 KB (13307 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; arm variant v7

```console
$ docker pull registry@sha256:7d759bf90258361f232c593b6e6caa5f2939d4bb1e4e1b2e508ac6d50fe233ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16898028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c89183085a6a03fa6cf104f57e573b18aa59f354f5427390289a46f6e6d28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Tue, 11 Feb 2025 22:14:46 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 23:49:34 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2612ed5569e5f0f77818323df302652e4509b8f4d8e9814f8fe22b3be23d10`  
		Last Modified: Fri, 14 Feb 2025 23:49:35 GMT  
		Size: 13.5 MB (13504096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6a3085c1e4b81222063184f162188ae4ac3061857bbde73afc61ace2e59ab`  
		Last Modified: Fri, 14 Feb 2025 23:49:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df24e7d7afd68b91819169920e785f91fd691165648b2f2649849fc6e9d6bb41`  
		Last Modified: Fri, 14 Feb 2025 23:49:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:191da8cb5019974357b56dee258e814d503d03094a1eab270da1b6e9eee0f005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 KB (280595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04edc473d3aeda6baa2357e5c123ecc914f2038eb7f6806f05e9b375ca7df66c`

```dockerfile
```

-	Layers:
	-	`sha256:f9b9d7809c8c47d5453241c92520a507baedad677a680e6c450c3cd07d58ed7b`  
		Last Modified: Fri, 14 Feb 2025 22:38:59 GMT  
		Size: 267.1 KB (267073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb6d6e6a22ffd935341512e0313d4ecb9bd77ade8230e45957d432768fcd680a`  
		Last Modified: Fri, 14 Feb 2025 22:38:59 GMT  
		Size: 13.5 KB (13522 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:695402e6c9a518c5381f52b90a366b33870256ec57d9b5d0b3c8c2325004a820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17578469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76974e3100f954e273b33ef0ca308c1f0d3a7e4ba6c5622b247dcbaeb4ecd858`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Tue, 11 Feb 2025 22:14:46 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aa1d43e92f86dc074668d0ee29a76fd40e91e4c4142a8f0580170417c1a1e6`  
		Last Modified: Sat, 15 Feb 2025 00:23:39 GMT  
		Size: 297.8 KB (297842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8253751fb951143233f4b968236b4ca26e7d73358023bbdd0d5d048221cf65f9`  
		Last Modified: Sat, 15 Feb 2025 01:12:29 GMT  
		Size: 13.3 MB (13286987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97abd9ca292d05cb7975b33967c409ae9b53e40aa0eb06f6bf5236d62f46125`  
		Last Modified: Sat, 15 Feb 2025 01:12:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0f15aa0ed800b84585fac8cbd1b5b6b09697a251b6ea52352113d0f3a964ea`  
		Last Modified: Sat, 15 Feb 2025 01:12:27 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:9970e52aa8586ce5ef2030fe6f5b436fe17c2fd0d259c8c11f8a237b6c991553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 KB (280621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d190f2f7688dc2b0f81b236c85cf6cadbdad48bc126f8ef069ab51359f3fbcb7`

```dockerfile
```

-	Layers:
	-	`sha256:e46337be8444a9174f6b79662abb7c0ba56eb849fce30e95cef7a88c220702dc`  
		Last Modified: Fri, 14 Feb 2025 22:39:01 GMT  
		Size: 267.1 KB (267081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63402f3767e1f70abcea216f27ca1be8ac9521d09c1fd4c5bbfcfc8a55ab2498`  
		Last Modified: Fri, 14 Feb 2025 22:39:01 GMT  
		Size: 13.5 KB (13540 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; ppc64le

```console
$ docker pull registry@sha256:b0346931ce6e62fa535a6c44e325e17fea4d8b5802ce99972222094c479cbd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16837880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e969a226382a21c11a3f25f6ca0f4ff3cc9605f953cb991bec21da8044738bab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Tue, 11 Feb 2025 22:14:46 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542036b0f90df8875e93add192346f3bcc8edd586aa34c11a6af80938cb06173`  
		Last Modified: Sat, 15 Feb 2025 00:31:41 GMT  
		Size: 298.3 KB (298267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226b5bf9239b4979dcc435664e1ceb5603821891ff414c4ca433c8e95e309561`  
		Last Modified: Sat, 15 Feb 2025 01:12:29 GMT  
		Size: 13.0 MB (12964658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3b350d73eb5d5acd261f7f36698dbe84052b47702d51b5af5023a8872c02ed`  
		Last Modified: Sat, 15 Feb 2025 01:12:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00a13624eec9a4c113bc355a8137ddc66a5e1ca095248031272e7dadf79ab32`  
		Last Modified: Sat, 15 Feb 2025 01:12:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:f51a177410e6967a74fdb82551ee419b75d2fa1c1630d5ea5823f47024c58387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47897a3a8f388c25a5a5d5af64b965db544c69da8f0d44988e1fbd476daf7faf`

```dockerfile
```

-	Layers:
	-	`sha256:bebd7015d1c32542ed959f85488983b3df82a5cc80733246ada67cda00360bf6`  
		Last Modified: Fri, 14 Feb 2025 22:39:02 GMT  
		Size: 265.1 KB (265126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d97452806aad9cc4df0cea29fe77cd80628f4b6c8bd3c4d7f48f561c77259db2`  
		Last Modified: Fri, 14 Feb 2025 22:39:02 GMT  
		Size: 13.5 KB (13485 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; riscv64

```console
$ docker pull registry@sha256:fe38a08bed41e65038a26adef9f95c3bf280e75e5f280ed3512398711d143f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17319418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae2a1836886e5153747178c6780bec44d7090d631a578e243c3432d5ee19ac4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Tue, 11 Feb 2025 22:14:46 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 05:52:00 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1476fdbb66e72839670398357898b33e7e1971d6a95b6359fa00965e2d510191`  
		Last Modified: Sun, 16 Feb 2025 05:52:02 GMT  
		Size: 13.7 MB (13672021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1706949909c1a738c579288ae9d8f6e6d7e9df2aa0fae2af703128756949d828`  
		Last Modified: Sun, 16 Feb 2025 06:07:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21739a9cada8d0f71d368c9c12de7d7944e30832a0f5110b4fb37058c8d0f2b5`  
		Last Modified: Sun, 16 Feb 2025 06:07:18 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:391fe55010dbb11a9b00ab3a257471993e417b0a217edbeb76fc5575993c19f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d88a9cd901232f93f27c864f52d6769e49010859acdf4a532cc0ea8a9c9ed8`

```dockerfile
```

-	Layers:
	-	`sha256:427a0b11c13c83b66e4b25fcfae382ec811f599814079196d1f3cccdd53ae31b`  
		Last Modified: Sun, 16 Feb 2025 07:38:29 GMT  
		Size: 265.1 KB (265122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e25805f6d0fce7da7fb7e540effc3b359fa815db57ccb3a5c93c60f7cf59e255`  
		Last Modified: Sun, 16 Feb 2025 07:38:29 GMT  
		Size: 13.5 KB (13485 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.3` - linux; s390x

```console
$ docker pull registry@sha256:d7e49a8f5089af77a38d9a1e39ef35146148924069b084d9f9be4e7f8a88d49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17616634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297475f2eb99f3de67e178232cc855bc2783fb9e9258dacef777b0831d4d2654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Tue, 11 Feb 2025 22:14:46 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 11 Feb 2025 22:14:46 GMT
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45367ec7901486a744e83b8e8c40908894d960175ae2dea51903497a09542717`  
		Last Modified: Sat, 15 Feb 2025 00:31:43 GMT  
		Size: 296.2 KB (296178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5407cb0913bdf8c1ae0ede260b2c5e4834b5aeb2cb0503c2fcb59b7f00b39e8`  
		Last Modified: Sat, 15 Feb 2025 01:12:30 GMT  
		Size: 13.9 MB (13852278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4153e8c198b26e23e24aae98c4e79754c6c99bffb0e2eb22912effa77630bc`  
		Last Modified: Sat, 15 Feb 2025 01:12:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b4f322a2bf85030427730dfe619c05a24cc4a900908d05c5244fcb2fde5a18`  
		Last Modified: Sat, 15 Feb 2025 01:12:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.3` - unknown; unknown

```console
$ docker pull registry@sha256:9a53438b1df324c07471cc7e9db59e60c03ced32ecc13d9c97421eea2bc5be19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 KB (278557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008a3ba41f96effa7f9b9d7a1c7114f9a8512ec9733ff48ae707ea4ee75f5add`

```dockerfile
```

-	Layers:
	-	`sha256:aea6147343c20b229095781aec7813694707adf3cf39f843c3f37d6ddbaf14a5`  
		Last Modified: Fri, 14 Feb 2025 22:39:05 GMT  
		Size: 265.1 KB (265100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8732c0405a3855e9abe273bbb511e2c0b4955f414b8b695f05278a6989f7b295`  
		Last Modified: Fri, 14 Feb 2025 22:39:05 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:27 GMT  
		Size: 180.1 KB (180062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a76c78501fbd32c96667efc8c07506d8a4b52d8ee80f1dd12c5184e92e7fdd`  
		Last Modified: Fri, 14 Feb 2025 22:38:27 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:28 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
		Size: 180.1 KB (180098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1970e71b094e5b797deb75611d0a98cd09880f898ae91b4f82ba89fd57520d3d`  
		Last Modified: Fri, 14 Feb 2025 22:38:39 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:41 GMT  
		Size: 180.1 KB (180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a5ce400b19e271e46772e9b6dbabc4a372acb92f7693cc032c465c94ee0a8d`  
		Last Modified: Fri, 14 Feb 2025 22:38:41 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:32 GMT  
		Size: 178.1 KB (178145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9fd8d94c257b5cfdd6dcb57c64d7a4431696c2074d2d0896ae36f18304c4d3`  
		Last Modified: Fri, 14 Feb 2025 22:38:32 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:38:33 GMT  
		Size: 178.1 KB (178111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ee0fc123440180ad56dbb3639d50d42c8e882e7dcc1c662f421b4f7beaeda9`  
		Last Modified: Fri, 14 Feb 2025 22:38:33 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json
