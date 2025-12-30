## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:82f76b53bbe4befe34c1cd8c837004b33cc081f9258b3376a8ee0f3463b3ac7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:9df40b0ea9c95868d65e0d4230bc6cf3af140542662751ad4858fc2818faad93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a2827ed3ae4e6c34042eead78d08bf2cbd5ca365feda35134f83f64d5a78fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:00:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:00:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:00:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360a3db99ecdb732a16f1f126976d4207aa9d983372d036f2b27c3fe152fcb7d`  
		Last Modified: Tue, 30 Dec 2025 00:00:54 GMT  
		Size: 11.3 MB (11269725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d2f319fdaefa9ea946357280ed31787a8424d1c2fb90c5c04233a3421762b2`  
		Last Modified: Tue, 30 Dec 2025 00:00:53 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b35ba6c19f111c946178b9e375dadc3d8f1ae76f9a5eae2ff0ae89ae98090a6`  
		Last Modified: Tue, 30 Dec 2025 00:00:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a28bdb6feee559d1cd4dfcb333fa279e90a66e33e29f8ded0cc4d368faad44`  
		Last Modified: Tue, 30 Dec 2025 00:00:53 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:32a86f15faa5dcc16bf6c784d55a31b761c66ab7c8529554d1657d0458cef74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5312d8239141252c42ebf8df81bc38e3b7cffbc8a79c6beb0c2a61fb1aca054f`

```dockerfile
```

-	Layers:
	-	`sha256:47bf88e7f96240e091e5766b95388b68ff7beed8b87d60f0b4fc52a3a2dd6b44`  
		Last Modified: Tue, 30 Dec 2025 02:08:04 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bed509e4049d93b04efaaf9a8cea41fe2da5b01edcea80dc537c82f331659f`  
		Last Modified: Tue, 30 Dec 2025 02:08:05 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6833c0bd4b9f3b8516fff1dabd1be547a6755435608d0c7d5bfb73bbe5896b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac88fb8f2f18c14f33633d001057ccd8332f2b7e183bcfb88b19303409bd080`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:00:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76de6c96e27597369b524e7338a949708ab094acfce0ab9acf41063372d76b11`  
		Last Modified: Tue, 30 Dec 2025 00:01:21 GMT  
		Size: 11.3 MB (11253479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cb27afeb28fbf93480fe947d17b3bbc43b3b8413a6e64f2718c9eb6798bbbd`  
		Last Modified: Tue, 30 Dec 2025 00:01:20 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01298f07bbc2cddc4313c6e7a20c79eb3b315e8de19434e19c11f9b8060cf534`  
		Last Modified: Tue, 30 Dec 2025 00:01:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267428ab28b53f5994fcac1d5a6d79dd9b2e94492fee8c05b7d29f5c115377e`  
		Last Modified: Tue, 30 Dec 2025 00:01:20 GMT  
		Size: 93.5 KB (93507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6f2599c0efdadf08ab22a3d433cf5372b7aa1621c29b1a9da6a236725c60046a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7e3b4ad787579bf2b2289c8d421f4fa997cdef176d24b19bd2425ac6d8feeb`

```dockerfile
```

-	Layers:
	-	`sha256:34f8520afdf262ef9c568b886a0ed65c06d34bf6c59174fd757244317d01bc25`  
		Last Modified: Tue, 30 Dec 2025 02:08:09 GMT  
		Size: 4.1 MB (4075478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d952abe5c366f262ecf4300fd673502af65a4e9c98038025db08ffad9834a4`  
		Last Modified: Tue, 30 Dec 2025 02:08:10 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:e541bd3d6e8c2e350585ff969178f5b1eb50d8c9ba616b7bdbf2f8399c5f14aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7d620a96142dcd3f186a6fe338504785161072efe1e215f5852fcfc5f84864`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:15:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f52798efde006ed1cd5f8b1568731b4e192bb8d42469448e91e101a0db4474`  
		Last Modified: Mon, 08 Dec 2025 23:15:29 GMT  
		Size: 11.7 MB (11690144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab9b17f9e8302b4007852306001a4fec79b4040b0206f90e41917f36c14aaf`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80fb5d370b48a0007fee996c5762d278fe813640bb9c94a63fb41e8d8b2e096`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b644a9afbba75e07f7cce8cdc7ddff087b8ce4f882d4922da7656fe6eae3e1cf`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 93.4 KB (93393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:682023088122f95448d674072ec064ed9c5f200510c386b7da9b9572a60dcf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb59ba0285827e553a3b085b7aa8dcc0cb47e214ae0b993a08817c9ad3cfb10`

```dockerfile
```

-	Layers:
	-	`sha256:ee7b2db1f021c38b521cae01de099d8549088a69985b97fdf1eae25474abc095`  
		Last Modified: Tue, 09 Dec 2025 02:07:38 GMT  
		Size: 4.1 MB (4073204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a489f0243008eccca8a2550085e9994ad5c7db757f3065e9cbac12ae22242e1d`  
		Last Modified: Tue, 09 Dec 2025 02:07:39 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json
