## `sapmachine:11-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:23914d7e0e4aedb92c962a5842a85be3766e44e6742ff795be27d75383cb5e16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:1b003ca420411c852989062e2a1c2db7f8c3c026daeff30d15cd8776e41037ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229679454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8452685f7256e3c64bf822e38f350580c3d65fa0efbe299686bb61a1af63ac95`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cdfd73131579c16aaf7b23a3adb5e088b2f3a2963969e58a4de5c2e3eac452`  
		Last Modified: Wed, 16 Oct 2024 16:18:36 GMT  
		Size: 199.9 MB (199929091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2b6849011d272b39910ea1cc3362142cb0b2525109aedc11818ead5b0037d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4aa42e8579250dd618254494bf66fbcac92594692802f27ca18359a2d02e795`

```dockerfile
```

-	Layers:
	-	`sha256:7794520f27eb3dd4c48bbcc6ec63643732382ff21daf18e2df64f5acda95a9a8`  
		Last Modified: Wed, 16 Oct 2024 16:18:30 GMT  
		Size: 2.2 MB (2228290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df9401d710174c55a2d63437238722ced7197dbbe53b89e3d5cb377b3d95e78`  
		Last Modified: Wed, 16 Oct 2024 16:18:30 GMT  
		Size: 9.4 KB (9403 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b1b14ae226b19c1caf1ec24cb8ef1287e0ea16837ded769cbda2dd8155294312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227319870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d3bcb13c25058463d0dc82a237fcade47ac476f21d82ecec117c91c22aa5d2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce656a91ad3d68a436b43da2b0c7661836daa79136675a75dba4435aac6a7c5`  
		Last Modified: Wed, 16 Oct 2024 04:48:18 GMT  
		Size: 198.4 MB (198434025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c88edbf34fd1174e4eb94731fb9254b49fc601230f20a6c459d9d55056b56528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2238925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59020eaaf401cac22886dcf9a73eef555dae7de20bb1331c6ba2658a5d2ec026`

```dockerfile
```

-	Layers:
	-	`sha256:8147e9b44f201f791d6d9d27177817347e68e119e39eb12ea9c31746b4e35386`  
		Last Modified: Wed, 16 Oct 2024 04:48:14 GMT  
		Size: 2.2 MB (2229400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82048b336489fc6928e08b93a245f1c6ef0884246cf75d842ecaa91f141e0e18`  
		Last Modified: Wed, 16 Oct 2024 04:48:13 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f7559b651b818d843b1a7641fb968ef5c9ddb78bc858d99c80f13d565afc6581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220907767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abf298d57c3991d1a74502e07cb5c70593c839d337c610b8380579d9f9d38a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d32c6f321a6aed82b34ea5887a7f3c9d53a12bd1c0f08880acb935441713c84`  
		Last Modified: Wed, 16 Oct 2024 06:10:58 GMT  
		Size: 186.5 MB (186518798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:32028e653789c1f604cdfad3dce3e844d7ced7af6ea6e3f3a0e8a581433e895e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2239054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75e63bf0439013d0f420a421d5f63161313c4b150586e67f677e2c244100da1`

```dockerfile
```

-	Layers:
	-	`sha256:8fba7510921f855925d809e56c6a752f5c93ee1248ceab46a1a9e892e8cb1cad`  
		Last Modified: Wed, 16 Oct 2024 06:10:53 GMT  
		Size: 2.2 MB (2229602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5399d709164f648b209ed6eefac99539b1dab0f446888ba3da824150d1aa030`  
		Last Modified: Wed, 16 Oct 2024 06:10:53 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
