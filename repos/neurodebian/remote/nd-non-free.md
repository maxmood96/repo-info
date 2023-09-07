## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:55cdd5e47c29234704f78e1153161b36790feb4dc4b48b314af808864dd0e696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b771ee3290efa1a6c265af138725a8950240a5a9719d1dcaa90107df4c9a3717
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64169110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ad7b8bc81b61754cc3c0c2924d41f86ea94e73418d0115e3bfc254be913040`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:01:27 GMT
ADD file:48c88afb2094d5db855a4fe872b2cbb76a9d3c1b143c67463318da89ff28ed91 in / 
# Wed, 16 Aug 2023 01:01:27 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:14:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:14:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:14:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:14:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:14:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:c111fea192ed7adbc203c571a96a882a3741644731e862353e7c2f3259608f77`  
		Last Modified: Wed, 16 Aug 2023 01:07:20 GMT  
		Size: 49.6 MB (49617313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a1753a4167c634c5010550a1f4f417b282f2e72009c2a83a24d3d670c294ad`  
		Last Modified: Wed, 16 Aug 2023 10:16:07 GMT  
		Size: 14.3 MB (14264309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed6425f36a7f840361853d24139d567df7ebcdf25533add46ae9b71a1b58899`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffee644b7121bfa1a75452287f0ec6760aca7d2443b5b40ab08d661983c822`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d34f1a1b9fad277ce6fab6fb5714ff0e477efdacb71481b1a19571270f5c72`  
		Last Modified: Wed, 16 Aug 2023 10:16:06 GMT  
		Size: 285.1 KB (285086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd83e062af1b4b3ed0bbe171920540cba07de2a176984b2dd9c1b9896a8146bf`  
		Last Modified: Wed, 16 Aug 2023 10:16:16 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:68103a114d46ec109870f9907a76cce6573e5d061e65bc487008c470c2fca20a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63780572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b48d3b4bc40be4cc63ead027f6c954b60660517805c27d724bad5bbd02312`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:41 GMT
ADD file:3fad0766985d4815384b52dbb02c3f23c3f0c6e9b05ae96cdb2f60692ebe3c47 in / 
# Thu, 07 Sep 2023 00:40:42 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:34:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:34:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 07 Sep 2023 09:34:37 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 07 Sep 2023 09:34:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:34:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:352986db96f4040761867c771dd7419bd03916c5a2f552680219ad48902eec34`  
		Last Modified: Thu, 07 Sep 2023 00:45:36 GMT  
		Size: 49.4 MB (49413074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd83822cb5183fa52ba8796ae530db76139430ea12dd7ba7b0b7d2600f3c4bd`  
		Last Modified: Thu, 07 Sep 2023 09:36:07 GMT  
		Size: 14.1 MB (14081293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f12b840d2fe814f1e0c677b1264b05eeee794f95b62a15f8fdebe3c487f1f2`  
		Last Modified: Thu, 07 Sep 2023 09:36:05 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c0d7739cf693bfd52f4e8ba9bf297736054fbf748d4f93d43a5ce7c614d837`  
		Last Modified: Thu, 07 Sep 2023 09:36:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86210c1554378900877143c9f650d66216976cb3bbe2f67dbbbc2241d006882`  
		Last Modified: Thu, 07 Sep 2023 09:36:06 GMT  
		Size: 283.8 KB (283804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3449423377434422f4ddddc2cde2a53d9455ea348cde683d78bbb25a0e193025`  
		Last Modified: Thu, 07 Sep 2023 09:36:16 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4921467d6df857e14d8b8556102df8c710077c33522d13dc47096ba8615d54aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65480198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71be0013e9512bb1486ad2fabbab4463bf5e08f7ec12a35df6ad29a56c0a5c4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:40 GMT
ADD file:ff611322e6674f9fde9d60d146cd9f1206176a7ad0bffa135200bb5ce18ef6fb in / 
# Thu, 07 Sep 2023 00:40:41 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:06:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:06:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 07 Sep 2023 01:06:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 07 Sep 2023 01:06:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:07:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:e341a6bda5bb8b3c55cc00b75f2a70088193c4ac06611dc91b32f6ca7c58df58`  
		Last Modified: Thu, 07 Sep 2023 00:47:07 GMT  
		Size: 50.5 MB (50501474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dec009f435be81ab6333f0fd04d3e3f14037e4180263c04a53752eaccaa5ab`  
		Last Modified: Thu, 07 Sep 2023 01:08:26 GMT  
		Size: 14.7 MB (14693114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad8e83f3fb87a840d0bbd2994fda0a110c1447982cacd72189532f404d101e1`  
		Last Modified: Thu, 07 Sep 2023 01:08:23 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e977f2bbdc42f8276c1750e2b32184d5bf0958603b0112a7ca4ea1cb4a9cb1ad`  
		Last Modified: Thu, 07 Sep 2023 01:08:23 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044d1e8cd023dad8f93c5476dc5421a67a79dcc4b05bd1731a93d7dc41919823`  
		Last Modified: Thu, 07 Sep 2023 01:08:23 GMT  
		Size: 283.2 KB (283208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbc46dacb688d46e7872a75321d7ffc16f7d903193c15fde173df1a289e16fe`  
		Last Modified: Thu, 07 Sep 2023 01:08:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
