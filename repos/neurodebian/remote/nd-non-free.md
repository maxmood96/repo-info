## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:790f3f37a60945a425379d9bbf7514dc38a6bde3459cc4fe95d2d2564c6300b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e668949d99fdcaa776069a8dcabcc7f92c06280add74b6d2d44a986fffa458f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9baa11b9e2318de0932554bc6ce85f2b70bd43b4c6f63259ef1faef75e61a3ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:46:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385a8564f579f25f1fa0091862faf1667f9d99bb57eb2d8d7d231e688a08ffb0`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 11.4 MB (11400554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fe6276a8f981a19cd267153efbd887e1960863e79415cc84f633d529be36ca`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f3d40ae033a5792a73f7042effbbbdb2c11e9c80d8e9242cb1bbc60372528f`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511c208cfebfaa8583dca48701b1de701916b85218fa6ca8d48a1ccf959989b3`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 89.4 KB (89383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfc8b61e4dc23cb303141daa73f93b5c3785184d487db0082a1eb1d756342b9`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c50a6fe2698c56337d96ba11f7b43114a0ddc059e6d6ff43299875cb2d8b4d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a4a2e0f7bb8530b6dff8701621957b864d0a23b2ae31c1ac981467dfbfd4cf`

```dockerfile
```

-	Layers:
	-	`sha256:da398cbf39c8fb41c6479f9a87ceb3f464cdfe56c93863ecbd56d3d42ebe1ed9`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 3.6 MB (3561805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9b4303c20ddff766e93d5ff40b68f06cf15ff76fb8dc3071c8f5a7447912547`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6b76a8baa5e5703b782986d03054140bb5f9c51a3f219cd3bbdfdb6e097b48b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60005540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ea7c2561889afebbba75f286331ba1118bdb81f98d193534f48e1183424a4d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:48:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:48:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:48:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f29437b24e4b4586fe357af3b6e2a0cd2bb4523e6dee73c3187fe1b261eeea`  
		Last Modified: Thu, 11 Jun 2026 00:48:31 GMT  
		Size: 11.1 MB (11093649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b2458ad9ad4a37d3870ee0be7b56fffd958237766aa0449ca76f2346e8d821`  
		Last Modified: Thu, 11 Jun 2026 00:48:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8c8f9d3d89dd50d605bacf929e2688267d93bf13ee4564d5dc39d004c7fff9`  
		Last Modified: Thu, 11 Jun 2026 00:48:31 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41c04a7fefd630d6ba41d8dea40c9bbf56c5bf080b069b449f6cfb2690e5431`  
		Last Modified: Thu, 11 Jun 2026 00:48:30 GMT  
		Size: 90.0 KB (90015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0f18be5600368b9aa251fc55917de6789bae5c62a407fac437536f84b7172f`  
		Last Modified: Thu, 11 Jun 2026 00:48:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c6ed9d6eb6d7be9b9b47cb3806493b95923bc062ac7e26b861f609264ac51edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3582581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2245c7f439db7a99cfc8d20357dc097d1272f3b902a7752a9aab0b8d48463c`

```dockerfile
```

-	Layers:
	-	`sha256:6cdc695a05d47bf2586613a897a82ca07f5b1afb508fc9deb9ae266b89134533`  
		Last Modified: Thu, 11 Jun 2026 00:48:31 GMT  
		Size: 3.6 MB (3566510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8984122e7bf9687e2fe6539b0f98adfb683076c15eae433a55c4b06a7e94f35`  
		Last Modified: Thu, 11 Jun 2026 00:48:30 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4c8cd0da45340fc16fe6fa498ab416e5612d234ee5454eed60ef2fbaada4a6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61827691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e041853d010700cdb92fa67e280982338cf0fbcd3ac4e17bb362c4ccb6352ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:46:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a32252638de41825057387ef73b5d4de843fa9726fc243c76636da258263cc3f`  
		Last Modified: Wed, 10 Jun 2026 23:40:40 GMT  
		Size: 50.1 MB (50105399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9985fd0b18c9239f0ab31829976aeb109a49fd849bfd9a60236038042b9bf44e`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 11.6 MB (11629273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea4f4dda4b51b86cdf991c17ef19d9ec22bd23e1f83387c2a0a394af0171e60`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14c15c1caaffdf6e712eb73cd67310f04db2b7f87d96808966faa0f9afbab3`  
		Last Modified: Thu, 11 Jun 2026 00:47:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f9dabe2674a7076fb586746dadf0251dafb312b34d09feedd1acac58026bd4`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 89.7 KB (89702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a8a745ea0d9c0a691481e4260da9b612159d1fbde02376618d61a65cdb6a6f`  
		Last Modified: Thu, 11 Jun 2026 00:47:06 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c64d7bcacbbd0d616fce071f4378b1e5fef0e66a3b2d7ecda1ff220339bfad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc0c1b4b48591db8ce8d09e831614dcc796be68744723ba7f71ada9c5148b78`

```dockerfile
```

-	Layers:
	-	`sha256:61ad8ecc20551e74c4214e7eb23ae8b0f075b0a45a9ce71574ecb7f55ab81464`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 3.6 MB (3559756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f2c487982789bd00ebaf87c0a4bb2e5538523f01eecb2517a960e0f1e6db19`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
