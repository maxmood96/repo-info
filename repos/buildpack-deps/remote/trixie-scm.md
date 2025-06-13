## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:29d545843277a205c0e87b695b9159805e1453ab7d6ddfe97f36bc1e3a901b31
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
$ docker pull buildpack-deps@sha256:79daef2071bdf2d4226f35b93b620529698a6e060a78d02da184c91bdc406880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142515221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299b1a9775e51c8e28bd2650caeab9ab907fb4f7d86fa8ff23af87a1d551b019`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f807a61ec306a45196094c9a44cffbe9d5d5a283a87c6e5c2469748ac3a19da`  
		Last Modified: Wed, 11 Jun 2025 00:01:30 GMT  
		Size: 25.6 MB (25601492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902f581532859d9e82510a6be0d293f24d77d5efa5a66349c1e74f899cb0e711`  
		Last Modified: Wed, 11 Jun 2025 01:13:24 GMT  
		Size: 67.7 MB (67659870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d3d1a461545dc5c1c378086a04f270851e3698f758c6dfc4b648c9d0d3c18d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245d20733dc8336784f2667d13f3c61da0b9f3bf22f32402332e0324ddc6163c`

```dockerfile
```

-	Layers:
	-	`sha256:5913cbed498151f5d344b2f20dba5ecafe0bbdc9d15cf36497ad4c0b66489637`  
		Last Modified: Wed, 11 Jun 2025 04:21:30 GMT  
		Size: 7.8 MB (7754982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f5ddde65cb3b0c7c9cfbccc817ca271753e677aa1ff575d3b36901fc180f4f`  
		Last Modified: Wed, 11 Jun 2025 04:21:31 GMT  
		Size: 7.3 KB (7312 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e1c17601c7db3b428dd3852d2e5c17be23053dddf592499e3a78cdbcf87b6987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137129814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f3c27c3737f325db8b138b295556a3fef81b37a7cf7d321c9db03a4e5f8761`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0b3435ddf0421631c0396c34acfc4d54793f2c51e2a8b92677402c8f9e0513af`  
		Last Modified: Tue, 10 Jun 2025 22:50:33 GMT  
		Size: 47.4 MB (47445410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be3896271877b3e95aedbf07f86334bdb2f5374ed0d8dca30695208865ab49`  
		Last Modified: Wed, 11 Jun 2025 03:14:18 GMT  
		Size: 24.3 MB (24326796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae1d6b386d300f718bd8ac1ab335ab4f9b2054343e637522505e1fa47faa99`  
		Last Modified: Wed, 11 Jun 2025 06:36:03 GMT  
		Size: 65.4 MB (65357608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ee00059f1b43f415905067617772efdf9e0f8d2856d414aadee506402f1e1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d836240ea01281392acc945785924a4ed4f2b2efdae191f2cd4f2c242b6e3580`

```dockerfile
```

-	Layers:
	-	`sha256:f06855ada5b5ea27e82724ca8914e72b5d33c3d8a57f75eeaa9b545f147b0d38`  
		Last Modified: Wed, 11 Jun 2025 07:20:46 GMT  
		Size: 7.8 MB (7765265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2fe1ebb81dae16d044c7c4f214096fff61028993ccc01bcb07a95d15a4e2f22`  
		Last Modified: Wed, 11 Jun 2025 07:20:47 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:841b355943c276b2aaff5b15e583af715ea0b47f70bd539a06808735e98cb838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132073652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6de4f6d4f2f79663dc2b759e233df920b86748e143bc9cfc1c4046fe0a7e8ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6c3b2ac1d8de7f6b9efb67d4f8df7036728aec7a9268a04eebbdddea82d555f`  
		Last Modified: Wed, 11 Jun 2025 00:29:31 GMT  
		Size: 45.7 MB (45702045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b97e79d9850f63633fd52187a6c3a6855596f84e391aa2167c27363cd92c43`  
		Last Modified: Wed, 11 Jun 2025 12:02:56 GMT  
		Size: 23.6 MB (23599533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f0250cd76d089e47a026dd511a8391d815ac5e1cd3ef860f0d3c434d13a9d0`  
		Last Modified: Fri, 13 Jun 2025 23:07:15 GMT  
		Size: 62.8 MB (62772074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9cc2afe9fdab2071a2e63acb35f30fb85e7e375948b0a72fa8790ef86b6c4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e4eb8dc1f5c78e7b22712257ab418f69e5bb5abfcdd37dc249b1541c1ca80c`

```dockerfile
```

-	Layers:
	-	`sha256:b5bae8db5dbaf575234046f55cc8df5a2278303bd9ad09506d3a9bce736da0dc`  
		Last Modified: Wed, 11 Jun 2025 16:20:59 GMT  
		Size: 7.8 MB (7755481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180af898d9589b388127a74230c111288c2a07acae2bdee026fcce5d75903ead`  
		Last Modified: Wed, 11 Jun 2025 16:21:00 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bad77fbfaa0afed3274707150e38e74127a8cbc7c776e50b3ad79358902357b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142252242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed90169c3bf6544f01334a37cc9a158f1eb642c6286af8397f96a9f08865499`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439ee882f07f6b24af6e46850d9521759d30430f3be41cdca454de5566ec0ab`  
		Last Modified: Wed, 11 Jun 2025 02:57:26 GMT  
		Size: 25.0 MB (24994209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded0afb06efd2b7ed68e17cae5e6e1baaad41593041fa16eb9d856160e2bca6d`  
		Last Modified: Wed, 11 Jun 2025 10:34:07 GMT  
		Size: 67.6 MB (67636505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c49280d1021abc5433a892c68cbd12293cec650b21b72b3e1c835c7bfd6d0913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59817eaf15bb620d5fd1ecd08fce5f045a8d50aa1efdb3ccb8c74b8c87f9376`

```dockerfile
```

-	Layers:
	-	`sha256:d5a4b4d4196f5072c0b97b9facdf7a358f3ce71e6290e35b284a6b381f3c4d7b`  
		Last Modified: Wed, 11 Jun 2025 13:21:17 GMT  
		Size: 7.8 MB (7762645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:447dc6ca22798449377296f45fe3e9bce459931df1b4422290e22ec73bebdc73`  
		Last Modified: Wed, 11 Jun 2025 13:21:18 GMT  
		Size: 7.4 KB (7394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:df6a231c26e28faa637a816a7abd5fad58e7cdc71eb7fbf788f93552bdaa7b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147194631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e455297c717a923ebd1e9e6cad288bded8d34cd1f13797f10e669712545bc909`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f24aa3f80422a60637035cbe1e280f72c031e00f6d803abf75d114fc69f38e79`  
		Last Modified: Tue, 10 Jun 2025 23:26:07 GMT  
		Size: 50.8 MB (50765612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60bf3250137ff5f937387763b677cbdfc73f6e6d8cb191bcb236dadd350bc3`  
		Last Modified: Tue, 10 Jun 2025 23:59:18 GMT  
		Size: 26.8 MB (26755336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a68b17b2aedc3eec75668b4c1f6433dc6f26215d13bf5c707dfb14bb20bfb5`  
		Last Modified: Wed, 11 Jun 2025 01:14:27 GMT  
		Size: 69.7 MB (69673683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:346224e44ffec5e36a54b05c29e2a7b4398a950c111689fe63b128eb991a3b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7758420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264520819891e0d8c97ad51ec7b1fa4da8180a91119b54350bd21cc21f554571`

```dockerfile
```

-	Layers:
	-	`sha256:98d28c1b00fff0d7d28acefed4ff40501053d62d84f3f19b90cc9625258bc294`  
		Last Modified: Wed, 11 Jun 2025 04:22:02 GMT  
		Size: 7.8 MB (7751128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44352474a9f40068dbc3dc8d124ca8b292ff87ec8d1974de3df18c6fc0898375`  
		Last Modified: Wed, 11 Jun 2025 04:22:03 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:585d162716f32d7a29145a1c94981a682443067560a6272feae63f0a051cb8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153092829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3e9238cb27384c430dfd5f27a6594f5587cf9c2a489d4acdf1cfb2993b82dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:70a0e6b9f26ae2a311f0c79d7ff095922eec7e2aa39f94bd8c4e5b385cfa847d`  
		Last Modified: Tue, 10 Jun 2025 22:52:26 GMT  
		Size: 53.1 MB (53090933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e8d7ca19325e1e81102ab8668168b260e6e57b98b333eee8bca0ca1d7fb15d`  
		Last Modified: Wed, 11 Jun 2025 17:42:50 GMT  
		Size: 27.0 MB (26982398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1399fac31c7028d2f04582eb0c8d6877de851a1d1a0a7124a505b94c5460abb`  
		Last Modified: Wed, 11 Jun 2025 19:17:13 GMT  
		Size: 73.0 MB (73019498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:223811f8b186d028ba0decc75de7d50be01ce08af6f1c3fb367dd19931bd4658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1dfe62f4af343458bf404a363513f7645be474ae0eb6b578aedb7d80e96aa2`

```dockerfile
```

-	Layers:
	-	`sha256:abe538806022cceb2a6ed3dc880847fcd9ebdf1151c58066abdba76b39e0fd7b`  
		Last Modified: Wed, 11 Jun 2025 22:21:02 GMT  
		Size: 7.8 MB (7771340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ced01579a609ac4f1bd0bf03fd295ef7c8d14b044ef6e70ee3c7b29e8809c22`  
		Last Modified: Wed, 11 Jun 2025 22:21:03 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5701aeda166bf86471943fd1b3a67d580e1b3319dddf8524c92d12dd73d3478c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139362168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8646b73d1c2cdf98ff32a6d563e015466d84a197303367423f6f80c3870de8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:183a50217c4846c3775204631f79c9cba563face97fcc3de4421f000af401588`  
		Last Modified: Tue, 10 Jun 2025 22:56:31 GMT  
		Size: 47.7 MB (47743345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821f4f32e32d9aba20b46d2290a43e58210fbeadb10dd55306d3440511ee2020`  
		Last Modified: Tue, 10 Jun 2025 23:38:17 GMT  
		Size: 24.9 MB (24937037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231678d8f7c532f9f566704f742fa3592bcf30ef8ae6eb20175bf220b23e5902`  
		Last Modified: Wed, 11 Jun 2025 12:05:36 GMT  
		Size: 66.7 MB (66681786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:826e47f3f80d35bfcb09f13d870d975e1584f626fded230a2dc304ecf5c7a063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7752145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb38b278818750b47c291067dad5da99158df2f23307f62045b10f3622f6517`

```dockerfile
```

-	Layers:
	-	`sha256:d425dac311321ce2b3934c1e454d38a181b197b89da6f0f97ddd195d8d0e7978`  
		Last Modified: Wed, 11 Jun 2025 13:21:31 GMT  
		Size: 7.7 MB (7744800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:603fb404ae13a3ee1903d7dbbb08e095f2dd9d63f0b8c5908cb5da5072691b79`  
		Last Modified: Wed, 11 Jun 2025 13:21:32 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ac0d28bfa605d4559672e52a97490d6b7015997a9b71b03dd047986fd85381be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144781081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ade171a934602dcded3e1be22fb5c37ed015f4a52604b8f531c87226aca855b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ffa7429d410cb8e2162450d6c2fc3a21121304db16d73a6b9feaa05000dde5c`  
		Last Modified: Tue, 10 Jun 2025 22:53:14 GMT  
		Size: 49.3 MB (49329768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588affbec95a011eae8d19fbc59b872f3d6089f972f16713469d6820e2e3fe6f`  
		Last Modified: Wed, 11 Jun 2025 12:02:59 GMT  
		Size: 26.8 MB (26767425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a368896f3f74324a185b32673baa96c49954c4d84388e3238beb96d3b4ffc0`  
		Last Modified: Wed, 11 Jun 2025 07:22:09 GMT  
		Size: 68.7 MB (68683888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1983480893303636c883521a9e11e920c29ef82a4da3ef905bbc7efc5837aaa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e317252bd68a8f6892450cbfbbb7a46008f2ef2d0fc3f7ae1dd0adc4f3304bdb`

```dockerfile
```

-	Layers:
	-	`sha256:5a0d919d8f367404d852d302f46874d7f6858ce0cabd056bc3dd893d4c3cebae`  
		Last Modified: Wed, 11 Jun 2025 10:21:07 GMT  
		Size: 7.8 MB (7765148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f60a009b23c5f810df4070dbd3bd7cc1fd94af08587a2c0bcfbfbf53fa255c00`  
		Last Modified: Wed, 11 Jun 2025 10:21:08 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
