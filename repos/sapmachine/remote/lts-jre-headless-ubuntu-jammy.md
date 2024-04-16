## `sapmachine:lts-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:15bcea79135a8f365ccb5123fc293a65eb92603deed5be0ca54560d9212789c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:6ade1af09547384d679e7f72f171a0be4e17fe310e2f5b0610f432013f309573
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89067560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d81f1fbe345036f0f5f644f043a7bb30d79fd7229fb6c2d3b0d29294aa593c5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 07:37:06 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 16 Apr 2024 07:37:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 16 Apr 2024 07:37:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b14f846a2f2e199000f70091eb7017cfc550e627667a34da2f2ba1939c65e1c`  
		Last Modified: Tue, 16 Apr 2024 07:46:55 GMT  
		Size: 58.6 MB (58627782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0b6d52983d8ee9b6189c3496601c8cde91354c10133da77d06c853a4fae9e3dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86098617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8801fbed69c27c3c4b27dd2cfdd71b40e442097592e3a5d2816ea96b17e701b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:44:24 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:44:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 16 Apr 2024 03:44:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fa159f4da10ccd5035e40039872dce97d5fd649211fe41f809a36f03779caa`  
		Last Modified: Tue, 16 Apr 2024 03:52:54 GMT  
		Size: 57.7 MB (57698319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:dda80fa79169b4aa977a57ab3e2310f42bc39e6ee0e24d8f3a5ef25e7a3f5948
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95619530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b70c94ce85edb954af13057050873edf462093d70ed954cae228adc94a8dc40`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:22:25 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:22:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 16 Apr 2024 04:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de2844af037eed2350f92d5addcbd08c67623c1c78af9a1c09ef3f3bd5d8e59`  
		Last Modified: Tue, 16 Apr 2024 04:38:46 GMT  
		Size: 60.0 MB (60032280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
