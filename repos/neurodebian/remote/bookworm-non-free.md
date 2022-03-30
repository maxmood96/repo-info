## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:46d446843168ba621720cd1ceec0b55484c7ecee64101a4ec3ed85fcfbf41404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:864008f6e52ee7eb6f35a7cba1bb9d7cf12cd5437a6da92bdb7b7f44b0fb8d81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67267863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6798ea6767196783ffb5803cae34dde2569c2b1ce09d1715580692d45444a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:21:48 GMT
ADD file:084dc3db6641669bf09de94b7a32f3180ca32152a22a677961428ad78324f10c in / 
# Tue, 29 Mar 2022 00:21:48 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:47:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:47:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 29 Mar 2022 19:47:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 29 Mar 2022 19:47:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:47:50 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:6673186ed4ed62930866783fb71f9386d0ece250e264d269d06e238753c30392`  
		Last Modified: Tue, 29 Mar 2022 00:26:08 GMT  
		Size: 55.6 MB (55584323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db1f2f06d73928c58913f2b7873596e4cb3f47fea50889172fcbdb9a408e6f9`  
		Last Modified: Tue, 29 Mar 2022 19:50:04 GMT  
		Size: 11.4 MB (11373733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2468bc689570f3401e0881774a205d4ada7d69c45f0e8a341b1439c0c33326`  
		Last Modified: Tue, 29 Mar 2022 19:50:03 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c251d0d5d854d84f86cb8e1f611e5aa397301ab8f4b052f679d84124f9a69d4`  
		Last Modified: Tue, 29 Mar 2022 19:50:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47ff117645b28e139a0ed297eaa24ad2a570332666f6554e432be57374aef24`  
		Last Modified: Tue, 29 Mar 2022 19:50:03 GMT  
		Size: 307.4 KB (307436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebba0632a4f4ad35337dfeaeb1b79b665393987294689b4de3d19f9a2f6e477`  
		Last Modified: Tue, 29 Mar 2022 19:50:15 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
