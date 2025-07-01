## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:9c964ebb4ab3d443f31be69b7f885dfdd32aa0a78af54de47aba96c9deb9151d
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
$ docker pull neurodebian@sha256:1ba5cf138a7958ba2373be9f3a012409a50d4f6f69a99b904a23eeaaea1d55bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c59c69d4545682de48af80c95c5998b828426900abeab9761815fc72ae6b8e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff56d4e02de9968c2f7acfe0f70a56dffa1f9e68f2fb07c3a96568b07b7b337`  
		Last Modified: Tue, 01 Jul 2025 02:28:40 GMT  
		Size: 11.3 MB (11266805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f23f67636b82e4340303c4759ba6af0d6c3c122f287fc4aca86952ceeeefb`  
		Last Modified: Tue, 01 Jul 2025 02:28:38 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa6d87e2202e3f134289d48a6e278a08d1307503a49cdffeb0f0aba78d4e845`  
		Last Modified: Tue, 01 Jul 2025 02:28:39 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf5f2dd3e0931e38c25146d41b51a5971c5179c3d275a6470fb1af10a9a8ba0`  
		Last Modified: Tue, 01 Jul 2025 02:28:39 GMT  
		Size: 93.2 KB (93174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c61b91917510b6f66199037aa56cb86698ca55682be722023e3947b2b93e71`  
		Last Modified: Tue, 01 Jul 2025 06:02:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa9525deb20d8a44682ea41f8709711b3b5463a1f1f52fafb72734e7084ef2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcad6a81cb20bbcb750f2326b07a0c6580b3fa3e74783793afd18043c88e63f6`

```dockerfile
```

-	Layers:
	-	`sha256:2a5919c0c461a5cb92cbfc424ab6ac00ab3192939bf304dd87472fe1a966c7be`  
		Last Modified: Tue, 01 Jul 2025 04:07:32 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f5ca90ced41104a890aeb7615ec137b6270f87a8c4709ec7c6510bea1c1a973`  
		Last Modified: Tue, 01 Jul 2025 04:07:33 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3f66b6cf9c777c7ee2675df679b3664db8db5bffb63e5f8aae246ebe7a13d88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9605c535fd80e79ed800f02eabdf96798a756d9383b1767f72ab8c2604a49ff6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5c2d6b1d7d5d28d02e2f2cac517a8cdde90e21e5a6e67277ee7cfaad9cb254`  
		Last Modified: Wed, 11 Jun 2025 12:09:03 GMT  
		Size: 11.2 MB (11232526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765bba7a7ecb589546d86353bd0d94577c74fca3b7a96a17b6372db8a4d46d17`  
		Last Modified: Wed, 11 Jun 2025 03:35:42 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bea4e39b1faf52aa6e75eed7c4e67851e88e15f1bad433741dee64f21654ac`  
		Last Modified: Wed, 11 Jun 2025 03:35:46 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571ff130ee2030768ccbdde40e0b0cc38a55d68706e2e115ed72ce1951bcdbe8`  
		Last Modified: Wed, 11 Jun 2025 03:35:49 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e5c12cb63606f72ac2d02d6c4454a55351dfa3a9d77fce2e7399bc1258ca27`  
		Last Modified: Wed, 11 Jun 2025 03:36:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c7e6a86aef74f4f3a8d6d667f461e989cbfab19d40cb90e57c7c188e15892bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2ec0e9052301c0bd49a05f5e70e49b8526e1e401d45da2f01932619441a4ba`

```dockerfile
```

-	Layers:
	-	`sha256:e78e5536cfdbd3ebd739c041c46391bcd6f46539462a2d07c4f2a1a0fc4632a4`  
		Last Modified: Wed, 11 Jun 2025 07:07:27 GMT  
		Size: 4.1 MB (4069065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd6c977ee13182fafe5148ade423f1ec36b61c08ccfaf59c11afed6705becd4`  
		Last Modified: Wed, 11 Jun 2025 07:07:28 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:79e0f033de8cee8abcd6534af7c53e0091dbfb09316a132841d416594cdc5fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0525af502e390e1a5eda9692553346a25c3c21839d2774a07e3778a5d44e41`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6f94804b284437d7ef08613d0829711c88d64ccd070369893a5912c9c05896`  
		Last Modified: Tue, 01 Jul 2025 02:25:24 GMT  
		Size: 11.7 MB (11688973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f54c1638f4bbbbdf67ed7eed767ce99e7a40e7650e32e8d1dc6b58bb53656b`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19552ffd563dcf7d4dc18d2007c211133183546c1158baafbb4e96dc50a9ec51`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ce5aeae3d99912366df51677ffad150f086248c24913ea58482354c707d571`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 93.2 KB (93214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14be2ed04a1ef342abb523a07e79991996f57b732c627bf7ced803dc8faede73`  
		Last Modified: Tue, 01 Jul 2025 02:25:23 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a84c5938426df0bdda06c3efbf12053b76c0eeb1e979fc464956185b4c4242c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94e7293e4eea8e4ddee297cb3b31e1961f22dc621faed88bca7c01a75783e3a`

```dockerfile
```

-	Layers:
	-	`sha256:6b08eb38b718237949b3eeccf1c246ac5b7f768396574a6db272c487b4a85a54`  
		Last Modified: Tue, 01 Jul 2025 04:07:44 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd4cd176f4c2ebabb39ea41aa1929c6dcef41fa670e7507291455902311ee16c`  
		Last Modified: Tue, 01 Jul 2025 04:07:44 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
