## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:e0fbe001d3a08d53127effde6310c1ea79e1de80e6770a493f18d1c7dc6e7c86
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
$ docker pull neurodebian@sha256:5366af3f90a45684e74903e70210e4bb68b49d59276eb6931adce082b981b45e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60032010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d6887d14c2e11779df6cb0d4e30520f6e8fa717b31b551c6ce8b010c1f8540`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:92b4a1a651b0c3628297f7472014e3ecb5580ebbd73dd0616ae4e5d399ff0831`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 49.6 MB (49575035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7db97dff5175af40ec6025214bb079c09ac897f5789989aff24bb46c90af7f`  
		Last Modified: Tue, 23 Sep 2025 19:50:58 GMT  
		Size: 10.4 MB (10363736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7cd68ebbe1b4bb5790baf1d4f8c57c2b1c6566d79b9243fe8d96506c3abf64`  
		Last Modified: Tue, 23 Sep 2025 19:50:54 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f5aaf1deba36ade8b00c1b1aed3ce3cba5b662b288e95fcd9767641770fda9`  
		Last Modified: Tue, 23 Sep 2025 19:50:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8d3b32d3a43489dbf76579ccbcc3d6d10c549d0d0dd14e7f8967a18fd0289e`  
		Last Modified: Tue, 23 Sep 2025 19:50:54 GMT  
		Size: 89.9 KB (89885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610f51ac5bbee14ce886acdea59761c66321ae40ad41ec1fd151a64c6cce3c6`  
		Last Modified: Tue, 23 Sep 2025 19:50:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3fce87b257cf771d7bc40c767e0e6d6c28b3794633c996aae20121189cb1ded3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807259444ad74f4c97676e376b584b585fab817dc8c497e10dec98d27acf9d3d`

```dockerfile
```

-	Layers:
	-	`sha256:592b60b52129e3462b375f44c2cdbdd5fd57a1374a2d7c3e79d1d2e07d19450a`  
		Last Modified: Tue, 23 Sep 2025 22:07:30 GMT  
		Size: 3.6 MB (3609692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53903836a6b295d6e68e9f43596675d6bc665dbaae112077cc8afcf758cfb22a`  
		Last Modified: Tue, 23 Sep 2025 22:07:31 GMT  
		Size: 16.0 KB (16002 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:92b039616dcf059809b62e835c2ce1fb356f4cd490c14c863ddbb4f81570d2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5695ee1268cbe16821e636a6a6de9143f516e858fba50a8746679ac8c8e02f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:43c9f83b4c0cbba0c49dce5bbb999963ed78f9198001feb88e7464916cedc070`  
		Last Modified: Mon, 08 Sep 2025 21:14:38 GMT  
		Size: 49.9 MB (49863496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad7660c35dc9245a3651760544eb6d528a0717570b22435a069d38bebcd4357`  
		Last Modified: Tue, 23 Sep 2025 17:39:16 GMT  
		Size: 10.1 MB (10143297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dd4856fbbd8812c3c3b07b916f604327d04013c0b756c50d815b3737d5a3a3`  
		Last Modified: Tue, 23 Sep 2025 18:26:23 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b49b1700cbeb581584f2de01718799af245efd3c1972207bb7a4cb2cd586b`  
		Last Modified: Tue, 23 Sep 2025 18:26:24 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c05e31d8c611a15105712c9f93a7d834b93de603459f204925647c9e891abb`  
		Last Modified: Tue, 23 Sep 2025 18:26:23 GMT  
		Size: 90.5 KB (90542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b573a07e48b33f323dac37694b9a4a2ac7a9be42a1d64ffe538334c6725ecb`  
		Last Modified: Tue, 23 Sep 2025 18:26:22 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dc967d49f585f0360b55969f2a013216fab797309dfe973f1d413f39b39e2119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6eb2694ece8d67925bc06c1ac0aa05f71d39d9a1852f52a881473f433cf61`

```dockerfile
```

-	Layers:
	-	`sha256:7f44ac7080f4f07f4a92b14c9203b3500126b0a1a15a00e395e3678201cdac02`  
		Last Modified: Tue, 23 Sep 2025 19:07:31 GMT  
		Size: 3.6 MB (3611207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b186d8b4531db4698e1f2b80fe05e77d72e2ae2c9b558c2e1e3b38bd5777443`  
		Last Modified: Tue, 23 Sep 2025 19:07:32 GMT  
		Size: 16.1 KB (16142 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:715ecfa0220f7fd01738785f9c42ee3d2ac9b835a64a08b806a94b5fb6a82afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61660669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49c25b5eb4f3ce42160d048e69202a5b427df77adbe42bf1c90db6ae05bcddb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e46ba83d4247b0505c7b4e05b89ae8056e10eb07f4e445e17e2dc44b8c60b063`  
		Last Modified: Mon, 08 Sep 2025 21:12:21 GMT  
		Size: 51.0 MB (51049810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361bd0e810695bdbe9086ecda5df8904416a487bc5a0ab43e7495d3598650bcf`  
		Last Modified: Tue, 23 Sep 2025 17:34:59 GMT  
		Size: 10.5 MB (10517223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f39ed7022b30182eeeb2b6e84799ec704eb6ed39b6b25a8ae84f4484d7e0680`  
		Last Modified: Tue, 23 Sep 2025 18:22:25 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317b5fe370cd1003cd49347234721b59a8595b0d60b476ff8e76e2a2f020a38`  
		Last Modified: Tue, 23 Sep 2025 18:22:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea9c5768445e1715d5adb3c925a6337fe3629fbba9d4736c7300a995c493bd4`  
		Last Modified: Tue, 23 Sep 2025 18:22:24 GMT  
		Size: 90.3 KB (90276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45b3fdb11b8dbbc68f00e2fc25d31ea20aca0b0cbd042c8e6812b59b3619f72`  
		Last Modified: Tue, 23 Sep 2025 18:22:24 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7855e2a2d3a399325fa66efac0702ee6144d1103a4aab879ba2ef8db9a1324e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25f019bc15a42d275adef0a10d965245e5a53d609818d34d0f8947e18168294`

```dockerfile
```

-	Layers:
	-	`sha256:273801161af411b9ca75df5f2ce6622db20fa373538ba54a0c24f2c4bf746b18`  
		Last Modified: Tue, 23 Sep 2025 19:07:39 GMT  
		Size: 3.6 MB (3607652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6349aefa2276bd907a81a03bfa347913a3a681b8efd053e0e8aca34bc5e0112c`  
		Last Modified: Tue, 23 Sep 2025 19:07:40 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json
