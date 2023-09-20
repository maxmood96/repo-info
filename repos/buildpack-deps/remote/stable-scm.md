## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:5bab68eab396fd6754431f5be707477894220eb0ef354fb7d158f6f44c4414a6
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

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a148d40ef5b742273b7fac6a0c6122a6a70de491912d48a11facec8cccecb8a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a39286ce9a566833fd06188af6eb75e3e0c6d122e0d2bedc0f7498ded60e92`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:26 GMT
ADD file:ce04d6a354feaef93795269c859f36667fce9efda23c61b37d7060263b66ed4e in / 
# Wed, 20 Sep 2023 04:55:26 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:20:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:debce5f9f3a9709885f7f2ad3cf41f036a3b57b406b27ba3a883928315787042`  
		Last Modified: Wed, 20 Sep 2023 09:30:18 GMT  
		Size: 64.1 MB (64112257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4a34e9cab15ab0b321852c10d6901afb10100af38bc42ddfa5cc8a2cddde218e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131678961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830018fa70a7de947e7d2d8ad6bdcb73626c6195a8a5a09684e2e54144ef24f8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:49:41 GMT
ADD file:4c262e2fcc04b6144cc529b2b0dbd984b5f44ecf09bd87707631cb5cad3012f0 in / 
# Wed, 20 Sep 2023 00:49:42 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:55:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1a754c9ac0c66ea612dd3e7313134a3f8bbc17850295990e81eb1848b34eabf4`  
		Last Modified: Wed, 20 Sep 2023 10:05:22 GMT  
		Size: 61.6 MB (61554233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c4e5e365fc554650d612190a00de626c2132abe316e2558217051315389d4c58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126431822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d6adf4a3a321ed069d39b4cd8753d97c42c0009604bb1c3a4334dd46996959`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:08 GMT
ADD file:e8c98b19a39772b96a8bfa0f38abfc620498f040012f9b9906640975ac01ce0d in / 
# Wed, 20 Sep 2023 04:57:09 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:24:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:4ecb66b8eee4d1eb823c09a41799c3f25f6ef9f31c3ef273c3b37419d8c39606`  
		Last Modified: Wed, 20 Sep 2023 15:35:36 GMT  
		Size: 59.3 MB (59262478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fcf2f43e370b5fb288290542ea5929b8a7cfaf340bedab92393d95c957ad8020
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137150035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210de9ceec6e7ec97a1ca02ff6f04942900cc0b3be82787f370bc540f2767f4b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:04 GMT
ADD file:7a0adbde6e967e2bcaafa69f04fabdec993025645c8d0d51acc991a31b404eed in / 
# Wed, 20 Sep 2023 02:44:05 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:23:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:23:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7d8d278f2f731ceff5e8c6f5010bef6b1bf18c555a80663ca612e3e42d013779`  
		Last Modified: Wed, 20 Sep 2023 09:32:29 GMT  
		Size: 64.0 MB (63988033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:12718683e9c885ddb0f9824ec1becff7f0477bebffa2b770de34fb1d3aab97c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141411167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdb30780ca90222c0c1a753eea63979c9b34a7a8a1d9ad032d6325c4e15cec5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:41:42 GMT
ADD file:23c52eb6ca90f95eb3fff17deef5cfb900f1807fd50deae367183075f49aa81d in / 
# Wed, 20 Sep 2023 00:41:45 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 11:25:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 11:25:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:bd965fff65d218c5dd30176fa6be9fe57accd5e588e2173f509ea58bf7d44ab8`  
		Last Modified: Wed, 20 Sep 2023 11:37:22 GMT  
		Size: 66.0 MB (65972489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:de5081c2d454bdb1fa06b9556e8cce7df5374926111acb4bd898ac1ba10cdb07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136105746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188e57c8f4f8bcd48a8be5bfcb254bab5808397e28785ebd5086df1dc0deb57f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 03:09:14 GMT
ADD file:fcce6589274e33563988a8b5cf9be10cd70df7b83bdf6713a5162f272a6c801f in / 
# Wed, 20 Sep 2023 03:09:19 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 21:45:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 21:47:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:270da23f34a3d46cf64368c2f1574be74de69879d2f3d04ce465cae23dee66f7`  
		Last Modified: Wed, 20 Sep 2023 22:21:28 GMT  
		Size: 63.0 MB (62950631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:668a75d912b21308d01ce2ffb2469c0bd519e772ea8d92a39ef2315dc58af8c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148796016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21542760a9ecba8d607f8d5bac2aa84d7e4c729a39f21ff465983dd5550491b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 07:52:31 GMT
ADD file:dc6a80175c6d467f50c4ff816701171cd27bd98fc9bb7292161e476ada0cfed1 in / 
# Wed, 20 Sep 2023 07:52:34 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:47:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e7a962ae127ab04dc4b0c1dc7a9f6ce9d0f64cb5981c0e114caaec07fd9c8c5e`  
		Last Modified: Wed, 20 Sep 2023 10:20:59 GMT  
		Size: 69.6 MB (69570258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fb8ba9fc338866b6ac9dc21b1d839f00f1524a71ffce0785df00c012e57f32f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135063829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915f9d73e58e710af784955c3983d5209257cea3c253cf6ee52200eb252ad3a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:09 GMT
ADD file:988f82e85974ad63522cfbd8ca56dddd8dd9825ed628600e9a5037d77d1bd890 in / 
# Wed, 20 Sep 2023 02:54:12 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:49:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9b068b7dafac8638b610a6cb2e2a91a3aa7ca68a443fa93992af5f0fe704f55a`  
		Last Modified: Wed, 20 Sep 2023 09:58:48 GMT  
		Size: 63.1 MB (63113324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
