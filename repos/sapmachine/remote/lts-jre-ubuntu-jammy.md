## `sapmachine:lts-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:f28fd999710d500be550644d97a81dc87fbb9ab2f2eb119033be74ec0f70e22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-jammy` - linux; amd64

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

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:lts-jre-ubuntu-jammy` - linux; arm64 variant v8

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

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:lts-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f92a9535c4a006083ce5a93efcabde9eb82f41ee69bb16be99ebdd34e3d493b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92134675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aac7bbd66d80d137092534c10c425a347e61c7230c31b6fadde49d513b1c914`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:dba7280e60062995b692f9b14413851fc98f3b15383ff3fa9b5ccbbc4e99c446`  
		Last Modified: Wed, 22 Oct 2025 11:43:37 GMT  
		Size: 57.7 MB (57687886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:872a961ff7a0fe5ccc357acd402b612a38f277cd0664e2201007ab74cbe89662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d215bca22613e9add62b36d419f981a6e8f97cd59ebd22ac33dc24d998ce2366`

```dockerfile
```

-	Layers:
	-	`sha256:712543c79bc611d632055c791e5a680be98d8f79baa9669b1849ed12d2c1b1ec`  
		Last Modified: Wed, 22 Oct 2025 15:11:06 GMT  
		Size: 2.5 MB (2548854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c4be048c311708bc30d29a320dcb9f6492dc5a4c53e7e2325c6748ca4af533`  
		Last Modified: Wed, 22 Oct 2025 15:11:07 GMT  
		Size: 10.2 KB (10199 bytes)  
		MIME: application/vnd.in-toto+json
