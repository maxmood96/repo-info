## `sapmachine:17-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:a911adfb8c63240fbd23803068f3dc1814c31e6b65a2cec0b17be55385f50833
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:800334c22dc3b6797067bb9d6b56c05c68a94d1525d332c3e2294251fa5ce15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82851807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439b9010d4ed8f68927d72902e9f5bae9fec53c9b5f524d27ab64a5a03feb71b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:28 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:39:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b264b6785b7499f983c78f8cf1f3a99d3cf5c435854ef4ef518079f1b3a196`  
		Last Modified: Thu, 13 Nov 2025 23:39:50 GMT  
		Size: 53.1 MB (53127119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:40c9c8f9649e20564a5c513832e29d604f0a3fd9bcb039cc549f85ec1e265fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc75d0d4d2ccc69c5705f2168e41a7f0f8ad362abde063adbf20abcc1fb508e`

```dockerfile
```

-	Layers:
	-	`sha256:73df474556846b648bf1f8fc64d475b3ef0d363e4fa575001145028b0a3b31c5`  
		Last Modified: Fri, 14 Nov 2025 01:07:27 GMT  
		Size: 2.3 MB (2271564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfb4d49fa86d36eedbf6ea56add80aa4475b15bebca6980804b200483519ff97`  
		Last Modified: Fri, 14 Nov 2025 01:07:27 GMT  
		Size: 10.2 KB (10229 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ff5d6e68b43b44f4e30c19b138d234d8197b1c45026fef72860f12aca457a9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81414172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0a754380a18f87897f87da64a886030b84f949360844f7a278cf9be9b6469a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:38:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2383fa730977451e7261b7a6485c5b2e6d20df8cb6842849881b4a645f0e888`  
		Last Modified: Thu, 13 Nov 2025 23:38:55 GMT  
		Size: 52.6 MB (52552215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ac368f8360f3d356504bfeb1433f68fe18e752c2026ebd3ee4918aac7fd8aaff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbce3d9627673d4c9bde8d54cd61e920081e8adc7f9379e5f08485c4f410d5c3`

```dockerfile
```

-	Layers:
	-	`sha256:7f6557d1e28555f3e085cc2aa28f70fbd5edb88ad5408bb4766906b2557b6299`  
		Last Modified: Fri, 14 Nov 2025 01:07:35 GMT  
		Size: 2.3 MB (2272071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98087397f0159f06cf72fb0141b4478a3e4bb34f849ddd221d95acd5b3f5113`  
		Last Modified: Fri, 14 Nov 2025 01:07:36 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:33a011ad733ce77a081a332866b67e2accefc618e27cf121f0d43058a3fdcf36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88446625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10fbd9b5e0a1de45ce7c81e83262e958489f8222139bb15ebc1f364483c2c01`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90121aef651b6278380ec19adff5976f5f17da8a1d97dc8741ab14b1f882eb`  
		Last Modified: Wed, 22 Oct 2025 12:09:20 GMT  
		Size: 54.1 MB (54143100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7dbdd5b5c8355a10c5f689ce7f2aa11b78c7480a045cc820770bef6c54da6905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8292fa3282204e455283cdb3066d3a865208e58b3cfc94b4e298f4c93b151a`

```dockerfile
```

-	Layers:
	-	`sha256:68e8f57a75557ab0d8a06d09c4abb23a47d9fd21da4ddc4777e180a036f5bf7f`  
		Last Modified: Wed, 22 Oct 2025 15:05:26 GMT  
		Size: 2.3 MB (2269564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4bcf7185d949261a98d62bcb49f47c133170ae97d4264da249768bec21915c1`  
		Last Modified: Wed, 22 Oct 2025 15:05:26 GMT  
		Size: 10.3 KB (10339 bytes)  
		MIME: application/vnd.in-toto+json
