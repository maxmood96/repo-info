## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:cc28a6809b96b66ae6f2143bd27abdb80520640edab13177d7869cce03d35ad0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

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

### `neurodebian:bullseye-non-free` - unknown; unknown

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

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:49cdd86d6094082e5c0b91aed3d41708edd31b2f433d55c9c6dcc85b20f4fb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63458023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479a5df7e493af38146eda3102fb71be7d6f336ee13b7a15319bd570ad7d152d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c495a26a9e4cd1f21f84bf5b3c134dc31e3169cdbb2ae21932a376b84c9af`  
		Last Modified: Tue, 09 Sep 2025 06:33:37 GMT  
		Size: 11.1 MB (11106011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd0b9d570ec2b080e33923af86d5f54c70cda76ed17161bd32a317ed00cd83`  
		Last Modified: Mon, 08 Sep 2025 21:47:08 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b48960bf6dc0d4e10f5e03f55c3a95296532ac622dd51e994e008d06ad396`  
		Last Modified: Mon, 08 Sep 2025 21:47:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4857e517b1c8570a0d32ff53cff06abe67744f65132d9a630d0987ba3304287`  
		Last Modified: Mon, 08 Sep 2025 21:47:14 GMT  
		Size: 101.1 KB (101096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa383623dc759a311dd6aba320a62daa8abb69707532e9c8b8e2a7e5662d218b`  
		Last Modified: Mon, 08 Sep 2025 21:47:18 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef64147d2a71637e0a769c0c5583af824cba73f5b6feeee0e9a80923f21b4773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8f10e5af3373299468ebbaec3cf5b3518e41b9837db3de6f26ff00a11ef918`

```dockerfile
```

-	Layers:
	-	`sha256:585ea56eeb16979083d627ff907af00959a6ed709cf48ed9de0abfc20e515c78`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2584dc1bbcd66f1c97c5f0904ab94a886650d24d982a46ae6812c2e864a74946`  
		Last Modified: Mon, 08 Sep 2025 22:08:17 GMT  
		Size: 16.2 KB (16176 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

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

### `neurodebian:bullseye-non-free` - unknown; unknown

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
