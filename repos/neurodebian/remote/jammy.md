## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:aadc2821c4fb100912b0a0d2c9ba79b614a0122d76baa24f63cfbfd0c062b184
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:ff397a72c04635a55579c8025e87c06b6cf211530dde5d332b8249d330403d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e39866c7946bcfc6840c4e0c99798ab2301423e994f67a9b59d18f006051ab0`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e387fe46d51819e286a445a33730411d77cc121bdb8d7ac28c4aadd0707c98`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 3.6 MB (3623974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54b7cc7b061332b4a6b548f407a16b338ee39763686db874cb834f2d4ad034e`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 1.9 KB (1907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520ca9bcfad5d90a0eb1962746c00b9e58f7f6a659e1955b030090931a988f17`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d29396d7a0397fad77c5b789679468a4e54292b1ca963c71a189bc1447add1`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 110.7 KB (110735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4fd0a38a8864f58f17eb71d15c509a9af8523f3cce63c9b1eed228223de4b276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4e035ed95fddeccc12432c50e575f8715ba7dff8ea464941082279652f25c7`

```dockerfile
```

-	Layers:
	-	`sha256:5d065183ca637ea10089b70a42744d342f113104e1de406d1984cb23cccc57e8`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 2.1 MB (2055399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fe24312cffe4674cbc61ea735748398745d60cce6907ad9b7499079489cda8`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:46b114c6a25d43df06b2367455c9208520e94efb8378f95ded9fb8d031489677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3eccf9b41da37d14ed42d0a2aa76b82cf032fab74de0b4cae3db7f8106dee4`
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
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9b9bbe7463741dd05852bef3e20e4918abb3791e642a53459b7d85a0df1441`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 3.6 MB (3595231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c9a28db0b9d01ec102aabc19b0194e5bc43f48ed9950e82f9438f3bda9f35b`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebccfe88dcf3d8d97ae8ae10386013782461c92e29200dbef75ff693b974276`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd85b43d1613815fca29c2e3b2c7ca24988c55da52443184599ad7aa6946614`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 110.5 KB (110473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:71f716a084d4d17ddb17637a7f72b7a8e75a6dd0aa10465d31d778990ff99e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ba0ba152a487af6adbfe538db7aa9421d5d5bd70884f71dda994d1b82b5ac1`

```dockerfile
```

-	Layers:
	-	`sha256:bff8e5a61a14d45e82c3c5f84b93a95274e27a52741f7a498c777670e183b4a3`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 2.1 MB (2055659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7103e27570378d3659f9b71c2a8a96c2531f4f5d95c7f33694c437951a1e222b`  
		Last Modified: Mon, 05 May 2025 17:47:05 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json
