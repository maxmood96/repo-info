## `amazoncorretto:21-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:6df8ac27bd5c14cc9ab9e27047d80d27734fb342bdb7b3ffe38469aa11d66fbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f84803a0d11c81bd9fe6c24a687b01f5a6bef1ce6ceabe9040b47f3a09235348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165205219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68add1745a27b7c2dc9752d4a6bfab6ad27208b6ec7e30224d0bcadf8d5b8bf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:59 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:00:59 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:59 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:02:45 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b58eba4c05cf61455ef297f9feb5b8d80ea42b95f9b4c15cfa7bf310e29b074`  
		Last Modified: Wed, 21 Jan 2026 19:55:09 GMT  
		Size: 161.6 MB (161578163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:41c597d4a0680b6c45cac3b0cbadc86ef84194afeb471b622f4fff62effab7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 KB (589930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057ca182041d12b8fd5ca888017f9e120c8b41c09293bfc136f68f4b75957aa8`

```dockerfile
```

-	Layers:
	-	`sha256:5ebae77d8cba9bcb4495eb333dce08317e7049d3810ed7c7bcaf587033637f51`  
		Last Modified: Wed, 21 Jan 2026 19:52:12 GMT  
		Size: 580.6 KB (580557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c2d94fe0fa9f9ab132447d51a9985f744b9badd35d03b60888d72fcc3452a94`  
		Last Modified: Wed, 21 Jan 2026 19:01:13 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f5b66789281dbc27256df3f2e53dcfdf4e554e3e7d796309026a79b1d14fc7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163708807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5e9912c981cc17e5c76823ed8ecc0a772407ff5a9ace73b197552f1258b458`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:22 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:22 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:22 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aad94969b530bfd5e73fd625a447fc905ac466cd49bffcab6a5961d341c6f49`  
		Last Modified: Wed, 21 Jan 2026 20:28:08 GMT  
		Size: 159.6 MB (159619430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c85bbec49a36e54905e3ee88701242930d691b8b7e9b201a4e1c338633d5c101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 KB (589454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6727b35482f303d6950bfb557e2fa22046aeba65c17e7472d0894996db49057f`

```dockerfile
```

-	Layers:
	-	`sha256:9677c4346f88197ffb2098711cd97c18e2e03e7a882eb1ce9692456df6578805`  
		Last Modified: Wed, 21 Jan 2026 19:01:38 GMT  
		Size: 580.0 KB (579976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3963b1447d53f64f0da505daee522840db0fa0b710feee6b2d97ef52f015a416`  
		Last Modified: Wed, 21 Jan 2026 19:52:18 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
