## `amazoncorretto:17-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:86ae67f6090da68a28b28b596049b4966c85fa5d55930b4dddf1eb79845be994
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6501b449072630aa320e38ed86e992f8b49a645681b6a4947773e88e0d8b36d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149649828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5eada06eca2477f2d4b35e8413179280488068509fba78c49bd531fc5dcd540`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=17.0.11.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=17.0.11.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148814c83486f9e7b92433082015b4ea4eb42a058cd97a0ea51b1839ab617e1b`  
		Last Modified: Fri, 05 Jul 2024 19:56:25 GMT  
		Size: 146.2 MB (146235934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0b3e006f1274fecabd654945f723488bb78254cb07750ef61ae2d66448850198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.3 KB (385252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd5926d99715a4d54bd4595195e3da61cd6de65153a89dda58336ede9c7fc77`

```dockerfile
```

-	Layers:
	-	`sha256:4d342686fb188fbcf017cd8bf1a28cb59b9a0773f4722a6cd27c5082204c844b`  
		Last Modified: Fri, 05 Jul 2024 19:56:23 GMT  
		Size: 376.1 KB (376080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39aca53b14fe13b8b18fdc7d351ae618548f3b097a6ef4b859ac68c133f69072`  
		Last Modified: Fri, 05 Jul 2024 19:56:23 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:67cb96962e702af07c143e8d248b89dfdbd137a40773eb22178fa8e3a42606f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147632818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c2f79b9cd595847ca6b8f25663579fb1a103b14f3a1232aceccb0c2a4f3ac1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=17.0.11.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=17.0.11.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa928b89feaf0fd3b1b4f53d8ad2e0054ec6622a320fbcfc6aa48b106e37af1`  
		Last Modified: Fri, 05 Jul 2024 20:19:06 GMT  
		Size: 144.3 MB (144294869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fedf18915d6f1d25be44c6a2050d52df9d5058dfe4f7f59c6fde45bf8c1a9cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.0 KB (384970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d797801a324f1791ce1862bb6e261e4fa1b9ec176da0fcb348eb96580b1605`

```dockerfile
```

-	Layers:
	-	`sha256:71654530ef2dba20554e9aeb3b0badcc36ab1e5556c591b1ee8e24bc3ed1ecb7`  
		Last Modified: Fri, 05 Jul 2024 20:19:02 GMT  
		Size: 375.5 KB (375498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3fd4a9e0f65414257ad07621cc78d0e387bd685033a8fa723f8569613b405b9`  
		Last Modified: Fri, 05 Jul 2024 20:19:02 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
