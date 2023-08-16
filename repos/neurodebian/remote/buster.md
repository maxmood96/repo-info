## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:8da30a13d55f682cb7b5abcb1ba4ec1948a418aa379db648ccb706ee46032350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:0da68b4aca50e778ac715c49714c6bba2209cfc37cdb1444b03fb7fa7558b3c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61309456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea452dff405f01f746e680cb1dc3b4c1457238a9405245d4c2d0774760300ac`
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

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5c066f0b95d700c7c3bbb02258c68faf30f73bd15cbcb5c5faffeb0222bb1468
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60108194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17ce73f54623eae40a7273f88ce32130e6ee13f6b8397d25ffef4cf59444673`
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

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:62ca31b62277e996a6e5bc4002e25e2d0e4341dd8e20e7341d0209219f7f4ec0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62430481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff2c883e44081a3fcbf67700e217756905f3b28e33ba79d31601bbd3e9cbf14`
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
