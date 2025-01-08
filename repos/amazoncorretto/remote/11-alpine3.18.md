## `amazoncorretto:11-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:abf2d7ee1101fa81668b3e0c5f9ea328eead28f146ecb3bafaca9bad6da8aa50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b03745db2ed177f470ed7199a0d4bb46545c31fde0ff44e43663486dcf8b9b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145317935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ad49524cfd86ddcbe3b8f09d67733a1ba1de7366ab7e594eab77365ef961fa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2f944e2e943788e6091c4ef9b268b253c6e9cc9444d9387b402ee0574f0471`  
		Last Modified: Tue, 07 Jan 2025 03:29:13 GMT  
		Size: 141.9 MB (141910303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dacb16f0cbf39bf852530484df3d88a3e17614519ddbab564cbf5b0167dc3831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8a1bfe3d7edc090fe8375feeda6ca67adbd5fbd4a0c0c64b1959f341538857`

```dockerfile
```

-	Layers:
	-	`sha256:32a3be944e831c03b26fcfde91cbdf4a4096abc2f4dd4f919c2138b72682002c`  
		Size: 387.0 KB (387034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1eb7cb3aa34fedad0e88879f93cff2870832437da5785f2b575f414564b943b`  
		Last Modified: Tue, 07 Jan 2025 03:29:11 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0af2a707a7289dea86aa8bc35dd53721215ba4d2e145e7036ebf27f60878b95c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143368499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03593b46b522725109d3673e470e267a867853a0e5b63e709f4da61b6f39e72`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8188621fd18ffe1ba2e81de7848816358b28c33737c847ac894975cd0b739abb`  
		Size: 140.0 MB (140031064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a06c4860efbcc19c568085c01f75fd8a6fcbe389c970ea2c43b910630fcbacab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 KB (396611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158efb84179fadb7e95b400bb466b9e12439561111cb533366e3462418f98997`

```dockerfile
```

-	Layers:
	-	`sha256:2eeba4aa417a96c4a704c734030fceb07d4eab606b29ddd3de181f01904cbc87`  
		Last Modified: Tue, 07 Jan 2025 07:21:24 GMT  
		Size: 387.1 KB (387090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d69b92e9573cf30b4141dea1647c1972e220e41903ea50206c2b3fa265baebb`  
		Last Modified: Tue, 07 Jan 2025 07:21:24 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
