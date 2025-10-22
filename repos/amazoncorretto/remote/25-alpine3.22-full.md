## `amazoncorretto:25-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:e36ee3b9b909ea19d98d7325860bccf286ee519c50c8d33d91cfc47805ff0be7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:beea1e223c241ca79eace8cb1810a4e3b72881e42d822f4c8d55db42feae0209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184529095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b4be0a7e214902da5857c61527b70634b8509374c7572e9ffa0c0d248db6c6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab128989e00fb32e7cc11475c0cea15f816fd34dc340b51075556313a79ba88e`  
		Last Modified: Wed, 22 Oct 2025 00:57:27 GMT  
		Size: 180.7 MB (180726643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6903bde2768846dc2aa468e32a94e4965e60f46bc6bf68ee9a459b73b9612f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.2 KB (604161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8342a9e435fd0593e04a5f7307fcf63f922a1ce628e5ca60d4bc88d80d85bbc`

```dockerfile
```

-	Layers:
	-	`sha256:f9660672f42476424014bebe650cd0d963603120fb310c65f499ddefca0a39c7`  
		Last Modified: Wed, 22 Oct 2025 00:53:40 GMT  
		Size: 593.4 KB (593441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895d33d647af36277a46430d4a0e7ba76493419b3dcaf852baf054be6e657bc0`  
		Last Modified: Wed, 22 Oct 2025 00:53:41 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:015e38759e7789fafb78c2f6c8bf0b8bf0a52cc3f743f2d9ffe3c9f0c12d11b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182507859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde0cc8f84ea716a6756bb209022d547f72f1bb5578bed4d8a2cb38bfde10b00`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c5f3bb4876c6aad498a033c9c1187005a2710a104690543fede50be55452bb`  
		Last Modified: Tue, 21 Oct 2025 22:16:34 GMT  
		Size: 178.4 MB (178369790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1344003a9e86589705e18dbab9550a7aeefcbb152ed69969388b21531d01d57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.8 KB (603777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab30916bdd2c833640edcd970d94ae30f691f98aaf3732065d5397e45b4c8cb9`

```dockerfile
```

-	Layers:
	-	`sha256:e63f3fcfc02519eb2ad4f7035b5fce7d85afbfd7eed5c0195d30a46888065005`  
		Last Modified: Wed, 22 Oct 2025 00:53:44 GMT  
		Size: 592.9 KB (592905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a58520c3ea481376df86387663abcc81455c4dedad8e37428c18ee8b14ee3c3a`  
		Last Modified: Wed, 22 Oct 2025 00:53:45 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
