## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:0f88bd0ec5e17d2cb503f429779d919f272278d590eb14fcc8172dc168347568
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1324249971b25b9e0f7bfbcb4ba4160e30dd14a3aee17827942c6fd196b21c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60938168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e3bed1d904015142866727f1c9ef5b093e2ab3d017858e81fd44ce8e646a95`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de5108429a11f59373651715b9784a49e539ede6e3f805e15791de2362df062`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 11.3 MB (11266565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55dc84dd6d1ef1641e3007a6900bad1f55de89683e01abb5b12c5bf778734be`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619037df3f69df28e13ebdf7c547a7a3edb46499636b2fa8b88ff6600f6bf41e`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f222c14670fcb7af3f8ba4eaa5016da2c015963ac7772601264c04088c585d7c`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 92.8 KB (92792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb0f830d1ccf6969fbc75d17d324667ee498ad683d50f823a83514cba413ac6`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:be881a18320b4f1498b1859437596d983b02d695b68298dc8c55a34c9fafb9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab935771651c8d1921eea385f4395ef910b7bb94a2d465db94c9c38a88b1f5d5`

```dockerfile
```

-	Layers:
	-	`sha256:15c1e7b9047fffe4ee424e2d4afa5c012d873d4f0662e04926797e43b68ecc63`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 3.9 MB (3901779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d38a08e967e42b6ccdbb3163ff5f5f3b750a4689b8b22f34ea9a7167aa86b0f`  
		Last Modified: Fri, 31 May 2024 00:56:54 GMT  
		Size: 15.5 KB (15461 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d618f33d5af2fb31fa36796bfd87f6a8c5170c6f6e4cfa37a82c5037896ff583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60940966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394cffc10c82bc96ff0460638c0e5b4940d173aa5cffc9ccdd2496c4984246e1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9782ebad61654b7a2473c30e527f7a02ef0ff05bbeecddfa2c2a63f5e2e99048`  
		Last Modified: Fri, 31 May 2024 14:44:20 GMT  
		Size: 11.2 MB (11232082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ee0a093ea753330fd619da92cd9d8620723145c8a836f8b74d64edf92a5d14`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e17f23f6fb69d4dea07617d31ead77946fcac635bc98263d0e0edfd62d3a4`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b77a1d67cd06ab552ba0ded4026133eecdee96d5c48543f468b3922517a9c4e`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 93.1 KB (93077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd8147b4588fef5f9141e32cbd7dbba8d5316da8488ec40f6aa5ae93dab2c82`  
		Last Modified: Fri, 31 May 2024 14:44:41 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a8574c6d120f66dd79367bbf464cf086bf7fc57db846e16e4821b635ebe1c89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82e6f2cd6c502f65580cc742a997c0e189ce903ee23cc816fef9f92165a897e`

```dockerfile
```

-	Layers:
	-	`sha256:2ef168679fafdc885aedd74fab6eb619f02fa79603bf0e20ae70ba14840c6e7a`  
		Last Modified: Fri, 31 May 2024 14:44:41 GMT  
		Size: 3.9 MB (3902020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e441abb00e97fa0e0d88299ab5846ddbeb86dfa258473db0c554cd7c5edbf06`  
		Last Modified: Fri, 31 May 2024 14:44:41 GMT  
		Size: 15.7 KB (15740 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7d6c8b4235db55cc82515f58088ffe599c694475bf9a61ffdb1458c09c883ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62386687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4239d56f5279cdea7597ea3479ee0379a5db524731ffa3a8897d35c876429e6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:1e1eac48c9d76a0aa3d81aa037ce0e962b5ddfce3364b10f3586db659d81188e in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:852c9038cb65e2e7439aa662ff4e286f79e1be04afd71b71b373c29c5611fcae`  
		Last Modified: Thu, 13 Jun 2024 00:42:59 GMT  
		Size: 50.6 MB (50602447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ffa67f849088d881ec1bd3050a216a615ede2edb4a511728ab5579a4fae22`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 11.7 MB (11688926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d8837ad2608097649f544d67a4577b1866865138f9e8a31b177912f5dce031`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161d8b08f6c9b9bd78b7414abdff21676319fc84d129807f18c1b8bfbe0305ce`  
		Last Modified: Thu, 13 Jun 2024 01:59:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16fdac0c82ae1c1ccc8e105f8f96121d356b25ed71c9e2f32f7b680ee7841fb`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 92.9 KB (92895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad11b88e0c406f04ba1f7bfc5b1e04abf93bbd0bb16200a45f9560e4aa5c536`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:064e42db5fb916ae8be69bc1f8b43ddc7e644e625a376fa6d05eb362ccbf9310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00f6fa8bc6946b7ac2df2495e1bbb4e29e45525ca16dea8af7b9c0d71326442`

```dockerfile
```

-	Layers:
	-	`sha256:4791f9f5accce2cb9c311cea7d28bfda43d210e219ed131cb338a3a4195c767a`  
		Last Modified: Thu, 13 Jun 2024 01:59:26 GMT  
		Size: 3.9 MB (3899700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432c1acfda6da922b96c421befb8a54378dbc7ca4b5d79bf4ffc808a14ddbca1`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 15.5 KB (15483 bytes)  
		MIME: application/vnd.in-toto+json
