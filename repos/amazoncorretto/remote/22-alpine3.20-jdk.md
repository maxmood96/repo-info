## `amazoncorretto:22-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:cc582c214ccab359d321b6e023b1e84c0c5f03aecc5dcd77e54a431055067d92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d3a84c441fb5e451b170fadb566b06d205699837c7739933b7fcbbb11c9072b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161220120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdef4db15922c50a67524a59a9a72a0c0463cb9261ffe2a16a918f40e1efbdf8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb01de3bfd5b3fe8a26d2ca773f9dc20aa11a2f723b2ef5c0a5589091fcd6cf`  
		Last Modified: Thu, 18 Jul 2024 00:56:07 GMT  
		Size: 157.6 MB (157596276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e810a77182660a8efc5f88db79f5e068028d910dd2ae1ee85ac3bf8337cb2f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445a6f7354f577dab8a1c93f358402071ec5b03e539ace0cb8354cd8b637bedf`

```dockerfile
```

-	Layers:
	-	`sha256:83d18f0b09618cd71429d3d3d154053895f67824f47025c054cb3dea7ece8b25`  
		Last Modified: Thu, 18 Jul 2024 00:56:04 GMT  
		Size: 379.0 KB (378977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:265dc82e1f2f82087e271937f6b96846ad00d1588dd24101463b1db29fee7b5c`  
		Last Modified: Thu, 18 Jul 2024 00:56:04 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:50d96af1da008ae08cdd4cb36476d59ca647f151c9adbdf428a6801658281559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159282692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598acf98423824ee77d8087c06086697791128fedeab71e4f57902317fa5b83f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0928dfd4eb881c902cc98e076f25b472614faa1a302120d50981b3628a023fce`  
		Last Modified: Thu, 18 Jul 2024 01:30:33 GMT  
		Size: 155.2 MB (155193892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e87c0e6777310d2d617ffa93192d847ab14a82edf042ff91e5e4b28230f44c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df963dce18ac4ea49becad2928ca28a34d59ca3f30330aa768b73eff6d94d293`

```dockerfile
```

-	Layers:
	-	`sha256:e23b9fa34442c2e1350c67c327922105f62b8f929cc9b6e5e5474392382815b5`  
		Last Modified: Thu, 18 Jul 2024 01:30:29 GMT  
		Size: 377.8 KB (377802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eabc3bb935450583a4fd4d126d185bf5aad17881f263693a893f672693900e8d`  
		Last Modified: Thu, 18 Jul 2024 01:30:29 GMT  
		Size: 10.8 KB (10823 bytes)  
		MIME: application/vnd.in-toto+json
