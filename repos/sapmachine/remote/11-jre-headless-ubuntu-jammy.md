## `sapmachine:11-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:269a1ba33687da2ff76dae67ac39e5c5731d7e980d6937bdf25003d2d3b63c51
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
$ docker pull sapmachine@sha256:e922b5cc4349d4feabc6c27c8b7b6bf305d9c9e1793f19da64c76d000a431949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78264697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e65a27598ee429ee19912dd3f165134f8685e8878a7679bee5010951ef79ef`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751801cee673eb5775da0ba3c88b9cfdb4ff3848b6212fc10a0d0a3bdca88e3d`  
		Last Modified: Sat, 17 Aug 2024 02:06:02 GMT  
		Size: 48.7 MB (48728672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c5f63cf0479d193ed1a71f7ff23f0a49f7173920244c6bee89c4254640070f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655b54b761ddd95a303c007ee7be6a94a0fdcb81726ac8c13ab779e7cd16e7cd`

```dockerfile
```

-	Layers:
	-	`sha256:5cb45ee6cd0caf7c5453a1ff03455f476c238cc94746ef78c7ecb18c226cac57`  
		Last Modified: Sat, 17 Aug 2024 02:06:01 GMT  
		Size: 2.2 MB (2156982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a5931b2334b5755afcdea384627fae678e6b2fa6d86145fab37d761c851d892`  
		Last Modified: Sat, 17 Aug 2024 02:06:01 GMT  
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
