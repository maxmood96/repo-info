## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:1f984d3cc4e6d7afc5c1064de5c8cdbe1d84c04e9fa917089f98b717359afae0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:3f0849fb6c09e9b0025324e62c81a802771a1cfde4548303f76a6e4295e8da00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256092006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b512cb330929c91366deab8ccc4a995d28950a2c5f22946ef9bf18431ef791`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 02:32:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8266a02e110cb2134e191660ee2e9e59bcc2ef71d0f5533b48dfa541ddd65bc3`  
		Last Modified: Tue, 07 Apr 2026 02:32:45 GMT  
		Size: 226.4 MB (226358547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1f8ddf24ec0d21cd456449bc96b75f9f1cd82b193203eeb05719a8cd08b5867c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2607038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fff46d8bfcdceedb0cc3096ca287c88f6ee6633e6764a7204fbe7bb9bb854cb`

```dockerfile
```

-	Layers:
	-	`sha256:de0346afc638f056533d0d39f94610e049a0e758d325551b499c30365aef136c`  
		Last Modified: Tue, 07 Apr 2026 02:32:40 GMT  
		Size: 2.6 MB (2594558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31fce449db3a5d8b48c367f7c294fd203da2c4dbb425df43ee00f1af57abb190`  
		Last Modified: Tue, 07 Apr 2026 02:32:40 GMT  
		Size: 12.5 KB (12480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:latest` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f90fb07fb7fa72529ac63a2925b6954db0c1dc38d4986ff2a6de0054a26000e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253109435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2331d92bf02483fe2486f73e6c963257e0a342437c52599419195b1ed2b0a5c1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:38:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:38:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 02:38:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e78fc1c0a6396b3a21b7cd7281de876a01ac981621033e1d5f2dc4b81420e3f`  
		Last Modified: Tue, 07 Apr 2026 02:38:30 GMT  
		Size: 224.2 MB (224235360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b4b003a479fd81b867bc8e6d37e7829075fdf77a732aa18f0c5fb8848e745795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2607895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63aa573ed98f675affae5f07e1aa6062f617907756f73d73acf3f367080915e`

```dockerfile
```

-	Layers:
	-	`sha256:da2a4865ddf1bad6fd280e604fa09785d7c30a63a739c8b434ed4e3ecbfd01f4`  
		Last Modified: Tue, 07 Apr 2026 02:38:25 GMT  
		Size: 2.6 MB (2595167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9eb5719786d813c6306685a7bad49615ddee895430ac29fbb00df19264f0fbe`  
		Last Modified: Tue, 07 Apr 2026 02:38:25 GMT  
		Size: 12.7 KB (12728 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:latest` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:875fbdcbcc9533e37dec914f814343ea7acc7efd09a910e662c4fd0f5b0809e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261929776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c34d2695382d32e88a55fccf6c7ea4149f108d3abd54f317f463d02aa62c95`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 08:59:00 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 08:59:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 08:59:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aa874c6c717d7685ce22c8aecaac19624a6dc23b2cd3d9efb9fa9bf5766190`  
		Last Modified: Tue, 07 Apr 2026 08:59:43 GMT  
		Size: 227.6 MB (227616442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f26af1bfca4d9ba78fbe7244cb46ab1f17a3775fe6dfd7aedd4db58764bb12e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2604136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c848378b9b4fe099f5aac44250ffa77b64796bc112876fbeb52e4365628fb18c`

```dockerfile
```

-	Layers:
	-	`sha256:e327fff54773a51d2fb44812b46b7a6f6c5867359c6fb01873bca3534e68d49e`  
		Last Modified: Tue, 07 Apr 2026 08:59:38 GMT  
		Size: 2.6 MB (2591540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:676a14dda70a204525eae2604854b652cc11cfd0b2467a7ee4e806215293bbd1`  
		Last Modified: Tue, 07 Apr 2026 08:59:38 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json
