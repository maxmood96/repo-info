## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:f1861e0571166fbfae31b98ff9b3282e233f809fa114ae25b0463aab1a19ceb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:af988d6adb2891ec552ee9990d0ed9def1f72d4be51fe2d300fdcafc016069a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59654381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394cd951cd1004584c418da9435be7a462e40a81740e3cf4f9bc52d014181909`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
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
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43fe9fa1ea5e364ff54cf0d2e96455c6f8402592c32777e452028e59e4f07db`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 6.3 MB (6289386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461430c5027f3982ecc44a03e50c617a66caff8d40bb1cf5ef7414dc7a44a51b`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d7d04684bd6207fd3fcdaa7adb93c457ebb7ede1f494ad1050bee39838aad3`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3c4d8af236dc0db54a33b8a382e921a52f482ebdedddff3af00da511fcb5ca`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 91.1 KB (91135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bce5156dc1fb09c732081a1fc7a9e5ea6ae57c5800e3909700a8f313fa0f99b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813c1b3abd826f7630168733dd6ca5f043765ae343d96d62556dfd0539ad11ee`

```dockerfile
```

-	Layers:
	-	`sha256:736401022b618a8c56d8b7cf8c577987243a98a5a24c0c31342af864ab7fb80d`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 3.5 MB (3529844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9e41aadddcdd8e9c307112d89d858cb3da930d97f8730ae366272fa4cb0e08a`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 13.4 KB (13435 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fceb7880ecff05e3fad1bd34562c0fee903764280c693fc06edbbb6b5093843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59996796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0c1c96bf04b236a96d091b001f637f30fc4267568e19ad379ebe0583a99ec6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
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
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207c4d641255ff6bd7b8ce630c8cf947966d1ff05bdf86f951c687f989e2f5e9`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 6.3 MB (6273546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c25f32db1b1126487143c75b9ce0d496e410c5bae14e76068c7767c3979041`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1aa1fca4ed404a2dafbd083628f990869ee0dd7b253df1199afbf67da6e338`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab4cc25b7109f5af55ff37456e9f7fe94f979dff175b36667bc066bff22439`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 91.8 KB (91781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f7c49f91f70d5fd7fdfb393e1255d65bf3963462449605a6b498c5dd601a397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c771ab1f610171f7a17f00660c97e22c04d5fa10ecb778aeed2a621ae3e94e5b`

```dockerfile
```

-	Layers:
	-	`sha256:5e03f04196d30611ce1df27f1d3cc5278240cd13a3eab0cd469eb97f145011bd`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 3.5 MB (3530885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec9935b092fb7d33339c675b1c15bbf6ecc7bdb04d95950c01ed5fca038b5e8b`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 13.6 KB (13553 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:b90f2c17e980947a7b20b3fde97e69b919f586f73c3878813c90846e895b4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60828971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28344bd679e7fa6b7c4fbb3378f9939e9325bab60060c34ac0858e971c02d2ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
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
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bf9a8e67481cd7b5126ca983ff2eb6360719268ef0d901ef9c0ab1397ebdaf`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 6.6 MB (6617928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93a3157ecf2b3e90f14bb799e97539e5da9b8e54c2fa24fb906ee69c4f58f3b`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7faf9478aaf287f3c93ce350f01a65b610825764a68728311533510f3bc121c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c402fe866ebbf8d95ad0581375c4226649ef229de419a9074877580e2287f4a`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 91.1 KB (91086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5508b170e6de67c39a46f664e38e6a6e388809ca959d663ca63d5647a8995f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3540353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c76c89ee979c78363abaee47580b7730e828bd4277b1eaab481c54ca64e02e5`

```dockerfile
```

-	Layers:
	-	`sha256:a08867bfaef8835491bd411c4b001522f5e609221f242241f719262e6ccda1e5`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 3.5 MB (3526943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d525a98f9cd254f377fa72ecbf05fda0d300d7e311a88722b4e21fcb727eb46`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 13.4 KB (13410 bytes)  
		MIME: application/vnd.in-toto+json
