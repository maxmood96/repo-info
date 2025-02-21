## `sapmachine:17-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:57d7d0c45afd3a1891ad152075b8583b2c8cbcab9d63106cd0782de1584d35eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:33905c5d80aa3ae2baeabc6db4663ce50536ace5d20216fcbc9387de48651b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229456670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74274b4ba62a0030f45c2013f9b4e50b9b7015f9619f1deb805c14168386774`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a891226481e9ae5d3b6e7856f19098167ad854fb2cfd86137743eb9acb52e`  
		Last Modified: Tue, 04 Feb 2025 04:49:57 GMT  
		Size: 199.9 MB (199920729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:277f18357c85ae74e7abe1234afe58783f17878006ce75353dc105d3236938fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e0b965083d20d28291f2c124d4632283d5cf832cfa0cc7aa1e73f09b496c55`

```dockerfile
```

-	Layers:
	-	`sha256:76cac1af6e5157e274d4f589bd55f4a3653ecaa39fd0cc3bc0e4a120469fffb0`  
		Last Modified: Tue, 04 Feb 2025 04:49:54 GMT  
		Size: 2.5 MB (2491556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c9cffe8d15dce236dbc277893730f3c1e3117be69a8897e7bea0c098a35ed8b`  
		Last Modified: Tue, 04 Feb 2025 04:49:54 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7117c1ad5e008a42341121db0efaf2725b2beaefa78afc6877fd3fdda3c6462c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225984661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410bc33782dd1a29c4531fe95606f33831e46832736f3994021e040f4fa8835d`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:52de9f116b77b1aa980eff2a2e2fa7cc742c44adbf43e8f4212f6b2caea0c7db`  
		Last Modified: Tue, 04 Feb 2025 15:37:56 GMT  
		Size: 198.6 MB (198626479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dea42cd097b65e774ded9a71c4974c2dee17cf4e1f63d44999ede1b1803eba90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82b24a3dd6a9c6efc48f5a10c99af6dfc26bf44b89b34d725f039ff8223b3ca`

```dockerfile
```

-	Layers:
	-	`sha256:bf0ffa1d72d8a05e59bcad7dda96228467174e319d99712f3510a0fa690ac660`  
		Last Modified: Tue, 04 Feb 2025 15:37:52 GMT  
		Size: 2.5 MB (2491286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf09e2b3ed308148d43e93a8dcba2a14d36b62f0bc0185897faf85ffeaa25e86`  
		Last Modified: Tue, 04 Feb 2025 15:37:52 GMT  
		Size: 10.3 KB (10290 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c4bb6cfdaf22730070b05c70330d43e7c785e3194d381b102bef39e5b780045d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235451340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1a4134dc19c608cc6c7f98a1eba631fc103875db14e3a1f28ef181c65be963`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86980d08d992c4a1b4e9533d5ded5bb466c98a62d84f787908bd1246c688b735`  
		Last Modified: Tue, 04 Feb 2025 14:56:16 GMT  
		Size: 201.0 MB (201003405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aab666e1d3dfd85e064cf843b788e84e2aad0c4da167f3b2b51241c22339ee31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22e7966f1a6b65afc4db983f997bd47c4627219e4a9062e020cb3808642a00c`

```dockerfile
```

-	Layers:
	-	`sha256:26c35fcb3a0eb16675840ba723bac8077e81dc8ea0d73e16a3f77f25f1823fcb`  
		Last Modified: Tue, 04 Feb 2025 14:56:10 GMT  
		Size: 2.5 MB (2493615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4267ff482546f86c7a2c0924f16e218c3c8219d12ba5df3171097929b127bd3a`  
		Last Modified: Tue, 04 Feb 2025 14:56:09 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.in-toto+json
