## `buildpack-deps:resolute-curl`

```console
$ docker pull buildpack-deps@sha256:0a3d0bc9cd41677d6e400eece4e0ec00798fd2f231e81e47532be71bc7d453f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:resolute-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:58a39579f3e92bfdd60b0ab2e2adf6a333ff477d4fdce9d65eb99c3b200ef2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61380168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15985955b2449cf1efd3f25c12577f7ba5f7971603140d9fc993347439a48e4a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Mar 2026 19:56:19 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.4403.tar --tag 26.04
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:56:20 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.control_data.4403.tar
# Tue, 17 Mar 2026 01:15:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:353172d2243ba412db836ee33433b5bf98b7b5e712d6a842def962f77707b920`  
		Last Modified: Thu, 12 Mar 2026 21:05:56 GMT  
		Size: 41.9 MB (41855369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b2f35783e4f17e635643c3b9a28f61d865c4853bbcc849e003c0ec3fe5f4a`  
		Last Modified: Thu, 12 Mar 2026 21:05:58 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475b6067e1c976b66998cdfd56bc20f210af1c6cbd552f2dd21127fa13f29a24`  
		Last Modified: Tue, 17 Mar 2026 01:15:36 GMT  
		Size: 19.5 MB (19524392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:06bd4f0bb4e772dfc9cf27c0f281e36f7ed2939838ab34a79a56a0e3b878a25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03cf6555d413448a9caa6d19c07a01d2326a6465289446845320584beed32a`

```dockerfile
```

-	Layers:
	-	`sha256:51ff27d0e4185eb1af73d6c3c342df34e476f5d963214db11e827cb67569000d`  
		Last Modified: Tue, 17 Mar 2026 01:15:36 GMT  
		Size: 4.2 MB (4199412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0396640c3180bbf79dd06da44b20032dbdd744d302712a3263b03fba3308e1d`  
		Last Modified: Tue, 17 Mar 2026 01:15:36 GMT  
		Size: 7.2 KB (7243 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2c5d9c8df5808a6f2de459823da24ca7d3227c19a23781c7b761669ccaa3b30d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56673543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7151dc428c4e0233d3b023495f4753c4bd5ea549e515cab5ba39cf1bb14685`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Mar 2026 19:59:15 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.4503.tar --tag 26.04
# Thu, 12 Mar 2026 19:59:15 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:15 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:16 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:16 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:16 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:16 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.control_data.4503.tar
# Tue, 17 Mar 2026 01:15:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f698dda2de4e496f317e4914f05ad776006c478a9d69939a895f32c14ceb6526`  
		Last Modified: Thu, 12 Mar 2026 21:06:26 GMT  
		Size: 38.9 MB (38857394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9654d2d19664354ab705e627dc9112e60cb09f957b1d848eaf15ccaf2cbca838`  
		Last Modified: Thu, 12 Mar 2026 21:06:29 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4b4821ddba9f62cd63e431042544efbaa19e2d5fd5f747ec179f809c5d2b2a`  
		Last Modified: Tue, 17 Mar 2026 01:15:28 GMT  
		Size: 17.8 MB (17815757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f33983c776981ea1f60155449bcb7f08760204fda19674f4ff2e03097ac521db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c459160a3051d685b3ecdbf51a54ad1f423d9fcbbd51412ea766acd835e82a18`

```dockerfile
```

-	Layers:
	-	`sha256:7c3a0d5f007bbdb494d8c52c62bf0f5d66661eb7194bf9ceb429e2d2c4aa50ef`  
		Last Modified: Tue, 17 Mar 2026 01:15:28 GMT  
		Size: 4.2 MB (4200914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe6fc78e6d7c14fb4a9c1aef747dcd813e93b8e19481862a714bcb21264d45f`  
		Last Modified: Tue, 17 Mar 2026 01:15:28 GMT  
		Size: 7.3 KB (7306 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:371ac4b3649a91bca10fa8fbdb5b43874fb8c7c54a1e5584c0acf30bd71b7cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60126840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48daf6cfc49f105e68b1acdb198d766a60d5a7e6c11444594a7aa377dc54c49d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Mar 2026 20:00:12 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.4694.tar --tag 26.04
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci config
# Thu, 12 Mar 2026 20:00:13 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.control_data.4694.tar
# Tue, 17 Mar 2026 01:15:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:deb605ffd5670438453f8cd18a0a75ac48b6f24bca27ba1a64802534315973b1`  
		Last Modified: Thu, 12 Mar 2026 21:06:05 GMT  
		Size: 41.1 MB (41064498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41816bff5f93f99104877eec3ccaca96ca2567a60b68cf2911937f97162d4a5`  
		Last Modified: Thu, 12 Mar 2026 21:06:08 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827eee8a5d03fb1b3cfadfdc7c60123e44bbefdea49f5e8ce8acad24e20454f7`  
		Last Modified: Tue, 17 Mar 2026 01:15:42 GMT  
		Size: 19.1 MB (19061953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9721a5bccfaa2bb981de963c207d0c2fd788b9aea6be6c457f73123408b3652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d67784de284bb2ca3e038e8c1616de992eecc7eabd5e28667b673a769c0c0b0`

```dockerfile
```

-	Layers:
	-	`sha256:930e43404134a82196a4bd1692c82522ed2097e8e8cc1a62ee6dec51e0c702da`  
		Last Modified: Tue, 17 Mar 2026 01:15:42 GMT  
		Size: 4.2 MB (4199670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6bf0988ddb2193d26debe082c19ec12d0576dbd97f9f5d9e8b5a986f4054ce2`  
		Last Modified: Tue, 17 Mar 2026 01:15:41 GMT  
		Size: 7.3 KB (7323 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9faaf8db70b50cabd8c2784e866f6d72f456a01dc61acde0319aaca67ecab010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67129777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1222c365691c8c86dab08fd44e082387cf26ce724528c4a07600f70b9f87d39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 21 Jan 2026 02:05:01 GMT
ARG RELEASE
# Wed, 21 Jan 2026 02:05:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 Jan 2026 02:05:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 Jan 2026 02:05:02 GMT
LABEL org.opencontainers.image.version=26.04
# Wed, 21 Jan 2026 02:05:05 GMT
ADD file:965035165b5a9607aa8c5bb045af27bc17ad5f8ba33ecbe10426988d7c087ecc in / 
# Wed, 21 Jan 2026 02:05:05 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:13:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b5ed12c0213034851f152051b56017b1e654738743050659fce37a1a1aabcb6e`  
		Last Modified: Wed, 21 Jan 2026 02:53:54 GMT  
		Size: 38.8 MB (38812135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218b035f88d928ca302b9ff3aa9991b0d88cdc1af3c26cf3a2e90174b06d0494`  
		Last Modified: Tue, 17 Feb 2026 20:13:43 GMT  
		Size: 28.3 MB (28317642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d164e471ca336239a8e5e03f40a0a427b2038b2fdd657c8fdc4f15d662ac8bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef491fd90ec92609fc35afb3f06395e86f8ef86ec5c6996a6110f7a95f7b69f`

```dockerfile
```

-	Layers:
	-	`sha256:4fdce5b4ce184287d4bd6dc900084df511290e39d1a35cc7da5befaaa0a7c76d`  
		Last Modified: Tue, 17 Feb 2026 20:13:42 GMT  
		Size: 4.2 MB (4189923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af1876ba8d325717746c8e693aaa94fc414b1dd401f8236df1abe2812664402`  
		Last Modified: Tue, 17 Feb 2026 20:13:42 GMT  
		Size: 7.0 KB (6967 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:81efae9cac546872c67201760bee45253c2856afc55a437e0933da1c448bb098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61492210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f172c14bb69fd5592496556638d19325a85c24fa03e1ff7175a4fd17e9f23a4c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Mar 2026 19:59:05 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.4449.tar --tag 26.04
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci config
# Thu, 12 Mar 2026 19:59:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-76cf8b7096278e896cac0fa322ab7d79/images/.temp_layer.control_data.4449.tar
# Tue, 17 Mar 2026 02:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bdefaca172ef708c1d64fdd846fca9c7c20ba96b3ea558c846a6e034985975be`  
		Last Modified: Thu, 12 Mar 2026 21:06:45 GMT  
		Size: 41.5 MB (41489128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99e8c75de62bbc8eb709650e730f26447a7ec4a999f02969cba49315e474a97`  
		Last Modified: Thu, 12 Mar 2026 21:06:48 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91370cb2ea39bc50fdd0bcb30ce054d63afb19753b5a1e066f3a7328b088066c`  
		Last Modified: Tue, 17 Mar 2026 02:20:19 GMT  
		Size: 20.0 MB (20002693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7360751aa91d9b58548009f079b81787e2cedf82f0028188a8abc7d9ade42cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c6c61b625bf471c20a0bbc8b4b7aac6126405f2f8180758c3014aa6d71f58e`

```dockerfile
```

-	Layers:
	-	`sha256:ba994a58b32cc5d0b237193429350c5c6ab46223b75e44f45ba0650eda5ff099`  
		Last Modified: Tue, 17 Mar 2026 02:20:19 GMT  
		Size: 4.2 MB (4201443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24cb368adbefda7c2cf1ab4d39fecf71e2cdf6f4041f2ba730c5b522ead1a890`  
		Last Modified: Tue, 17 Mar 2026 02:20:19 GMT  
		Size: 7.2 KB (7243 bytes)  
		MIME: application/vnd.in-toto+json
