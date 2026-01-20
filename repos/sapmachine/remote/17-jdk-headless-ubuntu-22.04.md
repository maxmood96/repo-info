## `sapmachine:17-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:3ed76b30f5b55d8863a0aae3aa2db6363a58cd300b095927f8694b7db2524923
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:fbad8e0092e0c81054a8c219d0a9e2faa8c4dc3579fe7de54c7f3d3903e3b5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228601387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ba38a87d442c9740be053d6d1bc063f4c9521796c85f2530d5cad878ff3e95`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:45:18 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:45:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 22:45:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42167e47f19001b5bda92d97d09c07968f6b471d9abb5f9a14c20ee6f6c541b`  
		Last Modified: Thu, 15 Jan 2026 22:46:04 GMT  
		Size: 199.1 MB (199064720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c74298e47d87ee6b891e9e1114e373fd753f6f251f62ea7643036ec19794ffa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121a0c212a5b34b5364c0056a0aba3ab75db66cbf7237edb9e54922433039746`

```dockerfile
```

-	Layers:
	-	`sha256:e1ace982c8554e90db4cc5f91a6f3847cb304a5624814e03313e5920040ca13a`  
		Last Modified: Thu, 15 Jan 2026 22:45:34 GMT  
		Size: 2.4 MB (2375779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8743636c81bbbcc5b8ef9b52f4ba56372042ae25f7995f29a1ce833aef0f30`  
		Last Modified: Fri, 16 Jan 2026 01:08:08 GMT  
		Size: 8.9 KB (8889 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8ba478ac7a72e5d0ba7ecf5c471ca17bd2f97f8b8b9d4d50fd45a38fe0732fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225122297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e0f9242f88ea14d680972f368bab96f58533ba3de14c1b7c8f2df064651651`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:48:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:48:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 22:48:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58942fe72c01471a19c842797759a1b555958d56b869a050637244d0e925b25`  
		Last Modified: Thu, 15 Jan 2026 22:49:20 GMT  
		Size: 197.7 MB (197738800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:af8c4dbf52617a679ae50610b66ec48cd0552368d8f356f5ace4f59edaa2b61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af18150876344c66267aa7fdd5a035d2bf5763431a8e47c046b1831cffbe1da2`

```dockerfile
```

-	Layers:
	-	`sha256:6f7a8aa3086725b6821453204d8772d1b29c20b61709dcedc3b1d859a0969dde`  
		Last Modified: Fri, 16 Jan 2026 01:08:12 GMT  
		Size: 2.4 MB (2375451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d1fea0299b2ae9e219ccaa79aa2a1eab2be59626a01b3bd218bbc2199c4654b`  
		Last Modified: Fri, 16 Jan 2026 01:08:13 GMT  
		Size: 9.0 KB (8994 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f0bda9990c40a6fd61ae8f897e18d2ed82c6f544e2ec1c6f453b9af1bc138cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234016260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7771f13724b771105bc361a8fc4add10173b8c6c7dfc3e36e5b37ad9e279338d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:46:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:46:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 23:46:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Thu, 15 Jan 2026 21:43:22 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c657b3c939c6f0b7108e00dd3a429ce5b45fd9be6b025b019944d4f026646e2`  
		Last Modified: Thu, 15 Jan 2026 23:48:00 GMT  
		Size: 199.6 MB (199569298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6e641f6356ccf855dab8f6cf08e5ca9aba81a575faba93467b4ada91f17621e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9144f43bc8e3e9bccd809dee43b00b7d8acdb2ac311a029c980b586c16abcb39`

```dockerfile
```

-	Layers:
	-	`sha256:fa3f189a3ae472b7412eb0c59c109ce968b5f8b971446b8b6ea233b4810abdae`  
		Last Modified: Fri, 16 Jan 2026 01:08:18 GMT  
		Size: 2.4 MB (2371858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b960b1828cbe3c4887dc976cc32888b68fad6e46d32d32eea94d38a44a236be`  
		Last Modified: Fri, 16 Jan 2026 01:08:19 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json
