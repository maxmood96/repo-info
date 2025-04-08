## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:f4eaca29f9f94121e8d5b1cb2392425b163b2d8e32c5197658255d175db7e106
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e9b08a4628cc0df81488abe3ce1e1eddc5c70f22369e2dbe723ff78225403472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64957378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d2a0a9ddbd93a0767eaaf18f1b3bcdc38c24b62533a24cf6f0c562985a80d3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2fc2274cc6634839d68f5e460a9544a5782d133f59626508b045414e2f27f8`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 11.1 MB (11105076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6b68ea8572b2570c073b9243b0db0755bdcd466de7c937673f018d1ddb6fe3`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f32b16d100896c8cb96acbf370519854f68fabf5252e129da5c49a635ce976`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80428172f8989bf82b58af2babdc46d7bea35f281d105c8a5a60c677b82602d9`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 101.2 KB (101229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db677a40776f6422a0f689f31e3f965d6bc24f44f6cc8811e567145883e7890`  
		Last Modified: Tue, 08 Apr 2025 01:37:12 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:31fdb5293eff980bf6e24668e5abdf9a455e640a6fa6d070df5d8cae2f4eb9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539bf5eb871955fe1c2af15745cd78183121c312b908e0dbf51e6b26ddacc6f6`

```dockerfile
```

-	Layers:
	-	`sha256:6fd14a45678113abdbeef00560f1034d94a141a5e8bfe3538ef072c6a51be24e`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 4.2 MB (4234746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84f902c5e5c6f814c43bd0abbc9897e15729cc1b9de0762b781673d50fce2539`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:575f0d6c76078c6a8d9806ddf6953b7641c7150bfe99933bec3d0fcb54829971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63464012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe075bbb7ee45dac5202adb64e4d47fa89d41eabb902a3e97d8c8c7019d04fa`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87946706aa736ef80d52aa62b6591f2914c573640b3b36ab0581897ab67232c1`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 11.1 MB (11106119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328bb261a19ee93d5235ad1623cb40c9fb7dc36a4ea866d51e418dd5bb75524`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5723df042ddc1277c89c7a1509daa7b17d8f5f8e95463f86467bdd6689acc65`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4164f8be20cd1c5fff9c06e619bb825756f4005a3439bbedca991306a75b0462`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 101.1 KB (101124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43195c5207b2a2869775a305cafeb460ca03ff3938082591b9f3cd39f945926`  
		Last Modified: Tue, 08 Apr 2025 06:35:45 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65415b1eba54a3fd24e5f47ad4b182b20145806d337227346d50ead8df24713a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b058dde6e782950b11772c5671f138d1c54c896d987103349f03dad57e06c`

```dockerfile
```

-	Layers:
	-	`sha256:bc9f7f017e0174059f0f1032f4beb8a56ff0df243b9aa3cbe18d7824f511a5ca`  
		Last Modified: Tue, 08 Apr 2025 06:35:45 GMT  
		Size: 4.2 MB (4234353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de14165df62a3c79cbf714192baeac35bae2b68c96d2dccf0d7cb723b0af08cb`  
		Last Modified: Tue, 08 Apr 2025 06:35:45 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a8ee53203df6e5dde510596d39428632c1e95f5c91d757bbb5d7f1275e77aaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66288560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008756991a14b89fd8de3242193f66450ca230da9df385fc3430ef12aebf2f22`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14a195df3e575bc81f4bf5db264dd69b9119e972d82f56708aaa3fef07fb796`  
		Last Modified: Tue, 08 Apr 2025 01:24:40 GMT  
		Size: 11.5 MB (11500460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daa007e54c239fbfbe5087cb47ca43af4a7d1df694c5e8a8020174726c19a42`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97eac2879e0c6b2ac36eace93767cf632bd46666df09233d59b0a518e37b7db9`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205f71647024d7da981756d414aad5c1b87ec5904332bbb27f834d260e8b0621`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 101.1 KB (101093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f1021c8f19beb5ca34caf396e54ede187b5ddd0d6a17667da83c0ece55b0fd`  
		Last Modified: Tue, 08 Apr 2025 01:24:40 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3f139afc6eea84db213d78138d5ff18dcda1d6b9105af3f17743f10c704af381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3157179441aaf0491abf19187475be087c6b41bde68ab8899132b16d601bd858`

```dockerfile
```

-	Layers:
	-	`sha256:00f891168d9d1b5d2facdaee9854c54ceb9bcdb7609c5e9112af4c72938cc7f7`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 4.2 MB (4231208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccf36a89e0212365ddf58f880ecedf46791ad68d8789f7d0319055de5de2dfbf`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json
