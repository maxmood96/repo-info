## `sapmachine:21-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:f930ad39e2b446226a8ca9c48c693fc7bef85dfa49e94b3595d472b83b19fbdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:56adbb844b4872ed52cb5ecdd22a4a46b3881170b6999005af928f38a61e6735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89276830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7b69c7f07cadf6dbd7778d9476320fd8c5a6086293fa07525a703e11ad6ec2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:24:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:24:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a8b69fc93dd597bccfb622997c0585cd3e4d4f9b68a008469f8ca5de8da63c`  
		Last Modified: Tue, 17 Mar 2026 02:24:51 GMT  
		Size: 59.5 MB (59544837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3a63114833f8c2b9f062a5b12aab0cae6af560879986d1318870a3aeb7aec9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7199c9602442653da5a3a8db11d71d43582ae560241a3d78212966e90f05b126`

```dockerfile
```

-	Layers:
	-	`sha256:395c2790f35c708d5bc5947446a53d28d564f7af235db09bcee9a705df38441a`  
		Last Modified: Tue, 17 Mar 2026 02:24:49 GMT  
		Size: 2.3 MB (2275286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb7b69f0944fe66cedb1a5474a514cd1eb1753a97e453642e12537902b55b58`  
		Last Modified: Tue, 17 Mar 2026 02:24:49 GMT  
		Size: 10.3 KB (10269 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:422890dee1d60eeb4f92d96785e852da5d74f034d297d101b3555864656a7f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87603597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded9fa6df40d59d40a0b0202695f6244f1c179dfe42e07acb49360f00ada7f83`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:30:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:30:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:30:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96baa25af87db182117a5ca9312649489cb83c5500f7bb2a9239b47a087b3ff`  
		Last Modified: Tue, 17 Mar 2026 02:31:03 GMT  
		Size: 58.7 MB (58733888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c603392a35677c797ebb30c0b1e85f36ed2f48e0790c006c9c4739291224b48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e53cb3d4d2c3e630e0ffc8146970a13858c18e66ffa6e4ecd01d33369cca87d`

```dockerfile
```

-	Layers:
	-	`sha256:b7142f408d5049848d3d4e177e1e68c7ffc9ebc196176af00848fe5b75033e08`  
		Last Modified: Tue, 17 Mar 2026 02:31:01 GMT  
		Size: 2.3 MB (2275793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:692e17583dfde6d47fb6ad3ecfe77904e4678589dc2a76f73c8793c492ff63db`  
		Last Modified: Tue, 17 Mar 2026 02:31:01 GMT  
		Size: 10.4 KB (10421 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bddf460c3dcacc69ac06294619b41b492dd3f9f2c7b827fe3d3bdd27f9cf9f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95011734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e2941d65cacc00bcb8539f53d421b03833212e85e9dde428b7851b3ad5d134`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Wed, 18 Feb 2026 19:15:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:15:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:15:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311bb581ed0b0ae2266affa8ff0ba813010ac3372f0311a3005654bb4408ac7d`  
		Last Modified: Wed, 18 Feb 2026 19:16:34 GMT  
		Size: 60.7 MB (60704828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:833f7e973a58b88341a2bcb83caf2acbeff00cbaf08c2d98bdefce9758c3e1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6022b9f1b990a994fa707d57ce1d9bf978dca3af1c6742a1c0a2b0e0ce57a5d1`

```dockerfile
```

-	Layers:
	-	`sha256:f1b597d567ce2c7bf290b7a2b14906c626849bc06ab4bd8787cc963d0af5e89f`  
		Last Modified: Wed, 18 Feb 2026 19:16:32 GMT  
		Size: 2.3 MB (2274663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb069441dfa1d4bd6749a88d730a07c61f32c7328a15c06bbdd31cc9d300c5f`  
		Last Modified: Wed, 18 Feb 2026 19:16:32 GMT  
		Size: 10.3 KB (10337 bytes)  
		MIME: application/vnd.in-toto+json
