## `sapmachine:jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:6727642b03f8938d2be49a5a76563c7576063b78b7485a00ce9d8636889917da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-jammy` - linux; amd64

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

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:846950add33457e78178870fa9af70c0886367ede9588c3077514f1fd78c264f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85495302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cf582df0acb43ac4f12fd7f076232dbac7244ece9b8ceebe48d723af72d9fa`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:46f51413c7f0906e09e4c86ddbde4b5c756f93ddf4ea010699b9e1aa4b1da8c9`  
		Last Modified: Sat, 20 Jul 2024 00:02:37 GMT  
		Size: 58.1 MB (58135277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:25613df503e57773c7b51c215be21076ee2e66e6c3c7f0c15dea72d08b4ce6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e878b100f1e4eb5c25ba92e690a540138c721686c06506d2b15a259e1f69a44`

```dockerfile
```

-	Layers:
	-	`sha256:359a7f778559b4c1e179bab0f78802574b651d15b53c5aeffcc3479da5424bb5`  
		Last Modified: Sat, 20 Jul 2024 00:02:36 GMT  
		Size: 2.4 MB (2389113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3224601b9ab7ccbbbac971d2a2793d4e1de2326262b711721a6e5c0c28e85e`  
		Last Modified: Sat, 20 Jul 2024 00:02:35 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1b838ca8806446400a6f0fbd91346e38cb052fb086185be7b6ec44e950ffdff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95035162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7b93373f7bc40fe78083d31f3d3753385a72fd55cca8698490b960faf65466`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:ff536e4f2306e3debf320bff16b2ed1c068c50587992791fb579458980d78e81`  
		Last Modified: Fri, 19 Jul 2024 22:59:57 GMT  
		Size: 60.6 MB (60574081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2418e685d2007657cf025856766b9c118d1a021aab7f5d15e43393b30569bf42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca763ec53335820f414c2350abce03be926ed9ce397e931c0a3ef0777dbff8a`

```dockerfile
```

-	Layers:
	-	`sha256:bccbaae4f77cd05cd2035eeb9b1bd10469283807a27932d3bc0f6fc2ee71a935`  
		Last Modified: Fri, 19 Jul 2024 22:59:56 GMT  
		Size: 2.4 MB (2393400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:943128ebb70611eadc418ee9911d9e7e0906a57c46359c1ef08862133579bbe7`  
		Last Modified: Fri, 19 Jul 2024 22:59:55 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json
