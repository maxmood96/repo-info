## `sapmachine:17-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:898357b068bb12958ef7f320c96f4b92c3fc556ea0bec841f0ee5eb7925795d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:49f57930c94c5cde4a6ba4d3a290aa6cfea20fa220a37d621a2c7ba9cf47233d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228239006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b1771a691937d650e405a40b5bcb1c01854ef5468dbc69111ea45187a3713b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fea495c2008218a20a8e3393b23f2700e9313921de5d8a437b1c234d20f1e4`  
		Last Modified: Wed, 09 Apr 2025 01:21:56 GMT  
		Size: 198.7 MB (198706641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6028a86ff54aeaa67ca49bc0e3be9da729bc598d4478c4a00163757e84a96528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a515c62e9be21b97da8e936f6969370e3ba5f1189eb7f0379415aa3292f63879`

```dockerfile
```

-	Layers:
	-	`sha256:1bffad9b16c1470c8f50efaa9bbf5de863e07959313efebc5af8bc97eeb764bc`  
		Last Modified: Wed, 09 Apr 2025 01:21:52 GMT  
		Size: 2.2 MB (2247884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66de51a66b1b7927c8cb85e174798184ca14baa58bc5a1da728fc867f0f48f98`  
		Last Modified: Wed, 09 Apr 2025 01:21:52 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:23722eb3d663dfba3de859d3ed8b359b4eaa253092dddc748306d0d51e9ca6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224768291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef5ca649c6c9bcdee02f73baa9c2699e9ebe5c9914e63eeaa951ff1ae56ff4e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92b0a78100edec635b14a56a7bfe468b06b7b756718dec125a02fc97815a0dc`  
		Last Modified: Wed, 09 Apr 2025 09:44:51 GMT  
		Size: 197.4 MB (197414060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b094ec09e7ac027db374823a0f2cf916eaf3f40964e03779f89d9406368accdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ba4c145e27d39ddce83198b7dcbdc6458f3c0d4b10a02a2a5dde2634990182`

```dockerfile
```

-	Layers:
	-	`sha256:dbf7196b7efb6f97cd02b3036df912d6987ff1bc7bed0b0ba1c11dd34e906c94`  
		Last Modified: Wed, 09 Apr 2025 09:44:47 GMT  
		Size: 2.2 MB (2247556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ecd913fce28717a780fbd20ad318b2ca4da05e539d0b4bd2d873e6ae563a698`  
		Last Modified: Wed, 09 Apr 2025 09:44:46 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4ff31aad6a7909add5b32874d4c7798458d2bb875b5e980372a16126c3d0082b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234049220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5012463a8d06a19aafc7fe874fd539045e9b8338a943c33fce21e4874a22d879`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f89508685f6f15e5e1c44bdbe46169f057caba5f71a2eaa9dec7556ef1e067d`  
		Last Modified: Wed, 09 Apr 2025 07:17:42 GMT  
		Size: 199.6 MB (199606524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:17c39ba61325b880f3f014499088c4759190e0408859a59832f111feced0ed6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25422befd0f16722baf3dead704693ca1524b3cb6899eab5196216a6e62e3915`

```dockerfile
```

-	Layers:
	-	`sha256:81394c9bbd3c2e17195b6f4d5defae19b296f0e2cfa5e7f3afb2ef32f6e39fb6`  
		Last Modified: Wed, 09 Apr 2025 07:17:37 GMT  
		Size: 2.2 MB (2249849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c19d7e17d87c5c926e940168925627b301528e46c6f2ff443b78f2ebbeaac9`  
		Last Modified: Wed, 09 Apr 2025 07:17:37 GMT  
		Size: 9.0 KB (8977 bytes)  
		MIME: application/vnd.in-toto+json
