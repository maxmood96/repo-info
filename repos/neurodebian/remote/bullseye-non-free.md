## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:8619e94863a7e6120b37060f2e45d4a3e6b1ecc47f30e5418cccbb58bc5419c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a3664b64f74716206ce118015164b4e83c8e03236dd79d6d6b5dda5ca4df692f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66680513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc8ae09bd086d04e8614e6632e92cb0040ca7d7d53995afa40f6ddcc2dc8cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051ad894cb437216f831870be1b1373822e49c3bf327dc19eeffa59b380b69b3`  
		Last Modified: Tue, 04 Jul 2023 13:14:33 GMT  
		Size: 11.3 MB (11310887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e0636f7cda9fadf509bd02965ce7fdbb0b9b5e8991fe1aa99e549644993b45`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ed933ab00f44136821a415459a973f0e06900f15055dde3afc8933b79fad26`  
		Last Modified: Tue, 04 Jul 2023 13:14:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea23e1a729371849451562ad79cc4e373450f1757a674a8e98e16cf17da650ef`  
		Last Modified: Tue, 04 Jul 2023 13:14:32 GMT  
		Size: 312.0 KB (311960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ead5308361a9d838b9d3e134bcfa5c09b2c664c755ddeff7d08096c61ae8edf`  
		Last Modified: Tue, 04 Jul 2023 13:14:43 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c79f16dd43a41a53551f24e44bcab68f7e25aae050b34270b4b6d9d4fdf6c8df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65331200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab45d0d53778ee619fe21002c84a503535d661328def02ebceb9889ffad4bedc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6bfd5ffd06d0d2448c897a82b7da49fc3b77dcd4f516a5fc942f49be8ebe94`  
		Last Modified: Tue, 04 Jul 2023 04:06:16 GMT  
		Size: 11.3 MB (11312924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25050f6c76dcfb908599ce51797de77f55bbc0c4941618d37d9331296e66ceef`  
		Last Modified: Tue, 04 Jul 2023 04:06:14 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb0987a239bde87bfd0cc0790f336bf17fb370dcb474fc40091053db73fc95c`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d44a75e1cb43004c926e63fadb5bc59a19c7ab795cbc8859b3c584aed966ec`  
		Last Modified: Tue, 04 Jul 2023 04:06:15 GMT  
		Size: 311.9 KB (311927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115fb106a48cee105f8bc705681ef1cd600e4ae858f2f6f1f40215cad7c61e37`  
		Last Modified: Tue, 04 Jul 2023 04:06:25 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:024bac8c6bfc8fc3756ad87e1bd83504396ccb407abcbcb13247b75d4e1cfba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68063188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4867cccb166e3bf525588dee87b37cd135772a137c84008d25278eb29cdc5c08`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:07 GMT
ADD file:6ae90664cb71d88535d2be8e87b3a14dadaa5dad7756db4b7c26638d53c55187 in / 
# Thu, 27 Jul 2023 23:39:08 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8de74d843a460b113b2683caf2d7e61b9d0ed2575871f77b575c62d4244922f7`  
		Last Modified: Thu, 27 Jul 2023 23:43:47 GMT  
		Size: 56.0 MB (56040964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b46c6f9717e8bb9cf3966bdd4d267ba624c9553a7466229409d774bc156f04c`  
		Last Modified: Fri, 28 Jul 2023 00:27:56 GMT  
		Size: 11.7 MB (11707994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea5e3ea6661df6d2265934332f10fc4591302aec1dced0508b69411c5d1c719`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8196a0421cc767786bcaa49d5a8ebdd018da2cdf015ae938e1087b45e361d8fa`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66bdef1bf48a64e6e72f78495e8122e243062d7c4ee73460e7f640b654ece4`  
		Last Modified: Fri, 28 Jul 2023 00:27:55 GMT  
		Size: 311.9 KB (311853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a98dfa587a22d76f618fe45988114cfa1854794cb5b7c2f39f42e05b491466b`  
		Last Modified: Fri, 28 Jul 2023 00:28:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
