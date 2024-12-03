## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:978a8625452ab39d13e6a7f02fb3cfd9eb7f71df63e1c1a81c553c61ce2b6514
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
$ docker pull neurodebian@sha256:41bdb44a634f5e4f772e8b59e7a7acd006ddae9b568a2e99b51fb2e2c257ce8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8083ab6daad4423e11c61f0c92526f7aa8c68ed7275722f632c9a567a37d5079`
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4769db03e4d35ea9c8cf75cfe915aed6f030961da59a336f4b4368ca4f71fca`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 11.1 MB (11105088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f91ca316c814418b68c407c49bea3fff42122da0c9c1893c000a54305d893e`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942eeb99ec88bc46a9080bd348da8680bbbb1a8b1edbd7f65059f75d8cd0cce0`  
		Last Modified: Tue, 03 Dec 2024 03:20:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80de4a826c59a53034b00bbe50abcf962f0854836822443071456f042f3ac96`  
		Last Modified: Tue, 03 Dec 2024 03:20:21 GMT  
		Size: 101.2 KB (101187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e891a80297e2f74d3274edf0b1c1de023918624816c8875663815aad0019c7`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7238d490a1ca5d396933462607fbbfb142601f035e62da4c4e3ed979bea56eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f78453b1ddeeb1ce16c0702886fa7638f014a6c09422da188ec507efaf3dc9`

```dockerfile
```

-	Layers:
	-	`sha256:e16018084601f4670cdd8bdfbd363f7ea4d46c886a0fbc2dfdbc68534065644b`  
		Last Modified: Tue, 03 Dec 2024 03:20:22 GMT  
		Size: 4.2 MB (4237079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:589eabc43436ba0627092ce4ea2ab4f3e528dd1139609ee803094bd027690982`  
		Last Modified: Tue, 03 Dec 2024 03:20:21 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5b57e8e5b7dfb431cb05d5d58451cf4d3ee9a357b94f59f83e5b9ac1145bf342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af5264ab433e8d3e3e5f80bbc2d75ff8af4a6193418868592de413d174fa84c`
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
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
	-	`sha256:56f9c61c4532d29032e3956422cc71112cfe60ad7e4ac47495587c0586fa15ae`  
		Last Modified: Tue, 03 Dec 2024 06:16:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d72ce6d5735dec09088eba399b7d1a66d7bd4d6dbc1af841657fab98c25eb3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1d6814225bb1f6e768e113c59455e43f0865dfa5c32dff4a8129ce2f3aa20d`

```dockerfile
```

-	Layers:
	-	`sha256:beae995b856fc77a3fe49b4211e6c69ce9120213835d354b41972d306304b5cc`  
		Last Modified: Tue, 03 Dec 2024 06:16:35 GMT  
		Size: 4.2 MB (4236684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a560d37582a8d74f5745c75dd7ced712a4b381c5461cc2870f7b0e246b42bff`  
		Last Modified: Tue, 03 Dec 2024 06:16:35 GMT  
		Size: 15.9 KB (15861 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e9b7abc0bb54d79a9a24ffc0b81d00184d09f10f0016a5f72d2d693308ec24ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66280058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8063c68d8e3e84d7c47d6a92ddba4264f9d204fc2b35bd2a81bcb84a8ca282`
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b65f3a96293e2cb168b19c54c2b62093b3728fddf28451b6b6232d90e106527`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 11.5 MB (11500368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c264fff16245d2054954a0c0d6a4e94402f127fa2f336a10d500b8c9365f237`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3dc84c047211a70772b4b5cc81d0f696576da04dac87d3c77c6b01c0c40856`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244a01f2463f793685cc01a57b4ce0420d030c5e38b8ce6a00c2f6813328436`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 101.1 KB (101065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb4dfbab157a0690d795d7386cf3563e5b4515abc4011077ce213843cb5c2d1`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:778a60719cc186db2508f107a4bda760adc002211fe26bac1dd1689b74a61152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4094e65772473b512ae8026ab0810de01b98dde7e8abaa654d59d8542c83d4e`

```dockerfile
```

-	Layers:
	-	`sha256:0a3e5db830790c929c589bf59f3b62306f609956fa0b2dd27ecb900bce3324cb`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 4.2 MB (4233539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e526f0f5199f5f0d41d0d602062811cff0642b5963d4c171bb89d35c5135ea`  
		Last Modified: Tue, 03 Dec 2024 02:14:59 GMT  
		Size: 15.7 KB (15691 bytes)  
		MIME: application/vnd.in-toto+json
