## `azul-zulu:25-headless-alpine`

```console
$ docker pull azul-zulu@sha256:c3cf4f6d4ea36056ae5ed6b52dfb614115578f1d8a06be37ae248f7727d3210b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-headless-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:22b4ca7e91caee7e658f98dedfe38bd2ed8eb0f9c4805ae056be38be1b303487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181929716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c92977fa806b1eacd4387ee9c4438e4aff520e750c83730b580712cbd19542`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:36 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:36 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:36 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu25-jdk-headless=25.0.3-r3;      java -version # buildkit
# Fri, 01 May 2026 00:22:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Fri, 01 May 2026 00:22:36 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:22:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2169829e7893a11a5e99d8be6bc5d114b100cd4d18e38e89b34932ffc02088e0`  
		Last Modified: Fri, 01 May 2026 00:22:55 GMT  
		Size: 178.1 MB (178065527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b04b50acc1a5ef25736317e5eff0fd5663d8e5cc2ac333dec9420edb017f7111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062e35cd39c64fe0944f88426bd71d7bbb72587db4dc1ad6d939c85bbf201b81`

```dockerfile
```

-	Layers:
	-	`sha256:8733a0b943fdf50421971fb4938bfdf9cb40d79600a3b5d9e48f5bcc2403243d`  
		Last Modified: Fri, 01 May 2026 00:22:50 GMT  
		Size: 7.6 KB (7578 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-headless-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:ace7a6f612ccf94a59e91580c598feb90ef3cc528c1e9b8def802d952410ebe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179862577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fefb5563cf7fcfe56c3ea2af78d4996e246878114e6b28aed43bf203cd6e68b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:20:28 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:20:28 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:20:28 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu25-jdk-headless=25.0.3-r3;      java -version # buildkit
# Fri, 01 May 2026 00:20:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Fri, 01 May 2026 00:20:28 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:20:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3168c1c7cf6ba693de5c0e0f4d61cfc87b77a2e28221b458b48b4aa300629`  
		Last Modified: Fri, 01 May 2026 00:20:48 GMT  
		Size: 175.7 MB (175662707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0fdec84d34fb84634a15acd9fd409d4fb67b7ad698e8b3781e01be4e82028f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dde01562f8839cbe86611ebb00d8826943a21bcdfabeb82d71e4ef309e8b2e2`

```dockerfile
```

-	Layers:
	-	`sha256:362b1c5c27f2c24de688d195f5c3214c624eecc98c89d6b04c961bbde1c7cf49`  
		Last Modified: Fri, 01 May 2026 00:20:44 GMT  
		Size: 7.7 KB (7670 bytes)  
		MIME: application/vnd.in-toto+json
