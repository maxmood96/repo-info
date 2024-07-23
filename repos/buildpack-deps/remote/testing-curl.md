## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:ace5a86d83dd0b90e17b6bc4438210d5af335390e3bcb90bcf2b668eaaf1928b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:db7e1584702e2ce2c1843e73785ea850b91f22b67a0057a09fdef7e43de922ff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72116850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbbda00da917e7c15e5ae572efa6c80ac276fd353d004993e53fb8b8c27c91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:26:17 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
# Tue, 23 Jul 2024 05:26:17 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d0f848dd15a13c8823fd99e5306acaecabecb24a04e2148715831928b219f3`  
		Last Modified: Tue, 23 Jul 2024 06:16:13 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:db1f5252158b47f3f9fa5ed5624b494ab78c51d4463b03f107f133fbb5ea5f49
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73217722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b039e1e67b088cf0cd7c850addcf872710e237ab7ea3dfa3aaca588c77ac4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:14 GMT
ADD file:03b45e1df3fc6931a8ddcada5ff0a44361f55a5f77b85b332a37efac67af70c7 in / 
# Mon, 22 Jul 2024 23:59:15 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7c6b0161e34fdad02b8c4ce71aed07442e95f3916056ffa8fc8957d554429aa6`  
		Last Modified: Tue, 23 Jul 2024 00:04:42 GMT  
		Size: 49.8 MB (49807789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aadbc8644d3857b913228d91ab9cef7cad02ed0c4961160ca60a012db531734`  
		Last Modified: Tue, 23 Jul 2024 03:56:12 GMT  
		Size: 23.4 MB (23409933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f9dc952f28f4f4fd3c026313044d8143b61e1b9866c641dc75f5fc704e353656
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69798698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2989804b2d5db3e6028493ab7b4716ed548cfe707075cba70ebf5708623bf36d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:05:07 GMT
ADD file:b71b90e852d24ff72e11c891781becf7dff5c6b7913fe6f75d4afaaf9dd0fb77 in / 
# Tue, 23 Jul 2024 03:05:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6a5c1f2df69e68e08287b3688c735ace9ad27b45503738288df9d10ef7066ce1`  
		Last Modified: Tue, 23 Jul 2024 03:10:02 GMT  
		Size: 47.3 MB (47313443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cc17ffe2d1d252bf936d01f2e7c153c81aadb436d6f199344bf17351709fb6`  
		Last Modified: Tue, 23 Jul 2024 03:50:59 GMT  
		Size: 22.5 MB (22485255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6bb5571000683cf101650820e0d2d92a728fde43ba391c4681078488b9de8110
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72060023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f9059e1f660e5d3c88f5c6fcbd1a8e538121c1ca202ab22d18e4bd75e80a06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:19:11 GMT
ADD file:36c12887052d1b06bbaec01740a2cd1b9dab4bc7827e406c3311158554478418 in / 
# Tue, 23 Jul 2024 04:19:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:493524e4a43f41421b39cb784ceebfde54145b94187eac6910c35f8178b410da`  
		Last Modified: Tue, 23 Jul 2024 04:23:05 GMT  
		Size: 53.0 MB (53026321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1a0ede68aa727c607d43ae4be3b7578d31d87709092b02d36e3b7e4a0fdbbb`  
		Last Modified: Tue, 23 Jul 2024 08:12:40 GMT  
		Size: 19.0 MB (19033702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7cccd4bbf4ceaf8dbca6aa841b6acb4b4d23f4ff686fbed7962ee9e81012c58d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74035615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442401ad9c62f629aa9238e9a3a47f7d55640fda00a3ae58c6c0958692b0cb9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:56:12 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
# Tue, 23 Jul 2024 03:56:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03acf0ea95beaeb6fc7c7cfac20f5747058cc54deb10ec36249d791cf845b7`  
		Last Modified: Tue, 23 Jul 2024 04:52:34 GMT  
		Size: 20.4 MB (20354365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0f420425a3e3e552c0a70a1c436e26f5e2e750c3914e1b22d7fbde7af0aa2873
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71407154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f58ed6eff53d376e39f4903d043d43b4a3d17e197634c8e49ac79add3e8172c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:44:48 GMT
ADD file:392fc10c04bd3df02b9ce57b447e54a4d1bcdfb0ec61a622808e7db6f2f1914f in / 
# Tue, 23 Jul 2024 00:44:54 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:50:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c50956a8a7195506ef530c7c5f445057322dc9fe660c45a79ea6c6084874804`  
		Last Modified: Tue, 23 Jul 2024 00:56:14 GMT  
		Size: 51.6 MB (51636151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff87574102eceba634bda143ff5b2bf4b17818f5418215956831655aa15d6f1`  
		Last Modified: Tue, 23 Jul 2024 02:08:39 GMT  
		Size: 19.8 MB (19771003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e5f97fe3f1a48f9e4aca45af9b3b7e87ba798a8ba240471261f529a919152f52
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78017519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebba4d5b7f38f8bf724f7d03b2866b7ddd69981687a27b688571964bc6e68e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:29:19 GMT
ADD file:3a2bd17a40219dbb040555571523f8df1fea9b1d1a82249388c40cefedfa6de9 in / 
# Tue, 23 Jul 2024 01:29:22 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ef086634154fd58171058df19eb35df551381968a0480be4625baa26e8bd8a54`  
		Last Modified: Tue, 23 Jul 2024 01:34:29 GMT  
		Size: 56.7 MB (56722073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58910df9409127e8ce8b003f5bc4570e63366685c5b298d2bb94fc69d37fd17b`  
		Last Modified: Tue, 23 Jul 2024 02:45:21 GMT  
		Size: 21.3 MB (21295446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:89d1d494114c9c2f0f75857f06665f950ca2720c93062acc91e730f6fd4a4173
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72893401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475f6498b1cd64a3a88462fec2b32b0c627d87abb7acfbaf75d585798ac49973`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:30:46 GMT
ADD file:5991487b53c92b85f56a9cb6ec51789428cf5b58777f5dee12014b0223fc1434 in / 
# Tue, 23 Jul 2024 02:30:48 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6deaf86d1b7bfd5bc637ea83983f978199741e71e1597a41b9ad7983be78ad34`  
		Last Modified: Tue, 23 Jul 2024 02:35:01 GMT  
		Size: 52.4 MB (52414237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd707523e73e3eba57ef16b7ac55b16771f34411fbf8a78ce790f60d615035`  
		Last Modified: Tue, 23 Jul 2024 03:16:57 GMT  
		Size: 20.5 MB (20479164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
