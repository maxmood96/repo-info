## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:5afb85f2496d8635a69203a7c04ed9db8a465ba5db943be33917de1c4a47402d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:57ac9966967d90158d5ed14efce8cfb078c77c9e6ae7fde8cdd527fa68529771
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64360664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b301be77e333fac457a00b8d0b197da2d3576869ffcea92a39480c24fcd620`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:57 GMT
ADD file:abae7408d5e68c3a696c708e7c3eb4b503251a424e5ebe4d3c7c8f10051a6619 in / 
# Wed, 31 Jan 2024 22:36:57 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:25:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:25:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 01 Feb 2024 01:25:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 01 Feb 2024 01:25:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:25:39 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:cc8e35210c92074bcaff9b0f9819d85e3d2721df871a170c5ffb2c3ce4d09c7c`  
		Last Modified: Wed, 31 Jan 2024 22:42:59 GMT  
		Size: 52.3 MB (52332875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6821912443e09ed5fcde9def07fe26b2f9c1311e72d99c86ad124e52548987`  
		Last Modified: Thu, 01 Feb 2024 01:27:08 GMT  
		Size: 11.7 MB (11738726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62718a42b59eebc636221f49766656e8cecde2bbadb775de7df997c2ef16e7be`  
		Last Modified: Thu, 01 Feb 2024 01:27:07 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d45599960bddbf0ff9aebd5b7b45a6a78dee839419a81b5ae9d8edd42440eb`  
		Last Modified: Thu, 01 Feb 2024 01:27:07 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce0a9b048ba678bb8a097007afe11ecdc8874bde93a6888b56d887e4e0510e2`  
		Last Modified: Thu, 01 Feb 2024 01:27:07 GMT  
		Size: 286.7 KB (286662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7252c33e31e4b06161c9e46b6c5dc57c68fe389de6d83453b993ecd20b1a286b`  
		Last Modified: Thu, 01 Feb 2024 01:27:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d7c8f2f28dc1e595eeb1bba490fc13616a49895f872973f134f9837d1fd73431
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64207132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8eb745118df5606e0cae3133aca71d13033288e43223bf1b84c0fa6cc1ff348`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:34 GMT
ADD file:2954a14564e68bbee21d166d50487168fb308da137db675f9c3d1d24d2c9b4a2 in / 
# Wed, 31 Jan 2024 22:45:35 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:49:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:49:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 01 Feb 2024 07:49:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 01 Feb 2024 07:49:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:49:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8940f7446dbd5a08b1ac5dffe6fc85a0d545f6a8c5d7a0b7df016fc1158b7544`  
		Last Modified: Wed, 31 Jan 2024 22:51:02 GMT  
		Size: 52.2 MB (52190514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad8f58bc6b17662d95d75595143ee9000586220306864a3196e88ace9905b9c`  
		Last Modified: Thu, 01 Feb 2024 07:50:41 GMT  
		Size: 11.7 MB (11727134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b14044b814fd767af991237d262e06025c93cdbd55709a2a2f8152fb87cf21`  
		Last Modified: Thu, 01 Feb 2024 07:50:40 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85cef27729517a15ca005260bff2375f19ba6e749b65f8512ac69d6450b35f4`  
		Last Modified: Thu, 01 Feb 2024 07:50:40 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabeeab8e968faabdacb103c7bf646bede697cca5d7c28f4e4053c438ea60f6e`  
		Last Modified: Thu, 01 Feb 2024 07:50:40 GMT  
		Size: 287.1 KB (287079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65f1fbeb2f9a3eb160db54add10e9ccbbb6b829e3b2f2e6f4c14b978264d4b5`  
		Last Modified: Thu, 01 Feb 2024 07:50:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:8d52498248aa129487c56985a983901768ea84cd7de886734dc0d9b48d22f0d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65614827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44ad958d9f8d619dc893196dc8fdf279ce33ed507428fef081478e8275a5e8c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:40:38 GMT
ADD file:7eeb9c69e51143f9785ae65d9c9acb80a1be34c1ca4af1f148948207f4ece89a in / 
# Wed, 31 Jan 2024 22:40:39 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:18:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:18:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 31 Jan 2024 23:18:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 31 Jan 2024 23:18:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:18:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:f0db883d85c18095d81fccef71599ce9faa085ec0ca27cea8f5e7945eaf77bfb`  
		Last Modified: Wed, 31 Jan 2024 22:47:09 GMT  
		Size: 53.2 MB (53169190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6aa1d51442b8ab50d80e793210f699ed2f9caab4319f23c27d6f05297f98bf`  
		Last Modified: Wed, 31 Jan 2024 23:19:39 GMT  
		Size: 12.2 MB (12156682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0cb7d719f43e4148bb01260b4a36b3c7eec0defbdfef6600b4151623b8e232`  
		Last Modified: Wed, 31 Jan 2024 23:19:38 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6673aa394e8f64b36a4b331cd86637e059ba37cb7934e7d04377448b5642fe2`  
		Last Modified: Wed, 31 Jan 2024 23:19:38 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802b86d4819ffee6f479dfa30a9beb1e62d78a2fe20f072558a025d8371be889`  
		Last Modified: Wed, 31 Jan 2024 23:19:38 GMT  
		Size: 286.5 KB (286546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6112753d85fe495391c4bfa1f0644c4176a7ed0c320a6d1676ab3c573062953e`  
		Last Modified: Wed, 31 Jan 2024 23:19:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
