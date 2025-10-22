## `sapmachine:25-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:dbe03e7d189fe90ba200345125455e073c89e2f2c13917653a1e982ab1a17dfb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:81feb706ffd07fb3845f8233fef0fc5c476df4f5d9323193ba41f190e83d3dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98698739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c5e733c0a79610754fc2267da8f5209cebcc5dd708587840dd20d599244075`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d3733145f9ff3c17db13cd2bd027734143a2e78498ac08764c6d5016b21c7879`  
		Last Modified: Thu, 09 Oct 2025 22:33:47 GMT  
		Size: 69.0 MB (68975592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:142796df756e18aa93b86bf616691257130a4b333b89dd517e7d4ab5c7b7d7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a7ee7ef59e8d0de8385bf00a9e5397c0afadb20732349f6b8523b3588d9adb`

```dockerfile
```

-	Layers:
	-	`sha256:7a1bd79c00dfc1702b89205352ce71f49af9729d44c682769fb5eaef19075d99`  
		Last Modified: Fri, 10 Oct 2025 00:18:05 GMT  
		Size: 2.5 MB (2526608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d269cfd6db3d0f42f9007fe88a0d725f4c8c1727f39dddd14e675478cec2b4f`  
		Last Modified: Fri, 10 Oct 2025 00:18:07 GMT  
		Size: 11.0 KB (11002 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d787ec08d9ceec83808534847832f1fc386c57f8032a02113a8188ed639fb6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85079637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84b920899dd4e8bf1bb4337cdd3221a26ef4b503a434945e08be2a3b5b3a22d`
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
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12a5b2a136a47b3f1fb8883cd998f54e85f2be5b6d9df27ec41dd3d3527c195`  
		Last Modified: Wed, 22 Oct 2025 00:05:21 GMT  
		Size: 56.2 MB (56217925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c5f41c34a7585de8a4fbf7fc3fc0d7d83ada73b892b3f3945d6d21a32c1aef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b4b9177657485f1004f7d85fa46dfd309162a8f79da5e8dff859ebdd5804df`

```dockerfile
```

-	Layers:
	-	`sha256:a346c4db452331d3511ab53d841814a01bbeb346a01faa0960c33f8bfe587708`  
		Last Modified: Wed, 22 Oct 2025 03:10:23 GMT  
		Size: 2.5 MB (2526621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e6e99acaf92f7fb5293c141c46de3eedbffeb15ab694e36f872ab66bfc4e74`  
		Last Modified: Wed, 22 Oct 2025 03:10:24 GMT  
		Size: 12.6 KB (12572 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:eb2430dcd8675844d015603634a13678eaee397878196c54f1917eaaadc281ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104219798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2422d3e62055dbfa09d90d25e1ffcf18008c10fd19f36a16774fa7341b772c02`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:e78788a06745032ac8237f49302a3290522f6e4e2630bea5c04a35790fd6eba7`  
		Last Modified: Thu, 09 Oct 2025 22:39:05 GMT  
		Size: 69.9 MB (69916273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2f8dccb702d01c05b0eefddc85127e3a9e04de074763fb150c9e203c822173bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7210ec735e419291878ecbc79f316bc9ac20e523dc3895fb56643b8561cbc102`

```dockerfile
```

-	Layers:
	-	`sha256:65f38c49a4b24b837721eea0f61da651d8c5a3c88484c0de70854342c493ad03`  
		Last Modified: Fri, 10 Oct 2025 00:19:15 GMT  
		Size: 2.5 MB (2524077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb459bf2ca43cc8ecbe9e87e04947420b1da586ea1bd491bfef53ab44bbf72e7`  
		Last Modified: Fri, 10 Oct 2025 00:19:19 GMT  
		Size: 11.1 KB (11088 bytes)  
		MIME: application/vnd.in-toto+json
