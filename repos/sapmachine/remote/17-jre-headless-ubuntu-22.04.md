## `sapmachine:17-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:68657b0d786f70e30b4de64020c3f363ef55555ac9b20287298c16dcc92a0bcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0d7211ac7ecaaa96e0a72f070affc488ca5cc5d934074ed26d3c64f8cdbd7fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82123658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b0d605b0045fa6fc1367fa44e4f165090119e23e30d742099f24e6bbf8e7d2`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:921242c83dab2fb4a4f202e8801f80f90d47441a112244d02d46582dfe4ed0ab`  
		Last Modified: Wed, 09 Apr 2025 01:21:43 GMT  
		Size: 52.6 MB (52591293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aa39c734eee4e5c79a447e8941053329528d2d62ec07ab01beb633d1f373999d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09265307e14b8aa4fc0252cdb133785a57aad774a924b5758412d5df0263b5f6`

```dockerfile
```

-	Layers:
	-	`sha256:c59316c53f3a75dceef65f953cf98a10b4f6c7f0d02c97ac1a41aae99107c94d`  
		Last Modified: Wed, 09 Apr 2025 01:21:43 GMT  
		Size: 2.2 MB (2164976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e87116d00afb3ea6a165313ad70d6e2a07e245dc5f19f7e85e66ed535f6505a2`  
		Last Modified: Wed, 09 Apr 2025 01:21:42 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:13ede1be2fadc08c2d385a6e165fb7c3c8f7507282f8a0062089a815e195313b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79349181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aecc0e79a1abcbd686f03351808705b3a2d6f9c713e6706a6d1a72eea260025`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:2e9063c5b9aff723ddd49375b86439afcabfeca21e37c5cd0a6e65922d284684`  
		Last Modified: Wed, 09 Apr 2025 09:46:35 GMT  
		Size: 52.0 MB (51994950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ad51f9160a3216d538c6aa8da134396f51873754bece3332cd2fb6c382b83ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4dac8d1f07aa3c88c3068ab1500a305e5c1b1722dafebadd503601d2919d1f`

```dockerfile
```

-	Layers:
	-	`sha256:c95902ffd74035835ecfdfa0f7276d7f187b4d626ef85a83b16eec76bab26ebf`  
		Last Modified: Wed, 09 Apr 2025 09:46:34 GMT  
		Size: 2.2 MB (2164648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ed03ab75e339dc6e6a3ed7105248e3ad65f0ecc63197658d417835f23f5537`  
		Last Modified: Wed, 09 Apr 2025 09:46:33 GMT  
		Size: 9.0 KB (9036 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ac20fbb97b23a30f59118087fe5819aa32442bcc891d6f4a538ddb4df2e63200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88369375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324204402f3940ad28691b502c0da713d854db2358bb24d8644873d1d20b6439`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:13c1b1bdac5ae8718c9477a774600dc114837a88516a8750047c02553cb6ba00`  
		Last Modified: Wed, 09 Apr 2025 07:20:22 GMT  
		Size: 53.9 MB (53926679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:31a3442a62f74d170b2d77b21f092ba3e116dd88a2bbea376ddf0dcaf134dbdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e0543719dcb3741def5f6bab91f21af220ba9be07d1249277c2da4b9dd589e`

```dockerfile
```

-	Layers:
	-	`sha256:a32f1f14024291e061a173761e61a04146a99b6ff60d107271a7d5e70079e5ff`  
		Last Modified: Wed, 09 Apr 2025 07:20:20 GMT  
		Size: 2.2 MB (2168887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5d4d912d1cc4ff529377240bd53db0c08bde8d180ac54fa85e9dc994b3ef43`  
		Last Modified: Wed, 09 Apr 2025 07:20:20 GMT  
		Size: 9.0 KB (8976 bytes)  
		MIME: application/vnd.in-toto+json
