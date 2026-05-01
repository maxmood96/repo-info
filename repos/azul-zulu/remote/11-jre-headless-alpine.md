## `azul-zulu:11-jre-headless-alpine`

```console
$ docker pull azul-zulu@sha256:bd452712f2dc3c691d855c126c82f7f3e7d574818ebd1d3f1e51eaa53d2b141f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-headless-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:561d12755c73ae85e7592e2af1e5d9c338fc9187cd45c9b599548a50dd13a484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63072512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af4836cc6c8bc46e82e659208fe8cedbc1c9c314230b9811528e9dce2a2abb9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:14 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:14 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:14 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jre-headless=11.0.31-r3;      java -version # buildkit
# Fri, 01 May 2026 00:22:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Fri, 01 May 2026 00:22:14 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9452f33cb263fc5f80af52480ecff6c615355e0a728c9303c824d2be93461a8f`  
		Last Modified: Fri, 01 May 2026 00:22:24 GMT  
		Size: 59.2 MB (59208323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2c7f4a8314f2141c7d183ade9f20cb46b900676c28b8af7dfff40bf5d08323e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6620f557663e1aae57fc63401686fc2d232abc175529b229ed199193b1861d`

```dockerfile
```

-	Layers:
	-	`sha256:1420e5ee47643292aa30166b6024d502f9aa60e9d50a9920a3037993ca967d38`  
		Last Modified: Fri, 01 May 2026 00:22:22 GMT  
		Size: 7.6 KB (7576 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-headless-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:4fa3a5f53496023f8d5af0f9f9d907832884bc13e57f156425d3a6ed0b4cf9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62145564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266f3381466c4405846083ea7b0d8706bd918a2f737ea2b1c7eb4081664f0616`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:19:59 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:19:59 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:19:59 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jre-headless=11.0.31-r3;      java -version # buildkit
# Fri, 01 May 2026 00:19:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Fri, 01 May 2026 00:19:59 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff28629986d6de4ae3c860bde950cc354d9ba55bdd376c3dcfebe3dc411c55b`  
		Last Modified: Fri, 01 May 2026 00:20:09 GMT  
		Size: 57.9 MB (57945694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9c1be32dc9e80349dd070fac03192caecfbfa65584db42665b70618badf9a097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b44425015826cfd9b66cd56004b705c20a08d137e00c2383df18c6cf28b026d`

```dockerfile
```

-	Layers:
	-	`sha256:e697bd86a49e6289a64d7b174b4ba0a771dba1e7c1f1412ea73f4e26d36ee31c`  
		Last Modified: Fri, 01 May 2026 00:20:07 GMT  
		Size: 7.7 KB (7668 bytes)  
		MIME: application/vnd.in-toto+json
