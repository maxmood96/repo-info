## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:42867206dcaabdcc8f6ca6e7f4bc71be9ce23c126da98e894e106aea435c655d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:1fcb3454549760d53b3c7ce3d16c5fbc63368b5b3e7a55e900fafb243eac40fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64056419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8595c9e3f9168c206bb7990dd891f2b82fe6d38adc1b1087db6cf55e24dbfb4d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:17 GMT
ADD file:bc0b5b71ee53adf6297821668404ace4f79c4256461b99497849721dbd8e86ae in / 
# Wed, 20 Sep 2023 04:57:18 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 05:57:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 05:57:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 20 Sep 2023 05:57:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 20 Sep 2023 05:57:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d036181e87bed9eb2432498f0ccbf7baa06719a2d8360c3bc9c496bd9f853a7c`  
		Last Modified: Wed, 20 Sep 2023 05:03:10 GMT  
		Size: 49.5 MB (49482728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5f448790412f2b4749596c323f460fd626e02a0a2cc2c5807fd227c9b2393f`  
		Last Modified: Wed, 20 Sep 2023 05:59:22 GMT  
		Size: 14.3 MB (14287421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46be4fb4c974cf5509873e1242391934cba1868808854057528ee20b65b371f0`  
		Last Modified: Wed, 20 Sep 2023 05:59:20 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec9aa8565bd54eb58d36ced36fad6281081fa1d832dd2c7555d1f17105b5376`  
		Last Modified: Wed, 20 Sep 2023 05:59:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3adfb7e9d68ffa3f542118503072e5f615786d815ea40213a0c0d7291714ad`  
		Last Modified: Wed, 20 Sep 2023 05:59:20 GMT  
		Size: 284.3 KB (284265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6d0b8a77b2446f4d790b1b8fcecf1fa204f0c5c4f7c944789dd5339d02a8fdaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63780178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9698a5a821150232bbdad81aecd9ab96f8ea965243e0a433465c0187d8c05382`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:41 GMT
ADD file:3fad0766985d4815384b52dbb02c3f23c3f0c6e9b05ae96cdb2f60692ebe3c47 in / 
# Thu, 07 Sep 2023 00:40:42 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:34:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:34:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 07 Sep 2023 09:34:37 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 07 Sep 2023 09:34:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:352986db96f4040761867c771dd7419bd03916c5a2f552680219ad48902eec34`  
		Last Modified: Thu, 07 Sep 2023 00:45:36 GMT  
		Size: 49.4 MB (49413074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd83822cb5183fa52ba8796ae530db76139430ea12dd7ba7b0b7d2600f3c4bd`  
		Last Modified: Thu, 07 Sep 2023 09:36:07 GMT  
		Size: 14.1 MB (14081293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f12b840d2fe814f1e0c677b1264b05eeee794f95b62a15f8fdebe3c487f1f2`  
		Last Modified: Thu, 07 Sep 2023 09:36:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0d7739cf693bfd52f4e8ba9bf297736054fbf748d4f93d43a5ce7c614d837`  
		Last Modified: Thu, 07 Sep 2023 09:36:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86210c1554378900877143c9f650d66216976cb3bbe2f67dbbbc2241d006882`  
		Last Modified: Thu, 07 Sep 2023 09:36:06 GMT  
		Size: 283.8 KB (283804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:491b9c8b3d7cd2efa9f041674dd484f6be2f69df48e454947df8afab99b97a4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65459826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22815772247b79196b081fdc3b1ea9f78efae6682beaaa918fc8ebd86ba4fea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:43:36 GMT
ADD file:89a1cfdf26e23095cc168a8c054aaa8afe0cb7f1b748f0dbca755e9aad935ce8 in / 
# Wed, 20 Sep 2023 00:43:37 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:51:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:51:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 20 Sep 2023 15:51:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 20 Sep 2023 15:51:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a77a25e288eca9c35f0aeada81ba65e2f4beb3d0b739a139eb41bdd87309a97b`  
		Last Modified: Wed, 20 Sep 2023 00:50:06 GMT  
		Size: 50.5 MB (50483129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00716f16669fbde1a6927877c8b01a86fadde4dba1fa729c70c2201e14dead39`  
		Last Modified: Wed, 20 Sep 2023 15:52:53 GMT  
		Size: 14.7 MB (14690576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142260c4269f1833147ea7d89316ff0d7fe446bca322be1c938c8f427b7ecc74`  
		Last Modified: Wed, 20 Sep 2023 15:52:51 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53f904f97cb7220a02a08fa85614a17ea76ee3034d7d80d3128bb31e257435d`  
		Last Modified: Wed, 20 Sep 2023 15:52:51 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba20fbcbd3f269dc55fa471a0d8557fe1660422530efd90bac3726276d870505`  
		Last Modified: Wed, 20 Sep 2023 15:52:51 GMT  
		Size: 284.1 KB (284112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
