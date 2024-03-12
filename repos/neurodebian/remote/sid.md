## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:1fd93c9db78279e04fc0a24c219ffd484ea021c7b72087ab93b1201cb40b6634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:7ffa336b9a0f2e594d1df70ce66a259db156902baa371337a6bfaae2eefa4de3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64419376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb929a86138625d2ed188dcfd6fea6669556cd055f27daceaa71ac51a613230`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:22:38 GMT
ADD file:3a737ad8ab65fe5ad068d6094fbf99ce9ed2b5beff9c86daceee8c2c50182bde in / 
# Tue, 12 Mar 2024 01:22:38 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:54:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:54:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 12 Mar 2024 02:54:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 12 Mar 2024 02:54:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:490d250d3b2798e2c88a398b87b4162c8ca53e579e4e79b47fc41c2c2aaca6fb`  
		Last Modified: Tue, 12 Mar 2024 01:28:23 GMT  
		Size: 51.5 MB (51512918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6023d7647e9dea83c63ecea3c8ffb631949da34cc23ccca6bc356120436fece`  
		Last Modified: Tue, 12 Mar 2024 02:56:14 GMT  
		Size: 12.6 MB (12616880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb219c41d8a51d50281c7cddf719296593ec6425298c6e0018c1ccf9ebafaef`  
		Last Modified: Tue, 12 Mar 2024 02:56:13 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b04c616174b1136ea7358982d663d233c92cecf297478fca88fc2f660f0bd9`  
		Last Modified: Tue, 12 Mar 2024 02:56:13 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ebf6eb132f0b70ebb2b04c431aad4df8563dba424583f0b24a3329525715ab`  
		Last Modified: Tue, 12 Mar 2024 02:56:13 GMT  
		Size: 287.6 KB (287573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3b2e542cabcc2189d3c7df450676235a4b9fdaa70e60dbbeb2f5b3b862d15a3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64235495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00ff4120f68b4813a6b483ee925e28c4fb1dcd04639bfad8ed7cf38bbd8b654`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:41 GMT
ADD file:1202a56d8723ce5bee3f68e3d9488cef88889fe8b2bb138cde766ff787577a7b in / 
# Tue, 12 Mar 2024 00:46:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 04:16:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:16:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 12 Mar 2024 04:16:51 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 12 Mar 2024 04:16:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e7b106821c007c3c67e9a4d248bd2f87194491ad746f2aa752c5b0ba2fca099`  
		Last Modified: Tue, 12 Mar 2024 00:51:35 GMT  
		Size: 51.4 MB (51353263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665e91bee5fc34351fdb601c8ebd8959f6ddbba04dd247c403a413100912d649`  
		Last Modified: Tue, 12 Mar 2024 04:18:20 GMT  
		Size: 12.6 MB (12591936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7147ec58bd21b17451278b4abaa9db077e2f193ba9a9d0b61398a473c2aed850`  
		Last Modified: Tue, 12 Mar 2024 04:18:19 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0a91119e249ef946a8f9bc60d1cce61a74415a38de2d8790d42dddd6f33848`  
		Last Modified: Tue, 12 Mar 2024 04:18:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8c1c7e43cfe8b176eb758a88dfbb5ce4fad9bfc99a01ea75b160bb12e9618f`  
		Last Modified: Tue, 12 Mar 2024 04:18:19 GMT  
		Size: 288.3 KB (288288 bytes)  
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
