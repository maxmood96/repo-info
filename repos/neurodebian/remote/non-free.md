## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:ddd99f9a7e190137380f659cef8a620dc9ce357bd44405f50295d88d02b2fbbd
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
$ docker pull neurodebian@sha256:8b9bc021fb3ea025c8a4caea80f4783f4839b5451e81de9c3a7a6b8e3266a1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6868e6a625948642d085f5e31ba2990f6afaa0d51e204e3a53e13960fd1d71`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:052f086288480e72435d634b2bf07198eb86bd50d8625c576e50f1c86e39f537 in / 
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
	-	`sha256:e2ec811b59a6f77ebbb7b1faa7ee83a70e39a8f7628970c01799c727a412a1ca`  
		Last Modified: Tue, 14 May 2024 00:52:20 GMT  
		Size: 56.1 MB (56076057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4903b1565147e50bff72947b12d1a74bc9b41ed86afe6d2c5010a6067d7ad1d4`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 11.5 MB (11500086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b862731b03a358ff30561b906e6381dd7b6e5a2e2b6658212c9f31941ba03316`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87281e9a3b4c0d00588f26599ef01f9cb268f821a34af340cd347f8c79442196`  
		Last Modified: Fri, 31 May 2024 00:56:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754affb0164f197b6da7f59f0e9f8f8d3b4b94fb67250631ea583490777e0719`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 100.7 KB (100672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a65acb8d006c150593669a5018814f72cd32c18e8ff272e75bb740640aec18`  
		Last Modified: Fri, 31 May 2024 00:56:55 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:095622314d07de012b61b065d9d20ad3362a8e9fcc99eed7ce7c691caea2f5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47127e4993270cbf7d1e481825a1218202784ed56429777c8c6db7560e449bbe`

```dockerfile
```

-	Layers:
	-	`sha256:758e9514d6046f709b6139c70876dc80809b4b36a0b579ab9477821516bc1131`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 4.2 MB (4195537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e36b91c9abad41ca187e1fe4c346d9e1d386ec3ff33fb4e84d21510420f39885`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 15.7 KB (15743 bytes)  
		MIME: application/vnd.in-toto+json
