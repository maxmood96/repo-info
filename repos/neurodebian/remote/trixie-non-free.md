## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:194fb31ad792baa783c15b32c26b5fbf421b824520a7206fce9ab548dc455a9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f9de03dc15e6ea47894139ca860bbb7df3077eab69fee2b7f574967ad636e9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59673092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36ae580edbfff25806f71d9e496b6985ec835b7fd8a4331978b9aafd98429cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:02:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:02:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4a3e55a52a3bf7a028c11cdd04765722bc5909c81b4d67215b6fa19d3e51a7`  
		Last Modified: Tue, 30 Dec 2025 00:02:19 GMT  
		Size: 10.3 MB (10289887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b144061b331bab67819cd04897b89738b7005071a8f0875b77226d420effb7`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49967f5f696ae80e5840802cbcb2bd1f5e73b290f75172b8fcc962647c0538b7`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ba8cfd8ea320a2d392ad2e66f06a7a61cdee8570bad69c5e59e12d224a8bb4`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 90.3 KB (90266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55878b042946a13598f4bc44dab8bd8b5c6cf92a29a5f88dd01768154044ca34`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:542fe53f92c587702cec1372b3bafb21975558dfbeb872f904af747a99edc817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad7da224205c770167075916abace896d69b70e42afeb45c22180a13d042950`

```dockerfile
```

-	Layers:
	-	`sha256:c281aa682144cfe81a19cf027fcc803adcd513786f32a54c63545a32824764bc`  
		Last Modified: Tue, 30 Dec 2025 02:09:34 GMT  
		Size: 3.6 MB (3613069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa707ba4df079680f05d88b1e02fb0f6aa7c05fc1835434c541f175e0a0ad6c9`  
		Last Modified: Tue, 30 Dec 2025 02:09:34 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:52252804a1c2803a046b7458af3a67b1982db6f527659eaa683317a8d0704c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d283cdfd359f8c32663dc926ca67419f8a476ffbc12a174e8172b39e9d52f28d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:03:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56e05de75caf223c899f57bdb45b54d71c3938e099e2fff63698d83c6515769`  
		Last Modified: Tue, 30 Dec 2025 00:03:20 GMT  
		Size: 10.1 MB (10073442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a034755a9ced70509ae5e0173325f4fb3174e73369ad3dc2a0bc0ede6eada`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370de170d9d2bd026322648863277da5d88439f4c023954ff3d26321f8995899`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5caeb08aa3984f98b10526c397fc882cf49ca878092e1ed0a2694b29f74951`  
		Last Modified: Tue, 30 Dec 2025 00:03:25 GMT  
		Size: 90.9 KB (90916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6250ad169fb763f2e49938340ca45af94a4284570dfb659a3dd2df016500f84`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:deaa6d6c962198eee187acdc117bcaf95cf20c5fa346b8bd13094f3981e74053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068f0dea854818442fbd9729cba1275127ce475030eba6ea6efd526437a4fb78`

```dockerfile
```

-	Layers:
	-	`sha256:892de4cfc5deb2e9340d4e17d825664258f8fa9bed32590cf1722dd856a82e8e`  
		Last Modified: Tue, 30 Dec 2025 02:09:39 GMT  
		Size: 3.6 MB (3614596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e515d0a2d41c8e48b890fe2c645ee20c1d65a39b3c49ac8c1a7315fa7e210b1`  
		Last Modified: Tue, 30 Dec 2025 02:09:39 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9b0e1fc75b7086e03028ded7268c930996566f27ed4ebe6986af4f4133852085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e8fb8b1115e8d1a034795321da0945d8141c676a3af169a36a251306f32010`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:49:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:49:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7ba68d5e03a08e607fe00d0a9f5d3925adc34700fc401165e5513c0d55ae9d2e`  
		Last Modified: Mon, 29 Dec 2025 22:27:39 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15d4727387b490529c60959b462d5ff808d069f42adcf8698cfea8eb42640ba`  
		Last Modified: Mon, 29 Dec 2025 23:49:26 GMT  
		Size: 10.5 MB (10462960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cd6a742b77687a3c9006dbf6a6b2a1420e4141771fc5f88ffcdbf45835a1b8`  
		Last Modified: Mon, 29 Dec 2025 23:49:24 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29861bf8a204c31d9556b106a0ca46fe104ecdcfe3a93b688f4752ca29f3bdb0`  
		Last Modified: Mon, 29 Dec 2025 23:49:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3e0f83298994d66e574410ccd0d07375bf6a07a902b2482273abed9ea89a26`  
		Last Modified: Mon, 29 Dec 2025 23:49:24 GMT  
		Size: 90.6 KB (90570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a97b46437a35cd110763f1f91999cd83b1935dc412cdf2b375a365bfcd30a7`  
		Last Modified: Mon, 29 Dec 2025 23:49:24 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a0a0dc5eb10d284d692f93ed734b454df4525a036079f340fb0daf438c7055d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539c0bf44b78b00ed93f5b088e77d06aa29fdaa46fe707092ef39876c687732e`

```dockerfile
```

-	Layers:
	-	`sha256:2c7193ca00748f91c96548174e8c2ee3aac799600ef52a40ce0263978c45d83f`  
		Last Modified: Tue, 30 Dec 2025 05:08:49 GMT  
		Size: 3.6 MB (3611018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2146d807b62383b9bf5a4bccafe54d1ed5eb88e80bac671b63e4cb2b9e850546`  
		Last Modified: Tue, 30 Dec 2025 05:08:49 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
