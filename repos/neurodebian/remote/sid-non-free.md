## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:5f6478a82799df646eaa58451762efdd50ff1ab828da15f5c266a9cdc8c0fd8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9b8b4e88733e4893880bc8cbf1a41fbe608a36f003775a107ec9b16fa1e4ec16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60346634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1668fc8ccca7b15da32ce17f9b81d0fb7e5352afe373f4d3eb1cf1bb20b8b015`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:26:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:27:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:27:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d8aecb4bc7b9e58c615fe5a04f51a5710114ff668af7b4f56dd368d492375e7d`  
		Last Modified: Tue, 24 Feb 2026 18:43:47 GMT  
		Size: 48.7 MB (48666927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983986cc5daed267e991e5ba174d898df58f07ec4c9a81b20cba4c1999e9c001`  
		Last Modified: Tue, 24 Feb 2026 19:27:08 GMT  
		Size: 11.6 MB (11585550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17f8a66bd580963d48d52b2b3a75e86696d00989037bf1fee0cd5b5800f6c0a`  
		Last Modified: Tue, 24 Feb 2026 19:27:07 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d13131a28adade66cab09bc31d3a3ec65cb74b77e50b4d4c31cf691fc1bd52`  
		Last Modified: Tue, 24 Feb 2026 19:27:07 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59225212c6943cbb079065a9706edf5fb74d3dbeb018d96db3d67908941607a0`  
		Last Modified: Tue, 24 Feb 2026 19:27:07 GMT  
		Size: 90.8 KB (90837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cfecc1d4b47a948d55e3647930547d7bc9d2e725f0d3083bf014b37de2c69e`  
		Last Modified: Tue, 24 Feb 2026 19:27:08 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ecdb1fab8942ecfb2cf0ccae4c06fe72ac0d2b7195b78459ad6732f75d8a0a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f269db4364c578376a104f2fd61c91130f9b184a656fa662ee7ad7cf6d9694ab`

```dockerfile
```

-	Layers:
	-	`sha256:774c72fad2c4d3a7d58719d9649e90364fdb68e2532ce8ad88fddb318ed2b940`  
		Last Modified: Tue, 24 Feb 2026 19:27:07 GMT  
		Size: 3.6 MB (3604839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3432733643b03e0bdd59d4263571b4519e5123a720c767a01111cdd74a654baf`  
		Last Modified: Tue, 24 Feb 2026 19:27:07 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:701d8323e411b8c7d2b865ae8baf8990ab80b36cbc20d7510038ecfc32077c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60091139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abf252a11f1810869e32d49d2b730536d5b5ead30e5b9f54a10e3bc8b0e068a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:31:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:31:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:31:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:61a95a2f6784ce634817550699b53ea6f85b093ca9ec55f99c5217b534acfb51`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 48.7 MB (48709262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad971ca2cf643d7c525791484feda38e04dbce81ea271ec06da0d35a056b93ed`  
		Last Modified: Tue, 24 Feb 2026 19:31:53 GMT  
		Size: 11.3 MB (11287027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffff0136576c0577c8d184df685bff2c2e9b2067034363083488faf11dd242a5`  
		Last Modified: Tue, 24 Feb 2026 19:31:52 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b498e0dd6ac6bbed19b5be5859d876ca6ee3c1f7668ce6f45a5fa119504fa5`  
		Last Modified: Tue, 24 Feb 2026 19:31:52 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e3206457e808e1e2a8a944e81f97eb40b1bc795fe5b5e5c9662b31aff0ecd1`  
		Last Modified: Tue, 24 Feb 2026 19:31:53 GMT  
		Size: 91.5 KB (91525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bad8e52e9ae94cfd6d1b42b5c082753ee92c5cbc21c4b4cdd03a7762de5e7d`  
		Last Modified: Tue, 24 Feb 2026 19:31:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c3ba3ce1cad2be64f6a53ebb22e85d405b867cbe80d4ae1b19abcc39b3ed57d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f2100b9bb6b47cf0efe84a777459619af396e51fdcedb82da0c0b55abc9625`

```dockerfile
```

-	Layers:
	-	`sha256:a183acc9226a54c9fef876a1fad6568c5d4be66c84abcb56c5536c888909839b`  
		Last Modified: Tue, 24 Feb 2026 19:31:53 GMT  
		Size: 3.6 MB (3613102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cac421205b406f1f4bfb5c5c46aa71d5657f19715554ed87fd10605447ade175`  
		Last Modified: Tue, 24 Feb 2026 19:31:52 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:001f9f8991e5844cda6427393159ea5861a71331c6df48cea1094b5dab5382bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61943507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3eff64a25f42e6f1a1afc939e8fb6a7b275479d809ce850d9ce318534f9b928`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 19:27:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:27:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:27:13 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:27:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:27:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:def456773a4aeca49d4b978ec8b12f148f201cb7cf9c2174e05e9ced13435b6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:59 GMT  
		Size: 50.0 MB (50022115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e99812faf86d8fc4a71cb41d2cdafb746a98b36a3dfb99aef2b9745d8395af`  
		Last Modified: Tue, 24 Feb 2026 19:27:24 GMT  
		Size: 11.8 MB (11826981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec990ed8e4ae5c803f69db7c65d159f49648fd281d828d678e04d4fc0fd31038`  
		Last Modified: Tue, 24 Feb 2026 19:27:24 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224ff852816d65da8f9dc02bbb73fac2000c3fa6cdb0efbc878d2ee2a05ddabb`  
		Last Modified: Tue, 24 Feb 2026 19:27:23 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a8fdb0f882b158b27ee9e47b185a51ec513f846999bf2265515e776f2bdd5e`  
		Last Modified: Tue, 24 Feb 2026 19:27:24 GMT  
		Size: 91.1 KB (91087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0991d1a5271a389180f96ad4fe4b66b8fb4a31c1f49311923288d99ab9631c6`  
		Last Modified: Tue, 24 Feb 2026 19:27:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a22b865f93fda39c0a326383c88266bd40690445851aa090d9f0c6dd28d59391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093314fb2fabeb49771dfd951c7f02300846a37b91a9f5373a68004c4bd4bac4`

```dockerfile
```

-	Layers:
	-	`sha256:c46479d220bf3c8ed769bfd4f490832f3c38b0f8b7457a9ce5bec2486eff676f`  
		Last Modified: Tue, 24 Feb 2026 19:27:24 GMT  
		Size: 3.6 MB (3602784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d2f07f9b9fab82eabba76c4f53469e27200d0461f16be04d1bab443a1ef079c`  
		Last Modified: Tue, 24 Feb 2026 19:27:24 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
