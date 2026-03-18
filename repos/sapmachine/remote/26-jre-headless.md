## `sapmachine:26-jre-headless`

```console
$ docker pull sapmachine@sha256:e91419cfcf87ff2ae511f1862380357968577042f11fb3307c10fe1d3c918fc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:1137182220ec16130c8c157fa215e5d001af83d4163e3e3ba0946acb65e231ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87536438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48154211435f5681f692f68e82fc3d5ee45fab81110df88afe2134e02e4c5466`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:54:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:54:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:54:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6bb6f9dc78f8c40ea75caba907e941f1228dea2ba16fe9b1e7ed9d581669ba`  
		Last Modified: Wed, 18 Mar 2026 17:54:28 GMT  
		Size: 57.8 MB (57804445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e88f5a9e2dadafd792846e8e20b1176255a43da3c8f6fc6ec6d41aa91a15ce5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bba0a2752bb8a6d077b450869ebebb4f81ea612cfcc9cd9ee40df5aab330da3`

```dockerfile
```

-	Layers:
	-	`sha256:c6ef085213508f4712ada2a2d2f3f565033c01fc5c27d8b4644718760f3e6596`  
		Last Modified: Wed, 18 Mar 2026 17:54:27 GMT  
		Size: 2.3 MB (2279044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4219a79923455895652613743b1a6c667769379f689649e0cd6a6d9748390708`  
		Last Modified: Wed, 18 Mar 2026 17:54:26 GMT  
		Size: 10.2 KB (10152 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:865a6dcd28f7326eab6ca503580cc6a7f9f95dcfd1212c76f4f4e18eeffd395a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85679091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26764cd4cdf3cfeaf94f9f8248e43a60ff9dd0e8251e4279defa58ee279323a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:48:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:48:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:48:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c80f33ee794c224d1b6f9cee80e3390d59ef6c37c2bbad571078dd64673f847`  
		Last Modified: Wed, 18 Mar 2026 17:48:49 GMT  
		Size: 56.8 MB (56809382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4cc450a6956584a7106c43662f498488bd871daab394d97e403093b57b41e52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c262a5caa6a0b6b7383456b7f3199ee11f2f27053ae3fad1a02dad9c6b1a198d`

```dockerfile
```

-	Layers:
	-	`sha256:c4955fc39a9649ebf8ed762e939d60fe8fce9a73d00bc2dcea319d0f98480a07`  
		Last Modified: Wed, 18 Mar 2026 17:48:48 GMT  
		Size: 2.3 MB (2279548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9676715128afb75932335d2161a0ee64aed92a6d2a2df25a3aa1b1000722773b`  
		Last Modified: Wed, 18 Mar 2026 17:48:48 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:246a28da728af7665cddc3b54b025586fe7e5a28a7bfcbade67adb79dc4652ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93089338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183d7cef088904ab27710c005ae25acd51efdd2be4d2d9db7f63aa101fd3194`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:48:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:48:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:48:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0235af8ff44edd3e0f4c7bdeeab02a82b82436b6853e98ce10e7a43742c8d7`  
		Last Modified: Wed, 18 Mar 2026 17:49:05 GMT  
		Size: 58.8 MB (58779287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:44409f0b3e57c24189881c32c8ab13923c2a6a2641329d8701fa9f3dfd320389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b80bf8bdd97ea801e8e668d79008fb6290db73b65fafcd9ffc5bdffaec5516`

```dockerfile
```

-	Layers:
	-	`sha256:450e03d23d040914a06617df565b631e3534d3b2c19dd7931b2d14cb3e230e1f`  
		Last Modified: Wed, 18 Mar 2026 17:49:04 GMT  
		Size: 2.3 MB (2277831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45a05d4958e71898f0745a192249ba5b386a8b173f2026d639428d7b92ee19b2`  
		Last Modified: Wed, 18 Mar 2026 17:49:04 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json
