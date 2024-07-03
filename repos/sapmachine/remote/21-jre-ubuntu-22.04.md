## `sapmachine:21-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:508fed8b358128b35ef0183985b0306029da0344b6625702b8646a367faccf55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:30f81e0ac6523a0859f543ce2f98d713a73345c20d494d5c98f4dec53cd1708d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89417361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408802fa6425616f5fbc259fccb7042b9f4fd5252df509d426e13624bbbf42fb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7318a6e5bf44ffaf32c57ed825312521f0eb3e5a7981607083300bb1dd79d0`  
		Last Modified: Tue, 02 Jul 2024 03:31:37 GMT  
		Size: 59.9 MB (59883306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2dbf04212e285a3f0196983536eb2deb3cb85546d06bad0b09ad287c7d231b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e799dfd33f7406db633cfbd6dbb1446e68bbb8c1fc1fcb1adbcdb81f058be088`

```dockerfile
```

-	Layers:
	-	`sha256:0ec0f806d7f0d18be9c61f8c4be40ba6c5e9ff6e284308d9a19fa29f2eb719b8`  
		Last Modified: Tue, 02 Jul 2024 03:31:36 GMT  
		Size: 2.4 MB (2359977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd49dbbe2a04388d5e717e83f73f2c235b523dde2e1edb818d4cd15c0a6de63`  
		Last Modified: Tue, 02 Jul 2024 03:31:36 GMT  
		Size: 9.2 KB (9244 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4b2e815ea275f4b3595adf0a3b7a00194efe3c1cb2678deea4cfa1ee20549f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86290808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f32999bd07b48a0b148c3b680cbbc98cc6b0af9a6adb9b1a0dac8969907937`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039176196596b8b83f43b8fc4f224096fb9e7603c16afda8313dfcbb2638514d`  
		Last Modified: Wed, 26 Jun 2024 00:08:57 GMT  
		Size: 58.9 MB (58929026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a7b652c1a9b568662aaa6f37e9bf250de31312cef02ecafa63da218af2ea8e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06825022d4a8866fccca1863a39a5c71ccbb5c2669a172c53d35f883c33630ae`

```dockerfile
```

-	Layers:
	-	`sha256:cb1c20f080f86dd0712ae98a8415667121743ce4f68d0334770a759f5ee0e984`  
		Last Modified: Wed, 26 Jun 2024 00:08:56 GMT  
		Size: 2.4 MB (2359681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9454270fc137d705366bc31c59b32175da8bef98c653cc1b230a2a3f502835`  
		Last Modified: Wed, 26 Jun 2024 00:08:56 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ebbb18605c98f1cee8034215fda227609f94dca9c6fee9d8750e4e3ac76e0051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95894228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d28ebeaae8a6d924406166b606a35443dcbe8c5f94c1e027a3e44994044d16`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e417c4b704d29c182e7a69b9b835595ecabb32fc4ac24a8fedc317f3fce92e22`  
		Last Modified: Tue, 02 Jul 2024 21:28:30 GMT  
		Size: 61.4 MB (61433147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ced66fa3285fa4a3bf91ee4293a0e36a362d29f0f64226e7c64cd5af6e7d18cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c797f63066459e6bc4d3bfba5f861e55ed85bd79020e475f0ab6a56806495e`

```dockerfile
```

-	Layers:
	-	`sha256:16f84be4aedb5727fa0fcf9a90d0631ce79b329c65de31b572c67c8b915fa3ba`  
		Last Modified: Tue, 02 Jul 2024 21:28:28 GMT  
		Size: 2.4 MB (2363968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7836f2711d87a09991d320301ff77e4dabe6c7b04530b1375c890d4cdf5cf6b7`  
		Last Modified: Tue, 02 Jul 2024 21:28:28 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
