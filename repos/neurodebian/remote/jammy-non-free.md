## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:c97324dc5cee79ae5805150419af6a22c0fe79ddaaca717e33357f6520c371bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f65ab94de2b8eeb7ce8e3ca843ba825e9c7fe90ed9b6634fbaf551a4d61fbe26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce894af6d2b00fbd05af4826250646684dcbb657ac827263cc9e0f14b863a70b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb4394bdcefc6fa3b661b40e6eb591c5f4d4a4948bb9f94efc8cfb2cca63ab0`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 3.6 MB (3624440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe5dd49d306503d46bfd8860d908db1bd43054f51630df3cae246cda80ab538`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc8033217859346bf8a7b9a474edfbb809fbeb1a627bad48117b921acadae46`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466de1c292093141aee6e0b2e28cdb5dead9eaa5b899e28405a08326e0afbcda`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 111.0 KB (111028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1816e7a377a6dd0ca7d84582d786a62e2eae934a80a7d10a4968032c0c09c847`  
		Last Modified: Tue, 17 Mar 2026 01:43:52 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3327cf1ff11761f7d3fd4c86c31125e43e1d212147fdd91197fb422bd6610d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42da9986bb0da24b6b98d1bcf5be809650d9e940fa3ccf81026bdeb9108e866a`

```dockerfile
```

-	Layers:
	-	`sha256:044f0f60135fd32871cae06a72337f371a8c9006584356dc984cdd534d47b695`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7e31bbe852e2d1e841c91b37d8c7c1547bbaf7a57650644745cdf4181ae15a`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:394de8222acd546223af23904aa1ed27bf129b9229cd1870d371c159048d9a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51928ab1653f2d374fa511b1c7850b344a4e33a52a58812c7a8ee6ebf75f6a8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:14:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4019784363cefaaa0608f44a7c43404f1b49123f5490bd18ff61d334344dcd03`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 3.6 MB (3604713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac14a880a2f296e4a09554d5f7d84793b55df94e7b4c331567c990b3480470`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7b185bb1d3b8189d1af6df1aeeb5e439b37bb515e3842af0b98424dbe2a5fe`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736213a2d43cf0f24c9174b8fb31963c318bcfb6708f00ace854f394cf5e34f3`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 111.2 KB (111166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57c1c1d3cafd08cbb99d7170a7ed6f9d171ccb1bebae7ca7ed6a66cb514d61`  
		Last Modified: Wed, 01 Apr 2026 20:14:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1c5645de0a996722122f4c9fe0b9ee1feb9f9fa5e235152031b99bd71d3229c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb25718c8f24128797396d2c2b144f786d6ab403adfddb2df3c99adacea0df61`

```dockerfile
```

-	Layers:
	-	`sha256:0957159b9394ba37b209348e8d8a8338cef651a44bbe52536707849659184f84`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8676f87d12d1ed89bca09e6bcafb4093ea3eeaac8b18ba0f5f60591dc4211c78`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json
