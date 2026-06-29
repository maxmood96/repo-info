## `nats:alpine`

```console
$ docker pull nats@sha256:c11af972c99ae542de8925e6a7d9c533aa1eb039660420d2074beed6089b3bf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4e53bdfe4a9d810005abaf974dd9a12374c9cd187fa6be4622eff6a73b9e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8ea3792d3865371b24b0504e2a7a61140487a85c1289a56e6b0a414f3aa451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb591416c4f81c00164a6df7c9a0df260683e8939dad253a229dad6006eed7`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 7.0 MB (7001975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a94003f98dbb2cec821705d1615ee3fabdb6278a14a965fad556f00935df4e`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca954dfa8945adfa8283aac38370a786f5ed56c79b3a242cdc0a7717732e4c01`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2617716222bd82abc599cbe8277f98292977c0dfdd769178f6be9d0fdbfafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf691e94e06290aeb75516eb80f45749858c6ac66c0462f375e5b23f89c0f28`

```dockerfile
```

-	Layers:
	-	`sha256:051ab4a8c59747a86c2b341f78f881dcb5ce383e1adb18760b2e37658493f9f3`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:13a3f0e29c614c6b948bac76e8511e103dae75a1f3aafb215d49defef515bda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10202964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0bb66ac4162fc21cb64f4e23f7840a339f47c9c6e9fe68e07f879189b36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c57aa7f84636f8b81c22758ea4a628036299dea2750a000eb5de6220234b418`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 7.0 MB (6992381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b307022eba60d3fa1d5f402e6c270a824a7c22733d6b54b89a11d8e47f5df06`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979223c0d164e45ff3d261730284785ca49e194cd773a37086da9bdd856159e`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cc9db77acad1e638c9d195fe27bf9cb73a582f1d6c8a48de4aac85d42fe8b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e4eea65b1e82754ac2719f2026f89bf4d253eda69a68c1c7a0753cc424985`

```dockerfile
```

-	Layers:
	-	`sha256:be67ebf23efa9ed614c3e6ecbd8dbfe60c3c196c67672894c62befc4102a028d`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:064222a09af7b194af6760d6089aa9ebd93fe7b8136ec2193ddb72dd78d8bd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b422fa2e0339d3eb86f18cdd7040198afd726fadc2c6c0f499eff9c9038c9926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45f995edc436f16aee98c90da4e281a787ba379a91c7b812155f24b01f240c`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 6.6 MB (6619532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721188e517e99c1592046fd1c1f9d23061e01b186bfce2cef6bc65a52a5f7fd`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d19df182cbee156b010b04853280b7c12519c2b2a73a5d9a80ae357c814c67`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e4aef08d7bba47a53a2cdfea2260f5792c1fdb440a5ad4ff982730170aa3deb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb8badc11acca1d928d62f328aa0f3707584a4655e9abfa03e3b1b697d59a65`

```dockerfile
```

-	Layers:
	-	`sha256:e3cd06dd05bb0a25b9621e25ea152cd6cffebb5eff99e2740970497eaafedfd3`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json
