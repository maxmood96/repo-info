<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bionic`](#neurodebianbionic)
-	[`neurodebian:bionic-non-free`](#neurodebianbionic-non-free)
-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:buster`](#neurodebianbuster)
-	[`neurodebian:buster-non-free`](#neurodebianbuster-non-free)
-	[`neurodebian:focal`](#neurodebianfocal)
-	[`neurodebian:focal-non-free`](#neurodebianfocal-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:nd100`](#neurodebiannd100)
-	[`neurodebian:nd100-non-free`](#neurodebiannd100-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd18.04`](#neurodebiannd1804)
-	[`neurodebian:nd18.04-non-free`](#neurodebiannd1804-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)

## `neurodebian:bionic`

```console
$ docker pull neurodebian@sha256:39078ae512762502c8dd9c99bdc04032b9372eb9c95adccaefe4aa9335a48ce2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:7d53ca6634bc4f71e803673f7e026a3ed063157817863650399f9949522d7a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30487136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a14ed1ba14993d490c686fd0ee743fab1e10f9718be288c5ffe99eb93c2684e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Tue, 30 May 2023 10:03:37 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b18c561194df3348da8d2b6a32ce63573a55c466f094dddf86b6ae60d1a27`  
		Last Modified: Fri, 31 May 2024 01:56:46 GMT  
		Size: 4.7 MB (4687003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465ef96fd4980c8f189fcc771c808915f063e4f3a24af79dbd4f7aeae609399e`  
		Last Modified: Fri, 31 May 2024 01:56:45 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a427df721c2b95fd6cdd252c60c00de7d94e502f684de005caaa8123bebfa6`  
		Last Modified: Fri, 31 May 2024 01:56:45 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7383c932e309628794f537a905e524fb3f7f5bbc53a3b5836cdb206815f89e`  
		Last Modified: Fri, 31 May 2024 01:56:46 GMT  
		Size: 107.0 KB (106959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bionic` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f823abed5bf0f9b5b7d1036931e95bce95877311d47e05e8738048ef73b622d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1920845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226b0897fdea8020ae75200a53b1f794b410f8188ce743095eef9d8b40b181fd`

```dockerfile
```

-	Layers:
	-	`sha256:59e86676c2427387b28ada60adfdd9939891e96da628232e059eb1b658d0522b`  
		Last Modified: Fri, 31 May 2024 01:56:46 GMT  
		Size: 1.9 MB (1907475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b14dd6f16011ffce67a8c764cde750bdf471aed1f3814b9bbdbf226c104a6b`  
		Last Modified: Fri, 31 May 2024 01:56:45 GMT  
		Size: 13.4 KB (13370 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bionic` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:576d684548e2dd160f926f3e3ab856ee19bf99609251b51346517a767bf22c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27090983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9899163376352bd0721873bf1a79dc123967b36d67bfe9cf09122e730bca535`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Tue, 30 May 2023 10:03:42 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddda72376ca07b81a58afcd07ab707bd2b65eaaf4b638adda578079eff8f5024`  
		Last Modified: Fri, 31 May 2024 11:26:02 GMT  
		Size: 4.3 MB (4268722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7386017dd0da8e1005b1406e7a864fd7c7378741bac7f1e6974da156b71c24f3`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d876a1c7682fb795ebc1e91e721061bfbdcea91113e6cf1289eddeb3ab5774`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b133983b820f58b53a8477086ebb696d7ca345e5daf8210097cde1b3d6f130c9`  
		Last Modified: Fri, 31 May 2024 11:26:03 GMT  
		Size: 106.9 KB (106852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bionic` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7d883ac5d61db58829f06278d94957b67b77a5702428e6434ad3a326595e48a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1921307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1facb2b2a872e5b8467f689e81da8e47b45d960a8e80642f4aa535467de08d9e`

```dockerfile
```

-	Layers:
	-	`sha256:74ccfed9bf877a74e0f2cbac4eed8243444b2c0870e5e297bd77097d98b4d391`  
		Last Modified: Fri, 31 May 2024 11:26:02 GMT  
		Size: 1.9 MB (1907658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477a659704ac1e9f683438b6b7a4bc2518c393f37c76a2349a34ad1fc56085dd`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 13.6 KB (13649 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:0ea6a040d3005bbc6d6adbde1b3c4dae2d89a4c4dd943ba32aa350e14452886f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:18169413818de1fdc43e158c849d34850b02a6390905f424f8b10ca50211ea5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30487499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad09230fe8daacf1f1a34dc9035a37fbae4351949aa366e5f398789759a0b839`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Tue, 30 May 2023 10:03:37 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e5846e93887a546e4f0410696260f4c77e386470678fb9087874d2e2524648`  
		Last Modified: Fri, 31 May 2024 01:53:27 GMT  
		Size: 4.7 MB (4687092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed4ee21cce42c14e3fb8fc307e972c22e1f37766ce10ea56c1b9a8a0a3b4e7f`  
		Last Modified: Fri, 31 May 2024 01:53:27 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e9dc044f0c27fa2a4801bd9cfe358b5963621bb4678ed04eaeaa39b47e216d`  
		Last Modified: Fri, 31 May 2024 01:53:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc8e83d4f824da3b76b601e84201c6a07c69a82d7fccea5c2c38a089959d580`  
		Last Modified: Fri, 31 May 2024 01:53:28 GMT  
		Size: 107.0 KB (106976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8aac03308dee46930f831ecbedcb6dbbfff06484b3e1e610839f45e1bc49e9`  
		Last Modified: Fri, 31 May 2024 01:53:28 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bionic-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:880afd29b8e91716e066711fb12dc7f417be006872cbaccd832e847019ef7cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1923112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f4199010c3c203b7b6090e2041c2d2d807bba800667a37d79712217f5d9782`

```dockerfile
```

-	Layers:
	-	`sha256:9ca82aa12724fbd0393e316e569d6ce7b654947400243964ec2d7559dd11f17b`  
		Last Modified: Fri, 31 May 2024 01:53:27 GMT  
		Size: 1.9 MB (1907511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd1a8a30123b9a8b1f54a4c61dcc0b6bd5ff9ebfaf54e0d66be9e3d7b9a925a`  
		Last Modified: Fri, 31 May 2024 01:53:26 GMT  
		Size: 15.6 KB (15601 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bionic-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9c0087fb2593667a29da5e15ca6c6195d981098e591806dbc153c933ab206780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27091244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854f697b18ee9a7e7576402c46570e83539fea823644d026b982df4cad449eba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Tue, 30 May 2023 10:03:42 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddda72376ca07b81a58afcd07ab707bd2b65eaaf4b638adda578079eff8f5024`  
		Last Modified: Fri, 31 May 2024 11:26:02 GMT  
		Size: 4.3 MB (4268722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7386017dd0da8e1005b1406e7a864fd7c7378741bac7f1e6974da156b71c24f3`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d876a1c7682fb795ebc1e91e721061bfbdcea91113e6cf1289eddeb3ab5774`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b133983b820f58b53a8477086ebb696d7ca345e5daf8210097cde1b3d6f130c9`  
		Last Modified: Fri, 31 May 2024 11:26:03 GMT  
		Size: 106.9 KB (106852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3db3528f80fffc9adc3f1840a8ce5597384283543a1634e3a255e81a5affd8`  
		Last Modified: Fri, 31 May 2024 12:13:46 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bionic-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a98b30791125fe37b5ddf48f5d03eddced0fda6fb5f219e49c18dff3963021e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1923573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd87183851da7fa8aa438d607d5c9dd841e3703014a8d9bb101d01f972e7c472`

```dockerfile
```

-	Layers:
	-	`sha256:6bd54ab750554eea7ef069ed465d824a8167370a301986aa94720c173807a075`  
		Last Modified: Fri, 31 May 2024 12:13:46 GMT  
		Size: 1.9 MB (1907694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1028c37d9672e46133b86c2713ededb3f570948468eac19912954a30057615`  
		Last Modified: Fri, 31 May 2024 12:13:45 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:72e661f83c596638a0c5504858cf56d93843a60aa19939a3ae08699c9098c660
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:8003ddd6f73b7806bc9583ea35d61132dc3378a3b194e0194fad7d3611cb95d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60937750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab80b10beb2a161f42eceb87ee4ba0552673f0c26475cd6eb2f527b436ec3da`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d0d5ec172ba144071ed0223437f3e4b990d14a4ac73b3f8aa119fdec79b9d2`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 11.3 MB (11266570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31940436a11ab29fc862e2d14d020075964dcb59f967bff291d857751bd4d197`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6de3ad8d62b9a7799615ee74064490747e19dfcf3c526742a4e60bac1397b6`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9baa1fb88a8638cd71a6802afce4c4b8e3980ba78a41930dab72ae419205b7`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 92.8 KB (92801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0aef42c6e0933296b5b46229b5757715801e8e0cbfc579d6bb261a5900300dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f8dc494e821e0ec0217ed94cb1b13b95699d0d150843aea5001b45df309e4d`

```dockerfile
```

-	Layers:
	-	`sha256:257120a633cceccddc68b5f94e49b59497b162ca95753b43f3396da277ab65f8`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 3.9 MB (3901743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c08d4dbe78cc309275b9c9eec0dfc9bd127c7b5d47601255c335c2ae6b2757a2`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 13.4 KB (13428 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6213e2c292c45b49cca98fe498a6808f2700584a9628e3a5624664d9840b87ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60940537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6100f105e85e080929e093c60771b4ca4ea252a385959b9b340af469a157696b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9782ebad61654b7a2473c30e527f7a02ef0ff05bbeecddfa2c2a63f5e2e99048`  
		Last Modified: Fri, 31 May 2024 14:44:20 GMT  
		Size: 11.2 MB (11232082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ee0a093ea753330fd619da92cd9d8620723145c8a836f8b74d64edf92a5d14`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e17f23f6fb69d4dea07617d31ead77946fcac635bc98263d0e0edfd62d3a4`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b77a1d67cd06ab552ba0ded4026133eecdee96d5c48543f468b3922517a9c4e`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 93.1 KB (93077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:54701503357d38dbf5ace89b77543c8fee2f2b62adb377e7e960062c2516a02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd05fd8622dccb239d931c85ba833255c0c1529b61cee5e678e8a219b7b04f8`

```dockerfile
```

-	Layers:
	-	`sha256:faadff5adb164e444a55b837fc6ce43c32d2f30627d4d1a82359fb8fe02245f4`  
		Last Modified: Fri, 31 May 2024 14:44:20 GMT  
		Size: 3.9 MB (3901984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cc38b6d237c2ebcca5ba6cf809711edf85703898a921cc5c6525ad6628ec43`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 13.7 KB (13708 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:b1ea3f82110646d04e2cd193cfcc390d242aef8f792d7c10cb868bb55028856e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62386418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff4e0dbf43c1e191ed8ab62082ff8800631ddda751cd3bf73dfd9466cdda4a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654914778f47e9569f4279608f872556930f59a164aef5c622de67fc5edd6f82`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 11.7 MB (11689077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763ff0412f0e24675a3c0094d231bb5d4e8e02027bf12f3b704a8d7af2450df`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef928bf7664c03b3c9234628507b67eecebb9081c42037bf5c7ca67f4433ae`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3051f898514f269b148860e9e91bfca7792a107c5fbf163511aa3cec10916233`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 92.9 KB (92909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:707caef59da5288b96b2f894add20f103d29398bf92b5384278fddcf7021c770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a559258217bbe91bcc304ed53adfd496f2848b2e2d4826ba094c773e63535de`

```dockerfile
```

-	Layers:
	-	`sha256:eeac70b13c9895aa8af3bec72409fb2823f2e7ca87b2c0aed76b6ccb8d679b19`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 3.9 MB (3899664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf78c99d9ca5eda2035fd438e3088bc64a084267eca3dffcfd65fb7e68f233f7`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 13.5 KB (13452 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:0f88bd0ec5e17d2cb503f429779d919f272278d590eb14fcc8172dc168347568
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1324249971b25b9e0f7bfbcb4ba4160e30dd14a3aee17827942c6fd196b21c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60938168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e3bed1d904015142866727f1c9ef5b093e2ab3d017858e81fd44ce8e646a95`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de5108429a11f59373651715b9784a49e539ede6e3f805e15791de2362df062`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 11.3 MB (11266565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55dc84dd6d1ef1641e3007a6900bad1f55de89683e01abb5b12c5bf778734be`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619037df3f69df28e13ebdf7c547a7a3edb46499636b2fa8b88ff6600f6bf41e`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f222c14670fcb7af3f8ba4eaa5016da2c015963ac7772601264c04088c585d7c`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 92.8 KB (92792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb0f830d1ccf6969fbc75d17d324667ee498ad683d50f823a83514cba413ac6`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:be881a18320b4f1498b1859437596d983b02d695b68298dc8c55a34c9fafb9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab935771651c8d1921eea385f4395ef910b7bb94a2d465db94c9c38a88b1f5d5`

```dockerfile
```

-	Layers:
	-	`sha256:15c1e7b9047fffe4ee424e2d4afa5c012d873d4f0662e04926797e43b68ecc63`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 3.9 MB (3901779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d38a08e967e42b6ccdbb3163ff5f5f3b750a4689b8b22f34ea9a7167aa86b0f`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 15.5 KB (15461 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d618f33d5af2fb31fa36796bfd87f6a8c5170c6f6e4cfa37a82c5037896ff583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60940966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394cffc10c82bc96ff0460638c0e5b4940d173aa5cffc9ccdd2496c4984246e1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9782ebad61654b7a2473c30e527f7a02ef0ff05bbeecddfa2c2a63f5e2e99048`  
		Last Modified: Fri, 31 May 2024 14:44:20 GMT  
		Size: 11.2 MB (11232082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ee0a093ea753330fd619da92cd9d8620723145c8a836f8b74d64edf92a5d14`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e17f23f6fb69d4dea07617d31ead77946fcac635bc98263d0e0edfd62d3a4`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b77a1d67cd06ab552ba0ded4026133eecdee96d5c48543f468b3922517a9c4e`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 93.1 KB (93077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd8147b4588fef5f9141e32cbd7dbba8d5316da8488ec40f6aa5ae93dab2c82`  
		Last Modified: Fri, 31 May 2024 14:44:41 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a8574c6d120f66dd79367bbf464cf086bf7fc57db846e16e4821b635ebe1c89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82e6f2cd6c502f65580cc742a997c0e189ce903ee23cc816fef9f92165a897e`

```dockerfile
```

-	Layers:
	-	`sha256:2ef168679fafdc885aedd74fab6eb619f02fa79603bf0e20ae70ba14840c6e7a`  
		Last Modified: Fri, 31 May 2024 14:44:41 GMT  
		Size: 3.9 MB (3902020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e441abb00e97fa0e0d88299ab5846ddbeb86dfa258473db0c554cd7c5edbf06`  
		Last Modified: Fri, 31 May 2024 14:44:41 GMT  
		Size: 15.7 KB (15740 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7d6c8b4235db55cc82515f58088ffe599c694475bf9a61ffdb1458c09c883ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62386687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4239d56f5279cdea7597ea3479ee0379a5db524731ffa3a8897d35c876429e6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ffa67f849088d881ec1bd3050a216a615ede2edb4a511728ab5579a4fae22`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 11.7 MB (11688926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d8837ad2608097649f544d67a4577b1866865138f9e8a31b177912f5dce031`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161d8b08f6c9b9bd78b7414abdff21676319fc84d129807f18c1b8bfbe0305ce`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16fdac0c82ae1c1ccc8e105f8f96121d356b25ed71c9e2f32f7b680ee7841fb`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 92.9 KB (92895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad11b88e0c406f04ba1f7bfc5b1e04abf93bbd0bb16200a45f9560e4aa5c536`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:064e42db5fb916ae8be69bc1f8b43ddc7e644e625a376fa6d05eb362ccbf9310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00f6fa8bc6946b7ac2df2495e1bbb4e29e45525ca16dea8af7b9c0d71326442`

```dockerfile
```

-	Layers:
	-	`sha256:4791f9f5accce2cb9c311cea7d28bfda43d210e219ed131cb338a3a4195c767a`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 3.9 MB (3899700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432c1acfda6da922b96c421befb8a54378dbc7ca4b5d79bf4ffc808a14ddbca1`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 15.5 KB (15483 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:f6e3e55fff88d76cefd14b3174f8f430397f89f8b3af15370d60ceeb6e7f4d29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:af0d2b93bcb42fd81d4aaef410dd4472adacabed56158f921f2f734107d574d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66307144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c371f8b59748f5cee78657d02842b010304a574eb20a5eff38c2269418a34121`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38696ace0e231833c5350b1141146fa871838e0f66f1f7490af4c5402b3eeac7`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 11.1 MB (11104999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c87467765b5a37d61c04f087fa4e848e9329b99d686598d39b5116fa5232719`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8100950653fc9224fce0d1d05eaee9e8cefed042e6de64d30b5731ad280ed05`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4314a0c2f43354c94fbb29548509614fcfb953500f3a32fb633f563d0bfdbe`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 100.8 KB (100757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7b3feb473978c56e0e6402c12cea3185c3dc1256496c90b321606e70c55bb5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2936220a96affe48eca18b1cb6f18d0540bf04b0197243276f9cc4e3def74a4`

```dockerfile
```

-	Layers:
	-	`sha256:290468390b78978c5f76889d14246e2e0fa803ac3deab6ea9643860a0c957a14`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 4.2 MB (4199042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85226dba484b356b8e0c43298c973e5e51c14f40e515bb3f8881936c18b1147`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 13.7 KB (13737 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bfda43b28611976c87ccbadb7e5ea0d877660f7252cf42e2abfc8b68e01ebd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8aee6e5a024afaa1fa4cae9d2599683aa2748e22f795ff4a85beb6ef4d0fbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1483c42dcb365aa70f1ee657cb621d71108a07cb14e7da7c0af1670b1d3dc`  
		Last Modified: Fri, 31 May 2024 14:43:25 GMT  
		Size: 11.1 MB (11105807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bdea9458a37f5e1417a645e4803ce863ee56f1bb909725f8a36979925dae88`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a358d18ad53e6c2f3626a6322cc6c11247f800ae4b985a091f6495eba713135b`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf2eb23fc03995a0b59c27e2f55adfc7906966f111740c748bb549fa4bda575`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 100.7 KB (100692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eaebc4698a949504bcb6c45f41ad30d9ff6b662b4686d2bcca1e2a0a21854bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bceafa6b6b5c0bf69ae9243a8a5b812fb7bcfa07e0e9bcaa12c82780278c87`

```dockerfile
```

-	Layers:
	-	`sha256:59c311a36ac8eb21fa89848f79a995fd2cb7799ed68a779ebb56a20a681b4633`  
		Last Modified: Fri, 31 May 2024 14:43:25 GMT  
		Size: 4.2 MB (4198659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae78608efcc11c0de2680a9c0c77c9a21def4c0676b81770ad20443d329fd3c`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:cabcf9350018fb62481d82da2d505e7435e413b523ffebfcc9b7d080ca3248d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88df1df83a11719da37c9375a2ec92d392548f66178495fbaa15ac872d52ce6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36508bc53306c02a9ef12049a2feecd1ebe42c6a54a9832472dc4a2dcf9f2c08`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 11.5 MB (11500070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650c52e044f44142bd08d3c99a7d5bb60aece0e021e835404c71f0536348cac7`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a9f7821bb8e6b0e0776e2b828f75a95c812314e6cb6a1c256c944d6ce720bd`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8868307403b220244baee51b838b348d00e384e65031382e9c786b28a9ec9f`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 100.6 KB (100649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea9a8508876015fc24d1696a07b00dee5dd053bf937c9f4480fd9c8c2b61ec11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4209252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b9051a1b5507153426df6c9faf52f91ef695a1e2b336bd9ba344c819261aae`

```dockerfile
```

-	Layers:
	-	`sha256:920dffb7e2a35971c60e1b62223af049b0b7015216e62ffd5b83c0c380c72d06`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 4.2 MB (4195497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082631cbc44059d106b213d5b38760209d1d120834d9b001cdb35972f003c889`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:388f6c2461bc209a692170f696d1f5ff96615b60c45bc27f86de6f1eef1b9fb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:84219b6ad2c59d4349766f7ea41188ef7fd7f23e797f234aa2fc118476d87a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66307474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00919434e4703f6acd6065bc95f564b675939dc982ac937077fb392e2b545964`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fff6731503f1b1a12f3ec6074982a0a7c9e1faacd14096103760258566582b`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 11.1 MB (11104993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ed83a5d194b8125fc4475a7474d7614f9fa2cdaa8ef76360838fc01af94e79`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87281e9a3b4c0d00588f26599ef01f9cb268f821a34af340cd347f8c79442196`  
		Last Modified: Fri, 31 May 2024 00:56:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52629961e0dfe4a11e23ee3273dfc2941ef9296958ce0433be941e583fd3545`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 100.7 KB (100736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a7775c23e5a426688a89fe8bb88b071c4b67d2c0c5bcfc7762283e0c64a8eb`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f5badf72a6a31f4df91f889b70573094f100208cb79dc40f13ebba462e395f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752e07c04e896d0e9354d9f9aaeea038b337272f1c2970023a1a6c328cfab70`

```dockerfile
```

-	Layers:
	-	`sha256:1c8a56fac5dd5913e2895f29ade5a290d191979513f8716a9f8b6417694c831e`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 4.2 MB (4199082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d009cbb1fc1738caa42c4c5f123155cca5ae8713acd80bac0f8599a98214bb7`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5d1cf82cceda318c0dd41a8a0400d8411edc8a4d51ee0500d5d15b787f48c559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56caf73109cc0abb9aec10f6936d04cff9ecc5e4ed695667363742eb5c0c880`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1483c42dcb365aa70f1ee657cb621d71108a07cb14e7da7c0af1670b1d3dc`  
		Last Modified: Fri, 31 May 2024 14:43:25 GMT  
		Size: 11.1 MB (11105807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bdea9458a37f5e1417a645e4803ce863ee56f1bb909725f8a36979925dae88`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a358d18ad53e6c2f3626a6322cc6c11247f800ae4b985a091f6495eba713135b`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf2eb23fc03995a0b59c27e2f55adfc7906966f111740c748bb549fa4bda575`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 100.7 KB (100692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8729b3ff44329714773e4eb7c4046bcdce6dcd6ddc587ddc086d3594ea516b`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9c183078ed2c49b83568bf2f7c05cf59aa86563317db10e1fd35dfd0c4700705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b2481a942ef60260cd04118ded9798eab96a09d5a9de29130742c9d682bac8`

```dockerfile
```

-	Layers:
	-	`sha256:a8cb3999134b399777bdccdbcfd6a6470c17788e420fd152629355c483c2d10c`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 4.2 MB (4198699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb260b9d6aa6319449c343ab09e6d08a9472f4d08310d1d79af533866fbeed82`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 16.1 KB (16067 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:30c029632c96bf37af9b76eb0393927bcf408d4d4637bddf613a7594b2681b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5864c6def933a6b6dd9adfb7a5ec63fd1f46aed4cd44d9bfd0cbe3d67f45c8c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b13addd2b2a32b9d1ff2ea9286439b5540ef92b6f2a15ae59e20801eaeb8115`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 11.5 MB (11500167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925784d52a7a52e17776422204b33b6f319d5ac291eecaed873d7c75d0bf7b5e`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc25404734dead4fcf99099c0b8c4c255e177881c3cf9e4bd15eecdda5bbfeb`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77175288a751964832d472ca502af30d298ab6d18b500e39100c7e2cf1941a1e`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 100.7 KB (100656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403eee5dd3ac973d264d6caf142749476a40597c843100f860fd812bbdd7152`  
		Last Modified: Thu, 13 Jun 2024 01:59:16 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20b1a751fa916af4b95b9306d65f00cc6ede2b46bebc04dd23cc8fd44391f864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bf79df5b568b2fef0e797dc3f58e562b7992622978ab8ae0de582edd25ac64`

```dockerfile
```

-	Layers:
	-	`sha256:5b95beda90bc46a2b778e530d4afd832492d8e6d2ba670872dd2bd272173e02f`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 4.2 MB (4195537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42daf680929d419028ac29504c6aa3762fea17ac4478e351fac146d840b2c94`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:157ca5d3647d5f702e04e110d4132355e9d04c74c3f170d82768b02fef2c91f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:020104f3971254f7e7ecda9d7906735733e55360f142eb78dc36c229471ebbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61070627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc56267455d2457752fbd7f8ef9bd1351f76f73d7f36ca0755faf9bdea833d8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723d87c39a56b2dd8a62649501bf04ba3a687a53896c94468000a095aaed760c`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 10.3 MB (10307517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1e2e602b28270d610b56d107afb7c3d4e767a70a6b91da844db452b91eb293`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d822bf0f40147d3330203054210369cf3c5dc3a52c16fc1726e82cfc84284616`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222234ed4691c00c09d259495a67f1e32ba942cd3f8c73cfff42245ad61d1327`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 104.2 KB (104212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:69131987bd6fe23325f21f49abca3952217bf6bb8340de090f82c2c03bbeb54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903b524f67be676e0a9620c5cfcaf385fb91379bd7be09e955dd7462a04a1ae0`

```dockerfile
```

-	Layers:
	-	`sha256:f1656c8c3a6eaa5e531f96856c15c839a51124b4c946824bb634826eae237680`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 4.2 MB (4215066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8cec8865692dfd27d4aa16a39200a8bcc72abbd0269f2d814dd2579901ab2f9`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 13.4 KB (13399 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:176ea7c06f6ea8f6ba781055db94356ee8143d00476e2f10e2e0afd2ff1535c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59872536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03153f64313411fe1da52555de68c42bc9ce00711b014e5fcc7da41d4f2415e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd9c59acf204c0d81aff8b7e5da56cc3b76c258fa40d482df9e225cd533596`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 10.3 MB (10313209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cc3300b9846c0e9c7dba482c8c981db848d2eeb56f74c62c65a1debee89e29`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60fd2e75c963791cd3b0929bb3c01c7671ec64f140a3ac83cf1212b4a5b5c4b`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e238e2f4604a403218d3037f6bf35bb3d8d7e071f2dba1a6a88fbe012a1abb1`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 104.2 KB (104250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:11acc36e9dc4881113c767f319b6fa4d3a7951225685756f733dbabcfce3c12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148c1afddd6bfd55467d4fe9da6aff8cdba3fbb67af8bc72b7f4db65583f8219`

```dockerfile
```

-	Layers:
	-	`sha256:c35575c2bbac68ddb1615f970a8ea5b91b80b162309aa73763693bc47d9e9daf`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 4.2 MB (4215248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5cad799d6f740a31955a3760590f73309e4d2879e32da05907813655385ac3`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 13.7 KB (13678 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:a76163b14df3412f9fea6b62101c8a3b3d81de779033ed78e753808b5d54691f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d280fa1db207ab1f86834891883d03e8cb9a15474e5d1b0a8e770440cb2201af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81eb6eaaa2db2f8610ccccd6bc1ba567a8f98b64e095fcaa6ba4dd344f99536`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 10.7 MB (10672362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e86184655aca75d86e8a7877fdb2ec9818923ae12e4ba8c8b6b6db64c0e816`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011c068dbed62dd0e7dca412001239f4d7843c04a22269387f161efac14a4e88`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3508b221dc7ad79957c24ad801f8116269b56190b332f04297e3cd58dbdaf239`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 104.1 KB (104134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6278e610ae8ff4f4069e330c959564104dc879c91f2848a3203547845a068740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0046e2e2e4e9ca91514877d1878562a0cd2e29ddd3d5ef59c27a594b325407`

```dockerfile
```

-	Layers:
	-	`sha256:a6e587ad4166f1ecbfdcb34af2443207d1ffb170307bc4619c3a3db05fd5eab3`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 4.2 MB (4212312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa44bf7d0ef4d049cb38b1d14a0405ee8ee349b6b306e47e1b41fc87ce50915`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 13.4 KB (13425 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:7412290695fb4975abe69bde2abfe56e4ef2b422581f60e4c23122766eb3eef5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a40a455e224e378e6c1ba53e49e80d54529f414ccade581cfdb22793781a5cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61070980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef3d76eacecaf0406c82147a394f54794bf4b700f87d152f5020f712da7a5a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f728c2a274152156adae707afd4c7acff7c3cda876d9f29783c874f87c6aa6d3`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 10.3 MB (10307527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314584b23585792203e4a076400bf81f382d644fcb124e3f4ddf4f81afd551b8`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d822bf0f40147d3330203054210369cf3c5dc3a52c16fc1726e82cfc84284616`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da49aa44fbf6acccb4122c994c67ba81c4a6140f03fb144120bd4253a6780cf`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf89c183f941a66ae90604d83e0ac30aee3197b51ab7e74b363a9999914ee77`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ee6ec2e169249fac98fe23df8d0c1eb252e19df7a7ff3b364d8f3f4fbee094e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf9ffef60121c1ac26664f0439c64670b139b6aeaa957af6334c6f9a79f540f`

```dockerfile
```

-	Layers:
	-	`sha256:1832a42524e696b8e542d88ce1fce9959d42d5e7148a1e06a6c337d4a32540bf`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 4.2 MB (4215102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3614377f3b59450f10c8124c7df977ab039c86c05526e2f7ad95c529a4408f`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 15.4 KB (15433 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c88056a47dc5318043679e57676a23e583df1c718e7983a3b57d31f2e4a093f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59872893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024422e05673ba9016411a9080801a2e926b1283e23186b85469a2b625cf8fbb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd9c59acf204c0d81aff8b7e5da56cc3b76c258fa40d482df9e225cd533596`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 10.3 MB (10313209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cc3300b9846c0e9c7dba482c8c981db848d2eeb56f74c62c65a1debee89e29`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60fd2e75c963791cd3b0929bb3c01c7671ec64f140a3ac83cf1212b4a5b5c4b`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e238e2f4604a403218d3037f6bf35bb3d8d7e071f2dba1a6a88fbe012a1abb1`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 104.2 KB (104250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b85b4e240f80a499a71af86f86bb3a75a46bc47a84a841fdc6cec3b6fb75e4`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60e9beea383de0d520744c632f02662cfb2ea54b541ff3608e4cd6c258ed5daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c823c4fb2948cba2750dda96dbc5bd93d2fd769c9b0aa6c4fb1a87091d8bfe5`

```dockerfile
```

-	Layers:
	-	`sha256:c502212cb34e8b56ae978bc283f847c2d4d457e1f762d554516348d43afbceef`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 4.2 MB (4215284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78431dc615efd921d0ece65d407291dd8c193f19e87e47543b1a2e182523b064`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 15.7 KB (15713 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:57f983e7f9f86acdfddb4d3f06279856dacc0db529dcdf3e7d9cfb75d9995c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8dd97f0a56db69579af7f6cb93a852bb53bc5231bd3d65066ca16225070f88`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e86b3dc0faa0645c9c93e23b272579368c4be6a1dfa842fdaa79acf07923271`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 10.7 MB (10672417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763ff0412f0e24675a3c0094d231bb5d4e8e02027bf12f3b704a8d7af2450df`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d3a22329274128cc292bb8b17fbfa44e331807b81e2d773c7cb72f3eaa412d`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34750594939305441facfa5a6eefcd1cb932fb637d427e856e2d4fd8a40cb69`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 104.1 KB (104132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbb066394ae147de6d5ae62491985cfc67be643195f5d6cec344e2c6a9bfd20`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c6a7a766039d129b00d2cb80d7d5d41439aaf354b23075d1e7326ce2f8c304c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1dc63b452c68125e8b1db6aac43ab686f120d7c6ac5815663e27bcdb864f93`

```dockerfile
```

-	Layers:
	-	`sha256:e2d563e3f4699cb1c3477375f76ac57e49733df27f30dc7ea01c8cbf4dd17229`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 4.2 MB (4212348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c16586447c4ba568049064444e9027010f79435b5b909d83ee830c6561b3bb`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 15.5 KB (15457 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:35696f693b6ef96260422b9091c766188a7983d82eb58b1eb04f6bd7b58ce84a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:8436872dff585d3f4fd9ba47de2a0c07d2c9601ea7683cd5d98156073fb3e61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69c59f4bc1665f4125a9108a35f53ff8fd3c0f0db4bea3086ff4c0cb4117d2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aadfed4b17ce30257b1e83849176e62dda5f82aa6e95a8478f76eec14d065d`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 5.4 MB (5360246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ad67a268cae8111d8fe8b7df873538bdf930ee3af83bddeae455228cf4b12a`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d727c6072b0d91a97e0e503910ae3a3875e0eb0f330dad37430449c5d538f6f1`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a1cbd18209d18420e1b340bb0af4bf1810b5523ee10e459833effca52500e`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 105.2 KB (105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af0c65cce1965a1a6b3c2b2975e967c195bd2eba5a033dfefc365029b377dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45da22baf7d2b89589eaf2d5f3e761d81c297d1c7034615e130e5031d2b182c1`

```dockerfile
```

-	Layers:
	-	`sha256:b358a4f2b71ae1fc1b775755876a2990c2755cb455ca4551f7204050603fd0fb`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 2.0 MB (1977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:543ad7176c91bae6840122d5e6913e1dabd6c77bfd53962ded0190dfc7eaffd4`  
		Last Modified: Wed, 05 Jun 2024 02:20:28 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0f5b1443b574b5ace2b0987cd1977e8210613ba725ed472573cfbe9c5cfe23ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b273064c8a6c81f5cacbef5005cb8661311bf23c477bd55a7c401646da2abe1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:284dd670c2b0916e7375fa296cc94b380cd5d78ea887f00690b52596df26c8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c3a8fbbf35052ef29f84d07daf978d8d877ce6f9fcacb449acf1ffd0144aba`

```dockerfile
```

-	Layers:
	-	`sha256:813766013ab606a80d4443383a3397da61d8900db25f42772d29d6cf04b2bce7`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 2.0 MB (1978184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1bf415abcaaa1e6c9340665180fe32490ac956e54c13e38d2b031ff973533bb`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:69eea5eee69951a81433ff44e3a76d25374f43b5ede7e2be7991cafbb9ab8480
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2614cd1459a929df672f30c4de3ff5f4f423b10d0204439ea00b153fb35a4ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ba3c03399056b312baca33d2bef793afd92675c192b7d90af7db16bd0fe08b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab32168f62b0a56e9d1738ba27dd0e7b6b3b7c2e892a19527bf5495039d950`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 5.4 MB (5360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c5f6a989efa6cf7d58ae9018a40243e81a4b1bdcb7a242de74e77d92f945db`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfefe3835ca69f4b947ebba8fa742346a61ebab4361ca98d383e7ba7489fb004`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdc23cea86c9950d617b60a8e9e162dfa93280986c8e4ea3c9efc6450810bbd`  
		Last Modified: Wed, 05 Jun 2024 02:20:11 GMT  
		Size: 105.2 KB (105229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026d40b80d1375c0c978e08b9ee3768e5635a011dcf98d75ec8a728fea6461cb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8052d782c0e8c3437bea67acf4b2a22d79a7dffa5297317f4776bdc773d0701a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1993579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b545e88e893b1df4e4133705e4b3af666a09fa688c52562b97322c9c6d4c0099`

```dockerfile
```

-	Layers:
	-	`sha256:fa21014e2151b093cd2b0f181163b6be1985c8371a5cc2d7e52e4613433f80bb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 2.0 MB (1977992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15b3763a1a7a0714189ffe6046baae58c42e3ed9f083352e41a11ca77cd14e5`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 15.6 KB (15587 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a765833d6e8524c6babfed520f054ff84a6adea03bbc27c95574cb07aa8fa14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10519d9344ce22cf8b6dffbe4a09a105acf140f518107098b2c66a242582141f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5151156e9cc1c424bbecfc412c4effcbd14bdcecf53693bab61b678ae9ed5fd9`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d450bd9f532b807f700d228fe37fceb706c7960f3b87d06090658a57978a3d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1994083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e25fe54f10b92c153df2cdadaa8eb3efa03f0dee4e099174db24e3ac65946`

```dockerfile
```

-	Layers:
	-	`sha256:ed1c978d1833cda54dd5250213c0833f524702bb98f9f00a81505d89c5d1b173`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 2.0 MB (1978220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b63cad0b9de5d2bb91de6e7fb6616926fabbf2094cb6ffb471176092d3df97e`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 15.9 KB (15863 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:623b758391fb029c0195fce359139e6ee027655959e76d09fb4ca2e26ffb941f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:62b21ea23ab0099bb7bb3c5dff41f062348f26f984ce63d7adbdce9523debbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d480dfd32cd52adab70bf29d18e316284e516732cd7b64ca8fa74057e78b2bf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13680b52a20c7f7235a12148a3b749ac0b8059a27ccf65a67280b22ab004496`  
		Last Modified: Wed, 05 Jun 2024 02:20:23 GMT  
		Size: 3.6 MB (3622659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9c4675fb06f3f04ba34fc069e9b8352212d06376d2db5919df67d4861e337`  
		Last Modified: Wed, 05 Jun 2024 02:20:22 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fe517f5124a0cd3234b7e232a0eb9bf389b9b8927d1108f376ba18f4a602f3`  
		Last Modified: Wed, 05 Jun 2024 02:20:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5c2f84665972fd9fb9573b2bc00b57c4d6633e031d81eca30d1f1a26e9c4a2`  
		Last Modified: Wed, 05 Jun 2024 02:20:23 GMT  
		Size: 110.1 KB (110101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b4eed60b439ab7b3dd6a8b8b389e08f83980039978671105075d770d2e36f4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94a87947aadbdb67abbf4192622756c526f7bcd4b104de43c0ae0302f13f532`

```dockerfile
```

-	Layers:
	-	`sha256:47a512237c86f29a05d8cd78319ca62f3d23f9959e965f73984dc89c544cfc9c`  
		Last Modified: Wed, 05 Jun 2024 02:20:23 GMT  
		Size: 2.0 MB (2015658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b7dcb1333f9cb8c4f4713875a80365a39445f7452398c4a29dcfca3d6e82bd`  
		Last Modified: Wed, 05 Jun 2024 02:20:22 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:182965a2a88e752d9531ab95095ea3f137ec86496b97f9e82a9df5c92f2338bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31070904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0020b4b6b75f3fda2b2fd11190ea6b59ae189b71d7fcd254bb3e3df2d195a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fee3ef976957c41d04767884cb43799b96170dc7f90b007a26b81ae7b51c1b`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 3.6 MB (3595512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad45b1472436df983642ff6f6d821159f3cd9284d480a5e549b8c52f96c74c6`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154dd0239ee03ec9e4d04dc3e50288d571e148ebe8a49b6b24e5b4dc41e65926`  
		Last Modified: Wed, 05 Jun 2024 16:36:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e65cd6fdcff0083c9d0e5d5a4702ce5a2ae4964d6c7640ff281a2687c2a4f4`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 111.6 KB (111617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3daf4feaf8b1af264759adfc71c17d64177646bcff852e4c561c28ee3ab4296b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a01233855c07d4d99141d81865bfe4168def1876fa3a1ef37be11dbdf4b2281`

```dockerfile
```

-	Layers:
	-	`sha256:b5128b7a8311295bf17b1da5ff28149668958c562a0f3982ea7b363c9a9ee90e`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 2.0 MB (2015917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09216cc84b65a36876b54e5c68b7ad1aafcc4a002ac17e4e904429aae09512e6`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:d636f78afb87861ff221bee82f72a33a40c1a079f2aa2c684d744e545637ec7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e7abef41958dd7dee0bae8bdc415b40824f92a6d4ec132396486116992b7b681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d23bccb9a816ef20f98f4d9b63173c11a283b12820991f11f7115d85a7c5d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb43413ee829cc75026067ac5d778cafafb77917da12b5dec6e0a6447a7f8686`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 3.6 MB (3622639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef34d71f1c9345b38a1e54a91fceb7aeda6c3c0467ea3f9b83f5beee6bb28afc`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7e8f5f4c30e732d2e22abb93e18bdc0a94b22fa7c33725f6be4f02110ed64`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4507960307afaaeb03a72f97620824aecd40f2cb9e3c423b414a6cd862a7594`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 110.1 KB (110053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111b9057540b39a6b4ed07fd7e9a6a01509e0ba6521ca9b08b2d1d4c91393069`  
		Last Modified: Wed, 05 Jun 2024 02:20:48 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:00e298aa5a60fb2c6ad6308605ac14e42df08b2449ddb03dd6710c33e30104e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b82f8e8554ab34024a8fb1f2871a2f17e9c69ae0cc5729ed7de770b5081321`

```dockerfile
```

-	Layers:
	-	`sha256:b22d44f8413e29ed450460bf31f184eb25021178d345ba4ce95411b57fd319bc`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 2.0 MB (2015694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583e8e5db7add610c022447326ac812279e0a609b548dac8e3235070b6543a27`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 15.6 KB (15587 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:896ef60abff1e40bcf2965d6d8df5d2a195851495349d25d494954c7b5bfa98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31071166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e612430921515a459d27a9426506ed0d62cc61fea28c924deae22abab84842`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fee3ef976957c41d04767884cb43799b96170dc7f90b007a26b81ae7b51c1b`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 3.6 MB (3595512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad45b1472436df983642ff6f6d821159f3cd9284d480a5e549b8c52f96c74c6`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154dd0239ee03ec9e4d04dc3e50288d571e148ebe8a49b6b24e5b4dc41e65926`  
		Last Modified: Wed, 05 Jun 2024 16:36:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e65cd6fdcff0083c9d0e5d5a4702ce5a2ae4964d6c7640ff281a2687c2a4f4`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 111.6 KB (111617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f09225e0cb5ea6674844916153d839c9066d4cd5ee893857fd71e33171f6f2`  
		Last Modified: Wed, 05 Jun 2024 16:37:18 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d1484488cfba61c7d8385fc94eafc909180fc2034587ef9a5ebb39ad12c50734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82076d7d5b1183a967bac10516c4364d113d0d845b3ec8566bab1e283eac3f62`

```dockerfile
```

-	Layers:
	-	`sha256:e1492c9297abfe99ebf8e9883509b49605e6e5b7b60818a7b896d5a6b0c63122`  
		Last Modified: Wed, 05 Jun 2024 16:37:18 GMT  
		Size: 2.0 MB (2015953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71ac22ae1be19aebdfdd740c17c6b8f039dc72dba7a8ce1b8f1f7d53b62e8f9`  
		Last Modified: Wed, 05 Jun 2024 16:37:18 GMT  
		Size: 15.9 KB (15864 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:f6e3e55fff88d76cefd14b3174f8f430397f89f8b3af15370d60ceeb6e7f4d29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:af0d2b93bcb42fd81d4aaef410dd4472adacabed56158f921f2f734107d574d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66307144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c371f8b59748f5cee78657d02842b010304a574eb20a5eff38c2269418a34121`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38696ace0e231833c5350b1141146fa871838e0f66f1f7490af4c5402b3eeac7`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 11.1 MB (11104999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c87467765b5a37d61c04f087fa4e848e9329b99d686598d39b5116fa5232719`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8100950653fc9224fce0d1d05eaee9e8cefed042e6de64d30b5731ad280ed05`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4314a0c2f43354c94fbb29548509614fcfb953500f3a32fb633f563d0bfdbe`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 100.8 KB (100757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7b3feb473978c56e0e6402c12cea3185c3dc1256496c90b321606e70c55bb5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2936220a96affe48eca18b1cb6f18d0540bf04b0197243276f9cc4e3def74a4`

```dockerfile
```

-	Layers:
	-	`sha256:290468390b78978c5f76889d14246e2e0fa803ac3deab6ea9643860a0c957a14`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 4.2 MB (4199042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85226dba484b356b8e0c43298c973e5e51c14f40e515bb3f8881936c18b1147`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 13.7 KB (13737 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bfda43b28611976c87ccbadb7e5ea0d877660f7252cf42e2abfc8b68e01ebd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8aee6e5a024afaa1fa4cae9d2599683aa2748e22f795ff4a85beb6ef4d0fbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1483c42dcb365aa70f1ee657cb621d71108a07cb14e7da7c0af1670b1d3dc`  
		Last Modified: Fri, 31 May 2024 14:43:25 GMT  
		Size: 11.1 MB (11105807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bdea9458a37f5e1417a645e4803ce863ee56f1bb909725f8a36979925dae88`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a358d18ad53e6c2f3626a6322cc6c11247f800ae4b985a091f6495eba713135b`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf2eb23fc03995a0b59c27e2f55adfc7906966f111740c748bb549fa4bda575`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 100.7 KB (100692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eaebc4698a949504bcb6c45f41ad30d9ff6b662b4686d2bcca1e2a0a21854bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bceafa6b6b5c0bf69ae9243a8a5b812fb7bcfa07e0e9bcaa12c82780278c87`

```dockerfile
```

-	Layers:
	-	`sha256:59c311a36ac8eb21fa89848f79a995fd2cb7799ed68a779ebb56a20a681b4633`  
		Last Modified: Fri, 31 May 2024 14:43:25 GMT  
		Size: 4.2 MB (4198659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae78608efcc11c0de2680a9c0c77c9a21def4c0676b81770ad20443d329fd3c`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:cabcf9350018fb62481d82da2d505e7435e413b523ffebfcc9b7d080ca3248d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88df1df83a11719da37c9375a2ec92d392548f66178495fbaa15ac872d52ce6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36508bc53306c02a9ef12049a2feecd1ebe42c6a54a9832472dc4a2dcf9f2c08`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 11.5 MB (11500070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650c52e044f44142bd08d3c99a7d5bb60aece0e021e835404c71f0536348cac7`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a9f7821bb8e6b0e0776e2b828f75a95c812314e6cb6a1c256c944d6ce720bd`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8868307403b220244baee51b838b348d00e384e65031382e9c786b28a9ec9f`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 100.6 KB (100649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea9a8508876015fc24d1696a07b00dee5dd053bf937c9f4480fd9c8c2b61ec11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4209252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b9051a1b5507153426df6c9faf52f91ef695a1e2b336bd9ba344c819261aae`

```dockerfile
```

-	Layers:
	-	`sha256:920dffb7e2a35971c60e1b62223af049b0b7015216e62ffd5b83c0c380c72d06`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 4.2 MB (4195497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082631cbc44059d106b213d5b38760209d1d120834d9b001cdb35972f003c889`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:7b10171b71a341f81d2db6867a5d45c17232a457064c0762e7aebdda3b94ad2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:9d6b76d38812539161f59c893466f5b49a8fd9591f8d2f2a01015142b1b7b216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60049164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9e6ae8e755fa691be543e87a19ceaaf5730a42a8b17045af0d7844f85e3ea4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b719a38bf4aed68db29b56d561e793f8400c5edee1406cefdc25ea0c72ae7`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 7.3 MB (7313247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a778cadd45e115aab99728a495443d9a0e22db2b4cac341924a9d85071fb5`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73059de92601721fef9ac2c3019771fb96130f0ef7280cc538253280cdf1ba92`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c97c37c295b1b834c6ff803661093e3f42e5e01f6c8a476778c58cfb56657`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 91.0 KB (91039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:388a04f898471e845839e7d41f20795d49ce13fa7087377c1fcd80379d946168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de95620c07d5b4bd87bc12d9b2921d0d89a03b37227a84549003b96bd538f2c2`

```dockerfile
```

-	Layers:
	-	`sha256:a4daf7efa1f24d0026d214c5a47303591dc8a26d4667e0022b33447e0bcbb444`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 3.6 MB (3592159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca62554e92aa67d490ef6f1f7c63bcff795065618587426f22dc4754279c1ab`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 13.3 KB (13348 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0bc06edf842750d1b8f488ba4dd6ce12a30c56db39f5770556bd2ef64474a267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60321222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6326bfb52a658f0caa666254da500a6cadce9719e0c53ec40a929200564b0269`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:65d77d3f6289af1318c696652b600f022ddbc3a1daaf105602e348ad91d2c41c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66334a1d5d0f0597e9440b0db265b333533e2fce7f5bb2d1fba09c85ef6cd21d`  
		Last Modified: Tue, 14 May 2024 00:45:15 GMT  
		Size: 52.9 MB (52930287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bdbf9908e45530061175939d20c6ded00e858fc7838427d8713e0ed59e84ea`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 7.3 MB (7297335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0922009db60c6f3c98281eecdef09a0c5ca68b58d2bf585b8ebbef25c57d30f`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26863f97217b3df00be0b9bbb64308b763fe60c3bcf24a1cfc8c16428395f03c`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bb75772d75f5c87c177220dd50d76572d354d75f97b9186a272610c1c9fa27`  
		Last Modified: Fri, 31 May 2024 14:45:21 GMT  
		Size: 91.6 KB (91620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bf6cd02827b2dd05aeb0613d98a66272fc567af92724bfccd95a38c27cf27ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cac57f1a7aa1101336c904343c777b772e3e3c16c662ea2deb1242cf1fded1`

```dockerfile
```

-	Layers:
	-	`sha256:1acaf9ef26e92ee887ebe48465d6d949355c6b19ad6a9c7529d7e63625abc3f8`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 3.6 MB (3593200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ea3f17838a54ab388d0a3af2242e54f2977a570e2fb3d32eaa408a183491f2`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 13.6 KB (13623 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:97b5f62de5f63780c6fb60c18fac80a4ae8cbcf56397376e609f8a665bd42094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59947484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df55d8fa11cb174de39000a2295c9dbf246bdfe3cb88605507a5506f7f2c7c05`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c7b81abba8966f408c068710549216ceee2b9d423c6a9411b04994eea156d6`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 6.6 MB (6551754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d3739f5e8659580229543579dfafaa8a624b3f230cc3c918f717afff60b7fe`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62789b7063d2d62b9591fffcf6f696ee77c7bde371b15b61b45647cc1c4139ec`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f020a648d73b4c99abcc87718351afc13962b285a67fb1149a89fbdd5789e6cd`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 89.5 KB (89451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c3a877c1de721606d524b8aaafcbee6ddbc5e18809486d6563c15c9eba88b2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaf78d03b9d7b700c0ec38992b872c759e77ea48b08ad2e0688433a71435d0e`

```dockerfile
```

-	Layers:
	-	`sha256:8e15cf37b593768d02d1e5e5ae9e91ac87a51f539dae42d421dcaf98d639257f`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 3.5 MB (3547113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29033c721523198453ef2a66dea5e3d3d2b8efe44b0c1bc7ea31d1db80dffb0c`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:1f347a1caba92ee7d0c0480f7c658da4c3fcc562cafcfef560129e81cc67bf61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5238cfe08865e6d220ee2e441d2a11b4dd3876aebfe8934d3ae847a062d39a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60049648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5fd9cf60415cc4d6a2e41b0ecb799b45050a2b735d4684059251269f304fcb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e371f96dcd488dcca9b548ef17888a30c45ce4185fb64de3935db57cdd0f075e`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 7.3 MB (7313276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663cae23bb39c60559275df0410ebcaacba26c9c421222281f939ee17f70d9a2`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7d3a1037ce374991daccf4e28eea64df1abe8c4db782678a283235875aa22`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962fd9f4dfaf26a175b8d9be95478724907ec51e80476cb047611792164825e1`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 91.1 KB (91096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a48833da318e61e1c29dc561a729bbdb2297e59817a9dce4d792c1a03cf48dc`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3932fe7a10c4ef043d4b16430814bb2f7593eb20a6a5f9e64f1a2ce9ca2961e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300a524f0ae3b5ca164f2d6494e49f4b28b5c83b20dc6b0e9e4e0b63d64a34b2`

```dockerfile
```

-	Layers:
	-	`sha256:d3daceb491c6e32ec20d264ba220ecf8d90a01111f4e1ef6b3395d3f0ab10f05`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 3.6 MB (3592195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce8579bbeb70277e1ebec780493f9a3677213b182e3859b373d3843ac4fa3485`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 15.4 KB (15380 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5fbf2db17bc959f10539122428b5eb7ce8872b4b81fdb911808dc8529e531f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60321617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce15232a20027fee120dde8e91fc9e494c52ffab824dcb035408941efdc5af8a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:65d77d3f6289af1318c696652b600f022ddbc3a1daaf105602e348ad91d2c41c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:66334a1d5d0f0597e9440b0db265b333533e2fce7f5bb2d1fba09c85ef6cd21d`  
		Last Modified: Tue, 14 May 2024 00:45:15 GMT  
		Size: 52.9 MB (52930287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bdbf9908e45530061175939d20c6ded00e858fc7838427d8713e0ed59e84ea`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 7.3 MB (7297335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0922009db60c6f3c98281eecdef09a0c5ca68b58d2bf585b8ebbef25c57d30f`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26863f97217b3df00be0b9bbb64308b763fe60c3bcf24a1cfc8c16428395f03c`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bb75772d75f5c87c177220dd50d76572d354d75f97b9186a272610c1c9fa27`  
		Last Modified: Fri, 31 May 2024 14:45:21 GMT  
		Size: 91.6 KB (91620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bd06c55918dfbf55eff1a7418f35b45e8b2fba30f5de58bd55be197b91b1a9`  
		Last Modified: Fri, 31 May 2024 14:45:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7b07ec51360998e4ccd0e8f52eaaa76f549978b314ee67ee743906d45083fe88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1465a6b9bc9754c12336dddafb4bfb733a2e0935d11482c115926a209ddc9e9`

```dockerfile
```

-	Layers:
	-	`sha256:fa652cbef2bde281071916747098dad578170e9376e8b7930103ef0e02e84f7f`  
		Last Modified: Fri, 31 May 2024 14:45:42 GMT  
		Size: 3.6 MB (3593236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db4cfe024664b5c03389ac7171d4573621a698e43b06e77849f945768715797`  
		Last Modified: Fri, 31 May 2024 14:45:41 GMT  
		Size: 15.7 KB (15653 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:d4bdf1159b48c2ecabc30bce4f3ea3ae73a8a2325c1326d2fbe45e7939f168d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59947750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b40502da47f32b5a185493da2779d36e20e7f4c4747590909e51d36de4b97d6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21de92121739d4fa9675f02b90861a34f4574dc9e316bb0802285d92e4ac9b60`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 6.6 MB (6551627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96fff31007030f5b9515a1a6aacbd32612b1d07ff9f3c78c1015183eb77672`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62789b7063d2d62b9591fffcf6f696ee77c7bde371b15b61b45647cc1c4139ec`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731f1ad43b355ce70365191a317496e08b26eb26184ca25bb2fccc05ede567bd`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 89.4 KB (89448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9d9e3bebf592f069cd34952600f4fdab904969c316ff205ecbec5fd7e4d7b8`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b8023242e636bf70cbbc9a46cfa11df011120a169a23c971e7b816b8727c27b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a40003dba26a551eb5404e012d47a3314c68829113f7442897d4a58fd15670`

```dockerfile
```

-	Layers:
	-	`sha256:9116b10c7dc54220fedacf31400461ce9e8ecc63e2359d29a7cfdda20ae5bdc3`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 3.5 MB (3547149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e85ecd426065713204ad4fcd588935afb2e9b8a8a114098388115cc0ff4755f`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:157ca5d3647d5f702e04e110d4132355e9d04c74c3f170d82768b02fef2c91f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:020104f3971254f7e7ecda9d7906735733e55360f142eb78dc36c229471ebbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61070627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc56267455d2457752fbd7f8ef9bd1351f76f73d7f36ca0755faf9bdea833d8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723d87c39a56b2dd8a62649501bf04ba3a687a53896c94468000a095aaed760c`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 10.3 MB (10307517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1e2e602b28270d610b56d107afb7c3d4e767a70a6b91da844db452b91eb293`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d822bf0f40147d3330203054210369cf3c5dc3a52c16fc1726e82cfc84284616`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222234ed4691c00c09d259495a67f1e32ba942cd3f8c73cfff42245ad61d1327`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 104.2 KB (104212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100` - unknown; unknown

```console
$ docker pull neurodebian@sha256:69131987bd6fe23325f21f49abca3952217bf6bb8340de090f82c2c03bbeb54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903b524f67be676e0a9620c5cfcaf385fb91379bd7be09e955dd7462a04a1ae0`

```dockerfile
```

-	Layers:
	-	`sha256:f1656c8c3a6eaa5e531f96856c15c839a51124b4c946824bb634826eae237680`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 4.2 MB (4215066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8cec8865692dfd27d4aa16a39200a8bcc72abbd0269f2d814dd2579901ab2f9`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 13.4 KB (13399 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd100` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:176ea7c06f6ea8f6ba781055db94356ee8143d00476e2f10e2e0afd2ff1535c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59872536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03153f64313411fe1da52555de68c42bc9ce00711b014e5fcc7da41d4f2415e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd9c59acf204c0d81aff8b7e5da56cc3b76c258fa40d482df9e225cd533596`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 10.3 MB (10313209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cc3300b9846c0e9c7dba482c8c981db848d2eeb56f74c62c65a1debee89e29`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60fd2e75c963791cd3b0929bb3c01c7671ec64f140a3ac83cf1212b4a5b5c4b`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e238e2f4604a403218d3037f6bf35bb3d8d7e071f2dba1a6a88fbe012a1abb1`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 104.2 KB (104250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100` - unknown; unknown

```console
$ docker pull neurodebian@sha256:11acc36e9dc4881113c767f319b6fa4d3a7951225685756f733dbabcfce3c12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148c1afddd6bfd55467d4fe9da6aff8cdba3fbb67af8bc72b7f4db65583f8219`

```dockerfile
```

-	Layers:
	-	`sha256:c35575c2bbac68ddb1615f970a8ea5b91b80b162309aa73763693bc47d9e9daf`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 4.2 MB (4215248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5cad799d6f740a31955a3760590f73309e4d2879e32da05907813655385ac3`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 13.7 KB (13678 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd100` - linux; 386

```console
$ docker pull neurodebian@sha256:a76163b14df3412f9fea6b62101c8a3b3d81de779033ed78e753808b5d54691f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d280fa1db207ab1f86834891883d03e8cb9a15474e5d1b0a8e770440cb2201af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81eb6eaaa2db2f8610ccccd6bc1ba567a8f98b64e095fcaa6ba4dd344f99536`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 10.7 MB (10672362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e86184655aca75d86e8a7877fdb2ec9818923ae12e4ba8c8b6b6db64c0e816`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011c068dbed62dd0e7dca412001239f4d7843c04a22269387f161efac14a4e88`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3508b221dc7ad79957c24ad801f8116269b56190b332f04297e3cd58dbdaf239`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 104.1 KB (104134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6278e610ae8ff4f4069e330c959564104dc879c91f2848a3203547845a068740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0046e2e2e4e9ca91514877d1878562a0cd2e29ddd3d5ef59c27a594b325407`

```dockerfile
```

-	Layers:
	-	`sha256:a6e587ad4166f1ecbfdcb34af2443207d1ffb170307bc4619c3a3db05fd5eab3`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 4.2 MB (4212312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa44bf7d0ef4d049cb38b1d14a0405ee8ee349b6b306e47e1b41fc87ce50915`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 13.4 KB (13425 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:7412290695fb4975abe69bde2abfe56e4ef2b422581f60e4c23122766eb3eef5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a40a455e224e378e6c1ba53e49e80d54529f414ccade581cfdb22793781a5cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61070980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef3d76eacecaf0406c82147a394f54794bf4b700f87d152f5020f712da7a5a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f728c2a274152156adae707afd4c7acff7c3cda876d9f29783c874f87c6aa6d3`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 10.3 MB (10307527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314584b23585792203e4a076400bf81f382d644fcb124e3f4ddf4f81afd551b8`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d822bf0f40147d3330203054210369cf3c5dc3a52c16fc1726e82cfc84284616`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da49aa44fbf6acccb4122c994c67ba81c4a6140f03fb144120bd4253a6780cf`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 104.2 KB (104204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf89c183f941a66ae90604d83e0ac30aee3197b51ab7e74b363a9999914ee77`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ee6ec2e169249fac98fe23df8d0c1eb252e19df7a7ff3b364d8f3f4fbee094e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf9ffef60121c1ac26664f0439c64670b139b6aeaa957af6334c6f9a79f540f`

```dockerfile
```

-	Layers:
	-	`sha256:1832a42524e696b8e542d88ce1fce9959d42d5e7148a1e06a6c337d4a32540bf`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 4.2 MB (4215102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3614377f3b59450f10c8124c7df977ab039c86c05526e2f7ad95c529a4408f`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 15.4 KB (15433 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd100-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c88056a47dc5318043679e57676a23e583df1c718e7983a3b57d31f2e4a093f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59872893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024422e05673ba9016411a9080801a2e926b1283e23186b85469a2b625cf8fbb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd9c59acf204c0d81aff8b7e5da56cc3b76c258fa40d482df9e225cd533596`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 10.3 MB (10313209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cc3300b9846c0e9c7dba482c8c981db848d2eeb56f74c62c65a1debee89e29`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60fd2e75c963791cd3b0929bb3c01c7671ec64f140a3ac83cf1212b4a5b5c4b`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e238e2f4604a403218d3037f6bf35bb3d8d7e071f2dba1a6a88fbe012a1abb1`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 104.2 KB (104250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b85b4e240f80a499a71af86f86bb3a75a46bc47a84a841fdc6cec3b6fb75e4`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60e9beea383de0d520744c632f02662cfb2ea54b541ff3608e4cd6c258ed5daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4230997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c823c4fb2948cba2750dda96dbc5bd93d2fd769c9b0aa6c4fb1a87091d8bfe5`

```dockerfile
```

-	Layers:
	-	`sha256:c502212cb34e8b56ae978bc283f847c2d4d457e1f762d554516348d43afbceef`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 4.2 MB (4215284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78431dc615efd921d0ece65d407291dd8c193f19e87e47543b1a2e182523b064`  
		Last Modified: Fri, 31 May 2024 14:42:51 GMT  
		Size: 15.7 KB (15713 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd100-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:57f983e7f9f86acdfddb4d3f06279856dacc0db529dcdf3e7d9cfb75d9995c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8dd97f0a56db69579af7f6cb93a852bb53bc5231bd3d65066ca16225070f88`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e86b3dc0faa0645c9c93e23b272579368c4be6a1dfa842fdaa79acf07923271`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 10.7 MB (10672417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763ff0412f0e24675a3c0094d231bb5d4e8e02027bf12f3b704a8d7af2450df`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d3a22329274128cc292bb8b17fbfa44e331807b81e2d773c7cb72f3eaa412d`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34750594939305441facfa5a6eefcd1cb932fb637d427e856e2d4fd8a40cb69`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 104.1 KB (104132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbb066394ae147de6d5ae62491985cfc67be643195f5d6cec344e2c6a9bfd20`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd100-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c6a7a766039d129b00d2cb80d7d5d41439aaf354b23075d1e7326ce2f8c304c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1dc63b452c68125e8b1db6aac43ab686f120d7c6ac5815663e27bcdb864f93`

```dockerfile
```

-	Layers:
	-	`sha256:e2d563e3f4699cb1c3477375f76ac57e49733df27f30dc7ea01c8cbf4dd17229`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 4.2 MB (4212348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c16586447c4ba568049064444e9027010f79435b5b909d83ee830c6561b3bb`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 15.5 KB (15457 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:f6e3e55fff88d76cefd14b3174f8f430397f89f8b3af15370d60ceeb6e7f4d29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:af0d2b93bcb42fd81d4aaef410dd4472adacabed56158f921f2f734107d574d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66307144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c371f8b59748f5cee78657d02842b010304a574eb20a5eff38c2269418a34121`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38696ace0e231833c5350b1141146fa871838e0f66f1f7490af4c5402b3eeac7`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 11.1 MB (11104999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c87467765b5a37d61c04f087fa4e848e9329b99d686598d39b5116fa5232719`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8100950653fc9224fce0d1d05eaee9e8cefed042e6de64d30b5731ad280ed05`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4314a0c2f43354c94fbb29548509614fcfb953500f3a32fb633f563d0bfdbe`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 100.8 KB (100757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7b3feb473978c56e0e6402c12cea3185c3dc1256496c90b321606e70c55bb5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2936220a96affe48eca18b1cb6f18d0540bf04b0197243276f9cc4e3def74a4`

```dockerfile
```

-	Layers:
	-	`sha256:290468390b78978c5f76889d14246e2e0fa803ac3deab6ea9643860a0c957a14`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 4.2 MB (4199042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85226dba484b356b8e0c43298c973e5e51c14f40e515bb3f8881936c18b1147`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 13.7 KB (13737 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bfda43b28611976c87ccbadb7e5ea0d877660f7252cf42e2abfc8b68e01ebd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8aee6e5a024afaa1fa4cae9d2599683aa2748e22f795ff4a85beb6ef4d0fbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1483c42dcb365aa70f1ee657cb621d71108a07cb14e7da7c0af1670b1d3dc`  
		Last Modified: Fri, 31 May 2024 14:43:25 GMT  
		Size: 11.1 MB (11105807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bdea9458a37f5e1417a645e4803ce863ee56f1bb909725f8a36979925dae88`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a358d18ad53e6c2f3626a6322cc6c11247f800ae4b985a091f6495eba713135b`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf2eb23fc03995a0b59c27e2f55adfc7906966f111740c748bb549fa4bda575`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 100.7 KB (100692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eaebc4698a949504bcb6c45f41ad30d9ff6b662b4686d2bcca1e2a0a21854bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bceafa6b6b5c0bf69ae9243a8a5b812fb7bcfa07e0e9bcaa12c82780278c87`

```dockerfile
```

-	Layers:
	-	`sha256:59c311a36ac8eb21fa89848f79a995fd2cb7799ed68a779ebb56a20a681b4633`  
		Last Modified: Fri, 31 May 2024 14:43:25 GMT  
		Size: 4.2 MB (4198659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae78608efcc11c0de2680a9c0c77c9a21def4c0676b81770ad20443d329fd3c`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:cabcf9350018fb62481d82da2d505e7435e413b523ffebfcc9b7d080ca3248d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88df1df83a11719da37c9375a2ec92d392548f66178495fbaa15ac872d52ce6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36508bc53306c02a9ef12049a2feecd1ebe42c6a54a9832472dc4a2dcf9f2c08`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 11.5 MB (11500070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650c52e044f44142bd08d3c99a7d5bb60aece0e021e835404c71f0536348cac7`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a9f7821bb8e6b0e0776e2b828f75a95c812314e6cb6a1c256c944d6ce720bd`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8868307403b220244baee51b838b348d00e384e65031382e9c786b28a9ec9f`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 100.6 KB (100649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea9a8508876015fc24d1696a07b00dee5dd053bf937c9f4480fd9c8c2b61ec11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4209252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b9051a1b5507153426df6c9faf52f91ef695a1e2b336bd9ba344c819261aae`

```dockerfile
```

-	Layers:
	-	`sha256:920dffb7e2a35971c60e1b62223af049b0b7015216e62ffd5b83c0c380c72d06`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 4.2 MB (4195497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082631cbc44059d106b213d5b38760209d1d120834d9b001cdb35972f003c889`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:388f6c2461bc209a692170f696d1f5ff96615b60c45bc27f86de6f1eef1b9fb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:84219b6ad2c59d4349766f7ea41188ef7fd7f23e797f234aa2fc118476d87a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66307474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00919434e4703f6acd6065bc95f564b675939dc982ac937077fb392e2b545964`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fff6731503f1b1a12f3ec6074982a0a7c9e1faacd14096103760258566582b`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 11.1 MB (11104993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ed83a5d194b8125fc4475a7474d7614f9fa2cdaa8ef76360838fc01af94e79`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87281e9a3b4c0d00588f26599ef01f9cb268f821a34af340cd347f8c79442196`  
		Last Modified: Fri, 31 May 2024 00:56:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52629961e0dfe4a11e23ee3273dfc2941ef9296958ce0433be941e583fd3545`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 100.7 KB (100736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a7775c23e5a426688a89fe8bb88b071c4b67d2c0c5bcfc7762283e0c64a8eb`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f5badf72a6a31f4df91f889b70573094f100208cb79dc40f13ebba462e395f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752e07c04e896d0e9354d9f9aaeea038b337272f1c2970023a1a6c328cfab70`

```dockerfile
```

-	Layers:
	-	`sha256:1c8a56fac5dd5913e2895f29ade5a290d191979513f8716a9f8b6417694c831e`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 4.2 MB (4199082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d009cbb1fc1738caa42c4c5f123155cca5ae8713acd80bac0f8599a98214bb7`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5d1cf82cceda318c0dd41a8a0400d8411edc8a4d51ee0500d5d15b787f48c559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56caf73109cc0abb9aec10f6936d04cff9ecc5e4ed695667363742eb5c0c880`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1483c42dcb365aa70f1ee657cb621d71108a07cb14e7da7c0af1670b1d3dc`  
		Last Modified: Fri, 31 May 2024 14:43:25 GMT  
		Size: 11.1 MB (11105807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bdea9458a37f5e1417a645e4803ce863ee56f1bb909725f8a36979925dae88`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a358d18ad53e6c2f3626a6322cc6c11247f800ae4b985a091f6495eba713135b`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf2eb23fc03995a0b59c27e2f55adfc7906966f111740c748bb549fa4bda575`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 100.7 KB (100692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8729b3ff44329714773e4eb7c4046bcdce6dcd6ddc587ddc086d3594ea516b`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9c183078ed2c49b83568bf2f7c05cf59aa86563317db10e1fd35dfd0c4700705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b2481a942ef60260cd04118ded9798eab96a09d5a9de29130742c9d682bac8`

```dockerfile
```

-	Layers:
	-	`sha256:a8cb3999134b399777bdccdbcfd6a6470c17788e420fd152629355c483c2d10c`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 4.2 MB (4198699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb260b9d6aa6319449c343ab09e6d08a9472f4d08310d1d79af533866fbeed82`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 16.1 KB (16067 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:30c029632c96bf37af9b76eb0393927bcf408d4d4637bddf613a7594b2681b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5864c6def933a6b6dd9adfb7a5ec63fd1f46aed4cd44d9bfd0cbe3d67f45c8c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b13addd2b2a32b9d1ff2ea9286439b5540ef92b6f2a15ae59e20801eaeb8115`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 11.5 MB (11500167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925784d52a7a52e17776422204b33b6f319d5ac291eecaed873d7c75d0bf7b5e`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc25404734dead4fcf99099c0b8c4c255e177881c3cf9e4bd15eecdda5bbfeb`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77175288a751964832d472ca502af30d298ab6d18b500e39100c7e2cf1941a1e`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 100.7 KB (100656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403eee5dd3ac973d264d6caf142749476a40597c843100f860fd812bbdd7152`  
		Last Modified: Thu, 13 Jun 2024 01:59:16 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20b1a751fa916af4b95b9306d65f00cc6ede2b46bebc04dd23cc8fd44391f864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bf79df5b568b2fef0e797dc3f58e562b7992622978ab8ae0de582edd25ac64`

```dockerfile
```

-	Layers:
	-	`sha256:5b95beda90bc46a2b778e530d4afd832492d8e6d2ba670872dd2bd272173e02f`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 4.2 MB (4195537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42daf680929d419028ac29504c6aa3762fea17ac4478e351fac146d840b2c94`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:72e661f83c596638a0c5504858cf56d93843a60aa19939a3ae08699c9098c660
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:8003ddd6f73b7806bc9583ea35d61132dc3378a3b194e0194fad7d3611cb95d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60937750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab80b10beb2a161f42eceb87ee4ba0552673f0c26475cd6eb2f527b436ec3da`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d0d5ec172ba144071ed0223437f3e4b990d14a4ac73b3f8aa119fdec79b9d2`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 11.3 MB (11266570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31940436a11ab29fc862e2d14d020075964dcb59f967bff291d857751bd4d197`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6de3ad8d62b9a7799615ee74064490747e19dfcf3c526742a4e60bac1397b6`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9baa1fb88a8638cd71a6802afce4c4b8e3980ba78a41930dab72ae419205b7`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 92.8 KB (92801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0aef42c6e0933296b5b46229b5757715801e8e0cbfc579d6bb261a5900300dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f8dc494e821e0ec0217ed94cb1b13b95699d0d150843aea5001b45df309e4d`

```dockerfile
```

-	Layers:
	-	`sha256:257120a633cceccddc68b5f94e49b59497b162ca95753b43f3396da277ab65f8`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 3.9 MB (3901743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c08d4dbe78cc309275b9c9eec0dfc9bd127c7b5d47601255c335c2ae6b2757a2`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 13.4 KB (13428 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6213e2c292c45b49cca98fe498a6808f2700584a9628e3a5624664d9840b87ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60940537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6100f105e85e080929e093c60771b4ca4ea252a385959b9b340af469a157696b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9782ebad61654b7a2473c30e527f7a02ef0ff05bbeecddfa2c2a63f5e2e99048`  
		Last Modified: Fri, 31 May 2024 14:44:20 GMT  
		Size: 11.2 MB (11232082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ee0a093ea753330fd619da92cd9d8620723145c8a836f8b74d64edf92a5d14`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e17f23f6fb69d4dea07617d31ead77946fcac635bc98263d0e0edfd62d3a4`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b77a1d67cd06ab552ba0ded4026133eecdee96d5c48543f468b3922517a9c4e`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 93.1 KB (93077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:54701503357d38dbf5ace89b77543c8fee2f2b62adb377e7e960062c2516a02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd05fd8622dccb239d931c85ba833255c0c1529b61cee5e678e8a219b7b04f8`

```dockerfile
```

-	Layers:
	-	`sha256:faadff5adb164e444a55b837fc6ce43c32d2f30627d4d1a82359fb8fe02245f4`  
		Last Modified: Fri, 31 May 2024 14:44:20 GMT  
		Size: 3.9 MB (3901984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cc38b6d237c2ebcca5ba6cf809711edf85703898a921cc5c6525ad6628ec43`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 13.7 KB (13708 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:b1ea3f82110646d04e2cd193cfcc390d242aef8f792d7c10cb868bb55028856e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62386418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff4e0dbf43c1e191ed8ab62082ff8800631ddda751cd3bf73dfd9466cdda4a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654914778f47e9569f4279608f872556930f59a164aef5c622de67fc5edd6f82`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 11.7 MB (11689077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763ff0412f0e24675a3c0094d231bb5d4e8e02027bf12f3b704a8d7af2450df`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef928bf7664c03b3c9234628507b67eecebb9081c42037bf5c7ca67f4433ae`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3051f898514f269b148860e9e91bfca7792a107c5fbf163511aa3cec10916233`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 92.9 KB (92909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:707caef59da5288b96b2f894add20f103d29398bf92b5384278fddcf7021c770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a559258217bbe91bcc304ed53adfd496f2848b2e2d4826ba094c773e63535de`

```dockerfile
```

-	Layers:
	-	`sha256:eeac70b13c9895aa8af3bec72409fb2823f2e7ca87b2c0aed76b6ccb8d679b19`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 3.9 MB (3899664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf78c99d9ca5eda2035fd438e3088bc64a084267eca3dffcfd65fb7e68f233f7`  
		Last Modified: Thu, 13 Jun 2024 01:59:24 GMT  
		Size: 13.5 KB (13452 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:0f88bd0ec5e17d2cb503f429779d919f272278d590eb14fcc8172dc168347568
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1324249971b25b9e0f7bfbcb4ba4160e30dd14a3aee17827942c6fd196b21c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60938168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e3bed1d904015142866727f1c9ef5b093e2ab3d017858e81fd44ce8e646a95`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de5108429a11f59373651715b9784a49e539ede6e3f805e15791de2362df062`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 11.3 MB (11266565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55dc84dd6d1ef1641e3007a6900bad1f55de89683e01abb5b12c5bf778734be`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619037df3f69df28e13ebdf7c547a7a3edb46499636b2fa8b88ff6600f6bf41e`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f222c14670fcb7af3f8ba4eaa5016da2c015963ac7772601264c04088c585d7c`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 92.8 KB (92792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb0f830d1ccf6969fbc75d17d324667ee498ad683d50f823a83514cba413ac6`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:be881a18320b4f1498b1859437596d983b02d695b68298dc8c55a34c9fafb9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab935771651c8d1921eea385f4395ef910b7bb94a2d465db94c9c38a88b1f5d5`

```dockerfile
```

-	Layers:
	-	`sha256:15c1e7b9047fffe4ee424e2d4afa5c012d873d4f0662e04926797e43b68ecc63`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 3.9 MB (3901779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d38a08e967e42b6ccdbb3163ff5f5f3b750a4689b8b22f34ea9a7167aa86b0f`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 15.5 KB (15461 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d618f33d5af2fb31fa36796bfd87f6a8c5170c6f6e4cfa37a82c5037896ff583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60940966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394cffc10c82bc96ff0460638c0e5b4940d173aa5cffc9ccdd2496c4984246e1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9782ebad61654b7a2473c30e527f7a02ef0ff05bbeecddfa2c2a63f5e2e99048`  
		Last Modified: Fri, 31 May 2024 14:44:20 GMT  
		Size: 11.2 MB (11232082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ee0a093ea753330fd619da92cd9d8620723145c8a836f8b74d64edf92a5d14`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e17f23f6fb69d4dea07617d31ead77946fcac635bc98263d0e0edfd62d3a4`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b77a1d67cd06ab552ba0ded4026133eecdee96d5c48543f468b3922517a9c4e`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 93.1 KB (93077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd8147b4588fef5f9141e32cbd7dbba8d5316da8488ec40f6aa5ae93dab2c82`  
		Last Modified: Fri, 31 May 2024 14:44:41 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a8574c6d120f66dd79367bbf464cf086bf7fc57db846e16e4821b635ebe1c89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82e6f2cd6c502f65580cc742a997c0e189ce903ee23cc816fef9f92165a897e`

```dockerfile
```

-	Layers:
	-	`sha256:2ef168679fafdc885aedd74fab6eb619f02fa79603bf0e20ae70ba14840c6e7a`  
		Last Modified: Fri, 31 May 2024 14:44:41 GMT  
		Size: 3.9 MB (3902020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e441abb00e97fa0e0d88299ab5846ddbeb86dfa258473db0c554cd7c5edbf06`  
		Last Modified: Fri, 31 May 2024 14:44:41 GMT  
		Size: 15.7 KB (15740 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7d6c8b4235db55cc82515f58088ffe599c694475bf9a61ffdb1458c09c883ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62386687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4239d56f5279cdea7597ea3479ee0379a5db524731ffa3a8897d35c876429e6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ffa67f849088d881ec1bd3050a216a615ede2edb4a511728ab5579a4fae22`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 11.7 MB (11688926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d8837ad2608097649f544d67a4577b1866865138f9e8a31b177912f5dce031`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161d8b08f6c9b9bd78b7414abdff21676319fc84d129807f18c1b8bfbe0305ce`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16fdac0c82ae1c1ccc8e105f8f96121d356b25ed71c9e2f32f7b680ee7841fb`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 92.9 KB (92895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad11b88e0c406f04ba1f7bfc5b1e04abf93bbd0bb16200a45f9560e4aa5c536`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:064e42db5fb916ae8be69bc1f8b43ddc7e644e625a376fa6d05eb362ccbf9310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00f6fa8bc6946b7ac2df2495e1bbb4e29e45525ca16dea8af7b9c0d71326442`

```dockerfile
```

-	Layers:
	-	`sha256:4791f9f5accce2cb9c311cea7d28bfda43d210e219ed131cb338a3a4195c767a`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 3.9 MB (3899700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432c1acfda6da922b96c421befb8a54378dbc7ca4b5d79bf4ffc808a14ddbca1`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 15.5 KB (15483 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:39078ae512762502c8dd9c99bdc04032b9372eb9c95adccaefe4aa9335a48ce2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:7d53ca6634bc4f71e803673f7e026a3ed063157817863650399f9949522d7a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30487136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a14ed1ba14993d490c686fd0ee743fab1e10f9718be288c5ffe99eb93c2684e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Tue, 30 May 2023 10:03:37 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b18c561194df3348da8d2b6a32ce63573a55c466f094dddf86b6ae60d1a27`  
		Last Modified: Fri, 31 May 2024 01:56:46 GMT  
		Size: 4.7 MB (4687003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465ef96fd4980c8f189fcc771c808915f063e4f3a24af79dbd4f7aeae609399e`  
		Last Modified: Fri, 31 May 2024 01:56:45 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a427df721c2b95fd6cdd252c60c00de7d94e502f684de005caaa8123bebfa6`  
		Last Modified: Fri, 31 May 2024 01:56:45 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7383c932e309628794f537a905e524fb3f7f5bbc53a3b5836cdb206815f89e`  
		Last Modified: Fri, 31 May 2024 01:56:46 GMT  
		Size: 107.0 KB (106959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd18.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f823abed5bf0f9b5b7d1036931e95bce95877311d47e05e8738048ef73b622d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1920845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226b0897fdea8020ae75200a53b1f794b410f8188ce743095eef9d8b40b181fd`

```dockerfile
```

-	Layers:
	-	`sha256:59e86676c2427387b28ada60adfdd9939891e96da628232e059eb1b658d0522b`  
		Last Modified: Fri, 31 May 2024 01:56:46 GMT  
		Size: 1.9 MB (1907475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b14dd6f16011ffce67a8c764cde750bdf471aed1f3814b9bbdbf226c104a6b`  
		Last Modified: Fri, 31 May 2024 01:56:45 GMT  
		Size: 13.4 KB (13370 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd18.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:576d684548e2dd160f926f3e3ab856ee19bf99609251b51346517a767bf22c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27090983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9899163376352bd0721873bf1a79dc123967b36d67bfe9cf09122e730bca535`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Tue, 30 May 2023 10:03:42 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddda72376ca07b81a58afcd07ab707bd2b65eaaf4b638adda578079eff8f5024`  
		Last Modified: Fri, 31 May 2024 11:26:02 GMT  
		Size: 4.3 MB (4268722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7386017dd0da8e1005b1406e7a864fd7c7378741bac7f1e6974da156b71c24f3`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d876a1c7682fb795ebc1e91e721061bfbdcea91113e6cf1289eddeb3ab5774`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b133983b820f58b53a8477086ebb696d7ca345e5daf8210097cde1b3d6f130c9`  
		Last Modified: Fri, 31 May 2024 11:26:03 GMT  
		Size: 106.9 KB (106852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd18.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7d883ac5d61db58829f06278d94957b67b77a5702428e6434ad3a326595e48a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1921307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1facb2b2a872e5b8467f689e81da8e47b45d960a8e80642f4aa535467de08d9e`

```dockerfile
```

-	Layers:
	-	`sha256:74ccfed9bf877a74e0f2cbac4eed8243444b2c0870e5e297bd77097d98b4d391`  
		Last Modified: Fri, 31 May 2024 11:26:02 GMT  
		Size: 1.9 MB (1907658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477a659704ac1e9f683438b6b7a4bc2518c393f37c76a2349a34ad1fc56085dd`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 13.6 KB (13649 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:0ea6a040d3005bbc6d6adbde1b3c4dae2d89a4c4dd943ba32aa350e14452886f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:18169413818de1fdc43e158c849d34850b02a6390905f424f8b10ca50211ea5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30487499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad09230fe8daacf1f1a34dc9035a37fbae4351949aa366e5f398789759a0b839`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Tue, 30 May 2023 10:03:37 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e5846e93887a546e4f0410696260f4c77e386470678fb9087874d2e2524648`  
		Last Modified: Fri, 31 May 2024 01:53:27 GMT  
		Size: 4.7 MB (4687092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed4ee21cce42c14e3fb8fc307e972c22e1f37766ce10ea56c1b9a8a0a3b4e7f`  
		Last Modified: Fri, 31 May 2024 01:53:27 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e9dc044f0c27fa2a4801bd9cfe358b5963621bb4678ed04eaeaa39b47e216d`  
		Last Modified: Fri, 31 May 2024 01:53:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc8e83d4f824da3b76b601e84201c6a07c69a82d7fccea5c2c38a089959d580`  
		Last Modified: Fri, 31 May 2024 01:53:28 GMT  
		Size: 107.0 KB (106976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8aac03308dee46930f831ecbedcb6dbbfff06484b3e1e610839f45e1bc49e9`  
		Last Modified: Fri, 31 May 2024 01:53:28 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd18.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:880afd29b8e91716e066711fb12dc7f417be006872cbaccd832e847019ef7cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1923112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f4199010c3c203b7b6090e2041c2d2d807bba800667a37d79712217f5d9782`

```dockerfile
```

-	Layers:
	-	`sha256:9ca82aa12724fbd0393e316e569d6ce7b654947400243964ec2d7559dd11f17b`  
		Last Modified: Fri, 31 May 2024 01:53:27 GMT  
		Size: 1.9 MB (1907511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd1a8a30123b9a8b1f54a4c61dcc0b6bd5ff9ebfaf54e0d66be9e3d7b9a925a`  
		Last Modified: Fri, 31 May 2024 01:53:26 GMT  
		Size: 15.6 KB (15601 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd18.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9c0087fb2593667a29da5e15ca6c6195d981098e591806dbc153c933ab206780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27091244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854f697b18ee9a7e7576402c46570e83539fea823644d026b982df4cad449eba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Tue, 30 May 2023 10:03:42 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddda72376ca07b81a58afcd07ab707bd2b65eaaf4b638adda578079eff8f5024`  
		Last Modified: Fri, 31 May 2024 11:26:02 GMT  
		Size: 4.3 MB (4268722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7386017dd0da8e1005b1406e7a864fd7c7378741bac7f1e6974da156b71c24f3`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d876a1c7682fb795ebc1e91e721061bfbdcea91113e6cf1289eddeb3ab5774`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b133983b820f58b53a8477086ebb696d7ca345e5daf8210097cde1b3d6f130c9`  
		Last Modified: Fri, 31 May 2024 11:26:03 GMT  
		Size: 106.9 KB (106852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3db3528f80fffc9adc3f1840a8ce5597384283543a1634e3a255e81a5affd8`  
		Last Modified: Fri, 31 May 2024 12:13:46 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd18.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a98b30791125fe37b5ddf48f5d03eddced0fda6fb5f219e49c18dff3963021e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1923573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd87183851da7fa8aa438d607d5c9dd841e3703014a8d9bb101d01f972e7c472`

```dockerfile
```

-	Layers:
	-	`sha256:6bd54ab750554eea7ef069ed465d824a8167370a301986aa94720c173807a075`  
		Last Modified: Fri, 31 May 2024 12:13:46 GMT  
		Size: 1.9 MB (1907694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1028c37d9672e46133b86c2713ededb3f570948468eac19912954a30057615`  
		Last Modified: Fri, 31 May 2024 12:13:45 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:35696f693b6ef96260422b9091c766188a7983d82eb58b1eb04f6bd7b58ce84a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:8436872dff585d3f4fd9ba47de2a0c07d2c9601ea7683cd5d98156073fb3e61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69c59f4bc1665f4125a9108a35f53ff8fd3c0f0db4bea3086ff4c0cb4117d2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aadfed4b17ce30257b1e83849176e62dda5f82aa6e95a8478f76eec14d065d`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 5.4 MB (5360246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ad67a268cae8111d8fe8b7df873538bdf930ee3af83bddeae455228cf4b12a`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d727c6072b0d91a97e0e503910ae3a3875e0eb0f330dad37430449c5d538f6f1`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a1cbd18209d18420e1b340bb0af4bf1810b5523ee10e459833effca52500e`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 105.2 KB (105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af0c65cce1965a1a6b3c2b2975e967c195bd2eba5a033dfefc365029b377dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45da22baf7d2b89589eaf2d5f3e761d81c297d1c7034615e130e5031d2b182c1`

```dockerfile
```

-	Layers:
	-	`sha256:b358a4f2b71ae1fc1b775755876a2990c2755cb455ca4551f7204050603fd0fb`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 2.0 MB (1977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:543ad7176c91bae6840122d5e6913e1dabd6c77bfd53962ded0190dfc7eaffd4`  
		Last Modified: Wed, 05 Jun 2024 02:20:28 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0f5b1443b574b5ace2b0987cd1977e8210613ba725ed472573cfbe9c5cfe23ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b273064c8a6c81f5cacbef5005cb8661311bf23c477bd55a7c401646da2abe1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:284dd670c2b0916e7375fa296cc94b380cd5d78ea887f00690b52596df26c8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c3a8fbbf35052ef29f84d07daf978d8d877ce6f9fcacb449acf1ffd0144aba`

```dockerfile
```

-	Layers:
	-	`sha256:813766013ab606a80d4443383a3397da61d8900db25f42772d29d6cf04b2bce7`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 2.0 MB (1978184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1bf415abcaaa1e6c9340665180fe32490ac956e54c13e38d2b031ff973533bb`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:69eea5eee69951a81433ff44e3a76d25374f43b5ede7e2be7991cafbb9ab8480
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2614cd1459a929df672f30c4de3ff5f4f423b10d0204439ea00b153fb35a4ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ba3c03399056b312baca33d2bef793afd92675c192b7d90af7db16bd0fe08b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab32168f62b0a56e9d1738ba27dd0e7b6b3b7c2e892a19527bf5495039d950`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 5.4 MB (5360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c5f6a989efa6cf7d58ae9018a40243e81a4b1bdcb7a242de74e77d92f945db`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfefe3835ca69f4b947ebba8fa742346a61ebab4361ca98d383e7ba7489fb004`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdc23cea86c9950d617b60a8e9e162dfa93280986c8e4ea3c9efc6450810bbd`  
		Last Modified: Wed, 05 Jun 2024 02:20:11 GMT  
		Size: 105.2 KB (105229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026d40b80d1375c0c978e08b9ee3768e5635a011dcf98d75ec8a728fea6461cb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8052d782c0e8c3437bea67acf4b2a22d79a7dffa5297317f4776bdc773d0701a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1993579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b545e88e893b1df4e4133705e4b3af666a09fa688c52562b97322c9c6d4c0099`

```dockerfile
```

-	Layers:
	-	`sha256:fa21014e2151b093cd2b0f181163b6be1985c8371a5cc2d7e52e4613433f80bb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 2.0 MB (1977992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15b3763a1a7a0714189ffe6046baae58c42e3ed9f083352e41a11ca77cd14e5`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 15.6 KB (15587 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a765833d6e8524c6babfed520f054ff84a6adea03bbc27c95574cb07aa8fa14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10519d9344ce22cf8b6dffbe4a09a105acf140f518107098b2c66a242582141f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5151156e9cc1c424bbecfc412c4effcbd14bdcecf53693bab61b678ae9ed5fd9`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d450bd9f532b807f700d228fe37fceb706c7960f3b87d06090658a57978a3d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1994083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e25fe54f10b92c153df2cdadaa8eb3efa03f0dee4e099174db24e3ac65946`

```dockerfile
```

-	Layers:
	-	`sha256:ed1c978d1833cda54dd5250213c0833f524702bb98f9f00a81505d89c5d1b173`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 2.0 MB (1978220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b63cad0b9de5d2bb91de6e7fb6616926fabbf2094cb6ffb471176092d3df97e`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 15.9 KB (15863 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:623b758391fb029c0195fce359139e6ee027655959e76d09fb4ca2e26ffb941f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:62b21ea23ab0099bb7bb3c5dff41f062348f26f984ce63d7adbdce9523debbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d480dfd32cd52adab70bf29d18e316284e516732cd7b64ca8fa74057e78b2bf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13680b52a20c7f7235a12148a3b749ac0b8059a27ccf65a67280b22ab004496`  
		Last Modified: Wed, 05 Jun 2024 02:20:23 GMT  
		Size: 3.6 MB (3622659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9c4675fb06f3f04ba34fc069e9b8352212d06376d2db5919df67d4861e337`  
		Last Modified: Wed, 05 Jun 2024 02:20:22 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fe517f5124a0cd3234b7e232a0eb9bf389b9b8927d1108f376ba18f4a602f3`  
		Last Modified: Wed, 05 Jun 2024 02:20:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5c2f84665972fd9fb9573b2bc00b57c4d6633e031d81eca30d1f1a26e9c4a2`  
		Last Modified: Wed, 05 Jun 2024 02:20:23 GMT  
		Size: 110.1 KB (110101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b4eed60b439ab7b3dd6a8b8b389e08f83980039978671105075d770d2e36f4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94a87947aadbdb67abbf4192622756c526f7bcd4b104de43c0ae0302f13f532`

```dockerfile
```

-	Layers:
	-	`sha256:47a512237c86f29a05d8cd78319ca62f3d23f9959e965f73984dc89c544cfc9c`  
		Last Modified: Wed, 05 Jun 2024 02:20:23 GMT  
		Size: 2.0 MB (2015658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b7dcb1333f9cb8c4f4713875a80365a39445f7452398c4a29dcfca3d6e82bd`  
		Last Modified: Wed, 05 Jun 2024 02:20:22 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:182965a2a88e752d9531ab95095ea3f137ec86496b97f9e82a9df5c92f2338bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31070904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0020b4b6b75f3fda2b2fd11190ea6b59ae189b71d7fcd254bb3e3df2d195a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fee3ef976957c41d04767884cb43799b96170dc7f90b007a26b81ae7b51c1b`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 3.6 MB (3595512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad45b1472436df983642ff6f6d821159f3cd9284d480a5e549b8c52f96c74c6`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154dd0239ee03ec9e4d04dc3e50288d571e148ebe8a49b6b24e5b4dc41e65926`  
		Last Modified: Wed, 05 Jun 2024 16:36:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e65cd6fdcff0083c9d0e5d5a4702ce5a2ae4964d6c7640ff281a2687c2a4f4`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 111.6 KB (111617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3daf4feaf8b1af264759adfc71c17d64177646bcff852e4c561c28ee3ab4296b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a01233855c07d4d99141d81865bfe4168def1876fa3a1ef37be11dbdf4b2281`

```dockerfile
```

-	Layers:
	-	`sha256:b5128b7a8311295bf17b1da5ff28149668958c562a0f3982ea7b363c9a9ee90e`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 2.0 MB (2015917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09216cc84b65a36876b54e5c68b7ad1aafcc4a002ac17e4e904429aae09512e6`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:d636f78afb87861ff221bee82f72a33a40c1a079f2aa2c684d744e545637ec7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e7abef41958dd7dee0bae8bdc415b40824f92a6d4ec132396486116992b7b681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d23bccb9a816ef20f98f4d9b63173c11a283b12820991f11f7115d85a7c5d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb43413ee829cc75026067ac5d778cafafb77917da12b5dec6e0a6447a7f8686`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 3.6 MB (3622639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef34d71f1c9345b38a1e54a91fceb7aeda6c3c0467ea3f9b83f5beee6bb28afc`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7e8f5f4c30e732d2e22abb93e18bdc0a94b22fa7c33725f6be4f02110ed64`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4507960307afaaeb03a72f97620824aecd40f2cb9e3c423b414a6cd862a7594`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 110.1 KB (110053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111b9057540b39a6b4ed07fd7e9a6a01509e0ba6521ca9b08b2d1d4c91393069`  
		Last Modified: Wed, 05 Jun 2024 02:20:48 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:00e298aa5a60fb2c6ad6308605ac14e42df08b2449ddb03dd6710c33e30104e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b82f8e8554ab34024a8fb1f2871a2f17e9c69ae0cc5729ed7de770b5081321`

```dockerfile
```

-	Layers:
	-	`sha256:b22d44f8413e29ed450460bf31f184eb25021178d345ba4ce95411b57fd319bc`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 2.0 MB (2015694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583e8e5db7add610c022447326ac812279e0a609b548dac8e3235070b6543a27`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 15.6 KB (15587 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:896ef60abff1e40bcf2965d6d8df5d2a195851495349d25d494954c7b5bfa98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31071166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e612430921515a459d27a9426506ed0d62cc61fea28c924deae22abab84842`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fee3ef976957c41d04767884cb43799b96170dc7f90b007a26b81ae7b51c1b`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 3.6 MB (3595512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad45b1472436df983642ff6f6d821159f3cd9284d480a5e549b8c52f96c74c6`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154dd0239ee03ec9e4d04dc3e50288d571e148ebe8a49b6b24e5b4dc41e65926`  
		Last Modified: Wed, 05 Jun 2024 16:36:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e65cd6fdcff0083c9d0e5d5a4702ce5a2ae4964d6c7640ff281a2687c2a4f4`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 111.6 KB (111617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f09225e0cb5ea6674844916153d839c9066d4cd5ee893857fd71e33171f6f2`  
		Last Modified: Wed, 05 Jun 2024 16:37:18 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d1484488cfba61c7d8385fc94eafc909180fc2034587ef9a5ebb39ad12c50734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82076d7d5b1183a967bac10516c4364d113d0d845b3ec8566bab1e283eac3f62`

```dockerfile
```

-	Layers:
	-	`sha256:e1492c9297abfe99ebf8e9883509b49605e6e5b7b60818a7b896d5a6b0c63122`  
		Last Modified: Wed, 05 Jun 2024 16:37:18 GMT  
		Size: 2.0 MB (2015953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71ac22ae1be19aebdfdd740c17c6b8f039dc72dba7a8ce1b8f1f7d53b62e8f9`  
		Last Modified: Wed, 05 Jun 2024 16:37:18 GMT  
		Size: 15.9 KB (15864 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:388f6c2461bc209a692170f696d1f5ff96615b60c45bc27f86de6f1eef1b9fb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:84219b6ad2c59d4349766f7ea41188ef7fd7f23e797f234aa2fc118476d87a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66307474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00919434e4703f6acd6065bc95f564b675939dc982ac937077fb392e2b545964`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fff6731503f1b1a12f3ec6074982a0a7c9e1faacd14096103760258566582b`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 11.1 MB (11104993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ed83a5d194b8125fc4475a7474d7614f9fa2cdaa8ef76360838fc01af94e79`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87281e9a3b4c0d00588f26599ef01f9cb268f821a34af340cd347f8c79442196`  
		Last Modified: Fri, 31 May 2024 00:56:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52629961e0dfe4a11e23ee3273dfc2941ef9296958ce0433be941e583fd3545`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 100.7 KB (100736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a7775c23e5a426688a89fe8bb88b071c4b67d2c0c5bcfc7762283e0c64a8eb`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f5badf72a6a31f4df91f889b70573094f100208cb79dc40f13ebba462e395f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752e07c04e896d0e9354d9f9aaeea038b337272f1c2970023a1a6c328cfab70`

```dockerfile
```

-	Layers:
	-	`sha256:1c8a56fac5dd5913e2895f29ade5a290d191979513f8716a9f8b6417694c831e`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 4.2 MB (4199082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d009cbb1fc1738caa42c4c5f123155cca5ae8713acd80bac0f8599a98214bb7`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5d1cf82cceda318c0dd41a8a0400d8411edc8a4d51ee0500d5d15b787f48c559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56caf73109cc0abb9aec10f6936d04cff9ecc5e4ed695667363742eb5c0c880`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1483c42dcb365aa70f1ee657cb621d71108a07cb14e7da7c0af1670b1d3dc`  
		Last Modified: Fri, 31 May 2024 14:43:25 GMT  
		Size: 11.1 MB (11105807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bdea9458a37f5e1417a645e4803ce863ee56f1bb909725f8a36979925dae88`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a358d18ad53e6c2f3626a6322cc6c11247f800ae4b985a091f6495eba713135b`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf2eb23fc03995a0b59c27e2f55adfc7906966f111740c748bb549fa4bda575`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 100.7 KB (100692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8729b3ff44329714773e4eb7c4046bcdce6dcd6ddc587ddc086d3594ea516b`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9c183078ed2c49b83568bf2f7c05cf59aa86563317db10e1fd35dfd0c4700705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b2481a942ef60260cd04118ded9798eab96a09d5a9de29130742c9d682bac8`

```dockerfile
```

-	Layers:
	-	`sha256:a8cb3999134b399777bdccdbcfd6a6470c17788e420fd152629355c483c2d10c`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 4.2 MB (4198699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb260b9d6aa6319449c343ab09e6d08a9472f4d08310d1d79af533866fbeed82`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 16.1 KB (16067 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:30c029632c96bf37af9b76eb0393927bcf408d4d4637bddf613a7594b2681b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5864c6def933a6b6dd9adfb7a5ec63fd1f46aed4cd44d9bfd0cbe3d67f45c8c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b13addd2b2a32b9d1ff2ea9286439b5540ef92b6f2a15ae59e20801eaeb8115`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 11.5 MB (11500167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925784d52a7a52e17776422204b33b6f319d5ac291eecaed873d7c75d0bf7b5e`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc25404734dead4fcf99099c0b8c4c255e177881c3cf9e4bd15eecdda5bbfeb`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77175288a751964832d472ca502af30d298ab6d18b500e39100c7e2cf1941a1e`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 100.7 KB (100656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403eee5dd3ac973d264d6caf142749476a40597c843100f860fd812bbdd7152`  
		Last Modified: Thu, 13 Jun 2024 01:59:16 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20b1a751fa916af4b95b9306d65f00cc6ede2b46bebc04dd23cc8fd44391f864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bf79df5b568b2fef0e797dc3f58e562b7992622978ab8ae0de582edd25ac64`

```dockerfile
```

-	Layers:
	-	`sha256:5b95beda90bc46a2b778e530d4afd832492d8e6d2ba670872dd2bd272173e02f`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 4.2 MB (4195537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42daf680929d419028ac29504c6aa3762fea17ac4478e351fac146d840b2c94`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:7b10171b71a341f81d2db6867a5d45c17232a457064c0762e7aebdda3b94ad2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:9d6b76d38812539161f59c893466f5b49a8fd9591f8d2f2a01015142b1b7b216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60049164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9e6ae8e755fa691be543e87a19ceaaf5730a42a8b17045af0d7844f85e3ea4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b719a38bf4aed68db29b56d561e793f8400c5edee1406cefdc25ea0c72ae7`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 7.3 MB (7313247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89a778cadd45e115aab99728a495443d9a0e22db2b4cac341924a9d85071fb5`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73059de92601721fef9ac2c3019771fb96130f0ef7280cc538253280cdf1ba92`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c97c37c295b1b834c6ff803661093e3f42e5e01f6c8a476778c58cfb56657`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 91.0 KB (91039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:388a04f898471e845839e7d41f20795d49ce13fa7087377c1fcd80379d946168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de95620c07d5b4bd87bc12d9b2921d0d89a03b37227a84549003b96bd538f2c2`

```dockerfile
```

-	Layers:
	-	`sha256:a4daf7efa1f24d0026d214c5a47303591dc8a26d4667e0022b33447e0bcbb444`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 3.6 MB (3592159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca62554e92aa67d490ef6f1f7c63bcff795065618587426f22dc4754279c1ab`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 13.3 KB (13348 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0bc06edf842750d1b8f488ba4dd6ce12a30c56db39f5770556bd2ef64474a267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60321222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6326bfb52a658f0caa666254da500a6cadce9719e0c53ec40a929200564b0269`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:65d77d3f6289af1318c696652b600f022ddbc3a1daaf105602e348ad91d2c41c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66334a1d5d0f0597e9440b0db265b333533e2fce7f5bb2d1fba09c85ef6cd21d`  
		Last Modified: Tue, 14 May 2024 00:45:15 GMT  
		Size: 52.9 MB (52930287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bdbf9908e45530061175939d20c6ded00e858fc7838427d8713e0ed59e84ea`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 7.3 MB (7297335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0922009db60c6f3c98281eecdef09a0c5ca68b58d2bf585b8ebbef25c57d30f`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26863f97217b3df00be0b9bbb64308b763fe60c3bcf24a1cfc8c16428395f03c`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bb75772d75f5c87c177220dd50d76572d354d75f97b9186a272610c1c9fa27`  
		Last Modified: Fri, 31 May 2024 14:45:21 GMT  
		Size: 91.6 KB (91620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bf6cd02827b2dd05aeb0613d98a66272fc567af92724bfccd95a38c27cf27ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cac57f1a7aa1101336c904343c777b772e3e3c16c662ea2deb1242cf1fded1`

```dockerfile
```

-	Layers:
	-	`sha256:1acaf9ef26e92ee887ebe48465d6d949355c6b19ad6a9c7529d7e63625abc3f8`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 3.6 MB (3593200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ea3f17838a54ab388d0a3af2242e54f2977a570e2fb3d32eaa408a183491f2`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 13.6 KB (13623 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:97b5f62de5f63780c6fb60c18fac80a4ae8cbcf56397376e609f8a665bd42094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59947484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df55d8fa11cb174de39000a2295c9dbf246bdfe3cb88605507a5506f7f2c7c05`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c7b81abba8966f408c068710549216ceee2b9d423c6a9411b04994eea156d6`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 6.6 MB (6551754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d3739f5e8659580229543579dfafaa8a624b3f230cc3c918f717afff60b7fe`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62789b7063d2d62b9591fffcf6f696ee77c7bde371b15b61b45647cc1c4139ec`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f020a648d73b4c99abcc87718351afc13962b285a67fb1149a89fbdd5789e6cd`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 89.5 KB (89451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c3a877c1de721606d524b8aaafcbee6ddbc5e18809486d6563c15c9eba88b2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaf78d03b9d7b700c0ec38992b872c759e77ea48b08ad2e0688433a71435d0e`

```dockerfile
```

-	Layers:
	-	`sha256:8e15cf37b593768d02d1e5e5ae9e91ac87a51f539dae42d421dcaf98d639257f`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 3.5 MB (3547113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29033c721523198453ef2a66dea5e3d3d2b8efe44b0c1bc7ea31d1db80dffb0c`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:1f347a1caba92ee7d0c0480f7c658da4c3fcc562cafcfef560129e81cc67bf61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5238cfe08865e6d220ee2e441d2a11b4dd3876aebfe8934d3ae847a062d39a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60049648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5fd9cf60415cc4d6a2e41b0ecb799b45050a2b735d4684059251269f304fcb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e371f96dcd488dcca9b548ef17888a30c45ce4185fb64de3935db57cdd0f075e`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 7.3 MB (7313276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663cae23bb39c60559275df0410ebcaacba26c9c421222281f939ee17f70d9a2`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7d3a1037ce374991daccf4e28eea64df1abe8c4db782678a283235875aa22`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962fd9f4dfaf26a175b8d9be95478724907ec51e80476cb047611792164825e1`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 91.1 KB (91096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a48833da318e61e1c29dc561a729bbdb2297e59817a9dce4d792c1a03cf48dc`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3932fe7a10c4ef043d4b16430814bb2f7593eb20a6a5f9e64f1a2ce9ca2961e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300a524f0ae3b5ca164f2d6494e49f4b28b5c83b20dc6b0e9e4e0b63d64a34b2`

```dockerfile
```

-	Layers:
	-	`sha256:d3daceb491c6e32ec20d264ba220ecf8d90a01111f4e1ef6b3395d3f0ab10f05`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 3.6 MB (3592195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce8579bbeb70277e1ebec780493f9a3677213b182e3859b373d3843ac4fa3485`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 15.4 KB (15380 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5fbf2db17bc959f10539122428b5eb7ce8872b4b81fdb911808dc8529e531f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60321617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce15232a20027fee120dde8e91fc9e494c52ffab824dcb035408941efdc5af8a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:65d77d3f6289af1318c696652b600f022ddbc3a1daaf105602e348ad91d2c41c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:66334a1d5d0f0597e9440b0db265b333533e2fce7f5bb2d1fba09c85ef6cd21d`  
		Last Modified: Tue, 14 May 2024 00:45:15 GMT  
		Size: 52.9 MB (52930287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bdbf9908e45530061175939d20c6ded00e858fc7838427d8713e0ed59e84ea`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 7.3 MB (7297335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0922009db60c6f3c98281eecdef09a0c5ca68b58d2bf585b8ebbef25c57d30f`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26863f97217b3df00be0b9bbb64308b763fe60c3bcf24a1cfc8c16428395f03c`  
		Last Modified: Fri, 31 May 2024 14:45:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bb75772d75f5c87c177220dd50d76572d354d75f97b9186a272610c1c9fa27`  
		Last Modified: Fri, 31 May 2024 14:45:21 GMT  
		Size: 91.6 KB (91620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bd06c55918dfbf55eff1a7418f35b45e8b2fba30f5de58bd55be197b91b1a9`  
		Last Modified: Fri, 31 May 2024 14:45:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7b07ec51360998e4ccd0e8f52eaaa76f549978b314ee67ee743906d45083fe88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1465a6b9bc9754c12336dddafb4bfb733a2e0935d11482c115926a209ddc9e9`

```dockerfile
```

-	Layers:
	-	`sha256:fa652cbef2bde281071916747098dad578170e9376e8b7930103ef0e02e84f7f`  
		Last Modified: Fri, 31 May 2024 14:45:42 GMT  
		Size: 3.6 MB (3593236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db4cfe024664b5c03389ac7171d4573621a698e43b06e77849f945768715797`  
		Last Modified: Fri, 31 May 2024 14:45:41 GMT  
		Size: 15.7 KB (15653 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:d4bdf1159b48c2ecabc30bce4f3ea3ae73a8a2325c1326d2fbe45e7939f168d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59947750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b40502da47f32b5a185493da2779d36e20e7f4c4747590909e51d36de4b97d6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21de92121739d4fa9675f02b90861a34f4574dc9e316bb0802285d92e4ac9b60`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 6.6 MB (6551627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96fff31007030f5b9515a1a6aacbd32612b1d07ff9f3c78c1015183eb77672`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62789b7063d2d62b9591fffcf6f696ee77c7bde371b15b61b45647cc1c4139ec`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731f1ad43b355ce70365191a317496e08b26eb26184ca25bb2fccc05ede567bd`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 89.4 KB (89448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9d9e3bebf592f069cd34952600f4fdab904969c316ff205ecbec5fd7e4d7b8`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b8023242e636bf70cbbc9a46cfa11df011120a169a23c971e7b816b8727c27b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a40003dba26a551eb5404e012d47a3314c68829113f7442897d4a58fd15670`

```dockerfile
```

-	Layers:
	-	`sha256:9116b10c7dc54220fedacf31400461ce9e8ecc63e2359d29a7cfdda20ae5bdc3`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 3.5 MB (3547149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e85ecd426065713204ad4fcd588935afb2e9b8a8a114098388115cc0ff4755f`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json
