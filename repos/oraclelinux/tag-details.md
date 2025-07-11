<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `oraclelinux`

-	[`oraclelinux:10`](#oraclelinux10)
-	[`oraclelinux:10-slim`](#oraclelinux10-slim)
-	[`oraclelinux:7`](#oraclelinux7)
-	[`oraclelinux:7-slim`](#oraclelinux7-slim)
-	[`oraclelinux:7-slim-fips`](#oraclelinux7-slim-fips)
-	[`oraclelinux:7.9`](#oraclelinux79)
-	[`oraclelinux:8`](#oraclelinux8)
-	[`oraclelinux:8-slim`](#oraclelinux8-slim)
-	[`oraclelinux:8-slim-fips`](#oraclelinux8-slim-fips)
-	[`oraclelinux:8.10`](#oraclelinux810)
-	[`oraclelinux:9`](#oraclelinux9)
-	[`oraclelinux:9-slim`](#oraclelinux9-slim)
-	[`oraclelinux:9-slim-fips`](#oraclelinux9-slim-fips)

## `oraclelinux:10`

**does not exist** (yet?)

## `oraclelinux:10-slim`

**does not exist** (yet?)

## `oraclelinux:7`

```console
$ docker pull oraclelinux@sha256:767c93c07b1fa621ae56d1f5f090e8c0dce7eb452e7dda1e74bbe7546504d63f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:7` - linux; amd64

```console
$ docker pull oraclelinux@sha256:7bd67d839b5296423b49806513e985d1440c1666732bdab49d8fe4f2eaa8882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95379377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27eb3f6a5a2ea765d10a69fcc8cdf5e8d551d46aad900344db5a30bc2790f925`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:51:26 GMT
ADD oraclelinux-7-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:51:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7e97d888e3ce798d1fd4f6290ab2faa2e76d131b997de8abd0073b19ce89ff9e`  
		Last Modified: Fri, 13 Dec 2024 17:01:27 GMT  
		Size: 95.4 MB (95379377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:48cbf9d2b2eb4e8b49abbc4a5ee884bbd4e38d9a7775f32d23521d4cb4ec9334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5986658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2d2f842db34aaa9439decd84f84e8cdd5677d3ec53e95365d21157d33f121f`

```dockerfile
```

-	Layers:
	-	`sha256:27e4fd6dc2a746095a9d3bda1f23775ebdee67e2f23c01fdc355d4073032ea97`  
		Last Modified: Sun, 15 Dec 2024 00:05:11 GMT  
		Size: 6.0 MB (5981509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c096aa08ec8ef96172085216ad2f1438f843a0454bec76e639965c1886237f5d`  
		Last Modified: Mon, 06 Jan 2025 17:55:47 GMT  
		Size: 5.1 KB (5149 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:7` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:fa93b39b22ba5975b662591e71d508b060c06a60b0dd149aedd57e8832dee1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97327013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1819ead03a2e5166f44a38f549f069a3b0a7d2987fb565b8c5165cf40e5bf2f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:52:16 GMT
ADD oraclelinux-7-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9d7edc91d9d8dde556a51cc4cb7cfc1cfea1a0c15f6388ab6c8b583c8f8c42c8`  
		Last Modified: Fri, 13 Dec 2024 22:16:38 GMT  
		Size: 97.3 MB (97327013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:382ad209af84477ee4b3dc4bcfee2f50041252a10cf71d5e0499285ae44489b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4bf0b4acbd52c5c2c36018b0f5310d7d7d5d8905633d958151bfdf0286fe62`

```dockerfile
```

-	Layers:
	-	`sha256:808b3b6e809d50e57eab82cabcc5d37acf7266bcdf087589d1ad337a77ffd5d5`  
		Last Modified: Mon, 06 Jan 2025 22:57:07 GMT  
		Size: 6.0 MB (5975000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0fb3a85603ebc1f4a6e7cb274bcb060fdd154bd987a2f2ee1d7d3022548e50`  
		Last Modified: Mon, 06 Jan 2025 07:27:30 GMT  
		Size: 5.2 KB (5190 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:7-slim`

```console
$ docker pull oraclelinux@sha256:1add6ed8602ea996528110fe75f4b03c2ca7ffdbe9497148dbb46c3cc9ce6acd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:7-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:645371a66c08ed18b7aacf217c964f0db70c26ac87f3d8816d7ae24160f178e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50488860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05211a081d592eb56daf16b0651eb55b233a65466492b28345804309b45caf21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:51:26 GMT
ADD oraclelinux-7-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:51:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:38299ae2e819f6ec4befee45312f809ca241167aa554dd79e0a4baf505b88d21`  
		Last Modified: Fri, 13 Dec 2024 15:06:18 GMT  
		Size: 50.5 MB (50488860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:3e60616703d321b4c868bf296f2fd6c8c6c5539d7252f553a29a38d9c7e381b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4265757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3719d88423e8ac803d456c5577f5999495b77126402be43cca2ffafe64bc5cdf`

```dockerfile
```

-	Layers:
	-	`sha256:93bca7b03d35bd2fefaf75af27762097b46af67876bee548d64a9b6b6006d9a3`  
		Last Modified: Mon, 16 Dec 2024 07:24:25 GMT  
		Size: 4.3 MB (4260876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e4ba8e10b3db73de89af88b81958d66dc02f595d255183dc19952eb0ce4e621`  
		Last Modified: Wed, 18 Dec 2024 02:47:55 GMT  
		Size: 4.9 KB (4881 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:7-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:c076be2394491ba6ee7e1c181bba19f7fb14b9b7a3d02a587e39990095e1f33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51085581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06f30900e46d5c64d59c1d25d8ab52556276be4385ec1a0390fb904c5264e01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:52:16 GMT
ADD oraclelinux-7-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7f916988e24d766c1f69587f05a2bec5c9eaa3b83215ef893b0a1c187a4080e2`  
		Last Modified: Fri, 13 Dec 2024 17:00:24 GMT  
		Size: 51.1 MB (51085581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:5b1dc952926404e7492092f571e5821751c628902e657ba855a481ed94018fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4261981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0d1dae38824c867305a6a9860f9e0aaa76d28518ec25c93b6e7e70a102f95c`

```dockerfile
```

-	Layers:
	-	`sha256:65358737d3c6c3d7c88bcc5babcc796654b2ea32bf52846e7df42a2576ecf66b`  
		Last Modified: Mon, 16 Dec 2024 07:33:07 GMT  
		Size: 4.3 MB (4257067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5767786f31b0ec8711c380c8c59ed27febec722831f991be9790f1ba558d597b`  
		Last Modified: Wed, 08 Jan 2025 01:49:48 GMT  
		Size: 4.9 KB (4914 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:7-slim-fips`

```console
$ docker pull oraclelinux@sha256:412c63a1a077bf720cb5371c81e8b3ff223068a81502115b5c16c6a8e0b47d06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:7-slim-fips` - linux; amd64

```console
$ docker pull oraclelinux@sha256:12ac0df82f5a3f2f09ecad7854ea4444fc1b708ef411c1e2f24d6f25d4245ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76371715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50463282112b0271e86226490f8f265a25803e9027da5110791e968ef330fe1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:51:26 GMT
ADD oraclelinux-7-slim-fips-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:51:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9e381a889e7f7459c839feb62226085f5b7525448d0f6680fac53900ab4ba12d`  
		Last Modified: Sun, 15 Dec 2024 00:05:19 GMT  
		Size: 76.4 MB (76371715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:3fac3d84b86523a883865ed8f2af0be8356d4aa35e684adae0a4479919f2f56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc0605a6d6bf225b94244189b2b8e89c5beede52a9b7cad51d157f3989a9f2d`

```dockerfile
```

-	Layers:
	-	`sha256:4f9cbc8a8c05259ded9bf3516634c155287aff566191d9c0da39f98bfc94f423`  
		Last Modified: Mon, 16 Dec 2024 07:25:32 GMT  
		Size: 5.1 MB (5121617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d014e356117e170e2658308a622945cc432eeaeb8dae01189679438180047e`  
		Last Modified: Wed, 08 Jan 2025 03:48:54 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:7-slim-fips` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:4b254a0e1369e408b33ec9790d2467649b6664dfddf2fcbea700d910d055e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77985183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede26b130cea5ed695383e2c7010bd152ff5f8ded3a7930551fd9370ce53b30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:52:16 GMT
ADD oraclelinux-7-slim-fips-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b50bd403ff40f287f6fc609d6d2c609ee8eb561a4fa13293b9c6b686bd8f7cff`  
		Last Modified: Tue, 07 Jan 2025 20:52:19 GMT  
		Size: 78.0 MB (77985183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:a168426b3c9391aa341551993a6681b05a63b3495ca97b187e8d66a81d4bf375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce130b99a71cc90c5ba4b4114df2a09f196d1985957304e529b7372e3531ff3b`

```dockerfile
```

-	Layers:
	-	`sha256:15a9e031bceed3e015eb997b73961b66e8704e7256dfcd494c2cc941ddd68762`  
		Last Modified: Tue, 07 Jan 2025 20:52:12 GMT  
		Size: 5.1 MB (5117808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf49abd27521aa834ddfe1bf3fd10cf25d974c06de2eccc4319593d0f5375cf`  
		Last Modified: Mon, 16 Dec 2024 07:26:00 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:7.9`

```console
$ docker pull oraclelinux@sha256:767c93c07b1fa621ae56d1f5f090e8c0dce7eb452e7dda1e74bbe7546504d63f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:7.9` - linux; amd64

```console
$ docker pull oraclelinux@sha256:7bd67d839b5296423b49806513e985d1440c1666732bdab49d8fe4f2eaa8882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95379377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27eb3f6a5a2ea765d10a69fcc8cdf5e8d551d46aad900344db5a30bc2790f925`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:51:26 GMT
ADD oraclelinux-7-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:51:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7e97d888e3ce798d1fd4f6290ab2faa2e76d131b997de8abd0073b19ce89ff9e`  
		Last Modified: Fri, 13 Dec 2024 17:01:27 GMT  
		Size: 95.4 MB (95379377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7.9` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:48cbf9d2b2eb4e8b49abbc4a5ee884bbd4e38d9a7775f32d23521d4cb4ec9334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5986658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2d2f842db34aaa9439decd84f84e8cdd5677d3ec53e95365d21157d33f121f`

```dockerfile
```

-	Layers:
	-	`sha256:27e4fd6dc2a746095a9d3bda1f23775ebdee67e2f23c01fdc355d4073032ea97`  
		Last Modified: Sun, 15 Dec 2024 00:05:11 GMT  
		Size: 6.0 MB (5981509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c096aa08ec8ef96172085216ad2f1438f843a0454bec76e639965c1886237f5d`  
		Last Modified: Mon, 06 Jan 2025 17:55:47 GMT  
		Size: 5.1 KB (5149 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:7.9` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:fa93b39b22ba5975b662591e71d508b060c06a60b0dd149aedd57e8832dee1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97327013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1819ead03a2e5166f44a38f549f069a3b0a7d2987fb565b8c5165cf40e5bf2f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Dec 2024 23:52:16 GMT
ADD oraclelinux-7-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Dec 2024 23:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9d7edc91d9d8dde556a51cc4cb7cfc1cfea1a0c15f6388ab6c8b583c8f8c42c8`  
		Last Modified: Fri, 13 Dec 2024 22:16:38 GMT  
		Size: 97.3 MB (97327013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:7.9` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:382ad209af84477ee4b3dc4bcfee2f50041252a10cf71d5e0499285ae44489b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4bf0b4acbd52c5c2c36018b0f5310d7d7d5d8905633d958151bfdf0286fe62`

```dockerfile
```

-	Layers:
	-	`sha256:808b3b6e809d50e57eab82cabcc5d37acf7266bcdf087589d1ad337a77ffd5d5`  
		Last Modified: Mon, 06 Jan 2025 22:57:07 GMT  
		Size: 6.0 MB (5975000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0fb3a85603ebc1f4a6e7cb274bcb060fdd154bd987a2f2ee1d7d3022548e50`  
		Last Modified: Mon, 06 Jan 2025 07:27:30 GMT  
		Size: 5.2 KB (5190 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:8`

```console
$ docker pull oraclelinux@sha256:03688b1a89797bafabc1d22b6b2da6d44aab08a7852069aca653c5ad625d036c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:8` - linux; amd64

```console
$ docker pull oraclelinux@sha256:76fd722f3542861a9c1ccff40d8dde32c475f152c6492c1b48d072f25190ae61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100837671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d4d815aca2d61d0e0ea7cbed217b55491a12fc73f4bcffc23dc68a76438fcc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Jul 2025 21:25:14 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Wed, 02 Jul 2025 21:25:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb7f7b0b4ba16a5cad75dd46e5d7ca6cb602abe425c73c9bbdbf79a496f3d0b7`  
		Last Modified: Wed, 02 Jul 2025 22:09:33 GMT  
		Size: 100.8 MB (100837671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:2b8b418b04105bad3adb607cd1a05252647af345090daec1b1073c080ca12623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6148565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f0404c8af4c6da12d7a0bed400ffa146987e090ff4ad4c1654c1813c0d5120`

```dockerfile
```

-	Layers:
	-	`sha256:51dfe2e49a3080a5dd8da083862fecae9faafc92c00cc934d75c0dcfd982c0fb`  
		Last Modified: Thu, 03 Jul 2025 00:36:22 GMT  
		Size: 6.1 MB (6143413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348b6fff78bb138a190f3083b9640f9cf5800de2a83f0ee67ead0633872be6f9`  
		Last Modified: Thu, 03 Jul 2025 00:36:23 GMT  
		Size: 5.2 KB (5152 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:8` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:2e3fba4beaab9e4fc1491c58c3273f7d338ebaf7d0da874d235889dab3926916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99676757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d1f7becbad04bb6eebc402fdd4b135abbcaeabb3d399159a17d0e1778a6fee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Jul 2025 21:25:48 GMT
ADD oraclelinux-8-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 02 Jul 2025 21:25:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:86b01d2f5bb65e26f72212bc4732a973810ad2aed5986e99cce39a035bad2f71`  
		Last Modified: Wed, 02 Jul 2025 22:12:50 GMT  
		Size: 99.7 MB (99676757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:bc751860da553675eecda41b0228b1b50f020bb5a97c8937c987863450a0be4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6147568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b266894c66a08fa048ff2e3961d436f09c16ba7fa829acf767c3699f34b33a`

```dockerfile
```

-	Layers:
	-	`sha256:4ff7418fc518931e19f20bb163403385dcff1f932253b69adc4c8477e1e8a24d`  
		Last Modified: Thu, 03 Jul 2025 00:36:27 GMT  
		Size: 6.1 MB (6142376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207ac7c555b2f84a82da3b4fccabbb32f77bd71b7048b647bf5a47eaae66fbaf`  
		Last Modified: Thu, 03 Jul 2025 00:36:28 GMT  
		Size: 5.2 KB (5192 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:8-slim`

```console
$ docker pull oraclelinux@sha256:bb2e6c9d504febf1abc7472fc2039dd0d3710296fe038f7b4640388e2db5dd3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:8-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:e90d8f6242a29cc770e4f2ae6d6a01f1fbd03add50675db0b983db240f41e567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51311558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b47aba2da7158993e7310386f9a0bb2a7be37324cbdbf35ed2a891df97691b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Jun 2025 16:42:18 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:42:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0915556054e5fcd1f04e454b0deedf305bb209616c5a72a8b2d83db9191e5115`  
		Last Modified: Thu, 12 Jun 2025 21:07:27 GMT  
		Size: 51.3 MB (51311558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:59e3e7cd5bf73eff47ca5c2f06e02ad54fb4f026117fc42d1a7efd36401b052f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2088920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cbb8b143ffa01372671e8eace88cbae6cfa9615e341e2a77c4ca51dd68c36c`

```dockerfile
```

-	Layers:
	-	`sha256:e871053468bd29b3962010be753acdc6c1607c171543c4f6fab36031fac6f3d6`  
		Last Modified: Thu, 12 Jun 2025 21:36:23 GMT  
		Size: 2.1 MB (2084039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c532d7ab1ab66525dbaff598fb887c47eac5dca12f106fbdb5c1f882a2545a6`  
		Last Modified: Thu, 12 Jun 2025 21:36:24 GMT  
		Size: 4.9 KB (4881 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:8-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:70d371bc733e62d10b29e2e5e361a3f6e36aa492a61ebead9ede186091cc7f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50039112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d340b398d0794c7b605c402b272d66e00c436260c8b84214e19d68cff57e01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Jun 2025 16:43:09 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:43:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d998890baf088acce50ef79f8e8dc3eab36a2dc008c7774fa6e1e1140c89c3c3`  
		Last Modified: Fri, 13 Jun 2025 01:08:32 GMT  
		Size: 50.0 MB (50039112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:33ba58dd10bd2270890166e7f7bdb8c63f41de25bb646383fad78f25fec885cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2088351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c34182bb44647c71e7f365337237a7da54a12de9267ea98c7abfedbfe6451b8`

```dockerfile
```

-	Layers:
	-	`sha256:e08fabc4ac1c8239d371aba41bb6182cd34b90cf0b5cf8b11b6e2bb8e8311f7c`  
		Last Modified: Fri, 13 Jun 2025 00:36:24 GMT  
		Size: 2.1 MB (2083437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:853f847658ac4691bc5d672b13ba97e27c1f572552c271df070607a53bc7b5ea`  
		Last Modified: Fri, 13 Jun 2025 00:36:25 GMT  
		Size: 4.9 KB (4914 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:8-slim-fips`

```console
$ docker pull oraclelinux@sha256:828922cc70f68d93b8fec0362fa51f9fd5b37016a9eba8f2e832e46f54928c95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:8-slim-fips` - linux; amd64

```console
$ docker pull oraclelinux@sha256:6946624d4317cb6b678dfbc6842913ced9616aff96873d87c357c5af7445c1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51319028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9157b2efb0c6ce10a95a3f5fa16cd3ebc47d1b47bbb499b693554b64cd8fd468`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Jun 2025 16:42:18 GMT
ADD oraclelinux-8-slim-fips-amd64-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:42:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:acdb69813747e7f3c9d245fdeb83de6143d52f2c0e3cba895877c944bd3420b1`  
		Last Modified: Thu, 12 Jun 2025 21:36:35 GMT  
		Size: 51.3 MB (51319028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:a83d553af0b3db3163bd478b465e1e606581355682102c7aee4e1f72271755fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2095296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb337953e72a7b7db81bfebb6abcde8dab8ddf197452618714ee6a80ff0dca0`

```dockerfile
```

-	Layers:
	-	`sha256:8d709a1af2457af452d80ef02282e2dee8768a3b9c5922f80ae26bafda83ff23`  
		Last Modified: Thu, 12 Jun 2025 21:36:27 GMT  
		Size: 2.1 MB (2090377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c9e0f341cee335d569eef71d6bbfb5fa776e3936b1b000ab218e912d00cc44`  
		Last Modified: Thu, 12 Jun 2025 21:36:28 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:8-slim-fips` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:2ef0f21f52d803bfffa81362e578f496876e2dde1ac8949724d1f476aa5015d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50042716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1836a4bde94911e9d3b4b15f2ac4902ceaf1f4fedd4ca2f52cbcda579a6ff05b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Jun 2025 16:43:09 GMT
ADD oraclelinux-8-slim-fips-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:43:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1b1402ae66a4041e770c0beecbc7f1f701004108806513c2f80f82b3a1a85bf5`  
		Last Modified: Thu, 12 Jun 2025 21:31:59 GMT  
		Size: 50.0 MB (50042716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:11cf4666a77c11fb87b9837d567786d93ce6a59763a1fe127207c053d0f2b068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2094727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a40b0da6c39887ae37c0f414d454f443b60ef136ac0eda3201121640511a9a`

```dockerfile
```

-	Layers:
	-	`sha256:c66a392c47a0871daf84496ea3d5b4c7dc2970b96168d6dea38e1ef9ba55d010`  
		Last Modified: Fri, 13 Jun 2025 00:36:28 GMT  
		Size: 2.1 MB (2089775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa168b894d93412f4031d380cf16d6333b9b8537bd34f9ecfc2fc8a2062ef55`  
		Last Modified: Fri, 13 Jun 2025 00:36:29 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:8.10`

```console
$ docker pull oraclelinux@sha256:03688b1a89797bafabc1d22b6b2da6d44aab08a7852069aca653c5ad625d036c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:8.10` - linux; amd64

```console
$ docker pull oraclelinux@sha256:76fd722f3542861a9c1ccff40d8dde32c475f152c6492c1b48d072f25190ae61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100837671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d4d815aca2d61d0e0ea7cbed217b55491a12fc73f4bcffc23dc68a76438fcc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Jul 2025 21:25:14 GMT
ADD oraclelinux-8-amd64-rootfs.tar.xz / # buildkit
# Wed, 02 Jul 2025 21:25:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb7f7b0b4ba16a5cad75dd46e5d7ca6cb602abe425c73c9bbdbf79a496f3d0b7`  
		Last Modified: Wed, 02 Jul 2025 22:09:33 GMT  
		Size: 100.8 MB (100837671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8.10` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:2b8b418b04105bad3adb607cd1a05252647af345090daec1b1073c080ca12623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6148565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f0404c8af4c6da12d7a0bed400ffa146987e090ff4ad4c1654c1813c0d5120`

```dockerfile
```

-	Layers:
	-	`sha256:51dfe2e49a3080a5dd8da083862fecae9faafc92c00cc934d75c0dcfd982c0fb`  
		Last Modified: Thu, 03 Jul 2025 00:36:22 GMT  
		Size: 6.1 MB (6143413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348b6fff78bb138a190f3083b9640f9cf5800de2a83f0ee67ead0633872be6f9`  
		Last Modified: Thu, 03 Jul 2025 00:36:23 GMT  
		Size: 5.2 KB (5152 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:8.10` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:2e3fba4beaab9e4fc1491c58c3273f7d338ebaf7d0da874d235889dab3926916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99676757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d1f7becbad04bb6eebc402fdd4b135abbcaeabb3d399159a17d0e1778a6fee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Jul 2025 21:25:48 GMT
ADD oraclelinux-8-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 02 Jul 2025 21:25:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:86b01d2f5bb65e26f72212bc4732a973810ad2aed5986e99cce39a035bad2f71`  
		Last Modified: Wed, 02 Jul 2025 22:12:50 GMT  
		Size: 99.7 MB (99676757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:8.10` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:bc751860da553675eecda41b0228b1b50f020bb5a97c8937c987863450a0be4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6147568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b266894c66a08fa048ff2e3961d436f09c16ba7fa829acf767c3699f34b33a`

```dockerfile
```

-	Layers:
	-	`sha256:4ff7418fc518931e19f20bb163403385dcff1f932253b69adc4c8477e1e8a24d`  
		Last Modified: Thu, 03 Jul 2025 00:36:27 GMT  
		Size: 6.1 MB (6142376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207ac7c555b2f84a82da3b4fccabbb32f77bd71b7048b647bf5a47eaae66fbaf`  
		Last Modified: Thu, 03 Jul 2025 00:36:28 GMT  
		Size: 5.2 KB (5192 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:9`

```console
$ docker pull oraclelinux@sha256:baabc922ec8f9636e5a295eee449ee1d2b15cb9bcac0623d7f1cf1b85efabba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:9` - linux; amd64

```console
$ docker pull oraclelinux@sha256:09672dc6f42fe0b88deffd9a50c8015d58b356b47862528493e2821faa3d7304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96423486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4ee8744b0dc026ac851afbf48326b58b287e7cd392025140e947b223fc4917`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 08 Jul 2025 18:36:39 GMT
ADD oraclelinux-9-amd64-rootfs.tar.xz / # buildkit
# Tue, 08 Jul 2025 18:36:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d510e3adc90bc9eafdfa137184e28e49d8c9db47efceea9dfdd2aa4eced52c71`  
		Last Modified: Tue, 08 Jul 2025 21:36:34 GMT  
		Size: 96.4 MB (96423486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:74c50cc6b5807ea8c1768abf2dc1a0acc3d978e1eea9d7d36c5e40572a57b389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a631026e0f9bc41680cc1deeee728c59c8921e02033d160f4bca81eeaef8646a`

```dockerfile
```

-	Layers:
	-	`sha256:b3eff0a7c1ae0480eb499b9530940b64c7ed4bc9a61eb0d021571a6d4a1adf27`  
		Last Modified: Tue, 08 Jul 2025 21:36:23 GMT  
		Size: 5.7 MB (5736494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74bdace8e2d08a0e20c1feea0e0ae6ead014b5ee0effeadf073f233b6c4c45f9`  
		Last Modified: Tue, 08 Jul 2025 21:36:23 GMT  
		Size: 4.8 KB (4847 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:9` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:43543edcce696370441468a66a8f9ad45b772f927c275c54a5a6aefb8a31b636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94824999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0557e94033606dc87b7ab7510e9225f6629a3d78d8d3640a7bd244fe114819f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 08 Jul 2025 18:37:11 GMT
ADD oraclelinux-9-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 08 Jul 2025 18:37:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:29c9ad30a66168609e2a951b76e5523a5e5b59106fc03b0293f9cb713e7b11ee`  
		Last Modified: Tue, 08 Jul 2025 21:36:38 GMT  
		Size: 94.8 MB (94824999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:877210ae3f96050354a532c031b2f1ec3a19b099f9ff3ab7c17604184f4f40c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd0f8596cde4368b31e9d4daaa369e792c481b1d2f1d7bb0619e29a1997fef9`

```dockerfile
```

-	Layers:
	-	`sha256:506c4722ccfd146c599ad5492fb76c0b114c6277ee32b77cea448514b37a4d06`  
		Last Modified: Tue, 08 Jul 2025 21:36:28 GMT  
		Size: 5.7 MB (5736042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9810ed99038b693a2773700f5125f76844cb481500e18246dbdd185139fdb3b`  
		Last Modified: Tue, 08 Jul 2025 21:36:29 GMT  
		Size: 4.9 KB (4876 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:9-slim`

```console
$ docker pull oraclelinux@sha256:4b745d63292f728e0a697dfccaae4d823a5f4942e7ea4c5c96dd9c674073de44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:9-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:097e8b0f2422589d1928e24959ae2f940b0841b1f2835afd3b3ab57a08fec82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49500548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae06af6843b5405e6a43dc4ccb1b9ac5c0e863fa9a625ef4c4be059c44f03ac3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Jul 2025 18:39:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 01 Jul 2025 18:39:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3d2798b2072afb2166cb6041ab9f9c9b2e8f24e24a86be4af701bfa5dece5e10`  
		Last Modified: Tue, 01 Jul 2025 21:30:00 GMT  
		Size: 49.5 MB (49500548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:a41d366bf4cbd9d33fbc1c3333b22c18b7e943e5dc2f91404f0849ffe7c6eedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2194706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb4df47f59fda2a31e1fe57db329ab9aa3b8ecd393480f8c22f24431a6c238b`

```dockerfile
```

-	Layers:
	-	`sha256:bfc14d1fe355ee00402c22157c6929525116e2f13c17e4753265dab644222ae9`  
		Last Modified: Tue, 01 Jul 2025 21:36:26 GMT  
		Size: 2.2 MB (2189825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a1dcf240515bae6d600066cac07d18abd2cfd03484e85548158645d7282efda`  
		Last Modified: Tue, 01 Jul 2025 21:36:27 GMT  
		Size: 4.9 KB (4881 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:9-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:0e95b82c87653f2465be63d40065f4a0c3aa8c87e64f659fa383d9943d677f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48087084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168d01560f1eda379d4d7c9f57d29db49e229cb0aa08cbc2ee2001e2255dbf88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Jul 2025 18:40:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 01 Jul 2025 18:40:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:40b5f8b6bc9880acfd6e05d4b46d40ffccdaa51cf95ba3b0b8be3492c65bf5be`  
		Last Modified: Wed, 02 Jul 2025 02:36:02 GMT  
		Size: 48.1 MB (48087084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9-slim` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:c62714d3d1b577fd3c51d02fe86d0c22895e5e343cfd88e227928957c3cdf12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2194151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fabadc34dd42675bff58de9847fa1f3a9419fadd324a8f2c718fede6a31f9f4`

```dockerfile
```

-	Layers:
	-	`sha256:debb8aec244e6fddc5f06e11795a7df7ae03d76b7be7623cc013d77522432b55`  
		Last Modified: Wed, 02 Jul 2025 03:36:27 GMT  
		Size: 2.2 MB (2189237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99c47513edf56aa9ecf234facfcba31911f2bff853d3e6b1e0286dd36463526a`  
		Last Modified: Wed, 02 Jul 2025 03:36:28 GMT  
		Size: 4.9 KB (4914 bytes)  
		MIME: application/vnd.in-toto+json

## `oraclelinux:9-slim-fips`

```console
$ docker pull oraclelinux@sha256:c8138ad3921c1b7254961fde4e5965fec40ffb981fcaf1fb470b66f2619cff27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `oraclelinux:9-slim-fips` - linux; amd64

```console
$ docker pull oraclelinux@sha256:b22040313894b0aa85dbb1485b4c92f23986eb952eb41e9139e02dde43695c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49508332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07f75d322dc5f04b4fc3aac51a3a9229e88f3c3223c50cce6d1e56c89d744ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Jul 2025 18:39:37 GMT
ADD oraclelinux-9-slim-fips-amd64-rootfs.tar.xz / # buildkit
# Tue, 01 Jul 2025 18:39:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:199d1c6baa082a75c4f19651015a1341604c648e731b184ea68487bac9eb8ea2`  
		Last Modified: Tue, 01 Jul 2025 21:30:01 GMT  
		Size: 49.5 MB (49508332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:cfacbac37a4307b4d8e47cbdbfbbb1dbbec11c5c7e058881533c500ad5787903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bae7c2d395db0212e4af31d18d1829a2f2f154f90617543e85f9b521c36d903`

```dockerfile
```

-	Layers:
	-	`sha256:48cdd2ddf1ad50344372c0ac5bf492f713f53a09a0628a83ec3ea4b0383d781e`  
		Last Modified: Tue, 01 Jul 2025 21:36:32 GMT  
		Size: 2.2 MB (2198092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5874dc1adc91dd278b66923a717724b33dc7c377556f8ea8e896a579b0d84617`  
		Last Modified: Tue, 01 Jul 2025 21:36:33 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:9-slim-fips` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:f7547072182c3d232777759b1028f4344c533bf38521624e5be83b8ef59e54fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48083033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1c82af3e1561b2f41c723c3b8ef51e619b2c7c60c027a64e22a3a6cc9432ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Jul 2025 18:40:37 GMT
ADD oraclelinux-9-slim-fips-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 01 Jul 2025 18:40:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:abb769ea36547a69f13eb4b48d6f5e7d9efec831b2a88e19638e01f71deed1c9`  
		Last Modified: Wed, 02 Jul 2025 02:36:16 GMT  
		Size: 48.1 MB (48083033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:441331a6e1f2ef36a7cd38798b18f74aad33309f7336f4be96c542245c5c8e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5ebde3ab06e25227e76976ccf1ae87baa87d32da9032692c757272a7d6d9ab`

```dockerfile
```

-	Layers:
	-	`sha256:a2a7b1922c42923d00fd8ed02a108c57ca39c272dbaf60a4c8f13a0fe077c8c6`  
		Last Modified: Wed, 02 Jul 2025 03:36:30 GMT  
		Size: 2.2 MB (2197504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a96b6d0469b8c54a7f15ce19701973d1c1cf8194603da49246bcb3a057a2a945`  
		Last Modified: Wed, 02 Jul 2025 03:36:31 GMT  
		Size: 5.0 KB (4951 bytes)  
		MIME: application/vnd.in-toto+json
