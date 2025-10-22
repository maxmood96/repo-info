## `sapmachine:17-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:3175e560025f5fca48143f59468d2c015f3590949992580e2c5cd8c1858b992a
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
$ docker pull sapmachine@sha256:41ed9cc4997f03f97488a376608ffc634b1645bc81412679886493299cc29a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228416597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63003bad76974ac0fc00607c78914d31863b3e14e5547bd6131b47065506abd0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56353d62117df78d6f8e2eab27b88478c3f63ec1a55a32e7755d070d191cd3fb`  
		Last Modified: Thu, 02 Oct 2025 15:39:54 GMT  
		Size: 198.9 MB (198879779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:16163a636e124b48d4e20bd094c03831df45a03c504c00f8a3829f00b3a91b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae53b16aebb74f3e280d2ef0ba598d5487c047842c6a84bd9b307a123893a2b`

```dockerfile
```

-	Layers:
	-	`sha256:dfb890bff68c6a2179c953c825920cff60b2b896797b6e942e0335ff7a73e349`  
		Last Modified: Thu, 02 Oct 2025 09:06:35 GMT  
		Size: 2.4 MB (2375767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3225c8fe3e8bcc012d074641dd144702ed78baa43817a471abef2bc1e4fe9aa4`  
		Last Modified: Thu, 02 Oct 2025 09:06:36 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:260cf498242da2cf66d1657666947458b3d2ed5d560c0a6ec65e358b8c8c2f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225122613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde51fdeb2aa22f657f553fd42df931e86c5ce9dda7027334be502dd7b604e19`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee2fe50d57ced071b011b570cdc7788896e21c4778caabfb827b86bea52df42`  
		Last Modified: Wed, 22 Oct 2025 00:06:45 GMT  
		Size: 197.7 MB (197739506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7271b27ad3d5a53f82522cd34db3a0d327519de9c6595c111f2ac18fc65995c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617fc5eee1a8168cc30e649afbb35f090857465def579af1eed05efef7e7a735`

```dockerfile
```

-	Layers:
	-	`sha256:fd998cf67943669b70aebcf6e55d188a269f2fb1f6376f0a1d107992944f0bd4`  
		Last Modified: Wed, 22 Oct 2025 03:04:50 GMT  
		Size: 2.4 MB (2375439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8993f51ce84b4bd5064e24c1b8cf0eacdcce7c47dcea7a7714bb422a36544b6`  
		Last Modified: Wed, 22 Oct 2025 03:04:51 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:312e398a1740abc95036ebacf55b3f88d5b8ed4958908e340971151abaa8eeed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233821962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f6c23c0752f8edec59849c3ac2066e4423be24f11a2bb1c416372883710be`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dad747e4a12a6d6704bf3072222540ed67631423511fdc4380f0d6eac5ec19`  
		Last Modified: Thu, 02 Oct 2025 04:51:08 GMT  
		Size: 199.4 MB (199375173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fc5ef0c4df2fd30f3ce2974ec83254d95147a28cf9d02eba2aa229df0575fb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcd2535f5997670f4a97b0cc55d6e302cb0fb06768212c48b3afaab00b34daa`

```dockerfile
```

-	Layers:
	-	`sha256:8cee16de4003663d305033447974e5037022e451ce8abce647f1f9b94fa8b8aa`  
		Last Modified: Thu, 02 Oct 2025 06:04:58 GMT  
		Size: 2.4 MB (2371846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd7cbdadf6429b1d6de15624e0b8cfa1d68a4921317e9e9148bef075ab63b68`  
		Last Modified: Thu, 02 Oct 2025 06:04:59 GMT  
		Size: 9.0 KB (8977 bytes)  
		MIME: application/vnd.in-toto+json
