## `amazoncorretto:17-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:985db251466ef9e58bd74289f7365b94f0750b7e2e9fc0e7bfa5f9971c137768
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4f98cc62c7f5b0def67eb984c56a38e9a36cd2a30127e3435c3b3d5fb60bc070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149263291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a61f816ec7faefe39f92691f5373382fbfa8a093e76a51ca69aa7647d935734`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacd015f7c1503cd701121ba71569d133f255bffa779a04e5fb151071146062a`  
		Last Modified: Tue, 07 Jan 2025 03:30:26 GMT  
		Size: 145.6 MB (145649292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:49810913f683c793adb85793f81cc1c3f2ee14c523ea029c5e5df5ecf05c1229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.7 KB (388702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad01f99b7ea88ebd65c34d89f16eddeafcc10c143209d44b26f0585c7117677a`

```dockerfile
```

-	Layers:
	-	`sha256:3ae9de9d7647d5c1ec5fe380c9fcaf873c3277c257a78b9566769d7fbb2a346c`  
		Last Modified: Tue, 07 Jan 2025 03:30:21 GMT  
		Size: 378.0 KB (377973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081da88a3dae1b10c362ad5e9956438e8cbc31d21dbc09933505e7e6fabfcd40`  
		Last Modified: Tue, 07 Jan 2025 03:30:21 GMT  
		Size: 10.7 KB (10729 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2245fe480c676dad214e688a93c9befeee014ee1384ab28256a4b2d2e7f4d0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148022470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a0988f94e7b721472ce7e32c585a98b0a013da53a92b0bcd61248b1fe9a544`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0052ba8722e483dc5f301c56915d49a286849a6e3e240007b8bf07dadfb85bb3`  
		Last Modified: Tue, 12 Nov 2024 11:10:25 GMT  
		Size: 143.9 MB (143934744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:224a3b0f0d641d7710bdaa33421613a00d59c2449798d606f53aefbb971daf02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 KB (388944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487202aaff303b68943e9237740230c4149647b97528cb4de72f488cec5d2a3b`

```dockerfile
```

-	Layers:
	-	`sha256:84f7980d7f09c51d8b542b71834e0a4db5db264cdd55f75330039a2f3ae389b6`  
		Last Modified: Tue, 12 Nov 2024 11:10:20 GMT  
		Size: 378.1 KB (378063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389d5cd1e7b33737efb9b40d9215c48cde55ac1b7df0f8066c765584e0535717`  
		Last Modified: Tue, 12 Nov 2024 11:10:20 GMT  
		Size: 10.9 KB (10881 bytes)  
		MIME: application/vnd.in-toto+json
