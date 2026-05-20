## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:fb78a302d8653e842ab45d60c058aa74ea89549dd319d94f4ca7a4aca05ea741
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
$ docker pull neurodebian@sha256:80ab709a5003e5bb19b5298fb94704be677eeacae57e1546f3a27c134e408a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61734334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ac3ec238f09fca3619da6c12e8411fbedf0953b46cb91f86aa5f9046836c0a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:26:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7753854dd3eda9aef2aaa8ce9d1e3f65ad0732a1084526b6ea495204123445`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 11.6 MB (11625732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80680d0e09afe77e520bc718136fe080de719a24960af381889b5325a007ced5`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc9462b033e2edd695c438057a9d245ada5fc84587ca3a58b07feee07ab51`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad603d2e8d78ab42ac28bace917a076937246df7f6d0c0633126b17f0cadb7`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 89.7 KB (89692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:57343788c201a8c001feffcd753e8cfbb1a6dbad640af928c8b65079937916d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583407654d7c95b5dd7f0c49b8cf2c3dda7a02034c8aecaa2c56a63e3009e10d`

```dockerfile
```

-	Layers:
	-	`sha256:d09a0b84829b224ad027b6f9b437d39c2e73c8cdb44870c4ca0bc993869b1c1e`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 3.6 MB (3551313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcef60f7d04efbb4e57e855b92a9b8620465376f9df755c28290b9aa572be599`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
