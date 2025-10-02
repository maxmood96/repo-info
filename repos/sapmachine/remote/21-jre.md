## `sapmachine:21-jre`

```console
$ docker pull sapmachine@sha256:4a97917027cbfac1ba2aa167d4192beb5ebdebb8714b844a6fa56b67bcb6794b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:5552c3c99d2ed4c7177a8902d50b074593850c6c6c6a02c29ee79713e344efe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89927303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b96ca8ad26a7ab7cc928fb0946d61f9ff9e804f9499c65f78c71ab544e712f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b82cb0d2fb867482353d73d4279524dbca69857d6829c6d254411319c88ae4`  
		Last Modified: Wed, 17 Sep 2025 17:38:50 GMT  
		Size: 60.2 MB (60203853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a125eab1127131c8d311ca44a143d7f592ff72c7316ffd20ab0f753c2987fdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3fc1a54eb1a4040158e075daa7f64d4d4587a501a1277e21a6ce98201281d4`

```dockerfile
```

-	Layers:
	-	`sha256:cc99d0db1ab0d025f67a311d5d466138708a72ae58b86376ba680aa4af2d001e`  
		Last Modified: Wed, 17 Sep 2025 21:08:11 GMT  
		Size: 2.5 MB (2518632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a728ec5a0f45bcfee21bb8a576aea22b9d63031356e433cc43a8a878774d399`  
		Last Modified: Wed, 17 Sep 2025 21:08:12 GMT  
		Size: 10.1 KB (10080 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e568ac4f72d53ec6a09a723c8236753740497b10104c5d78762f16dc7151b256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90471263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78da114991ec5bc92e5a001fff307c34cdb70b74b1d899a626f2270bd7c08c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b406a6532f571357eec77cfd1847b4513eafe91cd4a4eee6fcf7d16c5446f0`  
		Last Modified: Thu, 02 Oct 2025 01:34:19 GMT  
		Size: 61.6 MB (61609688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8d91ef2067f5f9a280f9aaf788b74f5d32d780d690be4b6288d4149f77d4da81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff8458e9c21dd3c9cfa9a3a82911204d54615d6735c33836b71d75a7b65bc45`

```dockerfile
```

-	Layers:
	-	`sha256:eab06de3ee60d4f97683ddc101cb1ca6f8d8ad0054d82d5c6fe853569f0c41ba`  
		Last Modified: Thu, 02 Oct 2025 03:08:09 GMT  
		Size: 2.5 MB (2519148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ddcb856c4fe97e7b04a597c84c08981bf0ade7ad99e92193e7929d16c88d8d`  
		Last Modified: Thu, 02 Oct 2025 03:08:10 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:586f2901fb2f88b3d45048eb17cf53202d63f49b7e6533ca407b986a8313332a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95739357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3f9da67f4b49acbb10486b25f9f7b7a44ed0e8ecdc614a075e22744ce872d1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556b947fa14dcb9f7bf6312cd045ff47a54ebe9f3f09086de61282535755b27e`  
		Last Modified: Mon, 15 Sep 2025 23:44:36 GMT  
		Size: 61.4 MB (61436230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:56e6d7d83e0b8ded8a20dea65bc0fce871d963d297d7cacd5910caada903a236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2526861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b586eee0362275c2464828865eaac40a3d918826f17881d54cacb0c42550ce81`

```dockerfile
```

-	Layers:
	-	`sha256:9040b7bdaef3754a5dbc20ef7c6d6a4a18c9a4ff02f0915c2eeed8a74a32ca5f`  
		Last Modified: Wed, 17 Sep 2025 21:08:21 GMT  
		Size: 2.5 MB (2516713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7206ac13e6311a92a38ef84b3e0ad6f2f00dca2bf5aba21fd40a0c2bfeff39d0`  
		Last Modified: Wed, 17 Sep 2025 21:08:22 GMT  
		Size: 10.1 KB (10148 bytes)  
		MIME: application/vnd.in-toto+json
