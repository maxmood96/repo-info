## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:3829cdccee4364db4c1959cfb67208062e1e9895a0f70d970201e3bf3f914b8c
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
$ docker pull neurodebian@sha256:a68c734c00b3698e7b11888eadb04a8991624b39bcf23290d300838be1056578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59864739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b109e02369ad91c522bb9e160852fce154742b03780232bf4cc904c120daf43`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b209413f350467a5ae5c418b73ac48d809463e6e3a290d3c1208cba9f34ab3c4`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 11.3 MB (11273289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958835a82131d9b249019b0445717bd4394054b82052fa141556a6d461bc9f80`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac5731f71ed9fc336e58efcce2de819cd14828671adaff420902f9ea091455`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b13f29d6faade6a1f514b290c009e4e3359f58d34d63eb1216860ad993e07`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129025ba31fda6ce65a428088c21ea0cea14bd38c373c8fd604bfd5a37d1e73a`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4e94433e88f2b411bb7b941a087ce937c99b12e028a35ad7e2ff891096fb5a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93eeca15a1daefa3344c6cee6c1ebd5491b3d9d6cd9da0063c9d72949d646ec`

```dockerfile
```

-	Layers:
	-	`sha256:aac31dcc3ceeda2a52871716697b75acce365af34fa105b8e1b5f4300226f219`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 4.1 MB (4075933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ba866a07c775385e7b15a1ddc70d503cab165741c7bdc97dbfe353dc296a8b`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 16.0 KB (15991 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:960268a0372f026e30de47583581420aab60507a81b59f30c9ec236c22d8beb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59728479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41ac9c5e150732a2c484624f2b4fa08dd0eea99f7668781be6b9c9dc59d69b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:30:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ea4a2729c69acfa17c3025a40f85513b1f8639dc8170799e6eec54c9c1bcc3`  
		Last Modified: Tue, 19 May 2026 23:30:36 GMT  
		Size: 11.3 MB (11252891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e1bb079ba66989f9a8f05c2354e7fd267fc98337b75e080b077d7f9d41a6e`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b8923883494084dd5136c060256ccf663838d09a4d3d46c8111d1cc801baa4`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad721159bb9271b363502e3e9d13a790c54d04a383ed7b61f4c0934f6812e79`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 93.5 KB (93534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb84a30c185b452bf5a889119a5572594d3c7d011797304bfc7ad44dbb80e29`  
		Last Modified: Tue, 19 May 2026 23:30:36 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cef5a64a1236af4f765b8b55512bf00b5960ae98634a89f831af7a3d3cd27f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49220dd3c313a7622e2379927a6d1d0d7d8298ffd7a53206ce6fbb0c4cb994ea`

```dockerfile
```

-	Layers:
	-	`sha256:183066e63f4513b84fc0147089b908d7f81c70d581695c94ac38738674cba9fe`  
		Last Modified: Tue, 19 May 2026 23:30:36 GMT  
		Size: 4.1 MB (4076175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebffd27b4acf3ef30f36b1a2650a111e7419e0033ca66b64ec53a948a253bc21`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7bc7df072b8d4192da532d04d6fead4b1e24bc92dc244d3039bd8a47c37f53fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3f5e69332c4e42d45a5f556b5626d9a922ed8e3e5702c07d3e8270f7a02cd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fd686c2be4701aa5e99504e0a0a231438cebab31803f9703d4f2817fcfaf3c`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 11.7 MB (11693032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c275dff193370be94cf6b05afcd2f50b992d61b429151ede147e0d16bd143`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed34c26dacdd7f022ad39094d3a0e7234c0e1adaf272d36639f4a548d0bb34a`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed24d41000306ac52cbf2623e08455d064489dded03b85fd01bce6bd72a7c0`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 93.4 KB (93421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c476f9525210c69f52698c6764a1dd93f0e3c72cb3941432ffad0b4dfe7ee5f`  
		Last Modified: Fri, 08 May 2026 19:44:53 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8707a48f987ea14bd078ac3746d28881d4119f0480d7627964a7d15c52545760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db7f5ae92125a30eea36bb373c2d4ef882b6f6936fbc0adf910cfc3e2feec4c`

```dockerfile
```

-	Layers:
	-	`sha256:f5e53c43561d0cbbbb39a871b900ba903431c52a26c9b7b5d743b6635d3bfdc9`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f6d2384fe0ae77451cec1bc567fb85d31e77c7b721f8bf337871e4e30ebdf90`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json
