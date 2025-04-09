## `sapmachine:jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:d05077307aeaec78df828681ec9c1ae29c3741bd8506627980a0ff0ee2afdeff
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
$ docker pull sapmachine@sha256:40c6e93d43304af0fb9a0f19e9df38f63d015f2794d45fcbc8b4fbf4defc87a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260332438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5e88ecbcaba01bf390c7a274f9ee16dbe38b3a3b9f57253e1ab84ed9f2b9f2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bf57f997a52e2d1372be43b3137975a147920338f7a3efa5ae83c383d7ccd4`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 230.8 MB (230800073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:40081a5e66cdbc2faeb2b194804faa72919e857c9376d01ba8db8edd5d0e6a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60054314650443526073733587b69f971a47556ddfb681681d1c8f65827d341`

```dockerfile
```

-	Layers:
	-	`sha256:405ba1367498acb6fbca6bf546372439760787db33597a561ee747824a9d4cfb`  
		Last Modified: Wed, 09 Apr 2025 01:20:42 GMT  
		Size: 2.2 MB (2240429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4858045cb1447c7a817932a9e363b97a58f139b9063b250a728ebe751f3c4ea6`  
		Last Modified: Wed, 09 Apr 2025 01:20:42 GMT  
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
