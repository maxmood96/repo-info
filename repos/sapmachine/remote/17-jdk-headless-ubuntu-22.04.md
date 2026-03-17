## `sapmachine:17-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:d7f6fdf1a2217e755944ad617176d4394fa6ea353789ebba4757cd1d8d453112
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:656bdf6126a35f8691ee7706259da66839eed195f9abcdbc70c32ef337aa60d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229621403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1168e051fb2f86eaacc82eb1a6533d1f42e9a72a38db08499ac77d4e7b2ca5ff`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:25:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:25:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15048911ecd93e3d696a1abbf2f1aaffad7233d42e272c1be6bb210fe2b11b43`  
		Last Modified: Tue, 17 Mar 2026 02:26:09 GMT  
		Size: 200.1 MB (200082883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c553e7e4fd31583ea1a458df86b6236e298589abdca2adbcfa7bc06ba5310f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa2fa8ab31e36e88926ca8a00ea9c1de2a17c62b688bd4157682f76f7376c68`

```dockerfile
```

-	Layers:
	-	`sha256:54e4bb7046bfc69a0aeaabae54ffff5c78b3a3c643fe2db206148182c4b9a724`  
		Last Modified: Tue, 17 Mar 2026 02:26:04 GMT  
		Size: 2.4 MB (2378155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab254a9ddd44cde7464aa1d1f96ba6ca47b75308ae18bdcbb285e1418cd29173`  
		Last Modified: Tue, 17 Mar 2026 02:26:04 GMT  
		Size: 8.9 KB (8889 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:afe6f1f7ba35e86c52014cb132a77122193a5878f5197f65c05fb99bb2ba97b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226156606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438b03441241f3924e276d67bdc8535cfe0aeef6e7534a707b9416f1bae8ce0d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:31:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:31:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:31:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2bd5ad92b7c70aff043bfa27e383ee08190c1acc945357592b38d94bdc60ac`  
		Last Modified: Tue, 17 Mar 2026 02:32:18 GMT  
		Size: 198.8 MB (198767581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b62d7b7d3405f6715d8a1f5ede37c89eccee382cecac939c26d247a171a0add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ef268c738249fead85be96ceb25d84308b18e184c6aa2895dd88324d3e63df`

```dockerfile
```

-	Layers:
	-	`sha256:727d105ce35af38ff8cffc991a3a80249e874e1ad7adfb7fde085e2ba087569d`  
		Last Modified: Tue, 17 Mar 2026 02:32:14 GMT  
		Size: 2.4 MB (2377827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4355ea7b0b98472658e6fd202ffa841c97cd59fced79d31e0ef231d477f311a9`  
		Last Modified: Tue, 17 Mar 2026 02:32:14 GMT  
		Size: 9.0 KB (8994 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:146876cbb720560b0bf2abecc1a6776cd9d14755924ce376a01f032873d98aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235130435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbba17c9d150c307d95091b2cc1422f431d1e5d32c10e955d486c7c88cbb00dd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:53:40 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:53:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 09:53:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313d1fcf6f3da70a33c791693d3c452a8a4bab6b4d5a99177034cc2171fd7ef0`  
		Last Modified: Tue, 17 Mar 2026 09:54:24 GMT  
		Size: 200.7 MB (200676987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:72f51d0c3d1d334a5f88947df4e6d0f94c51a89c53dce2ffeb9f529befea1f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734e6e8939c327b3c576ce9a2f9b9cda206783add58f0bcd027754ad5e8c561c`

```dockerfile
```

-	Layers:
	-	`sha256:0990b32d0bd50fada8e4bf02ab50d3f464b64cb75e861c1b66ccb17df3ba525e`  
		Last Modified: Tue, 17 Mar 2026 09:54:19 GMT  
		Size: 2.4 MB (2375651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebcb45d334bec7ca57a2728c095ce3cb87b25b0d5bfee026b31320dbd56a8694`  
		Last Modified: Tue, 17 Mar 2026 09:54:19 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json
