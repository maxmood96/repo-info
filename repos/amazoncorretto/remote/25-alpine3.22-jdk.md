## `amazoncorretto:25-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:ef516854cb77e63e373ab3f7182852cd3dd7f81593d2edc8ecf2fa1e62abba50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ebb2df6dcac6b0dfb116e3f1dcadd0cab0db23e84bee0dca3e048a0eaf5d2aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184570354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c941081ae7611c0d0dbf6904dfd80fe110596b8d113691ada3ece0f96ddb80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:52:08 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:52:08 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:52:08 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:52:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:52:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7736552575071636d1881ed4344ff4ecaaafa86bb652a96dd4698654440a067`  
		Last Modified: Wed, 28 Jan 2026 02:52:28 GMT  
		Size: 180.8 MB (180765479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:20be6d4a41da066532b2065385c271ac9dbb928d7fac5e963bd02f7f3f84812d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 KB (601509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7e1ca6b0ac0b969190653211aa915e5c2504ad9ea039e56b25d4657c132e15`

```dockerfile
```

-	Layers:
	-	`sha256:5ce368ef2712dab417ac97028e81ffdba59a1c9e50d386243435fc69d99611b0`  
		Last Modified: Wed, 28 Jan 2026 02:52:24 GMT  
		Size: 592.1 KB (592137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de51618a9660399354eb86e128ca2c2204828ce9222e9eab6b68f0779cef6727`  
		Last Modified: Wed, 28 Jan 2026 02:52:24 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4f08ab3b9630e0bade0f5264f217a6014518fc2b00bc9bebe2836024a21668b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182548700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5847ee7f0ab48f357335c7248650ef462126e3bf627d2f46eb670788ca2677df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:02:01 GMT
ARG version=25.0.2.10.1
# Wed, 21 Jan 2026 19:02:01 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:02:01 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:02:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:02:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a98f64dec7f57d2647fdae231fb2b4171649e55a8cc3c684f1cb70c248cc2`  
		Last Modified: Wed, 21 Jan 2026 19:02:24 GMT  
		Size: 178.4 MB (178410631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3fe71f0dd325446675e8603fb340190a4943526ccc8b38e2ccd99f147323cb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 KB (601028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf78d2115e727971bfa35682e03724ac33e384b08f7bdf65ff4b5c2de4d1301a`

```dockerfile
```

-	Layers:
	-	`sha256:dddb192213431cec90d463584ec0ee75a7b20e2943525a501a2744229c3d3dae`  
		Last Modified: Wed, 21 Jan 2026 19:02:19 GMT  
		Size: 591.6 KB (591553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3512f38fc7c4647925fefd8cd05d4c8a2e579d1ccd85d16c22e04d7e6ae618`  
		Last Modified: Wed, 21 Jan 2026 19:02:19 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
