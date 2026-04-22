## `sapmachine:jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:3a56b179e199f751ce3966cb5e1227849f823781854bee782b51e9cc64950605
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:40c374e431615529f67c6cb71e63683cc4506adca573bbab5864d673223a6a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87133842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf868be28c3ad6a251a0ea356423bd8c3a730792b9c0f21e34739ee99fefaea8`
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
# Tue, 21 Apr 2026 23:02:48 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:02:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:02:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a5b28d6aa198d16a655b01d181eac32736d040907e93197657998b41471d3f`  
		Last Modified: Tue, 21 Apr 2026 23:03:01 GMT  
		Size: 57.4 MB (57397344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:269a84e74ef0e81dcade587145e93c72e2e321481cbfc4dc70c49a547543d524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fdfa53307ed97815ed2d6ea76cbb9544421bfab819ddee343caa590bf56f0b`

```dockerfile
```

-	Layers:
	-	`sha256:a1c0a0f6b856a9e3ca47af21e6c6631e70b7aad65c5ac9fe826d231f640c8591`  
		Last Modified: Tue, 21 Apr 2026 23:03:00 GMT  
		Size: 2.3 MB (2301075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3f94801e94a69223c13ea6af794d05fc728a68a664364053e43f12a6f2791d`  
		Last Modified: Tue, 21 Apr 2026 23:02:59 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:098cdf95cba703132e1760772bc348cb8d53baf3a8a677bddbf7fddc0b764256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83969405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a010602f5bb587819f944dac75c4ea9dfa0711465a0fbf79b9ddec217dc118`
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
# Tue, 21 Apr 2026 23:04:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:04:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1938d72692a8c95cb84ea35ac1ea35c5cdd8e1bff1071b543cecb14879a6fe4`  
		Last Modified: Tue, 21 Apr 2026 23:05:13 GMT  
		Size: 56.4 MB (56362862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37c0c53087591b7c6810e087b3a5c9a3262397901315c37bfcb999470a7991e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f939099c835d66d5a1aa4cb9a06a79715f432e85fb7bf1fba020eb2f443b07`

```dockerfile
```

-	Layers:
	-	`sha256:d933629d9896cc3813eaaf0b202a4416e94414218259de98076d6c297f9ba1fe`  
		Last Modified: Tue, 21 Apr 2026 23:05:12 GMT  
		Size: 2.3 MB (2300768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6003c829e41d50e158f55914dcd0227cec0c6a52bdf6ff3f3b50e0aba264ca89`  
		Last Modified: Tue, 21 Apr 2026 23:05:11 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:19b6df03ce12277c8b92fc768dafd1b4de07caef69eba61c48e4b2ce3c4348d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92940916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf278c38bd5df57a58550b75395cc5975bde871208840ee03f69686cde3557b0`
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
# Tue, 21 Apr 2026 23:55:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:55:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:55:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd678bba411aabe57dee6acf60572da5ef346adc32fe4eaa60fbe3a2067c9d63`  
		Last Modified: Tue, 21 Apr 2026 23:56:09 GMT  
		Size: 58.3 MB (58292518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:595139c1506b38b0b7bd73f3826a929f54ac0597b2e38a62e205643a3d1b6214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9fb433aa9a27792729597233de953d1dee65d1eb1b381ff9b130b6adb04c44`

```dockerfile
```

-	Layers:
	-	`sha256:3d007aaf6ee456e3861bc008f6007858c12bfab1d20997c67e115e5426cafbb2`  
		Last Modified: Tue, 21 Apr 2026 23:56:07 GMT  
		Size: 2.3 MB (2299899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea8ebcb78f5ae94f8b11be6151786e1c3097c9add78d2eaa31b49866821ea3d`  
		Last Modified: Tue, 21 Apr 2026 23:56:07 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.in-toto+json
