## `sapmachine:lts-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:1f7e724db5a957cdfe8c67876aa237e396fc694ec1f03e760a109779eafff4f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8117a4c393b8403f6641c5584010fe22f03c6867384806dc6d1b34291a7f87d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86997968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb54b358858cda9259195ad1722d29f9b773a778b0800ce557f17c208de180b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2538687d544ddee31f021d0022e5759b8146b46635fbf159eb06d1c594d10f48`  
		Last Modified: Wed, 16 Oct 2024 16:17:49 GMT  
		Size: 59.5 MB (59486908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0bce145efcecf8812ffda37ece4aef583bdc5ea7edc934fe8de7ea78b787db47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f075668b2312190bd46322ab31b5adcfade0483682468e32e50b97823db89e`

```dockerfile
```

-	Layers:
	-	`sha256:03b3c023d2fc754d5d41ca7c9e2bd5aaa47dabdd350b345c3892b00eedce9dee`  
		Last Modified: Wed, 16 Oct 2024 16:17:48 GMT  
		Size: 2.3 MB (2282217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b94dab6ab729596e1260d874f4531c3c89b27f1429f8cb8a806ce67f1a7765da`  
		Last Modified: Wed, 16 Oct 2024 16:17:48 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c6278e30b46ea448e0c0e947d69e48d5084cd7db525505c9c23b216520cbf840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84555161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c599b7b9f1e2d0ffbe5dae010b7647e81036192e555ec96d5452c52dc4a0a61f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d8943e5d442c7914902c47e848352c2b622c79b6521c1d00ee382438a43e01`  
		Last Modified: Wed, 16 Oct 2024 04:36:23 GMT  
		Size: 58.6 MB (58581333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9622d77bf4b7b9c7dbefd5419ca98f1a0f1c2267badcdf72f21c458ed5944a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db92ace24246240a48a1e0d4f6c38c84d2bc5dc992a0aedb2085d2bc3822e0a`

```dockerfile
```

-	Layers:
	-	`sha256:5ac9765b722b880affb28e6ccda62414cc1247db89e32b8784b765b0cf0eb66e`  
		Last Modified: Wed, 16 Oct 2024 04:36:21 GMT  
		Size: 2.3 MB (2281877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9145f527c8ad268b76f891f40de477af1c2d8ad1f81f04534323ba1988f461`  
		Last Modified: Wed, 16 Oct 2024 04:36:20 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4670337961e9d837354456751d17e3010ab64e0b6ea27fe944d901ee9ec9699b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92747874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c778ef4835f5f617c1ffec20920abf2481f1a9b6a015c27e2ec5d5ee99bdd2b8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0fc27ddf528e5292d8541c953c172f711f8c53687fbb3354fad4926ae4dbc7`  
		Last Modified: Wed, 16 Oct 2024 02:54:31 GMT  
		Size: 60.7 MB (60671368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a9c5b98c504c71b5301aae5e7f4c61063f6e65588ecab5c94adf07719fba262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdfe0bc66c2e4bacec73ed70e604eb3d8efc58ea162421bf5a3929f3c2a1831`

```dockerfile
```

-	Layers:
	-	`sha256:2c481b2b5eb465a36b20e5d343a4be8a8d0339d5f270315426be15f9e6bf4775`  
		Last Modified: Wed, 16 Oct 2024 02:54:29 GMT  
		Size: 2.3 MB (2285994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97cb6f1e914f801f15d445b48486b0c8b62abca4d77624490ab0846301ae8693`  
		Last Modified: Wed, 16 Oct 2024 02:54:29 GMT  
		Size: 9.3 KB (9313 bytes)  
		MIME: application/vnd.in-toto+json
