## `sapmachine:jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:556ceea6d12f6a22225451c16fdab9c9a4b3d46421be8e6c02cac68491e007e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:d945161609ef4c05e5d9200db4ac1de387de10c40fb2d8009f50546e24769cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97506212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbffb308dd94b1652ad845afe3c17bcd70dc63233f3386626555a79e236f38af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84285e41cfb74fd9deeee12c69035bda2e1d1027c6d4caafbbc1bb3ff71b73ea`  
		Last Modified: Thu, 09 Oct 2025 22:15:53 GMT  
		Size: 67.8 MB (67783065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6b89afa2a0bd41f40352f855fb13f4c73462192811c0785865daeb79c0528510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9975338505e3db27f1f85b2e09294ed681a7e2f0a6d522c7fbbc3a0677922698`

```dockerfile
```

-	Layers:
	-	`sha256:a8c93ea54b7a82a1bedda233ddb61f5914e03ad3fa09b410c37c108a061632e8`  
		Last Modified: Fri, 10 Oct 2025 00:18:13 GMT  
		Size: 2.3 MB (2280858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c43796cc9e45b559354388d1dc7bec1e90dd91e65a03197a801322259bda5d82`  
		Last Modified: Fri, 10 Oct 2025 00:18:15 GMT  
		Size: 11.2 KB (11238 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3fb72d14c1c45726e8dcf738b762d00f93c7ed932a8e625a0917b08bc22b0772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95627363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda6b5e8a3f597dab27fc0f17897c4bc58b8480082f2b34dcc79f91257d7e29e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51469613aa4be124151aa5f4d3fe7e9ab530085d703af137c2ca827bdf1c3fd`  
		Last Modified: Thu, 09 Oct 2025 21:28:07 GMT  
		Size: 66.8 MB (66765651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b8b5a27c42338f75af31e75b1b35e70c0d26ed252cd5ef2ac852ed1ef94daf4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09834cd1f9a87d5b0bd9305de5f471a70a07b0278068df837f6b2fe13b0efa60`

```dockerfile
```

-	Layers:
	-	`sha256:ce0bfe289c3ea73e484260dc35fe12b454aca7c5f0b8bc52d99353eee741ad8a`  
		Last Modified: Fri, 10 Oct 2025 00:18:19 GMT  
		Size: 2.3 MB (2281398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed9d8edefc0da275f478544d2cf1bfb9a53401657a51f847189f0f31a9d0227`  
		Last Modified: Fri, 10 Oct 2025 00:18:21 GMT  
		Size: 11.4 KB (11427 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:063323c8cfe84ca7c16cfb5314c909552032f198e7ec333d11740e3b6c573b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102834665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dc71ae58cc63e156db335502817eaeed9f3413895398f8044ae67cd9a8a5de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefc2053144a0fd967d60f103a089596bd835b86335538a0b180524ad6cf7fac`  
		Last Modified: Thu, 09 Oct 2025 22:41:08 GMT  
		Size: 68.5 MB (68531140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1db0337a30d18d2b7f2af58301238a2b2b4b55e4c105732ee354c37110aa0f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212479004a91f8725a1e0eec9807ac771f7e50c7528c3998deb841a95abe4651`

```dockerfile
```

-	Layers:
	-	`sha256:4dbab6e66338d8ea8c6c258bedba64e467d2b465ff53d532a4faa8e42fab562a`  
		Last Modified: Fri, 10 Oct 2025 00:19:23 GMT  
		Size: 2.3 MB (2278246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f7357a00cf48a1eaa4dcfa40b92fc724faac29f5bc6e0683d312bea7be1778`  
		Last Modified: Fri, 10 Oct 2025 00:19:32 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json
