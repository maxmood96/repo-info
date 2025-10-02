## `sapmachine:21-ubuntu`

```console
$ docker pull sapmachine@sha256:fd277853b66ebc4fa20bda85a38682864f1324b6ab69ea495809bd2a93d9c808
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:900e02961485516dba7219dd63e070e31a24fcbfcf0aa9b69f3756beb159982d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245033508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe13dc867c901c486f902f6720f04247c82d508f752f6d4d770cc8dc1e226767`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6799639fa354b664aecbb07809bc430f5056b1c0fff0e692ee257009b4a23d88`  
		Last Modified: Tue, 16 Sep 2025 00:09:46 GMT  
		Size: 215.3 MB (215310058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f3682fedeb0153affde2251bd83a81c66650ee38c61a4007bb0fb3a0d47887c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c168870bcfe582e95e26c2b40ca563c9cb7e7b1c06f69b5a8fcfd6a570df91`

```dockerfile
```

-	Layers:
	-	`sha256:99375e0b76fe63b63627bce055e8d139885c3970d8ea3c5b03d3807e86b6dd16`  
		Last Modified: Tue, 16 Sep 2025 00:07:53 GMT  
		Size: 2.6 MB (2606957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4481445e609afec74a8af253fd4025dee72f99a495dffaf97a4dbff48bb1e455`  
		Last Modified: Tue, 16 Sep 2025 00:07:54 GMT  
		Size: 14.9 KB (14885 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:742ac822e709b115ef9535540da53a5af2cdabdb2bf7814233d9ec1da7fea585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244619471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23f1364679605fe1db79dbeb8214b5bcd186d51b85eda80cfbb136587af4d42`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc9faf4868e9920ce98d40927748b362fc49c0c99ce58437b5518cd47d9b741`  
		Last Modified: Thu, 02 Oct 2025 03:34:12 GMT  
		Size: 215.8 MB (215757896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8b56e4bfedf04f20b468dfce07a8fce23e302b354d7ec78ace15ff55579d11b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba05b91cdd58e2a8e14bdfb35403c9307fba635b08cb918c6afc16e644dd076`

```dockerfile
```

-	Layers:
	-	`sha256:351d6338476c176ac502290fe16e3de75b3847915c8c7da6d2605ba5d8aae250`  
		Last Modified: Thu, 02 Oct 2025 03:07:21 GMT  
		Size: 2.6 MB (2605313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0259bfaa9bc6078acaa1dfbdff44ef12833dd78333216b6ae98604e312f8225`  
		Last Modified: Thu, 02 Oct 2025 03:07:21 GMT  
		Size: 12.9 KB (12877 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:893c8605dda04015597203858d122c1fc40d671cd27a58e5730c44191c9a62fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250567039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33c0e3a9790b0855e907c078b6e67be12df1c8a0d3e4e84557648bc5c75f2a4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8762d0ccb69e8d6b499a8247236461d8f2f34e774fc7e07367b98febaf8085`  
		Last Modified: Tue, 16 Sep 2025 15:19:17 GMT  
		Size: 216.3 MB (216263912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a9e945f7aa7e0ca1b2ee8b06cc76bc12d917cf7458cb94dbbda089fb23208298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd9073f25017c987a10f18c3330266caee68d35d4ce26cdb6152d597a564c69`

```dockerfile
```

-	Layers:
	-	`sha256:7640c4f409d7d4f32846c44d6e71f6f0c76c17e080f738e1e2025cf5802078a0`  
		Last Modified: Tue, 16 Sep 2025 00:13:27 GMT  
		Size: 2.6 MB (2603182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:591e5d0e31dd669263e0c4be7cb778fd1cc5dc661f40c7320b1b2822088ccdf3`  
		Last Modified: Tue, 16 Sep 2025 00:13:28 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json
