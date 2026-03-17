## `sapmachine:21-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:0d329a2f4dda823db6ef2838db1823b0efadaf42c11e4357c805b7db816b94dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:5e4bd07c1d85090ae63881ba3b68c82752115679e5b51358438f65727a00b642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244426243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6b33c51158f9712aa786151c649f2d4c0aad03033c0a60b94bc1d57cafb056`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:25:01 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:25:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db6775e3feb6ad7d9f47a3c2b001cb33937ca52ea0791515d1dcd9d89907f17`  
		Last Modified: Tue, 17 Mar 2026 02:25:23 GMT  
		Size: 214.9 MB (214887723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:91c45ca2c4c3540b234e297ac11dfaa8297d06f1b86ee94e3a276cde61d9dcfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3a7110b72ff5d138a5aadc876af33b578a9ed3a3c46f53952d369c13b70027`

```dockerfile
```

-	Layers:
	-	`sha256:8eb24e97b562abcfaef5a1508542eca6b749c2a9975e21a94bf77b25ce733a5c`  
		Last Modified: Tue, 17 Mar 2026 02:25:18 GMT  
		Size: 2.4 MB (2380058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2958b231afe71a6158381ea7662feb36f30d0caa9fb1a72875ab7adfdb27e75d`  
		Last Modified: Tue, 17 Mar 2026 02:25:18 GMT  
		Size: 8.9 KB (8914 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e798931cebb927ce4cf0e48e51715f53990271a349c2f9ebec78a26d8f9dda09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240501740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8937831ed805c819444b3e7a7792bcb664b906acbbf718e173645efe13561bf9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:31:00 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:31:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:31:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7299316082e774de90d3b06d0be00da3407014d11a856699129704e6a5fbbe`  
		Last Modified: Tue, 17 Mar 2026 02:31:24 GMT  
		Size: 213.1 MB (213112715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ce8736e5b085b166d7ef7ebdae603348c8b1c1f2c9b4dfe80a2bcb8f920f698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fa77a3d545543016c0d40f7e7b1b6665fc1dea3a8f00011592b04202e19d6f`

```dockerfile
```

-	Layers:
	-	`sha256:539597fffd1ae1b52ab456a4d3ba9a051b56a78cb4589062cabd19cd713ea27d`  
		Last Modified: Tue, 17 Mar 2026 02:31:19 GMT  
		Size: 2.4 MB (2379730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c786e3625cf09e0bcefc676783941058a23c3334d880623822389ea1b708871f`  
		Last Modified: Tue, 17 Mar 2026 02:31:19 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:87635681a10637eaf64cd30574e34325638500da4a42f2c3723f23e49274e023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250122235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67a51702e558cd4cce35e2face6280fcdf8e81f93f32e883748096d46177bb1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Wed, 18 Feb 2026 19:18:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:18:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:18:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8fb1f39b3c120abfcf98b51c32153f1cd4a57fbbd4d2a96cf6b948c871452`  
		Last Modified: Wed, 18 Feb 2026 19:19:22 GMT  
		Size: 215.7 MB (215676133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2cec6f1ab9c9872a02e78b87db22f5cb0194a8b6a65f70652ed93cd420fa5d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ea66c2fc6eb5532d3b0076f0003bf9f059e448f9e1fbd69eb970ed5b16d7fe`

```dockerfile
```

-	Layers:
	-	`sha256:8b77101fc0e61221d5e190443bedb3dddb39c5193e91acd6ce127e8113500f47`  
		Last Modified: Wed, 18 Feb 2026 19:19:16 GMT  
		Size: 2.4 MB (2377554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4930c8b54c9b55888ef402f95830ea426d7131570a738b6426d94b5daee040fa`  
		Last Modified: Wed, 18 Feb 2026 19:19:16 GMT  
		Size: 9.0 KB (8958 bytes)  
		MIME: application/vnd.in-toto+json
