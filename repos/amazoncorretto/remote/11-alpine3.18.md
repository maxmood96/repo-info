## `amazoncorretto:11-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:2d3969271690016c2a73d6f5dd185ebb0a78e118390356d7d4f3e674af90db9b
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
		Last Modified: Tue, 07 Jan 2025 03:29:11 GMT  
		Size: 387.0 KB (387034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1eb7cb3aa34fedad0e88879f93cff2870832437da5785f2b575f414564b943b`  
		Last Modified: Tue, 07 Jan 2025 03:29:11 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:71c1fc2c19fafed8aaae853c2d20570a934f6321053482e4c5f377296e14bbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143371466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45635d2d6005a97ce5a85c6023488f0bf6f871ab6164c53d11a1578ed83c254`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0ad810209680ddf085e0c58d492b20708b9aec9f84ad9d0f0083690c16fad4`  
		Last Modified: Tue, 12 Nov 2024 11:07:02 GMT  
		Size: 140.0 MB (140031015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:60771f2ef39b4f35340b3a0dbf093ff8009ab251c95d4e365045e1486eb2b2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.2 KB (397247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad1d36f4d0bf4032c0d3871a30284d4d4a2192d42625c1380d886fb15f48a0b`

```dockerfile
```

-	Layers:
	-	`sha256:f64f9d0b858c5840657c7b9de1b3ab81754f98551e3b7b8eef1f9b166f474dd6`  
		Last Modified: Tue, 12 Nov 2024 11:06:59 GMT  
		Size: 387.7 KB (387726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376e301b81fee437f65fff9f3c117f9dbbb51521b3ec2109bc1c115678cd7503`  
		Last Modified: Tue, 12 Nov 2024 11:06:58 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
