## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:90c406e1ad93be3cf1597b156d0319e6a3de75db73325002f4f7b6a1ff02f23f
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7c982be856bfc0cff0d27ff9fe889ad88a29489f448f5dd62a796a9e12bc85da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74944538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee08c980524618fbab6be50a473f7ac28eba325209bf04f9ea317e3c749d6df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ae98f004043a012f0510d52ebd3aeed58b2ae219d3cf2b62637290692c9fc8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de51aeb72dac2dc3f64c772f67a5cebaf05604eeaa2b384d4383093a9de3ec4f`

```dockerfile
```

-	Layers:
	-	`sha256:3c0a8323a4e5e7fc69882950e9faa143cc66a964f7f00a12cfb8ef3e6eb81769`  
		Last Modified: Tue, 19 May 2026 23:23:33 GMT  
		Size: 4.1 MB (4120029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d948b28229cbcf7abd3ba626014bea70979a60f811ad5e2fcca9f912c7ca6ef6`  
		Last Modified: Tue, 19 May 2026 23:23:33 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; arm variant v7

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:deda4b05dfa31ee17044689ef80c07d4740b84afdc51a58d562cb480343ec269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74697826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed6b4ee3f74490247753b33674c78a167e8f8f6259b81875837f11be4016539`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8bfc260abbc0b2efed08f8c06d8a7deab5f1c1ef8ad7c1cdd7cbc38487fbe405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d86b1678051f42d700f32e1ba733e70a3161ccd42fa5bae191607edebeaa6b1`

```dockerfile
```

-	Layers:
	-	`sha256:09795afd75f85fea62f49105b7e798ea1ca8e6baed1e6d00fc32fbc8a12e67bc`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 4.1 MB (4120934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3686744fbe1a824e444cc7d83b16e4d6cd34b66478a7ffaf6f243291c740ce5`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; ppc64le

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; riscv64

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:eaa2ddaf7af29394eb7ad68735f9d02fa849381fbe99a4574c178c6deabcbf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76184593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ba8cbe218bebf51afe2dabf6508b231675093272ff7fe1269f62ff94ffca55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a95ac44f164c9c275ab328d3f5219a9cee0e2be081ed2ce1bb7cb8135bd49f`  
		Last Modified: Wed, 20 May 2026 00:19:10 GMT  
		Size: 26.8 MB (26804813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5aa32508dd3ed932a1d67b8a8522b46822f7ecee34528c69934d90e35e2e6d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d992ae19890c0d4545e53ea74365dc517bfae57aac2057502393e7272ce66b44`

```dockerfile
```

-	Layers:
	-	`sha256:3e0890b5577b972bc7c1f579c58d865cc3a5d9b2e53e367a4e6b6684aaabe1cc`  
		Last Modified: Wed, 20 May 2026 00:19:09 GMT  
		Size: 4.1 MB (4121439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b46da07ce03abe69f044f2bd635f90dc159f009e3cfd668710a71a453177252a`  
		Last Modified: Wed, 20 May 2026 00:19:09 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
