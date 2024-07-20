## `sapmachine:22-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:71523c59549f68e6c19a35124fd3324ee74e4435bd962ab0620c7d4b27c4e710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:c99cb6dbf56749527b386d117bdcb12067351c8479a44c57415488d1441f0b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241535350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9682ea0dcd1e893d0c8bacf2e1959cffe656b6644b7ec945cc635d9a234d4665`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84eef85accd8616c6d563e515bd1672dc3df01dcd7fa353243b8f0239b0062e`  
		Last Modified: Fri, 19 Jul 2024 17:59:16 GMT  
		Size: 212.0 MB (212001295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dc9c24ab366d478af40cf0ed8f4c8158160891ff1f75dc8b5e3470d6ec8c0e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2a45de203d9f939a85575303b91faba303547b0496374c1de307c0cb70457a`

```dockerfile
```

-	Layers:
	-	`sha256:b9e56b2f1d88167df92b64338c176e71321967315e0a2d6b15675c8ad90f3584`  
		Last Modified: Fri, 19 Jul 2024 17:59:13 GMT  
		Size: 2.2 MB (2231771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f4db8cfb78ad71d61aa941e53c4aeccb6b3391c151f8c1705549913522a0ed0`  
		Last Modified: Fri, 19 Jul 2024 17:59:13 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:664717c14ebe76f9043e0f1adaca29636d3a18cf736f40398d6ce389e319d989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237320455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad698eda4a9239526428abda419bde1584a967679ecf8992f5351cc82302d4d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0e8cc8077ac15d303c27b496fa18658523b35296c965881769a139e127e97b`  
		Last Modified: Sat, 20 Jul 2024 00:01:46 GMT  
		Size: 210.0 MB (209960430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ed6c2cdeac334eeb85e62a0c451e3d36f690436e0e6694c46eafad19729c889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868ad6f4f6822dcafa224bb4a1cd3e92e5dbb3eb7155554b461bc52f99277465`

```dockerfile
```

-	Layers:
	-	`sha256:0f6ae88da5a45321258cd921ed36f734a6a62663872bd888b57e7326a733e561`  
		Last Modified: Sat, 20 Jul 2024 00:01:39 GMT  
		Size: 2.2 MB (2230834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d02480f66084d2eb6d1149c8da400245f1b5672a142e635d50b781c05e898b4a`  
		Last Modified: Sat, 20 Jul 2024 00:01:39 GMT  
		Size: 9.7 KB (9682 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:23e4df1b112baacada95d314f6e044912d5b337e8cabd84f2d159504f6412ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247378679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4045ce19162a0fbec88600d084b40f8f45e5c68fc2f70b4ba0287f15ab274f20`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba44ce493db445bfa9d576e0882814526ccdc12aee63bdb765f74c7b3b64fd9d`  
		Last Modified: Fri, 19 Jul 2024 22:58:28 GMT  
		Size: 212.9 MB (212917598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:077fe066f78207b7117c9574bf77249fde6673172c3486683bfcfe43fa12438b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edab897a389c93ffda6999599da5b7e66d420d50cf6d67aa27b8d42712efeae`

```dockerfile
```

-	Layers:
	-	`sha256:9d4c462c2e9332a1ef0ec158ebab59d1356d45696cba1a022f80bf7df956b5a6`  
		Last Modified: Fri, 19 Jul 2024 22:58:23 GMT  
		Size: 2.2 MB (2233124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9e524ab2a9b5c77cc17a7654af877c5a54de75b4a423dde396e0746b3376e18`  
		Last Modified: Fri, 19 Jul 2024 22:58:23 GMT  
		Size: 9.4 KB (9408 bytes)  
		MIME: application/vnd.in-toto+json
