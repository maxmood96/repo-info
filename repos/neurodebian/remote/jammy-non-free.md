## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:efdea78c9ceb32fa30b09244de8778357f2127445e395d77b9b8bdae0bd311cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7628012c9ce33421ebe46723882b520d2dd3486af58d6dce9991b9ab4ee47c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33272732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac03db12eb00ddc67da22b7895962536be0140ac04c3e9a4f9717a2127e1b35f`
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
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41093334c179adf7ee2c998856026e656b770d3f0d616be80ddbd03bc0731f69`  
		Last Modified: Wed, 02 Jul 2025 05:29:07 GMT  
		Size: 3.6 MB (3624055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd96580cbdabfc7ae730a6c37534d8de4f2d40bb5504173b4708b34cd6ea5ecd`  
		Last Modified: Wed, 02 Jul 2025 05:29:16 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51be9392f49493c01c7da367417b8308180bf4410543718f8c661ba01829243`  
		Last Modified: Wed, 02 Jul 2025 05:29:19 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67067a6367ccc3c8bb0c66746345fa9bca0a7b36b77a33ab711d0d356bf366`  
		Last Modified: Wed, 02 Jul 2025 05:29:21 GMT  
		Size: 110.5 KB (110533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a9032471d089343a57e88445514c5d8984d3bd4c4bdee7e3a9f365f4ac2740`  
		Last Modified: Wed, 02 Jul 2025 05:29:24 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:afdec840f8c89302e8a1c53cc1fa311c7a21bde6644a75925dcc2cb4625db7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a3a57040ecb9c6010cb2005511b811a0de3721e7c3def314ef05ec028967bf`

```dockerfile
```

-	Layers:
	-	`sha256:3ffce0d8c239d874a3c1920ff688b4f673fffc8d45f6cc0278c101a79ca98edd`  
		Last Modified: Wed, 02 Jul 2025 07:07:31 GMT  
		Size: 2.2 MB (2198340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506fd2f6e007e29edb41b564cd18ef46633fdbaa6d13bae3e7f2248b09f26f3e`  
		Last Modified: Wed, 02 Jul 2025 07:07:32 GMT  
		Size: 16.2 KB (16205 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9606aa5b8ca07ec70c713c1595412fc1b5f58e187d466ff359f1625cafd91af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31067929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31630d872868bec77a1bd3273f93c01e05bca9b7134f48af85f1315d53d2aba0`
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
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
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
	-	`sha256:32962c795559f0f5f00baad5852df2b3dd9c691cc8aef40e9b650305a978f23c`  
		Last Modified: Wed, 02 Jul 2025 05:59:34 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:71661675e1b45bce08c679dd642e959257b9a0855429f18a85b83d2414a64249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7eafe1b7d0d14252b5ca09fe258c6114a61b1b8acebca3b07d979c01241393`

```dockerfile
```

-	Layers:
	-	`sha256:ad1bd99d1c183a2e738e4251371bf379198f16bf345cc125d6f300a2bf2e78fd`  
		Last Modified: Wed, 02 Jul 2025 07:07:36 GMT  
		Size: 2.2 MB (2198600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeadbc25eab435a9430ee266732355ccc2ee87783c480e703b43bae8149e7808`  
		Last Modified: Wed, 02 Jul 2025 07:07:37 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json
