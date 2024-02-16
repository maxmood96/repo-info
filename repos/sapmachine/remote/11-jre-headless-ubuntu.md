## `sapmachine:11-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:3b8f6542b206e3bfd7190f4691094af789d55754cb8d0cb854411026204cc3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:2ae424e6a4e7bc02f0dc510d3d175cb1d72b709d3e296c260d6665754ed063bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78988658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43acc1867e8eb4be29d91dd42c4aac745da3c9173d9cbad5f0653d543bcd33a7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:15:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.22     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:15:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 16 Feb 2024 03:15:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a34ee6724c695e060362ce8f1d802fe654f743dc492585d522ab36a8bc01904`  
		Last Modified: Fri, 16 Feb 2024 03:23:47 GMT  
		Size: 48.5 MB (48538581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:140f6d256a0ebe908794f04513de5a44bbf747f40257063ed416bc38b06ac765
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76181230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700402513bda74f7d1efae24193a0a16ee4bcea6f80c66176de3f76d2b8adfba`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:25:32 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.22     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:25:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 16 Feb 2024 04:25:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dcaa880db98ea5c99236d929ca9ebcbaa333ccf05de53a83fab1de55626e04`  
		Last Modified: Fri, 16 Feb 2024 04:32:36 GMT  
		Size: 47.8 MB (47780909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9be7bfa18967381a8a8920c2e3f43fe15df27ec81d0f6a612e23fb2be0d82194
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82576431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199d2f7d0f8a7e192e7ba3f9cce2117eca3ff5f77788ede416a66e04ecaa017c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:25:50 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.22     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:25:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 16 Feb 2024 03:25:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4695f83d194aab808fced837280d164cfda2b4129ab80eb30d3deaeec71ff360`  
		Last Modified: Fri, 16 Feb 2024 03:44:53 GMT  
		Size: 46.9 MB (46947593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
