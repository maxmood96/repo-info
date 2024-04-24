## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:cdf77acede391fd5a9fb542ff38bf71e5c2c1bff6e5353cb7a4df32135459299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:da4dfb4fd57feb809612292068b88cf45248d914f7dbf20b188d1c12dc854a75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64610465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998ff6a3fd8de4cba074e06a09d1adb79793ed5a0627c455c9056d68b55e6e10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:29:41 GMT
ADD file:2bdf145484732bc44972c30edbf4ac0d4400e2c23e993bf3575794199944fc3c in / 
# Wed, 24 Apr 2024 03:29:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:09:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:09:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 08:09:08 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 08:09:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:09:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:7930dce44f2f1c310f4efe60708c4f2a496a0490b6d354b92c75cd37256dc108`  
		Last Modified: Wed, 24 Apr 2024 03:35:15 GMT  
		Size: 52.6 MB (52577130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c7dfd06437e02fff0de53af99dc1c00f1276fbb8de9e98d2df6028c40b2335`  
		Last Modified: Wed, 24 Apr 2024 08:10:36 GMT  
		Size: 11.7 MB (11743087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd26b6c5d7f38213336fea92572312ac1832834e19f0645d8013bef455f1c5a`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ebb65957e8e94ec9c3a1b4f90b48587b350b1a5d2e066e0d8870c6438a93ed`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77527b91c07d267eb02ab1842c5fecf2250bc80f9a3071ca1c62fa510ce8a020`  
		Last Modified: Wed, 24 Apr 2024 08:10:35 GMT  
		Size: 287.8 KB (287843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1eb88e765e63782a59d495ea7f9b1079764f27094a1479608f41455b5c7f9ef`  
		Last Modified: Wed, 24 Apr 2024 08:10:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8eed19e43fe455a4467dc0964ea15c6a2527e735a32b26147778c5d4e98ba806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64889916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbddc970b69155e7710675b1470b74121ed4abae73cdad8df3316e0680cf6ed9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:40 GMT
ADD file:58d167eb75df26d368d9ef63173440fad7973e18049ffb23841be9cf507ee614 in / 
# Wed, 24 Apr 2024 04:11:41 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:55 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9914f5e7b79b9a6b9b6b7b39565cb50b06e8e20c51fa6732d67575dc53227762`  
		Last Modified: Wed, 24 Apr 2024 04:16:38 GMT  
		Size: 52.9 MB (52860803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d837feebd2f839b2c1f963eea7ebc9e63d698a5493a5a0400ac20b7f43a2071c`  
		Last Modified: Wed, 24 Apr 2024 04:43:18 GMT  
		Size: 11.7 MB (11738112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09977deff1fff17d1ef335ccaf490538bd16ff4a539f9e12bb7c0c3eb4cb0c82`  
		Last Modified: Wed, 24 Apr 2024 04:43:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b96de0d76100592b8310f330c37dad1a727ec9bf5e76ad94c35d9f20a35bc2`  
		Last Modified: Wed, 24 Apr 2024 04:43:17 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2df9bddff64eec380d895f9b9009fc18c563afecbc57fd1c443e6dbc7820ee`  
		Last Modified: Wed, 24 Apr 2024 04:43:17 GMT  
		Size: 288.6 KB (288594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec7a4c6962d047c0b07c813ee90ae3364131902545f2ce9a30b3453030562f8`  
		Last Modified: Wed, 24 Apr 2024 04:43:26 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:155a6aa73f6f797cbb52dd0f1723ee27a34e6ca66436fffd127e645c605aa516
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65922574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f964cf4e8b5588fb20195e40ae6af75e9ff4f8c5334e66cad9f41dc99f24694c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:40:33 GMT
ADD file:d8ee7d4701df61ad645e587b8b9747ac72c6dbdc2d358f14834282481c37711b in / 
# Wed, 24 Apr 2024 03:40:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 16:52:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 16:52:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 16:52:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 16:52:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 16:52:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1468f2e7ad62241109cfe49228c179a1529c8ad99c7e30f87c274cdba78b9582`  
		Last Modified: Wed, 24 Apr 2024 03:46:38 GMT  
		Size: 53.5 MB (53469174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6135decebfa86cfe306a186279cc32c37228d7f21ba8b56c448c995e84b037ca`  
		Last Modified: Wed, 24 Apr 2024 16:53:45 GMT  
		Size: 12.2 MB (12163224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05ecc15bba4e17ec3f6b1438544db739557c48f9351332184ea1810d53f6a8c`  
		Last Modified: Wed, 24 Apr 2024 16:53:43 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60626614aebcf8a1f55e3790d1f23a1683dce3f57eeaa67c8a9124902d65682b`  
		Last Modified: Wed, 24 Apr 2024 16:53:43 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e77807f33b04c7c375fa760620572c4ac1ea66bbace51da14d014caa5bcd47`  
		Last Modified: Wed, 24 Apr 2024 16:53:43 GMT  
		Size: 287.8 KB (287773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16721ca1386e442adb8fb6526c4b0efcf8e2b7cb5921ca650514c42e9cc79932`  
		Last Modified: Wed, 24 Apr 2024 16:53:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
