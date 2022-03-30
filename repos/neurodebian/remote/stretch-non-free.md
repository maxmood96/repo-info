## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:f303ab5d6e5e8afe57ba5b065476414c5cc6608b6769da2ae984501275519edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7efa55c4a6d4c1ef4d778296ae306a92cba36c9729ded0618990947634bd1ffc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52296211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c506e9e8fa6b4b663d912ec6a5e708b30c740957fdb1d7ffa85bd65b343494a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:46:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:46:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 29 Mar 2022 19:46:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 29 Mar 2022 19:46:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:46:53 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de3b0be30389c6006fb91cbc5533bf087a7c9d72df4f8c64a56cdbf6ebbd34b`  
		Last Modified: Tue, 29 Mar 2022 19:48:54 GMT  
		Size: 6.6 MB (6572706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8230ab46306b62d11c9337edc50cdfa6d2b0a4c68258f4a70590e52bece0d`  
		Last Modified: Tue, 29 Mar 2022 19:48:53 GMT  
		Size: 3.2 KB (3155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb83b218193869e309ac982203a7832959cbeb5b95085f52b2ff3bac65a71b6`  
		Last Modified: Tue, 29 Mar 2022 19:48:53 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767bad48d6a6dd9fe5de1e6b9732a9b8dab91c0c292b8d40eaad2e93e2f117f4`  
		Last Modified: Tue, 29 Mar 2022 19:48:53 GMT  
		Size: 292.3 KB (292275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac3d11b9238304773715fb3f190ded0a017123db82bdfadadd11d774c8326f6`  
		Last Modified: Tue, 29 Mar 2022 19:49:03 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
