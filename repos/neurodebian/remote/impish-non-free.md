## `neurodebian:impish-non-free`

```console
$ docker pull neurodebian@sha256:3d2e187fe6b51ab8920ae14f64a641b9f9e0c63773b5bdda1c767c7ca9a1d7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:impish-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:95d4f32310f9a745ed1872824b5291c47bf8eb3cd79406514131e23090c75e1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34389358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157f768d72636f7b777a6e298a6eb924161750b6ddc10ef17b8bb027d2c7e14e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:54 GMT
ADD file:dc66b6b0841e395b5cf9d65976a75c3a46a19eb2c0fda4556ac6b4c5b0fe4dea in / 
# Fri, 18 Mar 2022 05:30:55 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:13:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 18 Mar 2022 08:13:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian impish main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel impish main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 18 Mar 2022 08:13:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:13:41 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:49dc71d53e6dff9c7147b85fbe167470cff447114548e6df43606b75526c1451`  
		Last Modified: Fri, 18 Mar 2022 05:32:45 GMT  
		Size: 30.4 MB (30385910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02dcdc2dc3c600bc75fef3a31d1a5e174b094ca75baf90ba6d19587937596f`  
		Last Modified: Fri, 18 Mar 2022 08:16:52 GMT  
		Size: 3.8 MB (3751774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5a2abb4afa38d503f13785e4ddec9cf8c7dfecbc32a1044e17d914465c297`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c82d2f42bf7700d6f3b7a7d0a2cb65df389e99fc8590f8ea57f38faa9953606`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd139379a494abeceaea7b99b395b2dfa5d3171218e66e5b2a861bead4ef1e26`  
		Last Modified: Fri, 18 Mar 2022 08:16:51 GMT  
		Size: 249.4 KB (249399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4a25da4e998243c62595ed39cb7923223ddc183fb90108283b18a76655a42`  
		Last Modified: Fri, 18 Mar 2022 08:17:01 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
