## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:16a6d1ce738658a2031568e92a5601f2293809dddda1aea402bd11d38259d6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:00ddbaf7fe4f93a56291fcf922139bb90e3b8d9698650c3773522427da3c98cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120103440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db496ad03b64d15b0bdc2738edfd46dee072a87565600f8a423e3aa70575421`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:16 GMT
ADD file:c254898ceb4172f05cd40460f8d0b1ca2d39d5178bdddd4e794c7d3fc5a60a03 in / 
# Tue, 30 Mar 2021 21:49:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:03:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:004f1eed87df3f75f5e2a1a649fa7edd7f713d1300532fd0909bb39cd48437d7`  
		Last Modified: Tue, 30 Mar 2021 21:53:41 GMT  
		Size: 50.4 MB (50432842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6f1e8117dbb1c6a57603cb4f321a861a08105a81bcc6b01b0ec2b78c8523a5`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 7.8 MB (7832608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c2faf66abec3dce9f54d6722ff592fce6dd4fb58a0d0b72282936c6598a3b3`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 10.0 MB (9997208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234b70d0479d7f16d7ee8d04e4ffdacc57d7d14313faf59d332f18b2e9418743`  
		Last Modified: Tue, 30 Mar 2021 23:14:37 GMT  
		Size: 51.8 MB (51840782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:135e02907d8aa782eb58f05d571ad270117a56e69fd8eac21da2fe31535d913f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114786622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfbf74c6d665868dd23d3314e056076b74ad202a52aedc850c28c72b0b05203`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:44 GMT
ADD file:6faf9c88ecf5029b54207c4a7575a4afa74c06e6655ad84599d4139337866709 in / 
# Tue, 30 Mar 2021 21:50:45 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:47:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:48:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8df1bb0713d83752f3588df777df10475afe64f042cf61465992cf6074bf7bfc`  
		Last Modified: Tue, 30 Mar 2021 21:58:15 GMT  
		Size: 48.1 MB (48149101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd2fd7358baf32fba79f0cd737807891482dd2ef4c726a3b5ce0cc9a2769f5`  
		Last Modified: Wed, 31 Mar 2021 00:01:22 GMT  
		Size: 7.4 MB (7376451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf105079c9c0f9176755263bc667f2dfc33d84f5bf98bde9856d918802d2278`  
		Last Modified: Wed, 31 Mar 2021 00:01:22 GMT  
		Size: 9.7 MB (9687429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc4147608173616c34d4a051e7d7d4e6a1d41ba86d7e8afafdcea7ec57193d`  
		Last Modified: Wed, 31 Mar 2021 00:01:51 GMT  
		Size: 49.6 MB (49573641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:28aa821265012d76ac28ce5a144044cad28b994a2513b7d538a81f04e786fe28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109739881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791e73d4a5c76b7242084e63dba8f2abb7594750f01b5feecfaa479f60e3cd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:08 GMT
ADD file:bd48b3fec0eec547919c9e90c2055f1d879c78e4eb7d92598bf55c0f83c44836 in / 
# Tue, 30 Mar 2021 23:08:12 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:22:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:22:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 01:23:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bf0c5f21d801f530938b2464483aaad40947de697c29cedece44096ead1522c`  
		Last Modified: Tue, 30 Mar 2021 23:15:55 GMT  
		Size: 45.9 MB (45915428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec8c35c4e8e932b85e0233ff1c20dcdd8bc13a0238128bcfcde181c0b04b037`  
		Last Modified: Wed, 31 Mar 2021 01:36:36 GMT  
		Size: 7.1 MB (7123902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d88df2bbeddb232fbd4bf0ffd8efd62285f56f8eb6e2007c1a89ecfdc0f3ad`  
		Last Modified: Wed, 31 Mar 2021 01:36:36 GMT  
		Size: 9.3 MB (9343731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f670f49de9ae76f27610a984da50b932e5dc0d3fecb1935aea3c51a2714e828f`  
		Last Modified: Wed, 31 Mar 2021 01:37:03 GMT  
		Size: 47.4 MB (47356820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e57da7b516664297f88a055f0374261320f0b6054e456951f79f64481c25560a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119070349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53d818de131bcb0224a8735c12487c9f2f8a94a4491090b6a3ddc498e5a8916`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:46:50 GMT
ADD file:6a5cce92f1039ef2cb7ac6dd999c9f84289a9f6e1c0891d1edf791ea73b7e125 in / 
# Tue, 30 Mar 2021 21:46:53 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:15:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 00:15:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef28e7e77ecbd3b3b426832bc12e8f5e629959683767466e9bac149c3286e126`  
		Last Modified: Tue, 30 Mar 2021 21:54:03 GMT  
		Size: 49.2 MB (49225808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344d2d9a9cf41c137b0dbb41df255f95fb812a23771a10ee2ab5a8a5047c62c4`  
		Last Modified: Wed, 31 Mar 2021 00:29:59 GMT  
		Size: 7.7 MB (7694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299f3631f6b52be065a7342da0a46978d55cbd0d15c57fae22f4ca24efcc295a`  
		Last Modified: Wed, 31 Mar 2021 00:29:59 GMT  
		Size: 10.0 MB (9984391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba70c372ae296f23e908bf1e1ed9f4c0c81a8a6d7fc48c0e2db16035bb9b7a54`  
		Last Modified: Wed, 31 Mar 2021 00:30:24 GMT  
		Size: 52.2 MB (52165620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:df99a5f986d1afc355148187a1371ed32db480f4f7354f9df8c6e6e94b23a940
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122974482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c2de7dec7a97622fdaf4a58cc1e1b4ad57289575ae3d5e7f9e10f4e61e0dcc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:30 GMT
ADD file:a2981af3d3aa369b11e802f23b175abfdb0f7636cdeec3aed67488d7a1f28a19 in / 
# Tue, 30 Mar 2021 21:39:30 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:56:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:57:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a3a3dbaddd2d56d7418508211551c461f826d1cae349d39a355a1c22fe140b36`  
		Last Modified: Tue, 30 Mar 2021 21:46:05 GMT  
		Size: 51.2 MB (51198756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de970e2d41035ffe1a656cc3d1f8e17bc7b8539b23745405b8fccf25d10fd312`  
		Last Modified: Wed, 31 Mar 2021 00:08:00 GMT  
		Size: 8.0 MB (7997659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27a2cf0e2e609cc89ee5b623626f822424bdc818ac5eab541a7a7b158ef0c01`  
		Last Modified: Wed, 31 Mar 2021 00:08:00 GMT  
		Size: 10.3 MB (10340050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a5ef36d45f69154fe2b83a8e658d4f08c45428493e8e1cc74a8b03b3c4799`  
		Last Modified: Wed, 31 Mar 2021 00:08:31 GMT  
		Size: 53.4 MB (53438017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:879cc4a7c5c85cfcc2a155da1c5ae560c0e42f11507df05488065b198dbfd350
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117192933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f51bd00e64dcf8f440f695b3d2934a5cba1ecfa0a6749cd118fdb3e8b8f1aa3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:09:25 GMT
ADD file:80bc7c6935e37a30f99582a481ea9ab5b67120ce265a4d29963ea84dbc20e314 in / 
# Tue, 30 Mar 2021 22:09:25 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:11:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:12:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eafdc9ff229439b8b9998d865c33e726afd8b6dcef65b7d5f02b39c022d19a13`  
		Last Modified: Tue, 30 Mar 2021 22:15:37 GMT  
		Size: 49.1 MB (49081877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5895125ddf0fc95ea9b30c1869f31950905b89ad0e06af9ab022ff8a288e3059`  
		Last Modified: Tue, 30 Mar 2021 23:22:03 GMT  
		Size: 7.3 MB (7251232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf3955dcf92989b48c4dcc991612fad98cd9c1ce94e1bc4d6aefdef84d2a15b`  
		Last Modified: Tue, 30 Mar 2021 23:22:04 GMT  
		Size: 10.0 MB (10016345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2a8d35407cc21f77d27cfc4e124b989b953f8f604e862e24a8474df87192b0`  
		Last Modified: Tue, 30 Mar 2021 23:22:57 GMT  
		Size: 50.8 MB (50843479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8128a2733600e2d7a1b96e1a73fe0a55ec1cf7ce249f96ab2da98a3880b6a6c8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130636729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105b8d95b49d929eda550c4fa3c0ff522b9eff21ef51ece28066c4e8ecca6b91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:35:16 GMT
ADD file:74f62575b50eebcaed9b3ba5dc5831f946ac72e01a5b2c74bd28ae7b978dd255 in / 
# Tue, 30 Mar 2021 22:35:25 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:25:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 02:27:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 02:31:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:38c5dfa64be2090539ac26f739f111c457ae78ae6864ae0361c5355144c7936e`  
		Last Modified: Tue, 30 Mar 2021 22:42:08 GMT  
		Size: 54.2 MB (54179784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba1a4ccdf1bda9cf7f483e60e0934b4e30d67c6784672b23f2127046367c787`  
		Last Modified: Wed, 31 Mar 2021 03:26:29 GMT  
		Size: 8.3 MB (8271776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9327bab5d767fa86a8a5f40d035f76dd387470a6dd1dd5e07a8a42be42e753`  
		Last Modified: Wed, 31 Mar 2021 03:26:29 GMT  
		Size: 10.7 MB (10727812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fee58c9046288bf199d75b0f016a65a12906618da199b84e55864d8da3f4424`  
		Last Modified: Wed, 31 Mar 2021 03:26:57 GMT  
		Size: 57.5 MB (57457357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e45c826ee9540b05f702df44232f85b03b05d6e56fcf2f198d2d9a782415cacc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117663489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3433bb1cfc1700f2c7b24202672917e11479f53801fd348b523f1ecc0ed0f14f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:42:29 GMT
ADD file:79040b5dceaf577162ccacdf7ef9e018f89e7ae399d59b4f80b3860a0471177b in / 
# Tue, 30 Mar 2021 21:42:32 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:43:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 22:43:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dd4a1caade48d16285d95f8062825cc6952224e43c64222e0cdcf13bc87b44ee`  
		Last Modified: Tue, 30 Mar 2021 21:46:01 GMT  
		Size: 49.0 MB (49000451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e488b7badadfabcedd6ad7a531fa8681ffb922e9853deb7bb142c86c78fdd05b`  
		Last Modified: Tue, 30 Mar 2021 22:49:21 GMT  
		Size: 7.4 MB (7399948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab15bd749c981c81cfe3ea27b9a7aa17ecf7dc0ce0357b9fe7774d8006622fa`  
		Last Modified: Tue, 30 Mar 2021 22:49:21 GMT  
		Size: 9.9 MB (9883132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e972cd743ab6520beed6242099fac9a59889445dfb7a01e42ee1ced09ac0e5`  
		Last Modified: Tue, 30 Mar 2021 22:49:41 GMT  
		Size: 51.4 MB (51379958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
