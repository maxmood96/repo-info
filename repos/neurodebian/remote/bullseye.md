## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:c82eb4a0295a6c462d1a6fbfcad669ba6a1781427a03bcda35d1d23f7a113a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:60436cae9526ecd47b03c3e10bd77ec75e14f59ae0fe2c551bd61b6124fd1095
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66485588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9ef797259b3acbdcbb2f69a112f9b186b5839854a8b680548b1d6d58555e67`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:11 GMT
ADD file:54b23fc0b4b728c85082d50693e314d74e46329004bb55a97f43fea46c497dd2 in / 
# Fri, 26 Mar 2021 15:20:12 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:46:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:46:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 27 Mar 2021 06:46:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 27 Mar 2021 06:46:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:efee637ec1bae521f17fb8d92548c288e3396988c475551b8774c0d08c01c70f`  
		Last Modified: Fri, 26 Mar 2021 15:26:18 GMT  
		Size: 54.9 MB (54867948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350cfcb24a0700ecab33841e238931ed0b5ecc0921f08b4bfa88c8cfbfec42ea`  
		Last Modified: Sat, 27 Mar 2021 06:49:14 GMT  
		Size: 11.3 MB (11304981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fd1b4cb2211ac50cae4086cac774572af0ccb31ab78c3f0d89d27a9ab31c04`  
		Last Modified: Sat, 27 Mar 2021 06:49:12 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60fef2a8c3817d52f22d03e0a7fdb439d4a7259198622db80408b9d698f34b7`  
		Last Modified: Sat, 27 Mar 2021 06:49:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4462f910e6970d025db2d16bde1b4f993163e93d24a1499b1e256eb9287afdec`  
		Last Modified: Sat, 27 Mar 2021 06:49:13 GMT  
		Size: 310.6 KB (310648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
