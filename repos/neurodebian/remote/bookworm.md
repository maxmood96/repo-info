## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:936d6b469fbff5c8a402abe66b09f4bf64c61a8c2f7b9f929bf555bccbdd3fa9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:bcf81a5101225a7cd909074ee0d0b3b0edee6f32ade3caa814b5ad284f5bf410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e56c3919c86f15faaf5a11a91cbcb6dc32337e086476aa1eefebbaa987adaf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1ec4595a3d975d4fe1463c119991d3b97ea186dfdb9beaffbf86d82f87256`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 11.3 MB (11273409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ea247c34b90330172a7683ea0e1d3552d14a478c597b3835fb3f8dcd6fff53`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bba4d323b5bde10a427f41b802e88ae13e2502d12a6f71543f41c638086b13d`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1983b6eced4bb9a5a3435c20a0e80be0f95ec3298d68729b3e3d51442d6e8c2`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 93.4 KB (93386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b30d613e90e133607300246f61900aa635e8fae8b149e443014a815ac31f051b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e08651d25a04d45e850bdb93958025e7a5be0bdaf86f2425a902274a9c636c2`

```dockerfile
```

-	Layers:
	-	`sha256:2db9e2cd120b4ce9ace4b747159ff3a6af43f8835dea224090629d18e284c24f`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce89be306770279efb86a1ccc18a50813f0663a5fab4ec216c7fd2e419529bfa`  
		Last Modified: Fri, 08 May 2026 19:44:29 GMT  
		Size: 14.0 KB (13963 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c383b1c8bcc59487007ea946c97be72b381f54ee51d5fd892cf0629fdeb1c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628c1e90e3da7350faabb21fc74a0c88da8663666dd19dbdb74ba907e12ef2b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbeab365177c9b941a081ba0b6d957ba147319fe32dff22aa2624a53a06f29b`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 11.3 MB (11252933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fa205d0d4d9ff7d136faa66f376fb23aff6334613faa278f84518f8e5c01ff`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14309867687b534670e51c1d96567476c0f1aaed795f789d0445fab07399b4d`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89033d9b2184954874f8f00b5a17aecc6b429a80a8e0038b84aa6ee81ff3383`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 93.5 KB (93546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ede2b6186f52eb37d412780815c7330d58d6faa9837786a7e5c79b52f572fd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ee394c617722eaa31b6265fd68e7ac215a0a018ff4f39c2985bca8c06e3347`

```dockerfile
```

-	Layers:
	-	`sha256:d4b4657e224bc234c23ab66a4c0a2fe772e905a9fe22fae905f739583d04c417`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29aedf8be25ddf5a7975ddb70961e5bb9c8359ec72bba50cbb2e61f0f256a671`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 14.1 KB (14088 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:4db04057176b65f60447ea0de14d71e589435efc93f5f9e0942650cbc343e201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d0d6bea08068fbb0f25ca7e55202dd93371d5e2f960b095b57d73b56802257`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb9739c6b4f68bc7ceda360ba82976ffea2a2b0f910162f3baaddf10c30baaf`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 11.7 MB (11693065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d4aa3bbcd7f103db531b544aa469fc669490bf0f63070fb63340476b4b2ff6`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f5291b6f5da64f52099bfd741111dd36b90a2fef3af20ec6d5cc367da8d4bb`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea8274562ed42a6906cd9cd33a459780630e229f388af5b5627ab5ae06b749`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 93.4 KB (93437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e167ffe5ba168b8cc58cf782364dda325b14826d22b80241ce109a8f1f87cfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c80c7632358c017feeb7106b43d3f8a70130d34fb57220e3a95f07cf348c3e8`

```dockerfile
```

-	Layers:
	-	`sha256:f6175cf9e3596d080ca37a17bf2e4e4756b45b06df58d192cd2d34c654ec1021`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e857221844e8f6652439e116a12b9371a11d1e340573ecc8b292cf063c8552`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 13.9 KB (13935 bytes)  
		MIME: application/vnd.in-toto+json
