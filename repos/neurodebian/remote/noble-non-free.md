## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:59016cc49c2abfc881a3b7f98272c830ed6702b068e3793522e63aea1de703ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:67d3460643d6b26642406b01ceb9fc59c13a5d81cebb8e2e236091782d0bc89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e663e38b1ea80eb82dd0de3b799e8cc8de027247ac364f751d674fdff895817f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29805511ed58135c0cced999bd142320069a543e7cff17820e8850ce00ba67d9`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 3.6 MB (3558831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5beb5ddb9eb8c69b9e51380e1333941f9a3383cb298e38c08ce1da1560b752d`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d288e9927a5384721587c8026d993fd091363f600d2c85c7d71a491a54c19b94`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84d58661c2356672d5d22061624f076c4d9973587b3fda3a1fdffc710b3713d`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 101.6 KB (101613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfb151160d7106e163f969786f632abffbcd12e2addd8a1bb2065a701fb8a78`  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:388ad092ea4c672ffd86a98ec7837c638279e8131dd255ad16585091b1f17732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24755e2295c3813efe4eb005ced93eb41d9f3d212c725d79b577a930735464f5`

```dockerfile
```

-	Layers:
	-	`sha256:7f9c1aebb86c594c8832946485244dadee636144bbe25e29085eb0cc6d4e0eca`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 2.0 MB (1987233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d438d90a9e8992acc29bcca44911e036312b25385ab8a97f18d2902139fe79`  
		Last Modified: Tue, 03 Dec 2024 02:31:19 GMT  
		Size: 15.9 KB (15889 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3115bcb5eab088a991b0972bf07c6ab93b32a8106bae583c3b87c63fb59f5bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32555089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c92f5f1dd1ef10ea3757500f3a6a9d0363b5b0670f49b869ec33f67f84c0b03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c806577d234470cc5e1375c6c84e7102c2e92ed2f155ce9a119a4b67e98f9e3`  
		Last Modified: Tue, 03 Dec 2024 06:15:50 GMT  
		Size: 3.6 MB (3557863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5dc9f05589119104912fa1a1717ff92659e13dab1440dc6b266b58957e5ee8`  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc2614b4bbf71177097aa4d12c46d11d7578598e10aa3592123e9463cdfb0e7`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2df2b4e0bcd2792b731ac676570a2eeed647f45c932ddece55a8243a41bca9`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 102.2 KB (102155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285d29c45e6ed67911b928eeedda3837b4aa0fb0c4f54c6b1fc3cc5b80539494`  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:962a5986a3ecef9ad02e63677ab36ae8aaccb2752411b758ed8b69dba956f914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b395745909e449324cf5858c545fe8d7601ab6cec875cff3c6529d80c36754a5`

```dockerfile
```

-	Layers:
	-	`sha256:266eee23eb9f7320c750bc0576810f902ecbd111643a9682a5f89bcf08049865`  
		Last Modified: Tue, 03 Dec 2024 06:16:00 GMT  
		Size: 2.0 MB (1988278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9676ba9bc0661d12309280a6c4a0b4719091d811cab7dc686ec2953c8cce7ca4`  
		Last Modified: Tue, 03 Dec 2024 06:16:00 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json
