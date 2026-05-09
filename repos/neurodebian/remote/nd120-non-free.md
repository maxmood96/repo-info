## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:9301742359389f2d2738c1f6decafb303e83a33da734b5262947586e3fdba70f
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
$ docker pull neurodebian@sha256:99792aa6ba989a7415f0cd2cb8e195c8aa99bb3c897fe33a7bf5c35607c275fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517d328014a4be6f7b02aa9d27f2bb76abc751cbc7e0234bfbde2239a7433a8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157e5aa142e191f389177cafc25663cf3ead7455488e9b3ae8d80faac203470f`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 11.3 MB (11273453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b139c6137c970e0c7654c2cbd7329fc30bb23de4da7928a386b807149d6d4257`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eae6607455a450e3b7448918a266a5499f18306d75cae839cf0e46cdac78678`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de341e23682505074c2fde67892b0004b2e62d8351a93b78e388774d57c92afd`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 93.4 KB (93413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2970b98df9f5f093f0122c8c3983b1b6e87287a424fe66b37b04e459da79b8a`  
		Last Modified: Fri, 08 May 2026 19:44:40 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:21531d38e6403bf24665a621472f6c8082e62fa42aa9ae11d4bf72ae1bae6da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4593617393e092d54b447d141bc3d9055d3dd3fb0bc63c086ec490b43db5eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a5ec5d989239fca2a2f74da4290145a9fc4c5111be3458d332ca6523993ba972`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9c958dd7a81bf5555df9c02b20af25ae3d95a6fbc3d76dfe60c15f229dfa70`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9ce456a29d55af753754c81bcf6c489b588e4ef8d345a25a1185ac4ed38d7067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83671130319d212529fed9657df2275a72b7a9972a90c7d4eeb3087a8c2e780`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297af71f398d804e9824bb6964f5f84de1d86338b03a2c087345a9e6adeae9e7`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 11.3 MB (11252932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbc6e93f45b3f4cf455734139898464377b66e14251b76f3361f3d34ed49b9d`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2bd671e957e80374283f5fb64814dafa746ed40e7cf68d7972fffd7054de17`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c4f363214c80dee9f62e6d8d410c16b88764ef3e641e1d8bc9231b3d9cae7`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 93.6 KB (93575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1d2f24bc5c69d6c727ad3568cbc4addea466c9b6cc928ea044b626717466f`  
		Last Modified: Fri, 08 May 2026 19:46:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f29b6635607465a6f03d6780e7c09679fb49ac9bb340deaae75b283f8ed832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3acb1d5d8d6cb02f7c1e8bd1cb80b8eb98d8808fa839c362abc1fbb0ad92f8`

```dockerfile
```

-	Layers:
	-	`sha256:c992b9778cd7c443812a6eca47e360178d13695c8043203be74e9562afd8f30e`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5d86f16916b238e87145c3058d5b9f4308cb209db7450c1e9f13152f33e5b9`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
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
