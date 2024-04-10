## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:3930d67d9a26044c5fe9756e0e32e5c610bd41d2525d8ec764975aaa57808477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:89e812bf418a3b81e535987b9aea953b67676ddab317f4efc70be45753040048
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66710744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2eac4758b8ec401f4587c28ac2278706df8fa00453733de565febda6199b63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:51:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:51:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 09:51:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 09:51:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:51:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc27acd292d213af99b3b7b4a74c139da38205e51ec1547894f737ff76446531`  
		Last Modified: Wed, 10 Apr 2024 09:53:05 GMT  
		Size: 11.3 MB (11310854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4eb0cb86f7c768a23833f47021280ffb32eb94c126812ec66292370a8cfe13`  
		Last Modified: Wed, 10 Apr 2024 09:53:04 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a021ab8d25061d0cd6955408094a8e2ccf5cc5ec236773a0a01ebd6d05d85ef8`  
		Last Modified: Wed, 10 Apr 2024 09:53:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f278c5b5f3193eb46df4ba36f2086b30888e5eaac17ceed4bf0ad240b4726d1e`  
		Last Modified: Wed, 10 Apr 2024 09:53:04 GMT  
		Size: 307.3 KB (307252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26af55272cfb23a90408ea5975ee4b321e83d07b7e48491b9cea4797f14f10d`  
		Last Modified: Wed, 10 Apr 2024 09:53:14 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:176a692a1d73cc5b38da8fa379bb81826406144fb11f0d937bc5bdd4e09c45d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65351780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e3cf4a83ea23479e773eaa23cc8101357716fc0058482c6c431913837c2f70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:24:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:24:17 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:24:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c4e0ed3ca37f8d8d319efb1e4e47d588e61a1d0c1435cb7f5bd6b49a0ce49c`  
		Last Modified: Wed, 10 Apr 2024 07:25:45 GMT  
		Size: 11.3 MB (11313100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc807a9395116fa54f2a556c60adee6c73329a1105c255cf28c8e5609dab3d82`  
		Last Modified: Wed, 10 Apr 2024 07:25:44 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcc5fe9e3e9b601d4632ceb1943ddcf163728753df9d447148b368d89218264`  
		Last Modified: Wed, 10 Apr 2024 07:25:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a648a34e5a78679e5bc88e99ac5eac8dd1d5abc59fa1589fb9be96f5da533b`  
		Last Modified: Wed, 10 Apr 2024 07:25:44 GMT  
		Size: 307.1 KB (307132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf00b4e262140dfc2bbb7644ef3f4c10dbb2faab2ce8430822d8c72fad0d8069`  
		Last Modified: Wed, 10 Apr 2024 07:25:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b0864a7383d8c68c8b1237062b619ecce06878f1742e656c75ee017a823f2905
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68083557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a96f942a67cc85ef7cb701a6b443e8871de980aa20c777fc7f91299880c742d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:22 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
# Wed, 10 Apr 2024 00:57:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a843efcd4de34554fe990926cb1888702d19f617b066dc9494c8c1b615ae45ad`  
		Last Modified: Wed, 10 Apr 2024 07:24:54 GMT  
		Size: 11.7 MB (11707925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35819b2004141e930bba02a504efaf3504c0970865d527d6336246ee4310ded8`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3caf7de7396b15fe97edcfd0cc40e2a31201fe78ffb69eda49ac2f961be65e4d`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92e584bf5c2da8feca9223d74412055e85661a878463498f78a1d7c73399cb0`  
		Last Modified: Wed, 10 Apr 2024 07:24:51 GMT  
		Size: 307.1 KB (307067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120b7317a3b37952c50216ba072c4c503b22262cb884b3866f9fef9b2f40bc05`  
		Last Modified: Wed, 10 Apr 2024 07:25:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
