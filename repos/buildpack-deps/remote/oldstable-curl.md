## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:02493b823622f2fcbbfceca1c33308d5dafb344814c6ffb5b36748d63958a516
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
$ docker pull buildpack-deps@sha256:afdcb0c8532016704d3f0c15c568b957db7fc424465c1f9ad9eff84e49d47b97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68295538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575cae7b284f1a8a1ef7acfd6292f8c896657ddb4c1323eef0f5a120ef9efdad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:20 GMT
ADD file:d738977543f4afc4c3040c6fca3e3f15388ec3b7263a29a6aa83f9a4bf05fed1 in / 
# Tue, 12 Jul 2022 01:20:21 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:49:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:80b89a2b88b24e7be7c8038e2cbff99ad4fd2f07ad914da4bab80dabaadf8a99`  
		Last Modified: Tue, 12 Jul 2022 01:24:55 GMT  
		Size: 50.4 MB (50440555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0405f798f5b335d83b02371187f3be0ce2092aa0c6b6178ff11290ee6a14c9`  
		Last Modified: Tue, 12 Jul 2022 02:56:14 GMT  
		Size: 7.9 MB (7856888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab80b2b0494ab26b41941fb73a028292e2e5d2070c56b3488e890eda20e04641`  
		Last Modified: Tue, 12 Jul 2022 02:56:14 GMT  
		Size: 10.0 MB (9998095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0d3e12553ec499bfb2bb9e4bcb5b0795a30fd34e8d907a70609f84f34f4ba91d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65250367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaddf429ddd182079023416df77a9606025e7bf83a572f5517b6828e3affdc6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:51:06 GMT
ADD file:46ca1be3e2e70869adc2c2213ad21ac3c743f1c7c0bbec927f855a82888f603d in / 
# Tue, 12 Jul 2022 00:51:07 GMT
CMD ["bash"]
# Wed, 27 Jul 2022 19:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Jul 2022 19:56:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:83500cf45b6520b8ee0db35bb2065dcec25da5fca7b08fdb211039411146182b`  
		Last Modified: Tue, 12 Jul 2022 01:03:49 GMT  
		Size: 48.2 MB (48160548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3614dbc8455f283a03bbfe3df1fdec54f70177c8a2a7471eb91ee4d0b7868470`  
		Last Modified: Wed, 27 Jul 2022 20:08:49 GMT  
		Size: 7.4 MB (7401174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690635105de975fa2ba9c9de6bd3d35669dc154872bbec26d9f0669035ff8473`  
		Last Modified: Wed, 27 Jul 2022 20:08:50 GMT  
		Size: 9.7 MB (9688645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a61b0e490b0cfe7736403a96cf270ca09a259e53a42f15b7225a73e2d597e92d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62405300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956c4f27235a8a95ab69db445b5252ed606e1096d5c86d52ed4c7fd329860574`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:00:25 GMT
ADD file:8795228d7a914d37160bb846066961f7c4c5f5da1452e6ae888a2a766cd8739f in / 
# Tue, 12 Jul 2022 01:00:26 GMT
CMD ["bash"]
# Thu, 28 Jul 2022 13:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 13:28:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:13036b2c6f13fd64780f7786c065cc2f0788024adbc684878bc4e33285ffcd1e`  
		Last Modified: Tue, 12 Jul 2022 01:13:22 GMT  
		Size: 45.9 MB (45915505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ee655d152d3acb35f3825891e9643f3691ede0af3d9d3d2148308272ad147e`  
		Last Modified: Thu, 28 Jul 2022 13:54:29 GMT  
		Size: 7.1 MB (7145473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69443875e8fdb06680327c732654bbfa6b479a256d0d865012b3f931609bd0f3`  
		Last Modified: Thu, 28 Jul 2022 13:54:29 GMT  
		Size: 9.3 MB (9344322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e7ceaa6430a5f1563bf49da0745dbeba22de384f00c716070e96fd9a2e930c43
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66717603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab9f0de7a50e38a1bd04d8fcf1ab6cc53f735989733f0c7e67a2da8ff8496c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:46 GMT
ADD file:ea39534c5e9a548d7938f6b0e2459383caaf3906f3cc5eafe8bf66053b19f2d5 in / 
# Tue, 12 Jul 2022 00:40:47 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:34:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:891a1587d3644a8b4b6dab3726ef380a725a0e19bfbf0eac02a275f711985862`  
		Last Modified: Tue, 12 Jul 2022 00:46:46 GMT  
		Size: 49.2 MB (49228928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5d1ed6a27dab15e77b7afa9c8697a170f017a73ec9ea8f3f00d5f322e1d3ab`  
		Last Modified: Tue, 12 Jul 2022 02:43:49 GMT  
		Size: 7.7 MB (7720027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186afd5d5e89c602b988d31dd5210c9e3c19435f849f6cc4a6a22a2388e83cf`  
		Last Modified: Tue, 12 Jul 2022 02:43:46 GMT  
		Size: 9.8 MB (9768648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1e087ed8bde321e0c0132bc099f33819e285b96703957edb08e0384f688c4821
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69350591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135a9f4f2cadb7a742c5303ec8bd99c54f895951df4e62a8fb1b94cdbb3173b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:39:39 GMT
ADD file:0f1020fa1fb5b3518ec765b21180056cc802ac9258d1eed5e109edd83e0038d9 in / 
# Tue, 12 Jul 2022 00:39:40 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:28:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:28:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:87a13c20a9000f48185a3819712d2a14a8ddd6111bd1392856609aa18a233847`  
		Last Modified: Tue, 12 Jul 2022 00:45:40 GMT  
		Size: 51.2 MB (51204001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798a6241824db4c4cb7e4997fe37c17a97c4d76bf1fb544730ccdbbbc9aaf8e0`  
		Last Modified: Tue, 12 Jul 2022 04:37:13 GMT  
		Size: 8.0 MB (8022957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a99684560fe738e37dc34fae618fb12d6be36f03ccc22266fe649cb7bbb61c4`  
		Last Modified: Tue, 12 Jul 2022 04:37:14 GMT  
		Size: 10.1 MB (10123633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:34c2bbdc7bbfc75d29f8ff579447db8379921b69c1359ad1a39268672cf552df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66147238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d33eff158a70c0565008f898c339d93235ad7c294714bf9841682bdbc2766d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 04:41:32 GMT
ADD file:8ae876ce5db0069235a78103d9a680e349fc6b910a6111ea49467d374abbfc60 in / 
# Tue, 12 Jul 2022 04:41:37 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 06:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:18:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f63d44b039884b9b81e12964f9b3c96fb7d550431e7bb657b94e25e0aaa6bb37`  
		Last Modified: Tue, 12 Jul 2022 04:52:25 GMT  
		Size: 49.1 MB (49073132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c7a5d202e81fdd1d4ce140e78b454956f14227f4349a35cd40690c076022f3`  
		Last Modified: Tue, 12 Jul 2022 06:43:42 GMT  
		Size: 7.3 MB (7273075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb7b23ca08db2ded7c067fb3a76ba6a87e04788fafc9d03045c18ed1b73631b`  
		Last Modified: Tue, 12 Jul 2022 06:43:43 GMT  
		Size: 9.8 MB (9801031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f88c82a2d888734ccab78b9221f456296bd38f0ce038d04a107e827413628344
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73199468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469e20bc6fdc78c28c3b5e7d444cfcd08e81bc06e8436213b1e56112e3041c28`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:48 GMT
ADD file:2148d05c090aaf9547831ad92d0e8afca3df183ef38c21db2a5b8962fcc3bfa0 in / 
# Tue, 12 Jul 2022 01:25:53 GMT
CMD ["bash"]
# Tue, 26 Jul 2022 22:44:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 22:45:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:985c65736f23a90bf354a992729a4278b1841d9385b35f881ba5b8293ce58b29`  
		Last Modified: Tue, 12 Jul 2022 01:36:56 GMT  
		Size: 54.2 MB (54177075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7a789c037c1213028caf90471958a150307f11fa83385599382efd4359871`  
		Last Modified: Tue, 26 Jul 2022 23:49:47 GMT  
		Size: 8.3 MB (8293658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b74f28090e08e85a0bc514eff519f0a818a4ba5ba4a35fa902374b14b9ce9e0`  
		Last Modified: Tue, 26 Jul 2022 23:49:47 GMT  
		Size: 10.7 MB (10728735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:334bd5b072f2a1bd4fa453d60bcbcf07cb7717c6d096e1a5c98af330fea5708b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66315922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18306d642a29c6c1ea5f1785b334947eec05a04a64bf2182c03204718bf623e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:44:12 GMT
ADD file:b8babeb1255f220a475b65f77c9d786d49eda80433cab5dc00c944dc05d31c77 in / 
# Tue, 12 Jul 2022 00:44:18 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:42:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:99ceea1856d0a41d4fd9ea8821ed7e159ce3cc53839fdbed273f1a57f5d9f5b1`  
		Last Modified: Tue, 12 Jul 2022 00:53:59 GMT  
		Size: 49.0 MB (49006967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d39886922611614df255183efa3a602bc91f0072b4e1466a96123ed6a04fde`  
		Last Modified: Tue, 12 Jul 2022 02:54:32 GMT  
		Size: 7.4 MB (7424030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980866729827122d1363e7eeff83efd6aaf40f570e59520d17f45f371606fd3a`  
		Last Modified: Tue, 12 Jul 2022 02:54:32 GMT  
		Size: 9.9 MB (9884925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
