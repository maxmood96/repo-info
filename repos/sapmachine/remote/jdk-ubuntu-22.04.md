## `sapmachine:jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:cf324fc7935e41c43faf1f2c69794bf96126a2e5ebe3f7d94a6c7c3788758b68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d876ce8733a1117e188f073951adff2a6acd4852ed34a19b877f7f8ea910f4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255512797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a990c47bfb48fbff07d0a53883730e51893de153a638dd411a425df5e99a6265`
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
# Wed, 18 Mar 2026 17:48:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:48:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:48:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d1fc66bfc603f1c866b9800d6dbe07aca834f447655368a480a841a989a82c`  
		Last Modified: Wed, 18 Mar 2026 17:48:58 GMT  
		Size: 226.0 MB (225974277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:58a8dbfe86fef52844a54a7d251615f59bb5c22a216625c949f2c49a68a25a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5fe08aa2274fbae990406e063f6f5286e089fb61ffbb4b1efbe318ed36a649`

```dockerfile
```

-	Layers:
	-	`sha256:382630dc3cf9db84578f53947378696b8893f1bdffc73a2497b5ccea50654443`  
		Last Modified: Wed, 18 Mar 2026 17:48:54 GMT  
		Size: 2.6 MB (2619593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a5345d11364afa8ebca088f7e57d28bd34f3194e0ed2a3c5e0e9bb2a5e6c5c`  
		Last Modified: Wed, 18 Mar 2026 17:48:53 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cd573fdff10a03e900b50bca3a736049fda55d7f4a1a7a3e3dc52adc63eeff6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251185897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b32bcebf0e1f71c2ccec3698f05ad349847614b69014f55d65201c876be8d16`
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
# Wed, 18 Mar 2026 17:49:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:49:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:49:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d44f038226283ffe0907b6cbccdd05767973d5415fefce02d0ffb1862b7960e`  
		Last Modified: Wed, 18 Mar 2026 17:49:57 GMT  
		Size: 223.8 MB (223796872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fbbf5a99bc9e39789575586be4a7be194d1a4874b5512a1f47e15b32bf3c9d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd72b8467ef42ea78de92b0a58c79490466b17001f63da0d437d6b1827ad9712`

```dockerfile
```

-	Layers:
	-	`sha256:b2e800aef6ee010428146cd0d10673ce3eb3a112b2957cf32af8b6b183b4bbaf`  
		Last Modified: Wed, 18 Mar 2026 17:49:53 GMT  
		Size: 2.6 MB (2619320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b63bdd8425c209a8437e3e9f0ed514ea1dd5d1d94339bf56354deefa0b6342e8`  
		Last Modified: Wed, 18 Mar 2026 17:49:53 GMT  
		Size: 10.2 KB (10169 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:08450040b016e53bcba95bbfe8aa5e3c09b1db50d1ee0b7ebe55f76b23420502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261583697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467be27dfa1f904225ba0b9290f7eaa68b271a61cc5ff18cc3d13ed43cc5ca8e`
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
# Wed, 18 Mar 2026 17:51:02 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:51:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:51:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b891c41ba33bc92109b859c37e85055ebf0fb6aad1fb1a9aaa0c9cb50526b1f`  
		Last Modified: Wed, 18 Mar 2026 17:51:50 GMT  
		Size: 227.1 MB (227130249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fe4a425a6bf8cf869b4fa50fa9cd9d67468d41a78ec57ceadecf429c36c26ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ac55a79a9b394dd0aeb1ee4fa2a55cafa8f630d528245f4861221a021e792c`

```dockerfile
```

-	Layers:
	-	`sha256:f9560f2b9d59ed5f2aaea6857c7e2c84c613c7b95318c3b598c7e5366ad4e899`  
		Last Modified: Wed, 18 Mar 2026 17:51:46 GMT  
		Size: 2.6 MB (2616585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5522e292f46e5e708f3f74f2b36816cc6e6395110036039153834743ee4c03cc`  
		Last Modified: Wed, 18 Mar 2026 17:51:45 GMT  
		Size: 10.1 KB (10086 bytes)  
		MIME: application/vnd.in-toto+json
