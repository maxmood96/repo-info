## `sapmachine:25-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:d21c5604161d7427de6ab8e405740d83fb7e3664c6643514541b02ebf00fb187
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:cc87f5aaca2ccf36213997285f41250e698f10924662bc76f294a4cc8a2cbbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262769912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba22ae8cbd0359a4a02b8a467fd40a30d4141acf60bbaa56838fe38b4b1bea4e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa1a909f899376d9468743bc47f8796d98c774ad8b98f8b6b37d6251b02a0f`  
		Last Modified: Thu, 02 Oct 2025 14:45:27 GMT  
		Size: 233.2 MB (233233094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a9755b5ec5609d5b4d3abfc4ddbcd2b13ab97d9e6f9d99085b47f52fd20a9ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d50c1ce8fea72a5fa30deaa764c35fc35ac3ce31e3b7109f525422e40e818`

```dockerfile
```

-	Layers:
	-	`sha256:b351a8326224a08ab62f2035d0f64f9ebe0791d5e035738151ba961b0600857f`  
		Last Modified: Thu, 02 Oct 2025 09:12:35 GMT  
		Size: 2.6 MB (2622346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de60933603327bfad41462cdc0d236d72016c7ae84225f83196968f6428b8b6`  
		Last Modified: Thu, 02 Oct 2025 09:12:36 GMT  
		Size: 11.4 KB (11380 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:34a44fed2841265bdef6b078a8d9f1a6118b65b37a2fce5d0eb9b4cc21089619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258381108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a214dda13a5c83135e99ac97476bd159cbee5f542a656db2911fb96302b6726`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cc9e178b6f62e1e1eacc959d3a3cd959b07342d0fc01347faeafadaec3dcad`  
		Last Modified: Thu, 02 Oct 2025 20:39:45 GMT  
		Size: 231.0 MB (230998001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:544295818621958b885f422ebd5c9c1552b30b4845f8d246088beffa26e56f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8795068652f8d6ab37cdd2addb0b9a57b923a4a56c1ca0ab0270adcb5702725a`

```dockerfile
```

-	Layers:
	-	`sha256:69cfe9cb94d996eab088e09da705fad4224ebf557bebf65901a5509f52963ab0`  
		Last Modified: Thu, 02 Oct 2025 03:10:35 GMT  
		Size: 2.6 MB (2622121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7f8e8fa4bf3b818c3ee8a842eacea8489892a0647b1068de2856cacb9ba9194`  
		Last Modified: Thu, 02 Oct 2025 03:10:36 GMT  
		Size: 11.6 KB (11581 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e2439c5ef1a743df78ed2aa76c930efee3a6d0ebe629761b04d852b204d42912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268445486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152b6cce4eb96d149d3f6a9c528e3535b6f65aec2f304017316d3dc6a6ee763f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71841ecaf6381242b633450210074abc39c5d2c3865fa50490a2f0c1ea873a61`  
		Last Modified: Thu, 02 Oct 2025 04:19:21 GMT  
		Size: 234.0 MB (233998697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1c1fa844eb0ddeb9637fec633f941d9909a787d7644db361eb7f331a2af5fce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b038fa8e43e04776f84bc2fbe10022b55bbba985cc2df35ddc51e0886f318ca9`

```dockerfile
```

-	Layers:
	-	`sha256:0f6e99fd73dedd464c8b2ce1925144eefde1459e76c45c5e0f9f1ba8f90051d5`  
		Last Modified: Thu, 02 Oct 2025 06:10:50 GMT  
		Size: 2.6 MB (2617945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b677e75944621ccaef1e8385bb154f62cf80ac7d0de0d5fcb87bf4a53707ae73`  
		Last Modified: Thu, 02 Oct 2025 06:10:51 GMT  
		Size: 11.5 KB (11473 bytes)  
		MIME: application/vnd.in-toto+json
