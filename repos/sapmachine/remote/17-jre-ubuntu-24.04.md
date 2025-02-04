## `sapmachine:17-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:a2784bdbb96e14555037db4adcfbc213030f1b660926a75ac3b3b978ff5a324d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e12ba0a1fbd0443475218e4ef93cc67e2957f102bebc3eb38ef1ee602eb46b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83954636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f517d410ec6d37782dea70eecfa5249a01c127a81b146a8e4bb3f3bca0ab6262`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fed1e88515d5dce57005f39dfdd4f3789372168d44bc0477f38d65ae1dd90`  
		Last Modified: Tue, 04 Feb 2025 04:49:31 GMT  
		Size: 54.2 MB (54200346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4373096c064bc78ae7ec9250539b4621e2cee05245712c7245c4bd473d8e8ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a5da4185d7a7ca69a7ff0fafab993b35b60ae4eab50f1b8c639c20eab78768`

```dockerfile
```

-	Layers:
	-	`sha256:7252c771792d6c545478721d4e5bbf1717da2a8e849159e7941f9b7871b11be5`  
		Last Modified: Tue, 04 Feb 2025 04:49:30 GMT  
		Size: 2.4 MB (2387765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65355ffeac42033714b988898679d332360fb957d1c65b4d6d0ea8d8a466f4f`  
		Last Modified: Tue, 04 Feb 2025 04:49:30 GMT  
		Size: 9.5 KB (9470 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:beb447e4e8bf2a1978c2e4daa8cba7515af91b30a1c0ad3f69b0fa7dbec585bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82544137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b497d9e4704070d2696378f9f3b002fb9397d0c8c3a01d5a2600a7362000a0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7bdfc44b9382adbfc38fb4cb3b46d8c55cef2327b19c0924c981003aaec0df`  
		Last Modified: Tue, 28 Jan 2025 02:50:23 GMT  
		Size: 53.7 MB (53651466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ef058e0cef19adeccfe26e60e82cc10ef0242eeb5ad70eb3e4c32adf0557bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f678d8d64d01df78303aa4e8810a35f3ffe285058532c56267369d9802799f`

```dockerfile
```

-	Layers:
	-	`sha256:a90d917b38778b35b3050d213c7451f756009ec6d6e475c94fe025aa89020999`  
		Last Modified: Tue, 28 Jan 2025 02:50:21 GMT  
		Size: 2.4 MB (2384295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c63f23d303da11150284837592f1de7453ab24977711d298d6202238d15e23`  
		Last Modified: Tue, 28 Jan 2025 02:50:20 GMT  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b3e64ac1ad20a7775e5332609ebca4b5c48429a74f21db0683d076c14d05f2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90226219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cc936091a34e125f72d1dc855dca9c4a522ba7ad906c4102944f865114346d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7088ae3bbd8348758076a9cea7a01f5b5d4d79d34809d21f49207c0cab42c651`  
		Last Modified: Tue, 28 Jan 2025 06:12:59 GMT  
		Size: 55.8 MB (55837399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4ca684cc60e9deade6799c8b228eec8b31d79373df164c518f01b835a04bc663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46f81cd15f8de6b5ccf1e8c6a40a2c7f4576d73f5ff1a9fb04082afbad53e99`

```dockerfile
```

-	Layers:
	-	`sha256:33cf9fa89d79680d934258eeedad61b96bc07f3c9d49c0327da0fcc6717f1f30`  
		Last Modified: Tue, 28 Jan 2025 06:12:56 GMT  
		Size: 2.4 MB (2387754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbdf8cb09faa1462936ab4118d721dd08b4d2997d527338568aed68dab5d13d5`  
		Last Modified: Tue, 28 Jan 2025 06:12:56 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.in-toto+json
