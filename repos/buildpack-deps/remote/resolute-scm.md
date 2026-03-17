## `buildpack-deps:resolute-scm`

```console
$ docker pull buildpack-deps@sha256:3906cb5b2a7047d879eec84a62a88585f8126828f86c8ae5b8d36eed66072c47
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

### `buildpack-deps:resolute-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:01824a8a350fd044def0451eca86cb043d28fc5b8ec74e56e5911ce724633f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111195297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2eea68c0e5e347450a9803879e77fee6208ec8412f8b187a1e16e82450b0e6c`
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
# Tue, 17 Mar 2026 02:32:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:27ea5ea9e1677e25f72e17f23b3742d51b399b02ec77158e93f5817df2e1af9e`  
		Last Modified: Tue, 17 Mar 2026 02:33:17 GMT  
		Size: 49.8 MB (49815129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:acb0a683290f34b00c90608427292d4957403d6fe78d286ef815489d4458b109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d456fe1a23cf53a0b0ad1a76fd5f23ee7b7047171bec6f3ec77985d5b44ebba6`

```dockerfile
```

-	Layers:
	-	`sha256:66b7bc29f0f5df98326c6ee3eb970183fbc1b682ff842a3295d21874829bbaf5`  
		Last Modified: Tue, 17 Mar 2026 02:33:16 GMT  
		Size: 7.1 MB (7071599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca3d8c4abe21d878d08ae57aba325e4e65a1af117baed1b45add7fbce5f7e9a`  
		Last Modified: Tue, 17 Mar 2026 02:33:15 GMT  
		Size: 7.6 KB (7589 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:86c25ef0f013366358a7aafd21a6baf28dc87cd47ab4dc8bbdb8525ebec34977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109340894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8565c5ead617d6aaea0cc9468281ee8a6b4dcf39fb77bc2895445e5e1a27a4`
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
# Tue, 17 Mar 2026 02:18:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:bb2221f0541d0205e31ad9ab60b2a6ac6aa1f3da89bb4e37272bb559417fe200`  
		Last Modified: Tue, 17 Mar 2026 02:18:20 GMT  
		Size: 52.7 MB (52667351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c505fb4ef5828133f978e59930cc43b3adce5d884d51aa12b246aa95e37adcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac793a2577003e97f0a05d8a4dc54675f5ae11b0315031e27c33fc549bdae162`

```dockerfile
```

-	Layers:
	-	`sha256:8009eb34ac86bbd73acde894a48aa5698794c23ee3cd23ca6646eba787fafd62`  
		Last Modified: Tue, 17 Mar 2026 02:18:18 GMT  
		Size: 7.1 MB (7072128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdd01b3fe27dd2e04c8ac40e9bedd4a3589ef56d853353ec2c7fadbbcb1944f`  
		Last Modified: Tue, 17 Mar 2026 02:18:18 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:09f04cb9ef21dfec4f32658df36b3d567f210188b501738a8d31d468c116fd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109546741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2e1db2ab618bbd13e2bde230c310f5454e189c4d33e1884a2dab45304c1dc8`
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
# Tue, 17 Mar 2026 02:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:89e1c90ba0c3c664a710cc7747df3a96a7104aa5b4813f95fe43c425108431bb`  
		Last Modified: Tue, 17 Mar 2026 02:37:30 GMT  
		Size: 49.4 MB (49419901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:302a35bf8a689c365440c79ee972896b399eed02cb67555b776a2bf1f328f979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7085665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0f0050c235fd0c4a91bb08bda5a8d62026a37597b18840f59d33694cded062`

```dockerfile
```

-	Layers:
	-	`sha256:fef084b57f9414b27abae8d9b943419192d9ce75ae54c8355c64378eca6dc38d`  
		Last Modified: Tue, 17 Mar 2026 02:37:29 GMT  
		Size: 7.1 MB (7077997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af88e73844c620110e7efa45703526c67e2802b4b3006cf5110b978ee89e7d6`  
		Last Modified: Tue, 17 Mar 2026 02:37:29 GMT  
		Size: 7.7 KB (7668 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8bb4557b9a65cf9ca9a99ff49703d7aa5eb782ad655027d0174ffb57440e17f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121075020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1907837dea6f2c5d4764ac2d4be27b19a2d0d6e0283f8885a845024c8b3df285`
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
# Tue, 17 Feb 2026 21:45:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:daf98c8b2a343a74d54a62e9cc6362df8445c47cce3a012b806527aa4d9383c2`  
		Last Modified: Tue, 17 Feb 2026 21:46:52 GMT  
		Size: 53.9 MB (53945243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bbd3ad66889300fe0a7335160443a4c7cb0dd2b7885d4cdb6702d12a72db6bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7007834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414db67b44f7ec372b0f3fdeca3af6d80261d0ca5bb47e4cd2591af8d511cfca`

```dockerfile
```

-	Layers:
	-	`sha256:bb1356b8ec059d929962d1833456f948d158fba45e0cd838d68e6dc19d808481`  
		Last Modified: Tue, 17 Feb 2026 21:46:51 GMT  
		Size: 7.0 MB (7000521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0055df7f324baec24b62d22d1b1227294ecfa38f15f79420a225ec8cb13e416c`  
		Last Modified: Tue, 17 Feb 2026 21:46:50 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4627a4f3cc3e705c1775d5ea0b04e9807009e7e70543027a15d583ae59a5f48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112524488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6511182c3f8f5efe208ab499db5c46129f312e47393c9cd55dd346161c517827`
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
# Tue, 17 Mar 2026 03:21:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:d102bb2d97db4e0299f1265fe08feab0c7fe7f373e1d4106b25caeb53b38c037`  
		Last Modified: Tue, 17 Mar 2026 03:22:58 GMT  
		Size: 51.0 MB (51032278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9e3a7d06cf59d4fde1bc935c152fd7efa97a3d0b530f1aabe4dbb0d6d83a11b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7080715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa75a77d9ddea0cde9e65cc327ee95a8c3ac54cd52aba1c6b642d459d88de57`

```dockerfile
```

-	Layers:
	-	`sha256:a943aebdf20463a00041b701a5787f33f13800a8f78f20025641117dface560d`  
		Last Modified: Tue, 17 Mar 2026 03:22:56 GMT  
		Size: 7.1 MB (7073126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbb6dcdeefe6376ba9d94b3fb7a873d14dc8c24fa09886e8092cc5386c7d837`  
		Last Modified: Tue, 17 Mar 2026 03:22:54 GMT  
		Size: 7.6 KB (7589 bytes)  
		MIME: application/vnd.in-toto+json
