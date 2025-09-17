## `amazoncorretto:25-alpine`

```console
$ docker pull amazoncorretto@sha256:807ea3c4000a052986cd1e7097a883f9cd7a6e527f73841f462e3d04851b8835
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:151682214b8d93e6672928bfaadeaa547f14301f080228e4a484c231cbaa4f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182320699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d809cba8d748c8cf79511edaecb10d41e7ab85019261a911000aa18210a52084`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cb07a476f609d2287eaf6b137a40ec572e48ba56eba9ad05879115a3fcefd1`  
		Last Modified: Wed, 17 Sep 2025 18:57:40 GMT  
		Size: 178.5 MB (178521010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f524cab769a18256ddc3c0531f9ee24faa83fa2ffccbda1514a52696dd09f4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 KB (401578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a64b76c0952d2f77fc544fc14526ff2f4752575a8533747afb39792713ca1ff`

```dockerfile
```

-	Layers:
	-	`sha256:7199a8446c2e92455e7d850a0c4b330fc960055747012e79b6f088e60ac6036c`  
		Last Modified: Wed, 17 Sep 2025 18:48:47 GMT  
		Size: 390.9 KB (390858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc3ee7dc616b92ac02e60510d3b72e0c1d350d32406572eb7d71eea1e0689bc`  
		Last Modified: Wed, 17 Sep 2025 18:48:47 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:99cebb5dd582c1d5ab8fe4dc9ea5457d00deafe0d611b3f89e64935595cc06d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180201411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72969150ab5fd589a6563dacbe74102a19bc4e7ec61f0b596e9f0fa9f9217f3a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c399b6f243d42421efe409b77ef3aa4b29e98e1b3e494cfddb5b45c3256dc6`  
		Last Modified: Wed, 17 Sep 2025 18:58:21 GMT  
		Size: 176.1 MB (176070661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:18c2452031419cf7deaa361f0139c9aa4c47c807fe469d4362cc51bdf467a499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 KB (401194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8812a734862480b2616652f4765b64a2788aa3cba74f02f8f8323c4fbaaa5fd9`

```dockerfile
```

-	Layers:
	-	`sha256:93230ccc9eeb996592b70215766f9b8c3d2da477e0e1281ab7ec595ad5510e01`  
		Last Modified: Wed, 17 Sep 2025 18:48:51 GMT  
		Size: 390.3 KB (390322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:353566391c91ea841a226cb4c90790d9e4a4bb074473073a86f0d1560967af0e`  
		Last Modified: Wed, 17 Sep 2025 18:48:52 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
