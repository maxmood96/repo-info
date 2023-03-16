## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:de415dadc9039748b37b0af525ba7c875fb47ba8c91c031b91fba20af23a8a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:8104acfb158b83163d3687e2f0c2b7f9b5fc1205b031f3d439ccff348b0f86fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242933479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995f54f9f66d081e702da31ebff050157274a8778fc99d1cfce778e2fcd34dfc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:26:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:28:02 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:28:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Thu, 16 Mar 2023 01:28:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64f3b1d0b88367c9674c2ad7667c1472644ab30869cfa9bf4a742956941bdb7`  
		Last Modified: Thu, 16 Mar 2023 01:28:18 GMT  
		Size: 7.9 MB (7917721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ddeef58d4112a7342949cd2c59251512216586bcf19e2269d134500015f3c8`  
		Last Modified: Thu, 16 Mar 2023 01:29:19 GMT  
		Size: 206.4 MB (206437690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:bc3195e8662769ec48c8674d9a96cb93962c4e06a7ee4e1b984f6c6a6ec00185
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239517626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e265f70541fde18f1ba5a4c8524981c058814d49bd6ea1e71d538899c258c57e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:55:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:56:59 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:57:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Thu, 02 Mar 2023 04:57:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbd1ef482bb7f6d134f88a74c3373576d23dffa4b7de76d8eaaf911cbb884d9`  
		Last Modified: Thu, 02 Mar 2023 04:57:20 GMT  
		Size: 7.8 MB (7756310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d7ddae2289d136c402989c8b346ce00b2d3bb227631031edea8ecaabb1d9c3`  
		Last Modified: Thu, 02 Mar 2023 04:58:12 GMT  
		Size: 204.6 MB (204566795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c001aaa6fced4bc4daabf4d8ae30a4fccaf7a9c8981f8c27a718ee54d56e5ede
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249081930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0477f0191999d598ca1075d4e747341329a208ccefc7232a5617c86c52366920`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 05:13:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 05:18:57 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 05:19:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Thu, 02 Mar 2023 05:19:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c1a1c48cee329c0d94333d1fb94839d2d5166aedacdb58c84e5d4b61cedae5`  
		Last Modified: Thu, 02 Mar 2023 05:19:36 GMT  
		Size: 9.3 MB (9316642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae035c9719397fcb6e9a126e4d2fa842075240bd4810b8f57a1c390411b46aa6`  
		Last Modified: Thu, 02 Mar 2023 05:21:11 GMT  
		Size: 206.5 MB (206464909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
