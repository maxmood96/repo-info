## `buildpack-deps:questing-curl`

```console
$ docker pull buildpack-deps@sha256:7d0a989909cb662af13c6987dba2ab8072c8c396f87a676c46e5af1d2105d2ba
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

### `buildpack-deps:questing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:188ef630f9265fa7b7729e269e004fd1174e600c035b0c520ecab70898475a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48562242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fe5da02fb15e7093d4307f1f83631a659807fecad273b932bcb7d8a641c9ee`
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
ADD file:17cd460f059360977af8d3a00489852009c22a41f4352f2ba85943f0f8c5f41f in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3b9d892b6aacf4b0c1cf535d30918dc2256e0c2f52cc1d37bee19067663cbaf9`  
		Last Modified: Tue, 12 Aug 2025 17:03:12 GMT  
		Size: 29.7 MB (29699735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf6521f3b67e01b294cb3de33f7542134a1555d8668193478d0e42ffeda8ade`  
		Last Modified: Tue, 12 Aug 2025 17:23:37 GMT  
		Size: 18.9 MB (18862507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e151f9c870a47c471be91eedbba6f3756613c42cf92ba23a0bc7b7ed2155cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca274a843362f07f571201e14e3fec104439847c246c826705f7e47caa4d35b`

```dockerfile
```

-	Layers:
	-	`sha256:0617b89506c8b2d2342c5489999b877f5c12a73f7a80a68f38be3d40ce4838d1`  
		Last Modified: Tue, 12 Aug 2025 19:20:52 GMT  
		Size: 2.6 MB (2627933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33dad076aec8dd28be7ac8bda3a6a972dc792182fdfde4fff60865535b538434`  
		Last Modified: Tue, 12 Aug 2025 19:20:54 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c347db236569ea66f139e66c76a17fe36b9c22452db19368010fe59f8fced410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44995625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b6b009cadf5bc01275413eb1888ce27e7cfe25e23e46db94bd9e0a9fbf71db`
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
ADD file:9eed1b2293ee9b1a3f538aceaac3ea32a998f61f054dad9cd5a407828bc5e7fa in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0d7bc1e0094544c65656ef653b3c67a22bb857cf01de93e24e36a5b8bd9c6839`  
		Last Modified: Tue, 12 Aug 2025 17:03:09 GMT  
		Size: 27.7 MB (27736612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d602962dce0a4ffd02b7128b627e79af88041418e069c243e79a489d2c76cc9a`  
		Last Modified: Tue, 12 Aug 2025 17:24:45 GMT  
		Size: 17.3 MB (17259013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:704dd7742b727d7e7fb07a237356fc6633ae4a6f2d1469dda3d3ea98228c0f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9f90f7711d0f07766cd27304176f32cde7646a8bdfbd1edaa754f3005e5686`

```dockerfile
```

-	Layers:
	-	`sha256:530610fcd6362d98c2dcf97e67d37963101e5e0310903a603a810465688791f4`  
		Last Modified: Tue, 12 Aug 2025 19:20:59 GMT  
		Size: 2.6 MB (2629435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27682e5ec8dc400f3c1cf2c96e90d544ab58f6d36435437514e550a1091e1058`  
		Last Modified: Tue, 12 Aug 2025 19:21:00 GMT  
		Size: 7.0 KB (7038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3eeee05b590296234c139b5b3d3cbda06bfcce428a433bf8a677ee2ed0dbc714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47698595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8ca539da81875af3e624df3c04463896173bdfd9ec570c02983c95af471ca1`
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
ADD file:ec3f48e621d9128ce28e8aec63d50c4c4eefc59528b99116bbc3032f4279f5ee in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6f3bc6961ab41704f6454c7be252d2be9e9153165b095e56dea5e0112de7753`  
		Last Modified: Tue, 12 Aug 2025 17:03:14 GMT  
		Size: 29.3 MB (29314444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47763b1514857655ffbc66a9fedccd790dec27127100e6dbf9ae3a5fdc7b6d8`  
		Last Modified: Wed, 13 Aug 2025 17:21:13 GMT  
		Size: 18.4 MB (18384151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:42a39bc44c5013043bc02b42d046ea8efb1d7f2726b1329c7bfbd1235a05c473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a385b9c7981ad98ae5c38f69f65cfae77d806b2a6a3738e16d562b942152c2`

```dockerfile
```

-	Layers:
	-	`sha256:b05a20d6e77b12643ea37ec16525f0e69d204494fb3db206ad76787b6b36270e`  
		Last Modified: Tue, 12 Aug 2025 19:21:04 GMT  
		Size: 2.6 MB (2628191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27177b7690261d38580a43c413d29b9a6e8e386d85badd14120227fa9f5d768`  
		Last Modified: Tue, 12 Aug 2025 19:21:05 GMT  
		Size: 7.1 KB (7057 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e5ebf98c8a0f49dedd466596eae0eeee15459c802c32be64726cd2cb3a6a882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54857814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f29b392284ae90bbe390dfe491ac6c459645797f7db1defe214a95be5a4113`
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
ADD file:566d1fae557135e37d75df659c267bd6a62cf94b1fcfe7e157578d9270ef463a in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0b1109ae8bd2c2ee8f31117236bd09c15587a8d6ba7a611f16c4200c2bb761de`  
		Last Modified: Tue, 12 Aug 2025 17:15:59 GMT  
		Size: 34.1 MB (34111991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca0501624351fb3456fb0392bb33c5140287cc91e607e55eed9b0d1cd8846d`  
		Last Modified: Tue, 12 Aug 2025 17:27:55 GMT  
		Size: 20.7 MB (20745823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5cfc13e43d592454deb3a0710b13eeaa816c8cccb9d2131362de82b360cf9d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b0dbed77b044de35662b539636615199d1bf846d5bbabd7be60bf747f9cc8c`

```dockerfile
```

-	Layers:
	-	`sha256:0a7502d97d04a9f548f2358c170c66db387d74f7c9bf55e2acdc05ee03d65047`  
		Last Modified: Tue, 12 Aug 2025 19:21:09 GMT  
		Size: 2.6 MB (2631756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff502f9149264b0c70eb6247503f638d30748882f4c1f716362634af69a602f`  
		Last Modified: Tue, 12 Aug 2025 19:21:10 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:219e1fccba82e26bb799d7a10e7e7677f73b8c1e0b9376607838ab8b00d75b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50567938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e5175a07050ec5fa0d19d161dc31e17c9b211db8d4c8934d7225c875b4b6f5`
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
ADD file:2ad5f91fe5edd35a8a0cb6ec99904a35771f2b8a0819b888cca27bd2b8edc998 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c765da7735337fafbed911e71485d7f0505e50d1941beb7fa962494422b6b9be`  
		Last Modified: Tue, 12 Aug 2025 17:03:53 GMT  
		Size: 29.6 MB (29618719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53c981ca1715af0d0448a048d0a4642c6a7becf08354f007f4e1da1b9569b0`  
		Last Modified: Tue, 12 Aug 2025 20:19:20 GMT  
		Size: 20.9 MB (20949219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d054b12fee6ae53954cf2ebfbc9c691353f603821fe1157f6c1bebb4f3b06283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c72e6a6c5ba8dfe91b31a4967b94ce9e3a718ea37a6e293f006f56519e9dc2`

```dockerfile
```

-	Layers:
	-	`sha256:8dcc0107bfd41ce734fcaeff14c46b13ab75b7a83898fe4477e8bb0a845e5c74`  
		Last Modified: Tue, 12 Aug 2025 19:21:21 GMT  
		Size: 2.6 MB (2629964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75c70d3cc8428211b8a4c533c3af9e2f94e705d1d9dcb7ae9f8f7f80a1c26a54`  
		Last Modified: Tue, 12 Aug 2025 19:21:22 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json
