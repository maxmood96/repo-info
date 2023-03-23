## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:9f47f30171f9141170c99782cd59a563d18f71949bd1933b6444574ef598d6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:afa4b10de84e23db29f6f1b7d6ef28195645f359c8bd6a4e0262ddb6fcc5a597
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61246641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6f356db77ba481cb1de7195e9ed0a895d3b289dde5a5d61a99dcba2b2c8b33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:57 GMT
ADD file:742621d60641957542e01d843bc130e616ba577a7135783b21e53d3a5d77ad5b in / 
# Wed, 01 Mar 2023 04:10:57 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:45:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:45:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:45:12 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:45:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:45:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d80cbe2ffd4f13cce276662ea5b4fa412791129d545137a4bea79fc41c446e0b`  
		Last Modified: Wed, 01 Mar 2023 04:15:57 GMT  
		Size: 49.3 MB (49261286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f07b40e7e9f706f89a559924ad512bd3b0c4f082e17184a96aa7d5540686ce`  
		Last Modified: Wed, 01 Mar 2023 16:46:58 GMT  
		Size: 11.7 MB (11701184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b804ea73e1c67b7cfd483b59108eef0df77751aba531e24ec8a07c192cb6ab37`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09103778873997bf9915a011675211eb2bc00c9e387b1d994fbbf3af88764138`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cb9fe54ae4e96671ce48bdda7ffbe70f0eef14b7e934156aab2e1fae345d12`  
		Last Modified: Wed, 01 Mar 2023 16:46:57 GMT  
		Size: 281.8 KB (281768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06941c2c76256cec7bbde5b3f998444239e34aa3cfd46afe763196c5dcba4b36`  
		Last Modified: Wed, 01 Mar 2023 16:47:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:342c0311e4a3e51c8b6d2ba51cc2626c535413d7bb71b5e0427e14142a2cc3c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1704113e9c945898a8a0d7a241be127649f1269ff7fd5df9e088f5c8510fa74e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:42 GMT
ADD file:56248f74ca6cf497dee2c80a5824447bf5ee5e730a9c092f440d9c666ec1c076 in / 
# Thu, 23 Mar 2023 00:45:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:31:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:31:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:31:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:31:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:31:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:3a84baeeebe4b5ede833105ba5c2fe8b6102a8c47c386cc79b5833fea9489c99`  
		Last Modified: Thu, 23 Mar 2023 00:49:34 GMT  
		Size: 49.3 MB (49318983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0e8bba10f3b5b2432a2b1218e1c8025aa37e5b2848aba78cb30b14c96d48b`  
		Last Modified: Thu, 23 Mar 2023 09:32:22 GMT  
		Size: 11.7 MB (11677082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c996676719d71c02efc60656700e2212d3ad2c4aad1f607c5baa5644790eaad`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f354b2c84f012c8699569e7416cc07ba57b26ed0f605ae146d61586a3dbc579b`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c89a260248440979723f69655c586df9a7be34913dc586e4ccf4a675c842b5d`  
		Last Modified: Thu, 23 Mar 2023 09:32:21 GMT  
		Size: 282.2 KB (282220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbd26fafda5fed39ec26a8d1eec81c16dbb9f31c1a4593db76820237bb36856`  
		Last Modified: Thu, 23 Mar 2023 09:32:29 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6bf1388217fc75201eec1764ecf9ccc9d84becbc1a5c2fff97de123176d113bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62723225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5280e2b5efae98def7467cf9eecfc70f505f631e134aee484003dfdb9202f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:05 GMT
ADD file:6282b025bbfdc732e0b90ff88ecdc7d48b84ec602874ef46e276d0250551f12e in / 
# Wed, 01 Mar 2023 01:40:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:03:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:03:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:03:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:03:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:417b7bc42b68fb696c2efa25377639c22c351f4705d5168da4f5695d53e4ba47`  
		Last Modified: Wed, 01 Mar 2023 01:46:43 GMT  
		Size: 50.3 MB (50314271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee23b5bd34bf02ab736466a576525c5d19319388d1b8a4640648e8d37a616e`  
		Last Modified: Wed, 01 Mar 2023 14:25:40 GMT  
		Size: 12.1 MB (12124585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25463d084e76a8e19e579a372474aa2c1ae32aee022db7c2952d26a2231e5f1`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b53006d31828e9a51a9e14f54d3d3830f320beaa4d3bf60d7c2ec4cf492b974`  
		Last Modified: Wed, 01 Mar 2023 14:25:38 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c3d4f315a9ae18065eba4cd8471c7ace7d5768b7283a38f3c073569847cb8c`  
		Last Modified: Wed, 01 Mar 2023 14:25:39 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61643c2ab05c90ffcc0f8e261d002b4cd8d654267ceadef7f14d5b5f46a05348`  
		Last Modified: Wed, 01 Mar 2023 14:25:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
