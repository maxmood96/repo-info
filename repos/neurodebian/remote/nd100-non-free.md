## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:7e4263c18c493302e0997b1be3bb845fb8b2bab21c89fce6fb7796d5973ba584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a1bdd9b45aad906eea47ee012772269bf5422c4c625d82ea9fe347f429ffba84
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfe97d2fd7b4c7dc4431ea670b0b06a22c7bd5935941b40ab11a52b5276fa4e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:33 GMT
ADD file:dc52371b5f4608e5887e8c657ff951d1895e0047960f44b153c4a55ebf1726d5 in / 
# Thu, 09 Feb 2023 03:20:33 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:32:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:32:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 09 Feb 2023 10:32:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 09 Feb 2023 10:32:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:32:55 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b2404786f3febb4866f85b0c8f52b0b0b94dfdb6543e94cd65f961c68f325ff7`  
		Last Modified: Thu, 09 Feb 2023 03:25:32 GMT  
		Size: 50.4 MB (50449613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77502ab3ca1cfa948d065d90f0572b331e529eec6f234419b6ba0dd44c7e0135`  
		Last Modified: Thu, 09 Feb 2023 10:34:35 GMT  
		Size: 10.5 MB (10504538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec51aec442293416c6492307baf3e69b92abc070af15fe2f827239fb84259923`  
		Last Modified: Thu, 09 Feb 2023 10:34:34 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59955829e458d6ce57c1941668246f2fcce15209bf143652918255813981e54`  
		Last Modified: Thu, 09 Feb 2023 10:34:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3258ee389ec682ceb8b472c2883f47efb2fa9bd667332c5120470649b3a98980`  
		Last Modified: Thu, 09 Feb 2023 10:34:34 GMT  
		Size: 304.3 KB (304328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf843247789a5bd789d96ea0d938767321149236fc262ca618a3848b2966ef7e`  
		Last Modified: Thu, 09 Feb 2023 10:34:42 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b0d1d6eb19e18f6ac3d05f9e596e9830b7b478648e6cac296112c1ef9bfbbb7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60057040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd60cdda08423f59d6bd5a001400c73153e5d6a40a37837cb7d2771936674f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:46 GMT
ADD file:bf5b2f8cbddd98de6093dde190b043c3e2b58a5063d1acec0aba091e7d203dbd in / 
# Wed, 01 Mar 2023 02:20:47 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:23 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:00:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:30 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:06cfbde07ccb39d53563bd87f3c2b50f04ddd0c8f6cd52be3c7089a3413688e1`  
		Last Modified: Wed, 01 Mar 2023 02:24:34 GMT  
		Size: 49.2 MB (49240002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f17a319adfdaf70a0743c908ed30a76d664f69e943708f0373c6da2c9c67b7`  
		Last Modified: Wed, 01 Mar 2023 05:02:02 GMT  
		Size: 10.5 MB (10510356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bb398b76429a8b2432811dfcbcb6348bb36b23bd016af5d310d19c8c445d64`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf77cd6bf30274d4a68a065b517df02742ff5dba187db54ee967c6fc4210736d`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ea7526c13547805ba46a2fef0ad342e282d2fb5726b30dc02c59c32bcebe7b`  
		Last Modified: Wed, 01 Mar 2023 05:02:01 GMT  
		Size: 304.3 KB (304317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3545fb879d6379e51745374d6f1d63a7ae2126141a15b12572b6355ded4d8f69`  
		Last Modified: Wed, 01 Mar 2023 05:02:11 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:67c64ff956cb57efa4dfebe6c4c7150991d6f4fc47191cb124f5573bc5f4d027
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61991356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc45ca5c74ad14e514a7a4b704774bc433d2f3486af07bcc806487d21047ba72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 05:13:04 GMT
ADD file:043d1820efa588dcc60e5d9c340fd1edcd43f2988435e6284844a71d4b082dc7 in / 
# Thu, 09 Feb 2023 05:13:05 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:43:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 09 Feb 2023 12:43:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 09 Feb 2023 12:43:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ee55492a1c0f9dc3f2620641096fc2d501a92c463492dd5598f15a6634c4d8bd`  
		Last Modified: Thu, 09 Feb 2023 05:19:04 GMT  
		Size: 51.2 MB (51207786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641c4ab61efe8b684f2f70e427f740060629acab64b255865a739b677e0947ac`  
		Last Modified: Thu, 09 Feb 2023 12:45:15 GMT  
		Size: 10.7 MB (10672461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfbc65dea7c5bef81239621c61d98f3956bcf57cd5fba5d2a09920e4aed1fb2`  
		Last Modified: Thu, 09 Feb 2023 12:45:13 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3ea514e731298f7c296c9efa36329cb9a29422b0290649fdaab7c8c1aca590`  
		Last Modified: Thu, 09 Feb 2023 12:45:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252f61add039c1f47969b061f788e132a2d94ab712013ed772c1480332874361`  
		Last Modified: Thu, 09 Feb 2023 12:45:13 GMT  
		Size: 108.8 KB (108760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aa7209b6e78fe409e7508dd28ec663fb4b5351bac0ef5ed20fd61ae220f65a`  
		Last Modified: Thu, 09 Feb 2023 12:45:24 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
