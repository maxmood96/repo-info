## `amazoncorretto:21-alpine3.23-full`

```console
$ docker pull amazoncorretto@sha256:29fb96b59042d9637e3d51ff3b423be3a88f17f530cbfb767a91d4199457f395
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.23-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:db360dd8ea76514c6fdf0f83e81ed0e50aed060a39c960b1e5b279b25b3e0520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165454639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282a2057f663bb962cf665b8d7a5c1c7f28192a60fbecba26dc7f9a54cb01b46`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:20 GMT
ARG version=21.0.10.7.1
# Wed, 15 Apr 2026 20:16:20 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:16:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71448d6e675e667655615378e72942f52abaf0b0bca7c6602dc0fbe187e2c587`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 161.6 MB (161590450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a4b215d1329b6daaec97c07f0051caecafa82079d3c5177548f9c2d4407d609e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 KB (593750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddf2ed325a1a3b8ea477c43df0648312477b82dc5e741690fd773ceab9c7911`

```dockerfile
```

-	Layers:
	-	`sha256:4f8889c9bf4b6a11363714543748d5caf6ebfc6bc135e0957135090080dbcf2a`  
		Last Modified: Wed, 15 Apr 2026 20:16:35 GMT  
		Size: 583.1 KB (583068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697997eb2d86178f580f6ecc2f2103d0a7b2d91194f9b310e71bb85fdf7e9583`  
		Last Modified: Wed, 15 Apr 2026 20:16:35 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.23-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1db14313b6892e13c0b4936496a91b7f05c91629cfeb3006d6c623cc2ecd5a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163815592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583bd874d902bb0d564f830ea11d98bc932684cbaa960b480256f21f73d0b28d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:46 GMT
ARG version=21.0.10.7.1
# Wed, 15 Apr 2026 20:23:46 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:46 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:23:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1cf2342851f77ea9f415795ed3cd8dada823b419d754c75ab485a6a7a59996`  
		Last Modified: Wed, 15 Apr 2026 20:24:06 GMT  
		Size: 159.6 MB (159615722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:46fbc6db1a27c38e1c94be769735612be6fe7a10ccec7b1eb223be79a5c90be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 KB (592719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf33b5c6e1d528e585219b3d454811d13e85300a8f8ca8e51b0d2ef5ccb25b91`

```dockerfile
```

-	Layers:
	-	`sha256:32ba323a1ebf0d834323be97b9542bca2ab6a83226ad0273e31698da061b0acf`  
		Last Modified: Wed, 15 Apr 2026 20:24:02 GMT  
		Size: 581.9 KB (581885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb4e6cba5aa5a3f1597aa51e0053172769d2a93c2c9e2a3b40c09a9ac220f51f`  
		Last Modified: Wed, 15 Apr 2026 20:24:02 GMT  
		Size: 10.8 KB (10834 bytes)  
		MIME: application/vnd.in-toto+json
