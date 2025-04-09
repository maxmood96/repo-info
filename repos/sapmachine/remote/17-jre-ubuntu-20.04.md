## `sapmachine:17-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:5380239926955909f79dbd7fd344b900936dd89855616130122c5c0a7bb0b61c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:4b0e61da73cfd5b4b8bd36dcdb147582beabe700e7b5d40005e84e6d3361c300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80870724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b46b76aa52ea0c1be3e1d4d22b02542beaa527664fe17d3cc8b80c2755acf7d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817caa83d63f0af3fde6fa46686a1c2b549748b2a67d9bf199321585627f986b`  
		Last Modified: Wed, 09 Apr 2025 01:21:49 GMT  
		Size: 53.4 MB (53360330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5280417f58c30bedbabc3189db4ddc0a1ac33cf2ae19c675a6200b4e8934c997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720649190cbcfdcfac3037d59b4c4c0aa4dff8a37e06af1c30feb5154fbd4f38`

```dockerfile
```

-	Layers:
	-	`sha256:a4fddc9933f168e351f80f1bcdf58e22eb1b7722157b6a0ecc8015fdb8aca2ee`  
		Last Modified: Wed, 09 Apr 2025 01:21:49 GMT  
		Size: 2.3 MB (2299303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fbd49c4957cffe877459412d9dcf764430cbe817705fb4dd0a0c76c71c39ed2`  
		Last Modified: Wed, 09 Apr 2025 01:21:49 GMT  
		Size: 8.8 KB (8821 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:17485c52434316a63beaa74909ec6d8fccf7bc85061b89ac1900a52b9693f481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78767076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892995c57208eb9b1f77d2aa7b007af322f5b4f4bf8e16e088d75f0ac086b54f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fb41b93d3b811ec373a47f588f934adf7aa004cc88beebc3fe18491328378b`  
		Last Modified: Tue, 28 Jan 2025 02:58:49 GMT  
		Size: 52.8 MB (52793248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7fe44dacaf011fcdaf9e85f0bb09574dc582a43e57fcbc7e229f98c154c853ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c497bdef017491884089ee3e4e555b78e9f72b74dc420629814a7be1907b8d`

```dockerfile
```

-	Layers:
	-	`sha256:1ef54b29734cedb65ae2f9c5cd316d6fd20f4c9b6e48d0220f4d70953e031805`  
		Last Modified: Tue, 28 Jan 2025 02:58:47 GMT  
		Size: 2.3 MB (2298841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8ab2305c55acbed3d26038f5802ed16a544068910965e57169d6352436d58c`  
		Last Modified: Tue, 28 Jan 2025 02:58:47 GMT  
		Size: 8.9 KB (8924 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0633755f8373ba9bb257ae99e1ad21084f1732b325dab98fd54e9b962e6c2922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86568236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc487a39d39e86b253444a5ab8db479d1d2cbd4275c4cc12f9b272bb9328bbb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171a97e88ee8ac7fd610d5258e80ea63c010798edddd333fbc4dd298062113a9`  
		Last Modified: Tue, 28 Jan 2025 06:30:31 GMT  
		Size: 54.5 MB (54491730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b75dfb188fd1695304d97e9cb771a8de838b8827f37cea2eec49827a672febcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63a23296c5ea9069edc9bff396e571efb9c727ab8b046264f64c42a6004106a`

```dockerfile
```

-	Layers:
	-	`sha256:4093bc8f1b9df90f32943344576b7553d95ae17b0ae863af5db40bbf465d8913`  
		Last Modified: Tue, 28 Jan 2025 06:30:29 GMT  
		Size: 2.3 MB (2302970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52b3309f13e5f906ff6b6213a70ee86c7a0ef685638e16172a56b9bf2a2ad8e`  
		Last Modified: Tue, 28 Jan 2025 06:30:28 GMT  
		Size: 8.9 KB (8865 bytes)  
		MIME: application/vnd.in-toto+json
