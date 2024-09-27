## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:76657de75d2774ad7dd62dafb1bbb46c79a8a1837c2c8b049f675d7aa4f4cad4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:c8664a96795b166095b204fa54dbf0f48b5e6e4978643e8b763bb7c05b2dae1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb0c3b1ce774b89533bd30de564feff9ba4dc520f740d46ae423bc2653ea8f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffec6389bcbf6537d5f6a384d29b76f4fcfd4cc7522491bbc0e1e95e5c3eb722`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 11.3 MB (11266554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc93f4d62109e8a5d2f564ccd69d7bef7d80a32aa7a410bc6363888daa816a5`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d017be4b2180bbb56d6789d0382e398768bd1b3e8f19973efa1578db0296c75`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9ced1a1a098fd13cc5a63fe69b80bbeb7435fa6bbdc8331b130d68a6b87ba8`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 93.1 KB (93127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9f8466efd911fc1b98e6f430f3b1aab449dad4490a17f294deec380b6afab020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78075cb443a7999c807e8fb4699f6f1c0086f081b30c2d93be94680e05390300`

```dockerfile
```

-	Layers:
	-	`sha256:f1b4f0b3cc2badb64712a79a6915ffb632e856347854c52ff14ad2fe57846900`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.9 MB (3924252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69c5d58fafb7ead8986e2f8e1a098fcb901d06df3df04978588846236a6382f`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c345a247dacdd96d613b963e2e3fdeb72161e5c0f5a7740992bdb9e008a4ea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60913243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e470508b10c079f238639a81b1a0e47c435bf1a64e75213f6cfca87fc7ab16`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1407873c66503c0a93617924a56b4dd8e307ce2f1c2584c89a9fa1fdb32af2e5`  
		Last Modified: Thu, 05 Sep 2024 12:36:08 GMT  
		Size: 11.2 MB (11232270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71660075504871b9d383826ce5d80aeeafa0f24ef0d028e8c70c2106e2f40295`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9920d93d230ac89732db5e1368e9288d33ab00280170ed41ef415abb19e20b71`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80251e079aed2b00cf9612399cb10176c8e0143d29001b61c7468a9dfb9ce708`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 93.4 KB (93361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:be69dbe480fdadcaf18fadf575c4e568b8081c443cb058d2a983ac699af38c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809742a0e06d624313d6f4f95410ae5632623b4128683f3d68bd1a3a3c84c0c4`

```dockerfile
```

-	Layers:
	-	`sha256:12b6df0c491b4c73165be2fc940f2b5c7fa177ece053843b76b2ed5eedd97450`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b2553d87c1a9b1095a1a7cb0019d4b6626d96f473703640f98ce7e46bc8ed3`  
		Last Modified: Thu, 05 Sep 2024 12:36:07 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:1f762b90a16539d08e371cf9704aab60d8f8c3bd95c833c50e21668cf75d57ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62358760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ac852c496b2f0a3d2c1faf2f58f6de35195ce64fb3ff870ba31256f00ef489`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7919eb19b12c4b3fd8c8f9fcaef0c8c8df9e67b237eaf93ea5e98cebdde9abf4`  
		Last Modified: Thu, 05 Sep 2024 00:09:59 GMT  
		Size: 11.7 MB (11688944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba9b8b02a6740c4da8a43dfff05dd4473b4cb8ba489bfd5ba06c1dbd3285fc0`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fe05c6734e5dc50476e722cc57112d104c24e75fa204f8dd5066a7c29c59cb`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8c07cd6938f90cd62484a4e934e8fe7ade8182db8af02e6eb697cf53ad89f`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 93.2 KB (93222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4912857a7eec07b09ab0a4fa3da525e7f87d45f9af9f5eee2da079179c129abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23220b0a9fd93875caeee52955614a1b33f553ad4f6d378f2db9f8b784bb00a8`

```dockerfile
```

-	Layers:
	-	`sha256:9972c1ef7979b6a6373c836cb171ac20e39fe3638963c57848b4f6b0c138da8a`  
		Last Modified: Thu, 05 Sep 2024 00:09:59 GMT  
		Size: 3.9 MB (3922156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc254bb1124e09a0866605b00898566346278bdda14bb13896928fd3b65b85d7`  
		Last Modified: Thu, 05 Sep 2024 00:09:58 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json
