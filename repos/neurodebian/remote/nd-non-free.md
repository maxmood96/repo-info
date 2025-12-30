## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:317060eee8a6211519befeb2536466a45ee7873a63a6cf9184a216e68092c030
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
$ docker pull neurodebian@sha256:8e836983d8ef8af9b77b72e439f8c371405a985ae951915e508cacdf4a304887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60527842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8bd8e109166c8ab6131500dc2a65312eb0f2e7a0531b090d7e5c49e83624e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:36a4985327850927961426bc6fcb1fb8dc1f9b5e7f69f8061c7daf2f4aee58a7`  
		Last Modified: Mon, 29 Dec 2025 22:29:41 GMT  
		Size: 48.8 MB (48821118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a76feb401b8397b66d8f4ee4936caf4ce66640e5ad62ce2473a4370b983974e`  
		Last Modified: Tue, 30 Dec 2025 00:04:46 GMT  
		Size: 11.6 MB (11613267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4349a5f502c1a41bee3f9bf35364bcf75672e22eea699cf80c9742688a9bdd9`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1275f6a063430aa6e6996dcdd80dc6350cd45a3c55323e8c72a3d7f93c7ab857`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecf663483821f0c91f02e7906d1438595ba40438f653018436cb2c42eead2c0`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 90.1 KB (90133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01e8ccfe03ffa296f783478d077dbf0dc04351cd9d661d0d11173bdf4d7bbb5`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e2dde03b8446743a564589f52ad69e2183a9252feb374a8e65c51d5759d9b6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9f3512fc510055e8351d926027811d826fe487e04bcbe47540f3aa04f22947`

```dockerfile
```

-	Layers:
	-	`sha256:3bf02161c82deaa0c916d8c52dc679930df16850c8f23833ee058f9e94dd5bba`  
		Last Modified: Tue, 30 Dec 2025 02:09:14 GMT  
		Size: 3.6 MB (3589951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4666962ca4a0e7945f18ef88ea3a1626cacb025b5f89518de52002eede6468f7`  
		Last Modified: Tue, 30 Dec 2025 02:09:17 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a517ce131a941205f708b3d0db016d341984a51a9da4b10a3a4f792a41b64302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60160491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cd14e3fa38d095e6db623d1c695f978b5d759f00906273db739db2e07ccc0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e81a19d37d9900498b0ca8a841e2e3fe3dfde06146f7d10d1e71e1df7a8ae8ab`  
		Last Modified: Mon, 29 Dec 2025 22:29:24 GMT  
		Size: 48.8 MB (48801029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834c8f50bd273c3b0a7e017c0b2cad1be20ff06b111037ed997e1b7e6c74d504`  
		Last Modified: Tue, 30 Dec 2025 00:05:15 GMT  
		Size: 11.3 MB (11265282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3d5914282d0f6ff41770baa19a5d797df7b98ceee7055fe0306a26b4b0cc90`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7c39fcf0f25e352a9f478db51398f77c3977758ef5e7f4651da4740f38b6e5`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac86f94f45a5f89d87e751860014d3c51dafdc0cceb4980f31e30c5154808f95`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 90.9 KB (90856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4149473e2827caf5858b119dccfd23f16d508c25dadd652c6dc5402c067a013c`  
		Last Modified: Tue, 30 Dec 2025 00:05:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1fb1bd97e59cf21d0763d7ec666274764119ad57b35bfa3ae21a888a6b6ab2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b617c4be66c925f9ed0de633f487fd9131079ab60e35c2b1f0e31bc1b0dca1`

```dockerfile
```

-	Layers:
	-	`sha256:f48cef6f3cfd0ca31efc667f4faed7db31163b52a638ba7e96feae0b216d00fe`  
		Last Modified: Tue, 30 Dec 2025 02:09:20 GMT  
		Size: 3.6 MB (3590827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89bee813be1895a2e6cbc85ebbcc9b2756e96af992934777f53b651b4667b93b`  
		Last Modified: Tue, 30 Dec 2025 02:09:21 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5a29cfb436240c48ae82c7d58312c32f69718d0214125d90fc2cbc5a909cebaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61791287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ddf16f7e2b1fa2a4187129febad3fc9dc5ec4420a33a8563ee6c6934a1ebe0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:49:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:50:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 29 Dec 2025 23:50:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f17a69092f61f8d721afcb2893fe3fd9f89bff73ba6442fc317604ef6ed50dce`  
		Last Modified: Mon, 29 Dec 2025 22:26:26 GMT  
		Size: 49.9 MB (49939146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe52143281eeca48823c1e49c78c258c7a8ca3450943cc8c2498074e4c5f8dc0`  
		Last Modified: Mon, 29 Dec 2025 23:50:19 GMT  
		Size: 11.8 MB (11758281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba39c42dd57a2c8fdd46b06019c39004e71e6825a676cf68d2df677da5cbc789`  
		Last Modified: Mon, 29 Dec 2025 23:50:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5114c80057d2ba07ad9d6c3fc3130ed9f105aaac8c16365a847f577d24ae438`  
		Last Modified: Mon, 29 Dec 2025 23:50:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8bdc2478c0c57ce1ba67f5b76dc68a72f87f32cb427c7a45b701f9deb678b5`  
		Last Modified: Mon, 29 Dec 2025 23:50:17 GMT  
		Size: 90.5 KB (90538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c826d0f3301bef592b7d57d5fc15e85dc97e89aa54739547ff69d237b9be308`  
		Last Modified: Mon, 29 Dec 2025 23:50:17 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef3ad199b1ad7337900079eab6156c42521ad941f4a8ee03e12b21f0f3673b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26fa321ead56b848bc398750fa92def060b36adf6c242c1e327962696f67801`

```dockerfile
```

-	Layers:
	-	`sha256:c0408f9d49ea412f64c0a5f217240c303a3ccd4ee47c5adf1dc0f18b99dbd999`  
		Last Modified: Tue, 30 Dec 2025 05:08:32 GMT  
		Size: 3.6 MB (3587909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b960bd229507b51aa79f0b100f5e8746bd35218943a3e530f591eb5e6a09e436`  
		Last Modified: Tue, 30 Dec 2025 05:08:33 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
