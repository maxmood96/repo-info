## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:962c18e03e3a548d04848d7a44c64607bef92cc6f76ee495ed5d624cfe5f6993
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
$ docker pull buildpack-deps@sha256:d8514e63c4a3c2e2f85d4780764a310dd571053dcebfd8a0272122338b1b2a9d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73269774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda8c74ff25e51a0b26780901814ecb3e483a365f6c61063abc2624f7e46ece9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:11 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
# Tue, 13 Aug 2024 00:22:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:47:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000d3eb244249a76a53e7b3f03c8e999bbac83be7058bc1aa1fe0eebb494baf`  
		Last Modified: Tue, 13 Aug 2024 00:52:48 GMT  
		Size: 20.4 MB (20428585 bytes)  
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
$ docker pull buildpack-deps@sha256:d760cba9cf75b2188cd1842bb29133073fbfc53459b4026ea5aca60df2b169d6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73322085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e6bfac275b3e8319f6055f236d849e2504b85b69739aa0f3e5adcf26efe21e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:41:11 GMT
ADD file:44df8bf38e0a6481ddb1093ad0c25ca4508a15c2b5d1c0733757db62627a7413 in / 
# Tue, 13 Aug 2024 00:41:12 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8858b14d914bd710ce161898770a04753f6d66b911364becd105945179fc07fa`  
		Last Modified: Tue, 13 Aug 2024 00:45:37 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbc2390559926818fa461fbc23891f666f695df10963c68e66dbcd7d2a33119`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 20.2 MB (20169643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5d4fec0eb7d196988a99411e3ceb68545272536f7c53235a2c611ec0d9ecd380
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75222611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98cf295bc53b37cf4460d54ffcde842606c4ed9ef6385b5b153980e8310264e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
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
