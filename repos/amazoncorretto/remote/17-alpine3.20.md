## `amazoncorretto:17-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:71b6626c9d3e23a0a8e5e841ce775eb803995cc11b86156e3674814d95320443
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:012144755b1629ce292d68ab83e72cb026f08a8d42001e0617c0d72a8f7ae222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149641055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d80430da5b6b612545c7b723df57add939aebd765a477f055bc2004d36abd3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:da4df084d1a052a879dc2b5ce94e8ef87a38771ad38c16afab545b4be39353d3`  
		Last Modified: Thu, 18 Jul 2024 00:56:04 GMT  
		Size: 146.0 MB (146017211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:12f198d5f9bc93e9757adcb5ceb8a3fd170fc8edbd8a09cc540325c797ca7626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 KB (388316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fc07428f6d3260475604bd92ea4958732f374699f9830c44644519dc3361b8`

```dockerfile
```

-	Layers:
	-	`sha256:ab3e29e50ed98b4ca2140054a12a064706013b2bb892eee0455f0d334607411f`  
		Last Modified: Thu, 18 Jul 2024 00:56:01 GMT  
		Size: 377.8 KB (377836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a538ab8a670ff937693dd00ddb590fb3479be8b7ea5674635672e8039ab6836f`  
		Last Modified: Thu, 18 Jul 2024 00:56:01 GMT  
		Size: 10.5 KB (10480 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c71c2b78b41e1b4fe1aab4c4f8c830f33d0d75ca35f8d0a9bef85d32bf202e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148438274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c59aaf962f12e6caef0b402d35e31c4ed624545cd8569894351b25123d326ad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:10c1e7c2f51d2442529d657bb6528774bb10bbadeb668b0deb30d9277fea1793`  
		Last Modified: Thu, 18 Jul 2024 01:18:05 GMT  
		Size: 144.3 MB (144349474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:77f208c29c5dec58b9d57bf1e5c11500719e77290ef6de851b7a7d7f9d6a5b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.1 KB (388130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa70e486a122cb03861d9577ca1810b3eca87abe9b1681ca5368f52e49ca7ce`

```dockerfile
```

-	Layers:
	-	`sha256:4a51b4973fe22d474704da001f028bdd06074970daaee0b0d3b9ddc48cabe928`  
		Last Modified: Thu, 18 Jul 2024 01:18:01 GMT  
		Size: 377.3 KB (377302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d95e2b80a810d767ee9a0759820ea5ee5cf78b5a33f450a2014c8c213db3c771`  
		Last Modified: Thu, 18 Jul 2024 01:18:01 GMT  
		Size: 10.8 KB (10828 bytes)  
		MIME: application/vnd.in-toto+json
