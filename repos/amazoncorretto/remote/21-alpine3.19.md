## `amazoncorretto:21-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:9593b9bf81d40771dacc0574dcb38611c8d9db80dee65f90a1d0b65a486c0c78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3e1a908895811004aeb5d05dc51066b891e26d6da9263b56cc31ed84d591bb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162349775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ea39f0b8f4c3d4ff4cf87d841b7c7f2d91c5044c0dbae5a2832a01085ca0b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a687de8a81ed6abcfc4f4e46291d3e9e7af55d3a4151f62017fdb8306ad7fa54`  
		Last Modified: Wed, 08 Jan 2025 18:13:31 GMT  
		Size: 158.9 MB (158929533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e759eafc98e241680c06249c4840e7eefd8752fcddd6dce674ba7677e4be4b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99918b3dc5d630cb74caba0d77317b7b6e34c30d3f7cb3aec6043c101bc7ad78`

```dockerfile
```

-	Layers:
	-	`sha256:b3beca115967b26d8d4c087ce7ae37e6ed3e2ccc236a503acac29a4cc1df69f4`  
		Last Modified: Wed, 08 Jan 2025 18:13:28 GMT  
		Size: 380.8 KB (380792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29be517c3c3f05710eaa9dc9ad26a57de5c582572b4373e7bc483c8876e5eb80`  
		Last Modified: Wed, 08 Jan 2025 18:13:28 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:da985919e69dd8fd61219c48dc75a3272ff2cb6a62ce3252d569258b07055de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160239023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec951dbe80f4507f577fa68781f902bd778c086eda42b4fc191aac491afcd29e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb382648ee83f84b1ded4599239b4136f3c9f49497c753e0796189149cb1055`  
		Last Modified: Thu, 09 Jan 2025 06:31:32 GMT  
		Size: 156.9 MB (156878491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a90a9302f3396b2b25a9a5fe5fc6ef03aef7695a34b2fd025b94b4a8373b6d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedc876bb8e3f8e6759cdc011cb410837d11d5169cceecd39df8e60d98141ca5`

```dockerfile
```

-	Layers:
	-	`sha256:40019c46094f6fb36789b3ac3fd03cca5eac73c10d45227432b36a3deae51bf4`  
		Last Modified: Thu, 09 Jan 2025 06:31:29 GMT  
		Size: 380.2 KB (380211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c80bb48c75e7d7244e3c29f70dcbed021fb69b80a3b2a22c2eb71b05d0e4c9ab`  
		Last Modified: Thu, 09 Jan 2025 06:31:29 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
