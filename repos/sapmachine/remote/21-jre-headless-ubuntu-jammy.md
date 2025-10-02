## `sapmachine:21-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:82d70cd6023d5064bfab45a717281c11606dfbde4b9a9d3ecafd4bd3aa8c663f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:a348cee132ff8573678911a6a1aa0daaceeccf3260d9cf48358863c943c9a879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88133833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a774f44e26e3a47986df7df03290fe05bdf17f5716547bb57ca7898e9001c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a706f917e1cd8ec57c9f5922cf40098c81f7f4a5d30011c66fd056f20df5c67`  
		Last Modified: Wed, 17 Sep 2025 17:39:07 GMT  
		Size: 58.6 MB (58596898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bcf6a2e695c52f0a8a3d42de8d5d50df379a207e80dff5a8acc242d65e17cef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841ee8c66e0fb0559af858c8eb0c96bb0bd1ad18d5f5a823cc8a0cd710cf3780`

```dockerfile
```

-	Layers:
	-	`sha256:cf0c668910d2922bdfa1369fd1eb5750438bd4cc85eaf0c8b2d67890c06ad9d2`  
		Last Modified: Wed, 17 Sep 2025 21:08:44 GMT  
		Size: 2.3 MB (2294109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ff6f735913677d50d32059c11921949894139ef3f4a74bc8dbd39caffb7a5fc`  
		Last Modified: Wed, 17 Sep 2025 21:08:44 GMT  
		Size: 8.9 KB (8922 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8d297170cf2b16e51f0d71244a24d637696e1c2c7874e18e61d8c6954b8b9cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85111711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a572b6f25692ccb7fe1f0c595cecea53f197a047fa2e6af8407954dff2f124`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3761307c056e951ec91b90795b3c4e54498e89b111b7a76e5053261ba9355f7`  
		Last Modified: Thu, 02 Oct 2025 01:35:02 GMT  
		Size: 57.7 MB (57728604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1b64de11cd4b6ff58525d1fd0c25938d2485478b048b1df83c0a9628c03cc3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e17eeb3c7d1d50ae9a3c2c604aaa046f2beb13c752548577c017be3f355a92b`

```dockerfile
```

-	Layers:
	-	`sha256:8a94dad6b92adf83e202ebd32c59de53d1fe03fbaaa26cf130bdf490077bf2ed`  
		Last Modified: Thu, 02 Oct 2025 03:08:19 GMT  
		Size: 2.3 MB (2293781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2cb54bc26f7a4dcc8e35f8b18791c630c4433204075ccdfbd15457e7d023b02`  
		Last Modified: Thu, 02 Oct 2025 03:08:20 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b3f13cfb74ac5a460e4fc3b0cd03058fcd89b48047f63b4f5645b2739248a1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93992177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940eecb8c36bcad33b61328c5e9b80e2cebabaf9310b58d8e2ae596dc9adf0ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91da728f2d0a82b453c9741a3bde8cc4c3add71916c67b2a1d728429a9aef170`  
		Last Modified: Thu, 02 Oct 2025 04:41:09 GMT  
		Size: 59.5 MB (59545388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:854300dd1fbeb4cef9f9dba2e973561e0b19641a337da508da5b49009507d169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952f148239db4104b64e8200afcfee7245abc7e593373a02a9ff80caf1008fc1`

```dockerfile
```

-	Layers:
	-	`sha256:7a83fe2df33f5ba1e2a710354f14d9e199fa49ae044b23163e39a8e442fbf74c`  
		Last Modified: Thu, 02 Oct 2025 06:08:29 GMT  
		Size: 2.3 MB (2292134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a841a4c5531068c47dc8eb98498b7072a7e8d4a500b2f4f0bee8f17ed3b84e0`  
		Last Modified: Thu, 02 Oct 2025 06:08:30 GMT  
		Size: 9.0 KB (8967 bytes)  
		MIME: application/vnd.in-toto+json
