## `sapmachine:21-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:76c06f21f5c531b18ed961b7a50c59a3311d5bac94a8986615775f499141cef8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:2a20f5fd016e23e8b5cfd13b96615c67d346bfac67406fd1ec277aa62f696c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91140912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dc733b95b81e90a76f2323f2ce81715f72b68d0e7fdeea9dae3ee150086cbc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689365fa471280d7953657d3684dc48df1ea46cfef464469df9403540cd03ec7`  
		Last Modified: Thu, 02 Oct 2025 05:19:15 GMT  
		Size: 61.4 MB (61417901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0d2d4fcac088bd102a393c235298a05cfd3058f59ec8497eb5f75fcbc25fe505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9848d6cb667e468359d5dde902e8d1ff248c129193676cd32346d70911506206`

```dockerfile
```

-	Layers:
	-	`sha256:83b97f56943adcf94db09df7df6352704ced7580cc6ba6e837ce66264aa72be3`  
		Last Modified: Thu, 02 Oct 2025 09:09:53 GMT  
		Size: 2.3 MB (2272810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d09e122d145de4a5cd2f9939a075d4af6bb0847ffd5c563a4695343072586e4`  
		Last Modified: Thu, 02 Oct 2025 09:09:54 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:35f488db14034af2a36fccd4fc29c173404afa6974b9fa8626544c194fe2defe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89271383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b94af45bcfba3c9ec089dd7f8cddc74c03cdeca0af0f81b0f6b96678a6fa57`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11b84c98248a2f0615ed374a7a058ac9395aeea564190ab4ca9bf2bed618c7`  
		Last Modified: Thu, 02 Oct 2025 09:43:46 GMT  
		Size: 60.4 MB (60409808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e4cbd3cd604ee004f91b9bceafdd23c67c79a113583484c31597621a6e7d4e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c83f1d712a02b307ffa973c92319bf28ed4942adb918330e93111d2ec43a7e`

```dockerfile
```

-	Layers:
	-	`sha256:dca2681f7fb448b655669c5d3841020a54308bcc75b61001aa9f22d056d1e95f`  
		Last Modified: Thu, 02 Oct 2025 03:08:12 GMT  
		Size: 2.3 MB (2273317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e314bd51d08a63f159321659c72739e8459ce072e4c16d533765b69dba3744a7`  
		Last Modified: Thu, 02 Oct 2025 03:08:13 GMT  
		Size: 10.4 KB (10414 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fdf5ac0db465851d88a162320ee03c07b791753a6f69ceb151e017203499bb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96984873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1621e7ebb3af7d1bbaca32b8b3c6e3e2f927ef8b73478d536d0b4a00fa14e1d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a086cb5dd2c1c0d40bb7e5289b1fdf52ead661c4f60265330e6af9f6da3b64`  
		Last Modified: Thu, 02 Oct 2025 04:33:11 GMT  
		Size: 62.7 MB (62681326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a10a34a0b0d2d05e346c2855b9fcc2f0203e74a418a058f4479baff40483d389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8ad22e1f88d9fb1f40cce8a63c8ca0bd7b490f6d09f7f1343cf22093d01a6c`

```dockerfile
```

-	Layers:
	-	`sha256:ea25a344dcd7f587f049dc05359b57670c76aafde185ba94f37fb2a4a8fe6046`  
		Last Modified: Thu, 02 Oct 2025 06:08:21 GMT  
		Size: 2.3 MB (2270810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb159612b6767d0fc740cd6f88a13ebaf7b515500f668d89aa52ccc5ce1ad8c`  
		Last Modified: Thu, 02 Oct 2025 06:08:22 GMT  
		Size: 10.3 KB (10331 bytes)  
		MIME: application/vnd.in-toto+json
