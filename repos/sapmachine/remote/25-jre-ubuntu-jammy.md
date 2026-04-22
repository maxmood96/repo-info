## `sapmachine:25-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:e8231dee974f3e855a359e1809664289585ac81cd5469d63d9406a31807a829f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c573330f3a8c6e1f116f9878da9ab2bfeaeff66acc01e110e5b741a568a8587b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87422616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c42ac9e957533f1c34a21ffbad8888a07ea4e4c4cd17d33b3203e381e822eb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:03:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:03:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c386bd402e2a684f65f3dbe9ab8b882aef3688196d885d2014028ca7b3eb5e`  
		Last Modified: Tue, 21 Apr 2026 23:04:01 GMT  
		Size: 57.7 MB (57686118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6f40683dc6f93f6629751dd9640171388d155a2b5f230cade5585c6eec6f7952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2563151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877d63ef03ba24e376c9108848dd0cb5708d9dae444959b74de87d2d3f39384f`

```dockerfile
```

-	Layers:
	-	`sha256:8adcf5b99a75c7ee884d8832a539746d57b96acb2a7e9dacd801316783a85d4a`  
		Last Modified: Tue, 21 Apr 2026 23:04:00 GMT  
		Size: 2.6 MB (2553715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:657702ece40cfebbc08b896b5964ffae5cadf5edff52ae9707e58a6c74cae83e`  
		Last Modified: Tue, 21 Apr 2026 23:03:59 GMT  
		Size: 9.4 KB (9436 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:98d924f01d530e35c94a38b1dd5d0ca4d561c8720aa9e0d848fd58b7d18e860f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83867848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384c82359592454281416b980cb978f851973a2fbf9b0cb7dfa3fa9d0c218941`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:08:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:08:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 21:08:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae43ff49025df516af99e35bddda78d0fe234614cf18ae4f17ae8560f6ae90b`  
		Last Modified: Wed, 15 Apr 2026 21:08:46 GMT  
		Size: 56.3 MB (56261305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e2133dbda12fd3abafe9b0a39b1c6482f178cdae20e65f59b39c371c860b0747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3d2871b1cb19ddc51575aadde5796d0b8ae6f07d82a6bdc928604e066e491a`

```dockerfile
```

-	Layers:
	-	`sha256:5c966d56a00c65aec55fea02163ab966629d69c0c251577132e10d50863aa115`  
		Last Modified: Wed, 15 Apr 2026 21:08:44 GMT  
		Size: 2.6 MB (2552784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e765e98e6ac3367ceb51dbbc9b7f6e6ddde2cb123ac35c1c6076a058ae6531`  
		Last Modified: Wed, 15 Apr 2026 21:08:44 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b02aafa71edd32c250b41d9fa0abd98c1031a3df1663ff37435252e12f773802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92872398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6adef2d8491d2ed0f115a18251b4906c2c6e81fff567cef6be21fc29bbca60`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:31:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:31:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 23:31:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98777fa6939a4066443e19cddc83c101cd98be3348173074a2493666f03c98fd`  
		Last Modified: Wed, 15 Apr 2026 23:31:37 GMT  
		Size: 58.2 MB (58224000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:55233f88995f2a86d1de67cc49990e92b321e4f7c59c01cf28d9fa45e6a8e152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d6c9fd6b577e5887ebaf76c70dd4d916086f5440dcad3e5c3d2f440ce3b80c`

```dockerfile
```

-	Layers:
	-	`sha256:461c678422751e0a6cb0b1aa9e12acc35ca30ee74e6d0b85ddaa664a55cd8de9`  
		Last Modified: Wed, 15 Apr 2026 23:31:35 GMT  
		Size: 2.6 MB (2551995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4e26bbcdb5304e0b49e2f077d0b97e3896ab0f5afd1e0c1bb1d2dda415947b1`  
		Last Modified: Wed, 15 Apr 2026 23:31:34 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.in-toto+json
