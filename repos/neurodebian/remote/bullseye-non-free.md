## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:b568765dda1c8f75d89bfb487c2b63706f9ec53b4371511f73183eacba1af1b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:132037d5bed6afc85087f1c3bceaea5ab38dc0a60d67bb18be0e5e541296be59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361a62c5d109622bcccf51c35ecd19608bba94d901620b44f78e05b6c87782f3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205b46c6d980b5d149bfb3561d336408e77938927cf8e6738b9917903de0a079`  
		Last Modified: Tue, 10 Jun 2025 23:39:33 GMT  
		Size: 11.1 MB (11105048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2f38841dc3a9f76babfe13bec1e7c8864b9e924c522990e82854b1322a104`  
		Last Modified: Tue, 10 Jun 2025 23:39:32 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ceb617bc148dcaeeb9c7a28476263870764f4a8ba9f67604bc6e954049765`  
		Last Modified: Tue, 10 Jun 2025 23:39:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2346e301d767c129000931705ab6d325b8df9c5f195e2b0f08f4178fe75df535`  
		Last Modified: Tue, 10 Jun 2025 23:39:33 GMT  
		Size: 101.2 KB (101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee90b48568a2a7d2b4e906c4a6b3e2c96037735cb20e535eedf64701a81c4ddf`  
		Last Modified: Tue, 10 Jun 2025 23:39:33 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:45cd4fc83e2fc6d43a0619c2da0d8edc2f4b32a2d52c577f84de394647dca198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fe5af5b67fd5a1a06f71075baa3cd42be3d9fb211fa8e2b3708ec835a69efe`

```dockerfile
```

-	Layers:
	-	`sha256:1c7082a4068c6d2d69a870eadb5707dfdd23ddbb1d2b29b42488162eef611fdc`  
		Last Modified: Wed, 11 Jun 2025 01:07:43 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c9377c89b97c6a0e6690269150a432dd5d3548de6f2ded453b3668bb8b0bca5`  
		Last Modified: Wed, 11 Jun 2025 01:07:44 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:487eb6af1477b472784d8ff181842faa9554c439e8997e85d856da04addd518c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63461992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3817313674aec263c667c7c0375e41545695a0ab47e0d412e0f5682d3364587e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3704fbfd86a89305a8a4d0556a88966db2c9ae3b7731e49335164c93b49ba182`  
		Last Modified: Wed, 11 Jun 2025 03:31:02 GMT  
		Size: 11.1 MB (11106051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bcb90956441591df9a1f5f32b74f21a6fc4b2efa523a109f5c567befc57d05`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d5133fe164372190e333a26acb1669673c83c44225e9c4bcd48cdc24788087`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473514cac34b3a0a9d0a408fb13bb9096b3c088423448884d4944cb5a73eecaa`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0188df129a5bf05e4b7d7533b4024832da46a201a61f52c17a0cf7d680e65239`  
		Last Modified: Wed, 11 Jun 2025 03:31:12 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a76706f966dc23953b81d64372eb98fe5052592f72e6e09b34695ccda17de03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61429672d72dd0b5732c11f9dc1438caa35574e43a6edb429b227ff111c4220`

```dockerfile
```

-	Layers:
	-	`sha256:1892fd921897d803750a68fa30929929b8dcb565c5e16832c11bc194850efcb9`  
		Last Modified: Wed, 11 Jun 2025 07:07:35 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b4ae33e10e8f64c34ada68d09ac7e25acbbfb8fafab8622bd0f9e79dacdb5d`  
		Last Modified: Wed, 11 Jun 2025 07:07:36 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:dab444ff3f8407e3d4de6e7464a4655ad875790900a34472f880d4e134da8956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c818ad8397b6c6f378b2abd3ddb05d8383ecf0f90ba3ae27456b4481924dbd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1090fea6e28262114514910f5324244b4e2120957a41ba4d90e810aa74026514`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 11.5 MB (11500323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2ca97cb02bfd5ce55cc8e7b0881b53d52e5f1d615486d799f6b98d796664ed`  
		Last Modified: Tue, 10 Jun 2025 23:36:42 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3de78fa3225601752ce238073a7a0ff14b28dfff3036bec8c45136582470c15`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213ff5cb26b6544c857ea46597104ed49ec345e4f0d63ce5f67b479e813655a2`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 101.1 KB (101068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ced5d9c6980068de9c52da53fdd251cf15cb35439dcaa512d524e8f77d89107`  
		Last Modified: Tue, 10 Jun 2025 23:36:43 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14b2a64479b6355d09d583b6c1972e5e67c6a0015dd49abed2d79161f5ea7749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1964b7a6b0460dd581363d59d30987506200c3259cff7790f5317421e7a75d8c`

```dockerfile
```

-	Layers:
	-	`sha256:0954b888fba7569ad3f903df83458b3b1aca940dab61ad44ce1bef0f6fac2d2e`  
		Last Modified: Wed, 11 Jun 2025 01:07:55 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d416508ddb3b5096d6394d1850a38a6240edaee7625ef49cb254b80a5114d4a2`  
		Last Modified: Wed, 11 Jun 2025 01:07:56 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json
