## `sapmachine:22-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:4c980f8424df1c977495e79be7842e06739af4eb48b264bfc3bca5d7cdd0b6f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:b6ef0f3654f332c13d759e629e045cf0a66f6761f6a6b7cfeb49b3902c8b975d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243325560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfefa2c6c9a2edf4a077627ef322a4a211d126c6774e4cdcbf691b547116727`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c7ca8ce58b3c78ea16efea1d2c0fcf4243a9387951162e4d90a124ff10d9b29d`  
		Last Modified: Sat, 17 Aug 2024 02:05:42 GMT  
		Size: 213.6 MB (213619262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c22d9a9c56e00a916f2945012d1a8064c0994e16f9245a326f320fa59768b80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39e1c48e2841abea74af61b1b62928890e58d388cb4cef6062e658156327255`

```dockerfile
```

-	Layers:
	-	`sha256:cb6d55ac0cce510660f462537f7bc87168a38e63044d4eb61c882e7e18961b69`  
		Last Modified: Sat, 17 Aug 2024 02:05:39 GMT  
		Size: 2.5 MB (2450190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47521678878e875bd5ebedf109bc9b69ea26466e5802ef681fbdcbed02e8286d`  
		Last Modified: Sat, 17 Aug 2024 02:05:39 GMT  
		Size: 13.0 KB (13030 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6e05ec331552641116f8366a13149ca759865e30191aebf0dbc6676b5d48fc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240454773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa0e1b64ea21f3690115798ed7f58e723bb81b3225c43496797011597dcbf14`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:8cfadeeff48aee1833c0bcead3ce70130628740a0c8f0a5679b3e4344f0147c2`  
		Last Modified: Sat, 17 Aug 2024 04:03:59 GMT  
		Size: 211.6 MB (211611087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38e0a738b745d9bdd2ffc93be8635d9c80a85ce5de970e978c2d358e7d94144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a83787ba32ec24c155485e9b0f533a35998192612c895328987351188fbdc78`

```dockerfile
```

-	Layers:
	-	`sha256:4d1e47032872c88cb2116d7bccb372cce451d8cacc9825ffc7de7dbf2bcebc7f`  
		Last Modified: Sat, 17 Aug 2024 04:03:54 GMT  
		Size: 2.5 MB (2450194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b292c145fd4ab8f40e9e6e0528f0002676a27935a99da5a77e611438ab38a5`  
		Last Modified: Sat, 17 Aug 2024 04:03:54 GMT  
		Size: 13.5 KB (13498 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5665c3b0deec567a01e4db7222571dcd1c393ead38907eaae35ce93f045bb4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249346449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c92cd2bfc52a4f690423ba4c4510df343cee55b8a01074e85bd46f707198cb`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9532c4c5000556df154a237634817f3c1c27c39c6d8ec47c69390d07b795c34f`  
		Last Modified: Sat, 17 Aug 2024 02:25:41 GMT  
		Size: 214.8 MB (214838877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0960389cf4d88fbdd26f532032c75fef2a321369adde25c9ec7c802cc346d872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfafc0a42b016e05f7dc35139b0d7a4a824510d56168037b27912c7520315aee`

```dockerfile
```

-	Layers:
	-	`sha256:30bd6fe42a5fa9fff576071f5fb3ca47d21309199fcbda0ffb89014208fced31`  
		Last Modified: Sat, 17 Aug 2024 02:25:36 GMT  
		Size: 2.5 MB (2451643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0029575b62885662a2bd82cf2c318f43e71faca1a3ae662396d44d75b04132f6`  
		Last Modified: Sat, 17 Aug 2024 02:25:35 GMT  
		Size: 13.2 KB (13153 bytes)  
		MIME: application/vnd.in-toto+json
