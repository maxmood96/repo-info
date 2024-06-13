## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:388f6c2461bc209a692170f696d1f5ff96615b60c45bc27f86de6f1eef1b9fb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:84219b6ad2c59d4349766f7ea41188ef7fd7f23e797f234aa2fc118476d87a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66307474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00919434e4703f6acd6065bc95f564b675939dc982ac937077fb392e2b545964`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fff6731503f1b1a12f3ec6074982a0a7c9e1faacd14096103760258566582b`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 11.1 MB (11104993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ed83a5d194b8125fc4475a7474d7614f9fa2cdaa8ef76360838fc01af94e79`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87281e9a3b4c0d00588f26599ef01f9cb268f821a34af340cd347f8c79442196`  
		Last Modified: Fri, 31 May 2024 00:56:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52629961e0dfe4a11e23ee3273dfc2941ef9296958ce0433be941e583fd3545`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 100.7 KB (100736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a7775c23e5a426688a89fe8bb88b071c4b67d2c0c5bcfc7762283e0c64a8eb`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f5badf72a6a31f4df91f889b70573094f100208cb79dc40f13ebba462e395f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752e07c04e896d0e9354d9f9aaeea038b337272f1c2970023a1a6c328cfab70`

```dockerfile
```

-	Layers:
	-	`sha256:1c8a56fac5dd5913e2895f29ade5a290d191979513f8716a9f8b6417694c831e`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 4.2 MB (4199082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d009cbb1fc1738caa42c4c5f123155cca5ae8713acd80bac0f8599a98214bb7`  
		Last Modified: Fri, 31 May 2024 00:56:53 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5d1cf82cceda318c0dd41a8a0400d8411edc8a4d51ee0500d5d15b787f48c559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56caf73109cc0abb9aec10f6936d04cff9ecc5e4ed695667363742eb5c0c880`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1483c42dcb365aa70f1ee657cb621d71108a07cb14e7da7c0af1670b1d3dc`  
		Last Modified: Fri, 31 May 2024 14:43:25 GMT  
		Size: 11.1 MB (11105807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bdea9458a37f5e1417a645e4803ce863ee56f1bb909725f8a36979925dae88`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a358d18ad53e6c2f3626a6322cc6c11247f800ae4b985a091f6495eba713135b`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf2eb23fc03995a0b59c27e2f55adfc7906966f111740c748bb549fa4bda575`  
		Last Modified: Fri, 31 May 2024 14:43:24 GMT  
		Size: 100.7 KB (100692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8729b3ff44329714773e4eb7c4046bcdce6dcd6ddc587ddc086d3594ea516b`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9c183078ed2c49b83568bf2f7c05cf59aa86563317db10e1fd35dfd0c4700705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4214766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b2481a942ef60260cd04118ded9798eab96a09d5a9de29130742c9d682bac8`

```dockerfile
```

-	Layers:
	-	`sha256:a8cb3999134b399777bdccdbcfd6a6470c17788e420fd152629355c483c2d10c`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 4.2 MB (4198699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb260b9d6aa6319449c343ab09e6d08a9472f4d08310d1d79af533866fbeed82`  
		Last Modified: Fri, 31 May 2024 14:43:46 GMT  
		Size: 16.1 KB (16067 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:30c029632c96bf37af9b76eb0393927bcf408d4d4637bddf613a7594b2681b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5864c6def933a6b6dd9adfb7a5ec63fd1f46aed4cd44d9bfd0cbe3d67f45c8c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b13addd2b2a32b9d1ff2ea9286439b5540ef92b6f2a15ae59e20801eaeb8115`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 11.5 MB (11500167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925784d52a7a52e17776422204b33b6f319d5ac291eecaed873d7c75d0bf7b5e`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc25404734dead4fcf99099c0b8c4c255e177881c3cf9e4bd15eecdda5bbfeb`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77175288a751964832d472ca502af30d298ab6d18b500e39100c7e2cf1941a1e`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 100.7 KB (100656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403eee5dd3ac973d264d6caf142749476a40597c843100f860fd812bbdd7152`  
		Last Modified: Thu, 13 Jun 2024 01:59:16 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20b1a751fa916af4b95b9306d65f00cc6ede2b46bebc04dd23cc8fd44391f864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bf79df5b568b2fef0e797dc3f58e562b7992622978ab8ae0de582edd25ac64`

```dockerfile
```

-	Layers:
	-	`sha256:5b95beda90bc46a2b778e530d4afd832492d8e6d2ba670872dd2bd272173e02f`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 4.2 MB (4195537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42daf680929d419028ac29504c6aa3762fea17ac4478e351fac146d840b2c94`  
		Last Modified: Thu, 13 Jun 2024 01:59:15 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json
