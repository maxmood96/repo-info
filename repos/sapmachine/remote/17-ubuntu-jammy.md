## `sapmachine:17-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2eae0647de6ec18163fab09702bde9c5dc764c223651163ecde6fff8f9365ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:63cd6e3906dc6e2e177282e1bac84e828e5c0c36aa55e6e82899b82b62bb6b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229552265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d4570dfcae24a1616bc687939038a83a25e5a8d239d68e498718974898442b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6539e6cc934b187f65c78f5b9260ec9a26e1e70f951522d8bfaa8b064eea1171`  
		Last Modified: Wed, 02 Jul 2025 06:09:33 GMT  
		Size: 200.0 MB (200016579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dd71d957b844a03113cc57f4c6ffa67a332afd7a7db4d4786049792e8a17e4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2e0b26bfdd9e8cc9f8f5584483c28a4ce973a180cf8828338b0ce8001beb6d`

```dockerfile
```

-	Layers:
	-	`sha256:420a21b1561d83a7e97ba9b2ed9c190ce3eff565d96c4f8779b56d8386433d1a`  
		Last Modified: Wed, 02 Jul 2025 06:05:46 GMT  
		Size: 2.6 MB (2627847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe044e0c11583650882196ea614461d0ec6badb14eba3e80251c9b694594f433`  
		Last Modified: Wed, 02 Jul 2025 06:05:46 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:af5c015cebe69ed5accd4e2ee459a3f0f9066b3e069659e5ce9daba69c1d7450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226073182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed817773d2be289028fa5ffe2f4b89f7382004d44bd14b2174ec84a41f8883a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056a5cf0f6b7bbe4e87dc61b55a44a2c4639fdad4a82f8b84640d2640cf0ba47`  
		Last Modified: Wed, 02 Jul 2025 06:47:56 GMT  
		Size: 198.7 MB (198713910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e4e88d519727d50e715064cb4b32eef616e5f040fd96ec601e812b145fb6ebc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0442478e3a8e409b7b6dccb793ff5b81fb8789adc363dfbe21c7ab935babeca`

```dockerfile
```

-	Layers:
	-	`sha256:a26867d224dbb4469996fee024ee4c2c8023817a2136fba451d6cab6086b9ae4`  
		Last Modified: Wed, 02 Jul 2025 09:04:59 GMT  
		Size: 2.6 MB (2627577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fad7ba9495322e82904e6091ebb7758e9c3bed125c14443dd4d437d5bcbd3800`  
		Last Modified: Wed, 02 Jul 2025 09:05:00 GMT  
		Size: 10.3 KB (10290 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a6d2e26981fdc1131c6bbd51254dac06d54cbca53056cbc828b5ec610576ae99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235531295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01ac6bb93c352d2b08c53d2c784d22c5816de1c8eedbfc15deb9667d328e9bb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894a1be16041723efbab00f9442180358648594fbe6056971ad504e599a4bca9`  
		Last Modified: Wed, 02 Jul 2025 05:03:21 GMT  
		Size: 201.1 MB (201088674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37f0632753daf67203d7f97e62f4ce14764642af3b5b77a91757da01ce6ac129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b8398c87804888cbb19fe7df871a01cc6bb71c5a30e03b555136a4715f2a47`

```dockerfile
```

-	Layers:
	-	`sha256:32791e3c1866cdb2f28d99400de832943ea2fe5d5c2227322473608325e1b866`  
		Last Modified: Wed, 02 Jul 2025 06:05:56 GMT  
		Size: 2.6 MB (2630056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e427ff3b406ac2663c2f5a2c6d054e4f3b39359ee698fde3141af4a83bc1ed69`  
		Last Modified: Wed, 02 Jul 2025 06:05:57 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.in-toto+json
