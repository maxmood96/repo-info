## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:91e1013098602f6dafa788ec6fb0bbf4bc8040dbc7fccaccc7c48dceb3afb3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:06ee45c19a62857f81219ef6598170155e0f396c747024d67518fccba70da34a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66664763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98369e841a5eb20075d2b09c73202f2fd18e85e402ad108da9cb75770919bc0c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:11:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:11:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 15 Nov 2022 13:11:15 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 15 Nov 2022 13:11:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0861d14a16dff358b570e90c64b95102daff73e74dd0a4029798ba7213b142`  
		Last Modified: Tue, 15 Nov 2022 13:13:09 GMT  
		Size: 11.3 MB (11311648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0dad10036ecd6625b0e4188778610e17f76d43b59d5326fdd018f2f759e5fe5`  
		Last Modified: Tue, 15 Nov 2022 13:13:07 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e8665ed4bcb85c4e58999e96ea9dd2727b6df65b3f8191e9f9796c5441f577`  
		Last Modified: Tue, 15 Nov 2022 13:13:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401616f665690163f32419a45ed91c16c5f287be5e7684426a0b960d72c55728`  
		Last Modified: Tue, 15 Nov 2022 13:13:08 GMT  
		Size: 312.5 KB (312487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5e09019a301c8d3b2ab83f9d5b3afc6640c30795f0b36a9c8ea7bfce84a2a607
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65327354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d5a019f05c75e999786a4482009948d816582f197c3760778f5fd40c290c7d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:06 GMT
ADD file:b1e7652678bbfc9556636e77d79c947ff1436888e2929f9c5c3ddb42a50c1176 in / 
# Tue, 06 Dec 2022 01:40:07 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:06:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:06:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 04:06:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 04:06:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4948a51a9a3f176f30ac619014f4a2da453a943244eacb53096ee9742eb7cef1`  
		Last Modified: Tue, 06 Dec 2022 01:43:33 GMT  
		Size: 53.7 MB (53699146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da28d44e099dda5a3439e3df6b208731c33e42617904d30fc960019094d83999`  
		Last Modified: Tue, 06 Dec 2022 04:08:30 GMT  
		Size: 11.3 MB (11313742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5939d42b5409aaf562108671d59657ecec104e608fe3924506ddfb7b58e9cee0`  
		Last Modified: Tue, 06 Dec 2022 04:08:28 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab68dd460351f87b06f6cb615f0e4eb37b6777dab2ae1f37a7fecff8e48215`  
		Last Modified: Tue, 06 Dec 2022 04:08:28 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fcefb8b25de6520d9278ebc894ccb55b6a83dd81c6665faf9658e5057777ee`  
		Last Modified: Tue, 06 Dec 2022 04:08:28 GMT  
		Size: 312.5 KB (312457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:252bed257500da002dadae357eae51fb0aa113e7e819a0de509ca9feb80c07ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67629654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b822fdf834986427a23abbf6653a3a312872c567fef27b569b4a79507d1d06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:39:34 GMT
ADD file:f84226ae95254e2a6a67086b709477f04fcf4d6c3a6ed05dd9cabcda0156ec04 in / 
# Tue, 06 Dec 2022 01:39:35 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:36:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 06 Dec 2022 02:36:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 06 Dec 2022 02:36:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9be27fc8e6e19a1a3d5f3a8805c7b1a4c21e2db96b34ed6fd26bb06b286b67f`  
		Last Modified: Tue, 06 Dec 2022 01:45:14 GMT  
		Size: 56.0 MB (56022389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d4d936569d4a486991265208b9abbaadf8a75e06c6f7752b32d95767e942b7`  
		Last Modified: Tue, 06 Dec 2022 02:38:54 GMT  
		Size: 11.5 MB (11499952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8ce7b699405989593b23ea2e5a4a73dff9035b7cb044f9830d8e18c9fdb585`  
		Last Modified: Tue, 06 Dec 2022 02:38:53 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5521e090cdb208be8d78f94de322074b88fc0adbdd60c400626d6831351ebf8b`  
		Last Modified: Tue, 06 Dec 2022 02:38:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2dffe1f0bb4052c72c3fe39fc2520f33fb7b0bf37ccd28b8f7584f7b834938`  
		Last Modified: Tue, 06 Dec 2022 02:38:53 GMT  
		Size: 105.3 KB (105323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
