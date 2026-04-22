## `sapmachine:lts-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:4693790d754a5f0d56a9aa5e06246aa6b81f7cf7e46daa86de409a82ded7876b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:75704145fd41fd7a3a8f84c12448d34bbe15587122848a5b37a59cdfb8b80001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87805611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f555849a6ff7d61cf95dc3f8ede2965574014c74b21f360a58a6f64377fe353`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:03:31 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:03:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911938b11375c3ced4bed2b9cdba7ed5ddb06572ceac98b72d7791c0abc62086`  
		Last Modified: Tue, 21 Apr 2026 23:03:45 GMT  
		Size: 58.1 MB (58072633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d77ea36dae5a2601ba617259944fe7ae811ec847f45fdc12664ce8aa194a5be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec1aa5a6b7282a172575a84913c9daa96e2c5761bff5e7fdb2038446b20112b`

```dockerfile
```

-	Layers:
	-	`sha256:71f5eb821bf650fb0e375d29e1349e6813bc13afbc31285637bb5edc9d7f9b1d`  
		Last Modified: Tue, 21 Apr 2026 23:03:43 GMT  
		Size: 2.5 MB (2527808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88bf29be40f583911afed854d30846b04390825194b1693391a7064e88643616`  
		Last Modified: Tue, 21 Apr 2026 23:03:42 GMT  
		Size: 11.0 KB (11027 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:703ea78bce3010a94e02c372784d909367b284bc5b6a677f0f531f2537c973bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85916458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7dc0807a0d76d4575acea174b7f3226d9382ebf8fae5f6e3d75e5ce8e0d3ea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:05:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:05:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:05:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e840226fffda2ff6b26c6021211589825a48bb5330ea5e417e1fe06bf906270e`  
		Last Modified: Tue, 21 Apr 2026 23:05:44 GMT  
		Size: 57.0 MB (57040673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ad61d99426508c8bf558fe0e17fc8df4a616203fd1dcc2e5af6b491281ddf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50d3bd5316ff9b0da47fbc6aed7f796bceefb31a50ba0f017a83c6cf43a51fd`

```dockerfile
```

-	Layers:
	-	`sha256:cce612831ffe64a75c07c09f119e9b4d38f3e847d9ef59bb5780002b03c6f271`  
		Last Modified: Tue, 21 Apr 2026 23:05:42 GMT  
		Size: 2.5 MB (2528357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806be20813fc6d921d10c448877d689bd0b43f965f09f7acd28a7638b8b4d603`  
		Last Modified: Tue, 21 Apr 2026 23:05:42 GMT  
		Size: 11.2 KB (11215 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:383212c0215397fcd1b8c91c318e70b3acdca919d192a4c158420c6674943b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93262320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9c1fc8c7994a9f91a9b1f94fcfcdf6083ee3cc4973c1aafcc5c42725f891de`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:13:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:13:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:13:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5021ff4dd3d3b92b31c20f187ae7a04551adc5f2c6b3a628fed666247f1f6e7d`  
		Last Modified: Tue, 21 Apr 2026 23:14:05 GMT  
		Size: 58.9 MB (58948142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:784955ee5560ecf55d052ae733f1e89f6d0ea85824980bd750d1169313cf84f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5a0e9a984fc81f1c2f6c8142816d0c8819cf7a2cf31656cf18f9b63754bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:7d4118b9e970419c6e1114ae85734ff3b290888583dfc9773e9de9bf7562035e`  
		Last Modified: Tue, 21 Apr 2026 23:14:03 GMT  
		Size: 2.5 MB (2526694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f027065e61b8b6181af0b29b2837b2e4b8611fcb7fa7630293ca3d9af6976e`  
		Last Modified: Tue, 21 Apr 2026 23:14:02 GMT  
		Size: 11.1 KB (11112 bytes)  
		MIME: application/vnd.in-toto+json
