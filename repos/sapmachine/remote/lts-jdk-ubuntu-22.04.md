## `sapmachine:lts-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:2d5cd204ebbdb7e856b92ce4e95807189380f3e5ad6489547df1200fa81dda0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0b386c890a6865129e1402fde4af66a0890a5a557035fa0b63b3b7639b177eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244263790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80562ca62251c630ee0b4968742ecb7a5a6991cdd51f5885f9c4d09d6f40ad49`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38ab883b7fba415517a9aa23539eb0003ebe07ca5a84b404408bdcb6dfb5336`  
		Last Modified: Thu, 08 May 2025 21:05:32 GMT  
		Size: 214.7 MB (214731176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6c919e6634252383a15948cbc9ac4868d9affb035e0be280cc35dc68ebb92a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2506302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1add966a3196e0e21ad03f930dff5dffc35bb17dbc556094feb42c584fb567`

```dockerfile
```

-	Layers:
	-	`sha256:758c15d34abaab6e0a1415e218adff8f04310fb1d456e7031e0e25e737be6731`  
		Last Modified: Mon, 05 May 2025 16:37:00 GMT  
		Size: 2.5 MB (2494857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c07d51cef53f03a3a1c2fbe9afb1250ed2029a1ee678efe34a550bc4cbabce`  
		Last Modified: Mon, 05 May 2025 16:37:00 GMT  
		Size: 11.4 KB (11445 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-22.04` - linux; arm64 variant v8

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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877711cfc9c8b8234cc92f25f5016844e14fee0e6644392f7ef73938b50a057e`  
		Last Modified: Fri, 09 May 2025 04:48:56 GMT  
		Size: 212.9 MB (212944081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:lts-jdk-ubuntu-22.04` - linux; ppc64le

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
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2761f4884d7a6273e3bf2e2963b10b77321cbf651f626edbc12e261d94a80d`  
		Last Modified: Mon, 05 May 2025 18:28:13 GMT  
		Size: 216.0 MB (216030923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-22.04` - unknown; unknown

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
