## `traefik:mimolette`

```console
$ docker pull traefik@sha256:f51c7a1e285483c11d44eddd417f92b0a27657a5973e0d7dc4d8c18cdd3b1065
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

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:e6dd92895868c3f0b1c7ab01295f3edcc4f856a136884b3978ea92f5fc9551ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53247782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fd52cdad20a3bd28ef0f92528a7f371404494467f0ed5410183e44b025d717`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 21:38:21 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 11 May 2026 21:38:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.46/traefik_v2.11.46_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 11 May 2026 21:38:56 GMT
COPY entrypoint.sh / # buildkit
# Mon, 11 May 2026 21:38:56 GMT
EXPOSE map[80/tcp:{}]
# Mon, 11 May 2026 21:38:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 21:38:56 GMT
CMD ["traefik"]
# Mon, 11 May 2026 21:38:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.46 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ce045b7136347424751eda2b2f07d6d2b2255445b86a9d89d79a3184fd07a`  
		Last Modified: Mon, 11 May 2026 21:38:46 GMT  
		Size: 455.5 KB (455499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79739d354672a659cdeabfc1cb7ea6805d385ed12ef46d4c18b6a00a4460d151`  
		Last Modified: Mon, 11 May 2026 21:39:21 GMT  
		Size: 48.9 MB (48927726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b597ed4f139e05aaf608cf10e5bae789c6fa3a6a5f3a270cf557078cf741a7b`  
		Last Modified: Mon, 11 May 2026 21:39:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:3e5458119d0058bf63345854129cef0996191fa1720d294ae2827edf08807102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **878.3 KB (878317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f0ba860a35679a07eee81bc2c6d175d3626638f1800391b4f254db412859b5`

```dockerfile
```

-	Layers:
	-	`sha256:d31ad71741e40684ac1303d8e788ae21843163c28ba35e7d7e6a1b48b3c1ec26`  
		Last Modified: Mon, 11 May 2026 21:39:20 GMT  
		Size: 865.7 KB (865707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97a198b14280d5184ddeb708682915b78b435ca213484014598ac78b15487a36`  
		Last Modified: Mon, 11 May 2026 21:39:19 GMT  
		Size: 12.6 KB (12610 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:30ffe433d099551215510e50ea6d6a22d5ae41c9a7cbbe82252378762932b420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48876410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a97abd44e7be3b9fa17a5d1870b37fd11403c7d19157a1fadd5934d813d4ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 21:39:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 11 May 2026 21:40:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.46/traefik_v2.11.46_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 11 May 2026 21:40:01 GMT
COPY entrypoint.sh / # buildkit
# Mon, 11 May 2026 21:40:01 GMT
EXPOSE map[80/tcp:{}]
# Mon, 11 May 2026 21:40:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 21:40:01 GMT
CMD ["traefik"]
# Mon, 11 May 2026 21:40:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.46 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe60bdf341aa2b8559a85b65342383faeff638f7fcc3ddbebbc4bc3a7c4ea50`  
		Last Modified: Mon, 11 May 2026 21:40:10 GMT  
		Size: 456.4 KB (456352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e5a17a7bf7a6a7006aea52b3b3c6aada7d129d93bef3a2a630494b70e2ca05`  
		Last Modified: Mon, 11 May 2026 21:40:11 GMT  
		Size: 44.8 MB (44847826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07698809b9d54eb60c44ae53bda0c9cc3da74f714b5f39ef7e86d6b43470edc`  
		Last Modified: Mon, 11 May 2026 21:40:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:03bc800260080e09f5a546748d631eac7e27b085baf0f379756dbe5a8defb846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 KB (12511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae48bb49994909e90317c8202686a140945b4c588e468d9a09b0bb3e3b2f7f3`

```dockerfile
```

-	Layers:
	-	`sha256:925e187109604ec3fa6cc119e5b059c34335ac86fa3ca06b323ce2eb937800db`  
		Last Modified: Mon, 11 May 2026 21:40:10 GMT  
		Size: 12.5 KB (12511 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:bc30e9714d00f221bb38ce9627d67d6adde411b42c27a9958482e2fffad7febd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48537983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2b0faafc7ae893263713d463c1238f69dcf5b6c04c75cb6a03514bf2c6bc78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 21:38:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 11 May 2026 21:38:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.46/traefik_v2.11.46_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 11 May 2026 21:38:22 GMT
COPY entrypoint.sh / # buildkit
# Mon, 11 May 2026 21:38:22 GMT
EXPOSE map[80/tcp:{}]
# Mon, 11 May 2026 21:38:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 21:38:22 GMT
CMD ["traefik"]
# Mon, 11 May 2026 21:38:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.46 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed94651ee374f7d06d11c37d38df3daa0f33f4ad0053ed4cf6cc2644c064991`  
		Last Modified: Mon, 11 May 2026 21:38:47 GMT  
		Size: 457.8 KB (457757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0c5d44c6a327653dd0311a8504ae81970e2b2aeb6a55abaf3676e90cf2e20b`  
		Last Modified: Mon, 11 May 2026 21:38:49 GMT  
		Size: 43.9 MB (43879988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9740ff738b66eed7bbed723e67c3ea98e206b505909f888550284258976e2ffc`  
		Last Modified: Mon, 11 May 2026 21:38:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:d93fe3946e91976f277dcd6b20098005588c0f652c17acb9a88e3a311b59c9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.9 KB (877914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d332616f8bcb11f01409b9d741bb2828c43c38c394bbcc7dbbe2392864b8ebfd`

```dockerfile
```

-	Layers:
	-	`sha256:8b21b1e22aa77c12a5a30e4422837f053bc4f6009ef1dfa3a73aacb3774e096a`  
		Last Modified: Mon, 11 May 2026 21:38:48 GMT  
		Size: 865.1 KB (865149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c0f956f9a584320d125db5f508f5418cb6a597c40cc9bb61e30bf30ad78715`  
		Last Modified: Mon, 11 May 2026 21:38:47 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:51c959462f9ebf0d85cc359d571af426de603acc60d216a5a71d40cf18facf57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47050511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c02fb0248c9e6ffc206acdd36674d6899c56356c911d097e88da57a3cb856c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 21:37:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 11 May 2026 21:39:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.46/traefik_v2.11.46_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 11 May 2026 21:39:03 GMT
COPY entrypoint.sh / # buildkit
# Mon, 11 May 2026 21:39:03 GMT
EXPOSE map[80/tcp:{}]
# Mon, 11 May 2026 21:39:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 21:39:03 GMT
CMD ["traefik"]
# Mon, 11 May 2026 21:39:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.46 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e295c7cbf20e6b410eec35608a9d27b273b65b02b7566e8d276d9ba659c0ce9b`  
		Last Modified: Mon, 11 May 2026 21:38:46 GMT  
		Size: 458.2 KB (458169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f60afe8c9805d5976bbb82fc08d1332fd03ce4a731f5c43bf8dbe5ace6363b8`  
		Last Modified: Mon, 11 May 2026 21:39:49 GMT  
		Size: 42.8 MB (42761045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b6d6925cc6b1a84b845eaecab32ca854ef2f474e1d25cb9a05120784e53227`  
		Last Modified: Mon, 11 May 2026 21:39:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:06bb58545b60ae49b8648a1c985581458fc8fdb5b270fd31e43cf6d3a7b457e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.8 KB (877782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b11f0fa37b27d6ff04139c44cd4c2e2ace759fe5f14b42f9eecc1b03f4dee36`

```dockerfile
```

-	Layers:
	-	`sha256:7476b0b50e4e17fd629cdc8789feaa1eaf35ecf02b1135865d61a6ac446a42ab`  
		Last Modified: Mon, 11 May 2026 21:39:48 GMT  
		Size: 865.1 KB (865108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83669c0185411e74a1f9361165f9b153c90b68ee6a4fb413567c8bf68df98de5`  
		Last Modified: Mon, 11 May 2026 21:39:48 GMT  
		Size: 12.7 KB (12674 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:610bb887ddeccfb7a34e672bf317943238c4e5a046051fa02e0bd145a3ce1b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaae53ea793184a865d7e04e16a2b88d7cf8af39e320d7014aac48b9bc8fb65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 13 May 2026 12:19:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 13 May 2026 12:30:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.46/traefik_v2.11.46_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 13 May 2026 12:30:56 GMT
COPY entrypoint.sh / # buildkit
# Wed, 13 May 2026 12:30:56 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 12:30:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 12:30:56 GMT
CMD ["traefik"]
# Wed, 13 May 2026 12:30:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.46 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fec3377cecfaabfbad434bb7a79f5b7898b4b04500ba155118bee98bec26258`  
		Last Modified: Wed, 13 May 2026 12:24:36 GMT  
		Size: 455.8 KB (455808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26026d060247ac7e37cd84b95cb78b1dbce548db68c95c6f1b6c4098198436a3`  
		Last Modified: Wed, 13 May 2026 12:36:19 GMT  
		Size: 47.6 MB (47578265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d0f8daeecf260c9c7a36d49980ab49e8bd0e2cb575f942405fa5bde3a8a07`  
		Last Modified: Wed, 13 May 2026 12:36:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:2ffee35f48f8a5657d6bce73db059d9d9cde0ffe19cdae039893ca19486b6178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.8 KB (877777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006b46f4eb409a90bcf42fdfc011a85f71160aa3c77c5e879a6462f39751c5b8`

```dockerfile
```

-	Layers:
	-	`sha256:76318477fe5b5dd95e4fde441a1cb74519d935ec3a03c8b7bb66a4117bde669b`  
		Last Modified: Wed, 13 May 2026 12:36:12 GMT  
		Size: 865.1 KB (865104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4d5b66166b7cd65eed166dee97e6ad16bf0bbc164f65ceba8c1dc9d79e2de4a`  
		Last Modified: Wed, 13 May 2026 12:36:12 GMT  
		Size: 12.7 KB (12673 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:e07cf5c9443fb468ecbde9aaace047c43b5a2b3e172248dc133d5844a021ea06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51677429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b8e3df7c29f645d88c4e782338f1cb3579fb8fb208cc60665c40b5f0b065b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 21:37:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 11 May 2026 21:37:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.46/traefik_v2.11.46_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 11 May 2026 21:37:55 GMT
COPY entrypoint.sh / # buildkit
# Mon, 11 May 2026 21:37:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 11 May 2026 21:37:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 21:37:55 GMT
CMD ["traefik"]
# Mon, 11 May 2026 21:37:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.46 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a0e1ef624b816629ce7e4b8c857acb3b44caf3a6da2c884e89c4e542d5c0e5`  
		Last Modified: Mon, 11 May 2026 21:38:44 GMT  
		Size: 456.5 KB (456501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7786918bbd3d7f8ddb79e2dce20f4ae159387b31e17024d6dff894f09bac71`  
		Last Modified: Mon, 11 May 2026 21:38:44 GMT  
		Size: 47.5 MB (47494027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b53ad670459312846bd82c30b70d589a3beff2a50aea12d88c7ff4e9de5a3ab`  
		Last Modified: Mon, 11 May 2026 21:38:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:8a7321a99d0dab38b6c3e380e4e677a9e60c068d29c2809bc5e2a03af5b5763c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.7 KB (877662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5646de3e2ef2404b333fcda8c694ed54f6920b6556b73835d71f7e46cf22eb1`

```dockerfile
```

-	Layers:
	-	`sha256:a212e22215b8ef75582537079daaa55e3d291b463f10a7782d7f1819c776af1e`  
		Last Modified: Mon, 11 May 2026 21:38:44 GMT  
		Size: 865.1 KB (865052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e87d39bfa6f4e672cdea7d9134f853938896107f6e93020cbd3f10894a0a5e`  
		Last Modified: Mon, 11 May 2026 21:38:44 GMT  
		Size: 12.6 KB (12610 bytes)  
		MIME: application/vnd.in-toto+json
