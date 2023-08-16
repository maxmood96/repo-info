## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:bc20e10a5af1bc7ca8e59d8b30f28268d6d29323ee7590649b3a27c27245d829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:93f8d0afac93b903b63fa9359774326e1a25be96eb932e6b0f630d1247528fc5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5382eed41a72f0ff3b74550ad076459631f1d6d308c29f7b51c91db65318e484`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:19 GMT
ADD file:30ed10904e3533aa50c332544532891f0dcf06cce020988e07af9afa6b2f5df4 in / 
# Wed, 16 Aug 2023 01:00:20 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:13:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 10:13:17 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 10:13:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:13:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d6b7393fb4f375905c31c483d81ce2a2905f88aba8cb198874da2b54035bc41d`  
		Last Modified: Wed, 16 Aug 2023 01:05:31 GMT  
		Size: 50.5 MB (50498099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078d786e39fbdde08da5ac21348797106a8e48f83ec4f16eb988bae3d24b3d1f`  
		Last Modified: Wed, 16 Aug 2023 10:15:09 GMT  
		Size: 10.5 MB (10504726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067e4a986b67fcae5368b79e01f6f2bfa8c41b745cb020fcb702b8dec9ce0a8c`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39b10d61fb6b2b77af47566a04fb2f10162c788281459e74630ceeb4b713c2a`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e9b94a4b05fa98315a44b00a103167cea1a667dccf6483a4eb9f6201bac3b`  
		Last Modified: Wed, 16 Aug 2023 10:15:08 GMT  
		Size: 304.6 KB (304619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeffc707d6bc130465732198e61ac65ec3f1b7d04c28b3bf6d86a3286ca18869`  
		Last Modified: Wed, 16 Aug 2023 10:15:17 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:88f4b1a84b6f01382b277f7d3bf39f72a8b94b2548b554238fc77253f3ceb7b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60108549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7543797664e4133d57ddbb8a7a093b86e7323dfaa8a15c3327ab452d1a7db5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:18 GMT
ADD file:366546a703fa234d38591d2a54f10fbced83cc0e407775ad31751f0111c348c8 in / 
# Tue, 15 Aug 2023 23:40:18 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:50:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:50:44 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:50:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:50:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:745797452665e0b4d6f5d0f9b05ae67a86bccfea4ec3a2cf7c6dd89cbfafdd37`  
		Last Modified: Tue, 15 Aug 2023 23:44:16 GMT  
		Size: 49.3 MB (49290964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff548e71e5e2b2825cca5159e38ac0f04f9ea241d05e88b8df6c827bcc66890e`  
		Last Modified: Wed, 16 Aug 2023 03:52:19 GMT  
		Size: 10.5 MB (10510675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd3c3a2153366ee917527815d07c3d6084923d4377d36a0fb26dde691b7b20`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00dfdfdf86764a28629c52c3bcdfdad862c754d940385bbb1f38e6f03b18d8f3`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a825c8e8bc1a402e4fe8ab17fe0f155a3a9025417cb24bf4d2a2637170e57`  
		Last Modified: Wed, 16 Aug 2023 03:52:18 GMT  
		Size: 304.5 KB (304542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96918ab91a1c0ba75a677c85f091ac5a0d073d76bf8a1bc4f90cbdfc63f97c23`  
		Last Modified: Wed, 16 Aug 2023 03:52:27 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:d9dafca1013a713ff6fca9a964b8c9b56a92988935dfc370e02e1ab1693b1645
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62430837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bcd09ce9224a3e6205d4c33853d71f22d8c18f63259a4e7d8121b89ad39573`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:33 GMT
ADD file:f985eed393788dbeb3e4d9ab7f77d632d72f60bc5da30c59bb7de8fa3de0681c in / 
# Tue, 15 Aug 2023 23:39:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:41:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 16 Aug 2023 03:41:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 16 Aug 2023 03:41:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:41:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ce293edb9c35c6521b0a7d87a0d8e0252e4b0cab665a3103cb6d06e3e37cf414`  
		Last Modified: Tue, 15 Aug 2023 23:44:33 GMT  
		Size: 51.3 MB (51255460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c33de8dd8d88404193f8d100efd13ecaafbc18e3391f3688ce0c41b269c813`  
		Last Modified: Wed, 16 Aug 2023 03:42:41 GMT  
		Size: 10.9 MB (10868493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690636d1fbf114a0d369abbe65be2cbc0237d8715c0e8ef4b4226c1fb32cb310`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6912fa3cbe68256fbe65f857e365c177f93957e7048c96c4ff7ad44e3350b18`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f76675ef82d7692108de74c45d4c734a1277e8a1ad34a2383ba8e0cc3247c34`  
		Last Modified: Wed, 16 Aug 2023 03:42:40 GMT  
		Size: 304.5 KB (304516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9df965a7d01865ff78ea9517c27a9ca66828c8a0b44728b69854d721a577c5`  
		Last Modified: Wed, 16 Aug 2023 03:42:49 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
