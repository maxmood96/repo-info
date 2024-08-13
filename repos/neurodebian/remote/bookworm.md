## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:170aedc70cd23f86a79e07cfe881244443f308901b024288e129c051575f4bb5
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
$ docker pull neurodebian@sha256:0da3e2d072a602fc6aedb65562b6c8eb2c9f32c62fce9fd7f31c95032970c379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4a360ac191d5d2dfa259dc87d446570b0d3c15baaef04491f0e4aed52377b3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad183c8b3e3a9f8871698df5673c23c35a92c4c0dbad82013ff7a7a9e91ae0e`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 11.3 MB (11266613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab9dd5bbb30c88662b92c8e56c3d34b5edb303dafc7f29ad99a7be171618c2d`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9ddf544f7b3442b8f4e09584b274a5782a6291b1e323ee48f2ef808bbdf45`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24e1a01d8b12dd36957fa1a2d368dd060fb013e1ab87cb997abca2f333d1651`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 93.1 KB (93125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9a54adf117975620ed244ee1f30b90073e8ec8ba56c2cd8db94953d6bcea290f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f329d7193c18aecca9a1cf6b27cfd7121b4d26db5c4bdefb596abdc52b939968`

```dockerfile
```

-	Layers:
	-	`sha256:81f432ff269dc1a78c67656daffb6eee212e88c40fdb327917ca6d36dcf2e40a`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 3.9 MB (3924239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130e5b11daf010f2e0029de0a5d4f9c3ee0e49c677d22e39e3ca1ab41fde0912`  
		Last Modified: Tue, 13 Aug 2024 01:11:53 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b71cd83d5bd8b0be36b87ea3e0563cab2fd7fdc8fda441dfca994c724878c959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2a5069168923cdc4f70896cc2dcaf93a70115c7d82eaec01f4a07b469d6ef2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c4964b2c74b33113f4f9253f8fdbd6f9effb7070fabfe7998ec7f9f71a68c`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 11.2 MB (11231990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a84d3037e0ebe02d7b2e60abbfa3c50ab185daf05e3e55e3f8ff6cf96a45b2`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784313ea4757f773fd668b9d92e36d3061207f4d5f2fc7c75d857979e14d6f21`  
		Last Modified: Tue, 23 Jul 2024 18:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f51ef3b42547d51fc5c3da2f3e174e60effa7629f2f7e46098c454225497cd1`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 93.1 KB (93109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:757c7bd29e99f08e021102ec7bab71368c08fc5b8dedd1b342098d8ce5324fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd73107a0a9709640c47c4e4f59fa6ca1ebabf8a0658aa9381cbf4bde03a849`

```dockerfile
```

-	Layers:
	-	`sha256:862421904df231d53bf60f81099184d7c0682e30c697de8f23794783ed2daf08`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d478e353d009dfe08925d196921f6845eb6fe158e70304bc9b9b2fb952370c9`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 14.1 KB (14077 bytes)  
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
