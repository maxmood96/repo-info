## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:eec5743071ab61aa2cf34da2f1e8a57197d04422ee5dc71aafaf4a519125fe0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:af9f36583560add0684ae7dab1bdb816f61d3f044bc5d455d931f4ed617ad22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bdccdb9cea6c7c13ede7ea3a3b75fb283da72406aafbfbb73813d7525d7eb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:01:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087844227ed0cec1ba8c0d55d16a177a3d958608ac6f329ff2f6c631784c3e92`  
		Last Modified: Tue, 07 Apr 2026 02:01:15 GMT  
		Size: 11.3 MB (11273380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f71f3b70db64197307fb8014659f0717258a59dd1cf269b297abbf9369a15`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9dbdb0f05f5cc24a2a509c37a8a55370a45ec69644733fa4eccbd4c755aa99`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1ba3fe3df2cd610b2d6f5af43b9f3aac6f36634eea0c736cb6aa176082b004`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 93.4 KB (93372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed21624c95a06c5fd4414bb36c295eae9a954252902d38e2dcdff94cfa1b39a`  
		Last Modified: Tue, 07 Apr 2026 02:01:14 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ac3718cdf216ba5cd7faf127d896fa8317033f3fc6ecd9014408fe6180c605b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8abef2d402a5dae0cb6e2146b2e6bf0521b504d9d1e81d98e3519375037667`

```dockerfile
```

-	Layers:
	-	`sha256:78653761a1692a80ecf22c84ca7bd515ca9da4cf3c2d746a8da1750bdff35872`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9755936729109275be75495c721adc327e6540f8f6bd7bb7b9da1731cfd520`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 16.0 KB (15991 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:05ae6caad883291c05cf64301ea240dfb58e9ccf487c04dbf125593179065486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578adc7f11a9e18c0f6c3228e563ad98f58d374b38b4e7e76654e19262b20ba8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:04:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f29ec73e1886510fb1ecfb768935d56a0bdb2f3329b6deaed948e148f6e68`  
		Last Modified: Tue, 07 Apr 2026 02:04:17 GMT  
		Size: 11.3 MB (11252932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73e9830f6c7909f269def0fa09293e5734e8331bf6f21d021aad1d19281930c`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d3bab704f4df2485dc0b8b1b1d11c105ada61e1fd0e6720c102bc1bdc764e`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33e3f5f6b18c765c6fc844131a5bebbef69e1f6e26669c44008a1ad65654263`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 93.6 KB (93574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19aaa0d12a3f380cf5dac0e4a3d81d3d55b275b9bcb5768f64d5204af903c03b`  
		Last Modified: Tue, 07 Apr 2026 02:04:18 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0a47a902ef9ae281f356a699f0831cba6bb9248423abbd2b4e7fe6a8620bc720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68838707a3e479a7f2dde37704699cf4149b940ee08843fd666ccd5a39314951`

```dockerfile
```

-	Layers:
	-	`sha256:c6b4f56172d14829f8e80f3225a5350ba9e3e6464cc9b302d06f022d7152dadd`  
		Last Modified: Tue, 07 Apr 2026 02:04:17 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d59339a4f579694ce7b209551f0d3b190faf1b489c5c5ad478ed15dd23159a0`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3c724d4e45ca96bebf9f3fe357c4829339b3157a445848dfe46de5eaaae9c3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c734b7942d0eea2f2a08c52e5decee33af22cec203299e20516fd50b63aeec9d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:48:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:20 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9facbaad0d2e9efdf61ecbe5eae48392e462f6157769317a5cd77132fb5b51`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 11.7 MB (11693031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a0e5638a1662e5b018e668beba699060c773c9c9b5033e00982543cde5738c`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8414a4c6370804d818b9319fcfa6758e633a7415d496c9365dd0a1f42c514214`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df32f075adbc2243cd6c4ca9bd13113a880f00ca717165e78f34ac340e358b`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 93.4 KB (93398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe93084be076971d6e0edf6f5a7b43f04ecbd6ab6bc01a2f0a3194af7cc09d90`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9e32f6700d0f6d5346a0337cda926a571a48e2592e895b59b79ff9c772ad4934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1be16b2bf72dd8ba11a539af912bd560396aa55dae968808a92678c26e3467`

```dockerfile
```

-	Layers:
	-	`sha256:b6600f485447398b6186abad6be1aa3acad2eb1130b9c7fdc1f47432182bf884`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931719e6ab5e367efad0d917c166131e4686443e17a79f01f0b9072b373d387b`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json
