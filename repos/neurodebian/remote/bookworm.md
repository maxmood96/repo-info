## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:86bf16ea341131b94834b82b1fad1be2a4e2c758bdebf6269fb81005493e1440
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
$ docker pull neurodebian@sha256:baca0af0e600d4eb5673968b51b81e3c01dfbd4afc281940ff7d7c6d78ed741e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60918412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f5f8734b677aa4409e1fdaeb2596287562419a627a2047c28b218798897870`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8553aac5ada3d57fa02485752729b218183e391f256b8f556021e4da979429`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 11.3 MB (11266596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0920907450c5815ca556bc9418b43897f0a1b433d9c94fbc6a8f34fc477cf`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bfc646f22c7d6b23dfd43f1fd9e959530e4cdd2d7cc1466d873115d272717e`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5000c71c1b18acc1de1ce7d26b6d2e3b79868d9d487afef3e6c1fdba6610178a`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 93.1 KB (93124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2b8934708ecf6bbb786c047f9cbd663c371f1bc651676f2255113e3098c85c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c8695a09f10ad91087d1b0ee82aba1f221b3092ada8d8c9f9448a07dcb75e2`

```dockerfile
```

-	Layers:
	-	`sha256:c4d3094a41db65375f15c2e76db9bc8bc482af824a6a9a64abb0222a0ba0ce98`  
		Last Modified: Wed, 04 Sep 2024 23:10:41 GMT  
		Size: 3.9 MB (3924239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4124a58a47fb482e249defb5e353787cf657769d362036433e95e912192179ca`  
		Last Modified: Wed, 04 Sep 2024 23:10:40 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a1cb3b5b67cf0e33740eab0262c450d59e72b86b395d24c8d3a9f168a289b6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffdbe3d5fa71ad63f7f9ce991223af396c40a9156a0e8c62e855b7bcf88d251`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6516de16487e13fd76db87360111809c44b836a1dd673fa8de93b983583728c`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 11.2 MB (11232114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6108c7a663d245cb0932ddfae87f92ca3e1de7fecebcc1c63ff8508adf4e6db8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08a498a3c3c4bf8a5ccf542b868e62921588d0f25c6cc09bac0d6a005711aa2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e20e8cb909fb4d46a63b2053a3a0c458af529d893341a678b2c4b75796cb9b2`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cb795a0975baf1f75ee1ce62b377c40aac3dde2c15d9e5c6b8970685714a2510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0fba90f7da7dcd6b439e7ba720e8ab181de5d8193ac16bd8c915f30d4e63f2`

```dockerfile
```

-	Layers:
	-	`sha256:f48d7ad43d43e6852e3cd4b617ff75b9f95e9ec8c998d37041fe7d0e955140a6`  
		Last Modified: Tue, 13 Aug 2024 07:40:33 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb0c8dfdbaf13211fbc6bbf2d1f5e6a0992ef2ef16cb8a437b676e1d54898c8`  
		Last Modified: Tue, 13 Aug 2024 07:40:32 GMT  
		Size: 14.1 KB (14076 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:d91ae7a8e8e0a9cd1ffb1fdb782e80cfd9da956bc72f78806584839aec880e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb593a6077e15e3e59d1eeb6e935ed129fded0fb46fe5d39199cd3652ccb7d7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a474c2633397aa8306d1b46ed39eb7746779e75412486f5a38cf877780594f5`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 11.7 MB (11688978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54facb93fbe5b8f9909d31756bba5f2ded7ec557a297888397bb38450bc1eb8f`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fce3b83199534f3d75365cc5b58bc55d368f2ec44856cc75b30160bdd1d8`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5f31329f83d69533edc23d6eeae9ff2fb069d68a6cce9838698cd524b8c568`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f8897ff5043a7750fd4373550d72fc68d1b6d3d82d162871168d1f00796c311f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbe09b244eb3ae159769ad770a0dafc5091e558adfebaa8d5fb67510a9d6014`

```dockerfile
```

-	Layers:
	-	`sha256:fc84cae9d8bf21b3eb9bd59bdc787ae4b071c0b38d8be46234d7420219476b7e`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 3.9 MB (3922156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2e799e06efa1c383ee2a950c88b8103826599d4c0e5fb804093db0855c2bcd`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json
