## `sapmachine:jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:b74e7b7c7e35ab032481fabd545dc25813a8d08d96708996c52052ab136b1a7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6d54cee57ea607c07ef62c2a9fda70eb470f5eb5b8af88fb399932fb13d7250b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260335086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9bbb1043de2a77b365879d1564c0ba7099c5e71370f5f1c449e6fd0b98e213`
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
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de4e5dcbada4f6009739f6007b4ff6d07baeb3f3b55b8ea708f5accd451bd58`  
		Last Modified: Wed, 19 Mar 2025 20:46:45 GMT  
		Size: 230.8 MB (230799145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b5d35e86a48cd7696eabfa36ca1999671719ea7c2adff3c010838fc13697ad17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec8e15f3b4701e4887c5a2780fc1de4661d8e5fabf1fe9b059c918fafc51f43`

```dockerfile
```

-	Layers:
	-	`sha256:b622a1f2ae9e219e5570980c9844da03acd038d019ef17ec5e1a96e6f9c71e09`  
		Last Modified: Wed, 19 Mar 2025 20:46:42 GMT  
		Size: 2.2 MB (2240341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba5f8b0a2e297dce031a91d97152ea422eed15611e15c9a28634b1fc77c36a95`  
		Last Modified: Wed, 19 Mar 2025 20:46:42 GMT  
		Size: 8.9 KB (8888 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cf87df7b766e606fdcb0de4e9561d228ae760514caccbd902af5c88d1a3ebf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (256036710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afdd64af589dd2d60e414e2f96d9f85e576b72b8b87429c098a006637c474c77`
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
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f60f7710c860ec3ecea7705756064b4866acfd9057bb3f4589bc8a1356db21`  
		Last Modified: Wed, 19 Mar 2025 20:37:49 GMT  
		Size: 228.7 MB (228678528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c5c5df726852635edfafd561bb18ad368dfed926237f8ff2760304ef233f8fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71db45b224f38a5a322ec65aa98432e7050e60951a31763cc926c1b6e087db04`

```dockerfile
```

-	Layers:
	-	`sha256:db06d61c4879211893aa487cf1c99cb31c5f8b282012f9d3723ac8890e63eadc`  
		Last Modified: Wed, 19 Mar 2025 20:37:43 GMT  
		Size: 2.2 MB (2240010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b164ff159cc601d74b18fb06b8befc26a5a22538ba2648860b9339eed929434f`  
		Last Modified: Wed, 19 Mar 2025 20:37:43 GMT  
		Size: 9.0 KB (8992 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b56158f489681ce22f205f5ea65354a0d219d69fa6f7ce9bdff8def10ab0ffd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266278065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb1d65aa88ee301eb48fb3131affb23346ff85b2d3ec6e5f36aa5bc755efc66`
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
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd154d49240f0b7c46acd854665b98e05059651f41ae48feeb7bfee3cffed0f`  
		Last Modified: Wed, 19 Mar 2025 20:41:09 GMT  
		Size: 231.8 MB (231830130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9ae415781247ee5e9bd7c37ad4da4378a04342ef46fedcbb339c72c6d27e9764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07bc87940f3719524edfe2879d25c6a526813a3544f66944102eef013ed6c32`

```dockerfile
```

-	Layers:
	-	`sha256:32d1e5a3c60c38579f55bbe3715945329db04d80eab12f24cc5bfb1347f04a38`  
		Last Modified: Wed, 19 Mar 2025 20:41:00 GMT  
		Size: 2.2 MB (2241688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9fc35d4026b7027b9efd9049705438140fe7ac7a96852d6b0b0cee8da769a79`  
		Last Modified: Wed, 19 Mar 2025 20:41:00 GMT  
		Size: 8.9 KB (8931 bytes)  
		MIME: application/vnd.in-toto+json
