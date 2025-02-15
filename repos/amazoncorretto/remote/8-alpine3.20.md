## `amazoncorretto:8-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:c7191f18bafa378062d83145af35177077a2db2beaa3c2737a786dff3ad09335
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:142efab2983ca1290ce0b9d81a3f7df8d4a418f4b14e49312f4142232db533f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103851187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c889a90769a5a0f1de817a9540167b09e5231831229d6ce47d766382f71b2d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad8f540186d6b8baa6478251ce033fc2fcfc81124eb82e52f524e348058d70d`  
		Last Modified: Sat, 15 Feb 2025 05:55:27 GMT  
		Size: 100.2 MB (100224290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:22e1d94b3e76c0ab1b9921a7a506f753319629f81be26cf70379d452a1d77216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 KB (250800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48eee0929473c45fa9e0cda4e26985476ec7f366b138989c93458737adb8e8ef`

```dockerfile
```

-	Layers:
	-	`sha256:83c8735c59b7d0726ec99762542e73a1177eef1308b6d03282e7469d72ffc640`  
		Last Modified: Fri, 14 Feb 2025 22:50:06 GMT  
		Size: 241.4 KB (241402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8abde4e67740cc9bbd5449826f67cbb67cf3d1630e1719d5c6dbfc59c4b0c051`  
		Last Modified: Fri, 14 Feb 2025 22:50:06 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dfa6946c28467422c0591ad94db1794e6f96dfc4c07c2b7dfbdb156c0aadcbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104101177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468812de1831ecb1bd5356806ad9180466588dd8863fc93e8ea7ab4764798bd5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666cfc096acbfec1262b9688436e92366b9039a2911d1dd4ce164f026563a671`  
		Last Modified: Fri, 14 Feb 2025 22:32:52 GMT  
		Size: 100.0 MB (100010012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:db3f045e81a9a784f12de729a448904cc5f3408eee516e9984ec10c60e85a982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 KB (251036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03dd561b8109a1d523c52c320e8b471eb2382b79a33384efb9e043c7523e261`

```dockerfile
```

-	Layers:
	-	`sha256:7bd329190eec7b15305980f32322c4aa909f785e60919b0e9d8928458e4ceb87`  
		Last Modified: Sat, 15 Feb 2025 01:50:00 GMT  
		Size: 241.5 KB (241534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfd70c7cfeb543f897193a1c030f92ed1612fd3b9b4f0d2188d501625c210ee7`  
		Last Modified: Sat, 15 Feb 2025 01:50:00 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
