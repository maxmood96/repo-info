## `azul-zulu:21-jre-headless-alpine`

```console
$ docker pull azul-zulu@sha256:3a35e5b86a7e3b3348adabd24ac89b61d6488ef02e0a2ca95709083d6a011f74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-headless-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:14bd038551ddf85aec423415a2a991f7319e9995e25ff0fcc68bc2499aba36ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72708033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7cd22c40c50300ee8e8bbe7c129469b3dfa86c6dc125386b52dde7ec277e5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:35 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:35 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:35 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jre-headless=21.0.11-r3;      java -version # buildkit
# Fri, 01 May 2026 00:22:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Fri, 01 May 2026 00:22:35 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ba01bf479dd86df4ecd37057a4e037dcd8ba2c2e632a89375897eeb819cf7`  
		Last Modified: Fri, 01 May 2026 00:22:48 GMT  
		Size: 68.8 MB (68843844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:5d171e7debe9f2fa164b16aa69b150e93d93850ff060a8ae9ceb493cd6647003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c9750e9a831c716d1d61619e8087b1a297a25d93d81e40cf385218f2c93a29`

```dockerfile
```

-	Layers:
	-	`sha256:cad1a80cfd7278961d17281bcf8c3c376663687d35fa23e066f09e122184154a`  
		Last Modified: Fri, 01 May 2026 00:22:46 GMT  
		Size: 7.6 KB (7576 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-headless-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c4e47de487e7b5d4b65ca8cf22446b0fa76d5eefdcb63c96f66e2b6f48a51eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71744958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e90966e724e8fa6e736533212fa06b84f0e76d9e4d6746cdfc82440024dfe83`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:20:20 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:20:20 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:20:20 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jre-headless=21.0.11-r3;      java -version # buildkit
# Fri, 01 May 2026 00:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Fri, 01 May 2026 00:20:20 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c4bc279bc345508f39a276598d9c5a874c43ae8d83efbdb5b43a7b6ffc2c59`  
		Last Modified: Fri, 01 May 2026 00:20:33 GMT  
		Size: 67.5 MB (67545088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0cbea82205e520af2e2a17967ad9535167ef0f2158f3c1f570346fa5a038785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13eff61098072a2f03aa1639339f969300e7c5a9e8d291e2df68cf41746876c`

```dockerfile
```

-	Layers:
	-	`sha256:d84634f6b3804ce4e3537726f000ae484c58a779ec78c7b67e3498458d9f47f4`  
		Last Modified: Fri, 01 May 2026 00:20:30 GMT  
		Size: 7.7 KB (7668 bytes)  
		MIME: application/vnd.in-toto+json
