## `sapmachine:jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:aa789915f8f24bd7cca7c26cf7ae24a3e3d3b0d18284383e7fefaec8327617bf
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
$ docker pull sapmachine@sha256:c836c6a90f08885663f6ad48d9539905f857c9987f48f86811cc2a7b977eb4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241727780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1283560733434a968a43c8e418faccd11b328f498ac5f2898100f8a98d58739a`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8af7642807b74e4fd4d9c7788a74056e9e4bf5d04481f93ba0bf200c07ed3`  
		Last Modified: Tue, 02 Jul 2024 03:31:51 GMT  
		Size: 212.2 MB (212193725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e90b7c3d560c721898b0825d93de04e8e8767a27c8519bf18b7d52f19a4b32e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25651a9491d58e6bcab5186e27cd1f9ff64455db03ea2ca891bea3713845ba74`

```dockerfile
```

-	Layers:
	-	`sha256:ec646ff7e35b7ca636a82f24ca31cecf003b12c9c35f219f881c60c4932d40ed`  
		Last Modified: Tue, 02 Jul 2024 03:31:48 GMT  
		Size: 2.2 MB (2204978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a0ee32f3c1b2e428ae1db24c856372374f0d3c210b4930df5167dafaa86c113`  
		Last Modified: Tue, 02 Jul 2024 03:31:48 GMT  
		Size: 9.4 KB (9376 bytes)  
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
