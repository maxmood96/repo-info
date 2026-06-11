## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:37264e9014e928cf0bfda64869302438443988e6d0b8c9d6005e7f60d6cfffbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:798c059e8dc4c8074ba03a170658b96b1b6def955002bdb1bd5abd315fe3319d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60271205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967f1f20d5f480494e6014001acbc38aff48d42d4ec0ac6351768fd541058d66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:46:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5721d6b62cfc7a7bfa692b95ea547e4ea39b5e2bfe1bd3e1a88886f80c2846e4`  
		Last Modified: Wed, 10 Jun 2026 23:40:06 GMT  
		Size: 48.8 MB (48779274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a95da46269214aaa1d7237827dc71f5b5d8069dfd47fc510bc12bfd608acd7`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 11.4 MB (11399216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb2d7895f6cc503a3c75f0ab087eb2584e6322fc057533fb4e00c0b3b1f4472`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288413eea6b9f9875d894a238c3011a38834b38013491f522118fc98a55435f2`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411295c6069be613044d1319c9f54b3590cdc5e10b3aace199bb072cfd62be68`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 89.4 KB (89366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc95558a2b42225eb9e88d79e8becb9d84ddd839869c67835da9b77b53233ce2`  
		Last Modified: Thu, 11 Jun 2026 00:46:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cc82c554bf9c7436fcda1864d1b7a76221113c13842dc5020f4610325e81ea5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3578572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b68e3571054ad0151dfcb082a8a66da630e7142baf98899dcc74e926c517fa1`

```dockerfile
```

-	Layers:
	-	`sha256:335aad9da067ca64dacd08bd25766189ee283be0697c324e298c4d29de9d600b`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 3.6 MB (3562614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929848b26f9d1ea5e95bdd50689a4efd60d82cf1efcfba8397db62fc8458812`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 16.0 KB (15958 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c2fffa659dea9ac21c972d44d982d9e92fed478e02cea8d27d65902ed0acb2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59982196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca3b0896e8a800b0c4b4953ce852818802be1e08c89be74b5e5b3b28cba052f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:47:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:dbdf5115192d6ba17e54d5f2d3cd16e18cba052a9281223f09caff8a3d00462b`  
		Last Modified: Wed, 10 Jun 2026 23:40:03 GMT  
		Size: 48.8 MB (48795608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521f1c00810ede4b0c96988ae55b20fa413409b82a6e190d89816b03fc5a765f`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 11.1 MB (11093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3426a165d11ed3c48c1235f57c55e908c0038c6711048075e2f52785512761`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd26e10e2b3776525cd5efaed604687ef1481c14bb311ebbb49825f60e5ccaa8`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca93d601b6a3978a4bbc3b5591aede6efdf93a3ddb432a1761c30cbf0be0a3d`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 90.0 KB (89999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6e5214750a7948bc5252a9accebd4699c3c518b3fe689bceefde2960613b2a`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f94ce78ff663c717b15eda02d399f935a34aa0c328854c686ab9e4ab00b6c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341c8dd593efaf733c616fa33b61fe15cbbfb12102bc3f1d5a289ad3b9afc664`

```dockerfile
```

-	Layers:
	-	`sha256:815740f746f6fd00353b2cdf9ef1b64be736b95fadade3c0760410e8b8492e5e`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 3.6 MB (3567319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fced8e5795241aa8c06ee963dd4d74b0a962b1d76f736a720db51337099821a8`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ac7573e1a964cedc92762f1764c74e516f1ad3746228ed0c08651568cdee1c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61799181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fddba0f6579ebe47327071a3618c0aba6177f33aeb4a8cea77ce865ae3d4f04`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:46:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d6a4be7a6be3ed3c4d92863f22edf1e7aa21046c79f8c96f534040141953aff3`  
		Last Modified: Wed, 10 Jun 2026 23:40:24 GMT  
		Size: 50.1 MB (50076810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b472a6d8b7727a486701a1080e4d0e8b17435c83bab23bd2ec2b916a22b5a7`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 11.6 MB (11629359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056b0eb9c4e41949da3ec5420b12975ae7a0907918f66ccfd3a65482da204979`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a07b7219afe18068ac7164b86637e0a1dccb746ed0acdb1b0278a72d506c09`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615ed529cf578cb6a5ab9693f16045ee70cd90a54524463364191b5ed9c2ad2a`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 89.7 KB (89662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde751c374c1d4871c1deed9148e8dd53e68ef7ea748a3ec4e9e6159cc6cd128`  
		Last Modified: Thu, 11 Jun 2026 00:46:44 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b041bd8f4c37b1374e71d2e430366895c2266d010e122ea2c8f86a72be2b3cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4077abd8c2df574289455d03f7a6c0bbd1a5fc03a069961dc263bbde41be797`

```dockerfile
```

-	Layers:
	-	`sha256:a0b3dfec3b714a0f3659f3df8424dac0141979ed49efd25ed4e92a8d5461d602`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 3.6 MB (3560564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a422575041a54c249ce448c1da2996daaad5e1140dcf52109f78af6c2fb992`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 15.9 KB (15928 bytes)  
		MIME: application/vnd.in-toto+json
