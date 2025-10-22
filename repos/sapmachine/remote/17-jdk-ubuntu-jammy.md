## `sapmachine:17-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:bd1597a8f826f2a443916c81aeed3307e28c66fcbba96af6251b3242906d9fae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:2b4f081b531b6f5e53d8009b6f02c12c30298df8fb2ba954f359e4fe5ab6cdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229635498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419e21d656feedf53b492e720f3e5627a2ee58e8625c28ac565064c8f189b21a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2932a4014f7319ebcbf4da5669f157b2989ff27c2098e417904ad3aee17f7a`  
		Last Modified: Thu, 02 Oct 2025 06:14:50 GMT  
		Size: 200.1 MB (200098680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5f3d6b69ad21bf8b56020889bbc84dfcd60cc42a0e5eeb92840baadc41b1486f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45396751c78b45a9ff42c9fd110b15e5ad69f00fdbc45e00d2804ad8e969c20d`

```dockerfile
```

-	Layers:
	-	`sha256:1814ba8ee91e2b8d6a6df996272ae26bb473e0b69cb22bb267eed06a0311a322`  
		Last Modified: Thu, 02 Oct 2025 09:06:48 GMT  
		Size: 2.6 MB (2627863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd1386095e577ca90cc6d181613362e5bfce3d4f4bc15fc496ac2dbafb41d67`  
		Last Modified: Thu, 02 Oct 2025 09:06:49 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d81bdeeb2f77376d49cf98999c23cc7ec152d7dc88823d1e54c03062a0d8019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226334778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3e0237bef8d0b928b8e7ab6b16ddd439c6fa84d07c2a2de6db73bb3af5ea5b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09427dbff66b1148852713102ca1896285b8dbaddbd9b87dd6b65c672b685812`  
		Last Modified: Wed, 22 Oct 2025 00:06:44 GMT  
		Size: 199.0 MB (198951671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:930746b4de97a946e6303f30095190881c797a1c091e96d72a99806115502345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5970e5ee88c5a217087923db7681421b3683ed6f80b303409b52db2b2645abd6`

```dockerfile
```

-	Layers:
	-	`sha256:af909bfbe451e57831bcaa8a2e1ac3d6db3754ed5be07ef40a178aadb55832f1`  
		Last Modified: Wed, 22 Oct 2025 03:05:03 GMT  
		Size: 2.6 MB (2627593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a724ca441fc056babc58f03083314176b24395a4b70c78fa0d75027072ac6da`  
		Last Modified: Wed, 22 Oct 2025 03:05:04 GMT  
		Size: 10.3 KB (10290 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9ea5cf3b62a5cdb8e634865637c371a5ba5553ee95ef2598d4679c8c81238ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235214032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b380bc4b0c0f7431ce6b25c0107bbb625e46240b2a28ace593e2ea34e28d9afd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4090fd090ce96f2f32daa2bc757c0bdb7c90e3223dc64050ae77d4ca5c8bf05`  
		Last Modified: Thu, 02 Oct 2025 04:48:53 GMT  
		Size: 200.8 MB (200767243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:01fb63e06069747a5a394579714164cb00b66611f3c060975cf22702b3e2b944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f20d4a522fa4a72465d81aebb2c67381c3232b4cd4e05bc446deadb3a5409b`

```dockerfile
```

-	Layers:
	-	`sha256:0f9d1fe8de321b665942bb91a1fe40157a9f069cc0a6d658e18c0802cc7ccf02`  
		Last Modified: Thu, 02 Oct 2025 06:05:12 GMT  
		Size: 2.6 MB (2624056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652de9e4f46f68555f0a1f662265a28ae15f8ea3785a87e16f42c9e06bb48044`  
		Last Modified: Thu, 02 Oct 2025 06:05:13 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.in-toto+json
