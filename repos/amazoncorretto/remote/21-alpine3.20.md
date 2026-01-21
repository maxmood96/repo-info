## `amazoncorretto:21-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:5dcca06615a9a48039aba12916bd6aa1c36886c767ae0004df1754f1bacbb071
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:70f65a132495b3220649b9d5b37ddb7758ca86b986ec5ed853b27571ab858cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165179796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b12c220d55541cc6408c80771359ba21d16d887fc1277fa28f2ca7963c4793`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:06:44 GMT
ARG version=21.0.9.11.1
# Wed, 05 Nov 2025 01:06:44 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:06:44 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:06:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e74ebd25ba73269f97daddbc903dfc2ae9ac594d44247fe19659fb4d949863`  
		Last Modified: Sun, 04 Jan 2026 04:59:13 GMT  
		Size: 161.6 MB (161552740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:924443bad45671a1bf9aa6ff02592edf58aa33817e5964c30fafef3d91c639ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 KB (589925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d19bd3f6b9239e90f089029f4351fc2883227982cd78936af7cae5f17b8d1c`

```dockerfile
```

-	Layers:
	-	`sha256:4aeb4d1420d5b0da0a4b392106920c92726a55bad6bd2e5e7ba76ded91127b34`  
		Last Modified: Wed, 05 Nov 2025 01:06:59 GMT  
		Size: 580.6 KB (580553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fa0777c4edc86fd6e424f748fedd85f0e2bcb8da8d1587cbb77ecdd3e9a45a7`  
		Last Modified: Wed, 05 Nov 2025 01:07:00 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:05440052d42dc46a83083c1b045ba84e6587f0de2c4f6a84de9d0d5bfac07ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163682875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21deef0a981a12777c9c73770071b37ad60d134c9d3d08f0899c0ced924d3f8d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:21 GMT
ARG version=21.0.9.11.1
# Tue, 04 Nov 2025 23:16:21 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:21 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07528eb5340a5a340529e0ebc32cd5100f93c96be3c3720997e141144c52ad92`  
		Last Modified: Mon, 05 Jan 2026 09:02:47 GMT  
		Size: 159.6 MB (159593498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:79b73175aa4331c038a658895fc5be59d5c723cb4081b455f6f1746a564dadca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 KB (589448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c2bd98db9515f19fc4bf9fc80d0b9e5a8a7ef34fb7ea4d253ec8d5fe540923`

```dockerfile
```

-	Layers:
	-	`sha256:c5cb07816d218d295937899e4714f28f1ad88cb44dd5406ca47b2ae93e2cefc1`  
		Last Modified: Thu, 08 Jan 2026 14:44:27 GMT  
		Size: 580.0 KB (579972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77cc08ab6b1e4efd853be0cea7e1b73f15330fee8f0ea82fc0ce43501b9cf683`  
		Last Modified: Thu, 08 Jan 2026 14:44:27 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
