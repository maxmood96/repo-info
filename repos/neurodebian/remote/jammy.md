## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:92998c4c5d81e049df56f5890828db1584b68d253e49b764d3e59d53e6fc25b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:082741104229bc5d5307ec00e18c8f0e1b92d9ec3c0d18af7b8fd2da303d5fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33272494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e26208fe4fba34f21e765cd213d0f4c4a40dbbb8ffa1e78524916b9b61fe65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2e34da2dc37f3eef61c15e677301ff9791b8f8f70f26fc479ec4d012ed513d`  
		Last Modified: Wed, 02 Jul 2025 05:27:50 GMT  
		Size: 3.6 MB (3624101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865b016ac2b42012c3a60696e045822e8d422cd29395baa864a7750882c4831d`  
		Last Modified: Wed, 02 Jul 2025 05:28:08 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cd7d87cd4cd2188a43546187d892a77babe87c7bcd43debfaf69196d95599c`  
		Last Modified: Wed, 02 Jul 2025 05:28:12 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cf12ea66c74872173d9ccfa48d1080fc8044a3c8c9bd394e42aef1c7181445`  
		Last Modified: Wed, 02 Jul 2025 05:28:16 GMT  
		Size: 110.5 KB (110529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e0eca4a2f8c5de61848c772c9ef1a28487cc1c88c4504e2d616b6186940ce062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5154015829843e5eadc330b8f1dfb807434bda45074d7881987814d6df084433`

```dockerfile
```

-	Layers:
	-	`sha256:83bfad6ad8349036754358056739fd70f033a0c9071ab4468f016e43222b0f1b`  
		Last Modified: Wed, 02 Jul 2025 07:07:27 GMT  
		Size: 2.2 MB (2198304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588008c9ba816410fe986bb801cb8cc7612f36a539781b2e81047f79dde3e244`  
		Last Modified: Wed, 02 Jul 2025 07:07:28 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a43a9f5cf2b5a6919be93498cf5e14d07d6136bc8978e4fe547f9ae25e0669f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31067642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b929f546c7741727f1b32663b03c90e2455044869615ae7a69cf5d8f770349e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c5693e3ea902ddf9017fc917526111e4b850b883c94049575082a3813eafbc`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 3.6 MB (3595659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6817bd2e46a1e80de24744eceb3b542bdd1e58f2e0a52074aae33b6191465470`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a819b02cab05dbf414b013d4dd4f8a294a9bf8274c20f6be6614d19a5aeb796`  
		Last Modified: Wed, 02 Jul 2025 05:59:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dcc8e65b8099a3653adfe8c17639bdc3cae90813cac88317d52213709883f0`  
		Last Modified: Wed, 02 Jul 2025 05:59:22 GMT  
		Size: 110.5 KB (110530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:90637c4bf53ebcd381bf66f747337a22bf21290b659bee3c1e38bd4ed575e90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434a6ddbe1f0ad866bc56aa49fce5ea510ec7f5598a330fecc7c11b1e7d0625d`

```dockerfile
```

-	Layers:
	-	`sha256:cb0f6dc44507091129ad6235df76d8506eecfaffe65b952b1195d241880821cc`  
		Last Modified: Wed, 02 Jul 2025 07:07:32 GMT  
		Size: 2.2 MB (2198564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4706ff6aa3b2ec92170560336d9a608877d30135ca5b534fc9740b80c4fac917`  
		Last Modified: Wed, 02 Jul 2025 07:07:32 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json
