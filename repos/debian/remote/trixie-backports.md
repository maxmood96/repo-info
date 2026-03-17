## `debian:trixie-backports`

```console
$ docker pull debian@sha256:a904e0134f0124edf3e4b36f532db50a29b493bdf5e8c65631788cd710dfb0b5
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:64d07f4d479ca123573e20efda3b7e314ed56b8fd22f51d8a45b4f1e463c0f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49297753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e7db1328db84508b22da08529c1275f6327f2b6c2bac2ef21c0d241f76ff22`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:16:25 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87eb39c06f6c160503a3a65dec5c26b4437aa81c0659c0074c1b3a3fc815b65`  
		Last Modified: Mon, 16 Mar 2026 22:16:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:77dc3cbbb1d63ed9bbd36b14e989e4c97dc8162b90bfcc94673be52019e90418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11842ea8b5ca0ac08757e76915b4aebc973c9cb2800d2845487ee31af8efa8d4`

```dockerfile
```

-	Layers:
	-	`sha256:a2494d2ec7709cbac8b8ef7e8baa3beeb4a6f0abe78f44f70ddd212d95cc8b8c`  
		Last Modified: Mon, 16 Mar 2026 22:16:31 GMT  
		Size: 3.2 MB (3170913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd63365e68d33fab7bb9e74c684bb142af39a1d6560c0531e5e1b527d3264f43`  
		Last Modified: Mon, 16 Mar 2026 22:16:31 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e8aee2c7c6fc5cd9e4e4ab925613e58be3089edcdfd2e02e54c409c248f154e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47460835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5037151188bc82b65c9fa78da58a15e1bc6fe85b20d6c871af76b0bd9196e4b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:16:12 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8524aea9c07f7c3a1779bfcb961bdcea323ac7abd571c794a134ffeb31a825be`  
		Last Modified: Mon, 16 Mar 2026 21:52:54 GMT  
		Size: 47.5 MB (47460612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c4c5ac1a3fea3684cc9d20dc34d5600248da7fdf61fdab389af143d4617453`  
		Last Modified: Mon, 16 Mar 2026 22:16:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:38b674ab8fb93844a29190e31b9d4210316a9c9bbbf80518bfa65a6feac55f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c0d73ed750a6c21751b9b6ef348a10765d9798f1b538f28c35d729e9776d00`

```dockerfile
```

-	Layers:
	-	`sha256:cb2b682e83d285a66bb954a0356b7e53f24734888228e76a4d1818a740527b21`  
		Last Modified: Mon, 16 Mar 2026 22:16:19 GMT  
		Size: 3.2 MB (3173850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6384259d101430c4e96af39094b851009d98467fa45894e854baf9913a659e6`  
		Last Modified: Mon, 16 Mar 2026 22:16:19 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4262fcb9b64f0fcf43b4d51e3ddb469e733d249ffd954cf5febbd42d150ec746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45732871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340acdd177d01c2681b101a05c4c28f41bcd62b158474fe5f94e15a885a03062`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:16:01 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:83d3fd32d825865515469d080b5a8d89e630e2ed8f99a18d7b80d9c437631ab6`  
		Last Modified: Mon, 16 Mar 2026 21:53:25 GMT  
		Size: 45.7 MB (45732648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c9767adc70d21facdc853170af17a75e3e12b67eadabddea1ed9cebc972ef7`  
		Last Modified: Mon, 16 Mar 2026 22:16:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2282c766d245cd184d902a4f7645d248bb0cfa7c6976b74885ecf05a5f0619fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee62f6f8cc63c4fdd7778f815210aa16768b113fa304ab91e0f8d5ed4af7e31`

```dockerfile
```

-	Layers:
	-	`sha256:16dd0ec4bb1c1d4e02e282e7ec72613eabe6dbf8eeb52bb471080369a0d8ed6d`  
		Last Modified: Mon, 16 Mar 2026 22:16:08 GMT  
		Size: 3.2 MB (3172287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c23191468ba28fdb60f80db7744c61687eca7e225f268490f6c29abe15b664`  
		Last Modified: Mon, 16 Mar 2026 22:16:08 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:24799b0c64d89cd17ec29f68c7be00ff7d5715e63da3cfdedeb899b4c3187388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49665176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6c9b3853efb4a763b2906f31f6bc38af97b2d0104e4f57d3a05b91128ec6ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:15:47 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fc3c1d527dd3e59703284907387dadf237265612dca32f55fd0fa61e64414f`  
		Last Modified: Mon, 16 Mar 2026 22:15:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7759e20a1c19f524726dc024adfef40cf6960ad94369fda84ca50cb6cc4dacab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef758ae0a6bc49e21e6fb9cb02a3add5fa07d4725f27a2cfd17cfa80f0de69bc`

```dockerfile
```

-	Layers:
	-	`sha256:e49f51ae2934cbae0741f84d930cffd3cf63e80c736b85fd4fdfae2acf3e7a21`  
		Last Modified: Mon, 16 Mar 2026 22:15:53 GMT  
		Size: 3.2 MB (3172394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86bee5a7e8432ea87f525d331f624cda7516bc19d2ea87a0ed71986ec625462d`  
		Last Modified: Mon, 16 Mar 2026 22:15:53 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:b3b58c9b0ae08b4d608c90fa37b9d4bb8e9612b6ba12914a613ff9ca94505958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50819016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd35f79127b978cc0f9be62e6b27472565c8b8e0ee51733d888ed0cc03f22c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:14 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30659ebf539853e2f3478ae56eb7a781ac539c4cd7a552b1f3ca62df68a021c2`  
		Last Modified: Mon, 16 Mar 2026 22:19:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7ed577ac13f944a42a0e5c45f0d4a6ed154cedbe525701a73859eeb2b25ede11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ceb9d8ab1b161d641d7527d04de97d12a20c48a125b0fec9b5a7a599b4bbee6`

```dockerfile
```

-	Layers:
	-	`sha256:5f78090b18145681e9f6af965abd7707024cc8d1f0d1e22ab52bd842803c3ab1`  
		Last Modified: Mon, 16 Mar 2026 22:19:20 GMT  
		Size: 3.2 MB (3168115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bfac5a7c4683cc91b7d1a36d5f523b4a0a7be7f883fa2299e501c1dfca80c7d`  
		Last Modified: Mon, 16 Mar 2026 22:19:20 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4a8776610deb24c25f26e1c1929a1cb7c4eee9bca1453a777bf80ef0aac21cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53118572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b8c69e3939254cff3e73b6199b3b85d6f6c34cc94f459b1b3f573ac7292ffc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:34:50 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527d311d67725f5ee1801828f9dbc3aea04e2e1214bc1bf9316f150bac025f76`  
		Last Modified: Mon, 16 Mar 2026 23:35:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d69058b447ee9828125f98de1dc87cb6ed70eca6fa606f90b4d69e49758bed5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f80e8716c6683e772025bfb2ac96ff17355bad54ada1dcf0dae487708e8fe9c`

```dockerfile
```

-	Layers:
	-	`sha256:eba4c037d67b311a3ee025aa648c43a72622f6376a29945bb4fe3c8816352b8e`  
		Last Modified: Mon, 16 Mar 2026 23:35:02 GMT  
		Size: 3.2 MB (3174426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e83dffae326aec799d79e8444e918915e001351eed81a33fd47f91f9e326194f`  
		Last Modified: Mon, 16 Mar 2026 23:35:02 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:4820782f4ee089e073d5e2c69a2968f91d1beb57b55e1727b3fa77d9cf7cf938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47792550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a168edcf761ca6f72f15681b83ee6f432fc90d0aca491ee1b7bd0dc63519f6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:51:27 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07f5c4b5761d9a087f961d508ce1ba3ac7cd037d645ebd493bab463e38c35e2`  
		Last Modified: Mon, 16 Mar 2026 22:52:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f8e8805a658be7fd0aab50ce38eaff462d8c521449c6348addd536911fc39699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c2b96a761ab19e284d068215f1562a01084ad5989e1d53e8afb24c311d8585`

```dockerfile
```

-	Layers:
	-	`sha256:c2a5d78aa19cd2743bd72781e5172ad64df910ed89aec1a42caa9c2df4b37317`  
		Last Modified: Mon, 16 Mar 2026 22:52:20 GMT  
		Size: 3.2 MB (3163238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0f2aa419320eec4d42a536d1e3bea63daecefe0dc22d8f67c111b3bfaaed447`  
		Last Modified: Mon, 16 Mar 2026 22:52:20 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:f1ff59f5d881543509b8f728bb85acfd28404c2ac7b392ca6ffe7fe09e44fe95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49364999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32eb19b20782fed39b3db143cd59c658321f22877fe0ea5eb0ef1b04bec86e59`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:15:57 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fbde1f6827c6d6412938da6a30e699c67249992c6524048e4bba62180491e6`  
		Last Modified: Mon, 16 Mar 2026 22:16:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:57eec45c77a26a3cd2b3378bc4d508fc11820524216dc2f958fbf51721f61667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbafec93e53b807c57627a6a668bbde694eadb74f94acefb205993d7bf146b6`

```dockerfile
```

-	Layers:
	-	`sha256:0e233e8acbd5b8e52900d72bf60130ef34cf1e4ee420509f1dac72ebb947d0ac`  
		Last Modified: Mon, 16 Mar 2026 22:16:09 GMT  
		Size: 3.2 MB (3172360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:000c91fee94909bc7742d4992bed29c3bfab1073593aefcb81750b09b71b536b`  
		Last Modified: Mon, 16 Mar 2026 22:16:09 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
