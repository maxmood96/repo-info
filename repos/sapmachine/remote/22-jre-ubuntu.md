## `sapmachine:22-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:a13753dc174e36977ac15f6686505e207d9f596c4d79fd0340e540e3a8e1dbde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:91e0f39e905c9a2b673ac3fd2405fde693ea9973f55a5c1016c2e91e34634d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89215111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8902f6d367d17e01b10aca6d1ab31813e328e03c0f411175134a03618ba1faf4`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2283ad9c8833701e7a83547a4e809f1223c30a58026c81f08a82ce6238b2a5`  
		Last Modified: Fri, 19 Jul 2024 17:59:01 GMT  
		Size: 59.5 MB (59509958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:71b1d3f59dfd373446c0dd37d801283f38a78ed04e40a58f707b8f1d14b772d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76579578ae83bbcdbb16b38aab0bd0b74588b340a1fbe5676c45c65a6cdf166b`

```dockerfile
```

-	Layers:
	-	`sha256:6bc6f6261b9c7eb63c7a8f7ce88288e341a25b6876e01b73bcea481f9bb876dd`  
		Last Modified: Fri, 19 Jul 2024 17:59:00 GMT  
		Size: 2.4 MB (2363691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a502c015bdf4aeabbae7481aab10f782c9cd8abf0f6467839895b0ccc5740c`  
		Last Modified: Fri, 19 Jul 2024 17:59:00 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:329ecc0d69a64b10d643cbf50391294f390b5b194f42e88010c76754c75809d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87607492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39db1a646490ccdc8e1158946278915f46f6161c48e2f9d68e5507d8aeca4de8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78a0a6707d427d8054d231320ea8118f394a8641accc0c7d6b7f813006dec37`  
		Last Modified: Tue, 25 Jun 2024 23:52:17 GMT  
		Size: 58.8 MB (58764449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2b3977368fd048b2f34dc351feb9aecb7c72085bb81a93016a8724152d3d1755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2346692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f35c703486e5cca771abbf6c70e56c3d52a017a664c6eeed8b1d5f07696c43d`

```dockerfile
```

-	Layers:
	-	`sha256:184ebe084de6cad42d1b65bf136ba47ca5665e03ebc5b0b659fa4f2a314c5248`  
		Last Modified: Tue, 25 Jun 2024 23:52:15 GMT  
		Size: 2.3 MB (2336141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d778b232d507ed07e4747dc033d6a98041e5e53d02597b3ad9b050d7a3b8d3f4`  
		Last Modified: Tue, 25 Jun 2024 23:52:15 GMT  
		Size: 10.6 KB (10551 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:86caa94114380d9156c66155eed4533e6b4225a2f65573ef57a3d812fbd61658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95798346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ca501202edba9edd1b0b5f81adab435d9375407cb4f948e9c38310f533d398`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c440ae8728dfa116fa455fa1d8829e9aeae9828709552663f40f6c7c498bf5c`  
		Last Modified: Wed, 26 Jun 2024 00:09:50 GMT  
		Size: 61.3 MB (61292317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:14592eef8ebcff1f76b873de9ccf13a4aa32556e9154db2f1d01d0399163d0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7815fe9815fa2f423a6cf1db62fd29e13bfb938e2c358dfc88a046197d48c2f4`

```dockerfile
```

-	Layers:
	-	`sha256:a786aaa9ff1fb7341a8a9794bd35e2bc74960eb7c818acff729ad13f9399d56c`  
		Last Modified: Wed, 26 Jun 2024 00:09:49 GMT  
		Size: 2.3 MB (2339581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:177157010d53d2a367068da03724e339e3c862b6e8e902624d8b0ef4854a7f8b`  
		Last Modified: Wed, 26 Jun 2024 00:09:48 GMT  
		Size: 10.3 KB (10258 bytes)  
		MIME: application/vnd.in-toto+json
