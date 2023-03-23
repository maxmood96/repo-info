## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:00f4eabfcf6450382882359397323f5ce0ee1fb0cb6bb978eb328b6c33cd210c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:731d9416c74576d5a00e1e625dfb2f62359eb4424e53824e1c0c3587875911da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66670393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5671c8387d65e53e56174bc8c57a79128a786b69655ff42f370ba344b7311ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:56:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:56:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 15:56:41 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 15:56:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bec02b1c8819dcbbd4004998624fa263e8832c4bc5863f181009abb76389091`  
		Last Modified: Thu, 23 Mar 2023 15:58:06 GMT  
		Size: 11.3 MB (11310858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343785a862b6b92c2fee16d902fdcb9f6a8bf971722fcb260d1c57ae18514de9`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cfa7b419307b5004b261410bb3c591288b37f4c90424c3885f95c668910d48`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4155247909b7310bdcb63fe90856b19bf15168332ccf3549e39d5bd93c27f87`  
		Last Modified: Thu, 23 Mar 2023 15:58:05 GMT  
		Size: 311.9 KB (311912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:92868460c6fd1adf5b17efda71fe04f9a3f942b0d2207e5e896d945691c34f06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65329803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b09d7a97a033bde4a7708e836cf6e5e08c5f34d0e8bb9491dce8a4f1d87b51`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1073198b78bb3e7b1ce4370609ffa5310772b90829b03034acf5ff27fc5f6fbc`  
		Last Modified: Thu, 23 Mar 2023 09:31:48 GMT  
		Size: 11.3 MB (11312879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b494f8a0906f457066670c42f89edf0123014152733ca71c0b65dc7862cbfbf`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8d72de2ce242bb047e2e0892ff659ce549fe3be331a3354e2760f601b48107`  
		Last Modified: Thu, 23 Mar 2023 09:31:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5987ef310f1e22a1071117070fc246f525fcab178073b74dfac7696582cbab`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 311.8 KB (311812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:da3b10e574f62e0f4bba846fee6dd699b5409a6be486d34b511f843dca3eff0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68049766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0573a6d9cd656a17f913d9bb9cbb387ac1ef6f363c990c0459c2ecc3759afd47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
