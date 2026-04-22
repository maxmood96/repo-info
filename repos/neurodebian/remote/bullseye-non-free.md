## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:14daa788b62b5f8c8284fbdfa8ac92144f65e82b4a76575543fc1c4ec0842df2
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
$ docker pull neurodebian@sha256:555440ecc7c6f655a1f24cb37b25ac77f16f360a99049d9ea7a9c5c136dba234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38937761e563f02f1a8d4ba92e24ea94cdcd83de4203265bb370625eeda2fd05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:44:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0802b439ba506ee42b40891edfe6f9b4eb3055ea7d81ecbc3d1c87a08b141de`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 11.1 MB (11103547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ee071305f1b461b88de5416fff15b4f7563a181be72046ad6dcbe2c446b02`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f9afea8b6181ada18a56edd636f0726aed91cc8382c81977739411f231524f`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386ec5b98b370be832b747e784e7effe8e6a952f7ce138c4def942bcc243d7f1`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 101.4 KB (101353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c47ebcb0a700e2b6652dbc7de864c41d2126d949ebd0bca7ed3acfc9d8b614a`  
		Last Modified: Wed, 22 Apr 2026 01:44:12 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ace222ba3da95f703da60158d587e1157e099ecbbae7f02da2f2877bb04ba743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54135d0cb4cdfc7dfac0b8beb5954939cb79280fe680f47eec5643ad0f6e7346`

```dockerfile
```

-	Layers:
	-	`sha256:e768aa59b6fdb62033d29df462af080e0ce18d30ba88640f432b6cfaeb7aa0eb`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b29bfc03bd2c77e02f21088f2cda163050d8f828320dfa8b1d23037ce926f25`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ca2c3a23602a03460ca26b9f213125634e94c388063a32a14688d65217d6c3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db056d8cdcb4e95f441e800e13433a568632cd36316df6cf34c253006e4be25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:46:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfe1d2cc6d2e7bb43dae058bb8276b894a2be14a9f73e20702e37ada7e1fe5`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 11.1 MB (11109842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a075bb8e87576480a25c5a254e0d519391be348067703b2d5f943763193ce0f`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bcc8d253eed27b4d4602843d761fed0df2781539a674a8a4b9106c6202f4cc`  
		Last Modified: Wed, 22 Apr 2026 01:46:38 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd09e3648df09d52a3ca93bd4b09431847db6762c78313e0d77f1063016d0f3`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2a249bd2b04f947ebe8b42357abb8bce3037999ed2382683016710fd8dcf18`  
		Last Modified: Wed, 22 Apr 2026 01:46:40 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:05469b94da86816694db020fbd8796a52b653a4b98636d838ed60d6edd48cbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a111a28248ce005acab8e2fb2b881d722ab556227fbf28e89fa03563e4cb04`

```dockerfile
```

-	Layers:
	-	`sha256:74493f42a5664f6e345502e4b4592a060225154f0b5838ef5859a70bee364bcd`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4988e12d16a4ed5dac599982e9ffc5fe713452e61fd0d82004c31417b642c1b`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

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

### `neurodebian:bullseye-non-free` - unknown; unknown

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
