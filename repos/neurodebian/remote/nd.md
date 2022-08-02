## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:378fa43f964900dda4097c6660f5deb65b461d3d116166753605bef56dd9f7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:a08912361fc206b666ea92bf1beed3707c9ac016f71bfc02626917773477f26d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65176639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12509663902bd0d11806584bd2f907efd1a4b0490a0d1ed2a084a3e7aa8b8380`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:52 GMT
ADD file:8f3d1b2e7474fdc04cd1135312dce29db677e5567ff094e59c8338f5bd2465c5 in / 
# Tue, 02 Aug 2022 01:20:52 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:13:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:13:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 05:13:35 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 05:13:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:180517453f08358cf15a4972d7eafc4c2c649be2333940572c68856727b63bdc`  
		Last Modified: Tue, 02 Aug 2022 01:25:57 GMT  
		Size: 53.2 MB (53231560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd26774dfc2ca7add988708222d2ec5a8b271d124e8e613900b0ada08382418f`  
		Last Modified: Tue, 02 Aug 2022 05:16:34 GMT  
		Size: 11.7 MB (11650791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb26443561962761c21137e43dad6d243b32efdab5a5c5d702106976a9a9121`  
		Last Modified: Tue, 02 Aug 2022 05:16:33 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e59c400bdc10a6a8a04c00284a7b955c197a22f38a00d3c68eb104884dc862`  
		Last Modified: Tue, 02 Aug 2022 05:16:33 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132581afc4cd2fe14fd2f06def237abc733161ee4b2971d15f32a850fb2d3746`  
		Last Modified: Tue, 02 Aug 2022 05:16:33 GMT  
		Size: 292.3 KB (292278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:298d06f9fede57c37c75a2a15c45e367cfc4bf149b6b161348973624740271ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64856469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3ba2c11ffb710e401d30c92bd6e56a7d6169bb48780f8039be0ce102939a6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:38 GMT
ADD file:477966410dd9e274b01740d7af857db5c024b4c4e53a5e83b5da6854d5b0c209 in / 
# Tue, 02 Aug 2022 00:41:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:09:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:09:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 04:09:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 04:09:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:17bcb8e39c7f35480d4c2e5b46b6c0a58dac180206453cc49052707aa8053632`  
		Last Modified: Tue, 02 Aug 2022 00:48:00 GMT  
		Size: 53.3 MB (53311787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b23f22c8c00046bbf67cd59cd4f2af07dce5c5fa7a24ab5543ae0bb3564f4aa`  
		Last Modified: Tue, 02 Aug 2022 04:13:49 GMT  
		Size: 11.4 MB (11445839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155e679260259d507584bee8d944d898d1181db2db8ee4e81b619ee20fe55dd0`  
		Last Modified: Tue, 02 Aug 2022 04:13:48 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe48f40923db8199277d01e875d32310e9fc5ebbf9e02ea16c1397f9c07f2479`  
		Last Modified: Tue, 02 Aug 2022 04:13:48 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707dc6bc4aa4606f4136b46e3735effc8020caaff4770ef7e70e7cfdc6946bd2`  
		Last Modified: Tue, 02 Aug 2022 04:13:48 GMT  
		Size: 96.9 KB (96860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:ea8d222e2497026e9af56e804e43766d8135a02f16342b9f8f931091260e7d1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66183017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a112299439cd007b9ee1127ba5649c3c41c5eed23b5c0f65e1285f89eea676`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:33 GMT
ADD file:f76df7d0d2c0977290a0183cbc4f62656ab20d04eb0cae4d075fd31ddf9df8b4 in / 
# Tue, 12 Jul 2022 00:40:34 GMT
CMD ["bash"]
# Tue, 19 Jul 2022 20:10:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Jul 2022 20:10:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 19 Jul 2022 20:10:21 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 19 Jul 2022 20:10:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b7f5437d02adf5c6ebc8b31ebf7b4950c58003a838e1f6591ce754472a3bae43`  
		Last Modified: Tue, 12 Jul 2022 00:47:20 GMT  
		Size: 54.2 MB (54207595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cceee5781c9f099fefdd78893e31a26bd41859246858d435b15f686abc95d1d8`  
		Last Modified: Tue, 19 Jul 2022 20:12:43 GMT  
		Size: 11.9 MB (11877644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f601990e08e4e6b453747a5131289362248b1b66a2cf312e00428a6249a293`  
		Last Modified: Tue, 19 Jul 2022 20:12:42 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419720c8ad79105df57e634617745b4d24dfe22ed8055b5feec9e0375c63e978`  
		Last Modified: Tue, 19 Jul 2022 20:12:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad05b2cc3252576c38611644a853bba061eadb0faff6e2b261a0b63024ac2239`  
		Last Modified: Tue, 19 Jul 2022 20:12:42 GMT  
		Size: 95.8 KB (95794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
