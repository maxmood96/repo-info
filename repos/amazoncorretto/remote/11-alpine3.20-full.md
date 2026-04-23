## `amazoncorretto:11-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:8ca473aa7030b0bda7e42aa4cf669aa9107dabd3060215c9e3a1cf2233fcc19d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f5cbf66f454973a21c1e20c31da7e14d6f2f7482064fdb347b414fc172ec613c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147308119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3041e838353ffb7bc156ca72f966235c569f15fb4f03419b5166fa15a62472`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:28 GMT
ARG version=11.0.31.11.1
# Wed, 22 Apr 2026 21:33:28 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:28 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca3b8194c124880aef48659ad48a90d748879850e492f8e5f7d483e65ff0ccb`  
		Last Modified: Wed, 22 Apr 2026 21:33:46 GMT  
		Size: 143.7 MB (143677798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1699112faab349c80e63ab896dcd61ed8c9d039aa21c6521f962003386760325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.8 KB (596835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ad3d63403ea06ef1d353772771435108bfde765aa34acedd9705574bda3108`

```dockerfile
```

-	Layers:
	-	`sha256:a7fbea33e5d1c4f2935020d5695c946214cc5877b68ded88fafee058bf2a5060`  
		Last Modified: Wed, 22 Apr 2026 21:33:42 GMT  
		Size: 587.5 KB (587456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efad35951c6ed422a6730a1830919b407933903ab975cf11f60cb1969ba24a72`  
		Last Modified: Wed, 22 Apr 2026 21:33:42 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:edf9f19c87e44c3b6b10fcae48736f8d4621b51ec107cc574da17dfab975a4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146058296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c02a20fa6b1f302bff7410a3e7579589f7287379a505f0c20c5bbcc69b460f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:15 GMT
ARG version=11.0.31.11.1
# Wed, 22 Apr 2026 21:33:15 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:15 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c28ec3f6ae33f080b037caf5d15c09e618416a8e8e00e9fa051317689d268f1`  
		Last Modified: Wed, 22 Apr 2026 21:33:33 GMT  
		Size: 142.0 MB (141965977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f911a99f358c0d1a8b2ddcc69bd47b22cecd36a4f3d2a7ba2da597638a36c332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 KB (596995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47660a3a09e800685bdf9114af102e5c2265eb7b267a6e843374150a2bd4832`

```dockerfile
```

-	Layers:
	-	`sha256:63477d993b56d36c735e93793e1bb1f84f0f538573ddab454b3121fbed9d1f6c`  
		Last Modified: Wed, 22 Apr 2026 21:33:29 GMT  
		Size: 587.5 KB (587512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f27ea44ad077b4abd9d24159249a5d6b2e6b3d24b733ce023e59967bd8450c`  
		Last Modified: Wed, 22 Apr 2026 21:33:29 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
