## `sapmachine:jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:5f57c6a02e4fd3d7053790c1ff8fdfef0d89cedd0f71761f3e1f9a4e9d067bbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:91207fcc17c258f71c53f90f954d25221644f7a03dbd43766c7f1ce31d827968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.4 MB (263376342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0119d0f59f2610275ecfe05477966cb969356e768861bdb8450f83f05825d5f`
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
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cd345ec28d3c2ec15c4ce236071e3cc39fa12fc2849fd0ba40f2d7fccfbecc`  
		Last Modified: Wed, 19 Mar 2025 20:33:20 GMT  
		Size: 233.6 MB (233622052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d241f27ce121337b5c2f4f33f2b11923f3bcd047647395b1fd91aa90e1c99922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2235905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0cccde65f0a3432f264c327edfc5ffb1241d9474a8f5e616e74c6e0ed85bfc`

```dockerfile
```

-	Layers:
	-	`sha256:d7d118eeaf43667f15dc5146afd80c29faa155dd30330fa89abdbbc882c787b6`  
		Last Modified: Wed, 19 Mar 2025 20:33:17 GMT  
		Size: 2.2 MB (2226348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4a333812a20d19b52c82efb7d2ca5adaa9c220404551f659a39645e4336e75`  
		Last Modified: Wed, 19 Mar 2025 20:33:17 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:872cbb9a2f2e915bdf75cccd98326ff82eac9896ef96588d18ba634df6660083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260253896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf5521584fb8954bb83fd2c7033e1744e1499c601f07d4334cbd9b704a7c8eb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5376ff265040e57bb7e7d76f15e7dd7daa2f5fabd0a10ff689f6b2a7bc1685`  
		Last Modified: Wed, 19 Mar 2025 20:34:02 GMT  
		Size: 231.4 MB (231360298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2ccd859d8df89f506977fbdb763f448683676677342d2046eef4cf54ae44a527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8c5f33a0e90e6e336748d3b595cda4ca30fe2ff98bc392e93466e2d96844b7`

```dockerfile
```

-	Layers:
	-	`sha256:aa458612cd273b98e6e466b46d867a0c17aea542ac0b39efe1a54e45cd02417c`  
		Last Modified: Wed, 19 Mar 2025 20:33:57 GMT  
		Size: 2.2 MB (2226828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5950366204a7864f8bea5686a4353d066669a3d7e700ad2755b1cc7191506923`  
		Last Modified: Wed, 19 Mar 2025 20:33:57 GMT  
		Size: 9.7 KB (9686 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2e4aa76368dfc6ac404db47b598413b6b6952b5fa88f0ddd95bc21bc23298b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269371538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ace1b066e86756bdfd0cda674cb3343249ad5255139b7bcd43c78d1cc862ea`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8c947ff3331f03ae1d5f524e6f407911500e4b47f241052635ce1f6ca54ec6`  
		Last Modified: Wed, 19 Mar 2025 20:35:37 GMT  
		Size: 235.0 MB (234981714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:949331b5f2d8a1469640693040b3beddc376dcfca5e268b93965dbd20dc0f746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64199ca974979ee35222dd6ea5b6b18dc4c124e403bbb6b04084571bac14c96`

```dockerfile
```

-	Layers:
	-	`sha256:ef3e5683abd832322dcf63115e9c7535d08b5a1b844d5fcf4ee8a344c377ed10`  
		Last Modified: Wed, 19 Mar 2025 20:35:31 GMT  
		Size: 2.2 MB (2227672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea9a8c0db3b097aef5b864c46a70b5f1cf11b2c61683eec6c74913022660e05`  
		Last Modified: Wed, 19 Mar 2025 20:35:31 GMT  
		Size: 9.6 KB (9613 bytes)  
		MIME: application/vnd.in-toto+json
