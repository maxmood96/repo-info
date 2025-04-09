## `sapmachine:24-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:bdf0c5d1811358eea57c0bc38e803741c284ab6af4a9a5d6a09414f78179130d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-ubuntu` - linux; amd64

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

### `sapmachine:24-jre-ubuntu` - unknown; unknown

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

### `sapmachine:24-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d26507163605f6eb1b81ab5a3caafda9cdbe479f18e6cafe68d54fe5535aab36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95959535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd67460b947209e51901c543ef5d1e7adc1f1370ca0e33b8d90a631b321a25f`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4a05631d427d35aa4460e49b5b806479de8a7441a4d73af4331496e38f07b0`  
		Last Modified: Wed, 09 Apr 2025 09:19:33 GMT  
		Size: 67.1 MB (67112577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e2692f5a9a47e23bcd3d906f3d013276b722551e0fb55f780407d05cd1eba782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2ae5950ea69afe2b1a01c009e99c4b34386bae77d213d25b8504b2d288c927`

```dockerfile
```

-	Layers:
	-	`sha256:76c53b2e960f33e85f0ac3c371d615590aa58bf99c551634a39cd9804685bfd9`  
		Last Modified: Wed, 09 Apr 2025 09:19:31 GMT  
		Size: 2.4 MB (2394311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75fe9e6d27b22e44e347a9dbe60c55e48a7bd7ccb3668816ba3e41d1dac17071`  
		Last Modified: Wed, 09 Apr 2025 09:19:30 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu` - linux; ppc64le

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

### `sapmachine:24-jre-ubuntu` - unknown; unknown

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
