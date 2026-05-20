## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:c22e98275de6ea2ac1d03db81db0bd433dc5df29f1c16f823aa8f8fc5f00beac
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
$ docker pull buildpack-deps@sha256:1a4f7d33c5c7a08a65570e43df0cbf66f5ea95b2b334faef62a1b96f5cfd0046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142722270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ae4ccc29b57a20d2bb25630f77112d2793cd8c8520d7cf7a8c8cdd3eff2aac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0c7ac9897cc733a91be61e737989cf591871de3de99371523d813bcf3d4585de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbb4c8022e66f43a9b9b288d6562be0608d17c43e3a4e627f971479bbb21888`

```dockerfile
```

-	Layers:
	-	`sha256:dabca86899c51ac39a41e809379848df55656475f5cd0fde3927cf6fb91f42b0`  
		Last Modified: Wed, 20 May 2026 00:26:46 GMT  
		Size: 7.8 MB (7768415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98ea6333744cf198e8711afb90880d64436725c0eb8652133bcec755dffa1330`  
		Last Modified: Wed, 20 May 2026 00:26:45 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2e6cfb7b9f98034606e46bbf5bb539e48fdaf442446c99ecbb2cd559b1d61f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137190170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc75c7a7eb108a12d58b835cbe5df2c26816727895620b1266ed49dc937f498`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:c745eac201427a32c68c6433376345e418dca7bf01485c8f6ebcd45d9c6768fc`  
		Last Modified: Wed, 20 May 2026 01:18:34 GMT  
		Size: 65.3 MB (65335221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:693611b5631a1d9a7730eaf43ef273fd40cef144b2099c18ec6d1143c104958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2184e91bf0ca1df4bd95e1654f7f637106979cbcb342ab4cc52d46a7f2d289`

```dockerfile
```

-	Layers:
	-	`sha256:6d403e45303ffd90edbe51fe9014eb9f2e9ea41ab23f39e888fdb6168a276b1b`  
		Last Modified: Wed, 20 May 2026 01:18:33 GMT  
		Size: 7.8 MB (7769453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a74333b3ea9f0fcf2e2d4a92a123a59a1bd997353a5b1789d4b1369a96d5d4d`  
		Last Modified: Wed, 20 May 2026 01:18:32 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a64fb29cf7a30b1efc0b45d2546c2d04e408d67e9e77d4804229f174acdfa12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132121699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6800e8d0e27a93a014dc8246ce1d0138f3e179717878943d649a1a8473fddf4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:1279ada0eefe1ba158f90c1cefb9bda61c8de2e55c4f9c92965b87f7151a892d`  
		Last Modified: Wed, 20 May 2026 01:34:53 GMT  
		Size: 62.7 MB (62740413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b777b7736a8177375744719353d2d4f66013e7d16b1da42a1e7607365d4a49ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc21028ea863ca02c32b614299e27f88649d425907cf52690f60131cdd38fac3`

```dockerfile
```

-	Layers:
	-	`sha256:a9688751c50b976065c3f9196e0570693480506afd9848ddf16137c43d497547`  
		Last Modified: Wed, 20 May 2026 01:34:51 GMT  
		Size: 7.8 MB (7768922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76fb5a93b3bd0f217b3f43446667f58053e4f647ddcbd1c106c9d98e5f4e6a9`  
		Last Modified: Wed, 20 May 2026 01:34:50 GMT  
		Size: 7.6 KB (7648 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:03a4583b9bce0fa218a0167ec9208b7708dc0de192dd6e6451ef002970fd1bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142290675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688303730fa4a6acd3012c6125f4ce6c53d50ca2e05ce52589104bb00cb0fdc1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d4387de5f23db8f6ff5b84939fe5deffa02411199d479cac7387eab9e623d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d0d81c7ee031cdb83d3158aa28e3b4f18c99b09dc5b52303c6e87df936b438`

```dockerfile
```

-	Layers:
	-	`sha256:c3ba112a01f3599da177bb14f0f3af06adcd62b0c96b6b0953427ec25574dcdc`  
		Last Modified: Wed, 20 May 2026 00:27:50 GMT  
		Size: 7.8 MB (7775453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a5363f7070ff4c6fdffb0f2c2c4f106b6a77034b91c3ad79465f100056d8271`  
		Last Modified: Wed, 20 May 2026 00:27:50 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fee64da5574fd83e82e192e0e83a21a056944f6e43f7dad36f2ef24627fc6042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147449362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024758cd66c383a6cb59183717f6ed8b0c904f82ed25dd0c5e1ce8fe4edac922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:0d6db995dae312f4650e9596da7587e265fd6b48ac92ee4cf787e012233b3a9a`  
		Last Modified: Wed, 20 May 2026 02:45:55 GMT  
		Size: 69.8 MB (69824667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a393a772bca3e55b48a1da109e2bedb1d047ac97d3502d9f941f58e100c8a53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3177ccc6ecd219a42d83e8b24357025a4de066d29a3d4e61495d170b002e0371`

```dockerfile
```

-	Layers:
	-	`sha256:711caf1bd503309b26309a517000951502c30a249fba06f80d27c6f999aeaa7c`  
		Last Modified: Wed, 20 May 2026 02:45:54 GMT  
		Size: 7.8 MB (7764549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c7badfa40c9d771bb2a5c24ceda83b89d1617260fbdb51ac76e258d6fd0fa86`  
		Last Modified: Wed, 20 May 2026 02:45:53 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:07a9aeb22a7541b6c18264d14c8d3904bd696d7d108d9bad8b85ac09c7ccd12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153177546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8281861ce42aa545106289fe6d2ef6692dbc013cfda8cf89c38b0e6c6908ac6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 03:28:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:227313c51a1419e3870baa3444012fd55dfddc51f3e0064592c73f0b1336a3d0`  
		Last Modified: Sat, 09 May 2026 03:29:25 GMT  
		Size: 73.0 MB (73039748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:964a74ccb0c9c0484b93d4439f6ac1152a58ea8183f1541b71976d484eb9dbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f743fb35dda46991eef05c6b6a4ae18e7a84063630fa74a54cff0ae4dd1d332`

```dockerfile
```

-	Layers:
	-	`sha256:d96fad5c27f68161a40bf6040c6829fc2a50fb418215af24b86693232ee872ea`  
		Last Modified: Sat, 09 May 2026 03:29:23 GMT  
		Size: 7.8 MB (7775390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f9853f45b5a6e9e853288bc4c1e627b61fe7649b4650b4a976dec6102252eb0`  
		Last Modified: Sat, 09 May 2026 03:29:22 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ac445d6c7f810a61574046754daf94374d11a1d68e12c59be0541d6f1db2d37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139417932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606f3ca29746ee6674b219c79569727deb067b2553df01a30051a2ae19d6ae71`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 00:55:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:48:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:04052f76d54a3689ae0d16f104df08fec9ed091da2d2a2abc27589c5c3d933e7`  
		Last Modified: Tue, 12 May 2026 00:51:38 GMT  
		Size: 66.7 MB (66663509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:59b59d99cdcd28ef564b305a3d79c38439dc0336952f430235090586030d6cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9459bc85c89bb5a80be077a17ed14e1bb988b676e58e00052e7ecdf130059d1`

```dockerfile
```

-	Layers:
	-	`sha256:7486cb668c4b72a7c6ff61959415d2f2350717b6cbcf05e07d0b1639c1286886`  
		Last Modified: Tue, 12 May 2026 00:51:29 GMT  
		Size: 7.8 MB (7758103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b131b389479e6b00c5ba1bd26f521ad4b7ece4d538ba38a94fee4d6767fc87`  
		Last Modified: Tue, 12 May 2026 00:51:26 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:04f72540929f00e38afc97427dfc01236beaced360015d7478e0bd2163602fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144822644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611819ba580e91b04f7df402c7097de26c21b9801199ed0740a71b400044317d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:7ab366c3de62691a29444d50ed3d26e9d7524b8314a9b46521cbec555e978032`  
		Last Modified: Wed, 20 May 2026 02:06:37 GMT  
		Size: 68.6 MB (68638051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:af12bd247abdd3282628a2eca8a16fca02055ff858cd9ea51699cb8746ef5086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4948dea0102c09ec8efdad021bccc160d0310f3a6033bcfec3f0efb2807809`

```dockerfile
```

-	Layers:
	-	`sha256:93f85625df0a5fe466111424a9d1a9a227daf6d503a8d07dd77427103b67d76f`  
		Last Modified: Wed, 20 May 2026 02:06:36 GMT  
		Size: 7.8 MB (7769328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fc42a2bb932a2235010e80e4f5989420691832dfd7da4c1aa3a01d685dfad0`  
		Last Modified: Wed, 20 May 2026 02:06:36 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
