## `sapmachine:21-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:a8592ac0f81bb26afb74014cf5b77baf6c43d9bc3f4fc56cf376c1d385e4fe15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:f545e628026cf50910fc96c9403074d66b9b2ba8639bedd900a5f32e727568e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243648295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de904fa228ba520b4a6fa5806ce43170161349b65da70aeccb09c59c431ca433`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fe71f638f170277d79e8f17116cbf8ecd1c0dc64b7b1d25536cdc8fff2301`  
		Last Modified: Mon, 05 May 2025 16:37:06 GMT  
		Size: 213.9 MB (213930766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eea6a19a0f0e61f6369fa0459ec879b638efce6acf60adafbfc2ce42876e0f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f30b083280d8836e997dccf50ace45c3e54a704dc58860d42e7236bf4a3c00`

```dockerfile
```

-	Layers:
	-	`sha256:67ea760a8cba7cd9752a257a5c57527838d172b6a884dde560d53a185dbccd10`  
		Last Modified: Mon, 05 May 2025 16:37:02 GMT  
		Size: 2.2 MB (2234509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a82eaa9f920772c97f5857a0cd54e384dd30a5503b37d2716ce16e06236b5ca5`  
		Last Modified: Mon, 05 May 2025 16:37:02 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1258ce63e0665500268013d8e5b2e8b6ad1d7f2718885857b4464697122ac728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241030804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7754bae6c0dcc67649fd30f6ba5f2cfd25ef52262c6a60a7875677d222ac13`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d93b505eb5c7dc6c813be45212f4c9dbc255c296214d37b43ffaa4f77dfa991`  
		Last Modified: Wed, 16 Apr 2025 16:27:00 GMT  
		Size: 212.2 MB (212183846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:89385142624e3f6e82cd9a5f0183e09ec3dcdaa409327907446546415910704c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e830d602380daf939aea596f5c45d13d3151ff7393f0f7b6ade68068c2a39d51`

```dockerfile
```

-	Layers:
	-	`sha256:3018c94782e31354cad07c2e96a899c17a55147ec68d94be26088a86bc04b3b8`  
		Last Modified: Wed, 16 Apr 2025 16:26:55 GMT  
		Size: 2.2 MB (2235024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:476ab9412283dbf0aef114980333faeed666ea9e862187ab391fd059c0831e41`  
		Last Modified: Wed, 16 Apr 2025 16:26:55 GMT  
		Size: 10.8 KB (10816 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2eb1f19332208a8200edc069d58b692d6716c889b152800034ba08e7274aac9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249490721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48f69359775a7c7ea43ecb568ae16596ca65f4532a904d9771c9732f2d528f0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59e9359247ed387fde45280634650ca872dc0496a2523e8fb62e078b7691dc`  
		Last Modified: Wed, 16 Apr 2025 16:42:32 GMT  
		Size: 215.1 MB (215149854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eccb1ac0f0c635539b0ca324cd9869d0c6222b84ef53ecd83c72b9fb332997af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0c6ae69c4ce82fef84a901a294d0c7bf8e0d4c744d866c51a3d26d79408ac2`

```dockerfile
```

-	Layers:
	-	`sha256:c8d4f3dd915ec8ab2b0bf4fad8f88a347358188338ed8a9982affd94a652102c`  
		Last Modified: Wed, 16 Apr 2025 16:42:23 GMT  
		Size: 2.2 MB (2236465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a21fdb4bdbcb486a30bc10379d0ecd6c90213fdef963cc9bed1bca7a09d200b`  
		Last Modified: Wed, 16 Apr 2025 16:42:23 GMT  
		Size: 10.7 KB (10726 bytes)  
		MIME: application/vnd.in-toto+json
