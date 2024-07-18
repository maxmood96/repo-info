## `amazoncorretto:21-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:16a4f4dd750278036280b80b53b2fb5869aabe7312c0de260b3c458e51ace598
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:12b54a9187338629b343ce311ff539fdc4c38b57fcb2f99ef40b1f638f5d8725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163139684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979c24805ec53f0589cdf9bcf9172b7e8bd45ce872bff2b5ebec51257922c25c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 20 Jun 2024 20:17:10 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f327ccc21d5fda8fa2f94ecc33ae5aa5273cafb80825fc5445a182f080390785`  
		Last Modified: Thu, 18 Jul 2024 00:56:04 GMT  
		Size: 159.7 MB (159725790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:56adf1f115e6a40fba5185d802b7e81d6923c356ed84a1d37968f8c63cbd2feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e00e3f38059f4df36aec501f1916bd38df43076be31d6a80bd30b3b13030e31`

```dockerfile
```

-	Layers:
	-	`sha256:09072ce7123ebd9e86df121b7d6835478e1e2fc3280d183ade1e6bc72c38dbc8`  
		Last Modified: Thu, 18 Jul 2024 00:55:58 GMT  
		Size: 380.7 KB (380653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7601519fb6636e74e736dbc55d7c3b53b9a43958029f945a3b4b65acbfa0e52b`  
		Last Modified: Thu, 18 Jul 2024 00:55:58 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:25a61be200f4a1bda422f030d357c79b1e69063bdd9e3aafd5e1f0ceb8b31326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160819618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8857f57b5532c4a2ca5b8b8bc25c0607f556c264ce33ca1af5307250abb26979`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a08b2c964d3b0a139f75671e05d36fefe3932b0897835cb628e78ca7b62739`  
		Last Modified: Thu, 18 Jul 2024 01:23:08 GMT  
		Size: 157.5 MB (157481669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b208d588ea7ef557c9cd1a70de242809542aaee0cee63567a31d1fc1c4d78523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c1dc9da952f2cc75dcd992421897318ae537bb0631471614da86b169bed512`

```dockerfile
```

-	Layers:
	-	`sha256:8a7585c73f48d4431f7cbb5b2e50cf4aabd41703768091a75601166f6c0b4edc`  
		Last Modified: Thu, 18 Jul 2024 01:23:04 GMT  
		Size: 380.1 KB (380071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8c6006a890f3d46e348e18c1627e67f69069e2675f1db96802ec56c1f92487`  
		Last Modified: Thu, 18 Jul 2024 01:23:04 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
