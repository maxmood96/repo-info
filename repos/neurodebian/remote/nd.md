## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:2fddaff134d7ca3561871178fb51109683144c5ab6714a910003a8e6d0529a74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:b386e80e587d4c20ecf466054c921cfdc72aeb7e5502867ccdd6bac2d19048a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59631144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd3b8259795f4e2160852925aa7fbb7231a7e252c92696a27950f0303853dce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f475f97deaabc6193a3fa858337fe06184e11ad6b13315ab6c7f971b66a9bafc`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 6.3 MB (6287931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd7fed0f8636459064f9f964188e4826469f925ed396341fb68ce62fb315377`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9fec776045441161388c757e0ad726b5ab7fbd3548e03d22fa42b727e9b782`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e369688a9f2e20897b0342be14d8b6941a03ccb9fe3bb98dd6ddcfe4445ba29e`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 91.2 KB (91192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:822f4de5100bb1994064afb1cdd414af5247d0e87c51bb88c46ca6bed2dc05f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a37cb43875ddc7aa01e78a71637c84ed0a436c94162a5790e7bea0b07cc237`

```dockerfile
```

-	Layers:
	-	`sha256:8c16a39d93e2e784f37f3cbea84302594e573b2693f64b8b370f24ccf9d50237`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 3.5 MB (3542033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:503cf70ae76d49b40790396ff4fbdf7b5f3daaf8b7ca72be3e759ad8e79bcacb`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 13.4 KB (13396 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:58bfc8026888335070afa0f72044cdd664f87cf4b9aa4f26c46385c610885f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59958772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c27c5792cf7ac400d363febafbd72ae89764d94df31e0957faa9b3e6c9d75a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1707618fa9372fa7563234001ca06291da815e7c963e11719d290dcc36218024`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 6.3 MB (6270740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f92dac85afbe3987da72fdcff7499ef9a4bef39d0ea83f70ad579e421b2b1`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560ef25c1ef36b5b05dc1fd297de1698589349e5c080811754da6ab61635771b`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c67a14658f20791e7bebae65768af2451f13d17e95b1fa2ffbcd886802abb3b`  
		Last Modified: Fri, 27 Sep 2024 15:30:29 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7c1a8705a3413350f04f5a1d739bcdaf9577a3dcaba3ae5e1fa73e801f1f3060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53c580a80c3d5c1142885b2d547f026e496f73afa9516d55b492a1fd6e19aa3`

```dockerfile
```

-	Layers:
	-	`sha256:1236d910e711e1eb3ba937faaabef1ecbb76904d2147d9e237f9088e67d19501`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 3.5 MB (3543075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:383b288126aa4491dde9bca5f83e6279bfed5b9378f20d43c6e8ce721a75e949`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 13.7 KB (13671 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:8b1dc1ce8b5e8c3c34ccce9276cae70f96439f7a251b57b0d867562e4bb61c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60787262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb7e7e400856419fe6dcfba9476730e473001cdb7071f69bc5b2c70f24a3407`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7024eca1d35e4bf56690a81c3c1da49afee7ee27f30584fad073bcbea685f1d6`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 6.6 MB (6616326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e114f1c83df29eedcbf0676bad5078aa0615db7e6590d793bba0242195937669`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af5f6f47b991c182b45b50e4e4234c3e05547782c074a70ce4b5357d5c65900`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4229c9987c9434cde75f4619617a1b7d0b032708a7e4e5b415357838601309c`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 91.1 KB (91141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a1f9b369fb100fe194ca9bc43464f41bd1a6938a0a4815da6d5bc7a3189579ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d5866efd6fe0420224e5d5b639885adf9285db5a32cdaf1e966cba25ac2ebb`

```dockerfile
```

-	Layers:
	-	`sha256:a01afa53c29c892db3413fbdcc505cb39abe7e98a9a4ae0aa52c992c8d222303`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 3.5 MB (3539125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825884d205bb9ee0ceca812d5351085152132f2aa40ac72738cb9389bc0280d2`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 13.4 KB (13371 bytes)  
		MIME: application/vnd.in-toto+json
