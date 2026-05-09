## `amazoncorretto:8-alpine`

```console
$ docker pull amazoncorretto@sha256:3c8d804d0f358481c40d1d0b387f8e4001987e8d6db73cf56aaf8b435eabba9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e6c3325a879e1fcb19249e9c908c9be8ee4cb7f3fb32b189703db24b60d73eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104615606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c846fffbbbdef9ba65d3b9b2c7789cd60033801e6c0b277f8878395cfde987`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:58:42 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:58:42 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:58:42 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:58:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:58:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb78799819c2ab46aaeea7584a6e63546f8614eabfc576be9cb56de175814cb8`  
		Last Modified: Fri, 08 May 2026 22:58:56 GMT  
		Size: 100.8 MB (100751417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e776aa65f25f16270dcd486d1c96ab0334935d933b4192740e1ba9f5d75b5197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 KB (258346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56190a5704d9360a675507eb5a30a3371dbcfdfbda33c15b5efa110677a0564a`

```dockerfile
```

-	Layers:
	-	`sha256:5f35560097c02f533ba6b8ab9e7bdae5c0b59a448e05d943aeb45d66b205be93`  
		Last Modified: Fri, 08 May 2026 22:58:53 GMT  
		Size: 247.7 KB (247693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5676571d72c5119e8e28426d489d89cd532f2855072788f8d31e685024ecacd4`  
		Last Modified: Fri, 08 May 2026 22:58:53 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:908b915322af666fd22120b8ddc5e51f103ae6a52e85772a0b6c57db52bb8e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104744558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f025e5b707e83cda626c7a34b3c9cebff685d85d9b3f3640e67611a24e6784`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:48:37 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:48:37 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:48:37 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:48:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:48:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2b2750547d1382e8902a58f482ede14d5484098b6dbba6954feb54a9e3dbe3`  
		Last Modified: Fri, 08 May 2026 22:48:51 GMT  
		Size: 100.5 MB (100544688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2293154881356810d6990e52a9a0ad94fb487b7102ec5374679cafa3651cef7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 KB (258028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58dbb894e2f8b813b619caad37dc5a34b4e5a27feaa2caad7092666b0ef957c2`

```dockerfile
```

-	Layers:
	-	`sha256:fbd6bfde2df3a690e6294cef5e0e9bffae4785d6651a177fdb7903aa98706aeb`  
		Last Modified: Fri, 08 May 2026 22:48:49 GMT  
		Size: 247.2 KB (247223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24efcf8fa3a6abc7b84a69b86fa4c5004901317ffe851c29922d3e1c2838fab1`  
		Last Modified: Fri, 08 May 2026 22:48:48 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.in-toto+json
