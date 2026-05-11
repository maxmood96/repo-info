## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:780228051f3889d5f599d337bb4fbd911fb8601f817db99cbd4e369811a507b0
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4c763f7116f6e78e91b053bbfb49d9df0f5f1ab2801a5240d782fd20bbf9c956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74925426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75d503c0adc0e061af04877d2c1c55317b6cecca1456927fece5cb5522a08c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:80d1f38485d9b7fbccd50b1adad34d99449b442287e8cfcd837f4d88368d06d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e6c184e415e38835a9cd10acbea38f4ec238fbc192fe50542bd595e1c88e98`

```dockerfile
```

-	Layers:
	-	`sha256:11353697ba25be4e7b8a9e446fed32a40cb97cdb72f4e6da8b8ccde65c8cf82a`  
		Last Modified: Fri, 08 May 2026 19:40:56 GMT  
		Size: 4.1 MB (4119951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd6e3dac59e6ec23e603ac9f4f46866c50f2b6d0deaf35f62e9d575888d74c43`  
		Last Modified: Fri, 08 May 2026 19:40:56 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9c0ee0912e1d3e8eb9d5304edc70b1392681f2853d2352686fa3d9ee5be274c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71829946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580a61b304302126e02a013bb2d69853fb06aced5a986aa0c73a7ae9ff7c3fc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ab1ea4901b2e5ef4c23bc85e77bccd29b5e37409a6599c547024038487caa48a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 47.5 MB (47466292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2782236aac3a37777665c4737690456903e8f45d5d8a06d88dfd8fdb29da5876`  
		Last Modified: Fri, 08 May 2026 20:57:34 GMT  
		Size: 24.4 MB (24363654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c6cae2cbac5b16829602b5dded8c21695b2f66bc4ff135db84627b4f092fb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00507a83d3af7500aa7b66caae8749e1365a1b2674efd12c7ea635d88fc2302`

```dockerfile
```

-	Layers:
	-	`sha256:46d9a952ea56dc3dffd87a0a448bb09f0409bb18aa4a373830ba785aa1ce861b`  
		Last Modified: Fri, 08 May 2026 20:57:34 GMT  
		Size: 4.1 MB (4122941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd4470995933da8f5102ddbc3aab4f476449ac532a66457f92543eb6650edb6`  
		Last Modified: Fri, 08 May 2026 20:57:33 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8f4cc972147c179e63c895fe1a0ff997f246bb30bc6480cddeba4e216b95102c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69374838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb02990ce30db533287aca08e55153a0de3705516c67801bc69eab9fbc77fee9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:54e91da80876b5fdcd3d8cbdf1cebc52bdf513f8a587b419fa82f5fb473a2b30`  
		Last Modified: Fri, 08 May 2026 18:37:56 GMT  
		Size: 45.7 MB (45738425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa31143502952cbe5df185dc297d98ec2482b596177bb3d2884695855e7091f1`  
		Last Modified: Fri, 08 May 2026 19:45:06 GMT  
		Size: 23.6 MB (23636413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c4d1e90a4238bb6f4cb4826d28fcc1da122d16ad211995bf99649980a2337d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0760759d132f2142c3085e940406f2e03657fc06bb5569de9050a76948dfce21`

```dockerfile
```

-	Layers:
	-	`sha256:b519489f69671c1816079cdfa95fb3324288b7851dacaa0b2748492d66b772c4`  
		Last Modified: Fri, 08 May 2026 19:45:06 GMT  
		Size: 4.1 MB (4121452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81fb4133f88e6427515736ae41e669352cfab9f07ff3f7851796028bcfee60fa`  
		Last Modified: Fri, 08 May 2026 19:45:05 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d7036c90a342109bf3add851e050ef41bcb9e1becb818eaf29c0b3c14de86b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74692921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd7a7604864dc81c1b2a47b98c87e8a1eaf8002668d0169ef06f7e21d175367`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c082919fe4a5042e65713a7cc29c769140673e486308fb73a8330b0a8a379a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa04ab33ee0bc22d2a28d22b9331fac32d0e3c19299a5cdd77e2332974a00013`

```dockerfile
```

-	Layers:
	-	`sha256:d7ff2775a2a14dc8c2a6680dc560ff8101a4c0134b01cf327be6e6e220010db8`  
		Last Modified: Fri, 08 May 2026 19:42:45 GMT  
		Size: 4.1 MB (4121493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5bf9f3cb2a8e4d3ab52bd7348eb26e124298e2149e193c4fd406fd5a965a79`  
		Last Modified: Fri, 08 May 2026 19:42:45 GMT  
		Size: 7.2 KB (7177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b3d5bd018399e13b8ccf1b0a0f27f046d0c088d75d072e13c9fa19d3c281edd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77610522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac03cfaf4c1f2b0521a17192970ff8b62337dd8918171247b94d48c005ec85b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802713bb4712073d4a0875914c45b85ffab64ce3389edccc50bbfe0147fa12db`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 26.8 MB (26784941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1352e4c3cfbcb303968bf7070b4909d37edf0dcb8e7dc4b5760e0ee0b4b5b47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff780b4f907f1774f6b267c0258e0106da58bf395252bfae318e15ff89d6fa33`

```dockerfile
```

-	Layers:
	-	`sha256:7c8bcc9dfef1152030d2d30d6773c3180b9f11cc5d64e28bd8ae9aaf6f58131b`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 4.1 MB (4117058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbdc890e439485cee1770e4227ddd9202df018a6646fee39f5ce1a4715cb8166`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d8a163936018c05cc3a51285db88495715542e914ce003cafe7df20a2473d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80137798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08101d6c17574be91108a0defd87b9ba9a3e7bef6b658b76859a15f610750d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0e7e07df0234f8192ac6b8d0fa0e09c4847b899e2e0718e39e5caccda09936`  
		Last Modified: Fri, 08 May 2026 22:32:23 GMT  
		Size: 27.0 MB (27014633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:79206fa7ca4e6abf2ba17b88b89610ac1eb90ad8c3a7bb31421231fd65f55bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7122a37e90b3e71154e98733627b43a9840a89bf018a3e03aa41f2b94acdd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f74ca52789e45780bc16dd2010e1f810a474cf5e198436ef8307c05df8c50fd5`  
		Last Modified: Fri, 08 May 2026 22:32:22 GMT  
		Size: 4.1 MB (4123799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f631625d5e0102dba7cf1a5bf96a1a13242fd6428da6492599bbb8fb6e6fe248`  
		Last Modified: Fri, 08 May 2026 22:32:22 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cbd1fffd9e4fe49a362985ed37d494d35cbe2fe57f06cde6019cb953cb322c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72754423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b15de08a3d50093949f288cfb76242c06dbac2982a869364476972c1c10b204`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 00:55:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16def90c932096937daf06d99b8e59a8b74b84aeebf2940aac17817b2f543a80`  
		Last Modified: Fri, 08 May 2026 20:37:07 GMT  
		Size: 47.8 MB (47798394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7692e383ad230da32926d42cfa98b11eb90f51caea79109b6a826b07b59addf`  
		Last Modified: Mon, 11 May 2026 00:57:03 GMT  
		Size: 25.0 MB (24956029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db2fea99e3f0b50c90dc1062c5f3a0311643c073f30e1ba5f63de0e494cdf5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae36807ac9edf86708570cc594bf9d7435197d9bd7831ff172b012abd5fdcaac`

```dockerfile
```

-	Layers:
	-	`sha256:290bc6504025062306f1d46f8435db360da1d39689bc12e50ea4048e91d85f84`  
		Last Modified: Mon, 11 May 2026 00:57:00 GMT  
		Size: 4.1 MB (4112463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f297edbe5a3dcc28697fb32de52f6d8cc2830d99c731d084ec818d2700418b68`  
		Last Modified: Mon, 11 May 2026 00:56:59 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cc88150e65b3870656792dfc7a2951d1cb49576485b025cd8ad15c06ec9c56be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76174943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a00df544a3f81ed1c695f9dbbfe6362f8328c05fb3ac21ae5821964be3f6203`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:54:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0445f3803885031cb22352d4abf0c173876f6316acd6230b59fe9c5654bfec7`  
		Last Modified: Fri, 08 May 2026 20:54:25 GMT  
		Size: 26.8 MB (26802639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:03631511be23e96a142f3cca871cb7a53a23d0d43eda330b439b1e903374d7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c28635af4151058ae3c3a3de2d4f2107f54a59caa7b87c99c650ac47195118`

```dockerfile
```

-	Layers:
	-	`sha256:984d95c87cb48d5fe266d642052b82f1b79d86ec9e1b428a1e9cc0c9a4a020b0`  
		Last Modified: Fri, 08 May 2026 20:54:25 GMT  
		Size: 4.1 MB (4121361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9276db64fbb71dcdaa0a86e11036bacb377165d4ddd013dd04de84c8dc4d6648`  
		Last Modified: Fri, 08 May 2026 20:54:25 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
