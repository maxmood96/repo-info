## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:2ae61745c247d4a8c99d7c354b96029634ef5bdc33733e5b2da4bda458519e67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:95b63a109fc48f08237b877fb7cffa77d61e8df22bf5a4d7791c6efd09c4ef8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59551601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe81e410768586b5492844badee22adc900027cdac5b1acf7b379c3a674edf9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267a7066a313165935bf4eaaa8b9aae312287191547d2809b4ad34773e828a5`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 6.3 MB (6280356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aafa6a0b3025fd4652316fc5e3fe6ea05e11344376a905017040b9b985cbf99`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5cb880e6abea22dd0197684015c78086ca2948c36925678e0bfe28e3465c00`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04bfec15b0903df67fad5cf467dc6eb0ca7d397677702389607bc4733e4fd4b`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 91.2 KB (91221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3320834de6354f493c1d82186351c117223665c2f4ead32bb77e28427b89eee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f4e2f5a80b3b29afc74f04e8902b4b3c96a67b973d863de928e9726e32f9c8`

```dockerfile
```

-	Layers:
	-	`sha256:a20598f20436ee588f58c36585795a38adaac735394605a913cfb849c611cdeb`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 3.5 MB (3542857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1088db98014479771d8f0b3f7e94eab159c63f2a9e60f1ec223437d6c43cde04`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e045c8722a0d09fb924908b53557b97d64b916b1e5f7034d0d5f9fae67d5424a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59971880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00daadd7fcf3264abc9af0febccd9a59cf1e87e61f9c621afb2b7d106794a72`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23f6352824fd96c8c6b9838bfb904e1d7622f6bfe55b4c553cbf57ff483a36`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 6.3 MB (6261488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c0a4b3a15644d2d672fb44fb7ef754851b4b999ae2449d908d2bcb61514ef9`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620d3e5d3b378b7be79ad19c20bfcdc40531f8bf0971a901824a5e8be8263f1`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dce128f9ff7538248e2b5e2edcd6ca43e5feea1880d5b8a5290a08534c4e63`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 91.8 KB (91807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e2a4489f748889ef85e038e010495eefa34e6dca07c0894d71860b17f81eb310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626360cf88fe014495b6a029a63b3915e45368305e7c9a89bb1cb126907c91e9`

```dockerfile
```

-	Layers:
	-	`sha256:542bbb008b88b55265ccbbf2227938f846127e85ae4c7737802a2427e4e3107e`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 3.5 MB (3543899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2b4a94f394589d2ff4a612422d51f4eb84d2ddbc340e5d3f3f6fe458774f1c`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:98a7bcbd0f48607aba203c188fc584d3eb2eb44a7972910a22aab506ba373691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60755232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c978744990dfb8d2fefe9889d4703ac1fd7df41317879cb1f5a804f0ebbeaf7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d66646f8689060ae7f27f71816fcf459f852eb6ffd38e84da1a7977af7339f`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 6.6 MB (6602168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499956c24221d0887f18337dfa8a40a66ef78ea9e5070296934feb3bfd7d4a5d`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7116eda93782aaaf1afc07d9a8ba9c05b4a670e4895f060a253a01309244cbc`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0378a4a334d3b4cffb9cab48b3af6ec246e132da90a1800995016cf0bf3589c2`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 91.1 KB (91113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5361635eb47ff0c54139fb8d6f735ec9beb3988828092dd2fc5d3822db6a20eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749228d8c97e77fd9c454b59dade707186a17580df86a112f59d4294c25e7bb8`

```dockerfile
```

-	Layers:
	-	`sha256:d2d9148adae996142f2c520e17f483fbdc69659298daa1f02d4de07c78624137`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 3.5 MB (3539948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca28f4c520dba6f7987ca6746a6762200a61a360201024c7e94e22a89fda061f`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 13.4 KB (13420 bytes)  
		MIME: application/vnd.in-toto+json
