## `sapmachine:lts-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:6f80072bef418b297971b8159b34584ab3b89606fad223a186f95e9b3f74446d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:43390034864733be7b4faa1c760e8a0b8fc64a974dcba3e2283113c59be87846
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244101837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de9ea58c498e752bac901ac9d8b2ab8096ec6ec81c2cc1cb1344357a2edc28b`
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
# Fri, 16 Feb 2024 03:21:42 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:21:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 16 Feb 2024 03:21:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3487a3aaa31098e8cd5abe06d5131a5b1fd80a66142eea6bc1c04764c66cab5`  
		Last Modified: Fri, 16 Feb 2024 03:28:53 GMT  
		Size: 213.7 MB (213651760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:30ae3de49d07d14cd01ffd8755090bdc786d3b7dab3e36053f1375134af9a8dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240154362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c44ef332dde751644c202558aa41f97f012dfb96a8c35f5fe8f43c9b1b66df3`
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
# Fri, 16 Feb 2024 04:30:55 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:30:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 16 Feb 2024 04:30:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab42af9ec41f0173e32fa7f9bb4b650d838759a2148526e6071686a13c5b3ee3`  
		Last Modified: Fri, 16 Feb 2024 04:37:23 GMT  
		Size: 211.8 MB (211754041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ec44b8dec3ea26ebf9743dbce48ea1e44ca60971b4b2bdbfeb46e9d00de6151b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250450312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aaf718a0383918b20c08bf66bd3c0bacd042c5e5d5fe4d346152536172445a2`
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
# Fri, 16 Feb 2024 03:41:53 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:41:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 16 Feb 2024 03:41:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bba6918fedeb988abcbc76f1f152369a5699069ad204d98dee6ace34c24fc16`  
		Last Modified: Fri, 16 Feb 2024 03:50:49 GMT  
		Size: 214.8 MB (214821474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
