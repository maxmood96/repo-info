## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:a1a7eb754cf03efed037b8b4fa2152d9df87a9f9413c2feb558b61ef27992761
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:ccb1c49417bdb17839ee4faca82395fa33b144408227ed3a0ab93c2bfd7f10dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ff5a84cc8070c6f3751ad1cec4b2fe69f8cbd3d073a98d31b12bc6e26fcddf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c7379f1d27c60a35dbf8e3c0b5a3a47737a69ae5b22697d6e13a539cd9172`  
		Last Modified: Fri, 31 May 2024 00:56:49 GMT  
		Size: 3.6 MB (3622620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5ebf673575de9072e398f36efc89febc746722487b4e31b2a5b167070de657`  
		Last Modified: Fri, 31 May 2024 00:56:49 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7891f8c753aeaa72a7d70940778a23b11348f9285de4ad12a64d7eb076b9c7`  
		Last Modified: Fri, 31 May 2024 00:56:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb38a2a4b0a4055db3575ff7cec9b946b548973f374fa1e7cb459ca8b4bc7423`  
		Last Modified: Fri, 31 May 2024 00:56:49 GMT  
		Size: 110.0 KB (110015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6bdc07f79956602f0abd96aa4a4ec07d1f3bb03a34aa83c8b25be126821c3bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd2d22132481eadfdc656dec80e04fea67598dc9963907023710369cc034499`

```dockerfile
```

-	Layers:
	-	`sha256:72c59cb39b9edab43f4a8a3ef99f6378349744dd8d965e9f848c45b71eb2bd33`  
		Last Modified: Fri, 31 May 2024 00:56:49 GMT  
		Size: 2.0 MB (2015658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:125959a3389f5852c655acfa6186760dcb332558bea27f381f37643bc6567c9e`  
		Last Modified: Fri, 31 May 2024 00:56:49 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f543b59036464a59946ab9f73c998f71ecc609ab2c5ca2dc834af647bf8638a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31067211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f362e6117a66f67a5b0cde15ce0b8b078691e3ec78709d4ce540e2b08457060`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba218d1d7b661878c14487bced886a52a613db7b35be93fd5606033d2ee7cdb`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 3.6 MB (3594346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cbb193b892b230325e0954e37f9cc5888e4f5be69eac2c00586f369fa71eed`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b9f9da838e49a37d396367d4f8b41a6efa775664ae714448be35174fb50dc1`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f64b85fb3b544ce5bca4e7f032da3c58413de4c1e771a6265988ed8513dac92`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 110.3 KB (110337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9131086119189da2119fc9d99e995c97fdf410d3ca601e23e491fe8e5d6c0737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9ec91fe7e2d937b57cbf4d8b162a8c1a426b035b5c35b1fb4e27b983f9f278`

```dockerfile
```

-	Layers:
	-	`sha256:b09c69bb51cc9910fe5d3c1336f479b01906e19f21020f8966c5895bcf361bab`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 2.0 MB (2015917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc63a7363629720e2d76cee0af880ee53688d49b19199609270d58688489f6b9`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json
