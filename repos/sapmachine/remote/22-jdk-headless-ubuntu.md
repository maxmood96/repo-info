## `sapmachine:22-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:56c1ff636b35bbd3627a0e5cba4a9b1e5cb21a9b496bf2d27462e0f1f84abeba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:5ee5ceae5779d6bf468cd30c73a2d0a92b7d5ddcfec846e031d254d9d1beaaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242123914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84116fcfc3105e7579585390af9a25cb9186380193e67e01c37a8de71a0d709`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329126280cec58dc61b1f263ea2e76ac899ed981c8f771e6c1db2c7ca11ed879`  
		Last Modified: Fri, 19 Jul 2024 17:59:13 GMT  
		Size: 212.4 MB (212418761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0887d7dec9604a49f50414b6fe798e4e90d0ab4ed63e900b3a3a293f4a2b467f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2710df2ce5a15f0bf2b9b519806757d0c694a8cab9ee48f4cc32dea8637c4456`

```dockerfile
```

-	Layers:
	-	`sha256:9686292307d76477c5c0de19b13691838c08066e7724f86296026dcf66d230e1`  
		Last Modified: Fri, 19 Jul 2024 17:59:11 GMT  
		Size: 2.2 MB (2211291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb6df91a156250f030b45c92474d58f3db39bcd758f728fdc74de1fe09b27bb`  
		Last Modified: Fri, 19 Jul 2024 17:59:11 GMT  
		Size: 10.4 KB (10374 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e72cbf46f5d2eb2d8e3139533d02457f4b508ff94d9e9dd6faff793c8b41f936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239260403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbd04e91e15bf1d10521d268a53aee960552448d842fe2031430e97acb96023`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a16cfa4d7c10f7a773df4eba4b548f8e25dfcb815be818a22e433c24240756`  
		Last Modified: Sat, 17 Aug 2024 04:05:08 GMT  
		Size: 210.4 MB (210416717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5389f45f6746de6387892e866a3adbfd21f4e200e5d6ec2862b6a2eaa437bb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aae0255e858cfc48cb7d1a1961971ec1c55a7fe369ade1cd958fde6ac416280`

```dockerfile
```

-	Layers:
	-	`sha256:b9fd193173c5cb7f7a1ad914e2f837fd1a1edc5d89b2df7ba1f48b98b8372da1`  
		Last Modified: Sat, 17 Aug 2024 04:05:03 GMT  
		Size: 2.2 MB (2211178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c20b2f8e89a2783e40410d0762028fde25166df8a7bcfe9df4b6f8c7ef02a5e`  
		Last Modified: Sat, 17 Aug 2024 04:05:03 GMT  
		Size: 10.7 KB (10735 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0b1b67edc3672a81ef468616b12b9e60033293266d3193dade91cde0933446d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 MB (247953791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9fba3f46d151ebec971a760107e7f04e81c5c699e5cde0459237b1151fa394`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5da0e836e1a6a61e3d137444d75aa6049ef405498accda771c5b270ee99de4`  
		Last Modified: Sat, 17 Aug 2024 02:27:29 GMT  
		Size: 213.4 MB (213446219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e7ab13c8f3690bc962f68f98fcd808bf6849e1d78765571244d598c0a3a3768e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bfd006bf6a1932c07efd473f742dd2b9123742cee59e3d64021d776f11f8da`

```dockerfile
```

-	Layers:
	-	`sha256:1edd5602a2eec5ef2664ab7f7b6de809a75ca0c316b3c8fd8bd54a273915eb41`  
		Last Modified: Sat, 17 Aug 2024 02:27:22 GMT  
		Size: 2.2 MB (2212627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f20824dce0e6b3d0ac7b0a0b82dd17ccb611d94ae95fb345eb38f6222be870b2`  
		Last Modified: Sat, 17 Aug 2024 02:27:22 GMT  
		Size: 10.4 KB (10442 bytes)  
		MIME: application/vnd.in-toto+json
