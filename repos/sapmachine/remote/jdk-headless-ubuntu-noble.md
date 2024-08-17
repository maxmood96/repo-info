## `sapmachine:jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:45651e3d09b180f6d88bd2523b581f8dd84f6da7a71fbf6da42e486326e6a8d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:0a8ea60ff98cdb77c6e4893de24f47443b72987697b908cc8e3f5b301d727068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242125044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c22927e83a02146a6a7ab94bfc2ef4bdf5480cd937121cf2a812b7f45633e3`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19962a3944e4dfb10babb4941ad55ed57ddeeffd1ea2bec21d4c8292c6ef7d69`  
		Last Modified: Sat, 17 Aug 2024 02:02:37 GMT  
		Size: 212.4 MB (212418746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b0211d96728f74e178a99ae6c87fe5029c71967a1ba9bba8e6f3cd6777ef069e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c60c307c47b6f69904dbdd43b26874d9dd8b7c609f5a6928e8c3ee2ca974752`

```dockerfile
```

-	Layers:
	-	`sha256:52df9fd289eb4c0f1aaaa25da4a192b07ac5e8a4e002f9b3e6bb5761f77a45aa`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 2.2 MB (2211291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af7ced4b258e1dab562bf149e2c11aaefe4574274d0e554aa4cce7b0b7f9a1a`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 10.4 KB (10374 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; arm64 variant v8

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

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

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

### `sapmachine:jdk-headless-ubuntu-noble` - linux; ppc64le

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

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

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
