## `sapmachine:jdk-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:69703c715245f36c08cb7f4e43c394ee3cf5ced75eb51c3d69d3926ff09ae856
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:d7ee0de5fadc11942756f82b86245274421da1a5af7707bdee544710647b5609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259072833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9871694211b52d718607869421be2032fa87b943fcf3f714217436dbe46f95c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0af3d6f7b8986e848a37e7969774120d15480d8511c6ed13c2530bb85d2177`  
		Last Modified: Wed, 19 Mar 2025 20:33:33 GMT  
		Size: 231.6 MB (231561773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:428f875c9577a72e6fee1b5316ae085e4ef3239b65648926b4cbc11b51869788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b236ae94a55d84d00acd09ed6c304409a2885b66a9428449fb2d294da4ea8e4`

```dockerfile
```

-	Layers:
	-	`sha256:301e3a48bbfbe8a88fbe5d1a200a9f03d0d3f2539a93a7c5ce6bb5148e034260`  
		Last Modified: Wed, 19 Mar 2025 20:33:30 GMT  
		Size: 2.4 MB (2375940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e47badcc1cbcd00f9589ff60918fa01256c18b201f551d9e6f695e5adb325e1a`  
		Last Modified: Wed, 19 Mar 2025 20:33:30 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-focal` - linux; arm64 variant v8

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

### `sapmachine:jdk-ubuntu-focal` - unknown; unknown

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

### `sapmachine:jdk-ubuntu-focal` - linux; ppc64le

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

### `sapmachine:jdk-ubuntu-focal` - unknown; unknown

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
