## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:384828113ce018b109587fdbd0eed3455ed127d24c20f4cd7b567279f645e467
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
$ docker pull neurodebian@sha256:70189282e254301c784925ce371e2d46b8803e68c3bf317555ba516f7f30faf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60157762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc773844b4e251440616e054ab18d55d4fe865140e940d5f110fc8e0a61fd01d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:33:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:50 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:186ca733686ffcaca03fdc512b51c9498f39b93235775cf08154b1ff0b143901`  
		Last Modified: Tue, 04 Nov 2025 00:12:56 GMT  
		Size: 48.5 MB (48481364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2ed7e1eb66e73be7a81904f625e8af8e27bdbcb556d412220b4dd47da85a13`  
		Last Modified: Tue, 04 Nov 2025 00:34:04 GMT  
		Size: 11.6 MB (11583251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a2103db929aa61129b750d42223222a7b4692b76c2285cf0445cdad7ce42d2`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af62a6155153d6cdb65922ed9f2501a9399acd5dc27bd108f4abbeaf8a7ce14`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deca5aeb491ce74b8f40489e25bd1cb7d95e88698917d60cd807d9a6c68db73d`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 89.8 KB (89793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d896b07b7e37a7203598f231523daf17e786b9ab694595a4aff3f90eacaab6a7`  
		Last Modified: Tue, 04 Nov 2025 00:34:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bf76392847b143d89f63d547ccd03be8ce62c9af5bb9f0820a2cb949ff456788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfb5753a33312ff7862b3b9d32e1577419c78d795b37b5b5e3ab360f8743e80`

```dockerfile
```

-	Layers:
	-	`sha256:fb10025220538f30c02045c8f5d88fded55d77d4fdd339040983116e4d90af1d`  
		Last Modified: Tue, 04 Nov 2025 11:08:30 GMT  
		Size: 3.6 MB (3577441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b43e03910d7abc9bade8c2dd90b348ebcaa7ff7efcbb066f238608850dbf151`  
		Last Modified: Tue, 04 Nov 2025 11:08:31 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bc8ce6ed3e3c776152f99cb1104daea078494d0b923198a6c142487c62eace11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59936579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c69131f270dca8fcbfd32858708e9d91d5ac087ac5e89454675950b29f061c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:32:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:52d2706ca00f3431b3c37b306b3eb6cc4989781e31180bfdf93c4dd4108e1e3c`  
		Last Modified: Tue, 04 Nov 2025 00:13:40 GMT  
		Size: 48.6 MB (48583638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cd34f0ce98712d55741951246c28dc8f4fb5749fe6f009be810a15bc39e7c7`  
		Last Modified: Tue, 04 Nov 2025 01:32:56 GMT  
		Size: 11.3 MB (11259085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37370e1cb03e1aec0bca31b7c63d049563f347f1cbafba5f70d06d99e86b5dbe`  
		Last Modified: Tue, 04 Nov 2025 01:32:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17eba42e5d505fc3a5d3fd9987372e50964fc3542c2cdf1d4a193649b6d79dc7`  
		Last Modified: Tue, 04 Nov 2025 01:32:55 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b804357151b1a683a4a79a6e6c1980ecfd72123c62be18c932e14d3bd0684a`  
		Last Modified: Tue, 04 Nov 2025 01:32:55 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897b8e80528e0ef186efb3269fdf4ee30234c872372be7fa36d91d07b30d7ca`  
		Last Modified: Tue, 04 Nov 2025 01:32:55 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:47773bc2f2c9cf5068f8d72bdcd2fdb869f026c1927d9f695c39218b8917e292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767d0a3d4a306c0a128156ad9700a3ad79383bdacbd5764b54d4bfa729dd9191`

```dockerfile
```

-	Layers:
	-	`sha256:b40777566d143b66e58a9a658fe6e101d5e37c7b56860fb660b7f69556471886`  
		Last Modified: Tue, 04 Nov 2025 11:08:35 GMT  
		Size: 3.6 MB (3578317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30961153f32eea93b5027e2061824753dd9f37ace2199e650c0e21c4c49e8c64`  
		Last Modified: Tue, 04 Nov 2025 11:08:37 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:63d7073757f8af8afe32eadcc816f9af8a1235863947854f3cec2f8cf7759d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61637813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f76ec57eee1b56c541332f031778cdd216e88f6085d0c30b6e631b2600449bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:38:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bd86ecb6d3ac97cad4df6e0aeedefdf1790afb18f99112bd09ea68844e318978`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 49.8 MB (49809500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3fb4596c99fe5762ade8fb8b49b83646c2974bd279b25a5242783b6be97fa4`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 11.7 MB (11734764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a42eb16fe9637037091596145b07dbd6c26d5a89f0f60752ad47e9c6a4cc9`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c465762ff747abccb8f26f7940310315ad22c0fc83643d9a17eb2e44999632`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a908abcd3ddc1a45d84a8a1ee749cc706039c754ffc9b248a425d41c76ae1e`  
		Last Modified: Tue, 04 Nov 2025 01:38:57 GMT  
		Size: 90.2 KB (90198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1814fb1bc1df679152afd6fd24901df7384befe85816a664b3bda4f764d0fe97`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c777d330b6ca4603bc533b8b59a2d655e01875d5366fb0e49a18efb61c8a4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaf32981d88398acb2c6917a96cc42b7e3624895dc4ae282c20da5a261302cb`

```dockerfile
```

-	Layers:
	-	`sha256:f22f145d2d10c0e5d330f0abab2f7ca18e0529f5bb7a1ef06a8b9c9b96ceb661`  
		Last Modified: Tue, 04 Nov 2025 11:08:41 GMT  
		Size: 3.6 MB (3575404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c492288d345222064869611f8283ff114449640050c12d23dcde88c37772b53`  
		Last Modified: Tue, 04 Nov 2025 11:08:42 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
