## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:e20e07903423131efb91f74a682fec626270bcc614580a2e3b4c613405cb421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:59c6d09d8c8f79dd29a29496765d73f8a9df4a471f75cc4daa396c13f2e27ec6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62254235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4b1d959a13b9b3fa164f8eadc04bcfe511a1ac9bda9f6b8fc23e95f40f11bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:42 GMT
ADD file:ace32e845b2ef519c79a725518e909bcbe50ecb496c1dfc8e96fba83ffaf685b in / 
# Tue, 15 Nov 2022 04:05:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:11:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:11:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 15 Nov 2022 13:11:58 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 15 Nov 2022 13:12:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6bf34ac41ed5383f401a5e77ae46b55249a145be0fe8eb1bf8f0e4f7febfb2a`  
		Last Modified: Tue, 15 Nov 2022 04:10:16 GMT  
		Size: 50.3 MB (50311341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc63328347c005d689d25ab87b0e5aaacb8cea5a558a9519592c64723f7049d3`  
		Last Modified: Tue, 15 Nov 2022 13:13:47 GMT  
		Size: 11.7 MB (11660495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c400c7d420ddc4b0c8a6da21fb349813da4cebc3a78a33093be513508cb0ae3e`  
		Last Modified: Tue, 15 Nov 2022 13:13:46 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6ba9f38d1d36d9576b034da95130c6d391569c32a3ae41e0b18a061b8d8c32`  
		Last Modified: Tue, 15 Nov 2022 13:13:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7a77af15eb486abe75cc53404313ad673fd44018fae46e7c6762ca8cca214c`  
		Last Modified: Tue, 15 Nov 2022 13:13:46 GMT  
		Size: 280.4 KB (280392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a7cbc738575cee8991572c3f899c8e84ea5b0ab7d04344ee57935f2e2d824c5a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62259974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ac3d5ba114d40f1972c93e12afe413cd28f512611645eccf1b1306f78e931a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:58 GMT
ADD file:465db2e68facfda9a8a0c90d74ca46eaa4c6678539ba23e8b95ed5245b4c014b in / 
# Tue, 06 Dec 2022 01:40:59 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:07:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:07:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 04:07:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 04:07:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4eadaf994967069fdc4c6fb0c34ba7ff8466eb883bc166d386d6891cfde0d540`  
		Last Modified: Tue, 06 Dec 2022 01:45:23 GMT  
		Size: 50.4 MB (50356726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed6f64ec4652b7c3171c2645831997ab69b35317be6c56a1bb3b4caa4a36bd9`  
		Last Modified: Tue, 06 Dec 2022 04:09:07 GMT  
		Size: 11.6 MB (11620570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e67b31c0d7e5a83a1d975eed64de87d955972ce25a958e31324818cfe53169`  
		Last Modified: Tue, 06 Dec 2022 04:09:06 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd7ec5c16dfa5fc993395782ab3628879ad831177eae3e603b74d413cc749f`  
		Last Modified: Tue, 06 Dec 2022 04:09:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7017d11de64ba4289abd26711c68c33abb56ac774ec33a00329020e01d368ed3`  
		Last Modified: Tue, 06 Dec 2022 04:09:06 GMT  
		Size: 280.7 KB (280671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:68b8fe62a3fe9890c8ebd675559ce271ceb394971204e08bd09644c2ec116aeb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63345056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc42de4ec48704cd0dce0a26facadb64e16529cf38aa94242440e4e7ada4415`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:41:02 GMT
ADD file:0909d182d8916b1b37783d0c3582c9d3f3edddf6cd27e90100343ed0462c9c75 in / 
# Tue, 06 Dec 2022 01:41:03 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:37:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 02:37:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 02:37:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1cd5a2a4c5902ff854cd1178702a69271f9bf768ae5b99124c16b51e5c2d42a1`  
		Last Modified: Tue, 06 Dec 2022 01:47:24 GMT  
		Size: 51.4 MB (51358972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17be3d1436cd579bc8d98f3ffb1ef3f9cc4be510d995ed78bd2da0a30a663074`  
		Last Modified: Tue, 06 Dec 2022 02:39:41 GMT  
		Size: 11.9 MB (11892469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac792060cfa2b70d317c0d7f7b98db4fa37dc750f3305e1113697b77038ff1be`  
		Last Modified: Tue, 06 Dec 2022 02:39:39 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e1f476e348d11b3764ba14d711514789e329e70dd90031e0dab63582a9bfee`  
		Last Modified: Tue, 06 Dec 2022 02:39:39 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258c3265a6bd1a5b1f37b8643e486a04ec9e684278f6c30cf2abb9d512e464a`  
		Last Modified: Tue, 06 Dec 2022 02:39:39 GMT  
		Size: 91.6 KB (91634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
