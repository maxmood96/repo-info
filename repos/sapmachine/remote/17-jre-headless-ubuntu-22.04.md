## `sapmachine:17-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:bd3a6cd705254efb5995c5ebee8763191f1b77eef294f07be353a1c1365ac729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:324c5b34ff29822fb97f8b2a2ffcf90116d96e86ee07aaab32830072ed71eba8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82875469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a26901b0377c782549b3fb61d042bb9306c0d7f15eb417856f405fe47b007a2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 05:39:05 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.8.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:39:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 03 Oct 2023 05:39:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96509168b12e4591cacde4b2513d7cccb705005dc7a78114b30efadb7c86dc7b`  
		Last Modified: Tue, 03 Oct 2023 05:46:06 GMT  
		Size: 52.4 MB (52434600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:812e4d501611b310e379ebfc6beeae616b2d5df1e755ba5ba8bb80b15829bd62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80160354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351a0a6570e04bdaa8e665ae03bc8a437db7e33661a5920017655b08b51b0e76`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 05:40:14 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.8.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:40:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 03 Oct 2023 05:40:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07ec0a7941db49e932f26babc8cab29823c67206c6c5aa5175c48fe51188a6b`  
		Last Modified: Tue, 03 Oct 2023 05:46:45 GMT  
		Size: 51.8 MB (51768281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9b957bb888a1e37931e08dd193e187e6965345250ac5e82b5c33840488713910
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89445519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0838fb8af2811c3489131342dc972513cd9f3213bc2a93c689db3b6738443e9b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 25 Sep 2023 10:20:46 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:20:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:20:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:20:46 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:20:49 GMT
ADD file:4e52928c778d7e98d90ccfcaacd039ae1fdde494dfa310adbe229d7051c30918 in / 
# Mon, 25 Sep 2023 10:20:49 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 08:31:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.8.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 03 Oct 2023 08:31:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 03 Oct 2023 08:31:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8098558aeb0337452acaa8c74f02401dc8e9bc5a2c048e4c82c013b483a11f11`  
		Last Modified: Tue, 03 Oct 2023 07:57:52 GMT  
		Size: 35.7 MB (35702863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a9afe43d55b3945b3bd1926b6994a3feb01970c5517229ef683df538178012`  
		Last Modified: Tue, 03 Oct 2023 08:45:35 GMT  
		Size: 53.7 MB (53742656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
