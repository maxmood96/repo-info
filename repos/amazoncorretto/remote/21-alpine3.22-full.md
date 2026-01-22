## `amazoncorretto:21-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:3e4341b367e0ad2003c1deb60ac0fbd703413c887e2b22f6eaf3109cff16a902
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6dcf459c38e037f4f00e4e5157313dd6ccd5f41fede45872be942ae3d3793410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165395328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd17cb21746b62519c1b57b5e4d59b5bb0b3939562d24037b6da5232e3cf526`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:07 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:07 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:07 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee00ece26505c4748311a5f8e8ca5154a9abd7d752bdc7e8696db901479c5e4`  
		Last Modified: Wed, 21 Jan 2026 19:56:00 GMT  
		Size: 161.6 MB (161592876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d5111d0f251a4b9a57f27c594d06626ebc9c86de82e14600e7257f0d65b89d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.4 KB (592413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a03621c6113bae0c60808ac29b0cb547259f7793f8a86d8407632fcc7f7e1`

```dockerfile
```

-	Layers:
	-	`sha256:31e939680eb8c232fe77782ca16ddfea27d7c83206095f4fa1c65cb2fac2c747`  
		Last Modified: Wed, 21 Jan 2026 19:01:23 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb908fc683850a9208dde2b86cc328003fcf2d0305c9bbfde57ef43a4454aa8b`  
		Last Modified: Wed, 21 Jan 2026 19:52:34 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d049f8934b767d8bdeac6f38f6b081d85bcf98c6c68ede55c0893cca8acd0511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163753023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164ec02c56b2181d14fd3abea5aa76d7bdc71bc56d405215ccd47760b5fe51ad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:30 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:30 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:30 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e776e1895744760dcbf55f09831ab018d04a4456161b3d6727d206ba7f1fd4e`  
		Last Modified: Wed, 21 Jan 2026 19:01:49 GMT  
		Size: 159.6 MB (159614954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0704f674c10ea2258c07924eccc60a35c93d712d667cc1d7708390946f6502a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 KB (591936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792ead86cf9282613b1e118fffb00e7384af3547b264238862b9a5a20b8bd97e`

```dockerfile
```

-	Layers:
	-	`sha256:d6f81e8aa086f999d869f1626fbbf46074b49212f6f7b032f3095774a5197eab`  
		Last Modified: Wed, 21 Jan 2026 19:01:46 GMT  
		Size: 582.5 KB (582458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4693a8b9f64c4d9f527cc954c15bd99fb51610cb41de405c33167a433273748`  
		Last Modified: Wed, 21 Jan 2026 19:01:46 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
