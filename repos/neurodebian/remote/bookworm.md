## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:ec94bf7c865f976be23788ed104ddcba722d2b21b22964883302f3db52f334ee
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
$ docker pull neurodebian@sha256:2b8b12cb107a339fae3a8c5c4f8406b159a03f22fa0ad6d623bd16b49be537df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45016e4b694e24cbc231ee1f05accbb9afb5360d114865d01f0244908c102a2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:33:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d27a9437dd9fc4b0efd290a2bcb6346624c2dd6c60cdc5371306924ff363e6`  
		Last Modified: Tue, 04 Nov 2025 00:33:42 GMT  
		Size: 11.3 MB (11269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663c2d2d90bc6bcc23bd09c4c13c62c2b13f33aa7990a8367683297aca575fa0`  
		Last Modified: Tue, 04 Nov 2025 00:33:41 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae69ff1ea04b61ba0f99224ac7eecbfc020816dc408515a1c4f2687556492e3`  
		Last Modified: Tue, 04 Nov 2025 00:33:41 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a4eb19871be6279fea378987e872d76dfd7c954a44f4eeaccbf2731d02be1`  
		Last Modified: Tue, 04 Nov 2025 00:33:41 GMT  
		Size: 93.4 KB (93379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4958673bc05f2ecf24b3c3560203043ca1923fec6fbb7b3db2c053d9dd09dbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ddc6fe171c2cafc24b32616ca557363933035f42ff5885d8bafd1af458162f`

```dockerfile
```

-	Layers:
	-	`sha256:62ec6d7f7cd447db60df7966ba8b3ab7b7bcfb5d1bfb634ef231de15d7c9c7fa`  
		Last Modified: Tue, 04 Nov 2025 11:07:24 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067da4b2ed0e3bdb23696defb111cddb528d18310e11a0fce4d129f8305c44c8`  
		Last Modified: Tue, 04 Nov 2025 11:07:25 GMT  
		Size: 14.0 KB (13964 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2ebd3557ce31a6045fd165930762376e37228a68ddbb0cd51d352bf839927a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feed7c361f6454d2ebdca20d62eaa0208f7d77fdfbd2113e9ef339afd892a74a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:35:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:35:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:35:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a362910b4ff4e83d0dc3b8613b0eb94658f52d229b4411d4f0253056bb192017`  
		Last Modified: Tue, 04 Nov 2025 00:35:27 GMT  
		Size: 11.3 MB (11253369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d168b3317492e8db43d805d74c95ede9223b4334101713d7afe9e3c3cc93f27`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2ef3a583754a79f1f722a9b9976c108f72ba8983ec4bb24bb99010aafd6041`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edecae1bdd0f4220f6dcd6a59736227d042b109c1ecb4f47723783982a721431`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 93.5 KB (93501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:75feec74e5eac034fa9504f907235aece10e78c0f0ae41090a321ae023ec50fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82ee58d1c3a9e528dee7608a6c72d3042a584b594500f97872e8eec7b2b19ab`

```dockerfile
```

-	Layers:
	-	`sha256:619ddbb9c8584f00313f967f0c11265fe7dcd92403c29673bae6cc5672555029`  
		Last Modified: Tue, 04 Nov 2025 11:07:29 GMT  
		Size: 4.1 MB (4075478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a3294616fef78ed15fd035f53d08d63dc5079f3496cea9faad865804a8324b`  
		Last Modified: Tue, 04 Nov 2025 11:07:30 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:84ec72fe297f615978027618d7a29b7d4fdc7bdf614f6385c71871a006f781df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50834346a5bc41c0b659202fcd7fb0032352323cc91b14829b1accb034ef8750`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:27:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:27:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:27:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f533d2fca7b3ba5eb10a96c4bc300c35df5344af9d94b133311ba535bde1be7`  
		Last Modified: Tue, 04 Nov 2025 00:28:03 GMT  
		Size: 11.7 MB (11690117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b8e2460139c1d8b721f3aaa55562183415fa40d728ebf397973d0b552742ef`  
		Last Modified: Tue, 04 Nov 2025 00:28:02 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da94aa9d44a01d38241f6a206526b15dd27385151cf99dbf2352c5be5e0e4698`  
		Last Modified: Tue, 04 Nov 2025 00:28:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478356a0682b919a8511c7940954eb2b69432f859df6ea178198f69af1b62b56`  
		Last Modified: Tue, 04 Nov 2025 00:28:02 GMT  
		Size: 93.4 KB (93387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f053bcc51d8e520d03d28889ec38e3fa1eb698e639b24714846c4efd00d88bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aeb4189f2d1c01f722245843d4d06eb85d1f24ba7af1237d67e43be1890b6ea`

```dockerfile
```

-	Layers:
	-	`sha256:64c060ddfa2a6c4b6b512af8c7896620d501066922edecfb857aef9154314d31`  
		Last Modified: Tue, 04 Nov 2025 11:07:34 GMT  
		Size: 4.1 MB (4073204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def7727632c070776a3a72db4cf217f26b8e0eefb659bbe3bc34da0dbbc5ef53`  
		Last Modified: Tue, 04 Nov 2025 11:07:42 GMT  
		Size: 13.9 KB (13935 bytes)  
		MIME: application/vnd.in-toto+json
