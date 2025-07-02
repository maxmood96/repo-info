## `sapmachine:lts-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:76f62b2aa0ddb9699f318703760cf9ac359170dc36d75dc06e801ba9f8d3c28f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:7122e2a34b451468556b291e6357ea676bd859441b00ec3cc935e424a02a09a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89831170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496c65439f9cc3fa8a003f271445068828d3a2d2c238b2a74b4eb57237ebbca8`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ff75649e538ef19adac04d3b78a77f907d81d430829674d530e621399b1e1d`  
		Last Modified: Wed, 02 Jul 2025 06:11:46 GMT  
		Size: 60.1 MB (60112804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a1bcb33db45ced9bb1cb49e9f8e764bb771d32db5ec970290ca802e9e4dc51cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39a34dc6ac305bc041d3ff6a2f51b1dbb02b0c56f10b2f0e730d7344d3ae543`

```dockerfile
```

-	Layers:
	-	`sha256:5355f777a85ba01a113ca4b6c4046c9e85da8e146d88a2e4056d9fe665d0bd14`  
		Last Modified: Wed, 02 Jul 2025 06:08:09 GMT  
		Size: 2.5 MB (2518988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b69cbc020d910bb0ba78addb67ba0acadb470d37e1aecd493746189ac224c111`  
		Last Modified: Wed, 02 Jul 2025 06:08:10 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1bf6f34e8b038027263dbd6b3db07bf196a1cbb86a5dcd38860cd55b50308d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88165532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b0e56b8a41b5b419c635989cb5422d3b99d92e1951d82d38144a9d0869673e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdc7b7f442e3dfb2eae3902b56568f899a81b2a0a8193eb97110fc5e2206f86`  
		Last Modified: Wed, 02 Jul 2025 06:40:09 GMT  
		Size: 59.3 MB (59309514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:24314e3bf4abbe19ce509ce15f4df5f5cf71df5e7c71b6dcd95164866e5137f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d933b9e3f2bb716262ac84f7ba508f8717db6656c814e36059796d25166541a`

```dockerfile
```

-	Layers:
	-	`sha256:311449b8bbc0b237b6b8e512d17ce7c05560ac59c4fa1a02f253fddd4a58c2ae`  
		Last Modified: Wed, 02 Jul 2025 09:07:03 GMT  
		Size: 2.5 MB (2519516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27b6153bdd50b5f123f2c8502b68eb65878cf78f1bafdeb7a0afb66a3f56e72e`  
		Last Modified: Wed, 02 Jul 2025 09:07:04 GMT  
		Size: 10.6 KB (10614 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7e8c9301cdac957143be833b77cf6427d0303115eca39b4605a5ef5751f85ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96125494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814a167925b3381b6cee7978dcc13920d8e869f64da061165322fb09492a1d30`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e188163da45d0ad91a3cc5356a64cf5ddef93bf2d99a415ea9c67d004bc2903`  
		Last Modified: Wed, 02 Jul 2025 04:50:30 GMT  
		Size: 61.8 MB (61803988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08bdb893aa97d2def1727d8de50b5fa11b17ce018a3f6ba2c30246f1ed9fea2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080a38efb397e30003029c47f2fd2468b9a0a49093c13f164778125e82d52495`

```dockerfile
```

-	Layers:
	-	`sha256:3e930e3726943efdde0f0f6ab6a6d904c9464efd44a191c5c36459fd81eae0a4`  
		Last Modified: Wed, 02 Jul 2025 06:08:19 GMT  
		Size: 2.5 MB (2523091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8310318358097eaee6c426a715ea5378912fe7b4d886892c4227c7774bb24374`  
		Last Modified: Wed, 02 Jul 2025 06:08:19 GMT  
		Size: 10.5 KB (10524 bytes)  
		MIME: application/vnd.in-toto+json
