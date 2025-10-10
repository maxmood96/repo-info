## `buildpack-deps:questing-scm`

```console
$ docker pull buildpack-deps@sha256:3fac5b0cc8a3a505dee5f6ef7512bfb4b36a087f6e1db6d769971fd15ad58c2e
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

### `buildpack-deps:questing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f596e91e2e486d85e2d50c1596913f45ffe5c26b89e9800ddbe9a139423463e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101663771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f264e44882a4a382430ec6e197af3d536d071dbb1924eb96fcd44e0357d78ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:7992b30df2d5e1a9868a357037fee7a935fb600c535045c3dae00a6d2da0ffea in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9b965cd3592863b7a60b38bfeed24007834fdaf4994cb2c642c14d872f7ba0d9`  
		Last Modified: Thu, 09 Oct 2025 21:06:04 GMT  
		Size: 34.5 MB (34453346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7576d1bb6bbc5cda3456d256501881b6fe33fdd86baf9d81e296b44b4629ac72`  
		Last Modified: Thu, 09 Oct 2025 21:09:12 GMT  
		Size: 18.9 MB (18935913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01b2a607449ed42f8af633598423c355d043948545b440f818a3041f97a9533`  
		Last Modified: Thu, 09 Oct 2025 22:13:55 GMT  
		Size: 48.3 MB (48274512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:12df38be14721eebfcf05ed832d425a00a3effbdb13f70b7bffac0ed96e330bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8815382df97716dfe27210cbe1e4fa18c48ef9e2dc8e526fb88a4843f570b7d`

```dockerfile
```

-	Layers:
	-	`sha256:24427ce82f9e652184ca23ea684b9fab3a73eac5724c1a5429336c0920b51aa8`  
		Last Modified: Thu, 09 Oct 2025 22:20:30 GMT  
		Size: 5.8 MB (5767963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444b7c77d794f1abf2954f660e819f0a4e878f851afbe096f242ca3ecae2bfa8`  
		Last Modified: Thu, 09 Oct 2025 22:20:32 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:07505d8017427e54d1183c6e55ac134050eb977347be8678d57d5287e06bb7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99714150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c6a19116d1a978593e889ed890784e0246914ac711ad7f577b9f9912d4667a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:8bbeb482f2b247bef1627efb419885c5e995c29ac97454dfbe51dfc4ecf549d2 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d9a0dc3298847c4f5e3ffc1427dcb99ebe4c8fbb1c040628256b603b41f715b`  
		Last Modified: Thu, 09 Oct 2025 21:05:13 GMT  
		Size: 31.8 MB (31837227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5789843bac3bfe60c050b74177d6bdef81818507b015abb59a7fdba7199764e2`  
		Last Modified: Thu, 09 Oct 2025 21:08:26 GMT  
		Size: 17.3 MB (17313855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002109b64c318f0cddb99550d76900ca955f79ff25683a2f5e00126fe7346c26`  
		Last Modified: Thu, 09 Oct 2025 21:18:06 GMT  
		Size: 50.6 MB (50563068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1b0b46d1db831b69ae604d38a5fb9edd81c5ddec72441f5a86644cf544273052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f4eb851b682a06043dc5caf6a8540d4fff8a1d270fa4ca04a38e11f4dd9b9f`

```dockerfile
```

-	Layers:
	-	`sha256:8c7342ef34e04c832a3d8c9a81a7882e147263c294d134bb8ee5ab8a6924a13e`  
		Last Modified: Thu, 09 Oct 2025 22:21:17 GMT  
		Size: 5.8 MB (5768462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783dd0fdf63814b6c2dc5a21216737751edb375697df3ec1ad11255fe06b39b1`  
		Last Modified: Thu, 09 Oct 2025 22:21:18 GMT  
		Size: 7.4 KB (7388 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:38fe24fd4e79b4b776b62863bf9eed41b4d54a15020bf0e487f1b482dc4b397f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100489270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e87152ee9a4bc6f2895d8cf7cc144c5f4e75c5cab8bdaef37401f298decd972`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:8ccca3821827ab9c5998bd942e103c70878335f75be5b71b28f3fbe104f6c658 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4d90657552ac1b6284508877841188af829f382e60eeb51a71e7aa12b4a521b8`  
		Last Modified: Thu, 09 Oct 2025 21:05:33 GMT  
		Size: 34.1 MB (34071074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae8e65d481c24454a1936d3603010aecc1bac389df893175bccd3d0809a7506`  
		Last Modified: Thu, 09 Oct 2025 21:09:35 GMT  
		Size: 18.5 MB (18494427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f27663259df5fc48d274b5c5cee2aa50d96334d72713156abc98f7fd8d3b81`  
		Last Modified: Thu, 09 Oct 2025 21:32:26 GMT  
		Size: 47.9 MB (47923769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4627f814e402a37ca6d593669a69a840c3f89c382356cc02048cce0355af2478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97346f1ec6717886051a3d7baff139f1d2ccbf081a3287c3f01de9a5ab4f42b1`

```dockerfile
```

-	Layers:
	-	`sha256:a075d38724a92ed4df86d94bf553baa177b38d25141408ef10f2862550e822fb`  
		Last Modified: Thu, 09 Oct 2025 21:32:16 GMT  
		Size: 5.8 MB (5774351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61914d7a7d794834afa09b4fa2ebff2eaf99afef9c7edbbba8c6b2f338fda07f`  
		Last Modified: Thu, 09 Oct 2025 22:23:20 GMT  
		Size: 7.4 KB (7403 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:36ed26377ab61c5982364d0bca0809aea2a03f809ed0d941995769b1aea387dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109004490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199a2f969ed03c26d747046acc08d36f1cc66f84e6ac26a8cc862a4ae9063ae9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:49e4ea796fe843e65e0d5fb09f0a6555704c063422825381bdb201d4843cfe12 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3c8ebe2b438b5cc9c96e61725caa750ed639e2764eaf8da3c5a76f2580c4259d`  
		Last Modified: Mon, 01 Sep 2025 23:52:51 GMT  
		Size: 34.5 MB (34480208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e0c9c0bc001baae6754cacd7396757d44d020b3a3ba6c5ec0a0d0f7224f934`  
		Last Modified: Sat, 04 Oct 2025 09:21:23 GMT  
		Size: 20.9 MB (20860809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e39d9a0fb42af6b523f27db319d34fe787d04f59d17372e4c487e8f8f51a33`  
		Last Modified: Tue, 02 Sep 2025 05:26:52 GMT  
		Size: 53.7 MB (53663473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de0fa8d5a31d6de7660df5d26b9b5793371694899ac736c3ead5c69319ff3baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5446814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225c6d5aca7207f60c427e050972e55f6d57ad128e9a5633c41d67a4f6255882`

```dockerfile
```

-	Layers:
	-	`sha256:292db46bbb48171829bcbb05ce8530bcdaa8817e3adabd0aadc71b7a2816cc45`  
		Last Modified: Tue, 02 Sep 2025 07:20:39 GMT  
		Size: 5.4 MB (5439458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2662036e088a66d0f5458123c6dea52e9ad15427804e3bc4e09b09edabc00477`  
		Last Modified: Tue, 02 Sep 2025 07:20:40 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e2b63612feeea7fb0868f0ed9e155902464732e2d7a28f847571d3d2eb7d291d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104079302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869ba779e8b5052e9e251ee44af37f3effc5631f0747496df7afea4f7f738b02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:d010b851ba09c7b22e7c06ab89aea9736e9ba461b1db1e6347edd26e85142fd1 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3dc034e8b1803c3caeaa0e732c54a197159456b92e58767392c621a4d6017f47`  
		Last Modified: Thu, 09 Oct 2025 21:06:29 GMT  
		Size: 34.1 MB (34093464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a511c49d832edb64e439df348a903968f91f662cdbd34c3e67e37dfa8463ce02`  
		Last Modified: Thu, 09 Oct 2025 22:23:09 GMT  
		Size: 21.0 MB (20953890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d6e549c30ca73922ac70193f8b79eea3f7d2fa8c1fc05516d7e6bdac76a9f8`  
		Last Modified: Fri, 10 Oct 2025 02:01:12 GMT  
		Size: 49.0 MB (49031948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2a6f61865f14cf3545021d7a126161d7a2bdd852a35710f6859049439e40ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6833979ccfdc84cff3342fa15367aaaec7617e6b87f3098c53b1b64c752c9f`

```dockerfile
```

-	Layers:
	-	`sha256:b9a5d8462960d6b9977b50110f6d627ce75a4092da409686c43ffaa9cae695ff`  
		Last Modified: Fri, 10 Oct 2025 04:20:14 GMT  
		Size: 5.8 MB (5769500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d621b7b18fd1e66fedcff599016d3c93eb7b4998971e7d9d15e8597b93aad73b`  
		Last Modified: Fri, 10 Oct 2025 04:20:15 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json
