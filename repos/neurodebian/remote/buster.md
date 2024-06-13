## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:edb263dc1066d7f87dd8711aa0800bf1e1580ab43d82f8bfc27aa45daceaa777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:ba6092bf310c54130b9f46a6f86691ba0c1d67ba1ed3d835a162baa99abe0e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61071084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff39e7247fcadbe53c1798f2d1814082cf109cd683049d792a2ce144c674a19`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b27899bf0a8d8b410efed70f01bf312669da6f68abdaa68e5f6c0f4be18b1fe`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 10.3 MB (10307522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6b00f76d19036c95d91763ba410da86a6b529388b6bc37c6918db191c4d98f`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a03af6c7ef2e49ec9931727bfe5db16be273bc730330e78b0fe95a71070db16`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290b61c7a7487f5ecd78e9e2fd987a6b8a7bed99b47685294a58073df804dac9`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 104.2 KB (104206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a7b5050bf51fee196fedf7681cf858ba20eaeb314b4931a22fa50118cd5627e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb76fec206f8dad74637c6e97e5eebcb910647b26689296a58a6bf127b86a09`

```dockerfile
```

-	Layers:
	-	`sha256:e707f48bd06ec7ba36328c123e2d6a1a423ada9711f1be26c6ff2247524bda5e`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 4.2 MB (4215066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79edcb763fb5445281cd87f8155755f08061719948117b2a9a5697f828961313`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 13.4 KB (13450 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fd746e2f8879adaad1070324be21cf059380912535c42573683deecfd8ddf612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59872687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da29b891493a9e7ecc596a7298090ddb62ec08f8f547608f6cac3a8570ad970`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b27aa5e3def1997c89f7bdc1f4e88d9b5b55f9828ac737b3c69360f3981256`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 10.3 MB (10313240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34f3b0287bdf89ea74e53a548aabae1fe03c0146c47bf2c0dc275edc30feed8`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033ef7f47caf7b9ec62046617a97459accb5b59a7cc2e9fd7d3befc1d3ff35c2`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95a1bedd9437d691d7cf490e49ada31da729b4cc5bbff2f97af90bafbe84605`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 104.2 KB (104199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:91a424abc4307bf97a5eb20afe90834b1d3d40de0192a492e59dc8c0554765de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fe1a355bfdf96a96063cacd98766cfd9686624ce61eefcad52ce5c47d6ac77`

```dockerfile
```

-	Layers:
	-	`sha256:28d09605101094cf05fad8cffebe9f3f83debf8f039730924d4ab94b0a8a0b2f`  
		Last Modified: Thu, 13 Jun 2024 19:35:13 GMT  
		Size: 4.2 MB (4215248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f11f26f2f2ec9fc71bd370d9282834fcbb5e9e7fcf66fa6a57b1a89c0a68c8f`  
		Last Modified: Thu, 13 Jun 2024 19:35:12 GMT  
		Size: 13.7 KB (13728 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:a76163b14df3412f9fea6b62101c8a3b3d81de779033ed78e753808b5d54691f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d280fa1db207ab1f86834891883d03e8cb9a15474e5d1b0a8e770440cb2201af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81eb6eaaa2db2f8610ccccd6bc1ba567a8f98b64e095fcaa6ba4dd344f99536`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 10.7 MB (10672362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e86184655aca75d86e8a7877fdb2ec9818923ae12e4ba8c8b6b6db64c0e816`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011c068dbed62dd0e7dca412001239f4d7843c04a22269387f161efac14a4e88`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3508b221dc7ad79957c24ad801f8116269b56190b332f04297e3cd58dbdaf239`  
		Last Modified: Thu, 13 Jun 2024 01:59:23 GMT  
		Size: 104.1 KB (104134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6278e610ae8ff4f4069e330c959564104dc879c91f2848a3203547845a068740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0046e2e2e4e9ca91514877d1878562a0cd2e29ddd3d5ef59c27a594b325407`

```dockerfile
```

-	Layers:
	-	`sha256:a6e587ad4166f1ecbfdcb34af2443207d1ffb170307bc4619c3a3db05fd5eab3`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 4.2 MB (4212312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa44bf7d0ef4d049cb38b1d14a0405ee8ee349b6b306e47e1b41fc87ce50915`  
		Last Modified: Thu, 13 Jun 2024 01:59:22 GMT  
		Size: 13.4 KB (13425 bytes)  
		MIME: application/vnd.in-toto+json
