## `sapmachine:17-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:168d49e2dd31a667d2d83ae23b3155fa25f56d7eacc797b351d2d9b20f107cca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:5215943c4b001b70c430a19c61bd63403748deccb72800d51cbebd1767e674f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80769706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7575d2badcbf72c7f1c761cde2a049cc28023337d9ff9d6c96d69316acceae2c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e5823fa67d5e7677edc8d6eed383c112afbfacc3788966a2d07bfbafc4b57f`  
		Last Modified: Wed, 16 Oct 2024 16:17:53 GMT  
		Size: 53.3 MB (53258646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dbe2b5b4f1bd34eb57f2391ec06be6b5b6cddf703a71b765d2c07387b7f403f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31578bb1fe10ba2b9af98f3fd48e68ec81aff40fb1707eff762db82e184ec1ee`

```dockerfile
```

-	Layers:
	-	`sha256:8b4a980d63623f94bc0e707a5fd28bc5ebf60b483107471d730b8d0a1582b6f6`  
		Last Modified: Wed, 16 Oct 2024 16:17:52 GMT  
		Size: 2.3 MB (2279654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e6fa8aeb874f5a6dee4ee8a3bb45eafc3f845da63cbedf90d348d6c23f1a3f3`  
		Last Modified: Wed, 16 Oct 2024 16:17:52 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5609d0f04028a17a44368cadae3924e4b8a85250c7ff05babfbf3632ecd88181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78599935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b631173527799c797afb79407916f13870f3e1dade54dd88ae25771ef4e7a277`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af31028946f28aec8e9aa99c1834c983418b31f65e329c62cc0da64e3577a3b5`  
		Last Modified: Wed, 16 Oct 2024 04:44:55 GMT  
		Size: 52.6 MB (52626107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ab65eb70730d6171e66c76250e0cb5791c9d8a9bac48bc8a22f0240acc824024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b33cdcd6a3078a26256920cadef9e857e1a45ee8c0ea1bb5b8fd4a2b36e86d`

```dockerfile
```

-	Layers:
	-	`sha256:de1d8ef940470570fb673e48640b8bc54f3efa65678b9c69475810d9997c0ed7`  
		Last Modified: Wed, 16 Oct 2024 04:44:54 GMT  
		Size: 2.3 MB (2279290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c724c89b240923d96f3b925cef8313ea7a263c970adca34cd414d19690507099`  
		Last Modified: Wed, 16 Oct 2024 04:44:53 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:61a46c16e1d998a22bea649a4d9de33acf4e3a6c741229af5c7fb41f346eeb1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86438720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207b1a3e0c4fbae132fd8c0a480e8c5ec61036ecd40ea5923ecfc7cf6cd5b4f5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecaacf742458a4638fab7e9c327f150a969e92925b9a33073bc02c6f5259a96`  
		Last Modified: Wed, 16 Oct 2024 03:06:52 GMT  
		Size: 54.4 MB (54362214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ce491151b12ade61915198c46bfc17d5a268c95806ae68f7f4aacc626d4eafd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f6bb3b60cf8593850f78c3568032d2ad79e742606c9fbe19f11b311e5f515e`

```dockerfile
```

-	Layers:
	-	`sha256:adae2ea448cbf277bd79b6055cf23f8f03104f072f3b117dd102ffa5b2428e0c`  
		Last Modified: Wed, 16 Oct 2024 03:06:50 GMT  
		Size: 2.3 MB (2283419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa7e2008616fd0025f6e1284a192314c27d08440c8168fb6b078148ca382242`  
		Last Modified: Wed, 16 Oct 2024 03:06:50 GMT  
		Size: 8.6 KB (8643 bytes)  
		MIME: application/vnd.in-toto+json
