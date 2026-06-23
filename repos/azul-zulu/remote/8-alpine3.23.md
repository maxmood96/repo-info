## `azul-zulu:8-alpine3.23`

```console
$ docker pull azul-zulu@sha256:4bea4d3af8dcace60f6dafd2e7025bae4299a0dbf535f4428b6da7d7dec850a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-alpine3.23` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c6d25b4769f6cc29250731ef29c83203e0dc801a012700e67902b216c81e2491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60318794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ed112df611cc01bb4112757d19444ee03ec73cfd90a3b4c75a7be369e42a79`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:44 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:54:44 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:44 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu8-jdk=8.0.492-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:54:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Mon, 22 Jun 2026 19:54:44 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af784caa8b663070742fd77be0b6cb9cfe752184e290f6682892c7b406d1e3c7`  
		Last Modified: Mon, 22 Jun 2026 19:54:55 GMT  
		Size: 56.5 MB (56474373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4a4113af7f5079c6671522f8497960e1da03f7c4af33e5483204734a7681455a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2233bdb7de71a9bb938540390a0ca60179f4c96fe3d5216b6f2c22e9341949b`

```dockerfile
```

-	Layers:
	-	`sha256:4e1a5debe09ff7efed1ba75367f2b1505d88f55b7eebc381211388a3443068db`  
		Last Modified: Mon, 22 Jun 2026 19:54:52 GMT  
		Size: 7.8 KB (7790 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:5d4bd2e2632c04412db60777fd9700fff31d3c6720a30074f7ad02d2be59b108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59852311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0307e1fce05beff01ca81ba44f15c3dd818fc58fb9817a0deef410624420eaf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:13 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:56:13 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:56:13 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu8-jdk=8.0.492-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:56:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Mon, 22 Jun 2026 19:56:13 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fe509128e97703b97cbd40f126527217fd37516150fe7a06c1a93acb4a6957`  
		Last Modified: Mon, 22 Jun 2026 19:56:22 GMT  
		Size: 55.7 MB (55670451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:fcee00998e106123547d19fc58678e7e7bb7575d4632382490aa6c7f3373ff3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3914eddb5d1c19f8a2c7b8d3fbe427c0b9cbd4bf42142a6cbd2af9ad81cdb5e9`

```dockerfile
```

-	Layers:
	-	`sha256:534043e5c7a983ad671a4ac18569d3da1f9e8c94a16073d1ecf99a4e49b88bc8`  
		Last Modified: Mon, 22 Jun 2026 19:56:21 GMT  
		Size: 7.9 KB (7894 bytes)  
		MIME: application/vnd.in-toto+json
