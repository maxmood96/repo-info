## `sapmachine:11-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:930b570c8adffcf5a1f4b2ec9dfb8f8a4bae0527549d3ab572b8581fdd93609b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:648c0eeefbed0f5364db1cd144efa74c344b627033bab04f2b197202e4264bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230224314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045b81e0ca8ffe1d2d2d722d2fd37447b4c7a724c52957915a16719c28ece19a`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11774ed96e66050e2acfead86abec95cf7161cbb8a23c25e9c8f63b2865534a6`  
		Last Modified: Tue, 02 Jul 2024 03:32:30 GMT  
		Size: 200.7 MB (200690259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c8e79501dd99e0714bca43ef0545c4a1d2e1425f3733f956a7b73071db9ba41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4333da2f59468650e9b8a6e40520810365dbf8a6aed81d8c4a59773aedb978`

```dockerfile
```

-	Layers:
	-	`sha256:d157afa7ca4dd3a612931159bd06338e48d049616fb74a4a332ad0fc69868ec3`  
		Last Modified: Tue, 02 Jul 2024 03:32:26 GMT  
		Size: 2.5 MB (2460972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5cf64cbc1dd6268bbb858aa97d03d675227ea15a00eb8d42aaa568b3c8b4d5f`  
		Last Modified: Tue, 02 Jul 2024 03:32:26 GMT  
		Size: 9.9 KB (9901 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:23b98b3af39a0719f80758fff32486ed3c04009be9503a0eb64c5a2b3b968fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226527469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df5767fd46c6658783c3a671066979863c1b96935abeb38e242d433a2d63f2e`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a014dbc4a659d9ef0d863510763f3ebdf8c461f2ffe78c48338cf2ff5b32fc5`  
		Last Modified: Wed, 26 Jun 2024 00:31:25 GMT  
		Size: 199.2 MB (199165687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a5fcec9184cbcbdbdcf4d11f80959ed9a8f88c9ee41659a503b5739cbf10bfa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdf88a9af9313fc9af9d0c90ae3f0e2ffc0d42098ce99e0d6080ebeda12a43`

```dockerfile
```

-	Layers:
	-	`sha256:44d8a477b20d7f9fda91682ff13fb194d019d5cf5ab5fee4f6df0098e3ba1155`  
		Last Modified: Wed, 26 Jun 2024 00:31:21 GMT  
		Size: 2.5 MB (2461328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8624268f6dbe8bfe6a4cdc3eec077870d2aa151e9509bb068bdea493a643679`  
		Last Modified: Wed, 26 Jun 2024 00:31:21 GMT  
		Size: 10.3 KB (10251 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1238c87f43960b50e288ec33c53d254f8fad950d41051caa9fae31b225ea1e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221815519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1dd0ebfd0fc0e45303e36884a5ce6023b3dae0dbb4f3c4a2ec31a39fd8d713`
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
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25779fceb8fb3612399b3e7239d8d26e1822591d3c9ef6ae954c374c2aaa11e1`  
		Last Modified: Wed, 26 Jun 2024 01:14:16 GMT  
		Size: 187.4 MB (187354826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5217658132abec426e24b4321ea77ff602d803afa03cbdd3986a0bcd14a3cecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24391fe1f5c72d4edb81b6e1a565cc19de590c4c52515c47e750cedc0e7f11e`

```dockerfile
```

-	Layers:
	-	`sha256:68e205b2122def7f442b4320d836c40792bcba78fc33b3defd53f51c211c0e68`  
		Last Modified: Wed, 26 Jun 2024 01:14:10 GMT  
		Size: 2.5 MB (2462401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6b1af72acdc71234a0182f713649ea39235fa701b48f2e05d177c560082ecd`  
		Last Modified: Wed, 26 Jun 2024 01:14:10 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.in-toto+json
