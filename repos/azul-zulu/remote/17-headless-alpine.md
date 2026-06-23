## `azul-zulu:17-headless-alpine`

```console
$ docker pull azul-zulu@sha256:50f702d8b0db449064512ffecd3cd0603cdbaeb95bb27936fc90f57a157df2ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-headless-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:d5afac1126f53eacc8f0a2582063ec0a56ccecc4ec61f26b3d011d21d0a2c35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149082045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8225020736c9902a49aa11f1cc58c4bfb0d6a784c4d94328d591d81569ac9be3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:10 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:55:10 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:10 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jdk-headless=17.0.19-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:55:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Mon, 22 Jun 2026 19:55:10 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:55:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b334fdae60ca1766aa164b40cfe37007fefbf1016b2b6b82d696891e301629d`  
		Last Modified: Mon, 22 Jun 2026 19:55:25 GMT  
		Size: 145.2 MB (145237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:80b26b0d654b6c78518f75b611c77849e6143b012537f859f36e1a61c8062db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2abe7c975275ea76296af4cdf7a75d164d7342eaf05f63bfef1d8a8061326e5`

```dockerfile
```

-	Layers:
	-	`sha256:a8d7308d408b539d05578207b3d4f7de85f176aefc96b40adb2d5e522c08c75a`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 7.6 KB (7580 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-headless-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:988bfc6ec778517511aa2bcc69b41df1fa0f831c7b4e077634148a6e44473fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146800751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2514628269426335fd7008b86d030dc454e51880ba9b537179dc057e933608fe`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:48 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:56:48 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:56:48 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jdk-headless=17.0.19-r3;      java -version # buildkit
# Mon, 22 Jun 2026 19:56:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Mon, 22 Jun 2026 19:56:48 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71a97e29a94284e00bfffcd1d85c200f145f7fcf15bd59ab47c679bfb6c426c`  
		Last Modified: Mon, 22 Jun 2026 19:57:04 GMT  
		Size: 142.6 MB (142618891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d3610c92bf691fd53800f19c4827d2a0aca87ea895a26f714613e3176525a06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d68a2050d9b5a52c3db98b94f9587ed54957c863e10c5c7830ca7171f70007`

```dockerfile
```

-	Layers:
	-	`sha256:4df8817fe409a2ddc429463f64fe024ab9f47f4c980f329b5847e4ba03718775`  
		Last Modified: Mon, 22 Jun 2026 19:56:59 GMT  
		Size: 7.7 KB (7673 bytes)  
		MIME: application/vnd.in-toto+json
