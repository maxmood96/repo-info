## `buildpack-deps:plucky-curl`

```console
$ docker pull buildpack-deps@sha256:0414c249db16baedc6ff095191542c1fe48d1a832f37793d3d4ac4ffba6d5535
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:plucky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a423b946710233a62a0176f95024d4f9bb4541c01fff0609fdf169c130d63d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49842036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738bb88282ce10a280545ac228eb9b1a01bc11207f94eed5053cd9a46a9a51b1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:980bb2d70ee1d803d3c9180ebef258c9795083efbff9e9b7eaab4ae2ea044632 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1b3c8f62d074f218ad1cd11a4c801f7d6b73b93db485e1c170d6182a19604852`  
		Last Modified: Tue, 15 Apr 2025 21:45:08 GMT  
		Size: 29.7 MB (29710720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f757c9c78154a5f72abeb34fccd9ae44a8f5af313fc815debcf1f79b961ceb3`  
		Last Modified: Thu, 17 Apr 2025 19:07:38 GMT  
		Size: 20.1 MB (20131316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:548276c5856b3f09a066a0ae879822d37118b57e2243931cb0850e20c59ea7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd274076eaf774a099e165edb78c3c671710591af13e0094cc1642997cf6dfc`

```dockerfile
```

-	Layers:
	-	`sha256:1d6dfa51b36c7a6d66de30d7a13929431aa69454036f7657e535fee25b20096a`  
		Last Modified: Thu, 17 Apr 2025 19:07:38 GMT  
		Size: 2.5 MB (2462111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635756723a7e234b5445c5a5c63fde606e11498b4ac57858b0468a379f6cf4d1`  
		Last Modified: Thu, 17 Apr 2025 19:07:38 GMT  
		Size: 7.0 KB (6968 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0230b9ec52f886cf6bf459dff3467605132505cd589fd8aaf4126ecca919dcdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44576456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35218943ff0f9d851ae72c89b8125e3fb28c028c9a1b0959918ce45f4a57555d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:fb0f94fccc5217831c9326a88f9d43753e6977b91ade49b0b852f1e4ef22ea73 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:86d463765a1ef9e0563fb0c3823561d371da6b7f687151958aeb7efcbc80addb`  
		Last Modified: Tue, 15 Apr 2025 21:45:21 GMT  
		Size: 26.7 MB (26733303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab87d6883b32267ffea1009a181926e75ec6cf0ff7b79cffc076fa4735dc92d`  
		Last Modified: Thu, 17 Apr 2025 19:08:00 GMT  
		Size: 17.8 MB (17843153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:30b253c117b71d0f220a27e0f12bec8b8c3b826388c75d227b191db50a53d93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0335fcbe6a155a0f6312e15affbbe55e755bbd2ddf3c621d174197e5ea84052f`

```dockerfile
```

-	Layers:
	-	`sha256:09f2476e1535d9906e6a3f4b6c5798021b2828c7a50a18bed200b81836e923f9`  
		Last Modified: Thu, 17 Apr 2025 19:07:59 GMT  
		Size: 2.5 MB (2463610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:855a05671d48d1ab00854e19eec200392817251bbce31a8e9c38b37dfbf6c68b`  
		Last Modified: Thu, 17 Apr 2025 19:07:59 GMT  
		Size: 7.0 KB (7028 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1523ae8028a23301fc46fb10f700059de418a45d1d6a4035ad6535c9a9727930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47391385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fac5ef991cd00755d8244bcfb6035b17e0592625009c5d6c3a5cc62217c26e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:569b1b24c0a1612eb4d548884c87952b053cad17ead534d91b34f74bf31bd2e3 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36dff27e34eb6a337ae036fbb86e7b073ae0e8f1dc5d7e705423c419a175f092`  
		Last Modified: Tue, 15 Apr 2025 21:45:15 GMT  
		Size: 28.3 MB (28261176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86243b610edc9d6c1e787d92fd82404a07dc7df1137da6257f05b9a0e0e6b99`  
		Last Modified: Thu, 17 Apr 2025 19:08:33 GMT  
		Size: 19.1 MB (19130209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa1fef6d5d8575c6e1ea0a8bfeacde2015c2e6d22cb74c7a3f4821bdd47346dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d467501a547243f65788640df0f1cfac6974cbb998f97568ca1da4dfeef5f6b7`

```dockerfile
```

-	Layers:
	-	`sha256:aff674cdd833d9fb92047335371327508af6c1a5fab660d15d7a3ea599a4cca2`  
		Last Modified: Thu, 17 Apr 2025 19:08:33 GMT  
		Size: 2.5 MB (2462368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99ea963e5a71e5d5c329a7269cb2645ba085618319211e6046f1be1816e6a93c`  
		Last Modified: Thu, 17 Apr 2025 19:08:32 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:755f931baf8bdccc7ec9d764db8d910d7557de74361fe1a0a65ad820a5180c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54471030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac76656a91a863da45f0a16c2070e0dee2589e5ff82951c127b10a81454e080`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:7beeb672215e04d6c96e9a0d60bbea564ba541da31facc36a320d045fdcef6d2 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2731a3c5c15f5006b875bcf4a527fb9cc63904021559cd358c160c91018fe816`  
		Last Modified: Tue, 15 Apr 2025 21:45:28 GMT  
		Size: 32.9 MB (32912546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2beb87237962b8380a9e374cf35ac02c42ab0b99ccf115150e657e391e2bb0`  
		Last Modified: Thu, 17 Apr 2025 19:08:48 GMT  
		Size: 21.6 MB (21558484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ed6dcafe3af913998482846bbc3b751660a953ea455a5ea4eaef8a6d4c80422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb300144b6a0bc49de43b75d392ba75717a666775bb5862efaf0b2853503afde`

```dockerfile
```

-	Layers:
	-	`sha256:1cddd938b207e8bdfb6ae732fdba71bd76b3277128e7d151135518ff01d46423`  
		Last Modified: Thu, 17 Apr 2025 19:08:47 GMT  
		Size: 2.5 MB (2465793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0adcccbac9efa139d5e48044a6725e1da6bdc1438115ff9fa7ba19b2f837b07`  
		Last Modified: Thu, 17 Apr 2025 19:08:46 GMT  
		Size: 7.0 KB (7000 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d8f2f360dbfaaef57c14976094ea8ae78d31ae8f245a48c94562d5d26621cf6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49578229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112e116d802d766d90ff09fdcf2bdf0bedd6e1c7e1349df43f00928a152411b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:3ed52cbbe2433c5dc12dbb7e732f2e889444782966bb4bca420af94f96515440 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df4fa7894ea6fec34e9613aa41ce12d39e86174106bbc5e006a59c24f83a40a8`  
		Last Modified: Tue, 15 Apr 2025 21:45:35 GMT  
		Size: 29.7 MB (29711418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a28ce9969a80966c4d110ac26c6b9b392674b7c0ac90ca28268a9e5904c34c`  
		Last Modified: Fri, 18 Apr 2025 00:10:23 GMT  
		Size: 19.9 MB (19866811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1e0b39498a023e04abf757bb4e087f36becd608cee0413718e245cd1bc4059b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed038adc8973e918108fb089437112ea31d7c73fab821aa1ff8e785e0ef1a7b`

```dockerfile
```

-	Layers:
	-	`sha256:1334f8001bbd58003d588a7255813614b08e9f46f0260b198fabbeaa5b0cb348`  
		Last Modified: Fri, 18 Apr 2025 00:10:20 GMT  
		Size: 2.5 MB (2455379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:005443d303ea8cbcc24e616d10518cecb436612df0ed59da94d59ca7f5f38b43`  
		Last Modified: Fri, 18 Apr 2025 00:10:20 GMT  
		Size: 7.0 KB (7000 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:88fb19719b5d029fee59ccde04774cb3ecbe3b7d67a2566f01e0d4db73b64abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50072586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619e41c64a38f06299880a024051464b9311bb69a25858052c43ce280d01f27a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:5ca4f47f61e345e345a04e385f59c0dbae96e3d9a3847eff9ec82735a92e05db in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ec0a0fdff98ebea942fb34978c3e1893fee1092e8d0044b8d82301576686072`  
		Last Modified: Tue, 15 Apr 2025 21:45:41 GMT  
		Size: 28.5 MB (28540061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3273adb8720fb64f547b9a6d1a7ffd6d1330c51daf6ed393cfa037b238d8de1d`  
		Last Modified: Thu, 17 Apr 2025 20:08:26 GMT  
		Size: 21.5 MB (21532525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c90b298a3ceb2fe249f183c00d9b01fcf0f638f137cbbe874baf25f5c1f5d6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da144f8ac0332e45edaea108fb333182e1910f578a285fbd174953675e284b43`

```dockerfile
```

-	Layers:
	-	`sha256:b9d8dd843236bfb646a77209097c6412b73200e0b6038deb6c68ec1119fc9dc9`  
		Last Modified: Thu, 17 Apr 2025 20:08:25 GMT  
		Size: 2.5 MB (2464139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c43f257e086d104f057123484cc63835c4ea1b2219e99c31384f9c5a7bec0545`  
		Last Modified: Thu, 17 Apr 2025 20:08:25 GMT  
		Size: 7.0 KB (6968 bytes)  
		MIME: application/vnd.in-toto+json
