## `debian:stable-backports`

```console
$ docker pull debian@sha256:da5f31e7b49bf7b7e4c015f8cfa07cba420d64aebd4eeb0fbb8d623e377a52db
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:60ece4664f43d95f3aa9e9b1a6a155b00c8d6b8d1b4788d228c82822281f0738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48468062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e9ab9543c41aa76817e603340e8d42510ac5d49477b975681e6be5f3dc1137`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d13e9e1f0043297f2d26babd2da7b67a25bb005e4447e4f7f02d4d325cf23b5b`  
		Last Modified: Mon, 17 Mar 2025 22:17:39 GMT  
		Size: 48.5 MB (48467842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc8ae6c8f46400f23623f11d214f1931b6fa3234415da010bf823d8b94a4ed`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e1d00780cb800d5070e4f8c5e0c47c73cc27f64ee707b3d293657d010ad0d6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737043a116b7de1720bcde5f739542b42065ea6f0eaed868b521bea67463483f`

```dockerfile
```

-	Layers:
	-	`sha256:bd3f0e6761a423963f66d275ee91603a0f995af9ac041dbb42258970647aa0d4`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 3.6 MB (3619232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddece9284eae3b474aa796bf1affea42fb45276a4786e26e49b2110244501365`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:45b60649b8d47412ed3eaa39d11207d47a6ec89f8203232aaa9e090c6e178611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46004854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bd8866f9ab4be0781da53ccd26bc292d8b0e31e36ebe329211234a275afd94`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:eec9bc53b45e2d1c2fdfc7d297326ddef374c1efd2fb889260ccd7edbb68e8a3`  
		Last Modified: Mon, 17 Mar 2025 22:19:42 GMT  
		Size: 46.0 MB (46004634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f862d3093ae9efa7734c592b4eac35d80ccfa385d88de8354c93741caf2b85b`  
		Last Modified: Tue, 18 Mar 2025 01:21:14 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f1434cf91d843cc47a5b51c3852ec7978030742cf20b49bbd407e0fab5a6e119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a78ff84a634d5d6f134091fbdcf8b49ce1d11f9f4c8a616006325db35d6e76b`

```dockerfile
```

-	Layers:
	-	`sha256:ecc58de294552eb2adca73b42f7c64d5a14e21c1a3fdcbc633474746f4f3b9eb`  
		Last Modified: Tue, 18 Mar 2025 01:21:15 GMT  
		Size: 3.6 MB (3619433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f962045cde54a8364e8c2076cc786d836ce08e66a7ef5d00d96c673137104603`  
		Last Modified: Tue, 18 Mar 2025 01:21:14 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:39363b4f3d837215cdb8b92b2e6be75e10f8fc55dd077110dce83a40aa5e4cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44180515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd2a012d9624c734e8567eeb930141943bf56fa7b1238facd406be9bfdeedb8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:18d102153f0e178ce1682b0083f1683ba69f97acc2cf2c458f9800dba07987b6`  
		Last Modified: Tue, 25 Feb 2025 01:32:57 GMT  
		Size: 44.2 MB (44180292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6043e2cbc89d4b53ffa29abd463cb824966f4b27948b6fe03095c95159f3b2`  
		Last Modified: Tue, 25 Feb 2025 13:42:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f3529a0e7628f122c5694d31b716a4d0a530a1e8ce2539957702759322b524f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640aa94c847f4d4c477c064e9ea88a27a7d7b04be2300e35f9c7efefce0598ce`

```dockerfile
```

-	Layers:
	-	`sha256:b74fa576a47fc463ff3bb442c60917fbd6cf3497b6e95a286c69936411d5e644`  
		Last Modified: Tue, 25 Feb 2025 13:42:16 GMT  
		Size: 3.6 MB (3621403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d93266f6cec8a26aa6ca89189d831b37534df08ede6297b0cceb0f68f8e209a`  
		Last Modified: Tue, 25 Feb 2025 13:42:15 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d5267ad5eba2abd92e3eaecd0deab01da76bf723af4073a9eda52eb4110fe5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48308233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9ba90b09538cfb53dd0be698badf91252fb06ca866dc150e07b37bd930c115`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bc50a3b87241d2f15e157de1ad359ab03ec88196efa05d44e62fba74bb7a7791`  
		Last Modified: Tue, 25 Feb 2025 01:32:48 GMT  
		Size: 48.3 MB (48308012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a889d6d89557d7ee7348d3a565050f12e67199ef06b007835cb5f9a2d6a19c`  
		Last Modified: Tue, 25 Feb 2025 02:16:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:14ba3d411ff6759b0c03fa1e9f7d2a847fab922738635760a5f7b12a921bcd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a38421cc300fdc2a3d087b7a9bb676ca69aa68ef9ec5ed062c3cd8d01a5aeeb`

```dockerfile
```

-	Layers:
	-	`sha256:6e51c1798bc433e64be1a267e4c42a3f3722294d66662272a57112101f7503f6`  
		Last Modified: Tue, 25 Feb 2025 02:16:54 GMT  
		Size: 3.6 MB (3619439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a754b00e8a8593b9d1e64c5cf103bff8da0cba572862e961f28405abf0cb6601`  
		Last Modified: Tue, 25 Feb 2025 02:16:54 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:e80293d04e3f3caa0e0a39dfef2f75712419ee18072b03fb944acca9e93e1a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49454704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e57f025d59881828ea86b0829e8e8dd54b6d688a2c907e6cffc9337dcc041f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4fc2227b02b7753dec8fd6f4f9fac9ebf779bab7730575ff97e5d3ee7f09ac99`  
		Last Modified: Mon, 17 Mar 2025 22:17:53 GMT  
		Size: 49.5 MB (49454484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d6fa98145ec720918248eb1b383808d5a70b3152d5128032376b9b5aeb6db7`  
		Last Modified: Mon, 17 Mar 2025 23:24:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:df0a28f46d74a96d3a3f1d4624e2498a26929e0c460ae5f4ab9cd8b9f68dfd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e493d15e605bcf1d583db9ed19b1669d0d4e2a841a9f4782e4b20ffcfeb85f`

```dockerfile
```

-	Layers:
	-	`sha256:25ddcde88746ecee31774ebf605fc6793466ede2e685caadbe4bea5c90575e1e`  
		Last Modified: Mon, 17 Mar 2025 23:24:55 GMT  
		Size: 3.6 MB (3616393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94432faee273d02e470c35a340c004c8d28b73a6c5e5a3a304ca6334ca4ec55a`  
		Last Modified: Mon, 17 Mar 2025 23:24:55 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:05cb37de7e0f1e1bc0b1539c6e25e06bf213c14e39333c2b2ac2e9125c8d5edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48759215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5122d68884508d45553fbeaf4e2528cd33d6141a36855aacf36f2d0d75acb215`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b00717954dcfd9e14c301b7b40373054eb7ce9750f649a121bd9a1709d351715`  
		Last Modified: Tue, 25 Feb 2025 01:31:54 GMT  
		Size: 48.8 MB (48758992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b206ee07eea4cefc18424c245183a2b5518d7447d7b8e3497b87692efe018922`  
		Last Modified: Tue, 25 Feb 2025 02:14:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3f63d9ee11937fdc90aeda1837792eaced6b17f023f133db6eba2682d08f2385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f5e974bb8b30e051a9e22ff18e674ac725e70ca4b39195104b00b6c7d7ba27`

```dockerfile
```

-	Layers:
	-	`sha256:59605375e94f94b7a81ea3b733659c2459efb3619b7e789f8d48a7d94ee9b210`  
		Last Modified: Tue, 25 Feb 2025 02:14:09 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:be4ed0e3100efb07409ee71b9bac800ab858068478660222ca2338f085b5ec0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52306259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c948c25631b4762091cb06e2157b6469c87cd0dad1506a3ca1e6936786b666e8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7b170e7d04478940da61ab16e68f36f4af444ae52cf1c7f0e8c9d67792bd406c`  
		Last Modified: Mon, 17 Mar 2025 22:22:22 GMT  
		Size: 52.3 MB (52306038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bf40e1adb2d7131be8778ea08615d1e53f1f4a97b27b2867f619ab55dbda14`  
		Last Modified: Mon, 17 Mar 2025 23:56:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c656dcd659a711aeb8c0e528c1358d2c7ba2ca208737d48fd64fa889ef5118a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056f1bca151528689a43cc4134d861c9b3c29a6ee0eda387a7345d44419ca1da`

```dockerfile
```

-	Layers:
	-	`sha256:ce92b418180fecab20b2e35dcf09e296f431d6b26fe2a759fff8a436a051f666`  
		Last Modified: Mon, 17 Mar 2025 23:56:44 GMT  
		Size: 3.6 MB (3623492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c409efe0165099363931b70155d56b39d2f3367284a08d586cf7e7855c7816`  
		Last Modified: Mon, 17 Mar 2025 23:56:44 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:b1689d00cd77426934bae5d2340509cdd54e34849fc1475b713124b470e4f8d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47128064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76025eabf89ec145ecaae458fea136a35ef895a798a0dfada1de5c15cb09172b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:23f3511497dff03f3711f6582b939128944c601d8041aca263c5832d90cc09d6`  
		Last Modified: Mon, 17 Mar 2025 22:44:29 GMT  
		Size: 47.1 MB (47127843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d50bde5566b7dcaab15107427e461ea3a78ed6a5088e2ac5fba2dbf9af02220`  
		Last Modified: Tue, 18 Mar 2025 04:25:46 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:862a633175eb231103f53b1c113d82fc1228e7f47fb90b67686636174240d02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a089100d7a755ebe4cc711a479056aacd8d80a7c6f02df7bb43e6e9837578d6`

```dockerfile
```

-	Layers:
	-	`sha256:a293ed17555accda0f9cbe9c3a73c239e033f6904669c0f29d2c98b21c38f289`  
		Last Modified: Tue, 18 Mar 2025 04:25:46 GMT  
		Size: 3.6 MB (3618962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19ebcc2e267a73ad9c3a3b0be8a29899f6ea6b276787a80d87486790cfc3445`  
		Last Modified: Tue, 18 Mar 2025 04:25:46 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json
