## `azul-zulu:21-jdk-alpine`

```console
$ docker pull azul-zulu@sha256:96e4fa6d38833412206a29bd7c8b40439a66edeb61ea9bbb0fce8f847ebc3580
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jdk-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:034949efba2aaefb5a0516c301945380658cde002bf0d7e656a4ef41bd1f4fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165231046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92376ca0a5c52c9a987e48ba01bbb2bde9bd5b0e096d6dbf64987fa5732be115`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:26 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:55:26 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:26 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jdk=21.0.11-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:55:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Mon, 22 Jun 2026 19:55:26 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:55:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d22f57dbe349218271ef7c22686711447fed39b90300d7ae59f8a7316043bb2`  
		Last Modified: Mon, 22 Jun 2026 19:55:43 GMT  
		Size: 161.4 MB (161386625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0608b165c49b0e9f3d60e60e7b04316329a56de872614203d0f65bd759b10143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9887c95c30561f6858840e64cb9ed991d9262fd148cd11358a62494f19e21df3`

```dockerfile
```

-	Layers:
	-	`sha256:8baad2fa8c0838fc47439dbc5ad036e93a5fb160ddd2127d98f8494c4ea54b00`  
		Last Modified: Mon, 22 Jun 2026 19:55:38 GMT  
		Size: 7.8 KB (7822 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:8939ccffea870e84529c27a70bf57023305287d3f6aadbf633eedc69b41ab7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162791416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1fe05fe3abdd2e31f6087b814f2ea5a8cb41d710d729e5ff7c1bca1b0e2b3e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:06 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:57:06 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:57:06 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jdk=21.0.11-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:57:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Mon, 22 Jun 2026 19:57:06 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e037adfd03f313574620a5400f8a2fe1906dcae20c0ef30d86dd7b0c8e4f8e`  
		Last Modified: Mon, 22 Jun 2026 19:57:25 GMT  
		Size: 158.6 MB (158609556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:15e6afc28420847890a83de0f432ae91b2992bfcb5c98a693cfabcdf41f5243b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfcd66cd831f18cb6c61d9ae955d5c48a8dfb48d92b84a030faf342a43acf5e`

```dockerfile
```

-	Layers:
	-	`sha256:f67ba28ed3d7894a50522e6abdc55c607a420e8f4dd00eaec3e4243fdebb1e9e`  
		Last Modified: Mon, 22 Jun 2026 19:57:19 GMT  
		Size: 7.9 KB (7926 bytes)  
		MIME: application/vnd.in-toto+json
