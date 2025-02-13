## `amazoncorretto:23-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:22c1c6d082cc82f82e2fbdcd5234e7af5ab4a1eca972451c2ad1583cce03d0b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e2e6fda227603ab353b3f33abd8633b430cde9693746b02329b8ae874cc5c802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170330224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4a9768973fd24fccfa6810fea203b89383b620601b2121565f8294d357b227`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bef15c8cb6a42bea4d2e0d93935a6ead56049c80e99ad76efdca85b5f2ccd14`  
		Last Modified: Mon, 03 Feb 2025 22:52:40 GMT  
		Size: 166.7 MB (166688509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:936c5814e613f4610800e163997c1c3f956f1ce304810ebcbf7dbc9eeff663ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.3 KB (396253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ab711ccf83d2c866bcfccc6358cab0c2fc8699009ee3dcbff9d47bfe26f25b`

```dockerfile
```

-	Layers:
	-	`sha256:9f5b0a3c1296ea344f5bd539da827e23a6456f349e27b8823c9a13452f9b50bd`  
		Last Modified: Fri, 24 Jan 2025 23:26:22 GMT  
		Size: 385.5 KB (385533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f705b31e62c33db71e89a9e8e8caa54090454d74a25289473f58e11219039de`  
		Last Modified: Fri, 24 Jan 2025 23:26:22 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3d8ee739b392ec707fcdbd0a94619d6b78cbe85cc661e9deceb328f687f52e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168401314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e834c1e9561f232db469c1a63546499d41e7984a5eaf4775263e025294b8edbd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2878835051f9fbce2b6c083c3a44336794100ea7264ee2337f51a9e8faa287`  
		Last Modified: Tue, 04 Feb 2025 10:03:19 GMT  
		Size: 164.4 MB (164408955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d674444ab4b8acf5c0b91ecfae3df4d521d878d9277d2d9e595a766f84975f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.2 KB (395232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6444c93fdb68653a1bd95c8ab7084b90daed81f9a10b98781febada3ac5be49`

```dockerfile
```

-	Layers:
	-	`sha256:c87603f6823c96fe2b5e9a209281d338a6c4a0920ba394de4917baaf0c6bf8d6`  
		Last Modified: Fri, 24 Jan 2025 23:29:01 GMT  
		Size: 384.4 KB (384360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c7f9a828fcbf4e4fb98ba76f22d4b353c84ab5b88c6fa2ccbf008b16f53367`  
		Last Modified: Fri, 24 Jan 2025 23:29:01 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
