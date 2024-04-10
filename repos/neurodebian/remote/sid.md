## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:b658fb9b0538f9e9b5ba84bec0f365a1a60e5d86aebe116ca5f84947b54de5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:bf5a24a4197b8dea256cb5c4df5f23c267c6ec598c56f0ab5e7e5665335d46c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64410397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eea9024bf65192e41355fa593deb4a3c1c4cc42f65591ab72a0a198d96a2568`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:49:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:49:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 30 Mar 2024 21:49:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 30 Mar 2024 21:49:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9db754ac7589d0093c33a3961d1a053f062bf8f7da86a2e8fd295bf82f7a25`  
		Last Modified: Sat, 30 Mar 2024 21:50:32 GMT  
		Size: 12.6 MB (12620251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108cdb2759de0be751811be1a9ec0a3d5a543f4b709d26eebe254975f89f9094`  
		Last Modified: Sat, 30 Mar 2024 21:50:31 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3989b94ce025dc6c38b95c1c9d6e797f5f70a18f0c74a2be32956a022d73b`  
		Last Modified: Sat, 30 Mar 2024 21:50:30 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae806d0dd4474275a13b633b6599ebc17242b5cedf1846231915659054df8851`  
		Last Modified: Sat, 30 Mar 2024 21:50:31 GMT  
		Size: 287.8 KB (287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:39804bd0fa2b87c4b86a48c8b77042b98441fa73c0f841a38157f356c0a8522b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65028294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526385cd80c10bf1e21584c3952c54a6a21fa2f5a28f851121a478c38221be57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:31 GMT
ADD file:69ea41e74fa7a7601d1adbbdf992359f0c16c551447466cb4aaeac1914dc2377 in / 
# Wed, 10 Apr 2024 00:41:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:24:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:24:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:24:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de2b6ae488daf95901751cee985416dfee51a36f7f9f15e60031279618e00a20`  
		Last Modified: Wed, 10 Apr 2024 00:46:49 GMT  
		Size: 52.1 MB (52136998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d3314e63373ea49d2747bbacfd86de539736d0ffd0bedb258a47825bec40fc`  
		Last Modified: Wed, 10 Apr 2024 07:26:21 GMT  
		Size: 12.6 MB (12600701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd79efd98f63f526acdcacf17861110f1469da8409683c6a86aca38ef692188`  
		Last Modified: Wed, 10 Apr 2024 07:26:20 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fb0712dca88ceb3b40da1dfa46101e51680921e074b4e0e2c52d91ca134834`  
		Last Modified: Wed, 10 Apr 2024 07:26:20 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a7fd5f19f3cc1e174533a1b004cdf8eb36b373ccbd88b399d929068ba09561`  
		Last Modified: Wed, 10 Apr 2024 07:26:20 GMT  
		Size: 288.6 KB (288588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:40f257d65c33a3ca4bac3d5a8dd73fe5f681a38e847a622336bc25777511e50b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65963214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9414f1ef791b35f0e53ec296123bbf56fce785fd4afadd1a5b8dcba95f79646`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:52 GMT
ADD file:e239896f7b5e011b6d0233f2b19722dd4ed9b477a41df953ada860d9292309a9 in / 
# Wed, 10 Apr 2024 00:58:53 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:24:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:24:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:24:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aa1551ec75fa2e9c2e1970c5f0cf8c95e50b19638484e38cd439a1ae005100e7`  
		Last Modified: Wed, 10 Apr 2024 01:05:22 GMT  
		Size: 52.5 MB (52545296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679fd105449905a0a94707b3cba942d456bf9fe38526a79f7b341be509fb6708`  
		Last Modified: Wed, 10 Apr 2024 07:25:43 GMT  
		Size: 13.1 MB (13128155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2827d9b3036a22fee78ea17382d6ba1f730c8c763ef24312843fcaf186c8cc69`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc53f67a234b9e433bd5bc4d7b7c4fe1e787931568ce54d0eb27900e207d2095`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068b92b06f0afc1e120d97fe37e9366d8729e90600f03c95d7ccdbca3a3fd8b8`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 287.8 KB (287757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
