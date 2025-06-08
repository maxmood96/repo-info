## `debian:experimental`

```console
$ docker pull debian@sha256:76629fb1caa9ee645606eb44e4bee22f8b72ea69cee8d4c1ebf49eee9f1b4ea7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:30c958a8f0fb0198e1424b51613869c90f7ef5e005fcea9b025c458ce4fdbca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49250773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58229873c6417ebaef526c010877edca5495fabf47a99cbca2e4277b3efb9dc1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:e5f60aba4bd2f0b91de6745acf5c8d836b70017d92802414f62593dd3b23fce3`  
		Last Modified: Tue, 03 Jun 2025 13:37:44 GMT  
		Size: 49.3 MB (49250552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440f808c35738927d977a628f73a1b7a570578a32d40c6ca0f8367bbb16038c4`  
		Last Modified: Tue, 03 Jun 2025 15:30:15 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:dad0e9fe156f8e480329e2fa5f98a748618458db344329260f4503beb0973080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3090725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6097f419dba51497603e5af079148e5a0c41f02e4e625a25e431535f8fb31acb`

```dockerfile
```

-	Layers:
	-	`sha256:dc6d53f963cf3d81b8104d7813892144a0d144cfe103e746453bac5f8a474087`  
		Last Modified: Tue, 03 Jun 2025 21:26:12 GMT  
		Size: 3.1 MB (3084581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:399a5ac854fe25434d8b2c6dab7e24c5244c5c4113ab7e083cf901e460e0c579`  
		Last Modified: Tue, 03 Jun 2025 21:26:14 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:297ed5095cde4820d76c3428297d6132918fbcb699c0849d330198fefdea3305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47443120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd8ceb63696ab9d6c43a051b7ec9c3c6ef83bd5e7027ac64fdbe3d4cde8216e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'unstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:bd458edc3f313b5fedeca70c60012f2aa03aa7bba14506f8dcc5d46d4d7dba2f`  
		Last Modified: Wed, 21 May 2025 22:31:20 GMT  
		Size: 47.4 MB (47442898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2989a5d9bd1798be5310c185b2806fd3cb39451816f4b865f79c7e730ae81`  
		Last Modified: Wed, 21 May 2025 23:13:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:3b8ea467a93529d0793d71b65b7df8047171ee426813dda529555b8c6ef30721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4196c862fafc1b1b89e122bf7ca563dbbc6221d6cc6e5b67116292a48146b36`

```dockerfile
```

-	Layers:
	-	`sha256:81234d71e7e29decfb4a5e8324dc96fed923627be91981e54b96e1d9ef6cca58`  
		Last Modified: Wed, 21 May 2025 23:13:04 GMT  
		Size: 3.1 MB (3093898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c423dd153118c7b932205d9302ff3fbe7535b19f9543f3daefb8c876fdd8123`  
		Last Modified: Wed, 21 May 2025 23:13:03 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:021564f807c552e2092fc08b3e0f7c563c8b66c073af34b0ea4bfc97d5311c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45698853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b43afb7a03bcbe08b5c96873e8af61b5087619ac9a0adf39f8d921cc2cf5ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:15286b387cca78e52179168ba6efbb67ef9586bbb166b68b5f9f5ae8017c79e1`  
		Last Modified: Tue, 03 Jun 2025 19:10:08 GMT  
		Size: 45.7 MB (45698634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb071f287524a98fd4c5ff10aa913f7e58cfe06a150aa7e3c90a64bfe124ca58`  
		Last Modified: Sat, 07 Jun 2025 07:56:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:fcac09f9c8b82b9bbec45f219db1a57682400e351620587da5d8f82f7ec3f57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3092167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4913b04fc18aeadbf007b8b4e28f7372f870facb751dd2e493350ce678935e85`

```dockerfile
```

-	Layers:
	-	`sha256:fcb15d476b5dfa0110f6ffdae81689ae470d5499a34c66a0414ebbf39d5e4908`  
		Last Modified: Wed, 21 May 2025 23:14:29 GMT  
		Size: 3.1 MB (3085963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dce9b32ffebd3ea9d187f90f803f882420ecd1234f2e454896ded6ae219d88f6`  
		Last Modified: Wed, 21 May 2025 23:14:28 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f853b1d5798e67f85c1262a1cd282fe6e27aa6ef39e87e9c4f9b64505dbc1f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49618090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bf363fa68d8a443612e6d99823b129fb1cccfe66b9306871789a55819d76f2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:61f49b0d0f8d763edd3811a88e6d67078d4353df65e6742bc2e2f61ca8d51b59`  
		Last Modified: Tue, 03 Jun 2025 13:33:33 GMT  
		Size: 49.6 MB (49617870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2780d777b1d5d3ef777fe915e1be30293a0d847f9595a2df0a991219e73263fd`  
		Last Modified: Sun, 08 Jun 2025 03:16:22 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:87b0fea939d3b895289aefe168ccf06ad007bf022e75b56828b3678810e178ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3092298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788a8acb85a151e421e724bc0ee28058792bcf5e5b02e8c6e45b63409825372e`

```dockerfile
```

-	Layers:
	-	`sha256:070947db73859643ddbb98657566a26aee107acda47d1912eb49716d7428daff`  
		Last Modified: Wed, 21 May 2025 23:13:31 GMT  
		Size: 3.1 MB (3086074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f653817ba06752010fe548a5e050d92b9eddd840c9a983fe0788a8e48c523ab`  
		Last Modified: Wed, 21 May 2025 23:13:30 GMT  
		Size: 6.2 KB (6224 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:2709bdcd46093ff10a6c89627fb5d1024201189fe9fc1dfd5e26689de987b1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50760602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47709b0f14fcdedd8f1b63fc7e3f69adde8482f4f627fe1c4b9b233b5a49bc82`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:12e375ff988ac35c08058fd52d55efa1595b8c9b9628628bdf308ec892fee855`  
		Last Modified: Wed, 04 Jun 2025 00:23:03 GMT  
		Size: 50.8 MB (50760384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4adffdc167dc105a5d2a84eb6a87d997ee77714db0bc0b1fa1e52a67a53f9c`  
		Last Modified: Sat, 07 Jun 2025 07:50:52 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:2038b3fe41cd93c5b4b6fb12cd564d6da5f4bbb9a26cb363104a8aef23787f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e27251a7565b357edcea59711499c553557050ca92dcf6a2dc678888ae762b`

```dockerfile
```

-	Layers:
	-	`sha256:acbdb4dfc27cb21eda9007e8382d26e7c38fd81367432ea07f9ed825bffd873a`  
		Last Modified: Wed, 21 May 2025 23:11:59 GMT  
		Size: 3.1 MB (3081780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc4dcf8b58c1fa10317c7b97f457700d530e97a33f45c5ce58bacf818e0f2818`  
		Last Modified: Wed, 21 May 2025 23:11:59 GMT  
		Size: 6.1 KB (6122 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:a8c8e6d98d8db24e87ae997954408f78a834ba9abf6ef8adbf2c6e4c5f92aa39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49538553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1862d72ac3e0c88e43dffa71af025133ef40ebfdbd75c6fe6acc5a9b7cb155`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'unstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d550133494042d76ed54a283dd0d767c2bb5d21510960fd19f423f549fd0ba29`  
		Last Modified: Wed, 21 May 2025 22:30:44 GMT  
		Size: 49.5 MB (49538332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54de6c2cef44c1642a27a8dafaaf8e007af672a7d5db421d7e4369d5607df396`  
		Last Modified: Wed, 21 May 2025 23:19:49 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:def9370fb725631048c00ce54a402027438054f28c908e2df5292b5dcd567bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 KB (5977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545ba9563c8924d982bd335df98f855b4c191ac204d01e0485d4f2733dab3eca`

```dockerfile
```

-	Layers:
	-	`sha256:d2883b47f915d39fcd900f0f2f49a9cce30850240b1ed592acc2c88b4c8c6e06`  
		Last Modified: Wed, 21 May 2025 23:19:49 GMT  
		Size: 6.0 KB (5977 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:a0945cabb4c51454ff5c8421ad316fdfb5969c2540f7000871f764a854d6f96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53087246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd9fc0715ab802eac596fdeb763e8470d1356af73ccc54250bf82bfdcf00a9d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:e333a5f7e6f80df1ce13fc20119f14d4224f1ca47c497147a645053c604d5d89`  
		Last Modified: Tue, 03 Jun 2025 21:24:02 GMT  
		Size: 53.1 MB (53087025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d143634887981ce91d41ccf2125f1fb1747556ecea2995a48643628feb74d8`  
		Last Modified: Wed, 21 May 2025 23:14:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:af1d7734ef88db2aefdb5baa4f734cfde90ba7f7c39a6d92300db168e6cd13f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae46a975ad09c435120fbd7812852da50328cd2d16c76dfaa89bea7d42dfbaae`

```dockerfile
```

-	Layers:
	-	`sha256:10ea321512e41fee1eb3c0adb20f20032e2fcff3bba9617fb1d7b7816f5e4463`  
		Last Modified: Wed, 21 May 2025 23:14:05 GMT  
		Size: 3.1 MB (3094468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e980a55be7b9685aaa4647134bd7326738aa9d64443149189d1b7da2bd5f6b8`  
		Last Modified: Wed, 21 May 2025 23:14:04 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:83f3af2b2b88b29179a82ebce3d6d7f0100609bdcbab91d18a038735565acd6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47737783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20b27074727e3acef94d9772dc3158acb23953be248c1bb439719c783635f79`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:f151d2c11af6e2b45a78a50d495d5ac40408e9bd89ca077acc924a897d50997b`  
		Last Modified: Tue, 03 Jun 2025 17:37:59 GMT  
		Size: 47.7 MB (47737562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3de09075ab7b418acdeac2819b0f10c0ce29bf51cb0cd11940289ac992426`  
		Last Modified: Wed, 21 May 2025 23:17:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:762f98e51c337cba8e39fe142032bd67bb6edfc790c9ed4bf316de21b0863a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064c30829e75dd34e840e6cdb3bc4557de0eb15e4b89fbb5b010e3852ee8a8b1`

```dockerfile
```

-	Layers:
	-	`sha256:23e7e87a0d8ad692291ff9e3ce34c8cbee34bbb3369303e08bd3b91340b22098`  
		Last Modified: Wed, 21 May 2025 23:17:43 GMT  
		Size: 3.1 MB (3076908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95b9237a12cf44dd522bd5edfc98e2e4175704e40f056fd20fc7d119fb574b44`  
		Last Modified: Wed, 21 May 2025 23:17:42 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:b6728a277e6b23b4ea4923ca90d7d57c1e230e9a601429a658fd645dd7d06a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49325887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145715c51e677aa55069dbfb3ce1107d9215d4e9867ec8fe519fa7994cb2f735`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:9b11637ae3ee4e6565315e80a9868a0bdbea720b551325a7da2db76e767f1878`  
		Last Modified: Wed, 21 May 2025 22:32:38 GMT  
		Size: 49.3 MB (49325666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1bdfd6b46f7c62a31e3c815a667c6bf940c010c6d56bb29bf04a1d8592d03d`  
		Last Modified: Wed, 21 May 2025 23:13:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:a22cd41f56d230772b479f7d47d5be0c6942f47084c112e8c6a21f54755202df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3098544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db975f9529399a0e091f80655f10d4bba3098de87856053e9f33f81ac845072b`

```dockerfile
```

-	Layers:
	-	`sha256:c7f55bbaf1e443ea9c869b6437a1efaf133c0baeb94ae85027828c5bddac8278`  
		Last Modified: Wed, 21 May 2025 23:13:55 GMT  
		Size: 3.1 MB (3092400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cac07b1e830a9511a210d5adcb187df44b930cd6551a75b10f70227f179f0d1`  
		Last Modified: Wed, 21 May 2025 23:13:55 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json
