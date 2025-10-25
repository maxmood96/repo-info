## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:ea727422bb1da25898fbed3c13aa9f5aa3cf70903ec4de14621421adc7cca693
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fb5ffb7512537e0209daba60875bba321714921557f386476dedf39d71e5d03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142685373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdcd858f98f350a089fdb67b3e56468e6efe99952039ac85395a30181eee1c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d13c9e6e424c3218da6c4995313c6d7654ba5bd0c7f1d2445e00cf68e25cf52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833ee781794798a858a0c6cf8bb2a87b346709500c5d5aac5354613222a3a06d`

```dockerfile
```

-	Layers:
	-	`sha256:df8cb2c3ad9067d56ec50b7c412550b2b3876e396d4b6ed7f0a5b40eef4bc98a`  
		Last Modified: Tue, 21 Oct 2025 09:24:24 GMT  
		Size: 7.8 MB (7767050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32aebc3c6feea1e7ed615525ca7658eabab7016d5f4b882177400fa4cf151994`  
		Last Modified: Tue, 21 Oct 2025 09:24:25 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cbd2cb852c8704ddbc27bb17f6968c53082662372c6e0062189f5b125cc47945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137116319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2547a50d76a19c51ffec12c90e749e9d0ca53c11e6aeb26853838e2b6876061`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36e1dd9ce5730c29e323bfee77881b6b709a9ef3833ed3a509dabd626e23ef19`  
		Last Modified: Tue, 21 Oct 2025 00:20:35 GMT  
		Size: 47.4 MB (47448771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5aab8f083c99dfceb8649e1078e500b3226031e7fdab550eda596ce5b675db`  
		Last Modified: Tue, 21 Oct 2025 02:32:50 GMT  
		Size: 24.3 MB (24342547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a322d2ac28a78c43ffaa81483b3e7182f4b364130ce74f60ef2317ccf71493`  
		Last Modified: Tue, 21 Oct 2025 03:57:05 GMT  
		Size: 65.3 MB (65325001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c0d1701c51b62b7a69fb0ebcda37ca07bc2c53ace10badd5340a828b7632c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0510ea83903a48f17de5e8f16e52f6b86706c77ea524b17ea70523755ed0cafd`

```dockerfile
```

-	Layers:
	-	`sha256:7222734efeba70bedc9938afa979584a5274cd74f4e80d78ee1cdacff8ebd544`  
		Last Modified: Tue, 21 Oct 2025 07:21:20 GMT  
		Size: 7.8 MB (7768088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789438771b0cf9b890e11c19d61dddb83a3f4144f6fc0bcd600e39fbb9f1e6bd`  
		Last Modified: Tue, 21 Oct 2025 07:21:21 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:97ecafad04321113f2b7183396781824227d1b43994376917f6e08e480659c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132046560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a248340967c41d1a10d1b7dd5360541bffddab468081dbb97682ac05804053`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:efd7765e6822bb15378525628aa0b608eb21474f15252ee0d5f6811f0d9e6ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fef0df682348cdfc0704cd24d12cda2c649acfcdf99db7ebec39870fbab81f`

```dockerfile
```

-	Layers:
	-	`sha256:257dbe6343766f84aa165040443c6d40d20ae809eef6bf73c3cf29d9d3de1f56`  
		Last Modified: Tue, 21 Oct 2025 07:21:27 GMT  
		Size: 7.8 MB (7767557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b2bd78e910f0ac470b6b1eac86c373f9250b52d8f35142e4a65ea709ea0dfde`  
		Last Modified: Tue, 21 Oct 2025 07:21:28 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dcd445ca7571f42df1f9063735115a608338f277e8913cd74dc0bbe1720af077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142250315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f20bf0723ccc70a9e29c4d498eeb32dd65ab757eb3479837b2e3cd7541ca02`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05f3f7d6effb24e1fdde39bc923b44723017160963abdb919561decc0b70685c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b7dccd87fdd05825973c318c23380f9b12c5b729f2534450287ba98cc1863f`

```dockerfile
```

-	Layers:
	-	`sha256:e56d071622d79c22abf27d1c1742d6331227b63b9c5d389670403711b83740d2`  
		Last Modified: Tue, 21 Oct 2025 08:24:10 GMT  
		Size: 7.8 MB (7774725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d4ac234f868f5d288b8368125a69119cd0cdfdfcfa11dc0c913c59b087dfc05`  
		Last Modified: Tue, 21 Oct 2025 08:24:11 GMT  
		Size: 7.7 KB (7712 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:96b2fa9be6f46cd88e1b9207d968c964ed79d57b90b8c5d4a618fec63fb7eb1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147371292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be8c68bc6a87105435fb38c9247899faa259685f400c74ab3ad83066ff46e08`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e26cd0a52ed92f957fc3cc05893f4f7f60e4f7a73127856e36081fef679ee28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e953c7a502f74135ebb5c97a2ace6be08700dc62a4420abac2aac0c714756900`

```dockerfile
```

-	Layers:
	-	`sha256:671ea72610ce82dff3dedcd5edee8dee4b112b8fc3caf197e2b7ce1f2f9fb37c`  
		Last Modified: Tue, 21 Oct 2025 10:22:21 GMT  
		Size: 7.8 MB (7763185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee6a59edbe201a62058bbb559288f062d3df4944f71fba34e27c19114e86536`  
		Last Modified: Tue, 21 Oct 2025 10:22:22 GMT  
		Size: 7.6 KB (7593 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3d843c5b054d86b0ae2072a0aa7c5624f86e382eb266fe475c40260884c74d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153135368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b80614c8fa45528e2cc004b84225c8d1dcec0d63266288b03d438bcbdeb3c3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dfb88672cf0a942c4fdfcadf1912c35c9d30a3a001b18a9dad505fb960ae8`  
		Last Modified: Tue, 21 Oct 2025 07:47:00 GMT  
		Size: 27.0 MB (26996207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06029381e2f1b3a0885caf1b758b0461bfaf9db7b9642ca0b79ab28ed1dd4ecc`  
		Last Modified: Tue, 21 Oct 2025 17:35:58 GMT  
		Size: 73.0 MB (73029685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4871597e9e7cfecf8469d9bbc320ddffdc2fc43dc51f60b3296ba13960231bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e89b9495c6adffdefeb4751b3bbd1df704544002c979e27c58c0727b0790881`

```dockerfile
```

-	Layers:
	-	`sha256:589c03069d1d6372edbd1ea4950d57d0a3a57ba1cedb31411d690907f1e5be05`  
		Last Modified: Tue, 21 Oct 2025 19:20:46 GMT  
		Size: 7.8 MB (7774173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60412275fa31a71dfd01f825081c5e7ca04a36d18dc9a4a37c4a27103aad052e`  
		Last Modified: Tue, 21 Oct 2025 19:20:47 GMT  
		Size: 7.7 KB (7658 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d87a89f3ec977e572d06f6eba37a10c57497e51eb1bd363b741b1df36943a0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139386544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e594ff0d18dafbf92e81e01f41215158ab4e080333c11e2be34ba851f9702b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05bd658b6b88b72fcd0763d85f85d239e81655e6c5f5a33d4ae006af111afd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df2880ffedd1abdc9ea47b20067e8694d5c31dba96421fd891a621ad0eeff04`

```dockerfile
```

-	Layers:
	-	`sha256:c8fd5ff1f15beb51785c747c08ffc42fd59040a82f92f7b4f3ef8a6d1cd9b455`  
		Last Modified: Fri, 24 Oct 2025 22:20:26 GMT  
		Size: 7.8 MB (7756886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235bbb0d6fce496d9ae15f82e4d71956ea60990fce41397054289fde8911e24f`  
		Last Modified: Fri, 24 Oct 2025 22:20:27 GMT  
		Size: 7.7 KB (7658 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dd97f751d26f0fc8aea4751840ef6165faa9363addb66199bd426fbc8176f4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144765648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a379e2d580c1490ae60224d3655a00c49494cead0bca8ce4cbf923ea0b64fccd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7363509bdabaee507d788486430a67895cc266ce0b808959842f46de0bc92e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44a253cb1c6d35994addbd4b8eb06403a3982f0f2bd18ea3fef26efaf0ddd91`

```dockerfile
```

-	Layers:
	-	`sha256:9e782feec5ef538338ac3d315b9a647df87a78a854099dcd03263a6d7e0616cf`  
		Last Modified: Wed, 22 Oct 2025 01:21:11 GMT  
		Size: 7.8 MB (7767963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6430bd306930583d68f6d1a189ebe242a4be4f1a77c9656a4e6f77886413dfe0`  
		Last Modified: Wed, 22 Oct 2025 01:21:12 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.in-toto+json
