## `sapmachine:jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:dc767f196bbb0dbf9aade6a8dd8fde46913ba341dbf756a264d348d9e5a569de
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
$ docker pull sapmachine@sha256:5ee5ceae5779d6bf468cd30c73a2d0a92b7d5ddcfec846e031d254d9d1beaaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242123914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84116fcfc3105e7579585390af9a25cb9186380193e67e01c37a8de71a0d709`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329126280cec58dc61b1f263ea2e76ac899ed981c8f771e6c1db2c7ca11ed879`  
		Last Modified: Fri, 19 Jul 2024 17:59:13 GMT  
		Size: 212.4 MB (212418761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0887d7dec9604a49f50414b6fe798e4e90d0ab4ed63e900b3a3a293f4a2b467f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2710df2ce5a15f0bf2b9b519806757d0c694a8cab9ee48f4cc32dea8637c4456`

```dockerfile
```

-	Layers:
	-	`sha256:9686292307d76477c5c0de19b13691838c08066e7724f86296026dcf66d230e1`  
		Last Modified: Fri, 19 Jul 2024 17:59:11 GMT  
		Size: 2.2 MB (2211291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb6df91a156250f030b45c92474d58f3db39bcd758f728fdc74de1fe09b27bb`  
		Last Modified: Fri, 19 Jul 2024 17:59:11 GMT  
		Size: 10.4 KB (10374 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ca769601b8b8e0ef359489c1039db44e1927c7a36ed65baff15a2a7eef1b96c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239259757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4b77f9e9db8924b6946975a4e00fdc99ae780f0891011588b9ff8211b731b6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85f274b92f637670ade0b9023f0d71cbd54f701e66b3c3d44af3012a2c9b1a7`  
		Last Modified: Fri, 19 Jul 2024 23:57:22 GMT  
		Size: 210.4 MB (210416714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6f182014bafc6aab4b8adeb1750949a0400a175b2af4bc7c01c02619b9cd38d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56816d5f4162783d623f7b3739c58270d348738e157d17ccbfb8f3c39b46223`

```dockerfile
```

-	Layers:
	-	`sha256:1bac3972ed339fb635efac115ed0b7f7d92e9b631650a0878fe797b3dfc0ba47`  
		Last Modified: Fri, 19 Jul 2024 23:57:17 GMT  
		Size: 2.2 MB (2211178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d0978d675eed78897f31978589eddca4240aafc18429a7e20c8cefaf2e5737`  
		Last Modified: Fri, 19 Jul 2024 23:57:17 GMT  
		Size: 10.7 KB (10735 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c5b566f6efca7e65f3c286d33282f66fde6c68c4801110e19150308e86d85a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 MB (247952032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74e798f54f18e3232b2296d137deb5b11221a7f1623f15b15f0746ff13cc340`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7add7e3f3f98a952806bd48a4c3cd7c7e80b4c47624305a7fdda5ea48cb11b20`  
		Last Modified: Fri, 19 Jul 2024 22:51:35 GMT  
		Size: 213.4 MB (213446003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:47a0df8b3e2e8b70e087202f806ca3a2e273838877d5afcd7b6ace2e1d52364c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370d9b5648fbfbd3f5e9f530bddd91134afcfbe373a49768e32fbf2398fa3e9d`

```dockerfile
```

-	Layers:
	-	`sha256:a8752d18bb24da7e76e4ad598a0bc9d0dafa69ae7113f584c552ad73d4c614c4`  
		Last Modified: Fri, 19 Jul 2024 22:51:29 GMT  
		Size: 2.2 MB (2212627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85079d9aae5c65eca242930a95742ddd05b97d3241499e34f921421635b983f3`  
		Last Modified: Fri, 19 Jul 2024 22:51:29 GMT  
		Size: 10.4 KB (10442 bytes)  
		MIME: application/vnd.in-toto+json
