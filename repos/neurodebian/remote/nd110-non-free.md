## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:f365498c9e2b481ada8d12f84c514a7f7295e0c914aeea1b9b3304c2631451d8
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
$ docker pull neurodebian@sha256:3355012e82a73821bd5f25d4d18a752f127d206cbf799871d7de0441a7365df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66acd035f0a7fb424d390b78ce03e8934afc59084e81d8b4c2a49beb3281f883`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:26:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d054cefcc7307a052aecf20d180a8c03742b08b302a31c26a0b0642398c3192e`  
		Last Modified: Tue, 24 Feb 2026 19:26:19 GMT  
		Size: 11.1 MB (11103476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd6ecea2a4379a99674635b0fd7cfda1d84a09163fd32702e92b5b671a68bf1`  
		Last Modified: Tue, 24 Feb 2026 19:26:19 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d10b572a907d8408c8f54d3b3b8642bb1b5da762c422c81f4535828f8558f0`  
		Last Modified: Tue, 24 Feb 2026 19:26:19 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ef1853d1bd93abaaf3dca42d7169fadde8efa5eeb9085d27db14e83fdd736`  
		Last Modified: Tue, 24 Feb 2026 19:26:19 GMT  
		Size: 101.4 KB (101367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ecce14f61035075005430d5a0b29b1d8528b8d48ff878f2f14511887695b58`  
		Last Modified: Tue, 24 Feb 2026 19:26:20 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5de0f4afc6fd212a8e9a468b6cfe758698e08f414f99f6b302a9e0f6e95ade0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb87c19119a5cd356b6951c167e98eba01dff3f06dfd9f9e134d0f0ab173c31f`

```dockerfile
```

-	Layers:
	-	`sha256:b16ea257e3cec5342e120aa494425e113a7061eae2aa2296ed5b105137316431`  
		Last Modified: Tue, 24 Feb 2026 19:26:19 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935d5172f4dfb9d3213dcb712a08b5b39c10236aeabfabd2174fad0e55b2aeb3`  
		Last Modified: Tue, 24 Feb 2026 19:26:19 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:57617a56c44ff81119251ad8327f6d4d41c93939f3ff71f94b24dbfb62cbb54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63471954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1526f55a66e6a55234c0d1045062e633b629fafe8f0981f721485e049a38b76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:30:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:30:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:30:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:31:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ea58526955c5babf2494e482a0faf3d1f7e089127d4888ae67f51d94c9b360`  
		Last Modified: Tue, 24 Feb 2026 19:31:11 GMT  
		Size: 11.1 MB (11109908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdbc616934d7c53e155526daa7923553b7cdabff6fcc4803a23f64d616a9209`  
		Last Modified: Tue, 24 Feb 2026 19:31:10 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05ab057f7f1172a44ab877d312ce878d43e7795f61aeecd1d418ef4f10a72f`  
		Last Modified: Tue, 24 Feb 2026 19:31:10 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fd26a593977f80bb65aa2191e94ba7bc28ec94e4871e165449c65487f13c8b`  
		Last Modified: Tue, 24 Feb 2026 19:31:10 GMT  
		Size: 101.1 KB (101105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3ce7afa3a3d03ecd08d87bc6d3dbba4914effc4dcfc2825e4b0bd27d345ca9`  
		Last Modified: Tue, 24 Feb 2026 19:31:11 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c9fc83640ca76875237abfd7a58347f71636c6f2107ef85c5c3adc64380a2e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de729029deb6f8c46e0e53f25bc3abb6d88b2d66346e82509a7741c3040c08a0`

```dockerfile
```

-	Layers:
	-	`sha256:df3bcf5d2b510a0e4ddc22ad81652b3a2bfd071ea911fd18903143e4493c5717`  
		Last Modified: Tue, 24 Feb 2026 19:31:10 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330f588e0742ecebf93abcd097ef23f2f8bf42c87005b298530263104944c642`  
		Last Modified: Tue, 24 Feb 2026 19:31:10 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:dcbe0bfdcf428747c0b07bef65c0cdb214c185ef839836e7c102c28c801ec1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66305969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0a5f7443d9725e9f2eadbe798e6e205a0e9296cd5a4573daac3298f41e040b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 18:57:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:57:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 18:57:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 18:57:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:57:38 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:be7de57c5a292b6137b558f622789891088c38f02c67ce301a1559809fbe8ae2`  
		Last Modified: Tue, 24 Feb 2026 18:42:22 GMT  
		Size: 54.7 MB (54699784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f4504e637ca8816734c4c97630de5d3850e7f01f260b48713404ce66cb1855`  
		Last Modified: Tue, 24 Feb 2026 18:57:46 GMT  
		Size: 11.5 MB (11502374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1bc4d2793a90c632d051539dcf817805254b43567d05db1c1c9ecc7de783ae`  
		Last Modified: Tue, 24 Feb 2026 18:57:46 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d0552fa9f7f51d63319eb6579568a9a34fd1608c354c75bb8d7836f0d8a6c2`  
		Last Modified: Tue, 24 Feb 2026 18:57:46 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f594fc143cb8be39fa0aaa0b65b58598b76d9a318c0800f23b674ff3815d60a9`  
		Last Modified: Tue, 24 Feb 2026 18:57:46 GMT  
		Size: 101.3 KB (101264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdde090ecd3b95e47bb6815673bb7e1313a5e5794d6a0233cdfa59c01abbdd0e`  
		Last Modified: Tue, 24 Feb 2026 18:57:47 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fd601ccb57866e0f7135c4d40680a0ca9360244a68f16e4d434147097bf776d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e426efe67521c478c3860084ff276d3ac76e7643867b7b94be9fa89908ad1630`

```dockerfile
```

-	Layers:
	-	`sha256:87b6620ec88afd4789d34c28092946dbb31506283a1768673e75759e2384df32`  
		Last Modified: Tue, 24 Feb 2026 18:57:46 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab307919a23438fdee21968215012c242d223983601e6b67f43a9bfb81d95b3`  
		Last Modified: Tue, 24 Feb 2026 18:57:46 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
