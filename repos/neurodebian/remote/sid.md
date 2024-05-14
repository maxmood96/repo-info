## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:57238d7a00107cf2719ebbe57b8ebca28eaa7c09b85fa960f4230df9ff6603d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:d6f23bd21819674b163ecf6d32924d910d225448ff3518022e6e4517ff0a2a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64610069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97c9900b40f363d586167e78d0a9a1b29ca4e78d2add419fce9711a1e87c18d`
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

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5351af710581785e6f2098e3fda2a47d25fb0c14f95cd79fc7d70712d30c576e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65423858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2266100b38d8fe22c80c1af34961ed0354233c8c558eb4e5c86dc454b139c961`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:41 GMT
ADD file:65d77d3f6289af1318c696652b600f022ddbc3a1daaf105602e348ad91d2c41c in / 
# Tue, 14 May 2024 00:40:42 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:16:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:16:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 14 May 2024 03:16:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 14 May 2024 03:16:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66334a1d5d0f0597e9440b0db265b333533e2fce7f5bb2d1fba09c85ef6cd21d`  
		Last Modified: Tue, 14 May 2024 00:45:15 GMT  
		Size: 52.9 MB (52930287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d28a39104fd5e32ed412e20d214a05f37a1a4ec16fb97a9a449a83e52258347`  
		Last Modified: Tue, 14 May 2024 03:17:55 GMT  
		Size: 12.2 MB (12203403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e345603e50bdc3be68723503e6942f8482e09b422addd688b37650872fd3d672`  
		Last Modified: Tue, 14 May 2024 03:17:54 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d4647eb3dc1619353f3cc8078aae3ebf270c3f47cb280e016725bd6fda0aa`  
		Last Modified: Tue, 14 May 2024 03:17:54 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c81171b646346b09db33a14c3712df0f0f1ed3e82d9c5186dbf349c927fa9d`  
		Last Modified: Tue, 14 May 2024 03:17:54 GMT  
		Size: 288.2 KB (288160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:b6c09f454b40a21e5679f4b27007a526f7773056faaab75167beb2ac6c40e6ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65994337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d656edb6acc9dd16d1fa8e301c15f66c02d767a85492aa15aa5bb422e18ff5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:48:47 GMT
ADD file:e7eb6b079b0eae2716a306dfd153c88de0766961cbb0cbc2499648abc3b7bb7d in / 
# Tue, 14 May 2024 00:48:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:14:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:14:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 14 May 2024 01:14:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 14 May 2024 01:15:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:241b052c0f57772eb9a56c460c88c133545f781291832042a8e20e0fd5b01591`  
		Last Modified: Tue, 14 May 2024 00:54:59 GMT  
		Size: 53.5 MB (53539918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6432c619036630ab9cbaa4290dfee53004573077984943fec678cd8ad880b3b3`  
		Last Modified: Tue, 14 May 2024 01:16:31 GMT  
		Size: 12.2 MB (12164639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59801d1427ca4abfc6aadbe9f7f46d873038c2fa8ce83a8594b0acf005345bc2`  
		Last Modified: Tue, 14 May 2024 01:16:29 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a576d7123de0c664a246ed6ee290f283d6f95161e69bed1e2bf488f0b6adf2d`  
		Last Modified: Tue, 14 May 2024 01:16:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dd7767687678434aff9ec946d95ee379a4b328f9fb37492099bd03bd35a157`  
		Last Modified: Tue, 14 May 2024 01:16:29 GMT  
		Size: 287.8 KB (287778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
