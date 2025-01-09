## `amazoncorretto:21-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:dae256c13354a428f31f05dc1a2c95cd38501822332aa09b7c851dbe61d3b704
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
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
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
$ docker pull amazoncorretto@sha256:99ab2b6d36310049f2a5a4d758545c4a7c6a332d5a72b204e9aabdd8d1bc715a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160230443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0698a2f6072b1339a4ba57b7ac691cc03bfb04a27c2a17f605d992cda0b27eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Last Modified: Tue, 07 Jan 2025 03:03:15 GMT  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97daba5a9b8a7f42a3fbd1580bd00dac20183704cc8aa4747fe56af7f9d6bdbd`  
		Last Modified: Tue, 07 Jan 2025 07:24:44 GMT  
		Size: 156.9 MB (156878495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61c62545f47eee2fc445830d82aff882b44f8358801fd2533b5d6af153aba993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eeb8d8548278e135823204b03ab3dd2daeea2f690d54d6e5db8f25a0357ac8e`

```dockerfile
```

-	Layers:
	-	`sha256:74c0f0847ea162e1266f97ef426953f28bc1ef0cd359c1623d7c464d76595281`  
		Last Modified: Tue, 07 Jan 2025 07:24:41 GMT  
		Size: 380.2 KB (380211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba7989df23d55b31fbad9aa3af9586aecd7dea620dc8f35ba99a4a94856d556`  
		Last Modified: Tue, 07 Jan 2025 07:24:40 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
