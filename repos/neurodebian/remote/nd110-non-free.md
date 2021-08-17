## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:f37abdaf5a71138ff6b5e522cbc8e3d44c7ea9e491660f7fa782191f1b907a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5e2b0a80760bc955ad06fd67b984170e99fe0fbd73091329293fd17b267b4c39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66538058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6013efa885925229f770e7b1a7ee691323ee2450d8b34379a477160fd20e9e2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:26 GMT
ADD file:a528c112b566e7f129178dadedfa421b0c5b870997c4628327967850e54b915c in / 
# Tue, 17 Aug 2021 01:23:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:42:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:42:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:42:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:33 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4c25b3090c2685271afcffc2a4db73f15ab11a0124bfcde6085c934a4e6f4a51`  
		Last Modified: Tue, 17 Aug 2021 01:29:06 GMT  
		Size: 54.9 MB (54915004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7980c5f3aa1b56b00a43522300773b7b46a2893e5ef57cf76a2f95c78169172b`  
		Last Modified: Tue, 17 Aug 2021 11:44:34 GMT  
		Size: 11.3 MB (11309469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c33da905ad58fa70e2dcc7f460afaf846405f6c2d9ee4627ac4289b9173569`  
		Last Modified: Tue, 17 Aug 2021 11:44:33 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7649419684ebbeb22f83ef1d9d3d09879e0fbbce13e9c5c7c2227b02b2e1c4`  
		Last Modified: Tue, 17 Aug 2021 11:44:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d735f3c9625d83e34655ad9d3908af64dcb9467c99804b73e390b190624fb`  
		Last Modified: Tue, 17 Aug 2021 11:44:33 GMT  
		Size: 311.2 KB (311203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc7e4c6ee174344223cdf91d4360d44f13994916c77d9a96d19756a9098e670`  
		Last Modified: Tue, 17 Aug 2021 11:44:44 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
