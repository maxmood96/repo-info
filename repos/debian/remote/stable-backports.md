## `debian:stable-backports`

```console
$ docker pull debian@sha256:8033b57192fbba2bae0c5ccf477b0cfa7a2dd21c6395cee1701ecec07957b443
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:bd0d19d275ce2890db296a032d1f2a860ea2dee4deafe9e5cd336dc65318a0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49278504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3403bfef68e0161e8f5bed3952a528991bf73736270d52f990d5c070e48168f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:da0b5f91c7fa69571d66334a393ef7af7d8835b9b2063553bf1d6036a472cf64`  
		Last Modified: Tue, 12 Aug 2025 20:45:12 GMT  
		Size: 49.3 MB (49278282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cc8915ad3a9018f0641d9b32fc89a984a1f398779825dc5cffc11bc05ecdbf`  
		Last Modified: Tue, 12 Aug 2025 21:11:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e41e62d0f6dc8d4fe8f17590548af6bce892c12197a000dd35e9167246203f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b71603890c6ce858ad308d044980170a0adb8e6cb76623592b243191ab24692`

```dockerfile
```

-	Layers:
	-	`sha256:ff9d9691021d56f4484a95b54ec434dbf917dd8f85ffe94b89f98afd22b6f4ec`  
		Last Modified: Tue, 12 Aug 2025 21:28:32 GMT  
		Size: 3.2 MB (3168489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f363db57b05a30c9340b768b58ac9a64c423da4ef8f4d27196157f9d8fae8c0d`  
		Last Modified: Tue, 12 Aug 2025 21:28:33 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:45566ceb585dd5de7585f1c0739212aa81d91bb827e39203621523bc23175f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47442646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdd91f9919c20ea12ba62ec7cb9349473d7e733d61c700e6f9bda67896971da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6ba1443883422879077e2c4e37d25ad1c1fc308144ff7049b06ae99afd7b5c0f`  
		Last Modified: Tue, 12 Aug 2025 20:47:38 GMT  
		Size: 47.4 MB (47442424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9436a435f583446d73674777770bb317e67b850d9fd0af543d2d52f8c2f9191`  
		Last Modified: Tue, 12 Aug 2025 21:11:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:45270d3760d00055283ef32a6fe384b772f2d1cac4168134c40132d986b17f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277d3ec4eb826ab18ff2d048313125dbecf1ae9b28fabecf8b67584ea95ae894`

```dockerfile
```

-	Layers:
	-	`sha256:6ddcf7e500ce17dae0e39877e84ecae6871ab86194009f94454469c566f7ca9e`  
		Last Modified: Tue, 12 Aug 2025 21:28:37 GMT  
		Size: 3.2 MB (3171426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3f7a5c14a3ca34351567a9042ddb5c232c5bb496401f2039c63c3eba0057d6`  
		Last Modified: Tue, 12 Aug 2025 21:28:38 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:25f886e367e8e3dd167f0c3ce71a16424bc9f7d2de8fcce14b1ec366f0d9bcde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b5c9fc0cae894d644f6739e9aa5c1a2b56c70b62b2d2785882a8e2af2675d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9ddef5e918ef5637736328a4b0ef7d11249ebdd473c842da7c9a7232740f6dbf`  
		Last Modified: Tue, 12 Aug 2025 22:10:56 GMT  
		Size: 45.7 MB (45712629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b2467877e11adb495d77e7be86993ee4ee554865b2080414ba4750fb0a7334`  
		Last Modified: Tue, 12 Aug 2025 21:11:08 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:60034a5e6b1e2d08d69f1155e8b4d44334d94d6d31dd0a87f7feb445d79517f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61b43e0c72a9d2141a4f1171b057c6a766dedbec727349d3458ce4cddb80d52`

```dockerfile
```

-	Layers:
	-	`sha256:1363c46e87e61e5b820a72e74c716ec65e386fd8e99386d9629412d5bedd92f1`  
		Last Modified: Tue, 12 Aug 2025 21:28:43 GMT  
		Size: 3.2 MB (3169863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c08761271d5265aa8e037d5f48760ca5aacba586657fbd12b000ee87e850db0`  
		Last Modified: Tue, 12 Aug 2025 21:28:44 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a35bcca1a98affd1981176ae0aa9b08b56339a89b9ff0f5e7cca2625b6ceb127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49641828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f8cdfb2ddd45c4cae6951b5b191d09dbc57f1d6e852e6ca17ed7c2560a8b50`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2845d6002412d66b90e25b0053e7006768a0767644d69ca1c3b151ac64e01370`  
		Last Modified: Tue, 12 Aug 2025 22:11:09 GMT  
		Size: 49.6 MB (49641606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2713f99db28c8aaf6cc00a2d0fea2224b3e4a14c5aeeb0a81dcd5ef6a66e8a`  
		Last Modified: Wed, 13 Aug 2025 01:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4eadfc0fdc5eeeb821aef5a7ded527eeb362bee24d7b6d20dac9b4af5058aee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfbcb77ffe287b45d466b1dbb71c076872aa38d357e221e5bf3cdd23e8cb09b`

```dockerfile
```

-	Layers:
	-	`sha256:f2224831a520e5357cb42d68933756078a4ef728074cce2e646f8a48f98f0ab7`  
		Last Modified: Wed, 13 Aug 2025 03:25:20 GMT  
		Size: 3.2 MB (3169970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c643763e4b277e2fdfe82c42f6e9523ca94f620d63976023b66e5299cfd7e9e`  
		Last Modified: Wed, 13 Aug 2025 03:25:21 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:3056d4ec27a1b45c550bd2448a3aa3dbf5cdcd4d923310749ab5ee7d2a6e30c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50794481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726860c76953efc33851391c423ddfc06aef8a7de4da75fed36d62146fcd3cc1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:77d025dd6d525a7756aea06c40276326653d2e6f226a6cc79c78a470fc98b152`  
		Last Modified: Tue, 12 Aug 2025 20:45:01 GMT  
		Size: 50.8 MB (50794259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe56f5b382d742ef46b8f249d905873da28423a7d217464102faf5bdbf8367c0`  
		Last Modified: Tue, 12 Aug 2025 21:10:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d2130ab483259cbcd3e1236c67566aefdbd841ecf7d87c684136a2b7d257834d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15940b23d4edf2f66acd60ea6f7bf492f593447f7c51b321ea31e2bfb12b9b6c`

```dockerfile
```

-	Layers:
	-	`sha256:a1cf4c9a0b378994997108b54c766797d1dcf30420817a79537fec27b6892982`  
		Last Modified: Tue, 12 Aug 2025 21:28:53 GMT  
		Size: 3.2 MB (3165692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63dc7628638e19345c02481220c37786fa83684c676ccc18432248133a4e7b40`  
		Last Modified: Tue, 12 Aug 2025 21:28:54 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a05cb3b86b4abf20da938c951d3638083f1fde4b7a34be37c01da83890bbee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53103604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b29257c79e026f20d453b53ab3d8829c0a120825307e33250def6fef463ed80`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b142050848278803972c27b306ec85402b4ba66d59b412cdbb4fd62871cee469`  
		Last Modified: Tue, 12 Aug 2025 23:10:08 GMT  
		Size: 53.1 MB (53103381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732ca9ecd41574e0827a5678d79b33cbc2dae0a90c9a32ad06663c6834c6cc3b`  
		Last Modified: Wed, 13 Aug 2025 04:33:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d1fdab9557a61d1739e217ddd18bd0bbf346b46cb1ef80306b4b28f85866b9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc751dfa90a1fec0480df35481c89913f86f2598bb487b7ae8cd38b4d8db4ff`

```dockerfile
```

-	Layers:
	-	`sha256:022d8fb172813cdb3499c251d80c576e2c10c4f072225315657ca6e927c1087b`  
		Last Modified: Wed, 13 Aug 2025 06:24:52 GMT  
		Size: 3.2 MB (3172000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c59daa69cd5e26895cd81f1ced2704d509c2552756ce4e6c4263f6bfbe60b8`  
		Last Modified: Wed, 13 Aug 2025 06:24:53 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:73eff327a800783b9c944edb49ae9c41b221faa6ae848370c6e045ef4088102b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47764527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7a4ecbb8d6aeac813bffa0a620a987ee7d58f33559fdfe6102b4bc71b2896d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d3e2263364f38b7c5adbd0cec8377100e13ae4288dae026bc1360600669e44f3`  
		Last Modified: Wed, 13 Aug 2025 01:06:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf412212b715cf4fe28632d0baf548d063335f9c2120065740b0d1d2bc4e5bbf`  
		Last Modified: Wed, 13 Aug 2025 07:41:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:36ab098b57db7f6c2c78b2454d4f84726ae8a0b8e0550bbffb637af7fc726a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a37940182633267fc40eb4aa261cc0fc1177146e4682149c5cd8ede3182417d`

```dockerfile
```

-	Layers:
	-	`sha256:e8c8671d07b5fe4f592f4a762e68415d0c0ab4972fa2b94ebea6c52d1d035a6e`  
		Last Modified: Wed, 13 Aug 2025 09:24:53 GMT  
		Size: 3.2 MB (3160812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d09a9b5e0401e80cd84f8fd6b28355950e08b7cd1ee225f02d6a103a2d173a8b`  
		Last Modified: Wed, 13 Aug 2025 09:24:53 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:03bdc7b4fd335188666acfcfdf97cd0e446369e6ae99daec5e7679b1b429adbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49345384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee3f5d7b46721d6c1ed779bc73f8320ae263e9d0bbf0990702873af997de33c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2e0b7fc0414e1b20b90273c120c3c1d2d13aad6806e397db4a916b8d16d8dc98`  
		Last Modified: Tue, 12 Aug 2025 20:57:17 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2b349baffd3bf76bacf32cf9639bac978ff2a1bdea9fa428d6a4dce3f2650b`  
		Last Modified: Tue, 12 Aug 2025 23:13:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:12227723cc8e2556bc053b40214a3a55af5294cf17d6f522b820bfae6e922123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb36056c9b6ccfa1ba29c8bc65b4114beb6f3570b87c0cbedd622ae4fbf07c86`

```dockerfile
```

-	Layers:
	-	`sha256:77efbeab27d48e50a9ef2ab647e524d4a690ae8bf1ed0ded107a74ca68b1d4b9`  
		Last Modified: Wed, 13 Aug 2025 00:26:52 GMT  
		Size: 3.2 MB (3169936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a8fa5b54f512365f462689da953a9e71cec61670efa367f06f4202ce4576dc2`  
		Last Modified: Wed, 13 Aug 2025 00:26:53 GMT  
		Size: 5.8 KB (5825 bytes)  
		MIME: application/vnd.in-toto+json
