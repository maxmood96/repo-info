## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:4953fd2b6f254a0f6af5676bda8cffa13962e56be18c3cf46f7e505eb6ad882b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5ac9e3892a6977f1df68f9984d852b3f1c57bde29052850c3863c25aead9100a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31773718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb12b6fa8a2a1ee7b7c4f89a51abd507f3868c5d95abd28647e2806f1ff6683e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:18:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:18:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 09 Dec 2022 04:18:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 09 Dec 2022 04:18:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:18:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f315882d396169772cdbc738a350307327eace7b359f3ac364ecc633e3847786`  
		Last Modified: Fri, 09 Dec 2022 04:20:14 GMT  
		Size: 4.8 MB (4819773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379d2a050e045de972fb82c6f6919cde9c1faea51882cabe07ed6ec695fe11b5`  
		Last Modified: Fri, 09 Dec 2022 04:20:13 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b9116c5a672282932244fe02fbf4234a3e3ff1fb963e3d7b51ec77133010a`  
		Last Modified: Fri, 09 Dec 2022 04:20:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adca26b949f2fdfc8d18eb036c0f3d377715c2ef1be5902ecc682fb8db41ca1b`  
		Last Modified: Fri, 09 Dec 2022 04:20:13 GMT  
		Size: 240.3 KB (240322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704d31494851441ece6157459b08033fab157fb2ed957241c66d283cd26de2e7`  
		Last Modified: Fri, 09 Dec 2022 04:20:21 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ef3670710ec83e9a16ee106a49753686bebcae2b9be32afdc5cc3343b9cdd377
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28378146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dd8dabee678ebaf45ff1d168d7b71d65f4d65509c7dac8795a322c6a380dcf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:43 GMT
ADD file:eb8b2914800b2ed866666fbff73c8234f4ac2a5ef01743d6fea0984230c2f464 in / 
# Fri, 09 Dec 2022 01:46:44 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:12:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:12:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 09 Dec 2022 02:12:25 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 09 Dec 2022 02:12:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:12:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:87acad9590b042ceb59687d498c396e9344cf2e381923fecd299555966b14975`  
		Last Modified: Fri, 09 Dec 2022 01:47:46 GMT  
		Size: 23.7 MB (23734135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f61184f3a9b790e0a607c824da66bbd248053b5af93a4b06a1af387f90b43b`  
		Last Modified: Fri, 09 Dec 2022 02:15:03 GMT  
		Size: 4.4 MB (4401770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ede042e70b3755336665612d24bfaa821174317013287abb7d1c5c3ff1acd`  
		Last Modified: Fri, 09 Dec 2022 02:15:02 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82fef820b26b0185647ffd846d0b173c04bfa8fce4607b2dd97572477fcaa45`  
		Last Modified: Fri, 09 Dec 2022 02:15:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa768f88ebd974ae18e34bebba9d6b31fe8de438bd83201bf02787af231ec179`  
		Last Modified: Fri, 09 Dec 2022 02:15:02 GMT  
		Size: 240.1 KB (240077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dd4adb8f513235f1e34b1ed4448beac98319276c7cc80f1ea43a700c309d50`  
		Last Modified: Fri, 09 Dec 2022 02:15:12 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
