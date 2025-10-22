## `sapmachine:jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:c1ccbe9bcc11a5fd03e4a090173ecbce5bb17847045897bb7239e8916d8d26cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:5a72766f9b923805d8af687eee9c35223cb743e5bf6116faf0fc229b3fb440a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86428325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a387fe78276820931cd2b15b070eadae95ecef75d073545203dc73d4c6a958`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b7fa7cabd185a5d420b34c4042a1aa806c1c99a42988075900a5b6d1b72807a2`  
		Last Modified: Wed, 22 Oct 2025 02:42:40 GMT  
		Size: 56.9 MB (56891507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:19154fc390afab484c9c392007ca3a4a58ea9c3af9df3c7841b58524af0fd180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ad8c59ba344d9a6c7cb25562007a80f8d25351de3f7c23498d6f308cb2e699`

```dockerfile
```

-	Layers:
	-	`sha256:7d9acc0feb1e54a5ef607f539c895fb4e7bb5ad4e9ba6662a6d3516e4d2c6d49`  
		Last Modified: Wed, 22 Oct 2025 06:14:20 GMT  
		Size: 2.6 MB (2551345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f6ede0a4d937a0d874d564a287c8c09745e337550c2a675df38b0249aae9e04`  
		Last Modified: Wed, 22 Oct 2025 06:14:21 GMT  
		Size: 10.1 KB (10132 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:68cbbb462a538a5edfa421f0beb9d85b56a2579ef6a50ba24d70ddc99f6e7366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83162296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d1c9ff8283e0c9c67b30f55672376349b3515ca316776125a96f15d31b026d`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:bce7afdca40d5ed7e319d5c11e3c06ee3f315731d54fbf6bd47ae65d8a12daf2`  
		Last Modified: Wed, 22 Oct 2025 00:05:22 GMT  
		Size: 55.8 MB (55779189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fb5c72a7a3a80ebce4af4dc3571de46a9e31018edd9a6d486fba6c44877da6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa534b8d2ed17340fea78747aa53c54e7049a4ece4c990044d0d0a9af8e0dbef`

```dockerfile
```

-	Layers:
	-	`sha256:70cf910e9f1f89dc5b4b4e603e786f0df203258c285d148f769487df059e146b`  
		Last Modified: Wed, 22 Oct 2025 03:11:01 GMT  
		Size: 2.6 MB (2551072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8060f1715a739594204b04be0eb28603f8f47fa0c9d759fbc72c05d7a853324b`  
		Last Modified: Wed, 22 Oct 2025 03:11:02 GMT  
		Size: 10.3 KB (10284 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d92dc1f0ab14c864cad2ee07ebb325f05c4dc2eb89a350d95d70df219fa776f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103870567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d25149ab4c97d6046ef677a6070be35df8835bd9f309200b02120b37ce99b1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350a0f8fe2228e0044300258ad9eb05679192e4c68f047a012c7ac697d33007d`  
		Last Modified: Thu, 02 Oct 2025 04:24:03 GMT  
		Size: 69.4 MB (69423778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0a4bf334cf5f67187eb0ac25a55152849d308c8f49bdcf71e99df2237320d8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaec115530cfdc5a5fa4fe843711efa76130a75919171e539977c7fd19129832`

```dockerfile
```

-	Layers:
	-	`sha256:3551a8b8e4eb729d51408178157cee22959e884a0eb7e28929d09ce7ab363271`  
		Last Modified: Thu, 02 Oct 2025 06:11:36 GMT  
		Size: 2.6 MB (2550068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edbe0e3efdddef399b800090a741b6ae51502b4adaf6f58e1691518d928c07a5`  
		Last Modified: Thu, 02 Oct 2025 06:11:37 GMT  
		Size: 9.5 KB (9496 bytes)  
		MIME: application/vnd.in-toto+json
