## `debian:trixie-backports`

```console
$ docker pull debian@sha256:c4b9d852ddd2f2d751b3628ff2e5a4c03e4606cb422ba352f5a0d72b9c246a32
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
$ docker pull debian@sha256:dc85deb8dcc72a8d49b96ef2bf115c71d7ebf2a3f3ea56e391e8a8b97add3e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49285845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953b2fcc9ea47ad48b816ba4dc3d3b71f4e2a2c795c599e1d6c5bc75f0f8ad7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:13 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7358cddc6e918ce923801f0cabeb53fa573f88ea5d8554762d2b3477f165db4e`  
		Last Modified: Tue, 13 Jan 2026 01:17:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c7c9629b1e1c90240f4d0bdec84543bdab8775efb23a7eb09cb9c707b7a37e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b523a8c2b4873ec0ecf019de27218c0c0e7b3033344f967bf966fa91a2e1bc`

```dockerfile
```

-	Layers:
	-	`sha256:6e8f34d82e4bfa1b416dd865a07ba4e3718c24a64e553c427708712ab1b91f81`  
		Last Modified: Tue, 13 Jan 2026 04:27:39 GMT  
		Size: 3.2 MB (3170877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca31fc36a327b02c177de276180ff1b1a35c9a3c033e3f5d424264d6179a409`  
		Last Modified: Tue, 13 Jan 2026 04:27:40 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b9bfe7d813eaacd3afcfc77f6759eded8e92815474be7b6a3c20748bf0dcc62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c062cf7f5375d758fd1aa26ca087afeca190c45776aca2213ae7216139a9ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:30 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:16d4329ceaa8dc305221873389c356e4c5bf3cdb5b245a79ff75a1b1806f3778`  
		Last Modified: Tue, 13 Jan 2026 00:42:16 GMT  
		Size: 47.4 MB (47448362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddd1036f97e9f34060c3ddd1959387c4287240efe5a94904b8bc1d97e8057bb`  
		Last Modified: Tue, 13 Jan 2026 01:17:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f5c2e6e6f233884a9488af56cbbab2363d2cddcea0344542026a39dd71bee24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e87dd28ce773c265c53f2d1b389023e208d2e053b4a1218e2facb4259d9b25e`

```dockerfile
```

-	Layers:
	-	`sha256:b237b02b3a450bb7220537e286b1aaf6a6058d7787e705b5c0aa492130ee3cd0`  
		Last Modified: Tue, 13 Jan 2026 04:27:44 GMT  
		Size: 3.2 MB (3173814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c111271aa25fd2119d3e2471bb2d122745ddff1a170d5204deaace076ee1db1`  
		Last Modified: Tue, 13 Jan 2026 04:27:45 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:18:45 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:27:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:27:57 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:28:03 GMT  
		Size: 3.2 MB (3168079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc80188cb081fccb3acbaeddc63491681833a42dce49769597768f89f7e6f98`  
		Last Modified: Tue, 13 Jan 2026 01:17:22 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:656215d1b4f5fe4fc9371124c948d6ddd4bef3f79e154d4696d2be9df6d1e61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53107184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7483271b08567f03f79b7516480ffb5aa00f43c6f1704968966db5a45a3530`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:14:28 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e751f6aaee3af37e78e25fe51783051fa18693360a3377300a6a8213c20ed77`  
		Last Modified: Tue, 13 Jan 2026 09:14:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d8e697b2e299f9fb8e66dbdf0e7152510489f70ecf8198b1ac0488a3d76ad960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e54c9fa50a593cd15337d5b786a2f16d5c68fc8b0b67e443fc5fb205710e63`

```dockerfile
```

-	Layers:
	-	`sha256:b27f193aec2ca5b77a59b091add55f62039d0b928e3d3ef389672f06e7f745e5`  
		Last Modified: Tue, 13 Jan 2026 09:14:49 GMT  
		Size: 3.2 MB (3174390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54a273b3fcb1a49e619591aee98e9bc4e3327ad0b308941ba02bd41663fb45d8`  
		Last Modified: Tue, 13 Jan 2026 10:25:18 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:06:23 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71d02f0dc09f1e2ea78ca7e76a13a5438a033af0e825c9cc572062d365d58ee`  
		Last Modified: Wed, 14 Jan 2026 04:10:40 GMT  
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
		Last Modified: Wed, 14 Jan 2026 07:25:08 GMT  
		Size: 3.2 MB (3163202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1733f600103c0a065ac2373b7e7a546c0b57f51c76466b4f1ce323ef66deafdd`  
		Last Modified: Wed, 14 Jan 2026 04:10:19 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:18fdf937870474cf137e5be2fc73dec5253e4e6b4624c5d47ac074a77c067710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49348928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb404270967782a7c285c018594bc657bd9eae933615097bf7468f107064bfcc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:15:16 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f1eeace74daaef97c5e39d8ed1bb14ff8c483adba12dafd65289252914f052`  
		Last Modified: Tue, 13 Jan 2026 01:15:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c35aca91506c3f9736bb237fa80be3e512ea4092a6f83542fc48c8af1c47280a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059b355b4b06b14f9a5dbe1f2902d5fbcab335140b1797794dd431acc07e3027`

```dockerfile
```

-	Layers:
	-	`sha256:340513905bee344f8a966267693f9b7967da53ed365141242ef10ec7c6f40772`  
		Last Modified: Tue, 13 Jan 2026 04:28:16 GMT  
		Size: 3.2 MB (3172324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eb074ae1b67190240315b21515a3b66e04b20f0b7aa3d73205469f3a038e4f8`  
		Last Modified: Tue, 13 Jan 2026 01:15:27 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
