## `sapmachine:17-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:3c3e55ea3b5ec00d276bc19256f61ccdf4f0aa4ae5eed6efb06cd69956fde390
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:b7530bc12fa98554b6b48269da17fad6cfb9faa930d0b2b7c8b72f4c7354d40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (229020237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133c38b6536166feae8709fd9da074f7ace0529369f0c99b72518904e8d17cfd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431951e864e23e7b27ff102ba266640f9aa2d923f8bb30091597032631eddf12`  
		Last Modified: Fri, 10 Oct 2025 00:32:19 GMT  
		Size: 199.3 MB (199297090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bdf941b06cfef7b91cfe31774fbaea2020904c2c6bb5969b3ab065ac8acaf61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab5ae028b4effb388cf3535b801f7def8a9f98101bc53b7ee6b473b0f481550`

```dockerfile
```

-	Layers:
	-	`sha256:5614a8b914b4cd3307dfd645a2fcaa4c5e768effb48b82c3b4012b587685dc96`  
		Last Modified: Fri, 10 Oct 2025 00:06:21 GMT  
		Size: 2.4 MB (2354472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df519866618bf9dab577609c25ac153a7f5c37818910175128fc6f1cd235838b`  
		Last Modified: Fri, 10 Oct 2025 00:06:23 GMT  
		Size: 10.3 KB (10277 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:06439c67966add7458772540fe6f01125362e727b76ffb9ef07f8086def57145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226873106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368eeb1fc87b2e3a0bde634cdc0313cf30bf19d85f73f4a5ecf0566a3e7183a7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5346fb0df8428604533ce3f62d4667d589f219e826ba1918c42a11b555a849ba`  
		Last Modified: Thu, 09 Oct 2025 21:27:51 GMT  
		Size: 198.0 MB (198011394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2e3de7daee4037480412d48bd3c31b2a98cf1e54e1bc151a131f1fb7af02ebf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf2fa42cf6d0a0f70902da377462d3f07895d2f1ef74e93794e1b4df552e439`

```dockerfile
```

-	Layers:
	-	`sha256:337df51464499c1e94f4d1135786269f7b7019dd1f328f8b87e4e9c584731ef1`  
		Last Modified: Fri, 10 Oct 2025 00:06:34 GMT  
		Size: 2.4 MB (2354979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9b0f2f1803a0ad84d02bb8bb1b2c3d04c6839194bd41f630ce37482ac3aa9e`  
		Last Modified: Fri, 10 Oct 2025 00:06:37 GMT  
		Size: 10.4 KB (10429 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f5745c71520dfb2d7b684776cdd305306a6533978d675bbcd550e1bb22e1365f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236801478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105c3385f32f26e01868ff8a184618fef23c6b810b11b73cdae9125f4f1b2520`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d191911032a9c9bce40f2576176a4e1b564d92e9c5a3729dbd33e262c1c7e59`  
		Last Modified: Thu, 02 Oct 2025 04:56:16 GMT  
		Size: 202.5 MB (202497931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8cb5ee35d865603d9c90ae590ae9168e4292868829c12d5ebe5f2c481523e207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59864754dd844f6536ee5b6edb5b5686bc8438cb2e3515790b39c6f42754d6e`

```dockerfile
```

-	Layers:
	-	`sha256:646aa3803596be9fc342ae6e6f093956932252be6e55c26a02877fc2b2d076ff`  
		Last Modified: Thu, 02 Oct 2025 06:04:50 GMT  
		Size: 2.4 MB (2350526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52ff4d677f99e423a324b8fb1a65b1d4968b7249f1128186991517f6f96f065`  
		Last Modified: Thu, 02 Oct 2025 06:04:50 GMT  
		Size: 10.3 KB (10345 bytes)  
		MIME: application/vnd.in-toto+json
