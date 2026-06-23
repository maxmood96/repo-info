## `azul-zulu:11-headless-alpine`

```console
$ docker pull azul-zulu@sha256:28d014f576ff7aa0bcd681ce9ac1d2fc419ec2b04da910c402e9eec0981301b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-headless-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:5a4765644964cb32fc8346306eaf410c4fe6ac7aec33c8775a685048b832631a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144823963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8263e15ebe05afbd6a08c91af7dffaf99b6a049325d0e62179d907ca08db5b49`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:03 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:55:03 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:03 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jdk-headless=11.0.31-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:55:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Mon, 22 Jun 2026 19:55:03 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:55:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc7c4ee5e8b732236e801d2f71930eae6d45ad0b5988ee42368149e12a27d65`  
		Last Modified: Mon, 22 Jun 2026 19:55:17 GMT  
		Size: 141.0 MB (140979542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:690ea4de589a1e9b7d09dd43464a96fdc521278ea251d4c7b47d34624e50bdde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3574cd7269248b3901ea528c1a4117454f8cd6d49110485f3ab77c8d4a0c203`

```dockerfile
```

-	Layers:
	-	`sha256:4b3f63521ddea452add225d0b2adbf80fa705ee546645deb1d4ef8d3e9edcd3a`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 7.6 KB (7581 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-headless-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:0b9c7f14dc47341cfac46d84887ff9c9ab34590ed81a9238099b774f316236db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142430443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf506b5ea2d170486288daaa5f75857cb6ae5e30fa57cbcd9e2ef7029aad9391`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:41 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:56:41 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:56:41 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jdk-headless=11.0.31-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:56:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Mon, 22 Jun 2026 19:56:41 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d67b36cfcbc65f5126a122a3bdf95f982996c6dfb44692012827af0451213a`  
		Last Modified: Mon, 22 Jun 2026 19:56:56 GMT  
		Size: 138.2 MB (138248583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8c1c9155e5c5e49d4deae1539e15d0c7b0baefc3cade9f8e2ea52ed735a718f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de35ab2ab832a025b1fe6a87128bf3e4b49bfd076f616e021fc4c334f8f2a233`

```dockerfile
```

-	Layers:
	-	`sha256:1a304d31de9f62ab74c99b065bf35328c904a061e74c62b0dc6fcea897a305c1`  
		Last Modified: Mon, 22 Jun 2026 19:56:53 GMT  
		Size: 7.7 KB (7673 bytes)  
		MIME: application/vnd.in-toto+json
