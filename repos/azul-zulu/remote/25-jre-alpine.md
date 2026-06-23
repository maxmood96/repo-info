## `azul-zulu:25-jre-alpine`

```console
$ docker pull azul-zulu@sha256:472c38bb0d904b7076c147e252236ed5c47338c4357993f07a693564a7548e45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:94e8478bdb704298a5b88c2f9986b903ab19a8ddea81bedb260b852165252c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90272415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e34ab5141ce9686174efeb4cfc5cd281986ece3b0a4fdcdd88417260cbff73f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:52 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:55:52 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:52 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu25-jre=25.0.3-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:55:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Mon, 22 Jun 2026 19:55:52 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d042657c526b58bc2d65b2c6ce5d9e0a4da7c5275e1505f19c67bcfc40e841e`  
		Last Modified: Mon, 22 Jun 2026 19:56:04 GMT  
		Size: 86.4 MB (86427994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f9851aa0b8ba8b0c8b196202b256e6434637fec6000ac57c1802b4ae7aa88ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b67f9576b7588b95cad42d9cc5612c1cada467bd6f6f0e523d010aa3cde786`

```dockerfile
```

-	Layers:
	-	`sha256:9a8e1b01cc3e56a760c32aceeb01af91f6afdf8b5b9bccc0ae7a31960b4aa2bf`  
		Last Modified: Mon, 22 Jun 2026 19:56:02 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c24c08a8604582f9b20f967feb946d3eab884c4e780a9a6a7b1993fb46b4bc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89473647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4039d13ae648c70f4cee55fe92eebeccca0e1be64d15630221f939a830a58ab8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:33 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:57:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:57:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu25-jre=25.0.3-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:57:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Mon, 22 Jun 2026 19:57:33 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22e9cd7dbf87d635ed6b5ec206ae910cb3b84a4d56c4f66450f971fe906de6a`  
		Last Modified: Mon, 22 Jun 2026 19:57:47 GMT  
		Size: 85.3 MB (85291787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:390b947e62352d3cfbc989405ab86df3495244b424ecb2f319472a4941bc0c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7891a141189b0bde3eb0238e54556a9b4323acbdadc57d24e9eae68eea314413`

```dockerfile
```

-	Layers:
	-	`sha256:0eb7e39dc79bf07466a6e6ab34fdcdc7a0a7202c427bbe1218192b44fa9964c5`  
		Last Modified: Mon, 22 Jun 2026 19:57:45 GMT  
		Size: 7.6 KB (7572 bytes)  
		MIME: application/vnd.in-toto+json
