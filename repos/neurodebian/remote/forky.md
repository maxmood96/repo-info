## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:d5f6096a6a003f533e7c844997c6efa784cd8ab50e379117584c0895316a05a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:f57061aced5b88df44aa3221139686d245a805cd359f62e3a71f8f7c9c3a9109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60181755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7121d0b3446b9c3052cf5091a7bb78220dedb781a0c3d91d34dabde8f374a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30b85315dec2d58f35c416abc0e468c9a5fb485e83af8c76ba1b33292e721633`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48697206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c83530a6b51b03de05e55eaeecb58ea7b7ce335817e7289c21cefc0f862cb3`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 11.4 MB (11392191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d02498190a7406351e8a8b106b0cddb3d47e50d1b7880474dcd87e5dadde74`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543c19bffe03075382a45dfc91388da45cf11bf12ec5be4f33fb84234947212`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5270106ce715802dd9a6ba52b784375677aa57ea1f908f6657055fc3fa3adc36`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 89.5 KB (89451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:49dce879208c36525248f3b7d81cf77a7e45a99563981099c221033c55baf4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84c58a46f234563da19731d3792446c0a348b39255c47d65573ce856c991ce0`

```dockerfile
```

-	Layers:
	-	`sha256:963280b72f123e9ec9bc34ecc09368955c2c72f6338539252f0cced6feee7527`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 3.6 MB (3555633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d28a7d1dee2b324f02d370f9a9386e5558d48e4da78765b27a72b5a8c9d90b`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d2db333e4115682fce4df1e16d76b6fedc97c62b529c682a706bec75f471d3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59906141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e66451b03a9ef7caea93c64d629129a1f9d1211f13d464924e36243cb619050`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:30:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d4360d64f4e71c17817e39372cada00ee239c7d2715cf79f6e6cdc602a7cd46a`  
		Last Modified: Tue, 19 May 2026 22:36:44 GMT  
		Size: 48.7 MB (48720031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4576c4f7d45466740a199d54662cab12c85d21bc75740a97055a71b74822fb25`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 11.1 MB (11093120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a7a448cc8b0211eb9bef63518a33e6ab21d9096e89b4d32e81161f1b4437b`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e100d1e87b39987108ee142e1e682902047cbc3339a12200c2f6773805ef3056`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41863c941f5466e882167b32083d10a3cff9cb82e7186de9f4097e6bfb1c557`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 90.1 KB (90082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9c3438fe9c4af5de6d4d80b3d33125a7f7cdcf118c2ee3063e8d7a42175ac858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13987104def2f6995f2fe59b900687cbb3d9f7109576c03d65703666cd98da14`

```dockerfile
```

-	Layers:
	-	`sha256:7db5d6425f8abbb85f4075eeffe58aabf77d9534b67e80f7e686f18ac7c6cb83`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 3.6 MB (3560338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a85afa279224730598bd1b8225f47db376acdec114e15fd4c73c07fe25d2a289`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:229b368a6b98d7ce660433a55e8b2363a19a2f808ab9c873f24b05b1a8a7be84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61605870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075291128ef3150dc12f76a862c4d327c51305f9d2d92705a276cef92e88d3be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37fd7fd52239cf41c1513003560316f753d3b29bffb106c1c8cbf260e58621e`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 11.6 MB (11589003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b51446d80054a5f43c4ce780e4dc27dd69be5690c5515991223b5af7a9fdb9`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39c1cdcded0b2bce400d9caac28b0b5ddc7273cc5e5c057393fdcebbb9055d5`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3edebb8be1094d35833e792183bac8d8b69a4cce9b1de1627b384fde68c22b`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 89.7 KB (89744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7585901b3fcd61be98cc07c0fce812830eeccbd9bbbc4c73075927b5a94c6ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b2de58ad6d4212e7b4a3044a392c77b1cb7b570cafeb9b7a95c08097b9b83`

```dockerfile
```

-	Layers:
	-	`sha256:a5e656a37608c6c496bbc4e3f21f2e6ebdd0ca00774a6b5e42196d97aca1ff25`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 3.6 MB (3554190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac42095d0498fb668d35a1880cc1400381b34697805a03ea4a3cef3243668e26`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json
