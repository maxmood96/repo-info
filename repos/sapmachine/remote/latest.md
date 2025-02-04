## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:e09bbe282c913777b9206b2ffda087c8f437f9c373a4d51f8a68b7dbb4b0410a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:53fbfdeb9e479772ff9c649c50e7b4daae4f88a8353344738fc775dea321cf0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252399003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fcee0677ac1680e92c4382dba4c7fd3d3029b761d80379d10442399833fad2`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204da73253b023e94b8c12e04a9246b16bee3ba115ad94e578308c5ab575898a`  
		Last Modified: Tue, 04 Feb 2025 04:48:06 GMT  
		Size: 222.6 MB (222644713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:581d5f92763eba30929d94d60e73865dfeb3a4f397f017ac1a8554413960b328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2491581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab836867bafb93ee797a56b87c66ee202b036753d0c469cd0224b1a775effd2`

```dockerfile
```

-	Layers:
	-	`sha256:a3f1140034399968204c1a5f188319f0e6b68cdf6ea89584b4f010a7731599ab`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 2.5 MB (2478296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3004ed11c2994080b9c41f269ec3588ddb5d11858d6815dc43e30f69395043b`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:latest` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2a0e0d61fc3350e11dba57247412da025801d0ea97701c80001c0f94a3f4c3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249553181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44cd6cd3ba25e8af79e991f33230f6f755cd1cd5ea241fec7ca40baec15ef79`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b393702c63139f241a7b6ced4149bb2562ab7387f078624a5a9699610f318533`  
		Last Modified: Tue, 04 Feb 2025 15:17:29 GMT  
		Size: 220.7 MB (220659583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:455f8d1206ddfa19a9a5c4dada86eccf6b87015678fb48e78c257a5bb0c92f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2491859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aacdd77b243831447609553cf5ef204bce882d3f73cd4035e278dffc2d85f93`

```dockerfile
```

-	Layers:
	-	`sha256:e5dfa230a5de097a3c89cb69f079ba109d7a2006a9d3350315d16f47cf8a093a`  
		Last Modified: Tue, 04 Feb 2025 15:17:25 GMT  
		Size: 2.5 MB (2478302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f08102bf421832a63f3a865860e00818d59c9ec69ffce6bd95329632f56b88`  
		Last Modified: Tue, 04 Feb 2025 15:17:24 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:latest` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:22dc7f44255795da230e8fdc05c3889d82023eec2141a78de0e5d59d98c75998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258194706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a56d17e2fca0f8dd83a0776ddb52068839b2aca89592b11b9dcbbfecc4353d`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cb504b0f0b39eba54f37a5a1b7530fe147dc417b465dd929f2900968e88702`  
		Last Modified: Tue, 28 Jan 2025 02:17:22 GMT  
		Size: 223.8 MB (223805886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a6491657c7187e90c43ed9f16d41f5af736c6f8541434a9b354e8e2e91938220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2489206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5cc499605eda870d5e0cba1a47fc7bb8bf906dcec799c3ca3e8754192bc74e`

```dockerfile
```

-	Layers:
	-	`sha256:1789c6ffcf33f384b350c60af4ada14a43fad0cf996e54c28aac73f92c332799`  
		Last Modified: Tue, 28 Jan 2025 02:17:16 GMT  
		Size: 2.5 MB (2475793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ba5c44c203a21fd5539ca931fc9de3e74c2035cf28b403149918ef2341a72a`  
		Last Modified: Tue, 28 Jan 2025 02:17:16 GMT  
		Size: 13.4 KB (13413 bytes)  
		MIME: application/vnd.in-toto+json
