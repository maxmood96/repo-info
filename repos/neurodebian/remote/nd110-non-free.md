## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:d17d04f1ac02bad66995998e2ae28c3c82e88e2fcec99f59c0a18d3c776e78f9
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
$ docker pull neurodebian@sha256:b734657b642e08b08866caab9911835193fca7ed33794f7c4367a19454d09b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03085fb17625d1c30ffeb65005700bf706908973c00ef9ac990715dd9e90c25`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dae0b7e934367d2b88f1ac500e6538a222db97b01cf9cd7802c0b1be056884`  
		Last Modified: Tue, 01 Jul 2025 02:28:18 GMT  
		Size: 11.1 MB (11105057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd1d44863bce699262cd8600fe21830eae99bebb3c4423506f7175be56b25fe`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0f1d88169004dac6c5eb7b29ee577f97f8b081e5497bcae03cad289250deef`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622fb8793f15015673349d020e6b0a437839d9874df364993a396b6648bb6031`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 101.2 KB (101210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94b117c85b338d81d39e86682bd380689c8ca814cc3e8bb9666a9a2ea04786e`  
		Last Modified: Tue, 01 Jul 2025 02:28:17 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5315131dd1e8ea9a82c8c3913d1a9587a8e49fe669b5028cd92c0d9181e77d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be7bd5c287af5b1a13999232ebb8b3e0682549e9d5ff9fe28976cf9ae46bfb`

```dockerfile
```

-	Layers:
	-	`sha256:8a6cf0c7e239504b10520ed25dfd0d1d09f6fb84444cc1e8127ab89f8b28ceb7`  
		Last Modified: Tue, 01 Jul 2025 04:07:47 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d202e357168780849b4b8cac96436c5205ca0df4b7820c95100679a4ed7bd95b`  
		Last Modified: Tue, 01 Jul 2025 04:07:48 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5bff9a16bf98b571670d436bd5d9854bbd08cb1407f3efe7936ddbaa18ec2c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63462044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169ed75b5dab84a414129956ace0159c7a385174e3f72a3cf4b529b69d587201`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256555700ef973ecb73aa3c8bc0f0d7fffe8a2735fa5d91f54019a21aa40f89b`  
		Last Modified: Tue, 01 Jul 2025 07:24:23 GMT  
		Size: 11.1 MB (11106129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848df86738100d71035e2542674c218a455d241a7441815ae04161bb461b4067`  
		Last Modified: Tue, 01 Jul 2025 07:24:22 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f66cf5fcdebd52fcf9840b91315c7cedd0ef5515157b00fdebe3adc6927e24`  
		Last Modified: Tue, 01 Jul 2025 07:24:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17143762973cab51c96bac474ff8a3892f07cd997104e133db9585aafefe2ec9`  
		Last Modified: Tue, 01 Jul 2025 07:24:23 GMT  
		Size: 101.1 KB (101117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592a9b5681836457f57fd5729de52b55557dbe350bd0b8a5583dcd39c3f73610`  
		Last Modified: Tue, 01 Jul 2025 07:24:32 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:87e5ba0fcd5512d411875a571e6be060eb598013f084bcc4279e9234bde8e7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9585c29e2d492b76e03c778214e269e64a09e0e5b3033f86fc7e222c387eb7b0`

```dockerfile
```

-	Layers:
	-	`sha256:fdcf64bd1ea6623d9a42c16bfef1676e2bd7fa832839b1a186fdc9a1e014e919`  
		Last Modified: Tue, 01 Jul 2025 10:07:38 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95323069abd8fd7d64d7456366c353250e6e5a9627d8e79eb60a2ed185822a0e`  
		Last Modified: Tue, 01 Jul 2025 10:07:39 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:925b4666368a4ad774e9d181983ba3b3ca654c5abf1519e4d7416b99428a6cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f232b4231124a7fe88e3bc96558cea4458da2f22c3f3164398abd4580befafa6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
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
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74345852c65cd02e4e4397d96e28831791f8af681c186316d165d7ada9b85457`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 11.5 MB (11500379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a71a431b08003b189839ebe38675ec712265886ad39cb2bc38f36f37de3ed32`  
		Last Modified: Tue, 01 Jul 2025 02:25:26 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc894d9ac437edcd3a53ff02d8bfbd4d37bd998aa2b3adb659ac2c3d875988`  
		Last Modified: Tue, 01 Jul 2025 02:25:27 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d2cf47ac839f5eccbb25d4bfcee634c5ecabca37f62b002db96ff745a5f676`  
		Last Modified: Tue, 01 Jul 2025 02:25:29 GMT  
		Size: 101.1 KB (101053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d1bcbbabde5f272e8544c78b363ef94f9221c61429c88fd16a84d0957d01ed`  
		Last Modified: Tue, 01 Jul 2025 02:25:27 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ec739be98441231feb937bc2ae098276e6bc04a105445c89edfd6d558117edd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17289b404e71a37192089b551b24b5db8ce32126f830c878efde71a437aac004`

```dockerfile
```

-	Layers:
	-	`sha256:18a9a8c9a1b8d2ebd12ef4e4c4ed490f485fa5079e20705d93d021243ff15ff0`  
		Last Modified: Tue, 01 Jul 2025 04:07:58 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1013ae2bb3f383bdf4055979fff2420a9f9685bdb331af179c41b9e293bfee64`  
		Last Modified: Tue, 01 Jul 2025 04:07:59 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json
