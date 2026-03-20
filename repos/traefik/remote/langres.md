## `traefik:langres`

```console
$ docker pull traefik@sha256:232527a42156ad9f715619558265a96d59c22383aff81841bf5b33b3afe930a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:langres` - linux; amd64

```console
$ docker pull traefik@sha256:f95a85c64f61123b05c6a0c93c80a26d92ceef6eef35c63267f30cba569a6763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52259855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b740f0218a988ab147663e56d953d4866c3e18861459b4d5dd87f839a3095204`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 19:04:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 19 Mar 2026 19:04:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-ea.2/traefik_v3.7.0-ea.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 19 Mar 2026 19:04:14 GMT
COPY entrypoint.sh / # buildkit
# Thu, 19 Mar 2026 19:04:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Mar 2026 19:04:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2026 19:04:14 GMT
CMD ["traefik"]
# Thu, 19 Mar 2026 19:04:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-ea.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4643ea7567411c583bfa01c643df2f5c0820d77b423b173be3f4c27fcc54f7`  
		Last Modified: Thu, 19 Mar 2026 19:04:36 GMT  
		Size: 460.8 KB (460752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dd64f8ac9db1a322e5479cde00953f2e2427646e66b9b442af59948aaa0f6`  
		Last Modified: Thu, 19 Mar 2026 19:04:38 GMT  
		Size: 47.9 MB (47936913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8229a9774692fb77fd495ee179c35117a0ce603bf80701831ad08fa87d0f92`  
		Last Modified: Thu, 19 Mar 2026 19:04:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:2793a48cd6e35401e2b49653a4aaefeaf4d86909b9918bf498fe18723b635ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.0 KB (853981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec004a1aca70400e1785a73e9f280930dfa4952bebcf0498a081b80f42e42e4c`

```dockerfile
```

-	Layers:
	-	`sha256:758e1e927086764a2d6ce81b72dacd63985f558f83a0843923e176790fa4930a`  
		Last Modified: Thu, 19 Mar 2026 19:04:36 GMT  
		Size: 842.5 KB (842525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:167673981626d480633a66c6986755169ce96d4a166e1b3b35de7df40e655998`  
		Last Modified: Thu, 19 Mar 2026 19:04:36 GMT  
		Size: 11.5 KB (11456 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; arm variant v6

```console
$ docker pull traefik@sha256:dab28a010db8d739c3b839d0b10bec1f50caa67c3c14b78a6b42350970df7151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47537906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb6f32362d8da5c1f99caf40e317f1e18fa35fd1b3647e388fcac4d48a11ca1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 19:04:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 19 Mar 2026 19:04:49 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-ea.2/traefik_v3.7.0-ea.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 19 Mar 2026 19:04:49 GMT
COPY entrypoint.sh / # buildkit
# Thu, 19 Mar 2026 19:04:49 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Mar 2026 19:04:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2026 19:04:49 GMT
CMD ["traefik"]
# Thu, 19 Mar 2026 19:04:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-ea.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c1a25ef4d23b6c0274b9e9a18eedeb8841580b3342a381a7f5490e55e0771e`  
		Last Modified: Thu, 19 Mar 2026 19:04:57 GMT  
		Size: 461.3 KB (461252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354962e854c1c12d0703aae6a73362229755e296c1b6431b5fcbf0029825ae74`  
		Last Modified: Thu, 19 Mar 2026 19:04:58 GMT  
		Size: 43.5 MB (43506464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb74fe34100914a148e07d4f6e958de7a65af44b4f00841d134efe7635a33ba`  
		Last Modified: Thu, 19 Mar 2026 19:04:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:b5adbfcab9b5ed18ddee22090b32a706adbe03effc0a5288408f8df5b473141c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 KB (11327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec49cb3107555291ff9d42fa7184d16f306be6c8e3e1fd09836c856b4e82e1c`

```dockerfile
```

-	Layers:
	-	`sha256:feabfabf55e848e96e21aa31305ca88abc98f8bdb7b9ab780a9657ef26255b58`  
		Last Modified: Thu, 19 Mar 2026 19:04:57 GMT  
		Size: 11.3 KB (11327 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e97c409a90162b13663eec8b2eb35518a47172f9ad6bb8f92e8e89ece7781c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47476719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c36f70f62acae85fbfd91c53fc2d1feaf8fef0b24793ca6b1bd1ace8be9e232`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 19:03:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 19 Mar 2026 19:03:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-ea.2/traefik_v3.7.0-ea.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 19 Mar 2026 19:03:52 GMT
COPY entrypoint.sh / # buildkit
# Thu, 19 Mar 2026 19:03:52 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Mar 2026 19:03:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2026 19:03:52 GMT
CMD ["traefik"]
# Thu, 19 Mar 2026 19:03:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-ea.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad50546172361585197df1a64e87c13184f6be6fa3eee69e6470838f9d11107`  
		Last Modified: Thu, 19 Mar 2026 19:04:17 GMT  
		Size: 462.8 KB (462767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790994d6478390c445d44ea2fa7b306fc66c8c8968dfb039e61a38d9dededcce`  
		Last Modified: Thu, 19 Mar 2026 19:04:19 GMT  
		Size: 42.8 MB (42816492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e44864cba6da7f88b88175b7e447c59fb1faf4001f3cabfe826d798608fa785`  
		Last Modified: Thu, 19 Mar 2026 19:04:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:197da7f7cb8b25da61d042199d9c4bc09e0f52710a6a30f703b3536f87d912fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.5 KB (853483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e628dff742e07d8135bacd0cf9e3b77e0b5b049ec88036fc5bd8598dccee9a`

```dockerfile
```

-	Layers:
	-	`sha256:201096c32b513376c7255fe2f0fc33e0687419c368eec9cd466e767ae48d7b58`  
		Last Modified: Thu, 19 Mar 2026 19:04:17 GMT  
		Size: 841.9 KB (841919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf94a1e4b8e0588214c824c476a55561c55d0f23e0f24f68c4cde6c11ff4acd`  
		Last Modified: Thu, 19 Mar 2026 19:04:17 GMT  
		Size: 11.6 KB (11564 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; ppc64le

```console
$ docker pull traefik@sha256:9b5516f2d16a99af859c762e72d8ce53f6b99201cd900cbc82b0ff8b7550c2d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45672790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bf845a4214243cbc810bc43a7b8792f080281cd05c15425a93208335b6e0ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 19:03:06 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 19 Mar 2026 19:03:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-ea.2/traefik_v3.7.0-ea.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 19 Mar 2026 19:03:11 GMT
COPY entrypoint.sh / # buildkit
# Thu, 19 Mar 2026 19:03:11 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Mar 2026 19:03:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2026 19:03:11 GMT
CMD ["traefik"]
# Thu, 19 Mar 2026 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-ea.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af51bc42354da8eb1ff8345f831b3ea10ce113a35ee36906dcc5802964dca33a`  
		Last Modified: Thu, 19 Mar 2026 19:03:56 GMT  
		Size: 463.3 KB (463256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5acdc834ea2eb9406d9338119781a10248350290eec34d0b9899b78e3430886`  
		Last Modified: Thu, 19 Mar 2026 19:03:57 GMT  
		Size: 41.4 MB (41379522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7091330080b984abd6035818d91de2a457ffc6edd9b91c710c9c89300727177`  
		Last Modified: Thu, 19 Mar 2026 19:03:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:6c6e840e2efec4ba30bc0b6644f0fa746e9d31afa70d1f45317ca5265fca8d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.4 KB (853398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8605ec6809b5b8f10e2ad6ed2ac1c58a91dc5941127494012aacb70540fcd9ab`

```dockerfile
```

-	Layers:
	-	`sha256:1a7f20b01f8b808fccd53d0f51a8864b29a209f2573b58614e208471b3f0fee9`  
		Last Modified: Thu, 19 Mar 2026 19:03:56 GMT  
		Size: 841.9 KB (841902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797d5c80b10b6e51d5e114b8f76e64c555aae1d7c26ecd238298761ce9e9363f`  
		Last Modified: Thu, 19 Mar 2026 19:03:56 GMT  
		Size: 11.5 KB (11496 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; riscv64

```console
$ docker pull traefik@sha256:c58515e5af480ea20502ceaead056a920ce3494cee7922ddaebec947f838e176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50329980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c21209dfd1e99519309cd4359488040e0750946f90f4621fc71c6cbb4ecd4a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 20 Mar 2026 21:32:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 20 Mar 2026 21:32:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-ea.2/traefik_v3.7.0-ea.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 20 Mar 2026 21:32:25 GMT
COPY entrypoint.sh / # buildkit
# Fri, 20 Mar 2026 21:32:25 GMT
EXPOSE map[80/tcp:{}]
# Fri, 20 Mar 2026 21:32:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Mar 2026 21:32:25 GMT
CMD ["traefik"]
# Fri, 20 Mar 2026 21:32:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-ea.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2138e9bd4a0faccf25a9170a648b7e113eea3d334c9206782528231fbf39f`  
		Last Modified: Fri, 20 Mar 2026 21:38:03 GMT  
		Size: 461.0 KB (460986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed40026e459d9ac2b247a811f868ff0170acc13385bcc12c460633f7355f316`  
		Last Modified: Fri, 20 Mar 2026 21:38:10 GMT  
		Size: 46.3 MB (46283337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f877dfd006cfeab5fe4b0e4df1b23d9eb5f6e0c7b2128572767934dd26420b67`  
		Last Modified: Fri, 20 Mar 2026 21:38:02 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:d38c2a0dadfc072e5c459b168d73c6027c67e41412bd5ba7a71e41037a68cc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.4 KB (853395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284ea96914955b216d2548ea3300d5e9745ac3eb01c5bd5d180d23c47a66c32b`

```dockerfile
```

-	Layers:
	-	`sha256:6ddcdafce273b9b923d9a72e279193c015f5701fa553542a3bcd810143747c21`  
		Last Modified: Fri, 20 Mar 2026 21:38:03 GMT  
		Size: 841.9 KB (841898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf5cb21b30215a609dc146b6054f6b5fc3d0371146c8482b4040aa82607dd28`  
		Last Modified: Fri, 20 Mar 2026 21:38:02 GMT  
		Size: 11.5 KB (11497 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; s390x

```console
$ docker pull traefik@sha256:aa017911424c088a708c4687dba536096925b4e29bae4831029f169e55f7ed3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50288269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d7ff882f7c4d0330e51376d72d3584a51335d56c4d282fda7d03bc8fa83e9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 19:03:14 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 19 Mar 2026 19:03:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-ea.2/traefik_v3.7.0-ea.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 19 Mar 2026 19:03:19 GMT
COPY entrypoint.sh / # buildkit
# Thu, 19 Mar 2026 19:03:19 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Mar 2026 19:03:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2026 19:03:19 GMT
CMD ["traefik"]
# Thu, 19 Mar 2026 19:03:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-ea.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3eb61e9bcba184986507951ef1d9732e354d5bacdb475ddb3a0a115604e60c7`  
		Last Modified: Thu, 19 Mar 2026 19:04:31 GMT  
		Size: 461.5 KB (461543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f907b23f3d910242b90bc2b245f999d734a8d7567f84b627cc9016ee5fb98456`  
		Last Modified: Thu, 19 Mar 2026 19:04:33 GMT  
		Size: 46.1 MB (46101026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc36f50716ec89ea20fc968410ac311ccc72032485feded643dbc8b1a785fee`  
		Last Modified: Thu, 19 Mar 2026 19:04:31 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:8f9aa243d6b1fa34ef1afb14ba50bd080712b75fded7b9d4ee7101bfe1a6d879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.3 KB (853329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e78c9c8943f20dc5f617ac7d063ab36d6e7c0e4c33123d462c89bab0dc6cc17`

```dockerfile
```

-	Layers:
	-	`sha256:38ec130c04880fccbd81d1612ca0456c9e0b1e1ef593a9be9a92c74725366afc`  
		Last Modified: Thu, 19 Mar 2026 19:04:31 GMT  
		Size: 841.9 KB (841872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b1a4f2ecb6dd50c2d7e4779b073435e3d7429ead8844b06705ae0fdb60478e2`  
		Last Modified: Thu, 19 Mar 2026 19:04:31 GMT  
		Size: 11.5 KB (11457 bytes)  
		MIME: application/vnd.in-toto+json
