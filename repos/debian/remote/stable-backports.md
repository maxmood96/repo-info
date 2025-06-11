## `debian:stable-backports`

```console
$ docker pull debian@sha256:c3648980e6421ec2a84b54dbeaed30ae4a3aadf2c61647f30c08ee1d87c16d62
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
$ docker pull debian@sha256:e478b02c6f97b3797e904716dbf762834a89f8c163703228bf8d08ef93676525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48494496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da44fe96903f844026ba8b014f7540bd2538022dcf1ba7aae859736f8eff4ca7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0917e117371d10fed7da23c980bf7ab4e6a95a9a6e5a794a229095af300aaab2`  
		Last Modified: Tue, 10 Jun 2025 23:25:01 GMT  
		Size: 48.5 MB (48494274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3d629f196e05b57c5c6797130b74d1facfcfe0f956ab43cd57c5ade982e3cd`  
		Last Modified: Tue, 10 Jun 2025 23:33:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:579e8f5a5c82af9fdacf706efaee7137202d6f05be110c53dc2b70fb141ae7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8860ec024b66721e58950fcc7801ee2919dd375036e80118f5d6db4365583ca`

```dockerfile
```

-	Layers:
	-	`sha256:18661315966cad49c7a288b6be73d608ae089bdf6d97e48254620a983a0a910b`  
		Last Modified: Wed, 11 Jun 2025 00:28:10 GMT  
		Size: 3.7 MB (3726834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0c46ed606c78bf744edb1fc1d2c76286038f830580fb9a240b24d302afc9ec`  
		Last Modified: Wed, 11 Jun 2025 00:28:11 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:13013ab9fdf2e1d1409eadaea7edacf7fa4aee07dadcffaf6f470f06d33e3e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46026816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f36765239a46ebabc578ff2deb8cacbd457a0466cfa31e0ebc323c189b66f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4fb18b2f116cae4839755ac8895393ff439763259ae6fb4e3ba26eb6a0bfb803`  
		Last Modified: Tue, 10 Jun 2025 22:48:41 GMT  
		Size: 46.0 MB (46026592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e134cc22fb550785a699c57c0cf5389ae6efc4131ad09c970d8104e885c3c`  
		Last Modified: Tue, 10 Jun 2025 23:31:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3578a03262c88dfc1ce1d99f153b2d1968ecef376cbbabffbc1c7d703b2daf4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a5ed449f9c0946c730048aec57c9a212b19b4188a996b999e07f156a2c2924`

```dockerfile
```

-	Layers:
	-	`sha256:8abab33d3a213ac50e54b9c27e504c110a91babfb9f8cb9553e8a15cb0866809`  
		Last Modified: Wed, 11 Jun 2025 00:28:17 GMT  
		Size: 3.7 MB (3727035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79337bdc57b5f3b59501f4f83da51525ad48d02009cf4841802deb492fdc85a1`  
		Last Modified: Wed, 11 Jun 2025 00:28:17 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:86b0d46a86153dd914735444a3aff865b7e32d8e1f6f82d8271c42865cc119a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1de53199e8a107c7ca5ab854b1da907099cb743fe617e6b48dfa2464bc4698b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9e53d5ae35a18b40ad8455da08e5000dfebba311bb87a607a8e52e672a7aef00`  
		Last Modified: Tue, 10 Jun 2025 22:50:10 GMT  
		Size: 44.2 MB (44208208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f26b31227abeb66a74a7acbb172f93c74a9cfe67571150f7ce900c6571f8596`  
		Last Modified: Tue, 10 Jun 2025 23:26:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5c4fdbf61901c87b9f981c8d7476a1fd24463d816ba70440ec7e1bcba94eabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd675c96efc80e3226587be0f6109ffd2800f74f0ef598084489e48b522c80f1`

```dockerfile
```

-	Layers:
	-	`sha256:250fa6c8c435fb098290bec1f801db5ad4eba16214cc5939782c6a96502c8121`  
		Last Modified: Wed, 11 Jun 2025 00:28:22 GMT  
		Size: 3.7 MB (3729013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67236b4338727df59781e534c256b9fd457628a55cb06bc549f641a515f0578c`  
		Last Modified: Wed, 11 Jun 2025 00:28:23 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5136d0dec98470b5c4a7a5393121b53996a9d53e3369c804d195761b9775b868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48339076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a8fe84e9dcee6149befd586e9e6040617f4fa0c359477739fff01ad29dd4d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0d966ea3cd2ba2a18158b897ee88b3dae489c0c8dc195edc63c279e9c516f6db`  
		Last Modified: Tue, 10 Jun 2025 22:50:57 GMT  
		Size: 48.3 MB (48338854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab042ce53f8468b9a0e1f7f89027ee1c7ac64672f43fc914de255ed205dae15f`  
		Last Modified: Tue, 10 Jun 2025 23:31:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cb4155e5bbfcfa90980a6293d1885ec47449a000e105138078fe731cb54d1125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7225c44cba4b5b9b352d70f1687b417c16b7c7f6970e0988eb9d7bf64154ad`

```dockerfile
```

-	Layers:
	-	`sha256:8e80966fe100794337bb595d9aca413f0265b858ef7ae570a43813846ef95bd0`  
		Last Modified: Wed, 11 Jun 2025 00:28:28 GMT  
		Size: 3.7 MB (3727049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70884b678ad89262e4858a37c6821de2c79aaef473bdece0c845346da5159b2b`  
		Last Modified: Wed, 11 Jun 2025 00:28:29 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:8c2b24ea236ea6b0c315659202a5cae2c5373cf7786c68c0587f08d739540169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efe0a8200bdac10b3b72506c22c9b5313a643d2a747018c465cd1746b4e32d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:802d083e99bf8f8281b79886f72d03f19cef3d72634a16fb21570f37b28b55a5`  
		Last Modified: Tue, 10 Jun 2025 23:25:14 GMT  
		Size: 49.5 MB (49477475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4c0242eb167927c5f391bc3ddb89acd4a02f855799d2ff22eda5a9959285eb`  
		Last Modified: Tue, 10 Jun 2025 23:25:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a60166fe13599f59c38bbe1e3ddf10442629b3d57e010e1c048046f0ed5b11a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe954da87fa10937a0796588df72e288b09ecb15c016c224794345994e11d75f`

```dockerfile
```

-	Layers:
	-	`sha256:a6cefae4cfb7d13ea872153ac3b10d97015c05600e0a40ba915f40aac2f74b69`  
		Last Modified: Wed, 11 Jun 2025 00:28:33 GMT  
		Size: 3.7 MB (3724036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3783aa8f3705f67f357b71e05278c30e639922649c707aef8f2a0841bdf5ac56`  
		Last Modified: Wed, 11 Jun 2025 00:28:34 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ab2a9c26d9fc08c4430065ca8f4f41009815d976df4a9d3351331da537708b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48775821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd8ef1ade42fa70e037d89da1de7c04f4e05927cf4e7cd236946a071fa615d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'stable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:739195b3fff7c41f45a8a56dadbab4aa1a6eb863d8379f8ec43d624cb99309e8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 48.8 MB (48775598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d7186af7093dbf7726993b95145af3be4420f60ce1c7301052b8978c44dddf`  
		Last Modified: Tue, 10 Jun 2025 23:26:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5db68f7e7dce16e145174bf507e0f9d05a7d1be4fe34f11339a631625851acd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb8915469e9894bc368647a8e9ba841932b05637037f06f7657764d77d06d8f`

```dockerfile
```

-	Layers:
	-	`sha256:f11ed647aa5f5b758a475de3405a3ab98ae3619554dab7ef65c5ad8ac51982df`  
		Last Modified: Wed, 11 Jun 2025 00:28:39 GMT  
		Size: 5.7 KB (5650 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:03b303f025282884d9047e970699ae03eb590db0d29ce8724b461c60209d61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6cb2dbed8f60e6e67425fc9b8abb4c52911123b7017f4497b1bda091e8a20d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:67b0b41fc6743282661fba323e147dbbac87a463b846cf0e0f12ae59315d83a1`  
		Last Modified: Tue, 10 Jun 2025 22:49:38 GMT  
		Size: 52.3 MB (52337355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab042ce53f8468b9a0e1f7f89027ee1c7ac64672f43fc914de255ed205dae15f`  
		Last Modified: Tue, 10 Jun 2025 23:31:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2ef02394b4399ade320de94c0707b8dd352019a8b16ed3064fdfc5062328cea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73bd7696924cd6e29031fbf12b3b37a8de2a33685f54bc5c19b557b81dd54cdf`

```dockerfile
```

-	Layers:
	-	`sha256:ef8e18df0d9b97cf25e19e8c690c45ac87b4e13d6f33aee49c49a87fdf92ba91`  
		Last Modified: Wed, 11 Jun 2025 00:28:43 GMT  
		Size: 3.7 MB (3731180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69696866a8a60b92a7282e5c96443aa08520d06c4d3f5c03a308d9034606e37`  
		Last Modified: Wed, 11 Jun 2025 00:28:43 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:058f27a9d9ef3a1dc26dff0025025cf2e5454c832ecba7b18cc9ea774e90c9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47149635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c0291c83a6f6a11f7e7f94eb98f1c433293d85dc935d208eeeb962b4725198`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b8ee2507293be07ede443ef863b0f354adecedc21719aa8dc50c90bb9a133dd1`  
		Last Modified: Tue, 10 Jun 2025 22:50:26 GMT  
		Size: 47.1 MB (47149412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d18916c8459e5556b36d47aa7e04a100a4c17105377c4cdc0c87f75b74bc9ad`  
		Last Modified: Tue, 10 Jun 2025 23:32:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:687bde3ce9f2bbcd64e501e96c06e70469850cf95ad7bfb1234c312c38fc3282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbff85f50e8c88ab44f03d6f0b14a9aa4433c876b048d268b510c80ebd145589`

```dockerfile
```

-	Layers:
	-	`sha256:9bf10954ee2dbad4c39272bd8d436df14e1260894191032f703c0bc6f2c39890`  
		Last Modified: Wed, 11 Jun 2025 00:28:48 GMT  
		Size: 3.7 MB (3723672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e10ce17411dd4bee4f982a3304abdeaf6d339dd1bf15b0ff09437258cc3fbe52`  
		Last Modified: Wed, 11 Jun 2025 00:28:49 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
