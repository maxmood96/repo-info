## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:3fe7c675223c4e0405d4207e24eb1e4c3bf19ee11a9646cf0e7619d6e62779e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a35aa8b45c44873f50d11bb966c016c4668451a55520ef298bfa46fa311873a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60150471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6104e8936f061faa342c4c523fdfacfac26378d45d9486da91ddae637f479695`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8d64c6c7c21822ac171c4c396d70161707401d6d50d133075d661956f08dc756`  
		Last Modified: Mon, 08 Sep 2025 21:13:08 GMT  
		Size: 49.7 MB (49657990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144fde7d694dd5ef88504ba55ce29576ef669fa6f3df0c8853397b6a3268cbbe`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 10.4 MB (10399314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbf6772f1e0545288e07cf0ceaa3f94da2fc29c74d7eb03d4bf094e99392ae5`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fba2595e2127b79c17e4ae5386fc3f5c426141156e917da1355fbb85ccf90d`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f417ad3fc8c42aac0bc4283557ce36de1dc98cdfdd91eabb26c4a7b7d3de070e`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 89.8 KB (89844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f06a1a1687a3f978541c38dcb673e5ff3361f7b879268038c9e2420127745c0`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2be98938edcce0a407fcfe2b626638987bd84491450fe88ebaec0cc09dcd1ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e0efac7157da5dd4116b8db93ba1fa1296880d93eff0a00171cf0cecee7910`

```dockerfile
```

-	Layers:
	-	`sha256:af1ba855b844937cc2f5a8faba90ea901d7c9070e32458e6762b67c378313e49`  
		Last Modified: Tue, 23 Sep 2025 22:07:46 GMT  
		Size: 3.6 MB (3609976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d04311730d3fcedc87b7d493ad4f221c9022f4283ba58e82cdcb99f34672705c`  
		Last Modified: Tue, 23 Sep 2025 22:07:47 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9191edad731c3777239ab7a6df02e8c3cca27fd39f070d3a9f2130a27b286529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60205498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed9d6ab91c97c1ce364b776c074b575641047e24efa1851b32dceb9d3e43f91`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:00e024daab2d43f36749bffb01f2b299b405cff0659a8e4f4f00bb468dd24c27`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 49.9 MB (49934721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81efd0f0dcca0cb336b828640e6827714cf6b6db92f89cd82e323f6982d7f4d`  
		Last Modified: Tue, 23 Sep 2025 17:39:59 GMT  
		Size: 10.2 MB (10176977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603959d5699befce3d731668bbda6ef5af594a431dacdcd4f999328e185fbf82`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e002eb0aadc14a90478115b718f1549b2e972b9c8b9828cfcf24af8768e48b6f`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbcb7eb4cc610f644f057f5935ee9846750de3ed5aa29b6b4626721d2881bc3`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 90.5 KB (90473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f379b3fb391ace6e8169e270dfe80ba47aa454ebabc6a261938b427e9ba848f`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:84290dc5531ab703d1ea0a46c4080e9bb469fb5ffa14f513534e950f69ab9aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b99802cb1d850e1aa7fdd8c934d54b5c43752f6d208c43ddb6954d3353ab6b5`

```dockerfile
```

-	Layers:
	-	`sha256:3e46be236b4284404936a8f6998febda1ad729b8427e99900db52dfd85f23c32`  
		Last Modified: Tue, 23 Sep 2025 19:08:01 GMT  
		Size: 3.6 MB (3611491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a6e5fd5021e1f648ebc119ba8cab091880a2c17c44168587834ec61baf52878`  
		Last Modified: Tue, 23 Sep 2025 19:08:02 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:acab89f48ba43732b4aa66549b33e99073d08cb0d8b4dda8f2068b22a2150a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61759091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed2e9dfd34d78d1208dab49205386f5cb5dac7477cf3eeffd318a45bfd13e2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:eb039ce3bcf3fbed73729096e510ae45e98c7db73d412a09aa57aaad6f2f6267`  
		Last Modified: Mon, 08 Sep 2025 21:12:53 GMT  
		Size: 51.1 MB (51113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef9e924b51d56631ff7e60d9ffc923651a932453cc070c44c790dda109655cb`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 10.6 MB (10551936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a5c4260c5226a4139c1dcf60e7a5115ab5f76a7b0d9d8ab9dfba9e32017937`  
		Last Modified: Tue, 23 Sep 2025 17:35:57 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98aee0679f611ea7162c52e6ab4785f27f80c5589830cb5157d23e657c207730`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fd04207b73d5d0c0f97e7396b06c06e07035f1819525455162e75489f45e32`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 90.2 KB (90220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119bae56cac036245f6d4048fe985553edfdc542188b8fb42f75eb63b6c081c`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:72c4c16e05b5307900604596e5f718afa79b1171da6da0bbd2e78516f68dee81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4dd3ed7a3d34c1598c331733008530b70861d2d4880f6fde569b86843d3972`

```dockerfile
```

-	Layers:
	-	`sha256:74c2a34baf1ea8506bb8987565d0762224ddd979d8096a23060702450fd2d660`  
		Last Modified: Tue, 23 Sep 2025 19:08:07 GMT  
		Size: 3.6 MB (3607937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7f63ff5b26fd7dede37a98e92c1e59e3fcab2829d49ab90c1fc8f1296a48ec`  
		Last Modified: Tue, 23 Sep 2025 19:08:07 GMT  
		Size: 15.9 KB (15944 bytes)  
		MIME: application/vnd.in-toto+json
