## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:9916f35e29dee2c2881beba0a9c5561f1c36729376eac3d05474e6fe8f610100
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
$ docker pull neurodebian@sha256:171d7790834ff2dace09d75d17fc095f5e0ddb5a64ab2f2c6c20e979b8283e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58950607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed02da4e0059860be250a87aa0f646a80a9a97405ef1de79b37b13c9eece8a43`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2d149d696b13b9c3df064cbc77767f81d4635c7804547d50ff7da0c45c51990a`  
		Last Modified: Tue, 02 Jul 2024 01:30:17 GMT  
		Size: 52.6 MB (52634573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eeeaf4645947114337f3365b9e426c0269613f7bc3b5a498de5bfa2dc9f7d9`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 6.2 MB (6223730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bf23babadbd7e24e99d5f11987ac80999f65bba9925676b393344e7ee94208`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa10af556b8d2d97b814bc8adf79194667d8c4ce1a5024278442d4737439c5`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986345555fbfc0e18521aea6d42886d0b779a81cfe975e9eafc9ed31256d946`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 89.9 KB (89931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0757077789f6773bec41e3ee672f0542a27c2a763cadb11bcde5a56e46ba8dc1`  
		Last Modified: Tue, 02 Jul 2024 03:20:08 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73c2c384861f8818e86257a5bb7c489fe6c75e81009f7d36a5c4787a097dd6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be47e1f771cae7b74651749d34cb0056ec051866bf7e66c883ba536bab0438d7`

```dockerfile
```

-	Layers:
	-	`sha256:174f706621926c8028ac0797d12d9ea16ffd1a2a33d41ecd5081abc4d2df9679`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 3.5 MB (3543004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04024201415ee292c1e9d968a7e8f25fb4fa99f389a1ab14070d733a890e3448`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:afc79c7055d268b7a9421be92cad87792fba1ad94968d4946ccfbbeefecb0b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58995481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27c47d587fed9542a94257a86bfe482879229c5d5ca96d11ecb73508339da2d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012a9a0c6fc8e14dbae0dd211be74c76a40a0bdfe55e8fd25532fadc68dea49`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 6.2 MB (6219805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46829409c0895984dd0c82567ac3a739a6cf8e121453008052b2e558d75b2ab`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08328daef7cdf76f8df8778afcbc4c476fef35cd256705e6c768b9ce1033d6a5`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99980679ea6d0b863dc5d985d23bdce3df45e1f095ca22b3c2e45a70dbb5f47`  
		Last Modified: Thu, 13 Jun 2024 19:37:59 GMT  
		Size: 90.2 KB (90185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab908a816558985f15055c195cbb0d376fd1c6714e7e54daa161c41e0894a7e`  
		Last Modified: Thu, 13 Jun 2024 19:38:17 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b36a2d46a5120d388857f8ed4c930c3519384b84bd207f5d2f40b62de7c7a8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3566795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02096d9c06f0272564cf0a0bd536a43d85e1ea75de2987b4c6ff82a563329ee9`

```dockerfile
```

-	Layers:
	-	`sha256:1dd93fa599412c7ab21640af88ebae609db25942ee5b55918960f43879886c0d`  
		Last Modified: Thu, 13 Jun 2024 19:38:17 GMT  
		Size: 3.6 MB (3551091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9412b2354d62582e459d224f5786a6e9889640453840203358bfef864104f562`  
		Last Modified: Thu, 13 Jun 2024 19:38:16 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ccd33fe92961585e691320103b2d0f3466709f199056da460ca62cbe0d5470ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60169098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca223e31f2027f0bea7325055c5d03f33eb27502dddac3a3b4213eeb1fa81e7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fcc722c6a8b995b7f273820b7fc927164f6709bd0e428b87e24702a321694439`  
		Last Modified: Tue, 02 Jul 2024 00:44:25 GMT  
		Size: 53.5 MB (53522389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2067d5ad59a2a2d20bc80327b6f6ed28714940579539b9812e9e2f3157973cf`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 6.6 MB (6554505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc9e048603bc334e451f2a2ff1b8b689603b80171d863e44bdb12c8bc7a9d70`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5ed2c6d104afdf33dcc4ddf797b004d5933a8c960beb94d44ab97ea188f35d`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86bcc6164bd435f1f582154cd31a155f0749b0bfc6efc6e88c71e43f0a28937`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 89.8 KB (89832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b3440dcc43323d1971173e19bc352048910e85501abb4e5672519b888b9267`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e2c0308d75c24d63b042d64f6d4ff437b38ead191a1a197adc3d3dc0075bae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93a2eb119062ea2accb8a0e28abf2cae2a404016d635e3fea9a1e8d94f10085`

```dockerfile
```

-	Layers:
	-	`sha256:8de0478d7152d9c9a0cb48fdddef7ec88969d9806b1b0e61fd124ecbe855853f`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 3.5 MB (3540100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efe08c161cbe93376c006e2d9a437eab0416700e73293e4b0d953bcef3d26d97`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 15.4 KB (15400 bytes)  
		MIME: application/vnd.in-toto+json
