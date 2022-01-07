## `neurodebian:hirsute`

```console
$ docker pull neurodebian@sha256:a3f91be571c02c14b9f9862cda50f7c2abf8e93fd814597b39b9eb7a4f57b222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:hirsute` - linux; amd64

```console
$ docker pull neurodebian@sha256:e76058bc07db82ef077242435b87481cb4b35933c856f93d3778b33125f81582
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37552983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f058c786460f7a35486507263900dc3c9a280b2fba2c10a3b4e4fe3cb04e31`
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
