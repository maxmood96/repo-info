## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:91dbbdd5886f67a3162ac3fa08574384407c958cd9e3ace5fc00ed4f2c449888
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
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
$ docker pull neurodebian@sha256:76f6b5a63cfcfffceb39cb9f870a1d644f21d4e5562dfef4aad140f421d10d66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60264799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae21ebe5a6031abb8f43b9533f09e80e4b308d66eb965ad822ffb12aef24fef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:02 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Tue, 14 May 2024 00:40:02 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:15:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:15:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 14 May 2024 03:15:25 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 14 May 2024 03:15:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021d53e4d1b38dab81765ab5c87ffae5865728fe2af3d740910b5e4356ce5ef3`  
		Last Modified: Tue, 14 May 2024 03:17:00 GMT  
		Size: 10.5 MB (10510419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd61102fec171a48f90ec815ae0d011ce78eac3532a5ce45eba516a07a2fa35`  
		Last Modified: Tue, 14 May 2024 03:16:59 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca33e2727ac03ec34dd319999888eeeb7615d86fc266f20935f39f014a12f66`  
		Last Modified: Tue, 14 May 2024 03:16:58 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf7b60f52eb25315db443d7e9b5aa560d8972332470f7db6917306c18ba341e`  
		Last Modified: Tue, 14 May 2024 03:16:59 GMT  
		Size: 299.3 KB (299277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:408c3e1cd2f443916e857ded1382dc93f85b34a19964bfe25d293f2fd8dee173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4331f3d4bc117e2a005a9d84cee8627ac2d2e49f54b6995083016dc0a620f286`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:5e59addfe8663b7c16cce40874c2a3c8601e20e80f5a0897c86b64ba463c10e9 in / 
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
	-	`sha256:1a892f56e4b10aaecbb51b3219d90bd0d8a1e955acd0624a6ef27ed086ba168c`  
		Last Modified: Tue, 14 May 2024 00:53:06 GMT  
		Size: 51.4 MB (51419713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c69bf1688c8418e0a4181c9450d35a9e1a4be76cc447a0655c971bbece6817f`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 10.7 MB (10672299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f57c540aa2c151a92c082fe61fb8d24cc3122c024c083590fcf2a67d607e5c4`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e324ca101e0ea13d957f5a45d94621cb084dffaf4547471dd53b306ab98f49e6`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326d790e3e3814d94b6f80ae03b479cfb649503eece3652d4a8c8e3d2a48d31b`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 104.1 KB (104135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9e49372b57f4428e4144ec1b4be8b737435f2679c31fff55773cfffd1eaa2327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dca39fbd6bd4f26828d0721e504cd9202d1f1836b6794cb1dece3effdab7b19`

```dockerfile
```

-	Layers:
	-	`sha256:3951d6843c389685fa1ca30f3285aaf65fa2ea7485922c26d3a4f871aa49d36b`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 4.2 MB (4212312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7485ab859fbe734b3354d296b359244784d852ca5562cae306426317aa533ef`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 13.4 KB (13376 bytes)  
		MIME: application/vnd.in-toto+json
