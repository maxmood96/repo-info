## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:06b142b4d711bcbe195b005e3ded7479e8ac36e7da28e1dcbe3d3e3f0ad9914d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:8745b4739d43041fea2d9f3cfca5c5e72fcfcd7f09ba5e70b6d5363b833d37c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cd179c855f547eaaf62baa8b60401a814378d56efb9cfbe7656a01acb5be5c`
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
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b419c3ff37ef2ac5fa82f5b85314a380bf9dccefbcd3caf5c82f12d45db2dd`  
		Last Modified: Fri, 09 May 2025 17:31:24 GMT  
		Size: 3.6 MB (3623949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ffc54fef5a2d95fbe22699944431dfe32ea22be8fceb724c9a18978e3a546c`  
		Last Modified: Fri, 09 May 2025 17:31:23 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b757fab4386e86d70a5e84a8a4601e713cc6f6daa82716ceb1b547b41edbe9`  
		Last Modified: Fri, 09 May 2025 17:31:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caf4a0206137bf9258208e5033f88f354a90cc40585f68548a934a1413d70fc`  
		Last Modified: Fri, 09 May 2025 17:31:24 GMT  
		Size: 110.7 KB (110734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3443176ce74e235df7f2ec70f48ec7a2854b049c120c10ba5a497ee12cb2ae4e`  
		Last Modified: Fri, 09 May 2025 17:31:24 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:268deae095fe3c5d59a663f99295fd94d9a0b6f4eff5b68fd180dcd72677ec4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd244d65c53f38bc322681b81e82a26034d1932ed27d13d45c8ad73a52211c9f`

```dockerfile
```

-	Layers:
	-	`sha256:d1171e76917a57f087d2c9519be618651d11350d4f57894452eec95304e0dd80`  
		Last Modified: Mon, 05 May 2025 16:36:01 GMT  
		Size: 2.1 MB (2055435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d1503584e01253addc76624f770c194dde029241bcfe7f365cd29333796a49`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c63a127ef850b3ec3c132de842bd669ee2be494083d6bef49ec96eaa8823da47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c555e8be455732f19d45cd584d48a1533ad6edde311a21c8aa9dc5b6bbb2387`
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
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9b9bbe7463741dd05852bef3e20e4918abb3791e642a53459b7d85a0df1441`  
		Last Modified: Tue, 20 May 2025 08:30:43 GMT  
		Size: 3.6 MB (3595231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c9a28db0b9d01ec102aabc19b0194e5bc43f48ed9950e82f9438f3bda9f35b`  
		Last Modified: Tue, 20 May 2025 08:30:42 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebccfe88dcf3d8d97ae8ae10386013782461c92e29200dbef75ff693b974276`  
		Last Modified: Tue, 20 May 2025 08:30:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd85b43d1613815fca29c2e3b2c7ca24988c55da52443184599ad7aa6946614`  
		Last Modified: Tue, 20 May 2025 08:30:41 GMT  
		Size: 110.5 KB (110473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564cfd3215f87ca4868d1e044c8559b75a587d7ab8a81be3104288780e46562a`  
		Last Modified: Mon, 05 May 2025 17:47:17 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea84e072fa2cdb2fb3f2883fc76128e015c6df4df208436e4f62689758261b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a87abcbd2d0153452c05655e838d1d47ee61b4d91a78d94161824743b4c62c6`

```dockerfile
```

-	Layers:
	-	`sha256:1c6ad0d29e8ceab0824b00a9285f398a0305f3ea937b8905d8d097127dd9ca7a`  
		Last Modified: Mon, 05 May 2025 17:47:17 GMT  
		Size: 2.1 MB (2055695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939dda7ef0ca78df8d4c0860a093b314a5dabe7120df3d94b553415a47d19fcb`  
		Last Modified: Mon, 05 May 2025 17:47:17 GMT  
		Size: 16.3 KB (16345 bytes)  
		MIME: application/vnd.in-toto+json
