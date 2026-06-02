## `sapmachine:jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:c6214ffb5d476ebb047c4eb42de7c6b8630037a6b057d8a378af53245e0977b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:2afabf754b1b972af752338b238a6cae107aff9a4574c8a098e24e8b38781cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254925256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43ad3ef8a7526dae6da96707389865509a0ec3b5fa8cc65435eb56887baab02`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:22:58 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 02 Jun 2026 08:22:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1451e61c19df100e57530b4690f1423447b5bb4150aecd87f8829d08a96710c`  
		Last Modified: Tue, 02 Jun 2026 08:23:22 GMT  
		Size: 225.2 MB (225192451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a91ca122b4ce3327e6554983f3ae422f7a3843a5bae6726fef9784dc6adca9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b57ed33ffb60f4051cdd3435479ac1cfd03e3ca0765b642f61f69d962246001`

```dockerfile
```

-	Layers:
	-	`sha256:800d6f7a3f92247031fba8b0ccf66b58655be3a265f4f0e4decbf131a6b70f5a`  
		Last Modified: Tue, 02 Jun 2026 08:23:16 GMT  
		Size: 2.3 MB (2347676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86680c81a561f4392607934b6a9773218ce4847a5632ef8e1880a0169dfc4dfd`  
		Last Modified: Tue, 02 Jun 2026 08:23:15 GMT  
		Size: 11.6 KB (11558 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e424925e35b88af203807f0952b96b20d6eda1ec3dda8754b2324d6baa0d4ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251930060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0669c86daafadd000aa0cbe7656ded1a487322b5ce86f8d8e2cecbbc1b88f11`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:23:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:23:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 02 Jun 2026 08:23:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35917ce493ec37ea3971db97d4a756284b8c4c2395cd8c1e9f931e5247862fed`  
		Last Modified: Tue, 02 Jun 2026 08:23:39 GMT  
		Size: 223.1 MB (223053654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:365db83eb7336f40bfa2dffbfafdaf62e70308167f2bfd836b92873310440a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5180548ae98c4f07935f28a69bf5118fa8c0953f3e5e720b1750e2088e11345`

```dockerfile
```

-	Layers:
	-	`sha256:85e5e8c2503d1109f4d22761a20eeab4793efb40f6c6074d2c22ed84a3b88d3a`  
		Last Modified: Tue, 02 Jun 2026 08:23:33 GMT  
		Size: 2.3 MB (2348228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3f586ff15e6e4c3cf512e5d46744b100a424d5cb6edf0f08b432de55579f994`  
		Last Modified: Tue, 02 Jun 2026 08:23:33 GMT  
		Size: 11.8 KB (11759 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:99532c0628afeca2c9cab093df9883223178f2518a1606be477012e3027d882a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 MB (260575618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefc356fa933f5a32fbe248b70828ee3a8daa7c5b3375bfcddabb4fca15572de`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:52:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:52:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 02 Jun 2026 08:52:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5e245cca34af3e9ca6324e3f6eaeefc5ca825a623c2d63b275c8f15a27a5ac`  
		Last Modified: Tue, 02 Jun 2026 08:53:25 GMT  
		Size: 226.3 MB (226261519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6bd26bf4fc8205a9531389ca71eda7c69a7fa0a6aa69fb9d6fd35bc0527e2ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2356204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6c3bfccc71960b0764639d849063ba56fb0d9bf3cc5c90c5a832622d0e553b`

```dockerfile
```

-	Layers:
	-	`sha256:6a7e68d66d6fa71cf04be47123a2b8a16ee127bdfee9b4ce5809d8559a5395a0`  
		Last Modified: Tue, 02 Jun 2026 08:53:20 GMT  
		Size: 2.3 MB (2344553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45f4e7c618ea4ac54fdac800eb7b0614de17e8740ea4fdea2f6c24fdffa0fa84`  
		Last Modified: Tue, 02 Jun 2026 08:53:20 GMT  
		Size: 11.7 KB (11651 bytes)  
		MIME: application/vnd.in-toto+json
