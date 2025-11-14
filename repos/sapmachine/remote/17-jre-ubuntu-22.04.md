## `sapmachine:17-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:c5cb25e8eb68de9bc7752588448512f6c8e18e61013c175cf89f738b780c1bc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:fee0123a9d9e0c452fab2397265d7d2016a2ee6d301ce0c186ede21137817eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83466882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53be64d5b910486b0c4a2880d80f521b6e0a563d753e5be1a00ada271db418b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:48 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:39:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e485d886039c34ec79b44cd1aaa709de4863c96ec7664353e03cd87765c751f6`  
		Last Modified: Thu, 13 Nov 2025 23:40:13 GMT  
		Size: 53.9 MB (53930084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:89c6d0fb8325bea1f6afb2e8bf6706fdd8df615f839fce528a21748cba66cb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5641435a886a890ce85be39993088cc55b4e6f0b5aa5ab4b85aacad8ab56fc`

```dockerfile
```

-	Layers:
	-	`sha256:73177c310b1abf7f5c2bfa54b1fb3841cc0aec62981301a570a11a4b33355a90`  
		Last Modified: Fri, 14 Nov 2025 01:07:52 GMT  
		Size: 2.5 MB (2543639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3e209cab154091a8554606d8e8edc24541189b4a65908883a0cd08ff3838456`  
		Last Modified: Fri, 14 Nov 2025 01:07:52 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5a2ad5503611d07ea370262342b34878fb46963bce8881044841b68a2aefe105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80695306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1bbf9d09be6018469de72dbd78d13a29b0c15ed76be2cc008c9ae1c1fdeee6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:01 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:39:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8862e5cc45926151d316079fc2a24ee63eb4ba4956f7159d5a088ae1f255acac`  
		Last Modified: Thu, 13 Nov 2025 23:39:25 GMT  
		Size: 53.3 MB (53311429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:07c097ab247a651aacd39d59d63888b4127620a3f125768c803db366353622fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7023ba6da0753b21745336d82c724a6440ea64836a7fc654d6a96ff9a4a36f02`

```dockerfile
```

-	Layers:
	-	`sha256:cd62eedac94d54e3cbe73b2814954ec5c390a9c9e35f459d0ad31dabea13002e`  
		Last Modified: Fri, 14 Nov 2025 01:07:56 GMT  
		Size: 2.5 MB (2543321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c5891d905c9ec0668919604d7229353e609df1620317b92c3894cbc2cef704`  
		Last Modified: Fri, 14 Nov 2025 01:07:57 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c7770e4a10e80f24f420a19bb1c81215e3ba627fc65799474985814b93c7f0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89473162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db04a6617ddaaa0492008f3fd2df3857e65c80e66d2c552e7a578d68dfab9a5`
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
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1d628a43b8625d15fbb71283a95137020432968ba815b93c98337110c6794b`  
		Last Modified: Wed, 22 Oct 2025 12:15:44 GMT  
		Size: 55.0 MB (55026373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d5be35d761a4bbe416249b85c1abc329124f71534a0cb389809ea60a7144bdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2550615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d8b2d87c04f60cdf6019c3da7e0419fa185086ca2c318f0c56496e9bf05cb4`

```dockerfile
```

-	Layers:
	-	`sha256:461aed4f7ed75da430a3989083c9076715d90415d7499345492442d5cd08a70f`  
		Last Modified: Wed, 22 Oct 2025 15:05:46 GMT  
		Size: 2.5 MB (2541754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:780e0207ce8fcb7c2e54dcf2521d8c1465ddde173a17d5def3a09ed340fa2fa2`  
		Last Modified: Wed, 22 Oct 2025 15:05:47 GMT  
		Size: 8.9 KB (8861 bytes)  
		MIME: application/vnd.in-toto+json
