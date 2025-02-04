## `sapmachine:23-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:83f7b248928806acea5209839abf21532130cbbb43f7dfddbc9cd13e0e25883a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:5bfbd9b1baa8147f5be2c32babe5f26019f891e066455c644d1d28906717d9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88087369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566a1e48beaa56c34a549c59ddd2962099491fe5588c7324a1b6af03f4a5a8c9`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ec13198891f64dadf66c337353da22ce904f722d1f3a8775cab9f6888a8448`  
		Last Modified: Tue, 04 Feb 2025 04:48:33 GMT  
		Size: 58.6 MB (58551428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b7f6885650b4a1fd71ad8b0efddab5bed413348373230389daeedb5a831b1729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff09758f6272c3f9516d7dc139ddbfffda16a81d42c13a9ecfe2c9fe890f1044`

```dockerfile
```

-	Layers:
	-	`sha256:39edb70813cf19f82d9c7b54212238a39639d675c27bf9309e3ec7c815190f7d`  
		Last Modified: Tue, 04 Feb 2025 04:48:32 GMT  
		Size: 2.2 MB (2168104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99fa6d186734b25c2c854c846ca97d23abb3e571399eb6458eef8060a5894653`  
		Last Modified: Tue, 04 Feb 2025 04:48:32 GMT  
		Size: 9.6 KB (9611 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:bf5fe7c37c0410d0d80e7a41b7b252cde910b0d11fac4f991261d85e0f283a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84940349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8f39baa98fdd8e0b200edad49a12e0896e0d0a830bccc8eaf27fbf186e334`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1471a6b351a0dd528b38d2d750e8b6525014585ff63754269471f9f4eb9aac4b`  
		Last Modified: Tue, 28 Jan 2025 02:28:41 GMT  
		Size: 57.6 MB (57582020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6d87e2421f83f201371c31fd20791c12bc76635553543c6a077a31a5ce89a7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d8a04dd3a0071ff59d53474538bd123d502dfd537d662517131bbc3f7b51e4`

```dockerfile
```

-	Layers:
	-	`sha256:8f8ff118eaf884df18cc1f45d76eb65ffb46a0049f29d6d776d6356c1af834c2`  
		Last Modified: Tue, 28 Jan 2025 02:28:39 GMT  
		Size: 2.2 MB (2167170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb419e237acfdad8ff2aa4c614e22261da3e483f3932e3bff5d5da9bcedcb58`  
		Last Modified: Tue, 28 Jan 2025 02:28:39 GMT  
		Size: 9.7 KB (9738 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fe982a976b34536754be997c21bbdc4e832a2883fb545eb8cde091cc98a92bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94281267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5526de3d1bdd8737fa036ddf41138db93a39bdd7401d91c79fe30b4667fc49dd`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880b986c07a94c88f00e36ebea7a35b8a0854c020a2fdf254b066e194fe76863`  
		Last Modified: Tue, 04 Feb 2025 14:32:26 GMT  
		Size: 59.8 MB (59833332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:39e060beb8ed2a7e166a9edcd46d312799080924a125d00bc975ddfc126de749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f1fd74128ec32ae425adcd034121f26e1dd278f2a08c0b1a21dc57fc6fa3a1`

```dockerfile
```

-	Layers:
	-	`sha256:543f700c3591a50e3ef88097661f1651934f694604f65d22deecdec138a63d3e`  
		Last Modified: Tue, 04 Feb 2025 14:32:24 GMT  
		Size: 2.2 MB (2171397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773c852f06e94ea0be9db74f20528669e96379782e073b3efc8a756541be6f96`  
		Last Modified: Tue, 04 Feb 2025 14:32:24 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json
