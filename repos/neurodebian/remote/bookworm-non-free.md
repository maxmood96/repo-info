## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:d862dd1dc8d155384376cced3c739f8342968dec401b3ebdadbbf3371e2f3e84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:22518b5f38f00c2114e97b3187d585db438685a05930a18785e5b3adb73f6a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c97b3032259eac465ebf0c8ffe17b7906d09a91ee3ea949fd9dded523db104`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb6694c64cae843951d54e2b05e2610566e3fca8973c074796b9af8a498c77`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 11.3 MB (11269576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e794520964c3a381276cce16943b4362333efd5977a64c5fbf154c77b6015c2`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fc78f7af59fd7cb66064d2b76dac7beff22e85aa7dccb731fa985ed7217c7a`  
		Last Modified: Tue, 30 Sep 2025 00:16:12 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7265c0ebb450e80f788f289e5b00ec5e5704aea9278a33f4c5ed429a4c20df73`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 93.4 KB (93384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2065cea84fab934fcd1190024d9ddaba19177d1f00876c2ebb45a42ae19c4e22`  
		Last Modified: Tue, 30 Sep 2025 00:16:13 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f8b4ff6a2b23ebfcd87f18355293fc60648ca9af372ce29c6507b0427f7ac9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf7e694489c6fbe6ffde1e32ef3bb99627d8f861c8bda8b0918f984935bb86`

```dockerfile
```

-	Layers:
	-	`sha256:b614fb6a5adfe55efbafba13c46d348a4d8670764d9d9a5ea0205ca21574afd4`  
		Last Modified: Tue, 30 Sep 2025 22:07:28 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c25191c38856398fb7ad3b288b257d6f3e09f8978cd82e718e4dd7a99c56489`  
		Last Modified: Tue, 30 Sep 2025 22:07:29 GMT  
		Size: 16.0 KB (16035 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:14c6af47ab2eb20d548a33b4950a8064cadf5103151dbde85721d736f7952549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770036e294af01f132221eff46d03aeb9fd3ab8e68aedf7708ed786da2cebceb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3898d44334f1abae852d530a5cade80ec1ebb870e449f5b99d9f961a5315a02`  
		Last Modified: Tue, 30 Sep 2025 00:19:22 GMT  
		Size: 11.3 MB (11253407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb9ea5bcd6e7676c1d1f0aa5b1f1be9505c317be092c246d08ef9e756cbfcbc`  
		Last Modified: Tue, 30 Sep 2025 00:19:20 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ff8510b562165af3eb589e1fafdc7f2085c9e55c53a0d8875f05a9001553bf`  
		Last Modified: Tue, 30 Sep 2025 00:19:21 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b122a4615dd127bcc9eda078ce123a341c4fc07f38436b92fe87e539ecaa528`  
		Last Modified: Tue, 30 Sep 2025 00:19:20 GMT  
		Size: 93.5 KB (93508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a496b42997f524257237886d80a6f9fd59724b091a359ed42eb3d1f81b79ea2c`  
		Last Modified: Tue, 30 Sep 2025 00:19:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c13213fed3c5367640f48587d9c907be8453bb8585766bf1f5031f2d0df72438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6466a096093118b0e12f98547696e397648ac394f697616c6ccdf2feb87515`

```dockerfile
```

-	Layers:
	-	`sha256:03f9b0f7f7c935c94de22d574f043cc96ee44e8f1f089633c7290bacd55b2cae`  
		Last Modified: Wed, 01 Oct 2025 13:07:21 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee16f24e2006c7d9bf4faa0d7e58ef704cc6e5c6fad6790fb38d2403ecc35c06`  
		Last Modified: Wed, 01 Oct 2025 13:07:22 GMT  
		Size: 16.2 KB (16175 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:274603d10dd008ffaae3f5a404c2cb78e59ecd5706eb12e88af53bf598a57867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2e21fcc30f1784d46cc228997afb47e22ffedd4a368dfcf05b81367454dfc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8003e96b9e94adb93fc76f0aba6b61a61d93076bed93f875ac3df4c3b0774a6e`  
		Last Modified: Tue, 30 Sep 2025 00:46:13 GMT  
		Size: 11.7 MB (11690057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f40fff84c9df9d31e2e7597437f764b596d6d5cc1c91b257231aea263e70a9`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a8e013318eab027adcaa49bd9383346d072bc458f9f83465706840e91c6917`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66354afb13fc7968d1d014d293a2852ad99c3cd01320d7aeb89677a34f189aa1`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 93.4 KB (93386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc70e80f96db7f036acc3d8b7e90b499de2481acd8fd1bfba443b9576700b711`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a747702e7ac618c28924fff29384270841e58c2067491ed6db76abd16c244529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5eed2cc266a48e5259b2e7b9f08ec4d7cd2d6b99b22fe48f61fd62c376106b`

```dockerfile
```

-	Layers:
	-	`sha256:36458e6b34117b91d12dcd4244f4588605c8a0db6a8649b262ee724e880f54aa`  
		Last Modified: Tue, 30 Sep 2025 16:07:34 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e511c629df67a5cfedb1431796c40d83cf94f446c340de58678f642dfff2d9b5`  
		Last Modified: Tue, 30 Sep 2025 16:07:34 GMT  
		Size: 16.0 KB (16004 bytes)  
		MIME: application/vnd.in-toto+json
