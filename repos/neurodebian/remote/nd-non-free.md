## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:d003198606f45d89ccdc4096e03a7d24f32ab53914dbd743f80f2d7ec74cce3b
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
$ docker pull neurodebian@sha256:a86f4de25dfa6b6e91e64e0b6f5d40aedaa1ede6fb8e37582ef64613c19b1b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61734790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc88f1a9c7d540c5d0ded18483a54b1c35d38bd566e529c2d509069f6cc8ecb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:27:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510eda87fd6292dc0e1f9f0e55d72bafc27bf3b6fae3490ebf7da2201fbf34fd`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 11.6 MB (11625786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e78771190378876740c64297e71d7791a44fe070a7d393ec614e250dd891c7b`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a0595dec45a612a498719506c3131b9798d2f5b5909b4127dcb4ff8e4711be`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7047c4ee9b2e983af1985c1c6458f4f8a3b8074315a26585db4bcbef767e38`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 89.7 KB (89678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca8ce972bbd0785587fafbd77eee4417f7e1b6cff9fae89ccec68703c02373e`  
		Last Modified: Tue, 19 May 2026 23:27:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dab455e33202ee0696d74d63c649ac1104d40fe2e90ad3a2e7ecf50d4a94f42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f56c073239f966bc31414fa40751a0c54fb9ed1ed499e8038fb45888fafc6fa`

```dockerfile
```

-	Layers:
	-	`sha256:189d9d6cd49490617375e11667be902783dabc2a73ba55a06af2f6ce1542844e`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 3.6 MB (3551349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:231621bc9581f8c17abcdc788132da2cdd4e950e127faebf5d51ce22cffd68b7`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json
