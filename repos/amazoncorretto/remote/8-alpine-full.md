## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:30e1fc11c4d61a75e03181a9973ecb950ff3c9052fb07cca7d7df4879352f21d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:90eda87a83a6d18dce7ea7d5b406e1f99072fc9d535cd4c1f1721d8bbfd132b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104597661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e618e9632be9706a3a5abc1d39adbaa2704763471287ac324dcf19f29dfb3f16`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:11 GMT
ARG version=8.492.09.2
# Tue, 16 Jun 2026 00:19:11 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:19:11 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:19:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:19:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e012724ee24b9e32ed4d9d059565bf64520db5852157bae5995083a5ad3c0a2`  
		Last Modified: Tue, 16 Jun 2026 00:19:25 GMT  
		Size: 100.8 MB (100751270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7b11dbc19ff0649b047566d5ac6693c97cc7722f70c4e442b5aa8b09fccc6116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 KB (258412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549b65924337ed19d81f6d47b5837dd89891adf926fe65b84108058a0f8b8793`

```dockerfile
```

-	Layers:
	-	`sha256:694030748d09c92d5f33e6266ab64ae0b138519727315cbca7473d49dc528d97`  
		Last Modified: Tue, 16 Jun 2026 00:19:22 GMT  
		Size: 247.8 KB (247760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a9714f96db7cbc3fcb965eba3448b19c16e751dd39704c850488f62a374aff`  
		Last Modified: Tue, 16 Jun 2026 00:19:22 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e41fa71a8524fd3b26c4544a3524c0d333c3f672352c7bd965c6702d1e771e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104727765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afad2766b86aca0905ab643baaba040acf3742d9c3f8b02762780958b31d2d43`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:10 GMT
ARG version=8.492.09.2
# Tue, 16 Jun 2026 00:17:10 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:17:10 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:17:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:17:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed179bb78cb0c8841268f0ec59940476bfd9103344c16e74580feeae5c187e87`  
		Last Modified: Tue, 16 Jun 2026 00:17:24 GMT  
		Size: 100.5 MB (100544728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:966e61d4d8a10ab7c1cec5f0729ee84f73d620407648b76f7c7df165c5f9453c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 KB (258094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8107145d74a632f40c13f0fda7fa234d189a4a5f176bbdd4be193d24bcd158`

```dockerfile
```

-	Layers:
	-	`sha256:2aafa2f04b4a8d84edfe44a44df0a9218bdf46998ac91fe79bcc5015e096082f`  
		Last Modified: Tue, 16 Jun 2026 00:17:22 GMT  
		Size: 247.3 KB (247290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a23bd7b6477acaae396504455b431e2f7afae47aee657222e46c931d84ca6c3b`  
		Last Modified: Tue, 16 Jun 2026 00:17:22 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.in-toto+json
