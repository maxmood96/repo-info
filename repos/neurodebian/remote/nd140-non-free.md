## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:d1a3754b493305398f325ea3a6592d5dda3b5504d2c56e650caedb603b7d0066
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
$ docker pull neurodebian@sha256:3a9843542adba90737d65b1d0cbff2e65ebc3cc6115b888a9f62bca64c61c078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60562386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2a3b5c2fbbe39e2c2b707c7f008b15b58b7e36ba37cecf4be273c9037508dc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:34:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:34:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:34:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:34:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:34:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:743b991b49b557d24658aa3fd7faa6c90234b4433dabd04078e1e4904b8e483b`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 48.8 MB (48836497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55492b41b4a9f1fb29f9a699f2bdb4ab3567a04da18e53990fac8ee9a5067fe`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 11.6 MB (11632195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71003c85ea10f480bbb3572783de51413eda378dc9d0c08c05aec0a84be02f7a`  
		Last Modified: Tue, 13 Jan 2026 02:34:36 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911d42b2d1ed754afaf35635f0d655e1ef533470f8e9407b3bde73984bf77ecb`  
		Last Modified: Tue, 13 Jan 2026 02:34:42 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3302faea5aae0cc4ae334839e449b071eedf8fe2027cc204e87ec6b6875d53a4`  
		Last Modified: Tue, 13 Jan 2026 02:34:42 GMT  
		Size: 90.3 KB (90346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db05db04376f8dcb0185846c487862ff8f945ce3bcb30a123a22c98fb07b7da`  
		Last Modified: Tue, 13 Jan 2026 02:34:42 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8867b289e3c3d47d9a3a1170f86568a18de42083acc96a6f44a2e354088311c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406a671b2eb198d3e70ec2cc3d0d6f82f86b98ed1472463bba0fa84492e0cf55`

```dockerfile
```

-	Layers:
	-	`sha256:481b24813c55a95c43ed835dbc9612dbfe3043d76ed1423bb19f49560baeb7a0`  
		Last Modified: Tue, 13 Jan 2026 02:34:37 GMT  
		Size: 3.6 MB (3592516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e0beae277cf0606ac0bd78a66fda9481dc7a527009e3542e06b59031c7ff6ae`  
		Last Modified: Tue, 13 Jan 2026 05:08:47 GMT  
		Size: 16.0 KB (15957 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:311f95d8c09f720583c8bf71fe7f6a89b4dda12c1383d28957ad4189fae03e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60199406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee76e1175122295cf681eed5d09471821de89695b8dbdc0203f5375abc37a83e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:37:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:37:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:37:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:37:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:37:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f0e1c9ce589fdc56e77162978a9037d5d8c63c2e5d6fb4fd4b325ce20394aa61`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 48.8 MB (48820809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840a5ae9b27a3ace79b3cf0fdb2bddc6e0106d136b74b66d524377fecce1c8ee`  
		Last Modified: Tue, 13 Jan 2026 02:37:21 GMT  
		Size: 11.3 MB (11284159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b04b69ed7b0dc312198ad357b2412c074128f959f7293aed12772b8024660ef`  
		Last Modified: Tue, 13 Jan 2026 02:37:26 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ff9f4d2e3110d267b69e9306e4a2c646baa86f11542e5890a5a610a3d81b20`  
		Last Modified: Tue, 13 Jan 2026 02:37:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624da5a767e899231c0f32b59b33cb218d6cd91826a2f6983521bf73ce77dca`  
		Last Modified: Tue, 13 Jan 2026 02:37:26 GMT  
		Size: 91.1 KB (91090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b7c6b056e0df9d0635f7da4ff9b04e3ae4d6bba65d77282f987483a0af1b94`  
		Last Modified: Tue, 13 Jan 2026 02:37:26 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:af4aa92e279c4915e30df6e7cd29dd117fdacc453c824e0a90fe24c7b6d57a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32574c6ac80df83065fa624f2b51be56590164d0a5cd3bb7ae01b53b0c76a077`

```dockerfile
```

-	Layers:
	-	`sha256:b7dd2f04643444f2e93834bcaf87bfba2f61ffde30c642adee29597f4ed07e2f`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 3.6 MB (3593392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958c23f7a6c9a93a6fc9cf4709b5056222a686e1d725659fcc9f3c9ad5383603`  
		Last Modified: Tue, 13 Jan 2026 02:37:20 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4e99c3c6e5582d78c9e78cf02a431906f358c74b00f4f0194cceadef329c0811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61816562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b1b6bb9725c2c422ea1ff4e255221a0d3b6cc81e7d5b5bfd1509bab991daeb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:13:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:13:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:13:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:14:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0f5a7611eb50e1c295ff4c244485263852c6e6c8f18836cf55dc8b5a4162740c`  
		Last Modified: Tue, 13 Jan 2026 00:42:21 GMT  
		Size: 49.9 MB (49944546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf06d6cadb4b597f7d41ef40aa97534c966810a7be12ffa98ba0c62d0b6d87a`  
		Last Modified: Tue, 13 Jan 2026 02:14:17 GMT  
		Size: 11.8 MB (11777905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b17d2a39e5656e48ba83c086e5b2cc1bcf80b3fa2bd447dedcd331732869dbb`  
		Last Modified: Tue, 13 Jan 2026 02:14:16 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c37104f12b85966a7ba54059613e4fb6cee349b2e91746262d8151289c2b0b`  
		Last Modified: Tue, 13 Jan 2026 02:14:16 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30667de473d81a94e4ead18b60fd01798a848e3638b2f0aca250844c57926eda`  
		Last Modified: Tue, 13 Jan 2026 02:14:16 GMT  
		Size: 90.8 KB (90763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1be9d3fa61a9e252b493065fac5b67a71bd9f7acb6ee3d71de5a31fa1e7bb4`  
		Last Modified: Tue, 13 Jan 2026 02:14:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a83992b948f52e474ce13a2d7219f483a042dba1531fa41ad79976890dbb9bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf46cf6dd92a6377c617e5a247502d0f0d0faa3552ddd363c849b3c85277b7b`

```dockerfile
```

-	Layers:
	-	`sha256:d99390adbd9fc049478e9f3b542594c7912a0d5b18a72b084290199625a8d438`  
		Last Modified: Tue, 13 Jan 2026 05:08:57 GMT  
		Size: 3.6 MB (3590474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3fb5f51573288a20fa8174e7c6f3d3943d5d35eaeeba105e823e4cbfab7236f`  
		Last Modified: Tue, 13 Jan 2026 02:14:10 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
