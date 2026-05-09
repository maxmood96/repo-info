## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:cef5a7249de9c877b5f697fa3e104454149bcdc02e814a22d09bd463bda75f31
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
$ docker pull neurodebian@sha256:5226686b3732483477cad20cd6e322d9998a4bf932871ab9fc2f87848d7dad60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60077340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f04cff1ccfe79e7383ead04f269d7ec790faa2f6c04d69c1c31e94390981c27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0e929ba940bb6645aaebb3cf3e1b30d0ccaa2f7d53cb82e57d451efa023dead7`  
		Last Modified: Fri, 08 May 2026 18:23:00 GMT  
		Size: 48.6 MB (48622043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631bd401a9ea85121899c742741152c2d753c20f5063b4935e5677c9b9bb941`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 11.4 MB (11362517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c5849b7c2876a6e27b5173f8d1e8f02d5fcd243d1dfc50b858e91b67083f22`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a5f0d6856a2cfa52c99b2c2ed11dfd8851eb14b84b636b738a49ade15c18a0`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9758222cb4c90ec2c761ca114b3db8c018b0d6b65d329a9f50422fda80d02d31`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 89.4 KB (89429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e2980abcfd428f39d3236270246d8a542601ad7016f6a19e3f33ca6c13b26`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:51d3b372a86f0abfb8cf682c3f299797d0fa31e061849f6511133bfa2430f687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067694b030e0ad0f1a824f2d5271aac7d5f509e60a64cb051696a7c62e671b9`

```dockerfile
```

-	Layers:
	-	`sha256:51c0f2b8c73138f5a50f5cfb4cdb5f94ba792bf7099a8cd6c1236b12edd975e8`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 3.6 MB (3556280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af51c446d933ca99eda664c827ad478fc09984eed72ce1e7c5689ab96396f57f`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7c5f596c4bf8c0ccc478841c47092c4a4dad71a015d664685dc1c4b96dc058b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59812168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9528113b20964df2f7a7b1284f55ba0993cab2d96ad5485be40a46fb10c581f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be64bdc407e7e3b95b79a3ffa508782d23c39791fc66237b6b9ac0079e6f8e5`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 11.1 MB (11059006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a038166bca6013ff60ba5efd623dbb4e5fe1ee3d4446048b568c45cd48f1f4`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc2ed7a3a505ca3103c47fba46d5e291e08d49ee72ba39dedef20b1008f326`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a68e5868a8cbc24ca18677d15c10aa94f4c51fb3e1f19e418a98acd77848b6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0446785ebbf74532dcba92825c6decba78dcf6a16420b18506b2ed57f7928eb`  
		Last Modified: Fri, 08 May 2026 19:46:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b0d5416b6794a636e42304fdb74a53a9ee53950b35de114de8bbb04947b6043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bac42a5873dea8825b57dc7136a3a27ca3ab5b4fcb1501abbb9798be97ed00`

```dockerfile
```

-	Layers:
	-	`sha256:24443809fcc31ff23bd314ca750f0f95a8effe8849bd1131390892d2ec92e5a6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 3.6 MB (3561628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a27081017521680b89fcfa70690d05d07b6f2c8103aaa1557dbe8917649d344`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:03a1a328bfee5ff0a2bcd6a694bf094d95381b9b663a843aa2e3ae99924b758c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61606220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c3c7ade491f697623eaf25c70f50f5a71cfb7bb1d3153121edb8caadc6b964`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:45:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a99493d96d6f92ea6d88890fe995d3918a05c9baec0b84c6e9d10b95007a82`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 11.6 MB (11588918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a0c33e147fa59d9124cbf1b02679d5996d94f20e43a0b0dcc7bac0c76d9bae`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d6a895ebfb8de9b1aba761e3f5032daf08032da3fa41c4770fb7be187e4cf0`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d22eba06c949e34b02517b4968779ffafdb8e6ce52c51cf497c682389b154`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 89.7 KB (89726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2616c3f976bfa74ec623fc4792a7910f4ad8177ed3b117a8e270087f0510a539`  
		Last Modified: Fri, 08 May 2026 19:45:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c75c21cbb9fff8f22041a53794d1631c30d371e24e4a25d431e1c649eb7fa77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7075d85a25976a8e3bcacbf0a99c3a51ddb29e013c5b42c7da1a973f852c1ea0`

```dockerfile
```

-	Layers:
	-	`sha256:7ca33354efa5a678e18c52598a002e0f989c7bb096e45147472c2b5788c43e45`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 3.6 MB (3554226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53d2a0a43649d8f679119161461ce4dc60d130a0faefe0533fc5173dbdb17353`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
