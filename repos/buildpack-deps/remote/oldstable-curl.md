## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:f3fdd576027cc8ac7ef09484c8bb9ac0a9d2a06aef29e31c20cbe702d9696518
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:808c3c4795518eb91ba7d7fcff4c728ea3b39164a5f917bacc45dca81689f09e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68268694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce970a84a0280fbe5d5ce8e8ccbe7593540faf43ba5f74f73f0102ae1a12edaa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ad2bce0e73d4bfc9147607f9bc656bed7d69c15e9cbd5b16e7fd08e17ccb1b16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65219323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c951ff2760221da3aad3f3e33d852fbbeafd3fc74d508624915219fe7315d8c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:20:13 GMT
ADD file:730b9bc3596fff58668f18193a6ea2255ca145eaf1b34fa9d8810bdc685868ba in / 
# Thu, 17 Mar 2022 05:20:14 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:19:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:20:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:32f373add1937d0609f8db562b840e805dfcbf8545b161486c2b18b6752b249d`  
		Last Modified: Thu, 17 Mar 2022 05:35:48 GMT  
		Size: 48.2 MB (48154250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e73ef17629896e33fd24b8b4b6fab0cf090ae9f9a5f2bc403ec4e6d06421029`  
		Last Modified: Thu, 17 Mar 2022 19:42:25 GMT  
		Size: 7.4 MB (7377462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21228a64db1de7ed42a10a883608f6da2a28899d3161a13ad9a3c4ee8142b97`  
		Last Modified: Thu, 17 Mar 2022 19:42:26 GMT  
		Size: 9.7 MB (9687611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:26634980f4fbdb94e0a1ebff55a216a9b698c420920fb94b5a710fbf38a8d872
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62387171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a0e46ba61488d5c583b880e1e015c6a5eed90b0675e061ced2d524ed971875`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:29 GMT
ADD file:49ab7c627696d55c8512392867bee4593a377d34c5c4f75aac1eb176a56b672c in / 
# Tue, 01 Mar 2022 02:03:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:30:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5e77565ce5247d53df5dcb65e54c6d6e73e60996d11fbc1ce5ee34bf80dfa1f2`  
		Last Modified: Tue, 01 Mar 2022 02:19:53 GMT  
		Size: 45.9 MB (45918104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b40356d157bf4856aec771f3f51360d39ebb8715ba13f6f19d8153416eced08`  
		Last Modified: Tue, 01 Mar 2022 09:53:58 GMT  
		Size: 7.1 MB (7125246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02534a5c6a025b55da20b42dc333e67684e4ef06a3b2d46d0b0f00543548e29`  
		Last Modified: Tue, 01 Mar 2022 09:53:59 GMT  
		Size: 9.3 MB (9343821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:13b805388986d203beb8a143f8ad4bfc4102e1cc40a7992098fa845ccac9a727
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66685545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96384cb262ca4b16a0bb18a01add8bfcbb6e008497af8df0e6276c3ac95ac47c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:08 GMT
ADD file:37cabd1fec04269c22fc158f62ce5bc655934f2e58fb1ff3a1e366a33ba9bc18 in / 
# Thu, 17 Mar 2022 03:22:09 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:12:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3996f04b7c6c17d8b25c04c7287353b896b4a0b10ab440f47d00573a7d5c3e17`  
		Last Modified: Thu, 17 Mar 2022 03:28:59 GMT  
		Size: 49.2 MB (49222993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80907b498681187ef4aa817ec6f39ba351e376afbb4fcf4415841ab9015cfc59`  
		Last Modified: Thu, 17 Mar 2022 22:22:15 GMT  
		Size: 7.7 MB (7695349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8327dc7899c1a628cf11f95bb594fca3c86e45d1f4f0eb73d2ba9058eba5927`  
		Last Modified: Thu, 17 Mar 2022 22:22:15 GMT  
		Size: 9.8 MB (9767203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:65c5b2a74cb9885931274d82458506d6d9e248c9de986d0266d13f4b8a04ed56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69548204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1ecaeb57d80945e1bab47a5788e5204f707c1af26d7a3d606ed23ea93f0fd1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:47 GMT
ADD file:bdcedc0826a512fa5720a5481555b67977a75cc3a2c76cf5525f4067f6e30f78 in / 
# Tue, 01 Mar 2022 02:07:47 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:42:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:476db560471d1237921e304e3ff8f4080b6678e161577b3284ac8cc10eeacb64`  
		Last Modified: Tue, 01 Mar 2022 02:16:20 GMT  
		Size: 51.2 MB (51207695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c26a779ac27dbfd1d496436ab636b45a1a0157570daf0fe074b2b128251084`  
		Last Modified: Tue, 01 Mar 2022 05:53:41 GMT  
		Size: 8.0 MB (8000492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f554cfd6e25d31263311f533991fee169f308525eac5bfd2a37a744aca5580`  
		Last Modified: Tue, 01 Mar 2022 05:53:41 GMT  
		Size: 10.3 MB (10340017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3013165773a5014aa0c3767ccda0458373fd5899fad858411fb539f00e4d3813
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66133633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affc081a0992a55318fdd7e2676a9d2846017e472a3b9888e7f352419e4c77fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:53:34 GMT
ADD file:a0b3ac9e4bfb39c253a8a7a55fb55d0b908af833cdcc9931837698ec5f55b989 in / 
# Thu, 17 Mar 2022 08:53:39 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:29:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:047b7fb675b6ff99fd7dedbd4d0b0a3242855acbf0be0e3a69b39ea19852bf7f`  
		Last Modified: Thu, 17 Mar 2022 10:44:02 GMT  
		Size: 49.1 MB (49079461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55203676937c9ec933fb27d1c8139cf1a83a5d5d392495e941a0824319a07428`  
		Last Modified: Thu, 17 Mar 2022 19:54:04 GMT  
		Size: 7.3 MB (7253901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af9a4d78faa84f9b4e38f2bd9489ea3e3fb4b460d64cc87d7a259fab08daa46`  
		Last Modified: Thu, 17 Mar 2022 19:54:04 GMT  
		Size: 9.8 MB (9800271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bfbe544ddda95cb4c9188945e6c7f06a1a30ecdfd7536c29c946d01b4bb4e233
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73184484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5a07d8754946c2866a2c269cd49ed8fd627594cc6946805d3c78ff31f4f48d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:05:31 GMT
ADD file:b0fccd713cf7d422b1caea3a5d8c8bc230da590e6004fb58a27f2e53589bb87e in / 
# Tue, 01 Mar 2022 02:05:38 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 07:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 07:18:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3af27652881c17f6980cd7f32718c45cc6047a3391b74b55f499341c8efb5ec5`  
		Last Modified: Tue, 01 Mar 2022 02:15:48 GMT  
		Size: 54.2 MB (54183617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2afaad5be738f67c67e6b3d540b5a3dcad788dcd8f5180f494ca1465ac0c03f`  
		Last Modified: Tue, 01 Mar 2022 07:43:43 GMT  
		Size: 8.3 MB (8273085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd41299687186ba7a9a5ca4d29f672f8a2ef6047cbb81a80e5c8b78fd082580`  
		Last Modified: Tue, 01 Mar 2022 07:43:43 GMT  
		Size: 10.7 MB (10727782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a806c4c12568931cb2ed0fbd0489d31a4882a4d805be9755bf4af40368869cc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66290297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a04780d8387099d759848dfea68450567904614e65ace0917a2fa30e16ce4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:07:11 GMT
ADD file:6505b8e134084dbb9f879838b24cf47cd265cfdc5952f50ba2ddc63ff4553145 in / 
# Thu, 17 Mar 2022 03:07:14 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:22:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:22:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1e9fa32475c4074341da88d0325d6e125bf7587795cba4bef553a90bf7472c7b`  
		Last Modified: Thu, 17 Mar 2022 03:13:01 GMT  
		Size: 49.0 MB (49005525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dfc7a2d5d979460a379f74fd1adf756566aaaf27b9ad22b518b7b0b13b7b2a`  
		Last Modified: Thu, 17 Mar 2022 18:29:59 GMT  
		Size: 7.4 MB (7401708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1517a8cbcd9e9cd84fd94cb3e7e7a02def9f47cf27b751461484d31f85725361`  
		Last Modified: Thu, 17 Mar 2022 18:29:59 GMT  
		Size: 9.9 MB (9883064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
