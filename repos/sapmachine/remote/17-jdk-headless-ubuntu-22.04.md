## `sapmachine:17-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:83530f8efcb21f9e0f1aaa16f401691c2896d4198650c6eb49f44e4d9bc6ffc4
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

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b2c69f14fb0f43a62d0bd367aafdb473049d6ff8a1622d64ffd9e7f230a69a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224772558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6c8a25998a8dc87c0e254f2bddff20d347bd20ed14aca3c2becabaf8d6c2de`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dedb6123d9f32bbc5b21c68707808f1f912aa881212b0ff689b5c78a913be80`  
		Last Modified: Tue, 04 Feb 2025 15:39:09 GMT  
		Size: 197.4 MB (197414376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b28a20de9db25ca04f0138a30f8e9989b65ce499774f5edac6a563bd33e2def8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8639f80c315bbed998f0547027b25e49a2c170b1b3e262e0c0a5e4da6d8152b0`

```dockerfile
```

-	Layers:
	-	`sha256:d2b46d0ea970b4ee58be96fad8718b0c7eaefd2a8999e4e70044711264d43368`  
		Last Modified: Tue, 04 Feb 2025 15:39:05 GMT  
		Size: 2.2 MB (2247468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45fd316a394749bf24600211f802b22d7f21884719f26cd36fc91cfae8de43bd`  
		Last Modified: Tue, 04 Feb 2025 15:39:04 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1ff2785fc1fcfb03ef2c84d832fe30c1e645e670bb8459ef5f9837b620182a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234057305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3990608664b65a7a7ae254f08952ce02e2419568ec5ad8f1911ad28dd139033`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1fe41a4884440f6114ddf8b96132b2ca18a6f47d8129fd08782d6043f14300`  
		Last Modified: Tue, 04 Feb 2025 14:58:24 GMT  
		Size: 199.6 MB (199609370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a8ce9ff4f02555f1786badbeb2e9ff9e3cde9f8d2e1831e77501d871f4081a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dc804f76414948ad7e43db8d233d7f1d30cb646ddfa17d081c102e6d9d0a8d`

```dockerfile
```

-	Layers:
	-	`sha256:1c5f3ad226feb33c0a95b942110201af0ae28f174f5271e8a7da2a57b4cda049`  
		Last Modified: Tue, 04 Feb 2025 14:58:18 GMT  
		Size: 2.2 MB (2249761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fa54528273078c073a260aeee43b8f09e90495fbd08d9ffe4d29c6b0170023`  
		Last Modified: Tue, 04 Feb 2025 14:58:17 GMT  
		Size: 9.0 KB (8977 bytes)  
		MIME: application/vnd.in-toto+json
