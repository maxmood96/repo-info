## `debian:trixie-backports`

```console
$ docker pull debian@sha256:76ea45eaafc4d4659232af42ad4ae5d0dbc2a048ec8e2ae7c78547e3eae90b37
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
$ docker pull debian@sha256:c8f2b5eb071968ad7f86f52052966587a659bf14ffd8aa1f3e1bb52505dbad1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49293176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71220c88179cea7aee801f9ef8d75371b0143ab796c255cb90efd659de5c4343`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:08 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0190c28b9e941691d0b19e5f5f2812ac2421a1a2639cd384a0bed04209415b`  
		Last Modified: Tue, 03 Feb 2026 02:16:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:90984fec8136babc6267198499306aa18b46c44bb7b88eaa53465665e3a57e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3a212b368748b57e1cfc3c92bc2ade61bf79cc29668fa3a805400b607fb241`

```dockerfile
```

-	Layers:
	-	`sha256:f195dfcb8559825aef49118e7a673193ff1c8912a2615584078c9ace7b85843e`  
		Last Modified: Tue, 03 Feb 2026 02:16:14 GMT  
		Size: 3.2 MB (3170877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13fff96955d7c25dd331c49acbe92735381ba056dc4bdb2a52573ca865b5dc1b`  
		Last Modified: Tue, 03 Feb 2026 02:16:14 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8143c0b9240ae9be8adfbdeb9bcda0777dddfabf5bb4f1e3be94861d136353ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47454221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8108e1568c105d0599320fa5206cafae09e0b2efa3cac3b8bfb9922baf35730`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:52 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ba31dc65cf53cae37b5517f251f4d408e91109de491cbd8816a9f21c33a05203`  
		Last Modified: Tue, 03 Feb 2026 01:14:09 GMT  
		Size: 47.5 MB (47453997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f4cc758b75dad698d8ff526648bda8d62ff994372b8ffb4aa67db5ce2c1032`  
		Last Modified: Tue, 03 Feb 2026 02:15:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1e22fd3ba83f7cc23d58ef2e3b6dd400cb80cb59c6af3f99a8a82b35472cb812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3005ca20e93ab1c240a7680aa396ebbb16263483931fa6ed961bfcd384f1634b`

```dockerfile
```

-	Layers:
	-	`sha256:c76e9bea7f72ec250e28118d8f981fc5039765e2fa0b46b607ece21804c2823a`  
		Last Modified: Tue, 03 Feb 2026 02:15:59 GMT  
		Size: 3.2 MB (3173814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c326ecd32654d1a6e005ae31ee26448c6e7732d509a0cf5257df0193978b6d8`  
		Last Modified: Tue, 03 Feb 2026 02:15:58 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d90720843f727530d6c05b19ce301a45a3da80763cf42cd6f9eabdf6372eed92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45718043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4f3c1c780dec2b6b63391995f99d814fc423b4088ab3c7e993344e7a2ec4a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:18:46 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190d21a6c208ecbc03b1b9627ee72db79c3c6bdbc0e8d70fac9310b8af020eac`  
		Last Modified: Tue, 13 Jan 2026 01:18:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c4b01270725afc4ea6072c3ab431443a338a5f6e9b5de5f0007d4d83b5edce2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13feebeb208e72b489883d638810099d0e999ab1ad9877e27721b8ff4fe29c8`

```dockerfile
```

-	Layers:
	-	`sha256:20d087651f8ebf202e12facd1ff4be65e345e21285cb65379310876c83885c18`  
		Last Modified: Tue, 13 Jan 2026 01:18:53 GMT  
		Size: 3.2 MB (3172251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4fae63d6b834de035c67b6e0609c479da456be5c29be659b04b82104b10c634`  
		Last Modified: Tue, 13 Jan 2026 01:18:53 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:369689a6dd2247f37459014e42c0b17a8c53d9de803e0cb527f1363fff7002b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49648306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ee929a053b8e0bad014135ba9aad7d187a37ec6a201b5a1ad2301edd4c8543`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:15:50 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1e7c6cc1374844538e1d37ad655524ad18ab1c1cf353e9b5dde33c625e2dc3`  
		Last Modified: Tue, 13 Jan 2026 01:15:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:86596924e6379e00b5b4b0f6b2c48dbb3f23baeeaf4976ca9f76435b61bbe804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a047d06fa0584cf8a5e7521ac634f46088f19852b664b25fccbcb9c6a03582`

```dockerfile
```

-	Layers:
	-	`sha256:2d7411656c9112ad9e929061c017299151349790271652e48ce5c7ddee6d6442`  
		Last Modified: Tue, 13 Jan 2026 01:15:58 GMT  
		Size: 3.2 MB (3172358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c558a1c75107aaf1811b30b5ef2f8ee9220f27f488dd4374ab4a024ee0c68f14`  
		Last Modified: Tue, 13 Jan 2026 01:15:57 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:10edc22c351109044d93b8abbbdd3c05dac7d6962199f6518d8dd3b3f13a2fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50799098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20772e5433182f55c48fe878e40c346c21d213c92e6b81e79f474155b63f4501`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:15 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522aea9ffa2be9740ba1d32375d7db993e1977657ca8f17adbf583b585a7fe8f`  
		Last Modified: Tue, 13 Jan 2026 01:17:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d173348bf41bdf26b341bbc1b1ea836f0a44a899204baf725cd3da6cf6a0d838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef93ec566e19f8982320465178499efcd16e2c18ed389ffc1b5fc987d9f5f123`

```dockerfile
```

-	Layers:
	-	`sha256:4461135a9a2fa5bf11404e2781c37a548d969031a615d796c728959c38a03172`  
		Last Modified: Tue, 13 Jan 2026 01:17:22 GMT  
		Size: 3.2 MB (3168079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc80188cb081fccb3acbaeddc63491681833a42dce49769597768f89f7e6f98`  
		Last Modified: Tue, 13 Jan 2026 01:17:22 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a5446515087a8af0ef49eb8d8a352edca2dd9f5950963f3dabb90b5c80c3b564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53112340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299f7d10c9fa893da13dae709afa1cff5c4bc0078298c7e8066cfe33460c9a5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:22 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ba2d005d228b6e5baa8cf039e948417198fc943600b9c36c46538f422a505`  
		Last Modified: Tue, 03 Feb 2026 02:15:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0b86c7c5020df3b2610c27a23da05a2d2dde73b0c482521b6742f63f543488c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6902a8b037483ffcb0e50808df560cec23e56c7debdc9bcf0b8fdc6eabfc6ec`

```dockerfile
```

-	Layers:
	-	`sha256:bf484b22e26c5da244215a70471bee2fdbb0ad7ba2edf456195c00aad5ea1ecf`  
		Last Modified: Tue, 03 Feb 2026 02:15:35 GMT  
		Size: 3.2 MB (3174390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0470da5e993c6eddc143c42e2a7e14887062b411a543bce6b065cbd2fa358c`  
		Last Modified: Tue, 03 Feb 2026 02:15:35 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:e3c507c476dc21fa48706fecf0509666929fdedad797f77387adba595a541286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdc07dd72781394805910843d78b196c5f5bfa3a7bcf9f2e2fa42178461cbe5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 04:09:24 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71d02f0dc09f1e2ea78ca7e76a13a5438a033af0e825c9cc572062d365d58ee`  
		Last Modified: Wed, 14 Jan 2026 04:10:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:94e24be6c811c9716c4e5d1d27895cd8647a0c468d68f7d377e985f5b1915d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44c01bd87fff2359cf88f9b175598a719b91e45f06ee6bbfe868cfc60696a9e`

```dockerfile
```

-	Layers:
	-	`sha256:9bcf00fdac5abce660dcc7a5680b3077c909c245e57f3089d288417828a4e812`  
		Last Modified: Wed, 14 Jan 2026 04:10:19 GMT  
		Size: 3.2 MB (3163202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1733f600103c0a065ac2373b7e7a546c0b57f51c76466b4f1ce323ef66deafdd`  
		Last Modified: Wed, 14 Jan 2026 04:10:19 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:bf03821004c54071af0406c3a806a56b014719e3d907959119d1098db2611a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49354603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6b7829e7f337963cffdfaa89651be7b576ad536a5b0269ad7a169d3f421c27`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:15:45 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae09594acaa53f8dd35d9ebbf603935bdff0d0b5001c8d06409aeefdfc3e8649`  
		Last Modified: Tue, 03 Feb 2026 02:15:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:451f89f04445b11afc29a084645363933bcfc90d0c94d1abe1defaece499ab77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f26d0fcdb1313eef0203c78758806f525f7dabbaa867c466080b8027b45983`

```dockerfile
```

-	Layers:
	-	`sha256:bfe96903ba1f0a4b0681e81cb413f00675a34d257b4d4e957d521cfa20d1af15`  
		Last Modified: Tue, 03 Feb 2026 02:15:54 GMT  
		Size: 3.2 MB (3172324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9109c13534a81b2cf08edcf0f69241b4e6f88df34997daef772cd8e03d23fee`  
		Last Modified: Tue, 03 Feb 2026 02:15:54 GMT  
		Size: 5.8 KB (5783 bytes)  
		MIME: application/vnd.in-toto+json
