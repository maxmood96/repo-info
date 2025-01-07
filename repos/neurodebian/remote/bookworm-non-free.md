## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:443a23c1d6975b64d9ef984ca22ab68e6a7a7e8a60babb3d93567bcfd54d9b1f
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
$ docker pull neurodebian@sha256:768a5888324da8f10650f0864345902be005b88d7ea333ca49d729eba304bf93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18be643e311310cec76b259aa91c752d66eda009b5314841a821671d80385fec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc3f2ba2cdabe9286f5e36312b98da1c17f9f020aeaab444d860731680de491`  
		Last Modified: Tue, 24 Dec 2024 22:28:59 GMT  
		Size: 11.3 MB (11266769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0deac410ae9043bd2dc82cbee38b1679d26ca09c8aa209c1e724d414678348b`  
		Last Modified: Tue, 24 Dec 2024 22:28:59 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8d0b79701bb957f0dfbef51ba6875a52a2c48a37152bcb08c185754a6b0f66`  
		Last Modified: Tue, 24 Dec 2024 22:28:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267bcb64b35e6799972636f526e483e3aa87fef0037e69845743e0ca8b8e065`  
		Last Modified: Tue, 24 Dec 2024 22:28:59 GMT  
		Size: 93.1 KB (93134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8390eea91189a76a421f4d57bdbb1e57d625efd228f3316cbe5c6579be49b9e`  
		Last Modified: Tue, 24 Dec 2024 22:29:00 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7268f1535b731831e096a6c7db3c741401bef526399cb76eafeda86afe9cfac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74af61c14a4e36f7041f838e55bcfab42d41adf84312885cad5ce7fe0b48e43`

```dockerfile
```

-	Layers:
	-	`sha256:2223d1f3e771ecea574420349455caecd33a0a72a45bad63421db328a0a9a14f`  
		Last Modified: Tue, 24 Dec 2024 22:28:59 GMT  
		Size: 3.9 MB (3932850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ab5f83f7192c7ffe9040fbe39dbc121af4ddf43e4297120ed914b8bf00c2b38`  
		Last Modified: Tue, 24 Dec 2024 22:28:59 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fa97feec1d4944ff4684fa7ec8556f425fa31a11c10de0e0791700b8d8df1101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2577dbdb1d1713f34148796b855dccfb4c136e1de53881ff63bfb66b932eb15f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0367019e15543f02a69e834f1c24024f42ff4a354dc1d505f1fb3f7f641f344`  
		Last Modified: Wed, 25 Dec 2024 02:19:39 GMT  
		Size: 11.2 MB (11232347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a91a2c5dffa6242c8635282e5d3644e5542d4d3fa55a50296ad77f135894427`  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f7a3036299a2c5f2be4ab8d3c47a46eab3f06d55ab60826cc639ced1d6c067`  
		Last Modified: Wed, 25 Dec 2024 02:19:38 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06582c2036bcbd28dd303ac041a31fa9d209a44ef50795590fe9abd81bb38db7`  
		Last Modified: Wed, 25 Dec 2024 02:19:39 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea873f9506330dd9096c06c86ddf5aeae6dfe621dfcfb5960765ec2c9251a95`  
		Last Modified: Wed, 25 Dec 2024 02:19:52 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d450d31baf94e8405e36a31eb7e9b2c2dee3fcd5d08f4f68f25ff6a0e827faaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bae39e06a4ad965359f8e2212ab571a45be9a5c5956670e173bb3dbc1063be0`

```dockerfile
```

-	Layers:
	-	`sha256:8f3b70b147c37ed8d6c99456de344fb2031278ae354f9c735dacbb5088f512d5`  
		Last Modified: Wed, 25 Dec 2024 02:19:53 GMT  
		Size: 3.9 MB (3933104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d99980963c9a4ccf630c30593aaa1b2ca192c6318ca07d627096ff1744aeb9`  
		Last Modified: Wed, 25 Dec 2024 02:19:52 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7ec09d90b1c08b2bcec6573ec48c34ffcee477df590f112d5bf99f53db759324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b2316f1509e6210f4a7ff1fd05f9d56b454ee1e277932a55d63987e31b9e49`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae635fb490f2cae4d48b0dab392e6924439a9ff0983598ad44c3dd59a103e630`  
		Last Modified: Tue, 24 Dec 2024 22:25:21 GMT  
		Size: 11.7 MB (11689000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237a27182edea584b14c266d7502f3b4115cb5c41028d75ef2bf5fa03965032c`  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4c41a48b8336769e9e874de5d168aaaf9803703bbb14816f197a1f92dbd9b0`  
		Last Modified: Tue, 24 Dec 2024 22:25:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a543f8d766a8e16660afc6c1d3a72a188d6b8797c95b78b2946f8393bfe32f3`  
		Last Modified: Tue, 24 Dec 2024 22:25:21 GMT  
		Size: 93.2 KB (93223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cae7fd7966c639f84dc900379fb668174ae0d07b06ceb03c208e5eab1cadf20`  
		Last Modified: Tue, 24 Dec 2024 22:25:22 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:373503456b67e3ba1a4da14b390432a88c34ecf706b129f85e638c01da436ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db20ecea7fbf37361af5c2c9ceb8f16fbe9d29735172b54c184ac38f14c4b78c`

```dockerfile
```

-	Layers:
	-	`sha256:4ca959f7688b8d655ebe995ec8d4e77bfaa76d4f9795313c6ca478ec35d3ce5d`  
		Last Modified: Tue, 24 Dec 2024 22:25:21 GMT  
		Size: 3.9 MB (3930767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446645abb9cdf6a0ab3aab2d89e42cef15f7b51ca7e389f1540b11a44b1f224d`  
		Last Modified: Tue, 24 Dec 2024 22:25:21 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
