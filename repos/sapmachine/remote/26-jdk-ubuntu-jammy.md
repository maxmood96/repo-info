## `sapmachine:26-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:fcf07e7825dbe82f3c45daa78aa61850bac474eb9eb47be58c8a48e73de58dd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:1d3d38cb9e6105db77076e3ccb05679dd5bbdc33e686219b27c3803a6529deb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255718021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d0f9441920fc40608bdf8876dd8187ebcbc463548550bf24cdb26a4573b94d`
-	Default Command: `["jshell"]`

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
# Tue, 21 Apr 2026 23:02:45 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:02:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:02:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fc17ce8ec545eeea52d4a03803012d8cdc57e62699924287c449427a240adf`  
		Last Modified: Tue, 21 Apr 2026 23:03:13 GMT  
		Size: 226.0 MB (225981523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3b3a76f21d05d8e00585d96142785ff36ef58b4106292cbf53c154716d057a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2632323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd9d9857e8bf197ea4b25089a4f091f73aa077a2d581f08ce34a2379df923e0`

```dockerfile
```

-	Layers:
	-	`sha256:5f2a9f5dfa065e09028832a692b7f5429f72ee3f78404b784dc110d7e780c64d`  
		Last Modified: Tue, 21 Apr 2026 23:03:02 GMT  
		Size: 2.6 MB (2620953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1352bf590ac2c680e342e3c5565eeb1ba202ab58871ca6ab249957f8483716a0`  
		Last Modified: Tue, 21 Apr 2026 23:03:02 GMT  
		Size: 11.4 KB (11370 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9c4b3aa18f8b53d5e55a78ebd44be9b0debcf376b3dcd588e6f5a174d5d9a588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251418880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7848960ec6e17fe822afb30251fffc99110a634113adede1423493d5a6b3366`
-	Default Command: `["jshell"]`

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
# Tue, 21 Apr 2026 23:04:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:04:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed36f6316d00f8af4c4d39c4275965906218e231557c5abb70e193d92419d61`  
		Last Modified: Tue, 21 Apr 2026 23:05:25 GMT  
		Size: 223.8 MB (223812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f800c74efb1800ea90bafe8ada581df25437b364b3670444fd1c4c25746a3138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2632298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757feffc65a818554ec1657d3e3d701e57bb26fecc5a7a39aee322d68baa376f`

```dockerfile
```

-	Layers:
	-	`sha256:c25e391c13c00a68edfb71c35de17e5ff93000216791540ac6b356b775409f2f`  
		Last Modified: Tue, 21 Apr 2026 23:05:20 GMT  
		Size: 2.6 MB (2620728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4176e8d875f12b16da2b1c28f6982b8aeb840fb6fcb77d41bfccac7c5b10a1`  
		Last Modified: Tue, 21 Apr 2026 23:05:20 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:81fd69dbab894bb38a68907d25a1d47492a57106585649eab2285407838664da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261810270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f9e5f1ac227df459b680d21bf0f508adddf19266c4b6ba41829121ba3d271e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:08:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:08:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62874f3b4f2fe0cccaad2106d1aa2507888493b64951dda69054fbd6473e3b70`  
		Last Modified: Tue, 21 Apr 2026 23:09:25 GMT  
		Size: 227.2 MB (227161872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ea78f812fac7b4bfd0699a8e5e1c44e75b60c794db37b16326830b5d29f5ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142171b542376049d8b88237e113741458c2935dbc2d52cc46261d1640d3a9ce`

```dockerfile
```

-	Layers:
	-	`sha256:993bd9b9be5edced6c4c17c9b8fd3abf5a15a31bb3dfccea57d9e9a3008f1986`  
		Last Modified: Tue, 21 Apr 2026 23:09:20 GMT  
		Size: 2.6 MB (2617969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7312ce1fe03a55785f96f5dd3294d26c9faba87b1ac6b5709eb78ebd1e49205e`  
		Last Modified: Tue, 21 Apr 2026 23:09:19 GMT  
		Size: 11.5 KB (11462 bytes)  
		MIME: application/vnd.in-toto+json
