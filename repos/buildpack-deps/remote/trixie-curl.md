## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:93f6ced02cc2d7040790663335eaeb7fa2a28384d849c2db9c17e7471f0224f1
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
$ docker pull buildpack-deps@sha256:7f0c5f5b15c39ccc5c3a013d4af32f7891db71f3e1f74d79ba08d14f6ad85d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74952294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf9f21a3885c9141672418247d340a911829ee1ccfd2c43ca73f505bf587ac3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b365b6ff7b7e310e1b9a88f996e65b89969c7fa450492b68249d1d1c38e0676`  
		Last Modified: Thu, 11 Jun 2026 00:42:51 GMT  
		Size: 25.6 MB (25635173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f96ac6730a7fb0f2e51b2a6ccf7e60ca4af05ea0bcdb6cba8840eeb4da8c28ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38047f9c2bea440fd33d2a9fec2162af246447f93159991a8e5235d58e03cc2`

```dockerfile
```

-	Layers:
	-	`sha256:808e13126e7569401f5d480b50475ab9e426dce0dcb7ed63daff315c9bda3c6c`  
		Last Modified: Thu, 11 Jun 2026 00:42:49 GMT  
		Size: 4.1 MB (4120137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a2b658ba8404a8536044259f395f14ab49155644e116e419a1c26455f93bec`  
		Last Modified: Thu, 11 Jun 2026 00:42:49 GMT  
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
$ docker pull buildpack-deps@sha256:f0ee60f09b21b397638b844a7e6245842dea632eb64636843bd702abb3a9a266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74705080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a4ce75baa15c0ffea163be8b7c8522ccf09c18f6b5f4aa9d20b7f764c5a4c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ab02859108b91c1c26f2badd015b5215eb066b7ef4f3a22bd1536a8debe96`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 25.0 MB (25026911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0f62fb37f3b0346e0b6656f3c22afbda5030fcfa605a2963ab50c12543758ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bca7c103f9effa81136769e3a7585aadce2c8384d002e895f2a14f40f9b018`

```dockerfile
```

-	Layers:
	-	`sha256:e6611d88af4c264de0e7834868d003b5cf284994c5c5876a6634a49cdc035901`  
		Last Modified: Thu, 11 Jun 2026 00:44:31 GMT  
		Size: 4.1 MB (4121042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196e58fc654d64241cb8edb9a03d43d09535f276dea9c5cbd1b53a47c6095a5a`  
		Last Modified: Thu, 11 Jun 2026 00:44:31 GMT  
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
$ docker pull buildpack-deps@sha256:5913d58d59ddae2319066f2dd346b4422e77283180426cf584910458247819fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72762649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf970a831be66dc6c2814b55f491056281165dacb5f3d8725ba8ece5599e762`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:01:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e6afb0d9fe2fdfebacf2ccb9782fd129d9e416f637c13f72c2f0427e69c04c88`  
		Last Modified: Tue, 19 May 2026 23:49:54 GMT  
		Size: 47.8 MB (47796268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db76586e2d1a29e7feb120e0fcc7fa49e8df54823efd2e1b4e13ca0fe4ab60d`  
		Last Modified: Thu, 21 May 2026 14:02:51 GMT  
		Size: 25.0 MB (24966381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aeb89f7ca961a55689e67beceac412aa435cbb1b9d9c0c2366cf5bbd99e8f922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304edae774843d44b1e746650a46654885c2f5000600d1d169a26a7fb312497e`

```dockerfile
```

-	Layers:
	-	`sha256:38453c92ecc2cd0e5f4de5fe6a9f77f2432f78aa57fd2b83dce80a08bd558f13`  
		Last Modified: Thu, 21 May 2026 14:02:47 GMT  
		Size: 4.1 MB (4112541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca4950b1c8a9b454671a622ade0addccc4f83ff935e3a3be8829438bcc2bc4ad`  
		Last Modified: Thu, 21 May 2026 14:02:45 GMT  
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
