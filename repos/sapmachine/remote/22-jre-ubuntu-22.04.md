## `sapmachine:22-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:9d9cf5065ad09503360ae73eee615c7c11f22d282aa35b72c95609dbdaad440e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:fb64a099dcf006e5260130027169847320360564e54f5513c38d38b282d0987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88667125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b496d4a0163b468860ff73b0f2917444b3e655cffbecb3c5bcd7ac35f209e19f`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:294f9501cb8f5b078c020494fa079a1acca96f6276094d0e5b92cb47602de299`  
		Last Modified: Fri, 19 Jul 2024 17:59:06 GMT  
		Size: 59.1 MB (59133070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:920535e6b026382ccc10ef1cc121c76b86b615e3bf93fe7ce4c0a4e35d8ab100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f526e2d5f3b3e6b647dc664687fc2a6324fbf7f500375ea0a01ac4b52952ea7c`

```dockerfile
```

-	Layers:
	-	`sha256:6803ea10bd7a7e2c6c6dde1aac44766f6f3e1eb2155075ea1a70e45af8697946`  
		Last Modified: Fri, 19 Jul 2024 17:59:05 GMT  
		Size: 2.4 MB (2390040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a786ba7edcdb38359b7e4a4cb769dabf84d8f21f803241e1e6c6e667d36083cd`  
		Last Modified: Fri, 19 Jul 2024 17:59:05 GMT  
		Size: 9.2 KB (9210 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:190968f0ddd8f2abe2b001b5c394ffb8d65af0382ef04b1b21f61abf37dd2490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85687525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8685c461df0fa8408af73a30ee38f9a5a8d6e45dcbfcc2a7af8d60d460ef16`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:dadf0073ac712f84ad733eeff6cacd7544179a18e1dcc3ac4dd1c6d14bc48cb0`  
		Last Modified: Tue, 02 Jul 2024 23:56:56 GMT  
		Size: 58.3 MB (58327500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08d7b571f5e53a802bd7a76bab9c190d0a513fcd87cb96642f91c0cd976441fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868a6e15d92981ddc4eaef4012678948920a92d48dc9912cf261a07dcf778ffe`

```dockerfile
```

-	Layers:
	-	`sha256:7b096a5f1ff17b79c0d7610348cf14287f402b729595f0d0d431951bf34e2c09`  
		Last Modified: Tue, 02 Jul 2024 23:56:54 GMT  
		Size: 2.4 MB (2359665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8db78047ac3fdfae6fbc72433d2f8039f2f51b1d92c2b5073f869484d686eebd`  
		Last Modified: Tue, 02 Jul 2024 23:56:54 GMT  
		Size: 9.6 KB (9553 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:884481b7efa91e6d9e3f21e2c246d41e5c2273ce29feade3c37cc54c162fe15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95230427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dfda923e5c7d0394b343f3038e5a85e4c0b17928fb23666950e5630764e91c`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:636acd77902d2f9b7c3b6668ea8bf29bf0d6834cbafd88466a2680e989679f29`  
		Last Modified: Tue, 02 Jul 2024 21:22:35 GMT  
		Size: 60.8 MB (60769346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cf65ff9de969a5072e962655b121f5fb014986881e705e620b6305c5dc3b18d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d7c895ab414c4f84ffa9f24a8737ede3a29e8acc20ad53225b4ce1c4b505a5`

```dockerfile
```

-	Layers:
	-	`sha256:b971ed3fdfff8052aa5f7ffaaf2d35ec06cd35bd3c5f039e7d910e921a1e5747`  
		Last Modified: Tue, 02 Jul 2024 21:22:33 GMT  
		Size: 2.4 MB (2363952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b18e6ca6fc6a6e1270a90997065984923efc49e471c0d811d1433afb106b2e4`  
		Last Modified: Tue, 02 Jul 2024 21:22:33 GMT  
		Size: 9.3 KB (9278 bytes)  
		MIME: application/vnd.in-toto+json
