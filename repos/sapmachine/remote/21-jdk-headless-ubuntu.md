## `sapmachine:21-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:9c2398296ed22a4a16a15a1867a567921d5ceb1e45ed9b5b5c75845f41294a90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:98dffa77999e8dc12b6cfc6a1b7dd2cb10c7745c6f1400cd0ba311a28e97bd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245040275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8599aad648c08f6b3020f908770b68ec0970f2892dabc99f63f553fb26adc545`
-	Default Command: `["jshell"]`

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
# Tue, 17 Mar 2026 02:24:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:24:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e43e519e990b7147074f5ce481e43d3c156d779fa7c193b779ab3330ed7d460`  
		Last Modified: Tue, 17 Mar 2026 02:24:40 GMT  
		Size: 215.3 MB (215308282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3f81e328b0e67a292e975f4369bd8e1de29b414fa2aed31a7e3a2a57d4657e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5080646eba04895590373110c65868c2bfaff4c2cce7ed5f77286b0113fff2aa`

```dockerfile
```

-	Layers:
	-	`sha256:fab85ab90c6d0b09c22eb420b384253d422f272dcb03ebf9f4585838d6cdbe42`  
		Last Modified: Tue, 17 Mar 2026 02:24:35 GMT  
		Size: 2.4 MB (2358807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4351921fbecc3ca6ecec13b09f384f458d38e9e6ca8d38212ca8a9ffb80c103b`  
		Last Modified: Tue, 17 Mar 2026 02:24:35 GMT  
		Size: 10.3 KB (10274 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9e65233e150a68bdb1634204af33bc656609211e78def43507d6f459d6317467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242430278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0337eaf6712b08d31cfcfb3f02e1448eb7eac772660069bafdbca4a390fd546`
-	Default Command: `["jshell"]`

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
# Tue, 17 Mar 2026 02:30:31 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:30:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:30:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a7b3d694846bfb023f377ba0cbce54fa6ed58eef5eedc7b0d53e4d437c1c0e`  
		Last Modified: Tue, 17 Mar 2026 02:30:54 GMT  
		Size: 213.6 MB (213560569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3cbe47ac6fb67b967fe8710f9cbddfb3522d0f7085ba4c60ca3cf1910eae4bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e36ec0a702cf055eae22a37ec92d20041438a4f21ff94fb9c220ff0e61e4ec1`

```dockerfile
```

-	Layers:
	-	`sha256:26b2d5454d84dea11a77a69d1c9ce3dc034e22203db1c83113dc134c7f50b21c`  
		Last Modified: Tue, 17 Mar 2026 02:30:50 GMT  
		Size: 2.4 MB (2359314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68b393306f25a795fac750fc4901fabdf763ca5fd635ed95d9d48c1e4d76a81f`  
		Last Modified: Tue, 17 Mar 2026 02:30:49 GMT  
		Size: 10.4 KB (10426 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:47b03337f659cb0e8fdd018a24c1e1465d5f784d34b2310e7bdb85ecd3caa4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250504292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a6eea939aa6a0dee08bbdaa65c350cd88c999bd85b068147329216c43ae20c`
-	Default Command: `["jshell"]`

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
# Wed, 18 Feb 2026 19:13:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:13:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:13:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7ec7fb542cc79fb9e63aefa5dd76cc36e34319cf801acd70cffb67fc93e032`  
		Last Modified: Wed, 18 Feb 2026 19:14:22 GMT  
		Size: 216.2 MB (216197386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dba8b4f437be2b81a49eddddd65c3f753ec94a407f27433965dce27ea9f9d95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2a9647f31186bb81b197608b0d9880c420f7a650d39291052a274297c945dc`

```dockerfile
```

-	Layers:
	-	`sha256:5226e9ab083e7a676ac389ba5a172e3ebfb81a9ad1438c916809a9a4ac5e3767`  
		Last Modified: Wed, 18 Feb 2026 19:14:17 GMT  
		Size: 2.4 MB (2356238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e9354772f2f4dbfa9193e037c8155b4454c1d09c2c30c0bcedb578ae237ac9`  
		Last Modified: Wed, 18 Feb 2026 19:14:17 GMT  
		Size: 10.3 KB (10341 bytes)  
		MIME: application/vnd.in-toto+json
