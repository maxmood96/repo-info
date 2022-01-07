## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:177132010bcbc538b9a5c4a389b20bff9cd2c28a5b640833db5df8d9a23fc3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:8445931a7bcc3de78cea7fbb73e83f86636b3285108c389310063a99cd91cad6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34295436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d897ee14cbc4c025f9682f8ea78dfc94ba858e810ef181cdf14230d14784762e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 05:28:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:28:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 07 Jan 2022 05:28:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 07 Jan 2022 05:28:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:28:28 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6037222680daab39c13e3361bf5f30b61283a5d312d65aead1ebb97af69ba4b6`  
		Last Modified: Fri, 07 Jan 2022 05:30:31 GMT  
		Size: 5.5 MB (5488730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed945fbc8d88c91a25d522999404a554fc4b0072e0773a64c533ea91a35514b`  
		Last Modified: Fri, 07 Jan 2022 05:30:30 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900194b011c5c000bcc8a947a23b208c5b264ae07877667229a316efe8f7c681`  
		Last Modified: Fri, 07 Jan 2022 05:30:30 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f755642fb201ee7f5e6a088ecf4d095c7a7869cc1b95d2d6a7e93f9448791619`  
		Last Modified: Fri, 07 Jan 2022 05:30:31 GMT  
		Size: 238.0 KB (238014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e373cc6c34866b99b615b679199d92043550b2fe57a5391ea68285d3fc44c976`  
		Last Modified: Fri, 07 Jan 2022 05:30:40 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
