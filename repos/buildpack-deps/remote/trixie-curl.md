## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:544547d379b78b8bad05ba28fc1dba4e9cf27b2518a0d2c9c7b368ebea92672e
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

### `buildpack-deps:trixie-curl` - unknown; unknown

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

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8d62a73a1885e0dcf4d1b4aaa0eff7ad2b4c618d7bfba51af0ef24a281d1f9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71854949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffc5ec2472cbadea30eee75d6ac78ea45dc0cf88d9b0db70260538f64ddc582`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6cf4508cae9439867ef520e234c0d389bafbf206c9c5e0966546716701d698c7`  
		Last Modified: Tue, 19 May 2026 22:36:48 GMT  
		Size: 47.5 MB (47488046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6871af73fc616d35749cec51e37c29aed76ddcc86d20d7f1f669b8ff2967c7e`  
		Last Modified: Tue, 19 May 2026 23:56:54 GMT  
		Size: 24.4 MB (24366903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f374572dd142445d7cef9e0c16149c3792be48845fe3a6c3f6a6e5d98e563b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce009dc442fe00112cfb8f525e9ea54d42af24d32303bc476879bc64a1d76d0a`

```dockerfile
```

-	Layers:
	-	`sha256:6c464673a7b66d0ff665e77afd9dbcf2e3195bb368b7118af3220fb5465cf06e`  
		Last Modified: Tue, 19 May 2026 23:56:54 GMT  
		Size: 4.1 MB (4123019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0982f566a0b3ed0b03b989693567845426cf09368daa641b0755470897cdc8e`  
		Last Modified: Tue, 19 May 2026 23:56:54 GMT  
		Size: 7.2 KB (7157 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f6b64a326c36d494c23728664aa45205a11600189e8683ea76bb08984aabbfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69381286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a11836921de2d9c397e2ba5b72b6d2e8e01ff5855fc550ed3248fa4379ed7c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16329e57da118ecb493828b7b07e7a4228b11fef4bc65ec0fa8d7fc9fac39b62`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 45.7 MB (45742031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a203c225dd8522bdd8715f76203677e263257613c0c04e14fd9a434bee887dba`  
		Last Modified: Wed, 20 May 2026 00:04:36 GMT  
		Size: 23.6 MB (23639255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee7640d6120ee753879bec0aa3c4a12c5cdc108dc716c3807bfd9060f2ca9f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cc0cf3778dd17452153de61f21eb4262caf67f5283a0907a9a34d91c8a664a`

```dockerfile
```

-	Layers:
	-	`sha256:0d0b5123208c0161c1a102ed8df34944a69f15406d405b11c4c7e13e6c04b0ee`  
		Last Modified: Wed, 20 May 2026 00:04:35 GMT  
		Size: 4.1 MB (4121530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0b81a0416a7251bbf90d8c133a74ba3616961ea9aec5792f71d51c433f4b3fb`  
		Last Modified: Wed, 20 May 2026 00:04:35 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

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

### `buildpack-deps:trixie-curl` - unknown; unknown

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

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a6f0a61c3873931f9ba38877fad0a1be75c8207783c7058cc67445380e0444b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77624695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23427b3520ce2f26c9b39935c31595dd8342d98a6203cf7e4f49c7f945ff788`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7297938c03ac6ad4e53525c3e0002337292340d300a5508ffbc391176c4868ac`  
		Last Modified: Tue, 19 May 2026 23:25:38 GMT  
		Size: 26.8 MB (26795141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d66d0993fa9ed776e8baa2beba3026e3638a96efd10d9163dfadaba3be9bdbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a06dd12dc110186e0113bd5c761ad81f857b25af11e69a66e489b9b2225d838`

```dockerfile
```

-	Layers:
	-	`sha256:bb78d279b63645292a83f8aac8cc6217c61bca049106b8759dce17f04c67931e`  
		Last Modified: Tue, 19 May 2026 23:25:37 GMT  
		Size: 4.1 MB (4117136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45efb40f00db31966b4382b7022edbcf111221198417feb62c7951ed4734eb0a`  
		Last Modified: Tue, 19 May 2026 23:25:37 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4fbf6aabdfd84f45f8220ee7ba44979148b0a576b3dcd552d94d702f21bc2d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80153331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a72d64907ace1a3ef34fcda1e0def532084f22aa8891da65ac9ec21137b1ef4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:14:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743dcca676e80d0b7074d4f03820f8068053078d4942f2a921fdf172c62897ae`  
		Last Modified: Wed, 20 May 2026 01:14:53 GMT  
		Size: 27.0 MB (27021149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22ba2cf175e52cb6829be5cd5405a06ace39c1916dff17de907c0f5c2231e4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9956c41f3a8587b3609d11edfa51a4615725168ef1a25a0d52938ec75824c435`

```dockerfile
```

-	Layers:
	-	`sha256:678f5ff7251d7e3e416159bc3d3edebb33bcb7d920d9ef3d85c98fc0eb5a8aff`  
		Last Modified: Wed, 20 May 2026 01:14:52 GMT  
		Size: 4.1 MB (4123877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae63a6469bf57f9e96c5010a1d62c81ac7363517cdb9250030e58e839092408`  
		Last Modified: Wed, 20 May 2026 01:14:52 GMT  
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

### `buildpack-deps:trixie-curl` - unknown; unknown

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
