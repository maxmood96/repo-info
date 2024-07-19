## `sapmachine:11-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:3a8a36d45c108ab8332030a7b5f2e38a08736025f86d2a8ae5a7fa2d861b3b32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-noble` - linux; amd64

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

### `sapmachine:11-jre-ubuntu-noble` - unknown; unknown

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

### `sapmachine:11-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:331284b5dc79ac7dee057f547000b2ef00c695ff0cbd57afb4ff82813dd06e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78495947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c6601a778e9d4cc13621efb3b2d02acb079a4eb5abed74e3ed59ae77ed8fa3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06822c977367d162b692ede8410e08a07d3e6af440243ae94feff2f89c9ba4ab`  
		Last Modified: Wed, 26 Jun 2024 00:29:27 GMT  
		Size: 49.7 MB (49652904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:78ae7fef19dbf62a992d616b771a8ac84757c3a06678e9b43b59b9c61333e089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2356768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91570b7d1a13501debb4bfd16e47b1bc26387c0d9f8fcf6a244a1dc205a00aa6`

```dockerfile
```

-	Layers:
	-	`sha256:56ee3fedb32aec62385d85f15e2caa197f75dd4a5ce431aebb0b89800f60b468`  
		Last Modified: Wed, 26 Jun 2024 00:29:26 GMT  
		Size: 2.3 MB (2347208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45d1b9319165d59e97af68a19c2292a7cbb0fe45523fa06f7283d4a8a33df68`  
		Last Modified: Wed, 26 Jun 2024 00:29:26 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6df24575ee574da613e21c2d91914a905510cb4e242dfd78e850d728d455a19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83598176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e75928ab2126161c0bbc0f5e9bc9faf2743e0bf9dd6718671caa35690069ac`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51e1d4dc3d0676cd0d3d7da703e63dae9c6165fae90212014b41e9da84bbdc`  
		Last Modified: Wed, 26 Jun 2024 01:11:05 GMT  
		Size: 49.1 MB (49092147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5882f16136c44791e65821ebc738f5f773b6c04908b0aaacc407f5a72c9eefb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6021be7222fe7bb74e3ab1da1fef7392c1f5013777b7873d30a4156bfa10e944`

```dockerfile
```

-	Layers:
	-	`sha256:245feed86d49201164381fbc1601980beca5f7d0418e56b1b6ceafefdb87ca4f`  
		Last Modified: Wed, 26 Jun 2024 01:11:04 GMT  
		Size: 2.4 MB (2350044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615a696494f21b300167605c446bcc948092eb312fa72c0ceb82665cef3969e5`  
		Last Modified: Wed, 26 Jun 2024 01:11:03 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json
