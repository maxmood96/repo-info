## `sapmachine:25-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:3e0bc02623cfae245c621bcb45adf075dd8d5288e0a1b8ad053c5896121d4385
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:5f99c20ebcbb79d968c5d9529cd58c3c11c7f0fa6efb7de816263b8fc514d9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85864958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f97e2b876eefb7253bcd55bc9a465773820d0ff4c40d12537a6ff725aef4d59`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:58:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:58:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 20:58:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769ff44de107ad6d101e462d087be00bda25f7cccf093021617c53aa25ac9f34`  
		Last Modified: Wed, 15 Apr 2026 20:58:44 GMT  
		Size: 56.1 MB (56128460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4789f27d4d612ca6aac9847ce1904514e25a52fe35aee16aedf3acd8f13f0941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8eeae987247d15f36901c90addf62f6da9fd99e43b6676e33e0a8299a44a367`

```dockerfile
```

-	Layers:
	-	`sha256:598fe1d53c1246741c667df2918fee440a3f584ebc499f0c11f9701658648b4f`  
		Last Modified: Wed, 15 Apr 2026 20:58:42 GMT  
		Size: 2.3 MB (2302355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8075addcc5a0a0c901ae3885691a8e82db2d4c1d6e2e86c8ab8ab0cbf1e670b`  
		Last Modified: Wed, 15 Apr 2026 20:58:42 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ccafb096d62fef39756660c6600d9485d685b1d6add2630eaa38094ced7d65e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82653018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54af013f1fd65653e660f61225bb3eb62f8469d5fb232995d1e5817403d8b296`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:08:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:08:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 21:08:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50efcd9ab5c4f89a35ac4d4b491120fabe0d0e804d926f58b66ce104a5022fa`  
		Last Modified: Wed, 15 Apr 2026 21:08:50 GMT  
		Size: 55.0 MB (55046475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b48c3ab3b727dfae9ddbeff6ddcb3e66adc541a05d1b3ce6ba71a3fc2516f860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a028df70dba8ec1852b73ebfb638b11ae2bb6c82c3708674dce0afe3a99289d7`

```dockerfile
```

-	Layers:
	-	`sha256:c33068cc9b9bf905d58b91d398eaf3c59692d0367182ec5db73ad00806ca6e39`  
		Last Modified: Wed, 15 Apr 2026 21:08:48 GMT  
		Size: 2.3 MB (2302048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ef5fe7621c4f1904b3b6faa43d53ce914454e7bf86c0fffd25fc673439ec4f`  
		Last Modified: Wed, 15 Apr 2026 21:08:48 GMT  
		Size: 9.7 KB (9712 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a7a194f310f92c22376875c7d761fd4c80a2f287e5bff3111bdd60038788a8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91483012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2aeb656d5dea883186dcc79aa40f9e4bb3766feff7889643308d25306c513c`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:46:51 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:46:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 01 Apr 2026 20:46:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a8390135ba6c4580317ea313811a44ee1769143631509ccc5e87c68902b61`  
		Last Modified: Wed, 01 Apr 2026 20:47:15 GMT  
		Size: 56.8 MB (56833352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:19f66ec14aef723e9aa8a39e9572f963afac65e53fa5bc4e3b25e1ba48ed99de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ed24cd7bb7d68facba402a8408952df043e90524f8362bcd61d315ab1810c7`

```dockerfile
```

-	Layers:
	-	`sha256:4d39e283e0889d4ad7fb4af2aba25d0776df4a4149b323b734ae286d33898d00`  
		Last Modified: Wed, 01 Apr 2026 20:47:14 GMT  
		Size: 2.3 MB (2301179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a39db2b186f275fd1a41bfc341d3bab23033eb892b74eb07997a70bd7613cc`  
		Last Modified: Wed, 01 Apr 2026 20:47:13 GMT  
		Size: 9.6 KB (9640 bytes)  
		MIME: application/vnd.in-toto+json
