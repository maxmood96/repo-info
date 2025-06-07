## `sapmachine:21-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:f98d1a6cd83a3acbc638d77148c4516a6e3e10e129de867508fd29e3fcd268df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:ea3c58d0f6d295c696c7ff4ef8bd306daeb0f07d030a94f6d956e086161826fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243646651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e007bd37ef56870891cb165ba98ba04d0e421645943335d17e2ca22275ec7e5c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7246b3b254f3ac4f9df92f31e6f089196db2464ea0b91a0e3fa118ac6b437dc5`  
		Last Modified: Tue, 03 Jun 2025 14:45:56 GMT  
		Size: 213.9 MB (213931314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:102223788ca610b512e2e9e1c4a84b80895f1328f5455450183ac5c754342cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2266405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec16fb7195bf0fcbe1db55526a9edbe1420f325fe8a5d0daa22fcdeec168fe8f`

```dockerfile
```

-	Layers:
	-	`sha256:5a4c051fa7ebd235c09b95c94a1061ea6d3137de5e474a643e344e15edb5f093`  
		Last Modified: Tue, 03 Jun 2025 04:17:43 GMT  
		Size: 2.3 MB (2255753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:debe9f6e3abc00b9791214879da07c8e22feabba178b3d71b4f33341b36bd41e`  
		Last Modified: Tue, 03 Jun 2025 04:17:43 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cf9019aa82932b512818fef2f29935de5605357ab8ad52b1aae57fb7409f7f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241036621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ebd1352d8aaf4f8a268d95786fd70a9f398f3eaa4142031c21252c3d6a022`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e3bc27e3b8e44a231b4fd09b5ddc0f69ac162e2e94f3fbb9609955987d3e4`  
		Last Modified: Sat, 07 Jun 2025 16:19:29 GMT  
		Size: 212.2 MB (212184722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6d1115e3f810d67689e7bd365f277dbfb334d18392016cf30ab292e002a1ac85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2267088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247380f8bdf4ef58be651acd512f322d7cd7ca661e0aa11759660ec9be22059c`

```dockerfile
```

-	Layers:
	-	`sha256:425701167cc365d188dc3afec18f8fdd62a16a3f9fed77f40bf90c757580ac9a`  
		Last Modified: Tue, 03 Jun 2025 06:00:14 GMT  
		Size: 2.3 MB (2256272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b00321e25339bb2182af5aed5aec5b488a71dce0b78127ef3a5feb6fdde0f8`  
		Last Modified: Tue, 03 Jun 2025 06:00:14 GMT  
		Size: 10.8 KB (10816 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:70c6c43fa53a82f5df6da9b43998ddef06451108db516ccc970228d95a444441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249475394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b33b70d20ce8e0c174ee17f8640fe46950745c019176ddf4445107054f7720d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ccbf79fa04dba1d013ea6a1d1e0249412f340f4eef7b105cb7a3daf6979b6e`  
		Last Modified: Tue, 03 Jun 2025 05:59:55 GMT  
		Size: 215.2 MB (215150184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:32b1616603de2ea2824c28d61b372d5da6332655acd7902e9cd9b46dd0a19162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d78b7a21673417c3d9d890290fa2d1b301d63ad4ba0c65b6a5ffb278712e39d`

```dockerfile
```

-	Layers:
	-	`sha256:04d352ee3d025450d0420a584d6e43453bada8d5cd750dc1dedddb623cdcd842`  
		Last Modified: Tue, 03 Jun 2025 05:59:49 GMT  
		Size: 2.3 MB (2257829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17c912d43d84928e905e8afb087e9448987bfbe5cbd2b113f978e7731bc6756`  
		Last Modified: Tue, 03 Jun 2025 05:59:49 GMT  
		Size: 10.7 KB (10726 bytes)  
		MIME: application/vnd.in-toto+json
