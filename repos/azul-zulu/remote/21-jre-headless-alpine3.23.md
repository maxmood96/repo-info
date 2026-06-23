## `azul-zulu:21-jre-headless-alpine3.23`

```console
$ docker pull azul-zulu@sha256:f40c97aeb725d3af2d2f854a4550efebe24a9604079599bd2e398b5aa759dcf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-headless-alpine3.23` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6a86875ebfe9d4ffbb5b512fbe0c6427a41b855077c125c2ee3250197dc028e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72688311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112b794610e783e59ae303ba340c9937b587e2cbb5db3f6e02fbeb8369066b89`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:33 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:55:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jre-headless=21.0.11-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:55:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Mon, 22 Jun 2026 19:55:33 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825d65cd2edbb32c7fd7a1924e14860c1398404cf83b8ae38c83c3223efe09e4`  
		Last Modified: Mon, 22 Jun 2026 19:55:46 GMT  
		Size: 68.8 MB (68843890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:dd1f609bfd40f53d34f9eb7b93fb049c41ff6ce63ea385cb21705b4d5234b2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc271bf34df2d4455cd6691c1ceb1343c67c70b70f2ee3bbc687d5d3bcae500`

```dockerfile
```

-	Layers:
	-	`sha256:adcd3e975d0c62f5ad5f100f5b61437b0600fcaca699d6fc0759ace492e22e54`  
		Last Modified: Mon, 22 Jun 2026 19:55:43 GMT  
		Size: 7.6 KB (7576 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-headless-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:b5b03b87c9d9794343a57315fc22ae2e32d91efe1e193a0ba0a1db709b2c4740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71726923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a6b65d65d5a84230d28983cebff9443e8351d57ba78a0133fe0ceae4df9ecc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:12 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:57:12 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:57:12 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jre-headless=21.0.11-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:57:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Mon, 22 Jun 2026 19:57:12 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a3baf466d6e06fe7d6455638c572d7e7aae9eba871013817413f5c62f51da0`  
		Last Modified: Mon, 22 Jun 2026 19:57:25 GMT  
		Size: 67.5 MB (67545063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4c34e7d41ae833684f1db4838cdd22854bbe1d46ef6364f61259476fae41822e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79287938bcdde4bb46b2b75a26023d3c55aaaec57e5e65dee9be2200934a93e`

```dockerfile
```

-	Layers:
	-	`sha256:d1b6136b07551f85c56b39e85a11d346eb8247c29d95ed3ea7674689db08af36`  
		Last Modified: Mon, 22 Jun 2026 19:57:22 GMT  
		Size: 7.7 KB (7668 bytes)  
		MIME: application/vnd.in-toto+json
