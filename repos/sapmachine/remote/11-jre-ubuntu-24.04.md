## `sapmachine:11-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:27cf6ab1563a7118dcadf38ef532982a9e7b784cab4dfcd8c519a1c1eb705bde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a33085505b4c471fa304f387bbb4fbb8e0614c17168f553f96d71a482fbd1ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80021668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148837d243c022fb6c02d1b99285d638e8f3616dacc4fd8b96baf931f154544a`
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
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
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
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5c05764f9c93c2ded839fae4d89514998fc5a7a14bf638dabfc48e755eb14d`  
		Last Modified: Tue, 25 Jun 2024 22:58:52 GMT  
		Size: 50.3 MB (50316515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f7c18915204ec669abb76d1b82eea468a92151d8cf1152223b22d4d83c485d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2355324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410c6a34cb747589d73940742f57b77d6f20b128d67f2ee25cedf3d3696cbd66`

```dockerfile
```

-	Layers:
	-	`sha256:89171fe1735805c986e5e476b1eb76043e9a44a09fc7fc094dda2b180f1e1e5f`  
		Last Modified: Tue, 25 Jun 2024 22:58:52 GMT  
		Size: 2.3 MB (2346089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad2db5792ee6701a5a0ca78c950a32c4f2144fc16ae6aa84c9e7f6d1855c81a1`  
		Last Modified: Tue, 25 Jun 2024 22:58:52 GMT  
		Size: 9.2 KB (9235 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:11-jre-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

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
