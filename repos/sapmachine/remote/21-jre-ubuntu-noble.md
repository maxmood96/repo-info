## `sapmachine:21-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:a412b684218b1ac34ee3918c844750fe3a25ca1ecdb562e04081826495573a23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:5ceadcfd6b9afb5d9429d678b859a6b5db8647c539710d87a911fb824da20688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90474322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e347c060c91604ccddd61c06594d772b3e611c0c128e696cf2b7c2054dd85e76`
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
# Tue, 17 Mar 2026 02:24:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:24:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2103bf0deb78a36b6f8347fb2904c569a8349e21f422526e6c094886641c15`  
		Last Modified: Tue, 17 Mar 2026 02:25:10 GMT  
		Size: 60.7 MB (60742329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:89cf1a6f827270951dc80dfe599e7e68d51f4e3b23764f43e954d2ae1c03aaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff6e936f24725fe36abf5c52dc4b8f419141d1423cf1e20d4adb2d39a934fc2`

```dockerfile
```

-	Layers:
	-	`sha256:eade8e4130cf93727111bf98f92e730e707515dc6022b52e54fc8b704d1688c7`  
		Last Modified: Tue, 17 Mar 2026 02:25:08 GMT  
		Size: 2.5 MB (2521108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8b9713f27b550ed84625666a182bb32a1504d805df26f54f08b3e0a1259cfe`  
		Last Modified: Tue, 17 Mar 2026 02:25:08 GMT  
		Size: 10.1 KB (10086 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c671fdb8dd9d94543d7398abf55ead9e094bb3386fe0408d6c84cd09c31263f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88803562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f4fb54e5afbd7dcaf59468adabb872b8b6f3fb18e1c9d61aef75ca41e92442`
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
# Tue, 17 Mar 2026 02:30:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:30:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:30:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3b8217a400ca6f5f3d95582b64b496f15a6aa60581e02d9d487dcc498196b4`  
		Last Modified: Tue, 17 Mar 2026 02:30:48 GMT  
		Size: 59.9 MB (59933853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a9553034df375a48d2351edfb6a6380406d75b548da38139289f812d8594c1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179dda0a4a3a6eb875c227e36f04b4369de3fcee87f849723ca4edb765f7dd19`

```dockerfile
```

-	Layers:
	-	`sha256:11d640d67d583c3eafea3853ac7523fbcb705c47d62f58babeaac4950f8b78e0`  
		Last Modified: Tue, 17 Mar 2026 02:30:47 GMT  
		Size: 2.5 MB (2521624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca2c10ab16518b720a5264ede74936d3ebbc00dfe27605bc58f25163a32ef8cf`  
		Last Modified: Tue, 17 Mar 2026 02:30:47 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:07f683cafc5715ecc0f9c289421a7e6fddab0e06f830500af460b78be2915b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfea1900d4e142e13063712c468f8a337636a130cc03823bcece3c8c57234c2c`
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
# Wed, 18 Feb 2026 19:15:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:15:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:15:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e697db08fb5c6a04a1a318f75b24e60c4a29dc744827ae10fc5a088c4a7f525`  
		Last Modified: Wed, 18 Feb 2026 19:16:36 GMT  
		Size: 62.1 MB (62077081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d6d12a5d1a51a91b35007f9d648a4327f4ac95d33089b4e3e27cc55cbfb17c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fbcee025f0cec13512cd1eba39862aafd0d8b692b67c2321eeba4d1d83f2cd`

```dockerfile
```

-	Layers:
	-	`sha256:f3bec3864034ed1806a47696eca42257aebd8c1900220ad3cc7252e5e6513237`  
		Last Modified: Wed, 18 Feb 2026 19:16:32 GMT  
		Size: 2.5 MB (2520566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79792400613eb2a99d9dc3ce121dbad313de67582f83e391b298e156c72f35f9`  
		Last Modified: Wed, 18 Feb 2026 19:16:32 GMT  
		Size: 10.2 KB (10153 bytes)  
		MIME: application/vnd.in-toto+json
