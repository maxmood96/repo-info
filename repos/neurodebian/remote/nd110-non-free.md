## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:006bb654698876390f6861a0e01bc503f5089f6e891d33d3e93608e93295b9b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ed53fdb5e8aa47b66a22d8e538658ebad6098cf08a563bc4364b74cbaf364af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dc7efdb549d31a79c7a7c2d7d9835c314a974733e6e4bf0eace26b5e2a4b01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fca013c373c9ce58b6cae21ac454c7d47366050a594e13b8250f10afe79b75`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 11.1 MB (11105101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5638541c3cf3d2a86eac6c5fcc3ffb9b67a57a9bf46c7182aa0c4e311665bdb5`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499ba193c40041c0e5fa201d166aacdf33b0beb97469f81b7a403ada1b74aa64`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc132915d360c4f2d791549fd2ca2f013a650e235933b950b6ea0d7fffde166`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 101.4 KB (101370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d96ede1e50978e8f730ea66b147365e342f86943fe800c73171995596daa40f`  
		Last Modified: Tue, 30 Sep 2025 00:15:32 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4af9a206596649c0e27466361f63c4c1a81826669a33c4bce29a21db8fb07424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c73b451f85aca4ffbd5a0ea300b70f779265df1295afa1807295ddbcd3dc7b`

```dockerfile
```

-	Layers:
	-	`sha256:d9759dd16036ea272c06141d4b727faa571738fcb11840b1e3f52dddcaf0e3c3`  
		Last Modified: Tue, 30 Sep 2025 22:07:38 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b0a72aaf5eddf29cbac0cfad24af7f1f15d3cce4607ecf2e443ecd47fdd859`  
		Last Modified: Tue, 30 Sep 2025 22:07:39 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1f30c996b1974cb30d1db39be8e14d35af351b8c84dccb11cf951e3cc9d9f1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718623496dce620b8a091b46c678973300bfa6e35ec5b7adc0220eaa71a28437`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e503815c3695e065c3bfebbe02e4ca6522e055f3d2811a15fbf0f7e671f7fe9a`  
		Last Modified: Tue, 30 Sep 2025 00:19:14 GMT  
		Size: 11.1 MB (11106034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f4b86a4499aeaa235b1bb5c60fa3f1f0a538facfee71bd3bffeedb937421b7`  
		Last Modified: Tue, 30 Sep 2025 00:19:13 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7c071199696c6bc66c27249bba23d3d61056f23bfd53331e3490c87150eac5`  
		Last Modified: Tue, 30 Sep 2025 00:19:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6374e812d78ea9095cd594a1ab8c52c5a1438b0e9701b7b90c66ffedf3bfbb15`  
		Last Modified: Tue, 30 Sep 2025 00:19:14 GMT  
		Size: 101.1 KB (101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d983cf93511e8b9e722d857bbb40a47af2452461f6c49fafc915752f11dd59fc`  
		Last Modified: Tue, 30 Sep 2025 00:19:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aad05f3c3dc155bb3e1cf0980fb82714fda5e4ad24ab9e3c31b7b0271f23d4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6776e87ce097931b04f1195033a91a66a08f69df9c7afaf23fd077ed706a38cf`

```dockerfile
```

-	Layers:
	-	`sha256:f149e404fb039204918eb81df1083ab7710e02a97e75ad9a80312a7ad77fbb99`  
		Last Modified: Wed, 01 Oct 2025 13:07:33 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d584879ab879bad46254130981389b7b21180def03e30acc6871281df46d3102`  
		Last Modified: Wed, 01 Oct 2025 13:07:34 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4eea0d4fd77d66b5b2802a7722eeb5fb2109fb7a02966f5d8635d076cda4536a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542a028b735297cf6aaa7fbc7248c5fa8f08bb0f6a5152c346243217df1be188`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ceabdec1cb201cbc144cbbf99606ecccc3942e0acc3ede261d7cced4e3f632e8`  
		Last Modified: Mon, 29 Sep 2025 23:35:34 GMT  
		Size: 54.7 MB (54699245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3377e521b27619564766572ea2f71b3559921ec242fbb887b220fd8413a3b667`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 11.5 MB (11500396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f01d1de35df3c14a84ad0035183ed7c1104b2e5f80f45b2a9683829e522e075`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8509e7b4bc6ce3aa5251a6dae3ad32ba389a23454d4b7adcc4c92228bf4f98fb`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac8c536f22ee766f2f5e553467d1f35b363ded878c8e388bfe44b6499783cb0`  
		Last Modified: Tue, 30 Sep 2025 00:22:13 GMT  
		Size: 101.3 KB (101271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e1e7d055597b7ae7b2fb8e3c043ee71c83f9caffb518b6a538a65f2c12f729`  
		Last Modified: Tue, 30 Sep 2025 00:22:19 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:99aaca37cdb012e66ae234bdb48111ffe493f7bf2d722d6de4fdc301d88509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337428655da965ead524ac77fe7953cb70305e76c5a4b1741367f923e55a810f`

```dockerfile
```

-	Layers:
	-	`sha256:c18dc37b060df10df4047be8729a361fc8895477639ac9b8c869cb13d6d9a49b`  
		Last Modified: Tue, 30 Sep 2025 16:07:45 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d12e9ab20c1ea4a6f193720b7539452b9adcc7655702e761d5bf73575fe789`  
		Last Modified: Tue, 30 Sep 2025 16:07:45 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json
