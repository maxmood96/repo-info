## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:f525bfa4960b360a59f7e7c830ef9bae66fcc2fb69b0833799a2cab2f047f202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a70c2a25f5b55499baa18733b8d19c2ee7f345e19f9559d1280d54b57c6f5123
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61259783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5134998283e1f7dc5d8979865877ce77c7a4ab55bb9cca9ed28dcdebcdce46d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:03 GMT
ADD file:96ca7e18b6141668321140f8ae1a496641f631313035513f1f9314e9dad2cd71 in / 
# Tue, 15 Nov 2022 04:05:04 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:10:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:10:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 15 Nov 2022 13:10:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 15 Nov 2022 13:11:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:11:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:2730d739afad9b8ff3e3029e23fd69d9533603751d6e42053ce0068c2b58e258`  
		Last Modified: Tue, 15 Nov 2022 04:09:05 GMT  
		Size: 50.4 MB (50448823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fca1bc133dec52587564a08d86ecf97ccbd619c537a10d7523e214fd7dc979`  
		Last Modified: Tue, 15 Nov 2022 13:12:52 GMT  
		Size: 10.5 MB (10504260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e431fb20443b2100d30c4dbaee3fc077f7cdf06ea25db1a50095ae44f9bf01b4`  
		Last Modified: Tue, 15 Nov 2022 13:12:50 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5daab9e1641bf6cd75e404663309d1587f798a59e047761730a172bb06d8671`  
		Last Modified: Tue, 15 Nov 2022 13:12:50 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3932639071cd8a9aed3bca4f449664c9c7021d039099b1d7a4b562f2bfe2d8`  
		Last Modified: Tue, 15 Nov 2022 13:12:51 GMT  
		Size: 304.3 KB (304328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422d382acd10c8c2796a2643e37f5aceedb11d912150e9b632bb2b80ac2d0ca2`  
		Last Modified: Tue, 15 Nov 2022 13:13:00 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b8a5ca1e768e4024b1623e757bfc1076af1d396b5a2ee26ca4a5657603158a35
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60050624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c31fba635ccf084a543e28263d1a683a2e7de0d2cda22c7e7fc3bb0342d084c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:24 GMT
ADD file:2deba7c04e28d01997b865f366cdc8d38a80aa39720c4e4d1fc581ac17e8ce4a in / 
# Tue, 06 Dec 2022 01:40:25 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:06:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:06:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 04:06:24 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 04:06:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:06:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:47d0ec2abdb05569eada58143acd16d47ee4b07a33535544cf5bf267bde20cc3`  
		Last Modified: Tue, 06 Dec 2022 01:44:13 GMT  
		Size: 49.2 MB (49233737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e928f3f303597bfd9fba2e92cdcf920d9fcafe42efca63103692d4366569b`  
		Last Modified: Tue, 06 Dec 2022 04:08:12 GMT  
		Size: 10.5 MB (10510258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8461cf556d4a4eaeaf44cbe29b1878cf0ad26ef6e36e98337ecc9eb7377b8367`  
		Last Modified: Tue, 06 Dec 2022 04:08:11 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feef9992ce9a2afe0529457ef73f13aca535f78aab518de102c86fe7217e2d1d`  
		Last Modified: Tue, 06 Dec 2022 04:08:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7ec231f354dd9452eb9dd010b908af0dee64ae8f3539f3420ce581f6bc97f8`  
		Last Modified: Tue, 06 Dec 2022 04:08:11 GMT  
		Size: 304.3 KB (304260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a274d6b33fdfdb3ff03c24d6b48fa9c1ad2b67698ae87efc6628f0a9f2a6c03`  
		Last Modified: Tue, 06 Dec 2022 04:08:20 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:442ee66855fb184f69fec37ef40d7299241705204afac8254e2747bf75c96b8e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61991111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9567bfcaad28e57bca18f8591427f8fcc30b5eaa4e8727dfa2f255c34235bc2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:05 GMT
ADD file:0688532a537bb23756917f3d062da18668cd55041d0ae6610cff386043ffbdd3 in / 
# Tue, 06 Dec 2022 01:40:05 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:36:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 02:36:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 02:36:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:54f3d93b8ab6f3a5195d99724d5bc911156006687d577448bd8e94d2fe049d4a`  
		Last Modified: Tue, 06 Dec 2022 01:46:02 GMT  
		Size: 51.2 MB (51207714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52f14263b329659da79ea4fcc974aadef164b5153566c19de9ced29a459fb32`  
		Last Modified: Tue, 06 Dec 2022 02:38:35 GMT  
		Size: 10.7 MB (10672362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000af179d21568271868a60e00d3a02ba057f979b6ecc853c0e63acb3936c2b3`  
		Last Modified: Tue, 06 Dec 2022 02:38:33 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bc8df4bf8edf0ca1930f9ae62123cb277fa05e81a481284d4224fd2b8eda74`  
		Last Modified: Tue, 06 Dec 2022 02:38:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f82edf13dc6975ebfb768a45e0428cd2a014991ed06cc785ae36ac908b64602`  
		Last Modified: Tue, 06 Dec 2022 02:38:34 GMT  
		Size: 108.7 KB (108695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2b9c826c1792ec0f2d646229375856ced52fdb0292dd5d81d4b84e92834e5e`  
		Last Modified: Tue, 06 Dec 2022 02:38:44 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
