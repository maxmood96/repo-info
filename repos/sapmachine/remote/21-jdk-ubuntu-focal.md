## `sapmachine:21-jdk-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:896e150725b7785cfd72b5f2bb1ab73f9a2dd9a844dd3af8a416e7a2f1c6e76a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:36023bdf1c831689ef2013c0732e2ef8b1792138075e6e9566b7d47b69b9bc2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241628184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f9da12cdf62e4925710ae6aad5de9be51d982d272dfbfdc7276886b2602230`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745d98d84ab1340dafe7d582dd10635db052cff3e79c9f248e25fa0211cdc44c`  
		Last Modified: Wed, 16 Oct 2024 18:59:01 GMT  
		Size: 214.1 MB (214117124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ce28856ffc3e92dc4b254a53d9c4b1b4422a93b47b5bbb472f3a9e3ff8f617de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6aa3a58b531bfbdc0addced99b161b88cc9c068fdb8e4cd59c8a77a4c2b382f`

```dockerfile
```

-	Layers:
	-	`sha256:02551df5fd66e73ecd0b08e8ac626a17050f9b6e1d58bf39d6d26bef73732b35`  
		Last Modified: Wed, 16 Oct 2024 18:58:58 GMT  
		Size: 2.4 MB (2373837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e10c9194b7d7194e1e3cac782182f970b370a1aa7ffd00a69ba6219fd184f3`  
		Last Modified: Wed, 16 Oct 2024 18:58:58 GMT  
		Size: 11.2 KB (11229 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:38d916781d873d4ca946eb4e764f84f57353dc8295e29dca3eff98df4ae28fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238257126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be44c594beb1fd53cc4a5ef6d8f5df21d94e0d58bd4341ca784c848cb0f2f75`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3498bbeb95e41b9cf39a2a337d82c0f30380eee72c272680c64f21be55392aff`  
		Last Modified: Wed, 16 Oct 2024 19:22:35 GMT  
		Size: 212.3 MB (212283298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0ad9d82ef96653cdfbed86bf756d854639a581b5c656622fad6fc78f3ae82ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487d01c9b49bcfe5dab15970e691b6eca829e1b1479b25f0ab693b22ac85916c`

```dockerfile
```

-	Layers:
	-	`sha256:a2b8c0a626ee8ee3d4d8a9c0f2162fbd56b36d1566bd14603e5e5676836deef6`  
		Last Modified: Wed, 16 Oct 2024 19:22:31 GMT  
		Size: 2.4 MB (2373569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ef50f6bca5d151a022b2d198cafab68c62d643ae7b4d24b0792df1187710ab`  
		Last Modified: Wed, 16 Oct 2024 19:22:31 GMT  
		Size: 11.4 KB (11423 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f862299685140512ed94d7973df0f2db7070973dbab29f637e168dc7e0d51593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247114076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72c45a383addc3bcdc5a757b27d7cbf5e0d7bcc0f923486acff8220b00a4c0a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd98f323fd4937301b934556eda684ccd1fddaf32a20c5642f83fe364bc46ef`  
		Last Modified: Wed, 16 Oct 2024 19:41:14 GMT  
		Size: 215.0 MB (215037570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:92885261564e748e4efe1d90ed515163f182dd6d0e5f5a61b14796d4718c09d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f9fe98caf958020c1fa0142338cbefac758faeb8cdafee597467df4edea1b3`

```dockerfile
```

-	Layers:
	-	`sha256:1923522e3d0420587703078b7fdbbd24dded79dc9522ec4161e6ac4ca71d10f9`  
		Last Modified: Wed, 16 Oct 2024 19:41:08 GMT  
		Size: 2.4 MB (2375701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a6d781b88eaa9a9b117a894b1ad0efa30e45328901d94bb07d1577e863e56e`  
		Last Modified: Wed, 16 Oct 2024 19:41:08 GMT  
		Size: 11.3 KB (11315 bytes)  
		MIME: application/vnd.in-toto+json
