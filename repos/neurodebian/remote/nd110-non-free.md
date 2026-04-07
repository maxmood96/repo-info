## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:86178481890d97f684454ded53c7f45765f092bbc50ff8ce6499015d9ca48ab6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fe085c2b66f5b98b8dabff665c090189b22b35705127c028d99a9de4ea2fbd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d884fcd0aa0fc7742ce71fda5592ddb3bdaa70abcfec2639be95de666e9a24`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:00:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:00:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3652b2041f6d71d5a4d2d4ce03be98853d697f2f28e3747ad8472df52258c718`  
		Last Modified: Tue, 07 Apr 2026 02:01:11 GMT  
		Size: 11.1 MB (11103609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072842f241cf41b2f78c655669448e3045739cc128d4db6f0e65a677f45acd35`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d227b73727a72f1240902141a5dd294aa2e87c47192b9198ef9072bb1e18a745`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d69b4dbfc56c2df58387113855e5cda409a9cbfe3d9e3ce402f3b5df010a35`  
		Last Modified: Tue, 07 Apr 2026 02:01:12 GMT  
		Size: 101.4 KB (101397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d923103343bc5dc334553f01396291d7a8d9d308763f616c40e0ebad605522`  
		Last Modified: Tue, 07 Apr 2026 02:01:12 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5b76ba35ffbf45b3b557b0eb3b42c7cc0a670ebe7b740ff28abc6f767b68d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5908ada024d71ceb6322e907e608c6a0c1ef4c4a62b8572c340c9b61e67b460c`

```dockerfile
```

-	Layers:
	-	`sha256:5b60da26860f07f069517505df7fde872e2c1542956d21035e652d9f1d5511f3`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a009cd19fa2fbddcb46841f1749649b56cda9c9f4f9b995b420d772a73b5d7`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8ebafb70a46289d45705b2924366ac85b68c040fc9b4fb0d212b6e1b14f3e47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63461361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dcf58c6c976daca65f1d05ca1cbe23a599a739b69de86a428b1cd743704180`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:03:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:53 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83dc7b608ee9f4bda69e556dfafd08b0deb8c7d5b42fa6c452c69fac9069b8f`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 11.1 MB (11109902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb66da7ba94831ac5b43b51d0a0aaf36b8246252e087373ab93e36d45e127d37`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901116b9c6b476b402eba10437d139accc48117e8396221afb2538026b321972`  
		Last Modified: Tue, 07 Apr 2026 02:04:03 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02b336969d84a4c8e10611b9c2470e6dbfdae6cfae1ef73b5745974d357c35`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 101.3 KB (101300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e190faa9f5e8d05e12f9dbe8984c181f00be94a7d7cfd8b8d4ca3d0c972c97d`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f59235285ee52e1f4c43c5ac7bc42631e373265d406e3a2a873b4ecbc791815d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3628bf8275b73b66b6703f4b0a233507b559112334b32eec23b58647aba7a5cf`

```dockerfile
```

-	Layers:
	-	`sha256:a7ede3816ed841103388f14a094f99b57b7988e98aafe1c9b20aa2ba51ea19e0`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e813811093f9223245e90f6a2c4e5d36513fe28f4694e3d10fca9fe6b70c9887`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7579a35afe8e174ec62d633c68614ae8124f1f401a290b9e69c0f62d50a5ef10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66308720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d676756c0d27d5b94529bd4c6cf71c8d72096117fc03c9b367501f8bbc5f3d4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:47:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:47:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:47:57 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fba7877b3ec8a566d97b730194c65658357ad675cdff2c35c6c1c8b5deccdb`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 11.5 MB (11502302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850a009dd4f23e9a62f33ec76651cd49ec853a8fd4707631e6d659cbd4a056e9`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3ba9c78991f613b0caa3f2f7156d2cb6faf06ac0d6819d4e02644dd1381e0`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b6b6dfeec66a8cc3a24e834879c3b4d6c1a36922d9d638bd2db930dd40044`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59daf1c381bebf5c5efa361f8527b353c71c67fe360ebb066dff44e164e82ab6`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7c5a566c3f8389fb009e31a33132c70c124e29e40a1eaf7c7d2ff15ddfdb3be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440cf12cf83a85140c6cf0ea5e40617e7189077c445023cca2e79d2844fa2737`

```dockerfile
```

-	Layers:
	-	`sha256:3f915c61028bc950f81318a5b1cd11ef596cd314b75ae7ac01ab9084e21f0ca1`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79910c58c46c2b4404c3dde156e9cd6932bbac7116f4d759f11d002c3b02bcb`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
