## `sapmachine:21-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:23aff345c484e5c4d5eceb20e31ba3ad45b89f72f5d8d1b6c9db8443dc9d0be0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:ad750451eb61e269b66069be8823fd5245e401e77a41b37ff1cb9cec84b0c0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243242027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5007e5674b45795cd45ad3f17c83df10fc2d2bab813f7dc75eeb9c0584ac4e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb48ffa75d10fc3cdb927fb953c62344bf00d31295951c23a9f2784da00b3d2`  
		Last Modified: Thu, 02 Oct 2025 15:14:31 GMT  
		Size: 213.7 MB (213705209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b27b010b7e65572bc2714e731b1b0ef39d7ec856da5ac107f151869c0c161ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53fe3a9c428983a46ef408a1faf35e365f5f3bc1c3c8f969878a1003905edad`

```dockerfile
```

-	Layers:
	-	`sha256:92b68c5219f2b5df63267974d32820ea6c9df60d3f34ba2df0821f090f066969`  
		Last Modified: Thu, 02 Oct 2025 09:09:21 GMT  
		Size: 2.4 MB (2377630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9665ae95a964e19833edfa0e7b9a1d82e2380baf509f9a4711971912029a248`  
		Last Modified: Thu, 02 Oct 2025 09:09:22 GMT  
		Size: 8.9 KB (8924 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d3fe8df3f82eb7692c9e82e7ec1da74bb8178b00288c3e14275b8ea7ee462d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239347106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aeffe4a27c1e42f295ab39214e0a91f512b8f020969bd78f5bb75beb8af10fd`
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
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f2f6f491922c88e35d89e7278593650082254550b74da61e791f43ec3b80a`  
		Last Modified: Wed, 22 Oct 2025 00:06:17 GMT  
		Size: 212.0 MB (211963999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:258a64824666684eca1535ac2458a58491cf77e2ef2214c4722c81a6d6639319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f724dd801ff6e59bfb8dc1c63b7e356db22af0992cdf47d2d43ecedd4e3f6404`

```dockerfile
```

-	Layers:
	-	`sha256:66ee364d49431dcc6125963e511080235be415e355d89070fc2798e2dfa974e8`  
		Last Modified: Wed, 22 Oct 2025 03:07:21 GMT  
		Size: 2.4 MB (2377302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e8fd5188314be195c8765f9bcce7376710403ff66850f5634df90495404d9b7`  
		Last Modified: Wed, 22 Oct 2025 03:07:22 GMT  
		Size: 9.0 KB (9028 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7486eb88c2f20f0d31b93581400bfc725101003d6d4cafcdd51f6e2279d75c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248817213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4d8a101faef982b1e6cc6db115a41e2ebd0b66177f9267b1875b9fcd5cc460`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c3836c20bb6ca5d242845ebe73ea015e749102395595db01cc6e5fc4cbf769`  
		Last Modified: Thu, 02 Oct 2025 04:37:29 GMT  
		Size: 214.4 MB (214370424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e6a3e7c0b4e202abd424de1db5503619b6e0dc27cba34f9b8c5921c4538875d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb67b99f3ad7b328e86f5d35bbab6b4bb2f14a9f153d510e318adb8860daad7b`

```dockerfile
```

-	Layers:
	-	`sha256:757b31ba609536f74bca1ad596bb30bc313b1cf94937d8d5a5069c92e3e46657`  
		Last Modified: Thu, 02 Oct 2025 06:07:45 GMT  
		Size: 2.4 MB (2373709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea6c51f92dd1901242681dad4b5e362bc49be60b4a99f9b52290b2cc3390fa9`  
		Last Modified: Thu, 02 Oct 2025 06:07:45 GMT  
		Size: 9.0 KB (8968 bytes)  
		MIME: application/vnd.in-toto+json
