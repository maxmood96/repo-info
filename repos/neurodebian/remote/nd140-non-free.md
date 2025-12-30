## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:5d6d8d57eeb27ae061f626cabf9ef3d65d05fca876fa44c9244b1ee702df10bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140-non-free` - linux; amd64

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

### `neurodebian:nd140-non-free` - unknown; unknown

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

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

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

### `neurodebian:nd140-non-free` - unknown; unknown

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

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9c694ae89ffe92080a90e99c91bb70f5782492801bf22d69bfdab0773a200567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61823690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3f5fe3aaa9349205d7519aee7e617e082408dcc69a0d478ad9e8d06f47e3ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:49:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:49:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 29 Dec 2025 23:50:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a557815b7e39210fb0b4048ae58b1ffddbc8cf0f656a5974b6c3b24f7bdafed8`  
		Last Modified: Mon, 29 Dec 2025 22:25:28 GMT  
		Size: 50.0 MB (49955836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdeb9f94da4fbfd5d7f2863d8cfc06b4a0e8527c6d81afd096dbf660ced3c69`  
		Last Modified: Mon, 29 Dec 2025 23:50:17 GMT  
		Size: 11.8 MB (11773702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed137d1e65cafb35a440f480f41a8364a4c639e84dd67ddd061e9e2e5bffeb53`  
		Last Modified: Mon, 29 Dec 2025 23:50:15 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f59724ec860def0a502af1d0d9231998e4d9e46288309642637cee97db1b9`  
		Last Modified: Mon, 29 Dec 2025 23:50:22 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4418614b93b7270754ddde788928f3ea1e37902f652194b935bf02ffee4e0fcc`  
		Last Modified: Mon, 29 Dec 2025 23:50:22 GMT  
		Size: 90.8 KB (90801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35872b3408f705e2f64c0e90841c0717906cd656cd9f724838f9f255e9e9a286`  
		Last Modified: Mon, 29 Dec 2025 23:50:15 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:55c5890084b8785ecf5685b060b64f456115fe8bbdf37fc430cff9b6d3e1cb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ac745515171b69b242c3cc01512ee2936511ed6b64da9b2326612d98a67b7d`

```dockerfile
```

-	Layers:
	-	`sha256:37190bf2e7aaaa075c57fa2d57ecd973617c569273a483609898c217e8d41b79`  
		Last Modified: Tue, 30 Dec 2025 05:08:13 GMT  
		Size: 3.6 MB (3590058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8561f8d2ac527f758f51477bf8309a23321a3b4c4751681c14b0f456b8d59106`  
		Last Modified: Tue, 30 Dec 2025 05:08:14 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
