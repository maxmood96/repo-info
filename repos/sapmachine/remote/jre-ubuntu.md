## `sapmachine:jre-ubuntu`

```console
$ docker pull sapmachine@sha256:b1fc422dc0a2557afd0364807a9b4feb13d69853b8c065f463df0cea8cd34109
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:cddd18f8784ebddf188bc161c37a04f8527566fc1e4f48c24a5aa8b6b9f9473b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89498798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c726139c5922710eb969caa0405a82527fe4d72c1c4a7eee6e603bac99de7c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f37912b94568f94ffb7b3e198e7b9166513b057924df4d348c8b6a84d011278`  
		Last Modified: Sat, 12 Oct 2024 00:01:07 GMT  
		Size: 59.7 MB (59748341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2be70187c36a500586ab9e173ce063888876825322ce0606fe21527ab14b3b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68904f50d5a8d2dcd258c569cb53224462d06c518990b7df098fe1cb14f3457d`

```dockerfile
```

-	Layers:
	-	`sha256:f2c9f5f7d6011b407aeda032b84f2d0e66bb11f427f4c1f0ac37aafeeb3afd41`  
		Last Modified: Sat, 12 Oct 2024 00:01:07 GMT  
		Size: 2.4 MB (2366526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4ac2e1f5ccf719128fed1a833b52972586dde92cb9d69df3bc00b82fb74efc`  
		Last Modified: Sat, 12 Oct 2024 00:01:07 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3ea687b1658120e81d830bc728a8a949d19f9f3f276c731b118963894821502e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87695838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def12cb1c78d87992311cf8549a56b4cc5c4d457800dab8461dcd5753ce0d07c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27ae060de6f2d64ac28d67d21a25a30c24b3ba609f3bad638f988f88f70c9ae`  
		Last Modified: Sat, 12 Oct 2024 02:20:55 GMT  
		Size: 58.8 MB (58810222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c749016dc079f50675737012713ed66a3ca305ef5a22edb6addc8c431b0f6d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c57c1160d0c0ab88ade88dcf6f755f4b48f5ae87bac3d8625d9f9df8536daf4`

```dockerfile
```

-	Layers:
	-	`sha256:a81390cc1c96b5cdb5edb613f5f03164eca3f0cb301a3ac9622f9d3d645273a1`  
		Last Modified: Sat, 12 Oct 2024 02:20:54 GMT  
		Size: 2.4 MB (2366386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed77efaf4f2bee02e7d5a70b4db042a6a5646c139455f172a404c7a9fc04550d`  
		Last Modified: Sat, 12 Oct 2024 02:20:53 GMT  
		Size: 9.3 KB (9316 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9980edc8b0952ec27ea46352e7380d1f552d6f465a54942436edaee1df52b431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95675418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29be394062d9dd8424f4bb3fc60cb553a397f3834ccb7ca2e262bcf8247ee9b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9b33cda72760ec5694f9cfbceee0a68ad188cda7f5cc4a52ead2ee9416dfb2`  
		Last Modified: Wed, 16 Oct 2024 02:36:24 GMT  
		Size: 61.3 MB (61286449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e0157e4fc0b7b4e899c4197d2067b937da4f1cb6bc7da3136f79ce3b3254902f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d221fd7170eae007aec42e66316bef6eac700cd4cb17ea6369e7f82101e789`

```dockerfile
```

-	Layers:
	-	`sha256:74c17eea20576b649be04c6e08bfb23831da7cee18f71f198c2672073b8ede28`  
		Last Modified: Wed, 16 Oct 2024 02:36:22 GMT  
		Size: 2.4 MB (2369844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3cc096d59443095712496e1849247dbdd64aac9736fe7aa46cb29d2d16c4a3e`  
		Last Modified: Wed, 16 Oct 2024 02:36:22 GMT  
		Size: 9.2 KB (9244 bytes)  
		MIME: application/vnd.in-toto+json
