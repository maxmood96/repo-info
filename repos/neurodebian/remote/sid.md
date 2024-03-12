## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:51ad8ff687ad3d0864b19bcc5f4c7f72699e658049fcd68fac191ef399f5eb2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:b536a4f64f57799d554aee0b5a0be7cfaf24fb9291a171a6d621056ef762256c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64365491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef4576b711032fc4d2e6cd8ef87b2759de4b274f8683be6604039bb88c58081`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:26:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:26:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Feb 2024 11:26:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Feb 2024 11:27:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2fb79b4bfc9a9b9bc98aacf93eb694ea7d81d7144f42b9f294e4e95e783d1d`  
		Last Modified: Tue, 13 Feb 2024 11:28:30 GMT  
		Size: 11.7 MB (11740332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd1d20f6aa2686e64bc73f8298e8ec534036d891c88437552ca541ba61456c8`  
		Last Modified: Tue, 13 Feb 2024 11:28:28 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4657c66cb5f7dbc54c6de898a2a898a046845ec208fb7138f15ee2dea84e8b`  
		Last Modified: Tue, 13 Feb 2024 11:28:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e883645c227cf89a583f421a0604968dbd09497c690cdce0fc5d6592c33004`  
		Last Modified: Tue, 13 Feb 2024 11:28:29 GMT  
		Size: 286.7 KB (286669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:96f6120dfdae6a06f6da690b989428924dc3bf5489c61d31f729afb91b1c42f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64215851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9806fcf993c81d694d2f39e2305b40747a6ff9508d485ea22f329a86ce25739`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:26 GMT
ADD file:88085ab115a08b9d412def1f9fea5d59c60a8e26965f72639d8199179230cb86 in / 
# Tue, 13 Feb 2024 00:42:26 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:28:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:28:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Feb 2024 02:28:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Feb 2024 02:28:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84e6541c14eb2246826ed0d079d915b03d190721bc05675c66f459f0cc97e40b`  
		Last Modified: Tue, 13 Feb 2024 00:47:37 GMT  
		Size: 52.2 MB (52195661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530d9fa27a5b36a7cb59316d7fe526dc5b251bea1a9f86c165075aa6fe54092f`  
		Last Modified: Tue, 13 Feb 2024 02:29:50 GMT  
		Size: 11.7 MB (11731160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80f670ddc162c044ae19dcb1808e1a0347e7fa4e9baa69b117caae4f075024f`  
		Last Modified: Tue, 13 Feb 2024 02:29:49 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbbe655aff736d787cd9cb88478fb9c3773d0e7f10b679bbb85e5c46a939396`  
		Last Modified: Tue, 13 Feb 2024 02:29:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8305489ee84dc4b7567d41f89b89fd2f4ab7f144aea32d30e8d18605056090`  
		Last Modified: Tue, 13 Feb 2024 02:29:49 GMT  
		Size: 287.0 KB (287029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:a6b32feb2fc82b487e4906b763e694263f5ff51341fe7dda557e210acca30da2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65659084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaffd75781403b1ab2658bba43c64fa50451762158f82f132b8386e0d837d815`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:40 GMT
ADD file:383595e3854ec7f22e8d333af3b6c0a5019c955f674a09a7c4bf1426ec9a661d in / 
# Tue, 12 Mar 2024 00:59:40 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:37:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:37:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 12 Mar 2024 01:37:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 12 Mar 2024 01:37:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8c85e8b663e835053744f416ba1ea5847d00b7b5cb5dac4003e16ea78fe851b3`  
		Last Modified: Tue, 12 Mar 2024 01:05:55 GMT  
		Size: 52.3 MB (52250465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd7555a20337a05fd7e07b812be4ec859e409d73e940c618b561d51894d43da`  
		Last Modified: Tue, 12 Mar 2024 01:38:44 GMT  
		Size: 13.1 MB (13119089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346f3c41ccbd57b4aa7ee1a6225a1cd6555f9f42e5ce75c9bd8d278c46f63ddb`  
		Last Modified: Tue, 12 Mar 2024 01:38:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517da467f152240640a6ae7b9254e7561f696ff1f2b536882ad18e40711d55a6`  
		Last Modified: Tue, 12 Mar 2024 01:38:42 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085187cab94862ed8a7c58d99f66ce66633c6c4587e7c29559663e39680df4b6`  
		Last Modified: Tue, 12 Mar 2024 01:38:43 GMT  
		Size: 287.5 KB (287522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
