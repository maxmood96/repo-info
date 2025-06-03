## `sapmachine:21-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:8611ac465dc8e7ed4c8c48a1168d6e26272415061b6e8fd1d7b06218017846ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:1d017eff8972d07ac3e12e6fcb12818d133365b8e6450debb057bf9230a531a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244264207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620e28a75b32e5f0a06e6aa2c49cad4f6fe4ce0d9e225507f49ff3719c9d632a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a4750eb5e7b5f03d94bdf2700de0950f4bc5f670b2dbd6cf983302ad25e357`  
		Last Modified: Tue, 03 Jun 2025 04:17:54 GMT  
		Size: 214.7 MB (214731204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea104fa785531c1ee8e579255c9678d5ac7f80d5b609a99f21b3ad275732a697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2532636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78094ad987c7a2c7cbfa6a2e8d0dff93673185baacbcaa1a163347024afdb664`

```dockerfile
```

-	Layers:
	-	`sha256:abaae4ec0c90e213b2a6fa62d0c11d8ef4733382b9ee5c7a1d5adbc490486aa7`  
		Last Modified: Tue, 03 Jun 2025 04:17:51 GMT  
		Size: 2.5 MB (2521191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcc3bd9148eec82cff1d8a7e0c2b708a5d7d82c7d156a23895bbe06b5a024c81`  
		Last Modified: Tue, 03 Jun 2025 04:17:51 GMT  
		Size: 11.4 KB (11445 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c7dc2b66c5ec38e0753949793945c48c689fd4a39b83ec363d0ebb4e7ae82502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240298292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee67a6f55a569bf127ebbcda0cb0d85eed38e5c2f8f92eeb07692425d00f30f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877711cfc9c8b8234cc92f25f5016844e14fee0e6644392f7ef73938b50a057e`  
		Last Modified: Mon, 05 May 2025 18:34:34 GMT  
		Size: 212.9 MB (212944081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b57562d5bde7dbb04e1bbaa5f42c9e90ad7a7ed321cf42f8b4708f29005cd0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2506280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b4d236c9e0a71bb265d4e2dcc123ec368862ac255dcd98c845567e18504813`

```dockerfile
```

-	Layers:
	-	`sha256:7e0f96e46d90a8ff22530499e6673b2a6bf65f5be0a149beecfd5cdab2b036d9`  
		Last Modified: Mon, 05 May 2025 18:34:29 GMT  
		Size: 2.5 MB (2494635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535da88c769b046cbdea85d4df87c18ec20a40d3abd32421f31dd111e8b2e05e`  
		Last Modified: Mon, 05 May 2025 18:34:29 GMT  
		Size: 11.6 KB (11645 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:087ca1e1e62f2619ee2b5ace2a4386c2c30e8fc3fd314b71ab4d3bd0c457efee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250474138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bd5f359066cce2c5e8f5e03dac4c967e0eefb8bb922cc55868b8a3da5e8ad1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2761f4884d7a6273e3bf2e2963b10b77321cbf651f626edbc12e261d94a80d`  
		Last Modified: Mon, 05 May 2025 18:28:13 GMT  
		Size: 216.0 MB (216030923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8f67d7e8bab6fe7ae515819491f53d2c388340f4a0f8f13273d7cc66e323d7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60cfd47961f4705e2e3655dee0892933b31d2940a55d741276c971d3246165d`

```dockerfile
```

-	Layers:
	-	`sha256:453c10a82d3c9e6e1f91f65a2a967b91ad9321cecadae0d90501b45f149a7bfe`  
		Last Modified: Mon, 05 May 2025 18:28:08 GMT  
		Size: 2.5 MB (2496940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b82a0426254a30b5901cdc6bd268ce726aa044a831742290f1fbbe40ab83da15`  
		Last Modified: Mon, 05 May 2025 18:28:08 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
