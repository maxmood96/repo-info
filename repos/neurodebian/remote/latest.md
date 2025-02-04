## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:c5fc612aef378edc5040666038d96b6456865d2490555fb269bf8f44f07745b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:8bd205c10b4041cadbd1fcca22274aa5c20d3f8fe27e0084f3151559b97a81da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92aa04dc56cd5ffb266e42ae358943d4c1e7945bb6dbb9e58b140cb2084e8063`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e056c90a35ce47771982d24b7fcc61091633579c7b380027153abf0be8a0d9`  
		Last Modified: Tue, 04 Feb 2025 04:25:11 GMT  
		Size: 11.3 MB (11266764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9445dd973287483622ad8a12b7d57e5e2f428a10bdfc73ee8c6e9147c34b5faf`  
		Last Modified: Tue, 04 Feb 2025 04:25:10 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4366916d277438c5d209ff48314585a3da7a3bb9f83807cdc64b01f8718e9a00`  
		Last Modified: Tue, 04 Feb 2025 04:25:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48255f3195db27485f9d836ea473645348f995806366a70ccdedc9914a1e1f02`  
		Last Modified: Tue, 04 Feb 2025 04:25:10 GMT  
		Size: 93.2 KB (93156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2acba0055d1ccce018de569cb6816196b3a69a4b8bcfe4b5acc04a5c58256f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b6c3f8012c2993eae156a323c9fc1c8e47779b48f8556d640ecf3cf2d4dffb`

```dockerfile
```

-	Layers:
	-	`sha256:15300fbfbfce7eb449496a29da6d1bd3941b01f1a739b6b61b06dca89100add3`  
		Last Modified: Tue, 04 Feb 2025 04:25:10 GMT  
		Size: 3.9 MB (3932810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddda2065e23d3cc71324756f91799b2e22ae6afbadcd2137d261fd2ee0f4805e`  
		Last Modified: Tue, 04 Feb 2025 04:25:10 GMT  
		Size: 14.0 KB (13999 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9b0213975411558e5ff5124fe813fa01e969f3b61934261793a96de6fcc86d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59634659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58ee2b44abaeb8f9501d1237b4acfa3a3387f8b830a1a747609cc7b6a0954a5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63297db49aa1fee77d18a7f692b7b36f85214cbaa7f8a77e111f638aea5edbd0`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 11.2 MB (11232397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30096a8bba85c4ddea6082a5ae4d246978818eb34e1a6355eb305dda4439e502`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9ab318aba0ec0653df3f41df8255bcf221a39e34c2e6e6bcc9f0b537063e7`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986c7651cc110568cd8c25742246a21c09c882a240da263ec1da9e18328d304f`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 93.4 KB (93378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:582a6365dd7c55a649fe64da2292b8564a73700f513b2c894db8b05d2ddc394e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0193816c2ec74a9d601419e17d3dec608b147c586a10965f1ffb2a4446e0ed0b`

```dockerfile
```

-	Layers:
	-	`sha256:66089c81f521c7b2149dd234104a2415cafc3aae704bf0ace16346b43f0e55d2`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 3.9 MB (3933064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a0374552620cd09151c204ec03662c75ad2b547f29e1c1e67debc1b929c23a`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 14.1 KB (14137 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:79d1bdd85f4c92174b4692c5fa24ccbed579e3d2bc786e37bf29be5054709bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61241670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64c03c35c5b760e3ac84db42c32583c0a26da65121199fc1f2a316949fcbe6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a579e05f9aac63ca4c3c3970019e7590d80ce5501672d3e49d5fdb41d6add066`  
		Last Modified: Tue, 04 Feb 2025 04:37:18 GMT  
		Size: 11.7 MB (11689006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3b0996f8a8ff1b7ff9fed92e374ae1898066dd74c1c0f015f58e8572b44bf8`  
		Last Modified: Tue, 04 Feb 2025 04:37:17 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be37b7269140b3ac5298ce9cede45cf4f303150d2cdb777f045726995c7bb803`  
		Last Modified: Tue, 04 Feb 2025 04:37:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477623dabda520f47b66bb3de232104b3780af0600811a7a264bf7f761c75eb5`  
		Last Modified: Tue, 04 Feb 2025 04:37:18 GMT  
		Size: 93.2 KB (93221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:99cbc32013132852dcca65f4db5f984dcdba9520f7ac44f6132bf9b8b680a10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af1f8df8e51d8cb78d1be8451f55cfa330a28f1010ecd692241e2097af3fcdf`

```dockerfile
```

-	Layers:
	-	`sha256:0d022824277e992437b9458b285010a66e628d4a233c21c5914764f1b8d48206`  
		Last Modified: Tue, 04 Feb 2025 04:37:18 GMT  
		Size: 3.9 MB (3930727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52456c3c03e5fe26eba9ed3c104fe103adaecea659499eed4f23ce982b61d67e`  
		Last Modified: Tue, 04 Feb 2025 04:37:17 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json
