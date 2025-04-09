## `sapmachine:24-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:25db3187e764205ef9dae48f01cb2bb7a53ed19580011291749372736fe908e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:d14b60c9849eab1030a9dc6ce41a95c7bc0867123d5c1b08dbfe20fffd3778af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262111536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47139728e4400fe65095f90684c34b7e38ac0e42761d1d373654f1b07c9f98d0`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:3437ed35f5c8d446cef703f6d9da0457dbfb86de2d1c0bf4dddc4f47150e8a1d`  
		Last Modified: Wed, 09 Apr 2025 01:20:35 GMT  
		Size: 232.4 MB (232393884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ea0931b0413f8b516861d89954e36461b477b9991e4730c5b86f28453e99c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84b410ab656dc59be41d698a829ecc347b564a25deb4ad64be4b6bb2fd39d5c`

```dockerfile
```

-	Layers:
	-	`sha256:435e3e8b04cc77313e3724358919e098afcc0c0cc48b0859615a532301b76164`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 2.5 MB (2462905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b701ef4041a5668065401afd8f458b30d9b9089a6c92f90677ebc29c23a345a`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 11.3 KB (11299 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f0a3e4889dec349e1b2f499e7384068dbd98d28700d9046d33cc4ee586972449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259193244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb0b3083f99c09628492cc18f51a30d24e87ce2b3fc74748215d16e014a2a6b`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b1c7edfdf6de34893eb2e6dd88cfc36488b8964fd60c7158bb7a9b3c802be904`  
		Last Modified: Wed, 09 Apr 2025 09:17:44 GMT  
		Size: 230.3 MB (230346286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:83a9477938e7a479e18d2d6b5f409c57a2a03f81a8d7ffd20e983ed336a0e3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0f62637f10bc4692e973f0d4b6ffc8672a3cc1b3fda4f9f9a9229354df03b3`

```dockerfile
```

-	Layers:
	-	`sha256:2a3e6c3235d3ad02ffb77126c0c488cb2cc559fffe6a55fb287ff30ab1a7ab4f`  
		Last Modified: Wed, 09 Apr 2025 09:17:39 GMT  
		Size: 2.5 MB (2463466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f0c854eb83bfea7f5050d8057c347f05e5bdf64ae78b835dfbbf625b6424c1b`  
		Last Modified: Wed, 09 Apr 2025 09:17:38 GMT  
		Size: 11.5 KB (11499 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9114fbeb4f6c3b602d7c34dd7473330d10d5f4a7062374bcaf7b2a1db8ecaa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268072893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add97a53dcba9389f98ea0b3388deebc6054604dcb06a5450bbba9aa6711cac5`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:99dbed487d09d89c96ca9a6f11775281f704f98f496f1ecd9800b0596428fb45`  
		Last Modified: Wed, 09 Apr 2025 06:32:47 GMT  
		Size: 233.7 MB (233732026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7f5ee978899c9bf1dda7a9736ba38c0d7e763c9c48f3d57299eb81496d03934d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265d55f0218085bb0807bd6c3fcaed6fd2b30591883236f2923ba2c65265f8a9`

```dockerfile
```

-	Layers:
	-	`sha256:7f9ad74d76d0a72d307413ae9de74b6d0a2b50c46e7efd8ca7eac55c3d17c8f6`  
		Last Modified: Wed, 09 Apr 2025 06:32:41 GMT  
		Size: 2.5 MB (2464328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:181445abacc6429a7d0461e43e8650835e9808600f1241d5ee4969a2f11985d4`  
		Last Modified: Wed, 09 Apr 2025 06:32:40 GMT  
		Size: 11.4 KB (11388 bytes)  
		MIME: application/vnd.in-toto+json
