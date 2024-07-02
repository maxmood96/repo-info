## `sapmachine:17-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:820542549c61e9b9ca62101c2700c9de188a41273b5f589f472b167cce7ea1b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b8ea7d1a5f73337b9c861c8e03828c1a065dbc5c2f1b2e2ee328411acae11a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81973325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4328a079e1f94bec9eef68873d0724ee80cda111bdf1e5a3c0aa6cb18601c005`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1052c73eed2cb3ed1fd0eaee8e676ba38143129ad2f98588453222f7a4f7bbe4`  
		Last Modified: Tue, 02 Jul 2024 03:32:11 GMT  
		Size: 52.4 MB (52439270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ec0d2766268451050b0eeb76e308f654d6114c5ce4a9bb0345d4444c0a6c34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2127455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b15433c6c1760f56e99b9d7f8d3075c7a6e8f8b2294344c9eed6ba9603e9dc`

```dockerfile
```

-	Layers:
	-	`sha256:6185fa4bd1454a8039e26673f6c5b09ea5afca084e48f86254a07181f36da08d`  
		Last Modified: Tue, 02 Jul 2024 03:32:10 GMT  
		Size: 2.1 MB (2118759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8b7f93ca0df800941b64bc8dea20ba69d8ceb2c22121bb7c556a2d069440c8`  
		Last Modified: Tue, 02 Jul 2024 03:32:10 GMT  
		Size: 8.7 KB (8696 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:019d66d0078ee1cde6a5f58fa076de4f3c09fac63c5f7834e217dd13199682ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79135955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4968f8898979b9b7d9ac9f6647b7ef71ecdc4c45fac4e8fff2b7092400216012`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c7a634ab9def42f36b14037fd1509602601ae3bdd257d1e6cdde32a591ede1`  
		Last Modified: Wed, 26 Jun 2024 00:21:41 GMT  
		Size: 51.8 MB (51774173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:91eb42dde1c44f962b5b484cdba4e7fd78dc23eab5d3691465d3051ae16a017e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2127425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fe072325f4210d711c35428bbb3d816daeddf7b075e8520343ed9cc8eef23c`

```dockerfile
```

-	Layers:
	-	`sha256:6a49111ecb7d259d3b2230a3f1c247a5a562742f0a981e37eead73bf21528443`  
		Last Modified: Wed, 26 Jun 2024 00:21:39 GMT  
		Size: 2.1 MB (2118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf7895a8a1b7d9b707898f56c82479023d5856c0d882d6391a02eda60b5b01d`  
		Last Modified: Wed, 26 Jun 2024 00:21:39 GMT  
		Size: 9.0 KB (8996 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bca5f98b7774d105795c0fc4daaca95286f29e341fc9a2e228d3117e9dfdf021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88202955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc8b48feb3340429b3241166022361a5515be64fb462824401694e80e495de6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60087c1cf6e72cfbcafb5480dbc60d438711f3429bb758a91c74ca1cb01ff4b`  
		Last Modified: Wed, 26 Jun 2024 00:58:30 GMT  
		Size: 53.7 MB (53742262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:812ea5f5674d81901826e1dee4ef158de9375d39117f3016f2c8da5847d0c09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630947c50acf7e6d7d7a3468f686ca2f6ca2768fd296ae596975addde463b0be`

```dockerfile
```

-	Layers:
	-	`sha256:3e88b24f4674307a7a0a10e86148cb550e5768b3dbab2a79210e247c8874e570`  
		Last Modified: Wed, 26 Jun 2024 00:58:28 GMT  
		Size: 2.1 MB (2122668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf287831ef59179f3553ce4ff46a3e57ff82be3d0ad3cd2af423dfa1f682ba1`  
		Last Modified: Wed, 26 Jun 2024 00:58:28 GMT  
		Size: 8.7 KB (8734 bytes)  
		MIME: application/vnd.in-toto+json
