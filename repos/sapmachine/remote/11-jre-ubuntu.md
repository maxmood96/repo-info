## `sapmachine:11-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:2c1c3af1bd4711da95f15a32c4b9d88f5f09e9468e20fe114cf4f239a49e8659
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:4572c1fed6acb4b23a3dd55a2bb08082325ac443f41b80c700f353c7ef7559d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80043965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b362eac7097a683d0865df1d799aa3f8b198a269cbc9763c16a5156a3de1a425`
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
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39369408ab0122719b608ea75ecaac9e85be0700fbac570698f644f06b80a1`  
		Last Modified: Fri, 19 Jul 2024 18:00:11 GMT  
		Size: 50.3 MB (50338812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0e43583d11b78184f7785e0f5996dfe66c2272cd6f809013297429cedf869934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6400c8f622eb069aa99bc470a9efdd20e8a76899900bf673712826644e98228`

```dockerfile
```

-	Layers:
	-	`sha256:b3eaf6123775c3e7a5affb7a4667c1a1aac0c6bbf6787ece2ac87bd766a12735`  
		Last Modified: Fri, 19 Jul 2024 18:00:10 GMT  
		Size: 2.4 MB (2372267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23690b52cb7b8bdf07680692b133966c9539bea7b4d06404c5eabe0a538fcfce`  
		Last Modified: Fri, 19 Jul 2024 18:00:10 GMT  
		Size: 9.2 KB (9216 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cf4f537bb46aae9f08cb1a4e17e649416764d98a38edaebc26a453b179a95697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78523782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49d8a5f5c5399be9240e7388de534d0ba1769b7007098d784ca43537e926e02`
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
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c948f21a24089b83fbaf37275b05aef3667acb42e032e94982290a0ffa3c22`  
		Last Modified: Sat, 20 Jul 2024 00:36:06 GMT  
		Size: 49.7 MB (49680739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d64c8dc381267ee698ac883497ca274f0d9685be343a20517c55d50b30c1559e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb233f0b3e7d3b21de674a9bf1f2744798fca512e4f3964c8ac610457940b40f`

```dockerfile
```

-	Layers:
	-	`sha256:1f99199f86b87ded0fba91dadf8303bdca902386fb8e9ce1b5b80ba694604d07`  
		Last Modified: Sat, 20 Jul 2024 00:36:04 GMT  
		Size: 2.4 MB (2373386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195c68b8a93b9c37d956ae41aef749fbbf8e5c3d079995e03cffdc89c1103668`  
		Last Modified: Sat, 20 Jul 2024 00:36:04 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:efb8020d5d480e8776342cea27cc91ec7f5919312bb14c610a63052aa20b1d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83605149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65706d698b557499c94e8bb3806b9cd5036dd917d891e1746e8b92487bab2a90`
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
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482ffe47f12d4b1ddfc5e09fef2de1d4117346a0cdeeb29fa8b72053d517b0ae`  
		Last Modified: Fri, 19 Jul 2024 23:53:40 GMT  
		Size: 49.1 MB (49099120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:09e1686034b1af4dcce97e2ceb75290df8c1c223b7ec8cf8c967e38ba2d53304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af52b40049ba76d3ac9d9c74ce334ac0109f8126d41bbca9be8f5b5245cf2f02`

```dockerfile
```

-	Layers:
	-	`sha256:4d83ff46014ec4836f80e21aa3035d59e051c479c47c6c26b41e33d36c7e566f`  
		Last Modified: Fri, 19 Jul 2024 23:53:38 GMT  
		Size: 2.4 MB (2376222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d9d4a0e5222600f66dc975cfa51ce17ae7fa78b034b6e2bcb1128a64f742a5`  
		Last Modified: Fri, 19 Jul 2024 23:53:38 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.in-toto+json
