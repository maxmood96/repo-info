## `sapmachine:lts-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:26f25d50b23eec1d0609dcece8b825e06d5b81ba0eb46dbbdabdee99b8c563a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-noble` - linux; amd64

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

### `sapmachine:lts-jre-ubuntu-noble` - unknown; unknown

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

### `sapmachine:lts-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8a499469c239a9464561979180e960f8a5406d4502cfad5750afd7bba1e1234a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96824720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cdb5e27488d711db4e83b67cfde66dc99261740564cbcfd90e58ef2ab63b461`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:de58eaf5046822025e90de7234d30fb0a34c84dd3a876fce74b06708613ee0db`  
		Last Modified: Thu, 09 Oct 2025 21:28:07 GMT  
		Size: 68.0 MB (67963008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:74ddbecbd02e22feec5a24a0a0ccc14f2ba78d84d862333437ad0d6fcabadac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb2fb881b84993486d391509ecb374dbfc5f1b8622475f1643947ca1fec4e54`

```dockerfile
```

-	Layers:
	-	`sha256:c8fd142411984f2c9285e93adc5caadef4d2a1c04e4762018b458acec91f7508`  
		Last Modified: Fri, 10 Oct 2025 00:18:15 GMT  
		Size: 2.5 MB (2527157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76ba85c47e01ef4f9b0ef3b29b487c00279aee2e7a93cd240a0ff3faa392885`  
		Last Modified: Fri, 10 Oct 2025 00:18:19 GMT  
		Size: 11.2 KB (11188 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5e305de8ddadfa12d26dae1fdcaa58db27df386c411524c280301cdfe03dd322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106843304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14f56bcb38901b71c401b797250bd82dd8c4fceb263f6343fc8c4372e430277`
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
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
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
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eb62c34c15cdddd5b94ae59eabeba45ad2dcf60055f3e30ad4f001c81eaea3`  
		Last Modified: Thu, 02 Oct 2025 04:15:27 GMT  
		Size: 72.5 MB (72539757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea08aa0c48f0ec6044db10862769835480865daa43a8cf0d88871a944ec1af28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d0eb45c56bedae9a8edc283e5d46903b5c285203bcfd8b6dad4af05fc0f677`

```dockerfile
```

-	Layers:
	-	`sha256:85b7fa1cb04c5693f2bf6d9e4bab47964f8d167bd26ab0fb89c6abd2b1657240`  
		Last Modified: Thu, 02 Oct 2025 06:11:03 GMT  
		Size: 2.5 MB (2524077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b2582a821b9ff07893a77c2168ceb955cc975b1aca1cfd960a730797508bbf`  
		Last Modified: Thu, 02 Oct 2025 06:11:04 GMT  
		Size: 11.1 KB (11088 bytes)  
		MIME: application/vnd.in-toto+json
