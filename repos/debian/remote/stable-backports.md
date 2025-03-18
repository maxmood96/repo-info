## `debian:stable-backports`

```console
$ docker pull debian@sha256:d778574d4cd7268f09188c513c52be25b1b214ff7040f3bfcbff8b5451ce3c44
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
$ docker pull debian@sha256:87ffeb914b44d02f9743d36234bb929eb17218a86f2f8a3af54273635da99647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52307879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa54910bcb4037f9d30d5342d0c1b2e82d4546b1adff676376d5bad1d395fb5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:76ac10ead5cd68e905a2bb06901683d02f01c7ed1e78371629895f251b5083a8`  
		Last Modified: Tue, 25 Feb 2025 01:32:16 GMT  
		Size: 52.3 MB (52307656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d499c867f40e7f0976cd9300f8d61bd9b7ca38e4263266b6534dc6768483bf`  
		Last Modified: Tue, 25 Feb 2025 02:15:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:da1c7d62eb6c811de181eb52df44fa76de7a02e0cb1a7eaf061476cbc3fedfa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86589a487992c4752ed4c3a980669da661a2218c3c45f2c0780e15bf0e0a98b`

```dockerfile
```

-	Layers:
	-	`sha256:e5925fa459d0b141ebaec57f5a6736db450a0ca5f4627c50b1f84db9745bfba2`  
		Last Modified: Tue, 25 Feb 2025 02:15:07 GMT  
		Size: 3.6 MB (3623484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23a782b2100f7ef871781496e7ca49ec0d039a72e5b4d06a39bac654a88b974`  
		Last Modified: Tue, 25 Feb 2025 02:15:07 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:725acb97c4b43d757ed862d296b1786b30bf637334805b83419c81db4da94fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47130215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeca435e19c69bf504ad13fe8c5d9e08246d706476c9b270dc24d8dfee0b3a9a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0f7d27d237065ed06ce13b57f4617f9db17930f64a7977c5a049c2db3b7571af`  
		Last Modified: Tue, 25 Feb 2025 01:32:01 GMT  
		Size: 47.1 MB (47129994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d362dfaf3ab83dfc1b31675ab9898063a8a3dcab92a94dafac10e64695b51ca`  
		Last Modified: Tue, 25 Feb 2025 02:13:31 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:94e298b935948cdeffee1538f9ddd004781cb85ea564319afda2de24fb9b2faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f869f8932b45e390d121bccd15d2b47e5407288699449979d9f9ccf7c2f15dad`

```dockerfile
```

-	Layers:
	-	`sha256:4abf790762cffdefe1994321ba5dcf009690f98e0008d1df8f241a75f772152a`  
		Last Modified: Tue, 25 Feb 2025 02:13:31 GMT  
		Size: 3.6 MB (3618954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ce047bbbbb867a3e1fe9de4c6d576382c8c961607d3fa2083b068761c6ac1e`  
		Last Modified: Tue, 25 Feb 2025 02:13:31 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
