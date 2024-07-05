## `amazoncorretto:8-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:19013d5253ea5175323b63532ec3243daf5e5616377ce07ee4c5343ef16ec616
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a27a9beef0e35045d1f1a6bfc175c901f723c26846d754d3433cf08366285ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103585023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042492707f79776d4fd504c6648daaaf2484a150f2cab6906fa6539156234a3e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:e99da11879cd6814b7acc18fa9f5fcb6edd8bfa3794dad2ce061eac5f5670fc2`  
		Last Modified: Fri, 05 Jul 2024 19:56:07 GMT  
		Size: 100.2 MB (100171129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:883d774e1be0c23fde08b597d0120efff5aff7139c696e393207786dc3875237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 KB (247850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b264466cdbacc4809dc82804d0572e5f860c451f4bb0711465039ee3b8e14b`

```dockerfile
```

-	Layers:
	-	`sha256:285f1feb0ef462a4626e5a91eb420b1d2b88a9232f20a68e328f83ffa50e2968`  
		Last Modified: Fri, 05 Jul 2024 19:56:05 GMT  
		Size: 238.7 KB (238698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a460a29ef516557d69ac2717af6d3c1b9f28127b6d83ae29491972125ff3c7d9`  
		Last Modified: Fri, 05 Jul 2024 19:56:05 GMT  
		Size: 9.2 KB (9152 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f78cc311499c6e9e7255e2269a291a4fdc25a0e80323fdfab22a40bbe155e8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103156827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552f6b1b451f538aac898750c83811f66f5283390fafac6efd3a1237e0677208`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:d22f69d8056873041ff99e1985c1f18e739a33f8839105764806614d4d903e92`  
		Last Modified: Fri, 05 Jul 2024 20:01:14 GMT  
		Size: 99.8 MB (99818878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1428a1c221196f41d7dfc254e8ea775cb4749b3fe13f3555168eef4510e02342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 KB (248282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339706a342064a573d598bfd7fd45fbb66093d527684526b7aaa79d0e9e9d164`

```dockerfile
```

-	Layers:
	-	`sha256:98ecb0f6bfe72c007bbc8825d6e13d86adeb55f8cc748d184d2675ef2fb33b50`  
		Last Modified: Fri, 05 Jul 2024 20:01:12 GMT  
		Size: 238.8 KB (238830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39d5151f12bf200822d33fbb35a9afe879d0966f35fd8cb4b164d7ddcc05d073`  
		Last Modified: Fri, 05 Jul 2024 20:01:11 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
