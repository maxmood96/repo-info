## `sapmachine:jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:8543e3d49e2b958a4e0bb5a1775cbde8a89461972226f9cd01ade3ed45e37f26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:17ef453e229bb2aa8759e5b96b2b1f559019f3048ee5c1d8d1bef5ca7e6825ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97776946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fe4a00ec0dfb0de0dec77f0d3b75f88c9fa877a8df98389fe400168c25a9b9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04656df36bc61cd010a7167a2eb29da4df8bb5f1b93d7fff8f1104136d62dca`  
		Last Modified: Wed, 09 Apr 2025 01:20:17 GMT  
		Size: 68.1 MB (68059294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ae3a91f1e16e7f898a1a661ee6176c4b2afc47bd8c334b1a758cf170bb12b2ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf9f5d510c364596ed799bc5b6ad99b06a29f90c91077ad45b21ee1217fc2de`

```dockerfile
```

-	Layers:
	-	`sha256:c2a06b7dcb2915f154af8909fa2b6d1c1c3305cb6fa1d848e8150e69990b8ccb`  
		Last Modified: Wed, 09 Apr 2025 01:20:16 GMT  
		Size: 2.4 MB (2393822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daef19f1b1960e36748c87d04ade6dcfbf295c2b829ba4af7c4185532beba142`  
		Last Modified: Wed, 09 Apr 2025 01:20:15 GMT  
		Size: 9.4 KB (9409 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d6bd86ce2c58ede9a193b7d9e1f0fc68e02608a014d06e2b0113b5e2b3634f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98202572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5c4fef9953627c4969cd024f107c531b9764a85aea9f3ecd4ce3a73794a93f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8ec2337e9df053b605df1dc92f6649212c2644797379367e54a159d7fff473`  
		Last Modified: Wed, 19 Mar 2025 20:34:44 GMT  
		Size: 69.3 MB (69308974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ebd72dca411d0b78b7d683d2f18a6a6e641705f1eefaf108ed3a3cb54d9394e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2406034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad6e91f3621f5ceb9b57778e49221c76d91d0d67b6c1245c2743f3b7d5535a`

```dockerfile
```

-	Layers:
	-	`sha256:d8fbadcff55c52b49c979149d846fc7bd317e55ab65b763c7461b598fea389bb`  
		Last Modified: Wed, 19 Mar 2025 20:34:42 GMT  
		Size: 2.4 MB (2396496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60108924554ee08863569db454e2cd68b2cb4cfe0eccbd0df5322abc98cc3048`  
		Last Modified: Wed, 19 Mar 2025 20:34:42 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b7e872596f8346ca4b9fb1dc3c4cc7f098ac678e26180066e7203350c3920b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103778959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fbffc6f11f97ea6530bc3130fdd42270925893a9baf98c9e82c20186dab0f3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2562a79b915122cc95f2995020196d88941e2b8a070e88830e86a9a03b0e7828`  
		Last Modified: Wed, 09 Apr 2025 06:35:51 GMT  
		Size: 69.4 MB (69438092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:477edf70ad3bdf1e347d7f0cfb3ea252dff8f679c4db2c82390c27ab29aee600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2406609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dcfbbd0b8d44f44e715932a9c9e59a74a9b28b1a3ad1f8784abe498c49a4b57`

```dockerfile
```

-	Layers:
	-	`sha256:4c35e42bfbe43afa5b2a271610fe9fc0f54fd8b9c62946766b863532431afa6f`  
		Last Modified: Wed, 09 Apr 2025 06:35:49 GMT  
		Size: 2.4 MB (2397143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868db7ea5b9b7afd9eebd20992d6a846273b7560d502ffdc39115af803cade17`  
		Last Modified: Wed, 09 Apr 2025 06:35:48 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.in-toto+json
