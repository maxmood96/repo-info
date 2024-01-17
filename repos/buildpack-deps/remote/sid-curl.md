## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:486a44127275e22fa929f8d23f68875881116bf36de992254cb75df7e6d89b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:64b5a2d6bd118137801ec9e87da46b673cdd40cfb36f0993f88363fd7ac2ae2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77214964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927e295d4c468d2fdddf65521f5e9a9fd15a65d3ce71c554fd8ab066d45b097d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:34 GMT
ADD file:4c1ddd73138f061e46cb63a959e0b45e213bbe55a4e9859988b45cbe28c1939e in / 
# Thu, 11 Jan 2024 02:39:35 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 01:35:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1f8012d8f125a645d98266e2a23733c0354f39eaae73d40ec23f48c12dac17e1`  
		Last Modified: Thu, 11 Jan 2024 02:45:14 GMT  
		Size: 52.3 MB (52267954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205021977bbd724db37ff45bd3e42a4406ad4a45db1fdf331064f268fab18963`  
		Last Modified: Wed, 17 Jan 2024 02:02:49 GMT  
		Size: 24.9 MB (24947010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6cebee5c8d10facb262f9db577902c9bded62de791d73a9bef6fa585e90659d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73263609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177e2beeb88bfc59562859fc51fdcafca40a0baf967b4ed51c9e6c6d42e9877c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:50:13 GMT
ADD file:9151e08b2e412287dad7d69ba24534b298db5f003230d2502a6ba98cec1ebd47 in / 
# Thu, 11 Jan 2024 01:50:13 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 01:54:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b1b81c0298ff01b74292896351d56a8bab04cfea53060a06c7a5a819fcaccaed`  
		Last Modified: Thu, 11 Jan 2024 01:55:53 GMT  
		Size: 49.4 MB (49383131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0aa5c0fce04c1adf99bea33a91564c487770dbbedfa0e7123639cdba9ee629`  
		Last Modified: Wed, 17 Jan 2024 02:04:09 GMT  
		Size: 23.9 MB (23880478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:03e387909d92c2be5517164750d31ae88f36f053f9d8d9dbcb98b68a390095c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70055562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfba095e13ac2f01025431d6b3e7f7ceff1324ca9d1cf9f366b7d227c4b112a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:44:19 GMT
ADD file:8fdf812544a777aefa5a72371aaae01c05618dad10c40d3f4c4535ab61effa5e in / 
# Thu, 11 Jan 2024 02:44:20 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 01:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:738b42c6f08e0cf326b2758999daf25b796a2257c832077146951a1871b3fa48`  
		Last Modified: Thu, 11 Jan 2024 02:51:44 GMT  
		Size: 46.9 MB (46880379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4344fe1539287bac9f410eb1d58d25127e48ba76d22ddf7aab276619eb1f72`  
		Last Modified: Wed, 17 Jan 2024 02:22:08 GMT  
		Size: 23.2 MB (23175183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e5f496717aee70ff5506fbd7b595820df2106840e59e444559af3c9e8a929782
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76846601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c92042584feb6124dfc81e228ee87333b33c1792a197b9c09e5b23fa2ee57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:49 GMT
ADD file:41d0336f9211d4665c98a2ae6d92a97885617a6f3ef646ad5e96e1c505887f36 in / 
# Thu, 11 Jan 2024 02:41:50 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 02:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2a6d440355d1d93856497f93e287cec8381a68287949dd140442830cc02425a8`  
		Last Modified: Thu, 11 Jan 2024 02:47:08 GMT  
		Size: 52.1 MB (52148723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a071c791a3f898706203101f39b2c6f5e50f5f2e65e4aef0050f6a0250f24dcc`  
		Last Modified: Wed, 17 Jan 2024 03:01:53 GMT  
		Size: 24.7 MB (24697878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:37f99534b98217aed72b019a68d835cb37c3d1220f444a93b5a320a8858deedc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79144464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d346bfc8a726e172605d7ad37e3e4a92fa194eb915086e792dcf0d6d3dadca8e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:20 GMT
ADD file:62936974dfc268ed9921277921d72e2fe4b8e316d02774bc95127ec6d56693e3 in / 
# Thu, 11 Jan 2024 02:40:21 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 01:44:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ed5772f4773b25b36078212363dc2fec6143ee364938f8da48464f4eec8f182a`  
		Last Modified: Thu, 11 Jan 2024 02:46:50 GMT  
		Size: 53.1 MB (53117689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7366ab7f030dd6fd75cb80e44fe5efd33fe64d8562144abacce7fa99c1488a`  
		Last Modified: Wed, 17 Jan 2024 01:53:45 GMT  
		Size: 26.0 MB (26026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9de9bb657e8a02af020ae5865f2d816b0187295b44e46ca27c77c1a0d2011e02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76702159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b39ff5f40a8eb40f187ee72033f6426df40a0cdbea190cb5983307195815f97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:14:46 GMT
ADD file:5f44d39d860d41ee2d969347a8ee97117d8464c5ba5bb8a7f437e02e02bfcb33 in / 
# Thu, 11 Jan 2024 02:14:53 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 02:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:44d8b0d43d4e86510a6929ab344b91638efe7be700303879a57bc650fbd84861`  
		Last Modified: Thu, 11 Jan 2024 02:26:21 GMT  
		Size: 51.4 MB (51364371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34500c41f528e10a93d61a7b2c77720744cfacc3cc339d67e587ad4119b447e`  
		Last Modified: Wed, 17 Jan 2024 02:53:42 GMT  
		Size: 25.3 MB (25337788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4b9e7b3fc3b3c83b8465758fbbdf1d4b0076fa1276822ff5e0f4b839f428da48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83569716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e4ec61a35c2a868a1c3ccd41d9c70b59dfc7f1fefe155ce219afb697f48d97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:35:47 GMT
ADD file:c2cc792d0e48795239ba8948f28a31a458128e8d2dade2ed88a7cc1830609097 in / 
# Thu, 11 Jan 2024 02:35:50 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 02:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a12077db2f3238d1c66f5358bd931ff537264797def7be2c14c9e9cd0ac05402`  
		Last Modified: Thu, 11 Jan 2024 02:41:17 GMT  
		Size: 56.2 MB (56185653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953634f1b57b8c59b18d596dc376d96fa64e96ffce9fd36d556dc75df00f8f88`  
		Last Modified: Wed, 17 Jan 2024 03:26:42 GMT  
		Size: 27.4 MB (27384063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:233add11b11afb20c312ef8c9e8427f2c1597ce743c067cab9761a80f9001f77
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75109938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a69e28821a20e995b01dac9b242cf8775e36af230f440ffa8815035308f897c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:08:57 GMT
ADD file:2425f95373d17e6fdcc9fa7f49bb6c7911f6b90dc27b013c125e09c38c1691de in / 
# Thu, 11 Jan 2024 02:08:59 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 02:09:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c4051c39033b0cb21a5a8e11e0cc7f40eaa9806ddc6699457c2f509128c3a492`  
		Last Modified: Thu, 11 Jan 2024 02:11:46 GMT  
		Size: 50.5 MB (50487871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620f75619efa24a15de30aab437b0537549a4fbb6727f8684e27928355bff9f`  
		Last Modified: Wed, 17 Jan 2024 02:19:57 GMT  
		Size: 24.6 MB (24622067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2fdc6d13b5294b592c65e6fa0b2ec208b4cc3012497fdee956771fd639693b17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77701535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ca86d269a56318c6628ff9220f75480457e65a05034739c2a7e1c4d97ca91f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:46:39 GMT
ADD file:8031754126dba92ceeddd0be53523bca85fa55f5859c83eaa57be2b0ba8f8046 in / 
# Thu, 11 Jan 2024 01:46:44 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 03:20:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ce6f2c0c05e382af54def5b355ea9bda0f36bd689f9f43fdcd74463778010bc5`  
		Last Modified: Thu, 11 Jan 2024 01:51:57 GMT  
		Size: 51.7 MB (51672176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a14145a4b99d005f650993d40f727d6b617cf78fcb09069cfd0a590898a5ec`  
		Last Modified: Wed, 17 Jan 2024 04:04:55 GMT  
		Size: 26.0 MB (26029359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
