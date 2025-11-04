## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:fc69386df37f5bf119ef83293196dd59e80a4792d08d52e437c64ab8dbd886b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6879037c817de6fcd44e5e3e5669da89e8ba81a5efb8d55e046fb7cfa1155c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60161908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5d45b5bb82dce6fc9c4f872667cc486b1620d53b2513cab6da3ab558efb16d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 00:33:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2e77f12282fcde2c6f54d54624e8a7eef59205bf9001d755b40c1e76ea8e3238`  
		Last Modified: Tue, 04 Nov 2025 00:13:00 GMT  
		Size: 48.5 MB (48485640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c43c0422b532d4f7fd4389c7bcce79bb8e16a074d6cb2363789e53874b7bdda`  
		Last Modified: Tue, 04 Nov 2025 00:34:13 GMT  
		Size: 11.6 MB (11583123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704df9e7d2a22ca832d66d121411d6707d4ada86bc43ec80f2a555fa1d72697b`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb42e9230b83fcf84ee0a600f12e4cd26a55217ec3de7dd0c6c0aa252771704`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2947d93c1659c1730f645265acceb08d999ef27b66b5b7f95b9c3823fa6e88`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 89.8 KB (89825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2f35ee62eb9b30a2febc3d098c370d6d0e830d7b7067075dd4621db81923a7`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7d110273275d3a0b927c7c495a117dfbbbbb6b6b74e02853e56c4279a552beb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c438b5523469c0a8d160ad1023753bef5cb1b88ad7079cb2054bb8819965a85`

```dockerfile
```

-	Layers:
	-	`sha256:5954562b8f15d556fd976802885c845f79a74767c4ad3b3c218918e01ff0066a`  
		Last Modified: Tue, 04 Nov 2025 11:09:05 GMT  
		Size: 3.6 MB (3577431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389702f3e48418c9722705566d3d18e849d8d1444d2ac1cc0091dbf590eab8a4`  
		Last Modified: Tue, 04 Nov 2025 11:09:06 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:48e130fd3a3c32aa03d0a2768b47cac94653fe00c02852bea9f52c13ba2c2fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59938919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e45f4e9facb1ca6907f02bd36142baf06f206143422bb34218818416844b338`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:32:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e6429e9e41ca9e14d8856af7a396ce50bc2b9896b4f4cd83c36fd480cd4514de`  
		Last Modified: Tue, 04 Nov 2025 00:13:31 GMT  
		Size: 48.6 MB (48586018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6ea727459d544c8517f0c8256aa0fedcebc648fb6af23c240b500415196ac`  
		Last Modified: Tue, 04 Nov 2025 01:33:08 GMT  
		Size: 11.3 MB (11259082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9af8ac4e367a30a0f111ac0e743568cdd4e5bfa5d7d54d501aca01d1a3f256`  
		Last Modified: Tue, 04 Nov 2025 01:33:07 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d30811e3c51ec44c6a3a5af602fb03cd9579ed244d07f4a14a48b57d498929`  
		Last Modified: Tue, 04 Nov 2025 01:33:07 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4881ad860dbb9016aee3cc5779892b19a2e87de7a876fd0a2cdc004d197ce1cf`  
		Last Modified: Tue, 04 Nov 2025 01:33:06 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246186e66c3a37ef6fd03b09e40ddf97ef52d732a09918e66e3fda666c327633`  
		Last Modified: Tue, 04 Nov 2025 01:33:06 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa87ac3b4e56d1bbfc35a9e5af42aa76a5a321b219af7edd9177a076ddacb30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3525b0eb3432852f9349a598e3788fce3d01885c6d090fd8d04bbfc8966b4e15`

```dockerfile
```

-	Layers:
	-	`sha256:057302c439195291f1f16521b5f2283e18bfc246a8541b2478b4450684dc0cca`  
		Last Modified: Tue, 04 Nov 2025 11:09:10 GMT  
		Size: 3.6 MB (3578307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc4152efdfe5c56849b62b14de3352fe4dc0777258fd7875529be85a2cfc9d10`  
		Last Modified: Tue, 04 Nov 2025 11:09:11 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:c3fab4fa9ef2cd84bdfd791b0cdc2d4a41c22f90d873cf4f90dea71809f0c3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61637272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf02c6051aadb5284db513d6637e4ba5b536869da5a033f89fe262ecf18ca95`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:38:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:37a822686dc57d9a439e8fe6f90a9020bbd58f684341d3cac6e3e13c68f3344e`  
		Last Modified: Tue, 04 Nov 2025 00:13:36 GMT  
		Size: 49.8 MB (49809007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892d3fb4efe2a3e137aad659f9e65e47845c46362dfc05bc72e794dc3de155ce`  
		Last Modified: Tue, 04 Nov 2025 01:39:04 GMT  
		Size: 11.7 MB (11734755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e050807cf2c0cd74803b8a7acb3e0a4faeba92aabe9414adf78a10fe10f332`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c87cc361f91116017b998780cad41ea0d6555df2d7cc1f06ef61aa5519e9c4`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3311ee8f1fc40c74890bd5bcac1450256d6640b97d8f38ef6cd89a603849651`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 90.2 KB (90192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f0e7037e9d028f6faa7a5822186818bc2adca9d82fafea7ca41d47a9bf58c9`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7e55f505f925899d82e80d8b2c41f2e678958bb8a00f26f80bc93f422c763675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a94c61d7822dc33f6b22948d79ce5a82743c7b588d101fdfbaf8baf9fe96c67`

```dockerfile
```

-	Layers:
	-	`sha256:4e87a0cc8fb757426409cc233a258fea1c63f39172d90e807f21e239d4204dc7`  
		Last Modified: Tue, 04 Nov 2025 11:09:15 GMT  
		Size: 3.6 MB (3575394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac7bb0e2883695d8a9dc27bf4b5f90cec47a720f2c163d3e1c5bfb39eb5c4bf`  
		Last Modified: Tue, 04 Nov 2025 11:09:16 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
