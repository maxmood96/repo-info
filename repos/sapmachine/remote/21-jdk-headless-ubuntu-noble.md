## `sapmachine:21-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:fc0cf1bfbf3c35e02b1f1eb23c91a249e8492111a60358c218e31c6f2e862a2a
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
$ docker pull sapmachine@sha256:c56651831027abf4bc32593372977cf829a67fe5adc34e8c60c5611b34c8d494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244106588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef45a95a34e03dd49c5a873b090472c656a4ae65f12141bda2bb6d59ee3dede`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccac6d8f0fef1cf32b90b83d83bdf25223e53e880d7c4294e6f7070d3cf579fc`  
		Last Modified: Fri, 19 Jul 2024 17:59:15 GMT  
		Size: 214.4 MB (214401435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:625fd079c78c700cbb0c87e044392bf30bc29cb2b1e2e43e106e0176d7aed519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2c47df56cc1fe94f3184b983ee895b289cf76b0361db4aacbcc2833485f381`

```dockerfile
```

-	Layers:
	-	`sha256:c7095a770cec64e06ad5d923336a91877a8bfce6806566c7a316acc0fe8740db`  
		Last Modified: Fri, 19 Jul 2024 17:59:12 GMT  
		Size: 2.2 MB (2210696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5d406e3a9f5ad7d434ade2a691780e4fc705230616e53d1d5befc9be4b948a7`  
		Last Modified: Fri, 19 Jul 2024 17:59:12 GMT  
		Size: 10.4 KB (10398 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:19a416571253a47301c91de42985497abeb2b2e29243c97d7a8148736db09fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241205944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404b876eebaceabd1da567e64c25aed7d7dd7863fb87ea852507ddddfbff703e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8790bef797500a5f5738908b3c634f9836296d0d8c9ce83ed6dd7f4dba740c`  
		Last Modified: Wed, 26 Jun 2024 00:04:07 GMT  
		Size: 212.4 MB (212362901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0feefc3df284aeaa9621f866fe1b3e34441f98a21ae2d62b9a8d63da64a48383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2196911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f328f5e64d68567449b480b062fe6436fbc583ccdeb460afdc94b28493c244`

```dockerfile
```

-	Layers:
	-	`sha256:48e9284514697cdff1174562f9956f41c19f76b6a314823d118b2e4d43d32ed3`  
		Last Modified: Wed, 26 Jun 2024 00:04:03 GMT  
		Size: 2.2 MB (2186137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f767ec6054d264533f58f726b80c318de17c9546734ef9b8a4edcc8d33427f`  
		Last Modified: Wed, 26 Jun 2024 00:04:02 GMT  
		Size: 10.8 KB (10774 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3983f336d8488c069341141f6837d95cc25cc63a8d28ff01f00daeb863040550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (250033521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b93e1888d50dd9f47a471023fcee3cb52d74ff006feff4cde7609394b44aed`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5977f915d064681e5fb8f2f271765273c6312c344a59c944e7b352392bb3cd`  
		Last Modified: Wed, 26 Jun 2024 00:28:45 GMT  
		Size: 215.5 MB (215527492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a137ac9c79d28181b755f7611879685a0df26e6f4575e17de1c6efefdbc171a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2198058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18098d61cdb7b8eaa612e86770373d52fcff829a7332cd42013bbd12cf5ab117`

```dockerfile
```

-	Layers:
	-	`sha256:e67f81c56b4c3b4c660770fd7d29dc3de1bae5b3466d337fbb817947cff78cf9`  
		Last Modified: Wed, 26 Jun 2024 00:28:36 GMT  
		Size: 2.2 MB (2187574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba778aae1bb5080e046271c55456872950c763e705cbe26cf59d08320adb3593`  
		Last Modified: Wed, 26 Jun 2024 00:28:36 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.in-toto+json
