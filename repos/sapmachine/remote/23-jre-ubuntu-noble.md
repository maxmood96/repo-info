## `sapmachine:23-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:74f22ecd342d6b6382715003605e4311b0a8e47c18f354e2c349e07352cef666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:cddd18f8784ebddf188bc161c37a04f8527566fc1e4f48c24a5aa8b6b9f9473b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89498798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c726139c5922710eb969caa0405a82527fe4d72c1c4a7eee6e603bac99de7c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f37912b94568f94ffb7b3e198e7b9166513b057924df4d348c8b6a84d011278`  
		Last Modified: Sat, 12 Oct 2024 00:01:07 GMT  
		Size: 59.7 MB (59748341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2be70187c36a500586ab9e173ce063888876825322ce0606fe21527ab14b3b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68904f50d5a8d2dcd258c569cb53224462d06c518990b7df098fe1cb14f3457d`

```dockerfile
```

-	Layers:
	-	`sha256:f2c9f5f7d6011b407aeda032b84f2d0e66bb11f427f4c1f0ac37aafeeb3afd41`  
		Last Modified: Sat, 12 Oct 2024 00:01:07 GMT  
		Size: 2.4 MB (2366526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4ac2e1f5ccf719128fed1a833b52972586dde92cb9d69df3bc00b82fb74efc`  
		Last Modified: Sat, 12 Oct 2024 00:01:07 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0593eea706b84b06649741799e7532c9268141278c77397a94129f2eea868eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87695259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de61b8acb9e5654f5905cfffb0164eca0558929e7cf21a6400201eb714e276a4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df2b3aaccd38a25269ff56c65b97c7c1c651a2fd094c992a6bbe5f173346df7`  
		Last Modified: Wed, 02 Oct 2024 03:43:43 GMT  
		Size: 58.8 MB (58809829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6f74e7d4a48482e65305d6bf6b43b77117cd2cbd515c5ed50fd7d12535bc671d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a20f769644efd44a46c6e98f837502e6723807801a657fb475c52a3865303bb`

```dockerfile
```

-	Layers:
	-	`sha256:08be3a64ade88af4713d1259ea8a45f23dc6df31912093ce83cb9af50a372776`  
		Last Modified: Wed, 02 Oct 2024 03:43:42 GMT  
		Size: 2.4 MB (2365747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4cd3332a68aa685e8e4609f23d0eb3b36740080c4138e5dac142327f7fc3f8`  
		Last Modified: Wed, 02 Oct 2024 03:43:41 GMT  
		Size: 9.3 KB (9283 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f67d56995e30bdca44c4ae8756da3acaf761c403ffa3b04d2ba29381283c1152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95675797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9b6e2c4cce8d5e1d4f6f189f3476edf4f7a42e625acb4feaaeb8375bb80501`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e110547234fd795b1c6d90b50b5df43ec509107fdf663124acb5e3861c38ef9`  
		Last Modified: Thu, 10 Oct 2024 09:00:03 GMT  
		Size: 34.4 MB (34389412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667d0940de375cd20174b128d3d44d158a5b1f3c30913f397d06da4f4fc6a0bd`  
		Last Modified: Sat, 12 Oct 2024 00:27:05 GMT  
		Size: 61.3 MB (61286385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7b7689b82fed069abb7a24201a8cdc67ce3e2dcf9e4cd1e16c720660e766279e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2074ee61f0a0513afbb61ccefa25943d77e0c74f4371edf81cf535805f58a7ae`

```dockerfile
```

-	Layers:
	-	`sha256:8eb81a8ea08b5233970fc10308ee9a694dd8d527ab6a187118e57c4c877fbd1b`  
		Last Modified: Sat, 12 Oct 2024 00:27:03 GMT  
		Size: 2.4 MB (2369844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cefbd94bbe1a9d677079a860e047b20da8fbe866bb887d2591f052e5c5f10cc9`  
		Last Modified: Sat, 12 Oct 2024 00:27:02 GMT  
		Size: 9.2 KB (9244 bytes)  
		MIME: application/vnd.in-toto+json
