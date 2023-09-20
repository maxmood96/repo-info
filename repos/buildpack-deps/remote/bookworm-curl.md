## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:af25c1b6b6870bae8626e33224d3ef239105791eae75268e5d4444ab6f42306b
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1a8917f16277c64dfa704e09cfa5a02fddee367f8b3247028aac318d45e068f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73588123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1ca6b40d07afd7c7b58497c8b8f12477ec3e19366c6303faffee2d64770386`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:26 GMT
ADD file:ce04d6a354feaef93795269c859f36667fce9efda23c61b37d7060263b66ed4e in / 
# Wed, 20 Sep 2023 04:55:26 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:20:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:167b8a53ca4504bc6aa3182e336fa96f4ef76875d158c1933d3e2fa19c57e0c3`  
		Last Modified: Wed, 20 Sep 2023 04:59:55 GMT  
		Size: 49.6 MB (49557601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47a222d28fa95680198398973d0a29b82a968f03e7ef361cc8ded562e4d84a3`  
		Last Modified: Wed, 20 Sep 2023 09:29:57 GMT  
		Size: 24.0 MB (24030522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8df275efbef876ddcdb39bd4f85a78db3214e40e9b8db0798eb7f0a967a03ab3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70124728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2596d69701037a80c19c9550ff3014a25515deb44b08eebbacedc76cde00dfa3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:41 GMT
ADD file:4c262e2fcc04b6144cc529b2b0dbd984b5f44ecf09bd87707631cb5cad3012f0 in / 
# Wed, 20 Sep 2023 00:49:42 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2e728ebba2eb6503d5975d2d8245f959ffad36ab8a83164e1c7e45956c36080`  
		Last Modified: Wed, 20 Sep 2023 00:54:16 GMT  
		Size: 47.4 MB (47415014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19620991f32e48616e52febc5b55b219fc0e07a38ce2edc871e4e75601582812`  
		Last Modified: Wed, 20 Sep 2023 10:04:59 GMT  
		Size: 22.7 MB (22709714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c3ddc64df8c21d3fb2748edf03317b766013e8ab6899ffc524c31f8520368842
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67169344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b17ea1bed8110b429c3d269d81f242db151e1dda3c2343af98f58a0f40ef074`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:08 GMT
ADD file:e8c98b19a39772b96a8bfa0f38abfc620498f040012f9b9906640975ac01ce0d in / 
# Wed, 20 Sep 2023 04:57:09 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:24:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:013e3017888216ce95d0ffe3d0fb039c509402dc99800465157f56e7520abd4a`  
		Last Modified: Wed, 20 Sep 2023 05:00:53 GMT  
		Size: 45.2 MB (45232576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b45aaa3d8d542a2281410c108a016f367f050793bb029d35cca677cc0d500f1`  
		Last Modified: Wed, 20 Sep 2023 15:35:12 GMT  
		Size: 21.9 MB (21936768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:602454c1fca9ed0b77c98b3c8fb9ee158eb3646f494d5e193950813c18926b49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73162002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8457b965dd7f69de623ece2cc23ce8ebcf3a50486b27ded4bb51aa8cce5be8f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:04 GMT
ADD file:7a0adbde6e967e2bcaafa69f04fabdec993025645c8d0d51acc991a31b404eed in / 
# Wed, 20 Sep 2023 02:44:05 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:23:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:796cc43785ac3cd0081892bd48e545a0615415265b60c794fdf81ac95b034213`  
		Last Modified: Wed, 20 Sep 2023 02:47:15 GMT  
		Size: 49.6 MB (49591881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91290b4a059080b4227746016e1a8f32a290271d8712b213834e9296a38bfea9`  
		Last Modified: Wed, 20 Sep 2023 09:32:11 GMT  
		Size: 23.6 MB (23570121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5711bab7117d9b11653ffd41700a82bbdaff91eddd5b8d09b29ff518fc2bb9ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75438678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c912a8c4a4d344c2d4a7dbcedfcf953f1efb09f06da1285417a30874dd78d34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:41:42 GMT
ADD file:23c52eb6ca90f95eb3fff17deef5cfb900f1807fd50deae367183075f49aa81d in / 
# Wed, 20 Sep 2023 00:41:45 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 11:25:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b3de420baafed4c606a756da9f1ab4e930a007eb8cb0a1104bc280c0b7820cbf`  
		Last Modified: Wed, 20 Sep 2023 00:46:20 GMT  
		Size: 50.6 MB (50568965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4c8b4e1e9e09c6062a8931a468a599c126b11dde5f26fc56c31c3de3f4cf68`  
		Last Modified: Wed, 20 Sep 2023 11:36:56 GMT  
		Size: 24.9 MB (24869713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d96cb395b6341216f8a89c399308272f682513def8b5ebc63697f551a6749efa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73155115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e807ddaf321f495b4f2a1e09d753720cb9bd8f26eb43ea789e85c10e84967c09`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 03:09:14 GMT
ADD file:fcce6589274e33563988a8b5cf9be10cd70df7b83bdf6713a5162f272a6c801f in / 
# Wed, 20 Sep 2023 03:09:19 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 21:45:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d60e76f86e60c0c2ec7b83df437d97bc329aab62315d63446e73d0ccc6bed0b5`  
		Last Modified: Wed, 20 Sep 2023 03:20:16 GMT  
		Size: 49.5 MB (49542389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc2e2248e2cc36baf3ee5daf0facc6ebb4ffbfeacea598d0236469d9f6573b`  
		Last Modified: Wed, 20 Sep 2023 22:20:35 GMT  
		Size: 23.6 MB (23612726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9037d6abf8a180cb4e09dc36a216a5702c624481ab30afd88854e4a46d9eb583
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79225758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663a62d11088af0fd3ce3545c3b4940ae0db41bf58bf0dedc583f12a9f2ca30e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 07:52:31 GMT
ADD file:dc6a80175c6d467f50c4ff816701171cd27bd98fc9bb7292161e476ada0cfed1 in / 
# Wed, 20 Sep 2023 07:52:34 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dacd41a2ee8a7a272473dd20943e3e5c0ddac0964f5610239dd5ae6c807c000c`  
		Last Modified: Wed, 20 Sep 2023 08:49:21 GMT  
		Size: 53.5 MB (53544796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ec766d4028b01ee907aa2c7c4460d2a3a7b6046a77e25177450d4c40b848a9`  
		Last Modified: Wed, 20 Sep 2023 10:20:30 GMT  
		Size: 25.7 MB (25680962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e0b46afe1490eb8ed178a84d64f063e2a833010bbe0ff910f3fa2d30aa941f08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71950505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055d01254528d2e2671db44893319d91ed7c86ead68da19959627560a8f3736c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:09 GMT
ADD file:988f82e85974ad63522cfbd8ca56dddd8dd9825ed628600e9a5037d77d1bd890 in / 
# Wed, 20 Sep 2023 02:54:12 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:49:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca5551f4914a3e8f0c34772f4d772442cbf259e6ee48db35d827776924e556bf`  
		Last Modified: Wed, 20 Sep 2023 02:59:30 GMT  
		Size: 47.9 MB (47921769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d1899ef7b4679dca64e2b81a7d1bc3c4b48e9813dc2fa8cae7a5106d1ce073`  
		Last Modified: Wed, 20 Sep 2023 09:58:27 GMT  
		Size: 24.0 MB (24028736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
