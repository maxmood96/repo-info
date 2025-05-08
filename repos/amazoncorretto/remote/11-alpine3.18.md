## `amazoncorretto:11-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:7ffa11b950a26fe42f6244a36743ebf97fc873a33e5b035caba75567d6a556f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4c9236f1f5e978dbe652a5402c93e60de5c4a4e739baf6755487533e643acc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145364239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbd256c6d687aa08ee74c010f4e7ef21a08f92f08dd095f6462df6a7f44f169`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:03:06 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:03:06 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 14:36:09 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6e54a085ed969e8c571b3376dce7bb89d038ce78636e8ecff4f46e00636ecf`  
		Last Modified: Thu, 08 May 2025 17:05:36 GMT  
		Size: 141.9 MB (141945830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f0ad143f7c6efd93903a975bbe585f0d92ac373fd1153e720c4d3b624117bd8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd8e3ae55c72a050d7e2256b89093aa247f50e2fa9cc7634f597492939f99ef`

```dockerfile
```

-	Layers:
	-	`sha256:dee6a09c444c01dba6d67a8d5c1a238a1bdb0fddfc3711d1e37829eaa1cfec7d`  
		Last Modified: Tue, 15 Apr 2025 23:55:38 GMT  
		Size: 387.0 KB (387034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cb6210c992b8dbd7fb852293a9cdea2b32008cec0127e30ff7748d2736c3a8e`  
		Last Modified: Tue, 15 Apr 2025 23:55:38 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9e7797a702091d212822177c8e2e5ad45ca60f548d958054761aa7798cb1fc1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143409977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a022d7319cc782a6c4e19a546de8fd0931a334c20a02d8b18a9184ea858baf01`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:03:06 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:03:06 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 14:36:47 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f336e6c1c6647569dfc4a1fdee3051271972b381330018fde579082f2864ef`  
		Last Modified: Wed, 16 Apr 2025 00:06:00 GMT  
		Size: 140.1 MB (140067320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c00826ead95afa6c2ed8997b93dd339b90bacf6dac1546596cfbb02bbf8827aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 KB (396611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967d8d8f0c287b585000f70ac753018039c0189953180b2a75a3bac33b8c9f41`

```dockerfile
```

-	Layers:
	-	`sha256:baa71a9247ced9d9e0ead54f584f6800261b627ea6c1fe6b8c03eb700da4107d`  
		Last Modified: Wed, 16 Apr 2025 00:05:56 GMT  
		Size: 387.1 KB (387090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e776de8e22573fc56b36c6cdb1a81b280ce03486cd121ce35f0db7cf876a82`  
		Last Modified: Wed, 16 Apr 2025 00:05:56 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
