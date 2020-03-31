## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:4e0ae09e3fecd7539fd90f17ec71b4cf0e60e7c14b67beec1bec7f229f3343fc
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9fe01d3c96732b7a430aff1337ff4a0bcae707d7b5656798e296706bacc200ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124948292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13f8b600931556bb7c0104446dea63955c6d29c11404531711c47d98c9e3263`
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
# Wed, 26 Feb 2020 01:04:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:74a471741589e2b8271d8be85e5a2d0ba4eb2667b7207711b99787dc20fa3eb6`  
		Last Modified: Wed, 26 Feb 2020 01:19:37 GMT  
		Size: 54.9 MB (54915618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f29e79c81253858970fbda7a0e9add80034c6cfd062c9bf81d48fb2e16b0ac40
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119929632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0831f7f405f6df21d084531edf4ca391b13b0c907715fb18cf6259ae83ee242d`
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
# Wed, 26 Feb 2020 03:32:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:aba36494b890743c5415594ee83949a59b8e97262545880ca23c5428e07c583d`  
		Last Modified: Wed, 26 Feb 2020 03:59:28 GMT  
		Size: 52.6 MB (52597859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:90b6c33f5b3737f79f36d227073b2a78f7fdd49e947845bd3f6b4ba7c04601c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114789632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cca46f3ba333c128d86d9afde8ce628cae2e4cc0e011a9e135fc382c86a36c`
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
# Wed, 26 Feb 2020 02:08:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2db97fc91eb5d6d855e20ee37328160b266216205b0e2f0b9dbcefbb09c48b38`  
		Last Modified: Wed, 26 Feb 2020 02:32:24 GMT  
		Size: 50.3 MB (50332192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:24983c0a5ebb8379372492474099903eb62fba3a173fc6448daa38600366dcb8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123983454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba51b4b050059cc797014e2c136735bc5c32be10ef7a2eb2e8b7b49a8967c4b1`
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
# Wed, 26 Feb 2020 03:46:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a934273fe78141239ebcd7f15bd23d865d400ab5e8f9a91732fa22672bd4308d`  
		Last Modified: Wed, 26 Feb 2020 04:04:23 GMT  
		Size: 55.1 MB (55124898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c1db16337c66921df78a06bd3de413d91e7878cac727f1fe38eec0980c35cadc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129663892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0163ece584e91810a2856ff51bc98b406a1354b02036c4a8df4f5d094388f7`
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
# Tue, 31 Mar 2020 01:09:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e9e841cf9c625cfcbef38746fbb539d5caa4a613cdd12452b81811f57855f5f0`  
		Last Modified: Tue, 31 Mar 2020 01:28:03 GMT  
		Size: 57.2 MB (57166927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:57c84dd915a15f64973c9fd8f9f72f647ef7f03ce3d26f6d11b3c0805568552b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135237623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f919f0095039e2b687254c2118d96122e857e817f4efe34ea6dee4ebfc59e82`
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
# Wed, 26 Feb 2020 07:49:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:30f222495a1389fd4823cb320f7ee7ffbed38c52e80ad92cbba21081ebd6eb48`  
		Last Modified: Wed, 26 Feb 2020 08:46:28 GMT  
		Size: 60.3 MB (60250770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ebfbf15658b6e5ca23285622f7814015ab03f074ff850f5afee383b924cde2fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122412774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762051c3d27080269636615418f1fe101420fd76e33f63fbd10663925a4d3395`
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
# Wed, 26 Feb 2020 04:29:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:ead6ac3ccef377efbacc9ede45b74a41a368b1019a368d9965582272da21fda1`  
		Last Modified: Wed, 26 Feb 2020 04:46:40 GMT  
		Size: 54.2 MB (54185840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
