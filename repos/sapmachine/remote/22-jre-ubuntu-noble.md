## `sapmachine:22-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:05fdde974be3f116d18a6181b79e033dd16625e7033230f21a360563d48231bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:cdef57ea9a8e7f49af57b8b37047f8eef77b00eefbfddaac8cac1a8e04bdcb9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91663973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ecaf723ede08c227ffd03e0a6cfc5b338f7a0f70b192704ab3a948611a3acd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780c9ff68bf5f4aa5a04f18195a327a04453ff3adeb7ad792dfef50e1878e3b0`  
		Last Modified: Tue, 17 Sep 2024 01:00:41 GMT  
		Size: 61.9 MB (61914145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bf655f0ec5d6ad5777bd793b2586b7d58115487d99d4a56535a6be61f484b7c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833dc49e06c60021ab35f383f1f831a38506b294e4d992cbdddd5694764e6683`

```dockerfile
```

-	Layers:
	-	`sha256:a4e19c12ffc4021e02f5cb7e0531a4a67b10708dd77da09c36a9a0cc8112f494`  
		Last Modified: Tue, 17 Sep 2024 01:00:40 GMT  
		Size: 2.4 MB (2366249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9586baeddbdeaa36a5ea07aa881180751507600808b232f9da7196b2a8d3c9df`  
		Last Modified: Tue, 17 Sep 2024 01:00:40 GMT  
		Size: 10.2 KB (10172 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b071a204d47b2cae17ce3b01a2d78ba3a95b354b20cfb85fb076021d1d64eb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89664978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ab24cdf43acc029f4bf7375a904fd6d839ed109835b5b1c116222c74fc8628`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b508d9746d785425084a8fa2f7e224c201efc0d6f7170095b3dbb1efa8c10001`  
		Last Modified: Tue, 17 Sep 2024 03:10:59 GMT  
		Size: 60.8 MB (60779379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e814751a6517f14c58d7f945182f9383c4eb222f8660bb4bbaab809314a7a628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20a61e506ab74fab3181e5d67cec9322924cce291decb3379967740bd25123b`

```dockerfile
```

-	Layers:
	-	`sha256:806eaec5c6de09c5bc25f839976f15daa3b647125c89c520a830f7233a5002c1`  
		Last Modified: Tue, 17 Sep 2024 03:10:57 GMT  
		Size: 2.4 MB (2366145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4144b5f9ac9e466e48fcdab392f822287ff338fd3b3edd4b43bb774ac4e6545`  
		Last Modified: Tue, 17 Sep 2024 03:10:57 GMT  
		Size: 10.5 KB (10533 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0caabf8598df236e73acc6b84943ce6c1a9b77bd3f202525c446fbae9943e6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98097095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8693ce39e2f3955588d00225c29244d7d5c15068a7c1e8aefcc14a3746dcbdf2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec55be25442b052455b569312661d6c312110d7c91a325fac88366b23271285`  
		Last Modified: Tue, 17 Sep 2024 02:20:10 GMT  
		Size: 63.7 MB (63704750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:59d73ce7d0ae396f96628732c673d37cfc4b2602f66473cf74f35a728a597fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a242ac106567e64960fb01f068e67c4f855ee2ac9cdc8c28d0c1e1d294f04189`

```dockerfile
```

-	Layers:
	-	`sha256:82f60da7b45c2fefefb3cde059a1d46f8b3d513ae809a110d6eb74818d146cac`  
		Last Modified: Tue, 17 Sep 2024 02:20:07 GMT  
		Size: 2.4 MB (2369585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1382588ec36dbe92aa84a72ff25116b377074a7bd694fe7faf8d541c9fd39e1e`  
		Last Modified: Tue, 17 Sep 2024 02:20:07 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json
