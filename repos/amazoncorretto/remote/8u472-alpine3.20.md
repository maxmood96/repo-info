## `amazoncorretto:8u472-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:5135bd10b96570c969c95f37a030c0437c2c4f8fbaa162cab6b882387e8608ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3a7659cb75fa47ecce7c5ee25bf079ceb29e28263d303b5248cd79728cea1183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104384970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e839276832294da2eb289b6c077def09d3753a12dddbc1ff97c2d510a6928c05`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569bf71b64a6fd82c0ff9c288ebe5648da251e60c727ea6d7c880c2fbd536665`  
		Last Modified: Tue, 21 Oct 2025 23:26:24 GMT  
		Size: 100.8 MB (100757914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3be3474daf8b16d620765940bab5c004b205c2055ed57c0603d33777fe692a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 KB (254424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd0b10442a68a61e77473772132570e12f509a76aa76b4966647e3cf037b635`

```dockerfile
```

-	Layers:
	-	`sha256:508c53cf21972aaf758ed68ba5413f0d4fd4b7aab89fd51ca7bae8c81ceab8ca`  
		Last Modified: Wed, 22 Oct 2025 00:55:58 GMT  
		Size: 245.0 KB (245026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666ce8c59d71e41ade2825938c1da45bb14f8e05d4aa1a57ae96fc97d0aa902f`  
		Last Modified: Wed, 22 Oct 2025 00:55:59 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f833c77942070d77e98d9a894bc8945327c876fab95d8ba10e097983bdb9956b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104622743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72cda48d501dc8cd58189332a62e6da294f31918218021920a3635d0dbdca45`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Sun, 07 Dec 2025 13:54:57 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf37328f774b636efae1dcff8f5566a5444c0530840cdb37a514e3d029e3527e`  
		Last Modified: Tue, 21 Oct 2025 21:49:30 GMT  
		Size: 100.5 MB (100533366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e1c697d5b3f3a11ccee1cc281fb14cd62ad19d74498fa8a8db792e1c8624428e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 KB (254659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cf79a5d769b91c5f79bd4c6b5c2d4ea677d66cf7b41a5238b9200ebbc65ae8`

```dockerfile
```

-	Layers:
	-	`sha256:75964cf71edbb8dd270ce4c07e21a5ecbd870412ffa1beac88502359013a104a`  
		Last Modified: Wed, 22 Oct 2025 00:56:02 GMT  
		Size: 245.2 KB (245158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98abcfd591590a8b9136e633fe72c10bbac7c8e11480082aeec97defd6a6973d`  
		Last Modified: Wed, 22 Oct 2025 00:56:03 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.in-toto+json
