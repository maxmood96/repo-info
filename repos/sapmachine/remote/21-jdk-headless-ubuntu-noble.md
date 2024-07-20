## `sapmachine:21-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:1a89e4908073481ffa1b9c153a5a343ee42ac51f05696349a0cefa9cf8796f56
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
$ docker pull sapmachine@sha256:b1091121744d0c7f84d7cfc755b70f54dd54d8ec38110955cf1465f2923e814f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241344416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf69c3ac5399839eec7dbe94a62ac12e61460f8a9afcb2ef44326c7f59c749b9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c977d7742db4ec8fe820fa065fe5b1f20dd6511838e980a9be851e9db5bfce8b`  
		Last Modified: Sat, 20 Jul 2024 00:10:08 GMT  
		Size: 212.5 MB (212501373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7895318452c9119e741abd7188085d956f58590685b1df41cd8114db63427084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366af15bb571b9710651f531e12e8bf8d828e03801c718b405ff19c091bd4d3a`

```dockerfile
```

-	Layers:
	-	`sha256:fb021902c9eab0a862db75b28c32068e2b44bcf9264cd8665d77ffdad99b24c5`  
		Last Modified: Sat, 20 Jul 2024 00:10:03 GMT  
		Size: 2.2 MB (2211214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4650142ba73ce4474e6e193bb5488ba198367c7ae2e2aef4fbb177b7330b59cc`  
		Last Modified: Sat, 20 Jul 2024 00:10:03 GMT  
		Size: 10.8 KB (10759 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e5b4aa4c920b5e7a4219fc0940221ee1a4b4dadc2bdb1e0260f215960d9377b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250182636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af65b2b5e2cd4ad4c62b7f0fc22e89839781556afc58ad062daa3dc1f81fb79e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5290d3f1b91b4cd8dce74ad2cc72d6f968c351822899e4eeab021aa966099e2a`  
		Last Modified: Fri, 19 Jul 2024 23:13:16 GMT  
		Size: 215.7 MB (215676607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5c60756deb5ecdcdc89d53013dea9c7d03b48bec34005e84e69b6a7385ab5c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedda3720388ceba048e51a8caf7ddbe1a97aa4ae130272f15430179e3b7c17e`

```dockerfile
```

-	Layers:
	-	`sha256:febe2fdce43a21b4aa79a6b758be08e1b36cc951898efa8c16e998b1426ecbf2`  
		Last Modified: Fri, 19 Jul 2024 23:13:11 GMT  
		Size: 2.2 MB (2212651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc5d66119f5722171bf3e474eca9b449e281036740100b1209fa0d8d2684a62`  
		Last Modified: Fri, 19 Jul 2024 23:13:11 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json
