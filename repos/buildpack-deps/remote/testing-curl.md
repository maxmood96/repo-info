## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:24dac90f6f62f3f9b26c6b7fe279ceb87eaa555538007a5e7d17a516bd69880e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7543fd116b1e842b1385c55b49a5b46db75fcf71901d0c85381d6d0897d7425d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70032674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1a6ddba16e1853e1bb2855a82b3232567dc60d5122a699010bcfa9421e4b2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:36:28 GMT
ADD file:7d01effeba890adb1756ba0a76c42c1dde5a189003943fbf4cb9fae0c0e1a046 in / 
# Wed, 26 Feb 2020 00:36:28 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:04:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:04:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7a4501da464e996edc2ef85325afe9881a58061a9a35b142ca7f0ba598553e49`  
		Last Modified: Wed, 26 Feb 2020 00:43:35 GMT  
		Size: 51.9 MB (51852739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00055416d483b70a8fceb7d6e7685e08d5c76fd449df312352288b650f0a5f83`  
		Last Modified: Wed, 26 Feb 2020 01:19:20 GMT  
		Size: 7.9 MB (7921881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61eab3db52671a6130df45784942f13ea891360cc3cd5d39ad4208321078246c`  
		Last Modified: Wed, 26 Feb 2020 01:19:21 GMT  
		Size: 10.3 MB (10258054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d4b17f48c0c86359bc0e5b633ba19d6d4a3d2a35d68914a0158a8ec42e23112d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67331773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b631d46ff159e165daa0b3d743276c9e329adddfb8dac73716f01767e718adb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:46:25 GMT
ADD file:cd3f4cae9b31b83faef159941db546ad620281a9de9ad8b4c2e2230e329f629c in / 
# Wed, 26 Feb 2020 00:46:29 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:30:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:30:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b5f1b944f6f81b9832613484a0ab69b94fc4d7e69cec7cf9246276a84f198955`  
		Last Modified: Wed, 26 Feb 2020 00:58:09 GMT  
		Size: 49.9 MB (49859431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309dee70eab6e2c15144731cd3a34dc25e8045f43ccebd56bca46a938673eb9`  
		Last Modified: Wed, 26 Feb 2020 03:59:01 GMT  
		Size: 7.5 MB (7497952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebfbc2424c96e6f6b0bd4ccb126243789b984e1df82dfcc07372cbdd3c2ec46`  
		Last Modified: Wed, 26 Feb 2020 03:59:03 GMT  
		Size: 10.0 MB (9974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:93c2925c6cb8f7c58c2447f4684704fe094d27549ea7d975e0e1c425abcbc71e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64457440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d7acc7a1ac76cda28e524da9f79d3997a211f2a4e2811a15c44e5399766435`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:49:40 GMT
ADD file:516c2d0189c8132f97d954209787ec2c833e16a9d8a4056cc9ed22510c721b48 in / 
# Wed, 26 Feb 2020 00:49:43 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:07:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:07:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d46b4a12bd08cdd498cc190f7d350b7bfa151e105942f36a185990c238f53695`  
		Last Modified: Wed, 26 Feb 2020 01:06:24 GMT  
		Size: 47.6 MB (47581289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab620fe7c5ae5218251dd6127456072d85bebc5b47b3359937f36ce071d355df`  
		Last Modified: Wed, 26 Feb 2020 02:32:01 GMT  
		Size: 7.2 MB (7237740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba007f6e72abf7b8df1b3d1009db9b497e33953f02bd91c28566d6700b3e462`  
		Last Modified: Wed, 26 Feb 2020 02:32:01 GMT  
		Size: 9.6 MB (9638411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe352cabca4e55106c8d709e1c51dd2d81c826d00ab4ce1d36e8e311431668e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68858556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5744862282ca211f3e8d579b1e179b9eaeca0f103f3d93d752f7d763b7858711`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:45:20 GMT
ADD file:6771f02669c2a4d080cd86fa10f39851d26351e4a29f9ff3d63a76e1865f96ad in / 
# Wed, 26 Feb 2020 00:45:22 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:45:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:45:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f822750796cfd016baf6c8125f67a171683174c26da351c46b78a6cc9d234372`  
		Last Modified: Wed, 26 Feb 2020 00:55:10 GMT  
		Size: 50.8 MB (50808549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f2d34813aa8b1aea79c2e14a664c47e0950cb8413f1af463215020fbe6ad26`  
		Last Modified: Wed, 26 Feb 2020 04:03:59 GMT  
		Size: 7.8 MB (7797144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74820b1316f035b3f4e91222feb71d75980d5a8b243cd3ea1a4ef519acca4774`  
		Last Modified: Wed, 26 Feb 2020 04:04:00 GMT  
		Size: 10.3 MB (10252863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:de1471c713f1d5ae5408b31972d41e5e9202aaf5ac2e91a1c8d7a7a6d253ab69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72496965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d34d6313031595acccbf357525393006d8c2f1e6943370c64a6040ad966fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:38:46 GMT
ADD file:930e7a44cb4836bcd1f8f50505e46e4bf4fd398eaad8aaddac7c962b60ca7e44 in / 
# Tue, 31 Mar 2020 00:38:47 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:08:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:09:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3243f119e5f4c4b861f26f136c3e132ab2844145f46cb5d7b6cc9602b0086f3b`  
		Last Modified: Tue, 31 Mar 2020 00:44:42 GMT  
		Size: 53.1 MB (53061706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e2dd532613df680378f734636580b380c128d4698ca4b3fa4951dfe348eb9a`  
		Last Modified: Tue, 31 Mar 2020 01:27:42 GMT  
		Size: 8.1 MB (8100943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb8ef6d4279b94da7f069e17e431221e259d8eba9ab62fbab1fa2b13b383023`  
		Last Modified: Tue, 31 Mar 2020 01:27:42 GMT  
		Size: 11.3 MB (11334316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:689cf81c07f8daefa1bcc8040aed78a4a5441f0947fab031300d060086215fb7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74986853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a116ec8432551d31bbc1dee50a89056f0515c6e64f385f916eb6f6718087c467`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:27:16 GMT
ADD file:063d213502b9de933570a06d59fc9054327af22f028f43bf3dae3bb2337e65d3 in / 
# Wed, 26 Feb 2020 01:27:23 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 07:47:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 07:48:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:61866abd58bd3dfd0faa8b784006b357e3857249b9f14f991b94b177781a85f9`  
		Last Modified: Wed, 26 Feb 2020 01:45:39 GMT  
		Size: 55.7 MB (55696604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd4cf9557698766807ea94c033185ed83b6e04370a7816433b533ec6cb1e8c0`  
		Last Modified: Wed, 26 Feb 2020 08:45:46 GMT  
		Size: 8.4 MB (8354351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e797f591ebbce205ef19692c7c30651291d5798b87929267ac7cc8d78cefea8`  
		Last Modified: Wed, 26 Feb 2020 08:45:47 GMT  
		Size: 10.9 MB (10935898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:eeb0ea2da9ab9418cdd25d702caac0fb1917c418312f002f928898ecfeb4af86
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68226934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a234adf4918bc62e14e5df40692eba3d4e707a7c31976629f791058a04b55d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:50 GMT
ADD file:1f369094a028b147c0bd0497bf726fed9867b40f8ab4ff8cbca77817e313d055 in / 
# Wed, 26 Feb 2020 00:41:58 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:28:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 04:29:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d902b39656b1700fbfc6beb02acedb31fb8f4ec23e536097b114147f2c25b942`  
		Last Modified: Wed, 26 Feb 2020 00:47:01 GMT  
		Size: 50.5 MB (50483632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0078ba0f65846bcf9e36f2207f3d64df1ed914863973517ef84b39458409b3c`  
		Last Modified: Wed, 26 Feb 2020 04:46:20 GMT  
		Size: 7.6 MB (7595527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7948ad3e978e4bad0726f39f892ecdd078e0d511d71e61e9d003839250ac83`  
		Last Modified: Wed, 26 Feb 2020 04:46:20 GMT  
		Size: 10.1 MB (10147775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
