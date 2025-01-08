## `amazoncorretto:21-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:b58ad6dd59169921e674ab8704fd71e5b4f6444e6a1490d0354a4561737b7151
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9fdfd832bd43e0b64c9ae4f4bf871fec78fc6c04726503e9e093ab0d7a6c1cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162544108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7efa4b39a0a0851b35722b38e1e7326d2dcd8999af30952dcebf30377ee0844`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 23:53:52 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5eaf144fd07fa577b4bbd9fd1e553976ccf28625182105d96db8000bd93129`  
		Last Modified: Tue, 07 Jan 2025 04:20:14 GMT  
		Size: 158.9 MB (158930109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6b217245ee349675ca86c8203706aa4a2c1b0907d6ed7870d8fa7c85f75d3218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bec34ce036365b719f16b6417cb9b5c9ceb8af1b918b13b9fa22fd999a98ce`

```dockerfile
```

-	Layers:
	-	`sha256:75eb83ec0f610e95712182b3e0feb3f33fe10158bc87c11a8064170fb3d2c6a7`  
		Last Modified: Tue, 07 Jan 2025 04:20:12 GMT  
		Size: 377.9 KB (377868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f80665c783961653698f491e2d024f478d8dddc142f8d6b3f3b76eb04ca8ee`  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20-jdk` - linux; arm64 variant v8

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

### `amazoncorretto:21-alpine3.20-jdk` - unknown; unknown

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
