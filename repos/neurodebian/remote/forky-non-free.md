## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:0d1093c78227a5e6644478d81d5dd483f069a3187350384f12b58a2e5ae9ea9f
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
$ docker pull neurodebian@sha256:cb78772f90833a757dc6802286e148cf3c5fdd530666ccbac0f50d07cd172653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60159012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2defa8836dcf6459cf443a2e3c73a1fd010958213510f963cd5c1931d8a97569`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6776c7f73607461d5327de460aaf62de8b210cf5cbabd275c1527eff4955c3a`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 11.4 MB (11368639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fbbad51860c6c845e5d68293c56ed4d8041346dea6accc934bfd7afa5b04ea`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d47c55cd565e841baa3ec307cb01da37a958fb06b13982b82d4e1f04004da1b`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bd9aacf74bf4e163d7b40d6119ee3d8d48b3b2cc7078db0ce2a4c407aee1e9`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 89.4 KB (89368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7587b914565a5c0df3372adb2b48d808f6dd8d77481e277a8328669fe85f5a2d`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9fe49f9a5928025f88824469880a77736da4d7fd080ce7922107878270963dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad29b1f5f6319081ccdb52337076454a4d4aadf77bd661e55aaa98e33f4c32f`

```dockerfile
```

-	Layers:
	-	`sha256:b505af5a4b755ede91f3606295650585caeafcd0f080f4b5e6a7ad0bb04fedef`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 3.6 MB (3553195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfe9ebd24f1ab7fef1b09817ad0758a918d9b82241a822a3d85aa1887562effa`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6d7a6edd87813c48d375346b592699af2955f0f278cc312604805857a95aaebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59891975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6831f1fbeaf0cdcee9d00103c5ca7c213f3866eb8319ba76e6c877144ba19992`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:47:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:15 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:52be3b7a34a0f7d63c36fadfd1767c3f064e11b65df7fb6243fae9b94dd9f7c8`  
		Last Modified: Wed, 22 Apr 2026 00:16:24 GMT  
		Size: 48.7 MB (48726104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f336c7b8d6a171e1ba01081442a12e792d77a568986ba209c9900dc791b5f51f`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 11.1 MB (11072548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00987222f36f6f8bd0a2550c59b0ac95c7b6366478f8fa574c9754958fec4b1`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cecec54a68e2d16c3c71a28eb7f95b5f390342c41b54d106a429ca35828ae6`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97bcdd63d58b53bdbd95358360b21a312367b268e808cf231e17a615bfe6eca`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 90.0 KB (89970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39283d2169655980d2ce8369af2c8c0e93a2ed385dfc17ac3345ab676898f2d`  
		Last Modified: Wed, 22 Apr 2026 01:47:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dab52e5226ca2bb1cbc353608b25cb665bb16d5385cbd9355942017c10ff6179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd717cc30fe1dc636877e07191efea9e7480004ed7907ce36643e559442da151`

```dockerfile
```

-	Layers:
	-	`sha256:a6bff3b434305a1949b393a3635d16e90e881bf3f7560f921253f54deb69275a`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 3.6 MB (3559180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a68a912c8c8374f021c1329e9fd2bafb5b9d9b174b468cd2f78e3f36e7d2c68`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9bedad4528e45438d1623fafecc7ebd4869eb410b0dbb85e4a82aef61511431f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61577804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6518c25eacd6983972f820d07b0b03542e361c4746f0212991a4ab16af0c24ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad078a61f6e4be70ba6616078c3a30d7878e3c52bb074b890ccf08d7ba6c0c01`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 11.6 MB (11606394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d033c8c40129bbee090a07f5e1df4ee001c1ff1b1fd1e0e8fea876d4dfefe77`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6602b36874f6c218ec4f391df4b2e6eb6c4bfd9979f4f111c5fa69b47496ba2`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d50765ea499d27dee96965b634aa3a32c0fba2532d7f79e39a9119111c42be`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 89.7 KB (89666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedfedf99f96257ae9c575d353d0f5d352b036e3a8c97cf7a608eb3837152eb`  
		Last Modified: Tue, 07 Apr 2026 01:49:01 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4750e3e14c0f736243e2236c09b7da62c1b16042e8849a8a4da7588e6081eca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3479307f59614f39eb4a0fdeda1168462dd3a6ab17a49e6e26b68882d8a5e8fb`

```dockerfile
```

-	Layers:
	-	`sha256:e0ded4254441e42d507739c92b200d27c9f0e81de4f3ddb5ef6bdc0428724d01`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 3.6 MB (3550016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aea253b22bc3a5f64020d8dc3bdb1ea14d6dc3aeae1db43327b6b9d33432be8`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
