## `sapmachine:17-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:559e2f9d5e630152ef887623579c572e6fe962f21ff313b00a5a943ccec295be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:2cea78de053a63b1c9c6ce5a1c7ac7f4484d00f40b19927b4d23356b8e00b960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83345559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fde22d5e8455c4e1ab17deb9adf6e01d2fcddf4639f0126df85a459e1b160c`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1c4d57f604531d2215157582a99f874c49cb1b116406fdbaaf07a6a9d90e8588`  
		Last Modified: Wed, 09 Apr 2025 01:21:40 GMT  
		Size: 53.8 MB (53813194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4adb5c78edef5bff2373b36896cb0c59e9a510ee8274caff0f1bafcfb09bfc5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d99db39ff24dc32152214fde203797609fe0eab456669f06d0a1f06f541e71`

```dockerfile
```

-	Layers:
	-	`sha256:ab4ba8c9b51f070f1c77026d2fa312f3b2187dba4ce3c4eba70d21de231b43c0`  
		Last Modified: Wed, 09 Apr 2025 01:21:40 GMT  
		Size: 2.4 MB (2407454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fcc131dff0b97ce87f3df3fc69077b2ca5a23b3259be893e3a8ac6e579d3333`  
		Last Modified: Wed, 09 Apr 2025 01:21:39 GMT  
		Size: 8.8 KB (8820 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:03c716b8a4315757c70591760b114f7d62263b0b52171941cadded8cb14de8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80572598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48c083129023ecc2b609543d8e10358ecb1698e4c8c5de4e0a02b513d2f7968`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2404f8589aea7a30e27a3167825f821b7a992c9c11fafdb5980a97e92ba1f5c9`  
		Last Modified: Tue, 04 Feb 2025 15:40:05 GMT  
		Size: 53.2 MB (53214416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d9ee7b3812e27898b80cfaf311a0c3e43d381302b8493a6eb21c493d4b03b679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b6f9d5071d669288c12f7fb63c53291d1f74bfb8eea4bb320444d043d75aaf`

```dockerfile
```

-	Layers:
	-	`sha256:413d661335b53ec334c01522e289e177508378ae2fed32d67233100820f1c2a6`  
		Last Modified: Tue, 04 Feb 2025 15:40:03 GMT  
		Size: 2.4 MB (2407014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d5ddf496d7cc3a2397a6039754f618b4232520996cb6af3054e154e554e6f9c`  
		Last Modified: Tue, 04 Feb 2025 15:40:03 GMT  
		Size: 8.9 KB (8925 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b1dcf74e4ee0b69bff24e9d332c7ceb49c6582e2bbb5d39484cdce044ad0e3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89760946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115aadf998869347cebce2afb84319c5589f697a9bab55363e368f813f914e72`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c05b0aaf75274357d5fe2fcf1de6b31e70e98e686ef6617e137ad03d994060ce`  
		Last Modified: Wed, 09 Apr 2025 07:19:05 GMT  
		Size: 55.3 MB (55318250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5e2f9d736634fb3e52b8685ec23c2968330f19e04ad921c11b3e1f0b4dcb5d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2420300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da22b221cf5a115e71034906b7097fdbdfa87b9266a7a577cd9a0cfa1c78b9eb`

```dockerfile
```

-	Layers:
	-	`sha256:94aad1f7a1942fb074ee6e14a9ed686e83ac591f866775ad94710f1c5c83cc25`  
		Last Modified: Wed, 09 Apr 2025 07:19:03 GMT  
		Size: 2.4 MB (2411435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c43ae63f539945620e10052c362dd3d2cc03237644df82a7e952c793cae391`  
		Last Modified: Wed, 09 Apr 2025 07:19:03 GMT  
		Size: 8.9 KB (8865 bytes)  
		MIME: application/vnd.in-toto+json
