## `amazoncorretto:21-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:330ba2c26a460c3eef3312fb98a1048f63b944fc62ed7cda12b3aecbbb48b705
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f3e9cef8e99e55bae620641a79fd4cdf361c6911862c0fa304072d88e6739472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162554041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6876e84cb6b1455a4b0963623b037af045271f321104d2e067f1799ba48fc963`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf047165709bffe3a3624e99cceb7a7bf696113e52c26ecebfa07a01fc0ac18`  
		Last Modified: Tue, 12 Nov 2024 02:12:35 GMT  
		Size: 158.9 MB (158930137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:083d35fb866df23d93435ec1a4f5faa49a3e82d10453fedc8c697b1ebbf2c0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 KB (389212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b9d22bcf0c885ad05a787e9beacd46d1b9e8170fcc93670b3f9ce99aa331f`

```dockerfile
```

-	Layers:
	-	`sha256:77f33bbb6f8ab0f0f4cb092e8fc9e0c2b1903c578d0220d178f7757012fe825f`  
		Last Modified: Tue, 12 Nov 2024 02:12:33 GMT  
		Size: 378.5 KB (378492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a499727f0d67590d784b2d513234d79ca2d194c746255654f24fa6d6be0b4ee6`  
		Last Modified: Tue, 12 Nov 2024 02:12:33 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a2d3fe4a361e5fa38b2ae3e326d52e23b402b8d32e34378e874e6a6e5b07ffee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160967656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3553bbada4ff6ce37a2535f7299c9c6c814843d32586a09682e2a02bda5241e3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caf0a1ffd86bb63189c72afc5447c3e4d36fe0f610c98f82c31d967535a4628`  
		Last Modified: Wed, 16 Oct 2024 18:38:39 GMT  
		Size: 156.9 MB (156880010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0f1ef3e202a5b5bb42b002cf939dc1fc50559d9f50393d25d285dc644343aad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.5 KB (388524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5c81b4b775f29a6e4d75af3268aab18406df7ecd8e44673fe84726926a9c64`

```dockerfile
```

-	Layers:
	-	`sha256:54813018254face0db4d101b5d626415e10b8e6f3b04eda9081494613f9d7e81`  
		Last Modified: Wed, 16 Oct 2024 18:38:34 GMT  
		Size: 377.9 KB (377865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972e6cda40d6cce8ea80ff064abbe0070d6e1953691b7c5506dd0789a4c000c8`  
		Last Modified: Wed, 16 Oct 2024 18:38:34 GMT  
		Size: 10.7 KB (10659 bytes)  
		MIME: application/vnd.in-toto+json
