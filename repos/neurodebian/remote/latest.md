## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:7d615974d7618624acaf024c794146f6955178920e4a11205f0b463c1a903434
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:48409e2266289921f625e696fd82ae75b3dc7d3429568e904bccb3046e022dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e982b441ccd68e375ce55850b6f2530e35f89c4a858bb75344fd7a5dded7d5ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603e83f84352e4d604d1ebd2e7b11a116e1d73c815b1f21b71c35cf4d26a6adf`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 10.3 MB (10293033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9841317468747bb9c4d672ac9e22fdbaf7467995b3009c013af9504275765`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97afa150b5dfa5f4868492e1872f0bd5d68742189b24436efcc83edb5b863ad1`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80469e6eba86735ca23d5fc2e8e6e31019a42fe3e7a96b5d2580cffd3a1892ab`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 90.4 KB (90409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93973523588868a89ea7a3048595fc8a05179b43bd1a791ce32770712d00e9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3739871772f9c6753eab2831cf79f90dc38c2a6030448f67185547885e75dffe`

```dockerfile
```

-	Layers:
	-	`sha256:48c1c93d4580490d300f49739cf9b99e4a0678b32abf78a80898f5033fa0cc82`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a980516244bf1755bee0e5c4047d7bd22a6645fb62f256893244939631312c4`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d503ee17e4a04127673e873eadb5e238338d8534e69de76f9a2834dea00068f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d388d64eed3a472d75c0230a0f7e0ec18ea76b7a49cf2f265fc7b87ba9fbbad9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c629af507dca062ea56f93574fa391e844b4d6e1b5cd11cad63be92b46a1d6`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 10.1 MB (10078011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abab8ca898857514fc5bd463e6e97a767bbca2cb8aea60e359cd6acaaa15751`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a787e0f5c6e783915e7fc9afa550e0bcf87b812188a88bfe09536d428841b0`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac226701451e2fd232f7351b186bb36b4f7e1742f26e18192509106d28c45ec3`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 91.0 KB (91035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dc047d2f30ed6ac4ec61cc1afcc3087048f8b38a8af931444118db41c4d4566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfb1e88be3ddf79970c3f161eee07195b0acfc24a53e5306704d479fd7126a7`

```dockerfile
```

-	Layers:
	-	`sha256:4d576367898d58cb2af04ebc67ca27c1a684572a74fe8c3a8c3fa9d91bb20031`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349d03efc82e58b0fabaeba13d01e95372d1322c71cdcb42706cd4ee07d99898`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:674b7f113ab98f457c90a5407cf9fce5d326c1ada9d335c3bb736dac15df1d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd893df613b6c8c15a740d7cf4906096d1c477af22aea43f2c1a7965c5c10b95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918b15ce42e2f43331d7ca8a6909c2f318788178997f3be2a6c20d15686eae08`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 10.5 MB (10467078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d8c3e17a2f821d9a1e4a647dd71fd281974066ed12286ff5344c3c70918add`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745c310d83150426f135a032fe18cc82a8e5631e02d97a07354f8c9341131d6`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d13836b8f7a1419799c27ce5e5586655df8273d6004aaa0c492b5a99f6622d`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 90.7 KB (90733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e4dfc7f492836cce5f36a3a8e3941b8d6619c004fb9fb3e8a3df42c8c567950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1911b218b44e62288fb317f239ec58d54680252b6ad5b7b84abdeee0eff2adaf`

```dockerfile
```

-	Layers:
	-	`sha256:b35285063f63c97ca1e2f1b58a75539e178f06a4277ff94135e31ab43d844d97`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be65c44927642dbaf0443b5d950bdb2eba7e045ec2186605bd5528701cc1ccdc`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
