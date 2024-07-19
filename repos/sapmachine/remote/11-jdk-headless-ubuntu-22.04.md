## `sapmachine:11-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e6c8d35b6f522aceabfaf176177fb42dafa55f29a015b298e92a77725dce2adc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:031039a0a0e374fab95dad797a2282e2056c29c9c1ff2fd618f8bc30b4e62c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (229040852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942a5b9be92227ff0dd3a8902b5ec46353339ff16590a016ee181b177c68b706`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc14af9015edba9efb5d3c5bb74b55696d49d57dffcda5f56be5496bba4ed495`  
		Last Modified: Fri, 19 Jul 2024 18:00:57 GMT  
		Size: 199.5 MB (199506797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cf43d7f2a6ce86c28d42952e934510231a7e99e4a4d9b5424f360ca09afb4c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef022c2249ba535adc679d13e3b7a0b07827e81ee2f937be24049977d1ec8d5f`

```dockerfile
```

-	Layers:
	-	`sha256:a0f75ad98717e9c71d0e2795a68050a2d9455f68db7b7b31cb6ff9b484c521b0`  
		Last Modified: Fri, 19 Jul 2024 18:00:53 GMT  
		Size: 2.2 MB (2245890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded857992ca1011449b8af4be11e10d1f8094f6bb5ac6bb317f3b18d473612ad`  
		Last Modified: Fri, 19 Jul 2024 18:00:52 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4f6aa024d2e148d59d33b23c86e73f8ee9e4b04eb2f63b846d7639c4b856c0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225304561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7113fd4d8be7b58cf80c20484c1347acb31e36c40ef10ba5d91d49354519919`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1645e4c30c12a798284d2a1e36af67eb0d1a3f9ec04e7d8fe77697eba8c74`  
		Last Modified: Wed, 03 Jul 2024 00:07:22 GMT  
		Size: 197.9 MB (197944536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cb42b02382a1498151d0a13ee015355c0178f2bff4f72e9db49605242638365d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2230295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dcf0a89fc686434aceaf09052c15a0d45cb890996fbca522f6a395195a9147`

```dockerfile
```

-	Layers:
	-	`sha256:c6b83ab24198f8df11e148e4ad6958a9a317e403d4f6a582b11da1cd0fa81517`  
		Last Modified: Wed, 03 Jul 2024 00:07:18 GMT  
		Size: 2.2 MB (2221297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f247f436ba9fb75e78f9b022feac441e6af990824ead4cdbf82b1700c96dafdb`  
		Last Modified: Wed, 03 Jul 2024 00:07:17 GMT  
		Size: 9.0 KB (8998 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8f1d7de5f8d360faf240a45b1abd8a9487afa17514cf0942d126b41bd44db540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220416739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69936603169ed5584b49ee8e5f561e35ffd51685b3b4c94f229cfc3570d4bc7f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef95cacd81d92793e54701ecb6a9b9f839aa9c2423e4b4542ece3bfff92e23`  
		Last Modified: Tue, 02 Jul 2024 21:39:10 GMT  
		Size: 186.0 MB (185955658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b35a5572d9cdf95f7c37298915a109677dbaa86b8b4e3b9eb16ae4401d56ae25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2231069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8638dfc6b46e093b2686661e4d66a6dbde3c76b25f982cec72b1fc575ba340a`

```dockerfile
```

-	Layers:
	-	`sha256:9bf7e093a3db4632765c13a526574627f346ed160c90bb546b3ef4a2dd89a2d0`  
		Last Modified: Tue, 02 Jul 2024 21:39:06 GMT  
		Size: 2.2 MB (2222334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83959111566a68aee223ef798288e9b3b9af935acb24d67bb722b01fbbbc2d4e`  
		Last Modified: Tue, 02 Jul 2024 21:39:06 GMT  
		Size: 8.7 KB (8735 bytes)  
		MIME: application/vnd.in-toto+json
