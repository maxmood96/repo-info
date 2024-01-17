## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:10e14eb14ac2be041a45f1e52e408378814f115ec3dc39419926b7ada9a2df26
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:714110464ea651671b5390b311bd8dcdbe39be58ec30fbb089a919c9db77746c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146051653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54c073f944c936c684c7aaaa0ddeff8a859b2118b3291e678081c1adca186a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:34 GMT
ADD file:4c1ddd73138f061e46cb63a959e0b45e213bbe55a4e9859988b45cbe28c1939e in / 
# Thu, 11 Jan 2024 02:39:35 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 01:35:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 17 Jan 2024 01:36:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:cf8137ae24a343757eba7721bb9490ec41aff1749b41898b6251da8046ea10ec`  
		Last Modified: Wed, 17 Jan 2024 02:03:07 GMT  
		Size: 68.8 MB (68836689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f1d21e0f17a4d50a7b5f53084943a622f8c586ad7893bb2dbb602f494d66e6a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139698524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355ffa3db00f0511b1f47423fcc63d930517f2a1fe2ca5ff10fa375bc85beb63`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:50:13 GMT
ADD file:9151e08b2e412287dad7d69ba24534b298db5f003230d2502a6ba98cec1ebd47 in / 
# Thu, 11 Jan 2024 01:50:13 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 01:54:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 17 Jan 2024 01:55:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:22e404682147cc2de762c62385c04f11b3d998ef72568dee7bac8c8d9c8f36a2`  
		Last Modified: Wed, 17 Jan 2024 02:04:34 GMT  
		Size: 66.4 MB (66434915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b9a375715b9131335bdb1bb4b81495866575497bf20a1986d373f1ae6aa2781
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133697320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bd841a28ad91b2048864b0f54c8d9bc2fe01f385fb915d2f19bedf3bb59668`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:44:19 GMT
ADD file:8fdf812544a777aefa5a72371aaae01c05618dad10c40d3f4c4535ab61effa5e in / 
# Thu, 11 Jan 2024 02:44:20 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 01:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 17 Jan 2024 01:47:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:4e55be1911f0143fcd8b755c17d0cfe94c6e52c02fa9e53b00beeb667ed0803c`  
		Last Modified: Wed, 17 Jan 2024 02:22:33 GMT  
		Size: 63.6 MB (63641758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f98441b927900a264819ce30f94765982563bcaab12977ba88467a7900217393
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145751265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26433e6289bcef0b4b90af778f2e2e6fe33400f88c87a6c47b13014ea0adfda`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:49 GMT
ADD file:41d0336f9211d4665c98a2ae6d92a97885617a6f3ef646ad5e96e1c505887f36 in / 
# Thu, 11 Jan 2024 02:41:50 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 02:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 17 Jan 2024 02:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:111adc9a2a938129f51c7422978eb5f13578db96f13855a9c1f3c0f30178f70b`  
		Last Modified: Wed, 17 Jan 2024 03:02:23 GMT  
		Size: 68.9 MB (68904664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8aae1fc2ecbc99fb5f0ba822589ad57c3f952908f36132cb831ea83cdffba936
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149897386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e85cd252ac83d961053efb8bd074b19f76230c5a499007b8364c23126afee30`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:20 GMT
ADD file:62936974dfc268ed9921277921d72e2fe4b8e316d02774bc95127ec6d56693e3 in / 
# Thu, 11 Jan 2024 02:40:21 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 01:44:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 17 Jan 2024 01:45:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:b3af85fbac70ebaf309c2b98cc2a97f2badef47a0e558a29b619fb01c7a8d14e`  
		Last Modified: Wed, 17 Jan 2024 01:54:09 GMT  
		Size: 70.8 MB (70752922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b2a5e64abd19603b93de44f566c36d45a16754262bc5efb9c08dd088b6e3a8a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144279801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a7e3773c6a26cd509892f7a954c36a7363173632ebcb4e17d1856129908f75`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:14:46 GMT
ADD file:5f44d39d860d41ee2d969347a8ee97117d8464c5ba5bb8a7f437e02e02bfcb33 in / 
# Thu, 11 Jan 2024 02:14:53 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 02:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 17 Jan 2024 02:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:9dea529b163488b737fc5d7fbe86b045a873a473c3edeab6addefa4f2060c5d8`  
		Last Modified: Wed, 17 Jan 2024 02:54:48 GMT  
		Size: 67.6 MB (67577642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:364aa26906ce0ca0dca15a60bd9d8b7b17d7f94bdfb587148cc66cd645005871
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156799453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ad282d024978e28923a9585d44fb0a5c5f68392459167812599f5c8c82482f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:35:47 GMT
ADD file:c2cc792d0e48795239ba8948f28a31a458128e8d2dade2ed88a7cc1830609097 in / 
# Thu, 11 Jan 2024 02:35:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:13:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a12077db2f3238d1c66f5358bd931ff537264797def7be2c14c9e9cd0ac05402`  
		Last Modified: Thu, 11 Jan 2024 02:41:17 GMT  
		Size: 56.2 MB (56185653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25800b978411714d00508bd5510f9f780d186fe5a4b83794204a9ad4f6eb6bbb`  
		Last Modified: Thu, 11 Jan 2024 07:25:41 GMT  
		Size: 26.2 MB (26179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5849bf0a86283edbb330815a50679f0e541585b82098279c61a8bedd8a86f8a`  
		Last Modified: Thu, 11 Jan 2024 07:26:04 GMT  
		Size: 74.4 MB (74434454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f983af57a2e19707c52901eb0df8675c1c7eed6eb16b900e7dd4d7f6b4da5c4e
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143157689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22ca7e8187c63dc04772cbb83fbce441d7a7582470161f6fc40f2eeccbacbf3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:08:57 GMT
ADD file:2425f95373d17e6fdcc9fa7f49bb6c7911f6b90dc27b013c125e09c38c1691de in / 
# Thu, 11 Jan 2024 02:08:59 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 02:09:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 17 Jan 2024 02:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
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
	-	`sha256:2efb5904df863cf381e2ff752f4ca98dee45f13894e41bf058c1d395ce9e188d`  
		Last Modified: Wed, 17 Jan 2024 02:21:18 GMT  
		Size: 68.0 MB (68047751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ea27c289fb7caaada04fd9f044f49c4bf897322ac7a54c392945d108cbd29056
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.6 MB (146559528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17277d58179c3ddf94a071bb95809f56ab29c2426db21a0f2920964023436c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:46:39 GMT
ADD file:8031754126dba92ceeddd0be53523bca85fa55f5859c83eaa57be2b0ba8f8046 in / 
# Thu, 11 Jan 2024 01:46:44 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:13:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ce6f2c0c05e382af54def5b355ea9bda0f36bd689f9f43fdcd74463778010bc5`  
		Last Modified: Thu, 11 Jan 2024 01:51:57 GMT  
		Size: 51.7 MB (51672176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccdf962076103e72329069bf48fa3112a100d8a6deee506176beb22e27789a0`  
		Last Modified: Thu, 11 Jan 2024 02:22:51 GMT  
		Size: 24.9 MB (24850534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b64ba60f98b957715429fcc464c59051f469caba372893e922d41e0cf32bad4`  
		Last Modified: Thu, 11 Jan 2024 02:23:07 GMT  
		Size: 70.0 MB (70036818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
