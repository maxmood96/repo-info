## `sapmachine:24-jdk-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:b67d9f2418954b4384299152753b070219a4e57b49a8aa34e4dc2c374d77ece6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:e230fbcabc056b778a1451a717bc3d998fdab85d11ec0eab27feeb0dccf83ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259072540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c99ded0445676080234be8a304746bd9ed6f2a8ecfc8a66e08b66ed5d196fb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14b84e538a124d71a956b0c4927ef62171d1be199b6d94384deecf55fa9c0d6`  
		Last Modified: Wed, 09 Apr 2025 01:21:08 GMT  
		Size: 231.6 MB (231562146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:96435d760de4407c855636d9c5a001b431f730f41ad0fa121f99dffa9dcaa635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04356a79bdd0418f3f94f2bbb1352fdf81d36e2c63f27176682d744e13458fb`

```dockerfile
```

-	Layers:
	-	`sha256:dbd95bb1f879038a711cc0f94cca39a1678840cc0cb16add9e6534c58ab56bfd`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 2.4 MB (2376040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c75753289dbee3a138366cb4e42a49326a58091c45fb9ba73f9432482154278`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 10.1 KB (10058 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b691e2cc2331550f32e1c8e6e44d5dff27a0ddc4744d2d4e1796e9962bd5206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255452166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8188ebd7504bdf88802c624187544118c6525c8e0c6da0041173ada4cb5c803`
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
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43029358d94f864614bd834bdd0b7853c6a6ab1b5ed827e2aa871496c54709ae`  
		Last Modified: Wed, 19 Mar 2025 20:40:38 GMT  
		Size: 229.5 MB (229478338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c791ed7b3ffcdbf67cb190044e5964ee11d0131e5cf5c879ac8b6973160734c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a2fa4194d8b73a3e59137d5ffee5cc27c2116cb8a9b2a8a4c1be32d1206164`

```dockerfile
```

-	Layers:
	-	`sha256:de33325eaf3f386e9b4bf6282f0f6d98a996d40e059e57910d2cd0623ce54deb`  
		Last Modified: Wed, 19 Mar 2025 20:40:33 GMT  
		Size: 2.4 MB (2375623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ceee1c2eddeda6f1ea3ecfe66dce8ed1ad737ccf2c93c96e0f2a613c458461`  
		Last Modified: Wed, 19 Mar 2025 20:40:32 GMT  
		Size: 10.2 KB (10212 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5e690c50c6fb4abe0ba0341dc3c448b509481fb8073936e9d5d20011719d4a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264486052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff824ebb9d11fb69eb70089620819bfd2fcd94e80e64ead05b9b8709b18abca`
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
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2f91e668a37102f7e14f5c4f37af4ac724e56d4fc651e36bc92a5f44c14d42`  
		Last Modified: Wed, 19 Mar 2025 20:46:02 GMT  
		Size: 232.4 MB (232409546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c296f07c6f725e6ae33fa7809b3e1229c06fb6d9aee31cd949d78042b7c3666b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccdc8b0ededacc1f999d3fb02d7576d0d3d12d217538a142e36ac8c647eb1812`

```dockerfile
```

-	Layers:
	-	`sha256:87b146bc5efa807e26ddf0795800c8e1e27aaec91913ae0f073021090cc4ea6d`  
		Last Modified: Wed, 19 Mar 2025 20:45:56 GMT  
		Size: 2.4 MB (2377167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752bc345500135fa631ad222d37e0b0304a0ef20d8770c4554d00e5e143f3328`  
		Last Modified: Wed, 19 Mar 2025 20:45:56 GMT  
		Size: 10.1 KB (10129 bytes)  
		MIME: application/vnd.in-toto+json
