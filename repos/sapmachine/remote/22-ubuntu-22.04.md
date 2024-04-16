## `sapmachine:22-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:5ccf28c563ab22917abd95c946ed8e9fb5c746514ac0ac2f91e3daa67e4a0eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:22-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:01110f343fc3e9b5630eb92dc5cef55572f89f5803dd413ebd5092576b240c54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243787925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61613455349e4a59cb84ea660d0e21e35019fdfb3d812203d60678f8d6c5229c`
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
# Tue, 16 Apr 2024 07:41:51 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 16 Apr 2024 07:41:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Tue, 16 Apr 2024 07:41:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6aab17fd15cda8dedbc41ed853492cc5d34e9b5570c926d08b139f51f255c0`  
		Last Modified: Tue, 16 Apr 2024 07:50:45 GMT  
		Size: 213.3 MB (213348147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:22-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cbf01efbb383c490bfba96682bd1df5970a784bfb9344c1bfe0a85c367c3dce5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239674678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046d28edf4a040fe59b26dc762ffbb99eea34c44bb46c64e9f2d0a860966af42`
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
# Tue, 16 Apr 2024 03:48:14 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:48:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Tue, 16 Apr 2024 03:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec9eaa070afcf8511db97c27619f19bce98c4e2fe4d0d087fef0c827f9b28e7`  
		Last Modified: Tue, 16 Apr 2024 03:56:20 GMT  
		Size: 211.3 MB (211274380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:22-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:47046682772f31d074f2fdcb4b992855337ef3588137b6ef8bf3b4d638b2e10f
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249988559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1495e9913c076e3cd6fbf671e4a59121df60d92d641ee87b791fe8b778b3282b`
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
# Tue, 16 Apr 2024 04:33:27 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:33:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Tue, 16 Apr 2024 04:33:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1788c653485f26b7a437614ba8d6cdfed3a5e3e0e96c38f49632d09e84be7b`  
		Last Modified: Tue, 16 Apr 2024 04:42:58 GMT  
		Size: 214.4 MB (214401309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
