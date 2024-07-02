## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:27e5d99204405da3882a3bc5af6b5c4ba65c23dc8e9ecf30dcb861db46a1984a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e3bf02662763b1d5eed34c1a4c1b8e3dce143794cabdca3c4be8d0c5dedba8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9633672d57a08f62cdbd025d79d06e31a9915fee95a82cd7fb7f32e772f5e3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e0953de06e1b01ff7d2055b9f20a3ba20a1b7c1b748c5529b5f072d20d5952`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 11.3 MB (11266608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832603be935a7fa29c32943f55bb20bace3e68a72ea55d378d207ec681cfb62f`  
		Last Modified: Tue, 02 Jul 2024 03:19:35 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffa9bb75d9bfce162acaee83c0a0c73659d5290224c0ce3c945a841f43c68b`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509d4b428934a9fbd54daa8f6a05ab55ccf6275ffcb89ff275bf65ad5d986886`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 92.8 KB (92820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677717d1fae198d1b12a8ad6dc403da87dc3837cac5902e3759b7650eac3a07f`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:05990838518fbc3b56779b4bd1c310b7a4ae5b704c480343c6da477fe6882894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77f3904f777bef580a9c2b202de145686a8d49391d8146d08bc7a3c60d4df54`

```dockerfile
```

-	Layers:
	-	`sha256:56b145c5026738fafa379d7efd9615cbee2a070dc428efbc19ba0dbfcc4eeae4`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 3.9 MB (3901314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb50d3266d3f97f7c3f6c15944c6604256404fd2942bbeb309286e4dda2871df`  
		Last Modified: Tue, 02 Jul 2024 03:19:36 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8e94f874f91854196e6076d6b2257915da8829a2dbb0c69fc71c69daf1b8ee7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fb5732480a63ed944bfc38838f7166af4d048cbc08d2e568a1b23dbacdaacf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7927b2dcee59c324d2565fb954b8c435214f8fdeb6bea60c0852e4d9c1689b0`  
		Last Modified: Tue, 02 Jul 2024 16:01:03 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28aec732af5c3c764498d4ea15c9e9a9cfb30997ac2e931477765f8163e09fa`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f03c91194fd4cd000dc5b677f57a4961e7bc5ff7d6c8815b8f729aa564467`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc847eb0d1afe5aebbfbb461b0caae9339fed614b6c35baac60aba3f7208c`  
		Last Modified: Tue, 02 Jul 2024 16:01:02 GMT  
		Size: 93.1 KB (93075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510daac82ff29d856863532c2947e9b7b4b8412958014b7e27b1021ea231433`  
		Last Modified: Tue, 02 Jul 2024 16:01:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8021e1296bb25306964451cdb5141166c468b34ae37368033bb8f1d65aed8ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5e58c1860b53852a190f8de888e8ee2d107ed81b36e6b278e6169323e6f620`

```dockerfile
```

-	Layers:
	-	`sha256:c5dfdeb03102caf3591bb716ffd684f322a5eea6d9de32d2b05adbe0f0760d99`  
		Last Modified: Tue, 02 Jul 2024 16:01:26 GMT  
		Size: 3.9 MB (3901567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdb6da297076341b367ffa715a3be15c6b200ac589dfdbb604dcfb9da878c451`  
		Last Modified: Tue, 02 Jul 2024 16:01:25 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:efb49c63259515523fe8ccd10d2e69cccc919b28b7d019e9ec01ea54dcdf06e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11abf557d49f8f62cb12bb0f00abbe6d2f11a5c5cdd67090adce1925c9de4da4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cf0ac242a3e8035e29b47f122d86973244dee2f1be303a17ff4b0938c482d5`  
		Last Modified: Tue, 02 Jul 2024 03:20:03 GMT  
		Size: 11.7 MB (11688947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4332763d9633e70311cf57bf761078910fc849e2a62e3e4ddff60d9b01c7009`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7a762c898e69a0d9a80b3d2b2a66524cf758c0814f0b0f1d26a28eb5e5103a`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f764619c52a862d5c56b2e868e4f339f49c9456df8469c5f8e9f21f6ff7594e7`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 92.9 KB (92908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da9e058b6819c454d94409d52846b774b660804f0e4d95cb2370d94a3f56ee`  
		Last Modified: Tue, 02 Jul 2024 03:20:03 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b9fc7157c7288d7c94e2b56229184ddf05d77f7e6ac1a03a3e6e755e66805e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9a603113a72528b543d99a038c8ae5cf497833a1667db080ece5b7db83a9d1`

```dockerfile
```

-	Layers:
	-	`sha256:f8cfbc339e6496e89b256cd214b6f00cb1703ffc7269a8d5064a68da0dfe20f2`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 3.9 MB (3899231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a0024b48cc8c7bca0377f145743883b2cce1a49c5c8b64afb30495c6131988`  
		Last Modified: Tue, 02 Jul 2024 03:20:02 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
