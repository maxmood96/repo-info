## `sapmachine:24-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:aa28fdf12202315dc259bdc78910061ecdbc364c780d82133178f3e78fdcdad0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:93484eada849f627436d6a50cdcb9ff35b8951ca2d8cdb9d54424ea5fa37ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260372588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df46c42e0d74342b972b13c213f9e0a5cdb66a3d82f7e69aee10b990bbdee49`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cd09f7e2f3b0a480dea808ebf555e5a420a819003bdb14d4c2113d31a22e74`  
		Last Modified: Wed, 02 Jul 2025 03:13:03 GMT  
		Size: 230.8 MB (230836902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:afdd06fcffa551f4ed609d345da56e5aa9178cd2e29b16328a4b6b4e8c6a18e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf24d734568ad261c166e28fe30bf707246bb08fe159d25e9ce6a521c397353`

```dockerfile
```

-	Layers:
	-	`sha256:38db351dcaceefae14c8cc4d1be8b57bdf16ba74d5ad9b7246b048090cb1aa37`  
		Last Modified: Wed, 02 Jul 2025 06:09:23 GMT  
		Size: 2.4 MB (2369028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e017e794341205335035d6724cd9bad3685586e1d101302c74acf0c8bd1bbdcc`  
		Last Modified: Wed, 02 Jul 2025 06:09:24 GMT  
		Size: 9.6 KB (9612 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:98ccf398ee848f558758086a9ad2d155f0fa11afb164a7c6f364bdf64a42e10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256068549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca6a4987f11569671e770b758190347de5d142afc48258a5c135d02a13b9c31`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6697569ee6eba01ad83d5f5542ad80e7b959b666604222fdb46adedc48df29`  
		Last Modified: Wed, 02 Jul 2025 06:36:08 GMT  
		Size: 228.7 MB (228709277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f449ca1f8c1907082ed42e5a3082c4bb92c0e92e7c336f9406d5ca9e15f863c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b42a8c11a812eeeb2802ba8fb3f57278e5de38f0e2b7403fd923cec9a0a391`

```dockerfile
```

-	Layers:
	-	`sha256:efeb7215f123cdf5c3f35fe2df193d503add6ab5540bdef04b8218e170d06802`  
		Last Modified: Wed, 02 Jul 2025 09:08:08 GMT  
		Size: 2.4 MB (2368721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:300f4d608c49e04476614b39e855b0267d9c74eb7b89c8f1b7f402affcc96708`  
		Last Modified: Wed, 02 Jul 2025 09:08:09 GMT  
		Size: 9.7 KB (9740 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:32d0b85a5ed3aa4032b40c1e94b67d4adb51de60d1d35786de3dfbb067d3fa4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266305843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17af210dd84beb54cf2bc707e910a392c1fb3ee0e71c71451cbf179b58be55fe`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1433ebe3df2a3b83eaa367103fb6e717a0e753f75c983f2e72b8220df00a9e40`  
		Last Modified: Wed, 02 Jul 2025 04:43:23 GMT  
		Size: 231.9 MB (231863222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:905fbd43ca0795d62694389bd9f5870cdb573d314433ba2a979b4e059a20c2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3106b0e5a57869586b63bcb3828b2becee8454e40a653f94645cb5582bb7cd`

```dockerfile
```

-	Layers:
	-	`sha256:9034e9c27360fca2c552cd156d9da3c2a732e18b795d75e90d83eda49fd0adef`  
		Last Modified: Wed, 02 Jul 2025 06:09:32 GMT  
		Size: 2.4 MB (2370517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28b0a2bbad370cf3379b116b51c46d2a228c7579937e4973740fd07d960fe437`  
		Last Modified: Wed, 02 Jul 2025 06:09:33 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json
