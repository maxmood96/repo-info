## `amazoncorretto:21-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:cf90aedc6d50ac2beafed53e2ebbd87e639815a9337db14c330cf518f212fc17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:11b647d48718c98acde3c74c62f7474e4a0da13a72d7d350e4cc60b4898ce76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162556337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704d28523de9b3f8b1f4925c4297dc8f55787e9a4b9d3c82e5ff35ca3c8067d4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfae79ac77531690e0b6594d0ae10373ac91d4a1854ef04723718a0087231f14`  
		Last Modified: Wed, 08 Jan 2025 18:13:47 GMT  
		Size: 158.9 MB (158930077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:544a69709a3f8ef04ec1b39123834c2eb05799209a429ce6379107b1bc952a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5c92fe3e855c18425203a31a309ed0d62c5b91ef50ce76cca6fece9d5a1353`

```dockerfile
```

-	Layers:
	-	`sha256:ae4e08f5e9b65f6c71fff62e63dccadccd98dd45d1fa321561789df6ab25d538`  
		Last Modified: Wed, 08 Jan 2025 18:13:43 GMT  
		Size: 377.9 KB (377868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b527e7ecaa8ce356511ff964fa0f06fcfaa04159549aac6802bf158c5e8a31`  
		Last Modified: Wed, 08 Jan 2025 18:13:43 GMT  
		Size: 10.7 KB (10721 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a53411d73dbb812f7c56c07e1d95ff8353375c6c6001474e0203a454d9ba6da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160966665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a9b4cecd6c384dbb7ddc055efa9692d4ddfc34e471e2aef1c52dc6bad77ab1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48724967ce110c0d18131c37a55114477ca16846a593d0d51fde70024c2aa44`  
		Last Modified: Tue, 07 Jan 2025 07:25:16 GMT  
		Size: 156.9 MB (156879979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f77c0b2e72437cf0fb14fd323e5944779dcb2b09d81464bca0272b4d57486aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 KB (388208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d89f257894df8008b58098e85084a7b2bf461ffb28fc794b2be70fb0f225db`

```dockerfile
```

-	Layers:
	-	`sha256:80159bf2f1c32f8d4f2c0848cf1f31c9fe988ea4e5bbde978dfffadff68fc73f`  
		Last Modified: Tue, 07 Jan 2025 07:25:12 GMT  
		Size: 377.3 KB (377335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:066187b3b64e5e90c1ab9a40eb2a2bc72806f3e1b115239e430aad3e15132a8f`  
		Last Modified: Tue, 07 Jan 2025 07:25:12 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.in-toto+json
