## `sapmachine:17-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:9f03b240fc6787477351d458b904e9303a3e56e5f750f1952bb6560c9452bef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:55c4f583308136ca1f73f3f61a7b632893c30b1b014e945057e7330e4a4922e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82126037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4336dc65ece3c59bf7f15f6b0daebe91bb03e26a485f3592879735299d19a6a4`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:edf5368dc3e9a726be23df2f3d365f9d876f01afcc87557a4420dfc6f4d15806`  
		Last Modified: Tue, 04 Feb 2025 04:49:39 GMT  
		Size: 52.6 MB (52590096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:59b7a33beb5ccbcc4a199c66aace95da9c9f2bf6cbf1ec7ee76703e1b5741f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c475e08baa04359f4d81a67118c907a1997f7078c601e74abb987af0fa27bf7`

```dockerfile
```

-	Layers:
	-	`sha256:5688130f384f0ff3a2c7fc8d7ac67ff0b2d578546fdcd2fb62d68c80706e8185`  
		Last Modified: Tue, 04 Feb 2025 04:49:38 GMT  
		Size: 2.2 MB (2164888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ba0ddada8ceb91ea46dab19a5395cd86cf719832555d33c3c1d6dfc9089daaf`  
		Last Modified: Tue, 04 Feb 2025 04:49:37 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:478dc8ffd9b03cbf02d22d535651bd6071a17b045ff129d75f551f0cac5d3789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79347193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92db70beb2ea1fff22299a4ad79566892dcfebaf16a063a53489e9092cade585`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f006547f280e0002ce93ac65f8a762dabd96eb36bbfeef938cbd47d4e320f24c`  
		Last Modified: Tue, 28 Jan 2025 02:55:27 GMT  
		Size: 52.0 MB (51988864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:70400532a0e891c703859841e80150747c361d167636f275b43d86ba388c26ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c906d9a60932e41cb1cb6a224585db78920835148a7348e8f2d5b9796185a60`

```dockerfile
```

-	Layers:
	-	`sha256:ba8cbf2553e1c65e2f6fcd13a55467ae912a2060fca1424abae91731f8447a8a`  
		Last Modified: Tue, 28 Jan 2025 02:55:26 GMT  
		Size: 2.2 MB (2164560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b8ace4b35b2ad7e342a1879cbf15b44e2347af38abd678c31f900f1727c448`  
		Last Modified: Tue, 28 Jan 2025 02:55:25 GMT  
		Size: 9.0 KB (9036 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d64cd9f51ba5dafadf8efa0c4a09608adcb1192a6b0adda1230a3c6c0305b544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88379891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d7740f4a5b4d604a314e619b54ddb72ec8e3d0ba71d3696c147edc07d2e590`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:60481c705e89637757b324ca23413b50f42234a8b7413550f4a6171cc857b9c0`  
		Last Modified: Tue, 04 Feb 2025 15:01:20 GMT  
		Size: 53.9 MB (53931956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a2f9a3be4ec6030f6cadda3cbb9c54480caa8d414cc859ace3eb2d48d690313f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0fbf48ef8b74656808cd1c4e4f24cef983f097696e3319e92eb550b209ee94`

```dockerfile
```

-	Layers:
	-	`sha256:43afd42cab944cc9d66644c6a18efb6f94f96a1cfa00674d7f9be3b485f3440d`  
		Last Modified: Tue, 04 Feb 2025 15:01:17 GMT  
		Size: 2.2 MB (2168799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c3d5afa10a848fe7b20f2b2ef068808753c0857e15d1ed45dae1753f1c5dd20`  
		Last Modified: Tue, 04 Feb 2025 15:01:16 GMT  
		Size: 9.0 KB (8976 bytes)  
		MIME: application/vnd.in-toto+json
