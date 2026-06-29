## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:3c66911d53d63e76dd733c7994ca544c28602cafc68f27fbf47dbb8e37205e57
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

### `nats:2-alpine3.22` - linux; amd64

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

### `nats:2-alpine3.22` - unknown; unknown

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

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:afa0021fd5534b5898b5a146edea9264c8db26144b792c10a5315a35bbbac5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10482561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b85446ce3f424e4511a6ec5bcc77ecab084eb56464f1f1d28046674ab67a651`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a677c5f86a68cf2ce1fdf51d3b53c56b92e7fbe3b67443d993c093aac9e6a00f`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 7.0 MB (6986793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea037dcf8136a7791f9e560bda59f20a5e40ee8d447c9b81a75253956c52d2c`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91efd4d63f2001f13a850754a14e04788257c1dbe8f26cf095f7cc64ca2b5913`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7d4eebf896ed7b471bfb246e8823a02079e74eb6195ffc6edbc4246539be1a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4004102106793942ddb14115cf0e0684cc23e759a6ffca0eb4c60dd06d05b2fc`

```dockerfile
```

-	Layers:
	-	`sha256:cd7784700079db7a9f22cc194e5d89197a178370899405a829e82b5a633e3afe`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:91683fb37479895c178784386781a757532946afd57131bb405b062581ebef75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10188544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49ae72c112bb15690a11d8a5b7aa735cd4245c99549bce10acb4dc49a476ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8b795a8aa2f5335674b36741b17ce192443d940da95f3bbd597b70531689e3`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 7.0 MB (6977963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5097219f08bd67d8fa2e25a5a479e8bd0385d6216ab6343a4aa1875eb26304`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8e33bc51c0528dbfa912e61fdcfc8e25b5a0c5ed8ff2e87ebc145a65aa1605`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:753a5ea794f4139e119be983748b07d2258ba219fca43ac667a4533c6e30a1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b52454a96ab80fa5715d09b55b91072a66c893f75f0d94f5e43b01767f6c542`

```dockerfile
```

-	Layers:
	-	`sha256:a85da325cca4163e5d72d726f4f96a446323aa0b460ea8f228953398ba6b6171`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4267586f8d1941e8955323b0014cba3b61f65881b4c4c20de688fbe1c5fea804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10724412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f145de50057f413858c406b87310468fc4bd3effd1f88e329cf02fea0239e1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cfbf804236b512a4b9944ec56130b32a28b0a4b77458c90970f66f3a589254`  
		Last Modified: Mon, 22 Jun 2026 19:47:17 GMT  
		Size: 6.6 MB (6602958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92c950a70aceecc1179a9c484d238f8ec42132ddf44f71978023a2ac0e56fc0`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8f2ccaf61966a62729b5a1cfbdf7e05d864310ac230029a8a9cf60d0967ec7`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5deeca0a3264b5d656b04246f1c17f72ca74115b5de8e356adbe225c80c755bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a51798bd8628e715c409906689a2cf6fac8b1fee280fd2920de1e6a379bc4c6`

```dockerfile
```

-	Layers:
	-	`sha256:f0614b048154314f9962518fc36f249b39de8d985648d33ef1ce4bb9369f3f4a`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

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

### `nats:2-alpine3.22` - unknown; unknown

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

### `nats:2-alpine3.22` - linux; s390x

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

### `nats:2-alpine3.22` - unknown; unknown

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
