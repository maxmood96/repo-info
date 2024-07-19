## `sapmachine:jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:a88fd8b70fc2198ac7f83b9be59fdd99eb46c24fba4ed34059d4ba7cc3939c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; amd64

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

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:88789a32ca6689cba4d8acddf560b7c38b8ef498f65bc67cd01819e72a82b9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237484116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f505a277e9e88084711818e6f2bcc309bccd754f3c920779b5458177b6c3a8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecf34c4cb32fd49f336dbfab399768b14b5dfa6fc393830aa723818a1a6c3de`  
		Last Modified: Tue, 02 Jul 2024 23:56:10 GMT  
		Size: 210.1 MB (210124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eb86cd08e65419dc3cc40a4e0677abd27a9eb93f7c96a61efb136240c7ede905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d398cd9826c1329e6499ba99ac777f22d2c98529842f283421c2e879c8fe344a`

```dockerfile
```

-	Layers:
	-	`sha256:f3ba3a3c1abb0f0b15527050c2a9834cd74413daf72db852b14b31b2c7f07029`  
		Last Modified: Tue, 02 Jul 2024 23:56:05 GMT  
		Size: 2.2 MB (2204041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1a6982a4cbee1eac2ff4fa64304ca79587bdd23237a3e6e75e6d6a92bb12d6`  
		Last Modified: Tue, 02 Jul 2024 23:56:05 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:eb31d8482fe491ecfd6fb46e28e323093063886d3fea39ae2553c066605b44d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247549225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5877868dd6cdf7ced38ddf48e9726b48b3d44b0437327a9686c79555f44386d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6799c90a640e44998365b1a0a6aa44c129fa3db23f0ed07565b2cd6b3138bde6`  
		Last Modified: Tue, 02 Jul 2024 21:21:19 GMT  
		Size: 213.1 MB (213088144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9e019bea472f98cc4fefedb1cf95e0e469295295749bcd01180e79fbf50c73db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2215752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146da4f9e7eabef218de39828166aefef81c1c804e22a0873350ab5565c10816`

```dockerfile
```

-	Layers:
	-	`sha256:70e8eea04165df21e31866075abc66c67494899663ba0b24afa7792f3004facc`  
		Last Modified: Tue, 02 Jul 2024 21:21:14 GMT  
		Size: 2.2 MB (2206331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8dd07e19695f4fea8be1c9128c6c189c40ae497c094ee6041c928d660b90a04`  
		Last Modified: Tue, 02 Jul 2024 21:21:14 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.in-toto+json
