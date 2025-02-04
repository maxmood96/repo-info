## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:b095c651f4e0a26e3c337e04a407070b1a4473cb190a52f701dd54b81ea082c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:46e197e29b09ebdcf8b79f5d4243b7a2ee38de58322e566005687311f02d432e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33417662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63727e014a8b319207be5c3696e3f62c7f30f85182746de8fe5e457e4f26522c`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7437a2bec487e56640d2df97d10d20c5d1dfa27e0e438784633ab110ee53ee36`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 3.6 MB (3559073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bad12c5f1fc20ee11ebf084c7dd8083dedce42a054f7436d654477679aacaf`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec5188e249edf8869e827975c795e8ded14ec5f3814f04ca3c0265087ffb7ba`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617193eaa6a7126b5d2fc3b9e53bbe8c8e36f7cb2b96b13a4a83f55dc3b9af41`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 101.9 KB (101904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a3f3f74ba19973d7a055cd89339fd42e1201d6087d3579224e3c2537d82fc7`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9d45065b62fdb0cd8b64cf598efb96e01258ca787ac6de734ee33575a975525b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2006124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdf6861efa175af6d5346140760fb5dfe8909b8d400074154e6b41f1f4138f4`

```dockerfile
```

-	Layers:
	-	`sha256:a8c721ca171aa98660eda78e17b0b52c586d2d79b6038943078d2d88ca0308d6`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 2.0 MB (1990234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008fb6819e6444684199e2d580536f6842848264a696ed06435ef17f187be07f`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 15.9 KB (15890 bytes)  
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
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
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
		Last Modified: Tue, 03 Dec 2024 06:16:00 GMT  
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
