## `sapmachine:21-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:1b18469af0af37dd63ac988507062e7ad3337bcbc5df33514d5576d6e6144958
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c8b9a2f2ff2556a1ca9c07e8810c1f88933fcc8111a1c1979293cd08343f99e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244316726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c915543bc25b2c9a27dbf05ab4f5f7c15ebed2da7e8e2484d09789542123b0c3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:34:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f800ca17043cc4d91b72fcec8ea777bdc014ac8f72d5e98aed1370de3d66c63`  
		Last Modified: Tue, 17 Feb 2026 20:35:18 GMT  
		Size: 214.8 MB (214779360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b85c2469c8d0dc1fe8fd852041bca080dcdc1f132a0b9215eddb4a050afe8eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e939c3d89ceb2a97000073df94ce415b077b4d2b59797943a9fafc6f1f61ee4`

```dockerfile
```

-	Layers:
	-	`sha256:0c328cf56c53338c331a72275bbf86183d18301e91a0de6068146b7b87979970`  
		Last Modified: Tue, 17 Feb 2026 20:35:14 GMT  
		Size: 2.4 MB (2380026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace2a8e5d318cfc9b3f4dc0a2ca7bbf795c3c84ce212e5d27596c2868d9aed43`  
		Last Modified: Tue, 17 Feb 2026 20:35:13 GMT  
		Size: 8.9 KB (8890 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ad450716e34f87de06ea466e1c206b909ccadc0127e122ef214edbdefbdf9ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240369644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90b0d7321f0fc4dee6dedb0ac7b819717dbe36b6c3f833707252d02b9bc9fd9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:33:46 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:33:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:33:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6f4906d9ebbb91265c11c1cbd435298bf43bd2559a0892b64167e7426870a`  
		Last Modified: Tue, 17 Feb 2026 20:34:10 GMT  
		Size: 213.0 MB (212984700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9dca0d1bee3f40030a320f21f251b08ab5f5a799d83a92292b0e0b119ff89835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1e415cfe22c64b7fbf2d3696d9e0cad7d71cb171925c5dd52df56f430b1200`

```dockerfile
```

-	Layers:
	-	`sha256:fffb3aabedb725752f8e1582db6702affd813df48f4de0faa3c2ec51e25e2e84`  
		Last Modified: Tue, 17 Feb 2026 20:34:05 GMT  
		Size: 2.4 MB (2379698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af94c2db8a5cd7ef2a2971c22f5e52334be4d5cfe3e36d5aae3455e5d51b53df`  
		Last Modified: Tue, 17 Feb 2026 20:34:05 GMT  
		Size: 9.0 KB (8994 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d2a1215907b0d58e0e6b6e7b9384012eef10f4f75d2871e1cd4bbdb938cb29a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249968552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23180adb045673d41a7d59dd267b043047532503a3662d3ca6cacb261c8af1b6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:29:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 21:29:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4567df109659f5771cd5a65a1c036f60aa5a7b74e84068ce837a32f587ab296b`  
		Last Modified: Tue, 17 Feb 2026 21:30:30 GMT  
		Size: 215.5 MB (215522450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:44f82b1cb1f08d9193d807b607271131f3b1ff5c9461eb67f01e2df428876348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac4ce7c1c442bc6358f3a40fc008d55583b89c81e2c326afca731adee147948`

```dockerfile
```

-	Layers:
	-	`sha256:73db7a306f67faa0fe14664eb07f33e9764fe0746676ca7724ede40249a1d6f3`  
		Last Modified: Tue, 17 Feb 2026 21:30:25 GMT  
		Size: 2.4 MB (2377522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b2541e71635377a4a622daaeedf519a45dc2548ac8f5e58cfafaef39e50ef7`  
		Last Modified: Tue, 17 Feb 2026 21:30:24 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json
