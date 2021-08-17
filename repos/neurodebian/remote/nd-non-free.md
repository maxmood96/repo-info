## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:80a7a7c1946118af7d7021ff098f4b1181c437cf6078393ef71116bb7b4a1353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7e888b386ccd79eed3cc5c45d9c4e74665cbcd61c69317984194ea9b143c2686
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66554123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cc3785a6cdb16a17d84956f49da466b06e6a126197a0a9ae26eb68582e92ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:06 GMT
ADD file:3052ec53a19fa26baad5d50e4d2867be2cc386ae62195d8dbb9d90d0b904c464 in / 
# Tue, 17 Aug 2021 01:25:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:42:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:42:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:42:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:56 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:a6952a6bd46e0eaa2c0e7e851a45f288b3dc080472a9249e48c74b3fb7551fcc`  
		Last Modified: Tue, 17 Aug 2021 01:31:55 GMT  
		Size: 54.9 MB (54930846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410ec36aee1a8f201f9c0031cd0f05202d26dd1d1436a96bf9c25d7e16cd6409`  
		Last Modified: Tue, 17 Aug 2021 11:44:56 GMT  
		Size: 11.3 MB (11309853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511f77571d0ebc200d836bb589cbdbc218a43528b6107216fb05ac08b051e861`  
		Last Modified: Tue, 17 Aug 2021 11:44:55 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24c8352006baecfb22a1adb719cc0dd9979fc96bd6e659b84d5e08367516a4`  
		Last Modified: Tue, 17 Aug 2021 11:44:57 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3017795095606b9588affb41bc71fcda9f48a651b50d1e21b632ed47564d944c`  
		Last Modified: Tue, 17 Aug 2021 11:44:55 GMT  
		Size: 311.1 KB (311099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1f96b4ea8e389a530c0f176604c77f640d48f27ed379dd42b0624d42999787`  
		Last Modified: Tue, 17 Aug 2021 11:45:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
