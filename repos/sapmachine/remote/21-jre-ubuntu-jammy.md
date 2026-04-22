## `sapmachine:21-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:70a07268cc20121bfc98201d109d50108fe4ad64f0fa0741657a327ca1c5e354
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:cb6aca1f95193ac4a71b78551a275863cc2c86063cb4d44eb2879b0c7753d0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90186048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dff2b3f607fc3e3a165490655bc6c7dfc0a55eb38885bc2b1e188e58af40a8`
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
# Tue, 21 Apr 2026 23:04:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:04:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be81f59a67497229373e2b96ea5785033df05b45764bf7a31e50a717cb8dfa6`  
		Last Modified: Tue, 21 Apr 2026 23:04:54 GMT  
		Size: 60.4 MB (60449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9d596734e86fe09f8f8c0c9d475b82281e041b42f7e47290daed853720a6866d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e4107dde4f3b8de3e55dab53bd1d08df6f47d0e7e56fa49ef5d7f04158f9b3`

```dockerfile
```

-	Layers:
	-	`sha256:49ec85f5b6199135611f0ba0b76980d3bae319900b921d372e66874de75cfa73`  
		Last Modified: Tue, 21 Apr 2026 23:04:52 GMT  
		Size: 2.5 MB (2547919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab5e5cbeeaba65ff27b9efab48a03f428083edd51de20923116404a9e65b45a8`  
		Last Modified: Tue, 21 Apr 2026 23:04:52 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b5d29f6a923c7ae205aba58080fc436940650ac716de7675c6a4a9404691a196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87210943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ae7b80c3e35ccadeaf9eb4e7db2b7d7f3623cb89be94ae8c4266a3198fcc57`
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
# Tue, 21 Apr 2026 23:06:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:06:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:06:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a35553d729bbe73b0e2f903f3301346f014402daf18530079c0d1722fe21583`  
		Last Modified: Tue, 21 Apr 2026 23:06:46 GMT  
		Size: 59.6 MB (59604400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:27c0b9bf977afb53807bb9c7900fac4a9441c436d25bfb273fef94a1a83d8087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d035e61201e7c909476d52b2f3d078796c09b18388628b8cb7db765778a55e1`

```dockerfile
```

-	Layers:
	-	`sha256:778de1f3e1cbfac5199c0ad67b19cd1d6ac4b69b8e81d9027b951a3801307938`  
		Last Modified: Tue, 21 Apr 2026 23:06:44 GMT  
		Size: 2.5 MB (2547601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fb8b653fd10bf624db22f699cd323ca6b32ac1e783acde2396b5163d9b9ac5`  
		Last Modified: Tue, 21 Apr 2026 23:06:44 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1df887e96365fc6e8a496b68aec4a74984e46e1710e0ec0375b13c0424dcd481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96331425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843b1760fb6a3920d7cd6e57b01587a35e3f2914b68e24fecbad15e7f977ba06`
-	Default Command: `["bash"]`

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
# Tue, 21 Apr 2026 23:28:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:28:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:28:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501c242fb38b6f763e597c8ab645fd8923425312f5e1e75d458904c2c27767e`  
		Last Modified: Tue, 21 Apr 2026 23:29:02 GMT  
		Size: 61.7 MB (61683027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:40bfd3f9e69204097820257fecd15fd31d15c060488cbc8473a5feee12d2e4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05309a1779b1ae120d40540342efb1856dd036795ff35d8a5684bb6bfbf26554`

```dockerfile
```

-	Layers:
	-	`sha256:e94701eb23c897d77818a587c1ad64e78939daa34d04fbb92d1105c590074077`  
		Last Modified: Tue, 21 Apr 2026 23:28:58 GMT  
		Size: 2.5 MB (2547451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccb0a9927fa360a906defa95f936fdfde9f203f1cec6c2f4da949942a2b5619`  
		Last Modified: Tue, 21 Apr 2026 23:28:57 GMT  
		Size: 8.8 KB (8818 bytes)  
		MIME: application/vnd.in-toto+json
