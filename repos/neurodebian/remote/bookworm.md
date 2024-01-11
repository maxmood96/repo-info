## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:0c07f5cd547a9596b61e808e04fdb9bd17c6ec831f19ec83f11ed8c940755ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:44badbef7163b1cd798771bf25075521731b0592cb9d6bb67fa09a7245c6319a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61314951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce791bf5903056240cd0d81b4ec7b78f86e6940ff54bf4fa1b6921d2bfdc396`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:59:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:00:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 11 Jan 2024 09:00:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 11 Jan 2024 09:00:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c2830e0bb5b6a97105a49aadb136e003a060fb62b739edb2ee97d789251ffa`  
		Last Modified: Thu, 11 Jan 2024 09:01:37 GMT  
		Size: 11.5 MB (11463774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbf2ea8d7457566f0a53fcf4ade45ac67f164afafa4236e70fdd56b9c39fad6`  
		Last Modified: Thu, 11 Jan 2024 09:01:35 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8ed5c622141e1999a0d6d593464b2a7c5935290aad007cbf8796f7c0f60c34`  
		Last Modified: Thu, 11 Jan 2024 09:01:35 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f26d14150a8c46c65a1060c65c83068030d72236f1e5f18e17b138417c5d17`  
		Last Modified: Thu, 11 Jan 2024 09:01:35 GMT  
		Size: 287.7 KB (287676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7aa48c81d0f258a1cef966cb5b04d310d6b48d4beb65220f463ddddf4adc5504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61310112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4912938f4a8b7e5023dc2a582b1c301c017cc4dcf843699cab6ee19962c935`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:15:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:15:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 11 Jan 2024 09:15:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 11 Jan 2024 09:15:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba51178b10e759cfb9d6b784d176976cc7fe6e7f4849aa1de13a41bc16bca109`  
		Last Modified: Thu, 11 Jan 2024 09:16:36 GMT  
		Size: 11.4 MB (11427566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac037574514d5558b1a4004e4885259e6cb9b7d26bfe821144adeef7bb01ea0`  
		Last Modified: Thu, 11 Jan 2024 09:16:35 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac0fd12c52d3c8e62d6390793bc42a75dd17fcf4a9d42fab08ced67251528da`  
		Last Modified: Thu, 11 Jan 2024 09:16:35 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b6c7d52f21d871bdbf4315629fddac80d886c8c5a39fef7e6724b6a96a637`  
		Last Modified: Thu, 11 Jan 2024 09:16:35 GMT  
		Size: 288.3 KB (288286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:ce136ff7e171f321942fbf3bd4dada0c0a94eec130bf6e754202758efb1c1519
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62755696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599e47a22997b7afa85b05ad83ad929b4dac8b435e98446607622484c4416456`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:28 GMT
ADD file:c7cf48f483b7eba0a82956c5ef1a1c78e84c2b91d0b9cf17fdfde5b756fcba9f in / 
# Thu, 11 Jan 2024 02:38:28 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:27:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:27:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 11 Jan 2024 09:27:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 11 Jan 2024 09:28:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:348e22f3afa19ef4ed67af4c0a3dfafe2c1311e99bde0b9039be46cafd8069f8`  
		Last Modified: Thu, 11 Jan 2024 02:42:53 GMT  
		Size: 50.6 MB (50581977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01631a61ea8fbef5315f33c75d82725c2f3267c696bd185147a1d39cd36da8`  
		Last Modified: Thu, 11 Jan 2024 09:29:30 GMT  
		Size: 11.9 MB (11883718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1f7a26b5d54e105cd7c303c41699a158843bb8e6e9ba5bf36bfba6dfc35062`  
		Last Modified: Thu, 11 Jan 2024 09:29:28 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02c8f8cfe1175fc3a0ee098cb37b1570769935a702f667c35eac5af67e7be1d`  
		Last Modified: Thu, 11 Jan 2024 09:29:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c65525c0dfb2025ea40d018649ccaf788bd785d4696d76d97bcf29833a7f528`  
		Last Modified: Thu, 11 Jan 2024 09:29:28 GMT  
		Size: 288.0 KB (287988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
