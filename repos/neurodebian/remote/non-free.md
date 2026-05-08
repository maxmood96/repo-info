## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:7c25850f13514bb5f7076fc80bbef82ca88fa43e206d06b995215fdeba6734ee
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
$ docker pull neurodebian@sha256:fa0a0c59897f568dbd24d22d1ffad43f3d2d486c87b322decf55010e63ebe7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6e757416a31a10fe456fbce9f65637fcd410ae9060094eff8b83d22d495f08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e5ef169f8956ac3ddd8962c7f3ac33358eefd1d409b540f9de34c4124d4f5`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 10.3 MB (10292878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5324f86f94a30d26738538cdcc77789cffc104c7224bf71ffd4f31880bcf978d`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff8367d18ed54d7ef38179813a30136e56e90bdddf8538bd5d9e3bba79031e`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ff0e6d854abd5c8c1d58fe100dfa1ffc15291a14f8ba6667e78804e781dd23`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 90.4 KB (90418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dec1851547d03be0d4ac2b715a78ea782afcc8e622301546cbe2328b38c329`  
		Last Modified: Wed, 22 Apr 2026 01:44:45 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:662b1464f8f9fa2c56d9cf9b316bfc2d3763dd83b9636c49b55af1ad3f4301f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9a0958715426078c5d0edc833bbc12b2940a6f1bbecdea77f2ead608daf66d`

```dockerfile
```

-	Layers:
	-	`sha256:2b4f598d075bd78774768313e704b93fab3addc68198641beb64a73415ac06fc`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15201318cfc195a091a4d18d26e19b91e30563b7e8eb5245d56e2c91e87825db`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 16.3 KB (16281 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:57b13c1e50963a6187b7e20ca9c973fe30970f06aa206a968c81ed3e3aea7ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32a80663dcc17719bc1935a712da2852657de51fc94f60eaaa9ccc05276764`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77348ea04670cc60ed3fd70e8a942379a3a778401a47da14bddddaedbbcd473`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 10.1 MB (10077993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4f986dcc8620c40bddb431aed2820d258c0ba86a933a572cfb5aea1b7c8d1`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484764866e70b0d12ffdf225ed2ef6dc9af0cfbae6d1ffc072bc54f2bbd8710c`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13df355aa2411e3cab96fecc0b4927c1a75301419531a535765c87be27bdcc72`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 91.0 KB (91046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb102d2bb0e4b299a1747924f034d561048a35b0c3ad22fb08df099037f5e1e`  
		Last Modified: Fri, 08 May 2026 19:46:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a7fc429753a5755b5ee64226c7038ce723951b0fe08eabbc3fba8e4a1697e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c66c6f71d2cc072b4de445c3593012348006787233156dcc732fecc292ecf16`

```dockerfile
```

-	Layers:
	-	`sha256:4d3e70240cf4968ed03616db1c20e456abae7c75f133eabd39d8fea05bf2ab22`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac819a829dd4e682388cbb13c01e4c3ee1c2e11f1c959436f84e286ee2fb631`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fff406f046666fb4890c9d913ff9ba736422f2c6bdf8b908cd141bd6b2533580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377248caa6dfe840a39a0840a6918be642ebb10883f356f9bcfcd3b49da05559`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70486075489439e2cd8bc3d19b95f151daa410ec96b0b5ec410607342a763f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 10.5 MB (10467058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce5ba82bfe696b9b1e74d40cfc00fd3f4af6d09d2c28b0c41aa4ff6199d5ff9`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5396f55357f76f8761749a573ebca269a5ca3856757532ea722b50f24c7b5e83`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a642280bee42260dfea7eb3563d5dd6be3c1ee1adad589b34545dccc50afc2f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 90.7 KB (90737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb80dabacc2bef1a453fe4101f563092b2cfc66ed5d6694c1a5b44e3977c5b3d`  
		Last Modified: Wed, 22 Apr 2026 01:44:24 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c5c41f2d533954b0f70e97ce3faf5170feb5b028c3422a65a51b999044ef5687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07e627a3eebcd70224cb60daafb4b40d62d9550259916dc98eaa08114b81127`

```dockerfile
```

-	Layers:
	-	`sha256:648cc1a4dd4d99fca873e35292f97d65299d49dc771c22a38f4660698a9c562f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859385b3b4616b5fda752ed466aa158e53610e52f42c433757a2154725095aee`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
