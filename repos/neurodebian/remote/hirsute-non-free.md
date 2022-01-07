## `neurodebian:hirsute-non-free`

```console
$ docker pull neurodebian@sha256:80df44a574b66e5f465015cd8a1bda3a9513285e292b3dac2c30ca2eae658933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:hirsute-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ae5d3ca94490aa9cfc9ae627954f62dd7563fe9d9a5ca59c4c79a35f4b6ee5fd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37553240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145430492d697cf2b54ae75b022f0aa4b72c01feb07e86942c409922bae11909`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:37 GMT
ADD file:cfcb96e25bf4af2949d0c04953666b16dca08216ded8040ddfeedd0e782c6ddc in / 
# Fri, 07 Jan 2022 02:25:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 05:29:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:29:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 07 Jan 2022 05:29:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian hirsute main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel hirsute main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 07 Jan 2022 05:29:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:29:19 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:318226705d6bf4f94a70707b917c9bea2190a83f512b1c257dffbb691859831e`  
		Last Modified: Tue, 14 Dec 2021 13:10:17 GMT  
		Size: 31.7 MB (31703311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b660ab384dc437bac4dd8eb3eeea88790ecbc41073370f9809e3ef5634c2b4db`  
		Last Modified: Fri, 07 Jan 2022 05:30:50 GMT  
		Size: 5.6 MB (5597997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd0b3404d868b3d711cc60b5902931e6443ce7ddc26d84b8363849e82a8962b`  
		Last Modified: Fri, 07 Jan 2022 05:30:49 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de5396b81b6844d6a784a3610ad3921ffd0dbb22aebdec36810082dcf82a9dd`  
		Last Modified: Fri, 07 Jan 2022 05:30:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bc1968b1fdcb61c0cdc15edef48cd9714c0d46934f4b1b309595cf222a416d`  
		Last Modified: Fri, 07 Jan 2022 05:30:50 GMT  
		Size: 249.7 KB (249660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759376287264513fb56393470396a56e914a763abb0868583e316e04d107b6b5`  
		Last Modified: Fri, 07 Jan 2022 05:30:59 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
