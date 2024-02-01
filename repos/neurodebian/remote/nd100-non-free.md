## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:7ac677e871622b326bbcf27ea4692a7bd651ef360ce8dc20888c93edca8b7f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1d5f18d098ab8267219568e929daa66d70935834edaaaa83d3bdadc47944c6e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61306700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96337da60bf3c575daf6fb8317572e6f640407476e9ed29bbb485d922c71e6eb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:27 GMT
ADD file:ac13007eb56f6e064fe27101dfa666f02b04f4ce9a2bcf3ade6cf6055562b7e8 in / 
# Thu, 11 Jan 2024 02:38:27 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:59:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:59:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 11 Jan 2024 08:59:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 11 Jan 2024 08:59:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 08:59:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:7418de5ce68f67dad705c01c70a7bb811f9b886f8d7aac2b66110d376046fdcb`  
		Last Modified: Thu, 11 Jan 2024 02:43:26 GMT  
		Size: 50.5 MB (50500254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c823618694b7aac7e8b10a13fbc857ebf35a9da9a1f06ab6422471719a5a89b`  
		Last Modified: Thu, 11 Jan 2024 09:00:58 GMT  
		Size: 10.5 MB (10504638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f8019fdc1f2cbc8d9c0e52931936773a6f42ddb9904f0c06aaff394ad4e140`  
		Last Modified: Thu, 11 Jan 2024 09:00:57 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c6a00d048b89d5ac18693b465067503677c70c6617962e0275e4dab4fc7f71`  
		Last Modified: Thu, 11 Jan 2024 09:00:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919576d5e02c8dc3ce24ebad199121c5e37b4c7749198b6538e53cec9cb8979d`  
		Last Modified: Thu, 11 Jan 2024 09:00:57 GMT  
		Size: 299.4 KB (299440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8653eef7719293bc1c0f7bd7c53f527854244e4936e272711e09d0430287f2`  
		Last Modified: Thu, 11 Jan 2024 09:01:06 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4bb9a020a72cc76c31f0b7e4dcae8b3dae97840e258410fd15d2bf8cf2e787fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60101373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6b84166e576173f17a9dce7a5639aab1c1f391047c36bfa14597115ef397a6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:05 GMT
ADD file:e9cd54dd40d18756610852bf97172fae748b0dc8eb39d2fb1c97181382daed3b in / 
# Thu, 11 Jan 2024 02:41:06 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:14:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:14:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 11 Jan 2024 09:14:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 11 Jan 2024 09:14:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:14:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ff2e543b6a43ccfdb1731587b58c288c29eb3947f78a5877f4fd9bb8dfa918b5`  
		Last Modified: Thu, 11 Jan 2024 02:45:04 GMT  
		Size: 49.3 MB (49288871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb0a9f94651904d033658261a67bd8ee5dae03841d5b1703cb9b184b64acff2`  
		Last Modified: Thu, 11 Jan 2024 09:15:58 GMT  
		Size: 10.5 MB (10510678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920b550a6210ec9c208e766ee1587bd6da26a32c0170b10b1876235fc1221a95`  
		Last Modified: Thu, 11 Jan 2024 09:15:56 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de992a88a203c7f443b49a987a0259887be18b791a4a084ecd2136ce3df3b8e`  
		Last Modified: Thu, 11 Jan 2024 09:15:56 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c621ff48bb20203ec4fbba1621ecf148561ef4b9d8d7c60f23557b7ee2d7e2c`  
		Last Modified: Thu, 11 Jan 2024 09:15:57 GMT  
		Size: 299.5 KB (299459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeb636941f86f3a8a6ba0f57a92fd0702edabf51d54db9a1c6c9a8847405515`  
		Last Modified: Thu, 11 Jan 2024 09:16:05 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:eae3dcc6b4d7c1be7311f9116b57aeaf0c91194b07f8d85e4072ff4d49786b89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62425330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6a6b12f2951a140f83076a1060813a029c654762470174f4da466dc1b909bb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:33 GMT
ADD file:f1db0427c60f5ce5c0fdf61794e7b45091e044f4032ea88ebf7c03ae7a7e4de6 in / 
# Wed, 31 Jan 2024 22:39:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:16:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:16:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 31 Jan 2024 23:16:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 31 Jan 2024 23:17:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:17:07 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:ba068490695163c38116b67ad60e1418ab3585ae8f45a5e4a0d07cbad5406814`  
		Last Modified: Wed, 31 Jan 2024 22:44:59 GMT  
		Size: 51.3 MB (51255213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a726386d8d202bc1fa1db471ba665dba2d0c35c9a16671b515c9651b0523c328`  
		Last Modified: Wed, 31 Jan 2024 23:18:40 GMT  
		Size: 10.9 MB (10868339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac35795479ace9366532004918a2b32d48a0c008abc47b041a137fd5ec753402`  
		Last Modified: Wed, 31 Jan 2024 23:18:38 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d100cba3a6d58cae3f15a9894d8da87e86f4e1471badb3d125e437b182312cc4`  
		Last Modified: Wed, 31 Jan 2024 23:18:38 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955ca688af182df62cea1633bd2d143bed97fc041f6d946508434d8f9e9c4985`  
		Last Modified: Wed, 31 Jan 2024 23:18:38 GMT  
		Size: 299.4 KB (299408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be82b90c6fa60c2542153f9b683c4bf69358d0135d36d9bb292f6e638e00f0e2`  
		Last Modified: Wed, 31 Jan 2024 23:18:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
