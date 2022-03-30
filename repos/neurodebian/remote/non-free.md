## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:8ea3f19a6d8c4e22c2104a1a21414824a2a523544700526a6a5fa767398f89b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:655f739e42ff88ab6acbd9c2118e8f775c4fea74ea8efc7baf3abb14fab00efd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66561706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65296a09641f0950de01c1f2a70881f1caf926019317828cb8aa58699a0dd77f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:07 GMT
ADD file:e8d512b08fe2ddc6f2c85831c73e4c72b9c850fa428913d19da4bb1a34f84cf2 in / 
# Tue, 29 Mar 2022 00:22:08 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:47:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:47:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 29 Mar 2022 19:47:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 29 Mar 2022 19:47:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:47:31 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:dbba69284b2786013fe94fefe0c2e66a7d3cecbb20f6d691d71dac891ee37be5`  
		Last Modified: Tue, 29 Mar 2022 00:26:47 GMT  
		Size: 54.9 MB (54937710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f83b00d3523fc0a34a5beacf948421a6d6713db968b94e37e475749b4c1f471`  
		Last Modified: Tue, 29 Mar 2022 19:49:35 GMT  
		Size: 11.3 MB (11310350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ffd557d3b57bd99c9a35f75df09d3ecba6af7b5ad7c5402a2ded41313ad8c0`  
		Last Modified: Tue, 29 Mar 2022 19:49:33 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15506d8dc6df01871aee5d3792d0c7797eaa7583f1af812f85b6392d0ec9d81e`  
		Last Modified: Tue, 29 Mar 2022 19:49:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af21f79c8ae657571d6400422bb20a058c691ba9852402335fe33b6f08266602`  
		Last Modified: Tue, 29 Mar 2022 19:49:33 GMT  
		Size: 311.3 KB (311274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0d5077f6ef765768f5bf74377bfe2eddc012536993bd6fc38b601787dfc830`  
		Last Modified: Tue, 29 Mar 2022 19:49:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
