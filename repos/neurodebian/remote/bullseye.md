## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:fe18aff0849b4e1df68d19c274695dfba5fbb0fdbda98a07358e3385501a4192
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
$ docker pull neurodebian@sha256:98224cdf0cb804f50833ffd343c2cace4d0620cc88d868ceb1cd6c3f0b1be796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a7eacd89d2e958b8a3b6aef1e1fb0af72893321723ca18a1b85f80c3421cf2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a11ff2a1535c8fa479a7c320a495994c3166965074adb19749bcc81e94a236`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 11.1 MB (11105069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bc8189aefd176e625a1f58b86ef8ef61308725ac86d6fd1c717e9b85da58b9`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b867fc96223e2170f08b1bddac268faf03b601fe9d00b5f0ce2da019d85986`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d8f54f537c07c9a80af694512b8f79eb12644da787978689d518b57ffc4c6a`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 101.2 KB (101202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aabe9a95821368dc3e33ae33e0f56d648947a2b242fdc099a2b34d153e0445a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39da91d5bdeb24c36f8303399cf2fc0e0d4932a1f08f7e211d96ff785428d3c`

```dockerfile
```

-	Layers:
	-	`sha256:803d69e4cc55c299148ef4158b0e946e3807a73af9024011dbd4a65f5afcb275`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 4.2 MB (4237043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4709aab7e44720ade9fd334c8d1c2c7cd35b6e7eda4f7d0f5bc30dc8ba85cf`  
		Last Modified: Tue, 03 Dec 2024 02:31:29 GMT  
		Size: 13.7 KB (13692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:503b12cc63458348913441053b31b45bf94be1d0e08d898aaab1ee73d447c47a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37149593973f1cc0e79d75464579d66456f41879964a0c0f3d2ba14e8d194e51`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fb46d4fbacbba6f0e034e8d65131a0ae5d99a9803eaa1223ca1a1cce020e44`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 11.1 MB (11105958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb47f993ab8f56d97d07ec72b6ec7643575396ff3eb0ac2e06dad8348b99fa6`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabe4213d9e47272af07a9e329e0d77dfd006ade0e3035e1d7109e590c58f702`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd00afd1e307fc6212c5179f04ed778efeaa0b8d1c4d2f1cf0ef40961607d39`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d70b2455f8344e8e8324092bf06f83009f2f80bb01fe75818efb32a56e72b6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f454574e54a23090cf00dba92b65577480a93397a5a6de461e23e64b7a4e8db`

```dockerfile
```

-	Layers:
	-	`sha256:8dffb7f08ef77f3d5388260c476513166ccb0f27812ff4240ee86a096ec9498c`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 4.2 MB (4236648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d72e5d7a074b56de4153dcc7da35221212a240b3c5a178af2bf0a8025cebbe79`  
		Last Modified: Tue, 03 Dec 2024 06:16:22 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:7c5a39a701d8dc66eaf4bf30d54a87c77d1efe5ef0ae96588400f6492cf26489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66279694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cf762d4dd883d16a90d46ee45855b8a8179cc4efbe9bcce674e18a1138a672`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef34bc916fc85979e50d28fbf87a379437236619f31787c6253f9be255cf615`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 11.5 MB (11500365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c264fff16245d2054954a0c0d6a4e94402f127fa2f336a10d500b8c9365f237`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3dc84c047211a70772b4b5cc81d0f696576da04dac87d3c77c6b01c0c40856`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987ef48478380284df1d15d0ce83cc3d2b348177e1967cb6995033830ebca434`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 101.1 KB (101064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7ef6b6b3b18b388c4c6a0a2dfe818b51ddf588fa06bc75068201bd43cfe08813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736fb535b3e23528fa401960e8323a637abd1360e60549f9d64c45929306706`

```dockerfile
```

-	Layers:
	-	`sha256:e6431df809d0774340669cb6df2591eb71e2812dafed6c7c91ed5684daf5da56`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 4.2 MB (4233503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d59b514ee3f01c9758a94082d2709cff01cd42599e7c253880f815b86314d4b6`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 13.7 KB (13665 bytes)  
		MIME: application/vnd.in-toto+json
