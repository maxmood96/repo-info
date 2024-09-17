## `sapmachine:11-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:a69d68d01826c5fb4df9c94f0980622165c2159f5dff329ede63ab20d4eca795
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:ff6dc662a6ed6f0e1603f90d682ed690a44120d90f7a43c712bf9b2f86743ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78264308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5017df5b447ea1265dfe63feb9b2212e07b030030454e6ff8d9d84bdfe8c745a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5083cf04d346f42bc4dde0d2465adc56e1647e304d3a8bb1cb980a61b631a7`  
		Last Modified: Tue, 17 Sep 2024 01:00:42 GMT  
		Size: 48.7 MB (48728620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8e719293b645436e401118410a07f06243ab0c70201f545789604db17354278f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385f25eddb86539ed542522aa653eeec5e68f8908586f3c63745a7705a61b5ec`

```dockerfile
```

-	Layers:
	-	`sha256:635dc426a2c3a71a79e7d15ec855aae45c5fee455f4d95bdff4fe785df745f71`  
		Last Modified: Tue, 17 Sep 2024 01:00:41 GMT  
		Size: 2.2 MB (2156982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3fb5a715a12ceb82f278054429fc7033130a88fff75275508095ce9ec20d43`  
		Last Modified: Tue, 17 Sep 2024 01:00:41 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a5ef1ec9231fc9a06645311cd2492ef767f6ba74dcf723d21fe9f46a19e88e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75372200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f9756572c435a6576a5964503ab694ebfabcb659150ed1ab91e9a040a9b27d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdcf5eb6c26ae904f67d0c7e8fab3c24be6b73b817e6a80be9681bd592371df`  
		Last Modified: Sat, 17 Aug 2024 04:48:16 GMT  
		Size: 48.0 MB (48013517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c6f9eaf887a8575f6ef1912031723d9f6cbb37b82ec78fc510283caed158545c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2166259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fb01e86c971f1f827a36f6388fd203e3518a017f4a0fd8f43274229a11749e`

```dockerfile
```

-	Layers:
	-	`sha256:41cf1502458af5c3cc6e1224667dde70ee3c5b97d3552b871ce044bc822629d7`  
		Last Modified: Sat, 17 Aug 2024 04:48:15 GMT  
		Size: 2.2 MB (2157280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27946748ec95249f1539bd751d0df2038001c285e8e416e1c93e87481745b96a`  
		Last Modified: Sat, 17 Aug 2024 04:48:14 GMT  
		Size: 9.0 KB (8979 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8b2ac3813832470652d3748eaf9c6d935ede537b10276d56219c189fe6da2fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81652049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7479d5b5bb9fec052bb7ff8140bf77a675035c564363c0c2a6121b4207a58d2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d5dceb31f09364554aa583cda1373b9e595d0ddb96f7b819be528bc7685225`  
		Last Modified: Sat, 17 Aug 2024 03:38:16 GMT  
		Size: 47.2 MB (47187871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:219cf4b0503102a35bcdc5a11248d249ae905bbc676b01a32daefea974da8624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331fd938521b02ed8eaee51e4ae7de8608d210009da4bec2b4314fb8802b80ec`

```dockerfile
```

-	Layers:
	-	`sha256:a4ac39f631cea42495507bc3076228eefbbf5e9e77c66d293dc83de647b39c03`  
		Last Modified: Sat, 17 Aug 2024 03:38:14 GMT  
		Size: 2.2 MB (2160897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d9f93482a47e1c2b053f3e3212c9b28d68f7786e57d4cc5730edeb79763a9f`  
		Last Modified: Sat, 17 Aug 2024 03:38:14 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json
