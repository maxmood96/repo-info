## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:7dfc8a363c3b6e2cb32e9e2807a2a143dfae159e132d3b06b8fecac0382c67da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

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

### `neurodebian:nd130-non-free` - unknown; unknown

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

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

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

### `neurodebian:nd130-non-free` - unknown; unknown

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

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b187bea3f10f39ea07ee4101dc0a3f18abbe7be34d2cff2bd6f7b49e13f3155b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafef6df1ba7f540161567b41abc65dc5bdb8501cc5fbcddaf3cacc06c4bdaf2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:15:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4b33922c04dbc376b8a5e1f0f1e92e63bb89043733e9f1faa4310e1504bd7f`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 10.5 MB (10462938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288115e75d815edb522e43eef503792b7e9e6c88509ee7e9ba4a8f7072e4f953`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641aa24ee325190ed8096c6c9438150c637d751260dc4f24335265186be298f3`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30ad08df9b38bd944f88c550208c2de69c4c644bcc8a39159b8149bbcab36a`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 90.6 KB (90624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48e15f7f8648267c2768f3207e320a23c1769e635224feb1f62bd2181b3e786`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7406b4bee75ddf498b716c53bb3d974de73215e6a867b443f199125346ea588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84d6396779efcbbaa4d5ca3717a85cea53fa601f8499d1d5e4932ecd0830673`

```dockerfile
```

-	Layers:
	-	`sha256:9689b9651a4bdf918275574dedc207d7f9b6a4d8deb9f363c0f94ac3816b45e0`  
		Last Modified: Tue, 09 Dec 2025 02:09:11 GMT  
		Size: 3.6 MB (3611018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134c12f5888db88b0afd397425b7c86d8d384dd6dcfee36c93eb7abe2abb0f15`  
		Last Modified: Tue, 09 Dec 2025 02:09:12 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
