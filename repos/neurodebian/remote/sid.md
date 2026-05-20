## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:d7ba43baf5310e8c3f0c94b93be9d680773a3b10f016e7ecdfc6bfd16e9b5e7c
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
$ docker pull neurodebian@sha256:40c77bc9cd15c45e56f92dd37748f65dccb5c9b25db474e5583299263a9a84da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60197651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91559e8c87c582c15bc416fbe03a5bbc5f4a584a24489ce55920c37298af5235`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:27:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:02991db6507c0026c404c68dc35ba4f9c80895d9d7fc4576cc1507337d1b4eb7`  
		Last Modified: Tue, 19 May 2026 22:36:41 GMT  
		Size: 48.7 MB (48712012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e58d1748e5151dadb72e1f165353c365ea3bfcbfeab0aa145d1b087b5d6f8`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 11.4 MB (11393325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b38bfcc5e625cbecc79aaa8b01e5e2d5059f226d6eb13898b0f437bd891e76`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e14b8ad488bc00575a9c73515d031181675b31576e3eb72253c6c475a0ed9`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7e3b6d7043fe182d56ec838ca1ec702b85b90778102555a622cd76f574beb`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 89.4 KB (89412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d847daa249197059f5e935dd19b4ea9eedf33149ed7e48cfe007c15f2309cfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952c080329812ec9363845d75ecc38cb4ac235bee430008cbde7fca8be845388`

```dockerfile
```

-	Layers:
	-	`sha256:66bbb59a3adb62e0ab6fa91117f8718bcc512e41d0ce510cd8df380040bf908c`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 3.6 MB (3553364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f5b45df19088a13691bb334527d8caf74b958c6ff741123494348b8f7f40b50`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:edd8534702838d10c4423132ede211ed67cb3b8aad6e0d66635e99db9a0f1062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59923588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdb84dcbc65ca8290823468d8ddcd2d3907e5ca3a931aaeb8b7de01ed7d468e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:31:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:31:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:31:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:31:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2bc0682b6790aa6b6a3a5a7933e32ea4a35d72d531a3c53509cd76aae83fc88`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48737609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8326e665e37dcddbb4117e65487a3fe42cad6dc654d0685797e71d08a81f41`  
		Last Modified: Tue, 19 May 2026 23:31:17 GMT  
		Size: 11.1 MB (11093058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3eea31e0306f1e7f62ba1545e5336a5b2882bddb05be08647685007419562ab`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8105a082b1fcef71cd46e3265f9493987a9fde8724eb7eef0c0900a25bca33`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1517d5423bb99fa782ff6a0604859e368e373d113f8ed534219ca5a9b438dd57`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 90.0 KB (90020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c7701d7e0a9709d5816ec7ea634a4e09304ea19f8f039720e6abe4353a1076aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d10534cb5a776d3b454d297628278677c6febc6e889117d2a786fa1624ab64`

```dockerfile
```

-	Layers:
	-	`sha256:65821c57772256a43a3e64aa43b60da3762a2de794db20f576d83d048cceea1d`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79dcebfbf845b6b95b62872c6707ec89579e790e83597c63c3dffcf4fd69e0a3`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:73ba3061222d6c325c0a346e63bc504de41f9532e07a59209fa44e4519dcdabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5af2eace4327f02703f432d25d547b430da3ef4030f8154d0d4dd1322459e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f0c0878f24a22f4bae1cce2bb33ade2528e750968c7f19e4683f865ecf624f`  
		Last Modified: Fri, 08 May 2026 19:45:28 GMT  
		Size: 11.6 MB (11625846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83aff980bc85ff5b2ce155faf54e6e3fbf0412fad6b9b461726d7a94f49ec8b`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1690741b56c00af9a9e027b2f45da2d3c964439f6016d2a01ae49e540c9a138`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403996057114e2cd0d36ee941960ee517faaab068e8e0cbc9de09e96c9223a56`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 89.7 KB (89717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ab1c10a7c00e20030be43916af676fbd69ea524a13a3d1f1100bc9cad07f30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df6d819178bee19b394bd34bd99b9a33ff2d758ed51a85705d80ba78362451f`

```dockerfile
```

-	Layers:
	-	`sha256:2890089b6f33dd50ea7d84ff7f43fd03e40b52a12e2925bb4cd5456bc7dd9b0a`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 3.6 MB (3554180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27aea920f78950a42d40670e7327c30443ef99b9d23d92570dbbee1e83f95701`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
