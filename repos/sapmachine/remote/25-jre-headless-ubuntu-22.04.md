## `sapmachine:25-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:06c70bc66debc2d5b4a1c70e31121b242f49882b07b987252a54c21efc05c6ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e83e723750bff2d15623046f0dad95c153847973a4ac05777d2271a845608334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85209304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2ea1867bda0129f59ea4748483e56d008583b5552262ab3f988528267b3260`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5336d751cc54fbffe48b8dd58ded33b7eca89ad91fed70c352dce615e2f6c2e`  
		Last Modified: Wed, 22 Oct 2025 02:42:49 GMT  
		Size: 55.7 MB (55672486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ad68746866d9c28ce61bd82e9d8639ad90dd0cea3491a898c09515f441ab1f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220df07b16b2977b1083df128dec0592167d76474ed8173ac8db00ff7cbde8c4`

```dockerfile
```

-	Layers:
	-	`sha256:0a233c06fec0e354cad093d15650845f2ff19fd6e177ecd5245369bd1dfc3ba0`  
		Last Modified: Wed, 22 Oct 2025 06:14:06 GMT  
		Size: 2.3 MB (2300655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2382fc731b3cfce53b60b5ac65a42026bd4de7cb3682e5c8ee50624e99ff0060`  
		Last Modified: Wed, 22 Oct 2025 06:14:07 GMT  
		Size: 10.3 KB (10315 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:df8cd0185ed228ae6bc593b49584c10437dfd9112a27c664f59074e38784eeda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81944376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbbb6b9f5634f3bab6ae192d5f3702e818694dc4ef13dfbb7c74dd52761dbfb`
-	Default Command: `["bash"]`

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
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975204121ac36c84183ff5a33733cf95fd2af9cbfa8f2d225e69ce8773ac2e1f`  
		Last Modified: Wed, 22 Oct 2025 00:05:21 GMT  
		Size: 54.6 MB (54561269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b2afb304e8aa4768319c98772c1d73512726e98c1e6ebee174a046538d6d0623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88195a74375f3afc1e8ca16fbf945b7f972c6ed864b847031b1e374a642e7135`

```dockerfile
```

-	Layers:
	-	`sha256:51249b6fc27d857e5e07c453c34249fe5e66acba3eda14521fe67cacf7482725`  
		Last Modified: Wed, 22 Oct 2025 03:10:48 GMT  
		Size: 2.3 MB (2300372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b2a54c39a58d4d1063173fdcce039d47f664b0e40b3dbba07aac4819c9c09a4`  
		Last Modified: Wed, 22 Oct 2025 03:10:48 GMT  
		Size: 10.5 KB (10467 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0ce2b7ee59a4330f67941c6ac42415e5c249fbb5b11d0424009b6d042f1cf9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90736753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59047c7e68e72f4ae6a16d973d9ab61ab4c9e3addc70d822a926ee421e88868a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d841a0a60144b98f709a389854575d04c5a229584626add443f4c4b2c6c248db`  
		Last Modified: Wed, 22 Oct 2025 11:45:22 GMT  
		Size: 56.3 MB (56289964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:be5e72d2de5f5429f5b9ecff03c0a7c3d36ba2aa994c1eea8149699dca6662ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa776f13fd821b5b8521cbc04d1c835743ec7691118fd30ffb6a7423598df3e5`

```dockerfile
```

-	Layers:
	-	`sha256:78d8756e8e22174c3f39762afd0d3d2a98400aa78ffcecde9b957eca464bbf50`  
		Last Modified: Wed, 22 Oct 2025 15:10:51 GMT  
		Size: 2.3 MB (2298074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee79ba69f9132c07d054838dfc2d7e7e468e974be0a576c419dd5bb4596aa41`  
		Last Modified: Wed, 22 Oct 2025 15:10:52 GMT  
		Size: 10.4 KB (10383 bytes)  
		MIME: application/vnd.in-toto+json
