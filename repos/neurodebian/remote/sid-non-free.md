## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:20227913c7318c94c1ff803b0a5a037a734aca42d03f836ed07f40d46112fcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:446468d05c7e0f5d14c19ced900572b224dd54bf9fcc0a7a7ee3a11cacc9f885
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64410791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fae9644227bbf8e3a487131284af9fb2e53208089a419dcefe03b5e74f0d6e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:15 GMT
ADD file:5df7677e65add6d6a9ff681d686094447da195b4999a1f7cff2192740e38e1af in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:49:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:49:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 30 Mar 2024 21:49:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 30 Mar 2024 21:49:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:49:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9fbbc539fc86b3c511f2260d35b9cf5ffb90638ed287142abafd6e1e4bdffbf8`  
		Last Modified: Sat, 30 Mar 2024 20:54:42 GMT  
		Size: 51.5 MB (51500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9db754ac7589d0093c33a3961d1a053f062bf8f7da86a2e8fd295bf82f7a25`  
		Last Modified: Sat, 30 Mar 2024 21:50:32 GMT  
		Size: 12.6 MB (12620251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108cdb2759de0be751811be1a9ec0a3d5a543f4b709d26eebe254975f89f9094`  
		Last Modified: Sat, 30 Mar 2024 21:50:31 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3989b94ce025dc6c38b95c1c9d6e797f5f70a18f0c74a2be32956a022d73b`  
		Last Modified: Sat, 30 Mar 2024 21:50:30 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae806d0dd4474275a13b633b6599ebc17242b5cedf1846231915659054df8851`  
		Last Modified: Sat, 30 Mar 2024 21:50:31 GMT  
		Size: 287.8 KB (287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf384396e793e84303d8ef0a63a605c1a74415b632011771225bfa0230f6870`  
		Last Modified: Sat, 30 Mar 2024 21:50:39 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f74ad56200bce7b9a4b8584f9378844a61808ec3fc717194e0328b2e0c2e7a33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64268920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd04d913029a9a79b39513ff4e0cf58f010d3ad061f493ee9cf2471d9db75190`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:01 GMT
ADD file:0431bf12596e1a5c3a0d8d282912373bfc2669375b5302333bbd39ecebd1e167 in / 
# Sat, 30 Mar 2024 20:55:01 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:29:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:29:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 30 Mar 2024 21:29:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 30 Mar 2024 21:29:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:29:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:7a4a3e98356da458ec5973da971b31825c760cc233f97a317c13cc7d3cf704a6`  
		Last Modified: Sat, 30 Mar 2024 20:56:59 GMT  
		Size: 51.4 MB (51377212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928895988a645257c9d50e6b037dcab1f9ca0e079cbe4a678c799c33f0be43f1`  
		Last Modified: Sat, 30 Mar 2024 21:30:00 GMT  
		Size: 12.6 MB (12600675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d522086a11870cf4c64c1203c8e0816095e225c68fbf240e8a0ab948692afa17`  
		Last Modified: Sat, 30 Mar 2024 21:29:59 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15936dcd0993f108fc148151704e102a66d016975e29a7bf8b5251379a03d4c`  
		Last Modified: Sat, 30 Mar 2024 21:29:59 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdc194a07f8c65c98f2bbf0817fd0d2ce8dd0571be27230b1c9636578421b69`  
		Last Modified: Sat, 30 Mar 2024 21:29:59 GMT  
		Size: 288.6 KB (288633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf9d8814970f45eaa02f280d3a03ff69973ed42b384024e20ff8b97bb908e00`  
		Last Modified: Sat, 30 Mar 2024 21:30:08 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:c049cabe345df7547337887abba4213d4a0aa7a8aed23021cce3786512d8efa8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65697464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18986172a4bce701c3a94b358d6162cb0f5e303fecd7cf42527d320bcc43109e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:47 GMT
ADD file:5c0cc8b80773608ad255427432daa6a4ea6c6d1257178c16e9fde71fe5f2c803 in / 
# Sat, 30 Mar 2024 20:51:48 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:27:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Sat, 30 Mar 2024 21:27:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Sat, 30 Mar 2024 21:27:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Sat, 30 Mar 2024 21:27:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:4c8e6f721d25b23e18d050c75bbf87b16883b01f37acac5142a881b7006f7696`  
		Last Modified: Sat, 30 Mar 2024 20:54:19 GMT  
		Size: 52.3 MB (52279241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d034e967e57fbe265bc07ea073ed8266258cf8519058f70a52dbf2beadbcec85`  
		Last Modified: Sat, 30 Mar 2024 21:27:37 GMT  
		Size: 13.1 MB (13128098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94aa0d366e753b71410932d85dc328a3a85822b7847c2e6ec2a24549ca771c98`  
		Last Modified: Sat, 30 Mar 2024 21:27:35 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b720efa1dd7998a8f5378b13432325b0d3f8547d217f48a6a71c2833015f4929`  
		Last Modified: Sat, 30 Mar 2024 21:27:35 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd96e3b76bd7c6555aa1d24098f741599986fbea6654e6a8eebebc22f1d8b467`  
		Last Modified: Sat, 30 Mar 2024 21:27:35 GMT  
		Size: 287.7 KB (287727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed766f16fe27cc23c4017646c70760c6ee27748a758048c9696ead39adfba92e`  
		Last Modified: Sat, 30 Mar 2024 21:27:45 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
