## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:40d8f80bb72b3aa959504d1bc1c49994e0a4f647b20cea47f6a45e6c0fd52b7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

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

### `neurodebian:nd120-non-free` - unknown; unknown

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

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1c2f14d1fdd839639fe6c436e69389697c8d4a6d0f1108791658e5c18eb971e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61335492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1980da6adbcedd4c36adb0ca2290fc614bdfbadf5cf26d972a13dd9695a82be2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:15:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:15:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 14 May 2024 03:15:58 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 14 May 2024 03:16:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:16:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6b30804fc340c2a4a913ef51f98f961d1a3fa6b50913e58d9970af4dd7e554`  
		Last Modified: Tue, 14 May 2024 03:17:37 GMT  
		Size: 11.4 MB (11429535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be71d7d3b9c9f6e2d93abbb816dd3f9788311fc900fd88b7a58f3af6bc0b7b`  
		Last Modified: Tue, 14 May 2024 03:17:36 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a8fa93742bc0ae81af2e337c5eb4ff5a09652c4c71f1f085174d042db75cbb`  
		Last Modified: Tue, 14 May 2024 03:17:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d587ea86da175bd7ccd502e5a0849f506813824744b97ce59c6e8616271a2f`  
		Last Modified: Tue, 14 May 2024 03:17:36 GMT  
		Size: 290.1 KB (290130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2668e65fcb92ec2ea87414770761b1e97aa9512dc7161ebaa4e8299b5827caf3`  
		Last Modified: Tue, 14 May 2024 03:17:46 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:806f07ff5a388427c1f22c990fa272cbc1f3225d618e9c105cd7ae811aca528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62386651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b472ebfd0f1e250a260cbf98071b70ab1d92e681d4ec4cc337c2ab550ee1a663`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:35709674a3b845511a896af16ea37a6022e7d48992d3198d0760c0c3208fe4ed in / 
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
	-	`sha256:4f2f2f6205661e555e772749ae7fd294fb04fc0d06cbc67a50a11fbb4ef44242`  
		Last Modified: Tue, 14 May 2024 00:51:31 GMT  
		Size: 50.6 MB (50602424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916dd4c93ee39ba270b78432ca8c4749a951a9997192a18c808dc865944db39a`  
		Last Modified: Fri, 31 May 2024 00:57:08 GMT  
		Size: 11.7 MB (11688908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecbd8508ad81d83165fb09364b284e975424098627dd360e2d6623071af632d`  
		Last Modified: Fri, 31 May 2024 00:57:08 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3e397d7c374b236476c37eff3ab5773d24183d94c7683ce951cc4644739747`  
		Last Modified: Fri, 31 May 2024 00:57:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a460dbfa02b2156e71fa507a7797000bb0ed1115ba491fdd0d8a0e6514e1e38`  
		Last Modified: Fri, 31 May 2024 00:57:08 GMT  
		Size: 92.9 KB (92899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b25fdb19536defcc745ae6b45cf0d6de422ad38ba2bff42730c9940995a584`  
		Last Modified: Fri, 31 May 2024 00:57:09 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7117194ab9f36ec5fe19d6219c05121882eee528b7bc1863463a9a13156961f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34ad5550754abbc704654605fc9557b923354d77364fc602e012152f3ea3f1f`

```dockerfile
```

-	Layers:
	-	`sha256:98280d5e38d4aad21a164aec478deadbfad186e49aa73b0ac8f58dae3b5fe84a`  
		Last Modified: Fri, 31 May 2024 00:57:08 GMT  
		Size: 3.9 MB (3899700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:103ff322a2bb5d4edb4d4639972ec9fe467de90e21c6565d2c456b591e2172e1`  
		Last Modified: Fri, 31 May 2024 00:57:08 GMT  
		Size: 15.4 KB (15433 bytes)  
		MIME: application/vnd.in-toto+json
