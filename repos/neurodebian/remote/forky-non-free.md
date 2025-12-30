## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:d635200f4e3f15d9c13d3bc4c8a68ef05d2a992afddd547ca59eb2450c05994d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:56ea8c0eba2929e786fc26a4b61337bbcd45c6602c0e633949dd1a233d86d173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60548879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa82304520ea72936c1f1be9740090de2d22dd3eeb4175e3f9f0d6287e2765c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:03:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e1869079ab5cc3b00301445717c112f3ddb9424b5d7b2a41713bc70d9482ee85`  
		Last Modified: Mon, 29 Dec 2025 22:28:05 GMT  
		Size: 48.8 MB (48830058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaf0ac99f659bb6461220191a78a66c276d9816bf54d5b7182576ada79daa7`  
		Last Modified: Tue, 30 Dec 2025 00:03:39 GMT  
		Size: 11.6 MB (11625073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f62653a9582b12b399b318130654cb00f1e7633a7dee96cbd1cbdb492a173b`  
		Last Modified: Tue, 30 Dec 2025 00:03:38 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fbae46621e155e25e4836a84dd7ca71e6e4f31f86ddb9924239ceefb1fcc0c`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5677abe2abd0ea16c83243a95dfa4d82828123fe243948ebecaf73a1a2137`  
		Last Modified: Tue, 30 Dec 2025 00:03:38 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6c1cf3b8f91aa7794755a003db44fc5c2f67b48acf65c7a0b9c8a7e7b4fa93`  
		Last Modified: Tue, 30 Dec 2025 00:03:38 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0d38eca5c86573632d19313a058b0ecbc0e568e302f0426ebe28033b93e719d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e043b1451aeae3d0b9327ad512efe6438e8f08fadd4e6cc75b4d8880a188dca`

```dockerfile
```

-	Layers:
	-	`sha256:b9e68dda9c60e65ccae7d20c80d1f74a3829b61170430a31144926ffacba2427`  
		Last Modified: Tue, 30 Dec 2025 02:08:48 GMT  
		Size: 3.6 MB (3592105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd14da38b318103abc72d4da22409c4d400f464e564ab525e1d80436718605ba`  
		Last Modified: Tue, 30 Dec 2025 02:08:49 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e3f88edb3744a1481d41725b392334f62ffe29db0291e3c93b61dd2df66c9a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60210263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ec30ac7f439988b4368dfd9dfa11d36be4411c8128c0f32ec915cb65d02c20`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:04:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d6ed83950a3f675536ad8634cde3cf4c241d5faea11ae3192ff5909f826256f2`  
		Last Modified: Mon, 29 Dec 2025 22:27:42 GMT  
		Size: 48.8 MB (48831993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278e9ed2ac59aa8e052b8c075a014ec12973527aa13dcfc47386b5fc849d09dc`  
		Last Modified: Tue, 30 Dec 2025 00:04:30 GMT  
		Size: 11.3 MB (11283833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e5e80e4b2f6c88528a91fe91f2b355ed86bbfb9e96088827682cf0dd2fe3f0`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28c95221e4cea56d32ff27ac8a53bb48fe70456cc900191a16be091be283769`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f473be47c5749d5d961e89ec52f21d33af161fbde6fa39bf270b3682b3906d`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 91.1 KB (91085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ec3638ca167076fc05df171bfda204d00eb1f3ea1d007ef3b85db710e0582d`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef6bb4894931f521530b7db4fd13f66c4226fe5bf1425c4d024c2f567edd946f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b389ba0fe727bd64ef60b5007f1271d09508c42e0364b7dc035f445ca4e7b`

```dockerfile
```

-	Layers:
	-	`sha256:5f14d023f73b435b23489a0d89f2a5bad5a57d6efc8da662e4abbb50418a0fa2`  
		Last Modified: Tue, 30 Dec 2025 02:08:54 GMT  
		Size: 3.6 MB (3592981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad81100e36b669c78cf4ab2bf837b7bcafd554fe4f55a126cc3bf816defae711`  
		Last Modified: Tue, 30 Dec 2025 02:08:54 GMT  
		Size: 16.1 KB (16098 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:310986ea6782ef724d41e8f67240e005c3c0fbfe36d6e9779c703452978b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61721053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75690de1cdcfaaa39c9be4ef65273d76e990e6fab068d68efa4f94bb0ba85995`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:15:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae4cf933beea0d74190c5108f5592160b361455d8d0aca4852d56b28f1816ec`  
		Last Modified: Mon, 08 Dec 2025 23:16:08 GMT  
		Size: 11.8 MB (11752199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69195fca673288bc2be238012fb534a989339e533d6a8f67d5d4ee43d28117d5`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3571e3ea3babea5298321571e0ecff849e4104964f3e97b88921df3717d1aa`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d10761b27d78d3cab80c345eade32d07c1317137a5ae92a9998e523977655ab`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 90.9 KB (90921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6e1907cacf4ae722d1b080f12e49ca31d368e482e1835e219185719e6c1090`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3638e2924b6b21634a03c10613ef941641ea6b6d835763bb584846dbb4776e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9d1adf120a2f484750d4044e9113b7a12ad4287c721ee006427934f80f2ef3`

```dockerfile
```

-	Layers:
	-	`sha256:536b0ea1c809e7d334f738198e24640d9fdcc2284f7ea5394d9ac75a89aa1e12`  
		Last Modified: Tue, 09 Dec 2025 02:08:21 GMT  
		Size: 3.6 MB (3583567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1afa97a40023bd48ea41bef0a9c7435b97b608551dcbf15388b584d2047e4326`  
		Last Modified: Tue, 09 Dec 2025 02:08:22 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
