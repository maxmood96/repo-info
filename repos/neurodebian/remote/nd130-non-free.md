## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:3e23a92aeecd2290424ae44c5cfab9e52839456490e40bb5b506a268735cb3ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:82e474c2ae8e21c50a816ca8623bd88bf10f268ef4546821dfabcf820e0bf1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59491933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fec2a1fcc57d10ea266a88d73ea6e17c9ecd09671b8c84fff39ae6cf7a2f9fa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb091556b81f4904845d65b2153884d581ad6cbbdac107a2f862a6707fc5218e`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 6.2 MB (6245445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4580af063012cf07a90f4c4deb394f146cdf7a02a156056e6bdfc9c42840ea5`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d6de5a32ceb96497a82ed7c607b87555825b7a60056bada7560264dde688fb`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea057aed6cb485a17c4bc68bdcc1a81cb4787ac1e05596faf20d1bfb1b86802c`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 91.1 KB (91127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f784639f20b4c216890d379aa5486b23ba801d021777b1a6cc9c39255a331eaa`  
		Last Modified: Wed, 04 Sep 2024 23:10:49 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eace15c747f6d6ffced917962585b4c110fbc7fb653d9b6c85a0e23f34046b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe746e3f282968ed6262d9350bcbac0318a90f681615ceff1ad8f1a1694be9a`

```dockerfile
```

-	Layers:
	-	`sha256:01346c0147987859ad6490f74cf8d191bc6fbcb44bcc43313726df86733bf3df`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 3.5 MB (3533320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:390a341ebc9b73743d3a5a6e4b1534734c72b485ad249e8411fd2931a60e476c`  
		Last Modified: Wed, 04 Sep 2024 23:10:48 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e0fccdebbb4c3e1a4c51702d3bcfc7b8ef28c1fdba127fb501398b54b9d97be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59481178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078b3ce0bc1dd7b36af04ddc5cad250a918b6391f24707db77d6c92c9b0d3553`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:44df8bf38e0a6481ddb1093ad0c25ca4508a15c2b5d1c0733757db62627a7413 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8858b14d914bd710ce161898770a04753f6d66b911364becd105945179fc07fa`  
		Last Modified: Tue, 13 Aug 2024 00:45:37 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb7ace09fdfd476fb95d4fd5a8a2edd7a9fdf7565c943ea7c1ee453011b5697`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 6.2 MB (6235166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af976523b1ff0ed7a6ea2d97619433f9e2ed6a36abcae442c116f36141f7c5`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe64922d76d36467a2655a19d8f70ca78b033cbb756a63287ef0050ee43aff9f`  
		Last Modified: Tue, 13 Aug 2024 07:41:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2ce3529f0b82b4882db3aa1ee50dd070dbe6994cf2242d75819e76f0acfed4`  
		Last Modified: Tue, 13 Aug 2024 07:41:29 GMT  
		Size: 91.2 KB (91163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab7094a272c5f55af989aed29e9331e322fde90bcc6e6310d1f9cecf4f1bcd3`  
		Last Modified: Tue, 13 Aug 2024 07:41:48 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f7bc75943597ccf63423e01147b4cd0be252e263339ae1466d4530d5bf245fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311ff9447377aa2faf72ae51c9a8a6cdba678c8bf81924249c2ca218cae908a4`

```dockerfile
```

-	Layers:
	-	`sha256:60ef82002dc4188c276c967733bf3f7dfe6ed10afb436761e28b05f01c47748d`  
		Last Modified: Tue, 13 Aug 2024 07:41:48 GMT  
		Size: 3.6 MB (3561403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b732592ee34b5f02ad33eed797d157f745cb26004c31735bb1a7c10c88fb8e63`  
		Last Modified: Tue, 13 Aug 2024 07:41:47 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:68b54664e3866cc705204223f34e3b14687d203d5d8c4ccb41d48a81f93cedfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60690777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ecf48c44eeb66c35ca0c57c59bea6b4f55484c38154fdbe47d4f5a3a0da326`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6ca0a177e1bacc5298df02655f64b86d9c9b9ef5ac4afddf6bf3b8ffb6845a5d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3fc63360233033ade654647f98461e34e405a88696c8a8470032f9ca8e3d1a43`  
		Last Modified: Wed, 04 Sep 2024 22:51:30 GMT  
		Size: 54.0 MB (54024286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6dbe168d1cbed58c86837c3c4e445deb7290ec698957ef32f5871b9708532c`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bba1583506d4cdbc507d7cc5fffa09a2d9182d563c6773b582cd5a11ddba1a6`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599299994105b13034a726b2027742dfa6c475364a0fb2af06e771388ee88540`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b8d36492ad7711b0cd10c10c8006d7288a6bbfc26cf33de3dbc6b4d8838fc0`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 91.1 KB (91064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048a377a5d58435f09efc2825d6314ff49bb86ccc8095cbdf3c9db7213d852b6`  
		Last Modified: Thu, 05 Sep 2024 00:14:55 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:78656ca2d10386314de4b1fce30ed2e6cbacbe7ef364b24e35c52c26191db06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdadccd02e0062c0e688529e7768b067ed807a1977bd6a231c79fc058c2637e`

```dockerfile
```

-	Layers:
	-	`sha256:e109f57e1ad3ea88bd73422a34f6383337b13ad53168635fa526b691ade511cf`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 3.5 MB (3530418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bf143c4f772bceb5e893f350906929badd77d0929c34a2a5173497b82a00535`  
		Last Modified: Thu, 05 Sep 2024 00:14:54 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json
