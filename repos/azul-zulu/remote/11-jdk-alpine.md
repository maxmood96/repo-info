## `azul-zulu:11-jdk-alpine`

```console
$ docker pull azul-zulu@sha256:211f44c704298d0b07f3a8d2fce6003d452119b4aab0a3ce1c9a44faf91d04f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jdk-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:9e2d3c1b853633f71258393618dbb275387c7cafe5eb8f0582bf61f0ee6ae4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147954672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ee2bb5382941f55e8ef1db82c5499a076aecd14561bff60d09c9643655dc76`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:11 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:11 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:11 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jdk=11.0.31-r3;      java -version # buildkit
# Fri, 01 May 2026 00:22:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Fri, 01 May 2026 00:22:11 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:22:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75301a22c1dfaca1cae1e2cf172a642a880d04d2ea7f6a8202d5e001bc296963`  
		Last Modified: Fri, 01 May 2026 00:22:26 GMT  
		Size: 144.1 MB (144090483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:111ad3f7ecaab4e1270ab69898f70ba85230eb88b54dc49765897c2705387dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c3df6e5afd3f5abba34a4ee7af73f9dce0eec12a65295571dc4f4092d1a7ac`

```dockerfile
```

-	Layers:
	-	`sha256:95089ad1447d55cb10ffad5d96f6c47291c70fbea1130e55642d1bf0a28941b9`  
		Last Modified: Fri, 01 May 2026 00:22:22 GMT  
		Size: 7.8 KB (7822 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:ba5c3a4cd04a7d45e823683da397195e72a1da0af06112138ce6f49f620672e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145633027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9e1a879485fad441cedf36d49781ee95ea58b3e8abdf285339091c472f7fe8`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:19:53 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:19:53 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:19:53 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jdk=11.0.31-r3;      java -version # buildkit
# Fri, 01 May 2026 00:19:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Fri, 01 May 2026 00:19:53 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:19:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c081a538cd49b1cdbc04e686d6aeeaf3a7f7f1bb4e23439293b40d9fa6f50ed3`  
		Last Modified: Fri, 01 May 2026 00:20:08 GMT  
		Size: 141.4 MB (141433157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e2c443151eb880da6dbcf78ed7e8bf8f29d133be25c6f6f2b605927128e09ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd8cb486165dab649490e1780082338448ac9e1d565d1b615ad158b439134e5`

```dockerfile
```

-	Layers:
	-	`sha256:6abcfd8fb7a80fdda1bd13392df81e5758672b007d81075cd951e50140392ae4`  
		Last Modified: Fri, 01 May 2026 00:20:04 GMT  
		Size: 7.9 KB (7926 bytes)  
		MIME: application/vnd.in-toto+json
