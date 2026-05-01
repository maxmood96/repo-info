## `azul-zulu:26-alpine3.23`

```console
$ docker pull azul-zulu@sha256:72899f82f924b69368b75a236c8aab23da42e4ee934a51341aa9fe8f5bf537fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-alpine3.23` - linux; amd64

```console
$ docker pull azul-zulu@sha256:2884c2f1356ec32ce0ae5c6276c47928dc49cc5e65daf33e4f3cf659ad878439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187921955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca94e6713d27ad75e88885f0dd9d286321bcb45f834c99bedee5b282404764de`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:45 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:45 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:45 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu26-jdk=26.0.1-r1;      java -version # buildkit
# Fri, 01 May 2026 00:22:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Fri, 01 May 2026 00:22:45 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:22:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa69702304a52b495da8be17ee042e6981d55b16403642c6bacff0e1364bc250`  
		Last Modified: Fri, 01 May 2026 00:23:04 GMT  
		Size: 184.1 MB (184057766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e977a934d7c5d471f0dfbc8b8a618ef9ff03dcb0678d37b43e827df20f112696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b544cc51042b80010a5610855f3d7968e16d392377e3678fc1cb53aa71d153f6`

```dockerfile
```

-	Layers:
	-	`sha256:909268c703628fda35a2dd32097a95617686547edf15c10570f125aa8abf6c49`  
		Last Modified: Fri, 01 May 2026 00:22:59 GMT  
		Size: 7.8 KB (7819 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:1a579961c7a18e476436bdfab29e8b0a68fc1f084a9f20d80ff60abe821798b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185779472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a491f4a036006dff82d84f818dfa2e43d1864b4d85b655a1f61292c0b8ca0f6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:20:32 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:20:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:20:32 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu26-jdk=26.0.1-r1;      java -version # buildkit
# Fri, 01 May 2026 00:20:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Fri, 01 May 2026 00:20:32 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:20:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6e43f5954a3f0a5063c850a443afdbb3fcb4166021ba6380956c2b91dbf4a6`  
		Last Modified: Fri, 01 May 2026 00:20:53 GMT  
		Size: 181.6 MB (181579602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7c021ebd94b35047046b279fba9c0a16e41f4170285b98702c9964ef48e39408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae0e5d315d94713f791d32fcd904b3ae265110bb713560789535297c3f59920`

```dockerfile
```

-	Layers:
	-	`sha256:eb566be9078696f3189aa2d2a50c8a9e60aaab944e852b6bf7d4052ce156af48`  
		Last Modified: Fri, 01 May 2026 00:20:48 GMT  
		Size: 7.9 KB (7923 bytes)  
		MIME: application/vnd.in-toto+json
