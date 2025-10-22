## `sapmachine:17-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:3fa22802d3ded4b412d2d2b978ddd9371c9c449bfd16abb37d3698d088ddc7aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:e021b5d1b1f2653a9fe1f4dfff1d69f141e6af54062eff07b754db65ba09bbb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83978721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6dfcd5bdc00943fcd3828ab3dff995f8064f5087dcb6c5cd08d0c1de40220e9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a3bf9e4e705ddd07a94762f38f7ff683c2ce4c2f26a4b27b6d0f87dc9cdcaf`  
		Last Modified: Thu, 09 Oct 2025 21:28:08 GMT  
		Size: 54.3 MB (54255574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ccb00f9b45615bfcecce6f85dd3359acc71f671f77e6e8f7ae74b0d1f6211cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2527475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecf88b6296cbd9831ff82a6d05a485bf2db64a27c5822d39d72af5f747a7b3b`

```dockerfile
```

-	Layers:
	-	`sha256:3197930f4329775342c7035ee3965cbf2471e7acc9f0679f9c2a2a27cf84f774`  
		Last Modified: Fri, 10 Oct 2025 00:06:54 GMT  
		Size: 2.5 MB (2517386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06f49f099f9d308956de1a85bcef1f6c31c8ffae5147ac9d2c83ba54ceb99f18`  
		Last Modified: Fri, 10 Oct 2025 00:06:55 GMT  
		Size: 10.1 KB (10089 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ac6688a5722734dad837bab807ae435815f8adbd8d334f11b0602e8e62b4fd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82613915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba0b899166773f77fcdda7bbd21682f45ee6b409962e13042b15876fb9002c9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d959f781f10824b759c75f1511117016240a20421a092e598becba437b62dfcd`  
		Last Modified: Wed, 22 Oct 2025 00:06:32 GMT  
		Size: 53.8 MB (53752203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5afc66ccabb2e88f04906a4fdfc77dffda9e14c5f724fcef5b7df0f4e06c405b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f896d435de878c311b4e3c26e285ca0edacb041cae0e1851bebd1757f3cc1d99`

```dockerfile
```

-	Layers:
	-	`sha256:837c159fdf8cebab06d643976010f065ee191bd902fe220c20d951632918474f`  
		Last Modified: Wed, 22 Oct 2025 03:05:16 GMT  
		Size: 2.5 MB (2517902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263ba7dc08cee7e491e1af893f9e0355673f43a32806395c9b0a226b7a93eb07`  
		Last Modified: Wed, 22 Oct 2025 03:05:17 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b239051806b83d8e1ac766447e08a88919653706b8b49fa55c8169bb1f44189c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89750965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c55e72934433191e201be757beaa16ca716fdcc238c2fe595c36c557d4a6d55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa009a9c92d7be50cde16d6b6f3455afdc406b1f4449f2efa660c114a94bda1a`  
		Last Modified: Thu, 09 Oct 2025 22:55:06 GMT  
		Size: 55.4 MB (55447440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:69905a6d534deb02508cbbbf3d6925545bebc6854d45a8458eef8374dd6b30f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2525624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8832f79b1f25821fe88fee7f47b4c8e7be8b914441b579fee0b4f738103c60`

```dockerfile
```

-	Layers:
	-	`sha256:916aadb5a4e2820c727fd8cf9537ece97eeadd8677ae5df53b67a7babd573868`  
		Last Modified: Fri, 10 Oct 2025 00:07:57 GMT  
		Size: 2.5 MB (2515467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b72556f9c8fe16c73b7e12ea1772ab4f769a42b9724b2a6b31244b5fd5b20fd`  
		Last Modified: Fri, 10 Oct 2025 00:07:58 GMT  
		Size: 10.2 KB (10157 bytes)  
		MIME: application/vnd.in-toto+json
