<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.7`](#consul17)
-	[`consul:1.7.13`](#consul1713)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.9`](#consul189)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.4`](#consul194)
-	[`consul:latest`](#consullatest)

## `consul:1.7`

```console
$ docker pull consul@sha256:cf99387a5437272d4b0db0f183a43b999197c729f64e2719cdebf47c8f9b74bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7` - linux; amd64

```console
$ docker pull consul@sha256:0a21ba1ea665210ae4b803ad6ad02aab46221942e5906de632266b4bf15c249f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43132841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721ea43958a8cdedcdbe6f64ca01a6a4e7080550a10a16e8e747fa47a14d741c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:43:10 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 02:44:03 GMT
ARG CONSUL_VERSION=1.7.13
# Fri, 26 Mar 2021 02:44:03 GMT
LABEL org.opencontainers.image.version=1.7.13
# Fri, 26 Mar 2021 02:44:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 02:44:06 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 02:46:56 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 02:46:58 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 02:47:00 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:47:00 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 02:47:01 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 02:47:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 02:47:02 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 02:47:02 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 02:47:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 02:47:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1106305a820aabfafb8774783f8f7078792bd7e826b88ff3bc48f6432c6eac91`  
		Last Modified: Fri, 26 Mar 2021 02:48:12 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c2cd23190fd8f90e9d23d9e12f2f29597351d7c60f99c5b2c8bf6477d31c62`  
		Last Modified: Fri, 26 Mar 2021 02:48:20 GMT  
		Size: 40.3 MB (40329783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108b7b0a0b20f3c8e56df0815138f27869ac1e54c98a965e4b4d629821f2b40a`  
		Last Modified: Fri, 26 Mar 2021 02:48:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc020fd91774ea237f210263b1fa9100550c283d005419c7dddbbf1088b617c`  
		Last Modified: Fri, 26 Mar 2021 02:48:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46ff46c5b9ef9aa5a4a00d6b39bf553d724e0d41e9efacf820ae2089c0c0ecc`  
		Last Modified: Fri, 26 Mar 2021 02:48:12 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:56d4778b8542176ab9f9787f283c11a51db09ae620e335210acfe30b5264df86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38829684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff0c663b94bafa65171effcad2ce02299d760c2abf094c491344bfb2780cbc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:19:48 GMT
ARG CONSUL_VERSION=1.7.13
# Wed, 31 Mar 2021 18:19:50 GMT
LABEL org.opencontainers.image.version=1.7.13
# Wed, 31 Mar 2021 18:19:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:19:54 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:20:05 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:20:09 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:20:11 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:20:12 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:20:13 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:20:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:20:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:20:16 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:20:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:20:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529e7baba67302a45e39b19648a7a5087420bd12e6c5e7edd264de9bf0c5246`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe80981258c00e5deeae7d6a7bd7c31df363947dfc611fc8f63f58c0da83539c`  
		Last Modified: Wed, 31 Mar 2021 18:21:29 GMT  
		Size: 36.2 MB (36221735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a12e832dc4bf86a46031d49fdf7baec415ef626977c66eb162dd10bc0991259`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2575599c9a8e8beba97f517f4a60988ab6436cbc40263726f09e72b20799ce06`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65db31c460e548d6b2581483491186419b784f36355111139539d912f60190dc`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:42135e08c9b8bc1672e3e91475a499eccd807d89b36a5015c4c518cbe968716c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39044174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1d735cddafab670dc751bb724be9eff95fe94d3b187853d52aeec6f32e913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:44:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:49:42 GMT
ARG CONSUL_VERSION=1.7.13
# Thu, 25 Mar 2021 23:49:46 GMT
LABEL org.opencontainers.image.version=1.7.13
# Thu, 25 Mar 2021 23:49:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:49:53 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:50:05 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:50:15 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:50:25 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:50:29 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:50:32 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:50:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:50:37 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:50:46 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:51:17 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d56e71e4fac738ed8214ba2e022d537c959b1eb69e0e7d172ee08fc1340ab48`  
		Last Modified: Thu, 25 Mar 2021 23:54:31 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b187c13caab548b3692396f0534ba8e8965af05b303eb293ec3611e530014ea7`  
		Last Modified: Thu, 25 Mar 2021 23:54:39 GMT  
		Size: 36.3 MB (36331197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7241ca0078ca5e6eec4a777dc5ee46ec8597d76c55846ec932b1354274a33bb5`  
		Last Modified: Thu, 25 Mar 2021 23:54:31 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24709ea58e497984a722c1642225065e984c45ad3c84bf67ce1475abdc08714`  
		Last Modified: Thu, 25 Mar 2021 23:54:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac7932c4e4af13dd8e5fd2e4efd4fa28fe085e5e73ae79a41dd28d00fb35cb4`  
		Last Modified: Thu, 25 Mar 2021 23:54:31 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; 386

```console
$ docker pull consul@sha256:1cfda55781340c835db6260551947813b1459e0b905f2046b59aff0ca9bddad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41938947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58104fb1f88b8045824c49cc20ffb9b198b8f9161b549e393fbc28ea35d21d77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:08 GMT
ADD file:053c3a6154e80758106cbf0fec936c3b41dabf24a9f5eda36416caa90556810c in / 
# Wed, 31 Mar 2021 17:43:09 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 01:21:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 01:22:32 GMT
ARG CONSUL_VERSION=1.7.13
# Thu, 01 Apr 2021 01:22:32 GMT
LABEL org.opencontainers.image.version=1.7.13
# Thu, 01 Apr 2021 01:22:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 01:22:33 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 01:22:38 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 01:22:39 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 01:22:40 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 01:22:40 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 01:22:41 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 01:22:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 01:22:41 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 01:22:41 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 01:22:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 01:22:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eca83e4805e4c5e7b071425a4603bc4b02885b817aa7c1bba9605bd2cb9125a`  
		Last Modified: Wed, 31 Mar 2021 17:44:26 GMT  
		Size: 2.8 MB (2794977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893ce3db6debc969dedbf90babb2c4f7f699f290229304eb62073d129908bdd5`  
		Last Modified: Thu, 01 Apr 2021 01:23:53 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f3307521d89857d4a61746c0acbd35571281218a1a8052c016ad66eefb9600`  
		Last Modified: Thu, 01 Apr 2021 01:24:00 GMT  
		Size: 39.1 MB (39140678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b767934d01d9396ad8790e5d2437107e3150c474916e2d07ca60cb854be82945`  
		Last Modified: Thu, 01 Apr 2021 01:23:53 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0a4538b413e1c29dceac731f5ce84b6c869fe10ebee8534102241ffaeb503d`  
		Last Modified: Thu, 01 Apr 2021 01:23:53 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357d41df9e29d8c63d89e757c7660ee4be8b02fc9d661bc6a2f4c8511e4364c9`  
		Last Modified: Thu, 01 Apr 2021 01:23:53 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7.13`

```console
$ docker pull consul@sha256:cf99387a5437272d4b0db0f183a43b999197c729f64e2719cdebf47c8f9b74bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7.13` - linux; amd64

```console
$ docker pull consul@sha256:0a21ba1ea665210ae4b803ad6ad02aab46221942e5906de632266b4bf15c249f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43132841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721ea43958a8cdedcdbe6f64ca01a6a4e7080550a10a16e8e747fa47a14d741c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:43:10 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 02:44:03 GMT
ARG CONSUL_VERSION=1.7.13
# Fri, 26 Mar 2021 02:44:03 GMT
LABEL org.opencontainers.image.version=1.7.13
# Fri, 26 Mar 2021 02:44:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 02:44:06 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 02:46:56 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 02:46:58 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 02:47:00 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:47:00 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 02:47:01 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 02:47:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 02:47:02 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 02:47:02 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 02:47:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 02:47:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1106305a820aabfafb8774783f8f7078792bd7e826b88ff3bc48f6432c6eac91`  
		Last Modified: Fri, 26 Mar 2021 02:48:12 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c2cd23190fd8f90e9d23d9e12f2f29597351d7c60f99c5b2c8bf6477d31c62`  
		Last Modified: Fri, 26 Mar 2021 02:48:20 GMT  
		Size: 40.3 MB (40329783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108b7b0a0b20f3c8e56df0815138f27869ac1e54c98a965e4b4d629821f2b40a`  
		Last Modified: Fri, 26 Mar 2021 02:48:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc020fd91774ea237f210263b1fa9100550c283d005419c7dddbbf1088b617c`  
		Last Modified: Fri, 26 Mar 2021 02:48:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46ff46c5b9ef9aa5a4a00d6b39bf553d724e0d41e9efacf820ae2089c0c0ecc`  
		Last Modified: Fri, 26 Mar 2021 02:48:12 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.13` - linux; arm variant v6

```console
$ docker pull consul@sha256:56d4778b8542176ab9f9787f283c11a51db09ae620e335210acfe30b5264df86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38829684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff0c663b94bafa65171effcad2ce02299d760c2abf094c491344bfb2780cbc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:19:48 GMT
ARG CONSUL_VERSION=1.7.13
# Wed, 31 Mar 2021 18:19:50 GMT
LABEL org.opencontainers.image.version=1.7.13
# Wed, 31 Mar 2021 18:19:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:19:54 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:20:05 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:20:09 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:20:11 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:20:12 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:20:13 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:20:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:20:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:20:16 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:20:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:20:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529e7baba67302a45e39b19648a7a5087420bd12e6c5e7edd264de9bf0c5246`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe80981258c00e5deeae7d6a7bd7c31df363947dfc611fc8f63f58c0da83539c`  
		Last Modified: Wed, 31 Mar 2021 18:21:29 GMT  
		Size: 36.2 MB (36221735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a12e832dc4bf86a46031d49fdf7baec415ef626977c66eb162dd10bc0991259`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2575599c9a8e8beba97f517f4a60988ab6436cbc40263726f09e72b20799ce06`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65db31c460e548d6b2581483491186419b784f36355111139539d912f60190dc`  
		Last Modified: Wed, 31 Mar 2021 18:21:19 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.13` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:42135e08c9b8bc1672e3e91475a499eccd807d89b36a5015c4c518cbe968716c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39044174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1d735cddafab670dc751bb724be9eff95fe94d3b187853d52aeec6f32e913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:44:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:49:42 GMT
ARG CONSUL_VERSION=1.7.13
# Thu, 25 Mar 2021 23:49:46 GMT
LABEL org.opencontainers.image.version=1.7.13
# Thu, 25 Mar 2021 23:49:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:49:53 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:50:05 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:50:15 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:50:25 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:50:29 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:50:32 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:50:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:50:37 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:50:46 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:51:17 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d56e71e4fac738ed8214ba2e022d537c959b1eb69e0e7d172ee08fc1340ab48`  
		Last Modified: Thu, 25 Mar 2021 23:54:31 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b187c13caab548b3692396f0534ba8e8965af05b303eb293ec3611e530014ea7`  
		Last Modified: Thu, 25 Mar 2021 23:54:39 GMT  
		Size: 36.3 MB (36331197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7241ca0078ca5e6eec4a777dc5ee46ec8597d76c55846ec932b1354274a33bb5`  
		Last Modified: Thu, 25 Mar 2021 23:54:31 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24709ea58e497984a722c1642225065e984c45ad3c84bf67ce1475abdc08714`  
		Last Modified: Thu, 25 Mar 2021 23:54:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac7932c4e4af13dd8e5fd2e4efd4fa28fe085e5e73ae79a41dd28d00fb35cb4`  
		Last Modified: Thu, 25 Mar 2021 23:54:31 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.13` - linux; 386

```console
$ docker pull consul@sha256:1cfda55781340c835db6260551947813b1459e0b905f2046b59aff0ca9bddad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41938947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58104fb1f88b8045824c49cc20ffb9b198b8f9161b549e393fbc28ea35d21d77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:08 GMT
ADD file:053c3a6154e80758106cbf0fec936c3b41dabf24a9f5eda36416caa90556810c in / 
# Wed, 31 Mar 2021 17:43:09 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 01:21:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 01:22:32 GMT
ARG CONSUL_VERSION=1.7.13
# Thu, 01 Apr 2021 01:22:32 GMT
LABEL org.opencontainers.image.version=1.7.13
# Thu, 01 Apr 2021 01:22:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 01:22:33 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 01:22:38 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 01:22:39 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 01:22:40 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 01:22:40 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 01:22:41 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 01:22:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 01:22:41 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 01:22:41 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 01:22:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 01:22:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eca83e4805e4c5e7b071425a4603bc4b02885b817aa7c1bba9605bd2cb9125a`  
		Last Modified: Wed, 31 Mar 2021 17:44:26 GMT  
		Size: 2.8 MB (2794977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893ce3db6debc969dedbf90babb2c4f7f699f290229304eb62073d129908bdd5`  
		Last Modified: Thu, 01 Apr 2021 01:23:53 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f3307521d89857d4a61746c0acbd35571281218a1a8052c016ad66eefb9600`  
		Last Modified: Thu, 01 Apr 2021 01:24:00 GMT  
		Size: 39.1 MB (39140678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b767934d01d9396ad8790e5d2437107e3150c474916e2d07ca60cb854be82945`  
		Last Modified: Thu, 01 Apr 2021 01:23:53 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0a4538b413e1c29dceac731f5ce84b6c869fe10ebee8534102241ffaeb503d`  
		Last Modified: Thu, 01 Apr 2021 01:23:53 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357d41df9e29d8c63d89e757c7660ee4be8b02fc9d661bc6a2f4c8511e4364c9`  
		Last Modified: Thu, 01 Apr 2021 01:23:53 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:8add4c6dabd536fafb18bc622950e279e7ae6678ed542f833eb63f965ac14e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:2126a356ca0cfb037904e85be3f3afc7c60ccd379374bb56d31b3758772b9122
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46519232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84ae35d8bd17be7b9414c5b284057a9a7924a3ee86df904d8900e96be5af1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:43:10 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 02:43:36 GMT
ARG CONSUL_VERSION=1.8.9
# Fri, 26 Mar 2021 02:43:37 GMT
LABEL org.opencontainers.image.version=1.8.9
# Fri, 26 Mar 2021 02:43:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 02:43:40 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 02:43:48 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 02:43:51 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 02:43:53 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:43:54 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 02:43:54 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 02:43:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 02:43:55 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 02:43:55 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 02:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 02:43:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78c299d3ef19970fb9f819f2543360e0a400d514729e2f077959fd603da629b`  
		Last Modified: Fri, 26 Mar 2021 02:47:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8200a4c0661f5aa2bcaeb81f426f35395057d10002cc7e8de998b9a650c962e`  
		Last Modified: Fri, 26 Mar 2021 02:48:00 GMT  
		Size: 43.7 MB (43716178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b168f0410e6e126c0ea05ea6adb588b3577f3379dcbbfe8d3707986416bad877`  
		Last Modified: Fri, 26 Mar 2021 02:47:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f9a92c96ab9e1d2f6acd67b9869c4751c237986e62151cac925e5376e86b90`  
		Last Modified: Fri, 26 Mar 2021 02:47:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b924a20a61ac5750eb47704a7367a400db27ccba4c6fab695b3a9072a60d469a`  
		Last Modified: Fri, 26 Mar 2021 02:47:52 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:3ce0aaf87899af79726707ca5f6cce3aa05c0e09e60f744238f6c10ff02b379e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41786936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13df4b2e9e8f5beee9f678fb146d62f8f893031e03ca8d415e89ff6eba77f3e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:18:52 GMT
ARG CONSUL_VERSION=1.8.9
# Wed, 31 Mar 2021 18:18:55 GMT
LABEL org.opencontainers.image.version=1.8.9
# Wed, 31 Mar 2021 18:18:57 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:19:00 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:19:12 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:19:16 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:19:19 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:19:21 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:19:22 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:19:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:19:24 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:19:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:19:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6361f4b4701b9c8dd7e21881c0145615ccb6a248aa8747974b044ce2c13c79bd`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf5025eb71243b618ec0eb15217a060db83fe892c2df7c8dd7d7141a7b985d3`  
		Last Modified: Wed, 31 Mar 2021 18:21:10 GMT  
		Size: 39.2 MB (39178987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0009e1bfe638c28c30aad9b1b37a68410e1b5781cc64f528cd63f10e765c92`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bcca113639fa0e6481b1d4bc011c7302a4cca8a97f2dabe9f8445ae6dec5a1`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4819c38721e3cda06e2ad730593405bc4f0fd135ef6f6c9f75cf720ffa2896d`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:870545eaf00f07fa362c6308c5e2954f4bca7b838d2ad765a736c7ed94e3f619
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41954048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c05a8c45d317694aee98f5f48a389a0c4b7f99ba4a3de70715c9a9c43ec12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:44:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:47:33 GMT
ARG CONSUL_VERSION=1.8.9
# Thu, 25 Mar 2021 23:47:38 GMT
LABEL org.opencontainers.image.version=1.8.9
# Thu, 25 Mar 2021 23:47:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:47:58 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:48:08 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:48:29 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:48:34 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:48:36 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:48:39 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:48:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:48:54 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:48:56 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:49:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:49:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6afc3d6d6195e278f5519a82becbf56c981f11e5266fd6725a4de85f5558911`  
		Last Modified: Thu, 25 Mar 2021 23:53:21 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd49b88dd98fc5fe6a196669ce485ef3e6af41e2ac791ccae648f9316a4cf28`  
		Last Modified: Thu, 25 Mar 2021 23:53:30 GMT  
		Size: 39.2 MB (39241072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f18a0b5b4c19bfa0465b4d949585678875fa25b3579b3e7851e60bd175519d`  
		Last Modified: Thu, 25 Mar 2021 23:53:21 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9455c73876371636d41eaeb44ebba27aebec16808e1b3e4a13e5384a99cb0d0`  
		Last Modified: Thu, 25 Mar 2021 23:53:21 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1137860b43d68464234e30065c0fd796ed391996cefe69005199c8ca612760`  
		Last Modified: Thu, 25 Mar 2021 23:53:21 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:80689474c180d96ec715197a5eae3b79935d1d31aeffb185a647996784198618
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46043596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e4c7219543fc09b86be4abfc02929e2a4ba272259f34e273c875a055d1f84f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:08 GMT
ADD file:053c3a6154e80758106cbf0fec936c3b41dabf24a9f5eda36416caa90556810c in / 
# Wed, 31 Mar 2021 17:43:09 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 01:21:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 01:22:17 GMT
ARG CONSUL_VERSION=1.8.9
# Thu, 01 Apr 2021 01:22:17 GMT
LABEL org.opencontainers.image.version=1.8.9
# Thu, 01 Apr 2021 01:22:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 01:22:18 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 01:22:23 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 01:22:24 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 01:22:25 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 01:22:25 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 01:22:25 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 01:22:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 01:22:26 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 01:22:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 01:22:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 01:22:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eca83e4805e4c5e7b071425a4603bc4b02885b817aa7c1bba9605bd2cb9125a`  
		Last Modified: Wed, 31 Mar 2021 17:44:26 GMT  
		Size: 2.8 MB (2794977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1067568206d0e1fc99eeb01ebbd742ad9b38910eafe59484d06639b554982e`  
		Last Modified: Thu, 01 Apr 2021 01:23:33 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc78872870eba6d6ecb8cc6dbafdd66d99e088102e7ad3e0e334e60c1ea77424`  
		Last Modified: Thu, 01 Apr 2021 01:23:40 GMT  
		Size: 43.2 MB (43245329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b0186af352bfd50f344400a3e1db73797bd6ffebfbebca9c8cb16c1ad56007`  
		Last Modified: Thu, 01 Apr 2021 01:23:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1802628957717a3a1c183b80b640bd500e212741a70cc8046772fdd26a85a4a9`  
		Last Modified: Thu, 01 Apr 2021 01:23:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f145654d1fa11a0f6e1d697ce6f8e48f1cafbaab5ac1274ea32ffd84a4436d`  
		Last Modified: Thu, 01 Apr 2021 01:23:33 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.9`

```console
$ docker pull consul@sha256:8add4c6dabd536fafb18bc622950e279e7ae6678ed542f833eb63f965ac14e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.9` - linux; amd64

```console
$ docker pull consul@sha256:2126a356ca0cfb037904e85be3f3afc7c60ccd379374bb56d31b3758772b9122
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46519232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84ae35d8bd17be7b9414c5b284057a9a7924a3ee86df904d8900e96be5af1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:43:10 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 02:43:36 GMT
ARG CONSUL_VERSION=1.8.9
# Fri, 26 Mar 2021 02:43:37 GMT
LABEL org.opencontainers.image.version=1.8.9
# Fri, 26 Mar 2021 02:43:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 02:43:40 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 02:43:48 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 02:43:51 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 02:43:53 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:43:54 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 02:43:54 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 02:43:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 02:43:55 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 02:43:55 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 02:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 02:43:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78c299d3ef19970fb9f819f2543360e0a400d514729e2f077959fd603da629b`  
		Last Modified: Fri, 26 Mar 2021 02:47:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8200a4c0661f5aa2bcaeb81f426f35395057d10002cc7e8de998b9a650c962e`  
		Last Modified: Fri, 26 Mar 2021 02:48:00 GMT  
		Size: 43.7 MB (43716178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b168f0410e6e126c0ea05ea6adb588b3577f3379dcbbfe8d3707986416bad877`  
		Last Modified: Fri, 26 Mar 2021 02:47:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f9a92c96ab9e1d2f6acd67b9869c4751c237986e62151cac925e5376e86b90`  
		Last Modified: Fri, 26 Mar 2021 02:47:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b924a20a61ac5750eb47704a7367a400db27ccba4c6fab695b3a9072a60d469a`  
		Last Modified: Fri, 26 Mar 2021 02:47:52 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:3ce0aaf87899af79726707ca5f6cce3aa05c0e09e60f744238f6c10ff02b379e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41786936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13df4b2e9e8f5beee9f678fb146d62f8f893031e03ca8d415e89ff6eba77f3e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:18:52 GMT
ARG CONSUL_VERSION=1.8.9
# Wed, 31 Mar 2021 18:18:55 GMT
LABEL org.opencontainers.image.version=1.8.9
# Wed, 31 Mar 2021 18:18:57 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:19:00 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:19:12 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:19:16 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:19:19 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:19:21 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:19:22 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:19:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:19:24 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:19:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:19:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6361f4b4701b9c8dd7e21881c0145615ccb6a248aa8747974b044ce2c13c79bd`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf5025eb71243b618ec0eb15217a060db83fe892c2df7c8dd7d7141a7b985d3`  
		Last Modified: Wed, 31 Mar 2021 18:21:10 GMT  
		Size: 39.2 MB (39178987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0009e1bfe638c28c30aad9b1b37a68410e1b5781cc64f528cd63f10e765c92`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bcca113639fa0e6481b1d4bc011c7302a4cca8a97f2dabe9f8445ae6dec5a1`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4819c38721e3cda06e2ad730593405bc4f0fd135ef6f6c9f75cf720ffa2896d`  
		Last Modified: Wed, 31 Mar 2021 18:20:56 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:870545eaf00f07fa362c6308c5e2954f4bca7b838d2ad765a736c7ed94e3f619
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41954048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c05a8c45d317694aee98f5f48a389a0c4b7f99ba4a3de70715c9a9c43ec12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:44:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:47:33 GMT
ARG CONSUL_VERSION=1.8.9
# Thu, 25 Mar 2021 23:47:38 GMT
LABEL org.opencontainers.image.version=1.8.9
# Thu, 25 Mar 2021 23:47:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:47:58 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:48:08 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:48:29 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:48:34 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:48:36 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:48:39 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:48:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:48:54 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:48:56 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:49:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:49:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6afc3d6d6195e278f5519a82becbf56c981f11e5266fd6725a4de85f5558911`  
		Last Modified: Thu, 25 Mar 2021 23:53:21 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd49b88dd98fc5fe6a196669ce485ef3e6af41e2ac791ccae648f9316a4cf28`  
		Last Modified: Thu, 25 Mar 2021 23:53:30 GMT  
		Size: 39.2 MB (39241072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f18a0b5b4c19bfa0465b4d949585678875fa25b3579b3e7851e60bd175519d`  
		Last Modified: Thu, 25 Mar 2021 23:53:21 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9455c73876371636d41eaeb44ebba27aebec16808e1b3e4a13e5384a99cb0d0`  
		Last Modified: Thu, 25 Mar 2021 23:53:21 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1137860b43d68464234e30065c0fd796ed391996cefe69005199c8ca612760`  
		Last Modified: Thu, 25 Mar 2021 23:53:21 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.9` - linux; 386

```console
$ docker pull consul@sha256:80689474c180d96ec715197a5eae3b79935d1d31aeffb185a647996784198618
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46043596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e4c7219543fc09b86be4abfc02929e2a4ba272259f34e273c875a055d1f84f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:08 GMT
ADD file:053c3a6154e80758106cbf0fec936c3b41dabf24a9f5eda36416caa90556810c in / 
# Wed, 31 Mar 2021 17:43:09 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 01:21:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 01:22:17 GMT
ARG CONSUL_VERSION=1.8.9
# Thu, 01 Apr 2021 01:22:17 GMT
LABEL org.opencontainers.image.version=1.8.9
# Thu, 01 Apr 2021 01:22:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 01:22:18 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 01:22:23 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 01:22:24 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 01:22:25 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 01:22:25 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 01:22:25 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 01:22:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 01:22:26 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 01:22:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 01:22:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 01:22:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eca83e4805e4c5e7b071425a4603bc4b02885b817aa7c1bba9605bd2cb9125a`  
		Last Modified: Wed, 31 Mar 2021 17:44:26 GMT  
		Size: 2.8 MB (2794977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1067568206d0e1fc99eeb01ebbd742ad9b38910eafe59484d06639b554982e`  
		Last Modified: Thu, 01 Apr 2021 01:23:33 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc78872870eba6d6ecb8cc6dbafdd66d99e088102e7ad3e0e334e60c1ea77424`  
		Last Modified: Thu, 01 Apr 2021 01:23:40 GMT  
		Size: 43.2 MB (43245329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b0186af352bfd50f344400a3e1db73797bd6ffebfbebca9c8cb16c1ad56007`  
		Last Modified: Thu, 01 Apr 2021 01:23:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1802628957717a3a1c183b80b640bd500e212741a70cc8046772fdd26a85a4a9`  
		Last Modified: Thu, 01 Apr 2021 01:23:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f145654d1fa11a0f6e1d697ce6f8e48f1cafbaab5ac1274ea32ffd84a4436d`  
		Last Modified: Thu, 01 Apr 2021 01:23:33 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:27a4f100fbce2e5641e7e52d9bcc45c3c13807c7e8b311568ada4d9028b98b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:bec09274698fd058d6035434122715265d0d8a6e8ba83a7ddd3b2bd22a4fcd2a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45630966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f471bcfb979f8f38d9a06ec7f94e44f4f766a7e16af53b2ddbf511e2c420a26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:43:10 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 02:43:10 GMT
ARG CONSUL_VERSION=1.9.4
# Fri, 26 Mar 2021 02:43:11 GMT
LABEL org.opencontainers.image.version=1.9.4
# Fri, 26 Mar 2021 02:43:11 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 02:43:14 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 02:43:24 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 02:43:26 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 02:43:28 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:43:29 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 02:43:29 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 02:43:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 02:43:30 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 02:43:30 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 02:43:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 02:43:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d22e31ee01b8c422d795c73b65a9a8e75792393536ba3b99a0c3e36f0f67060`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7295ac900fa11a280a5cf85f90686414be12185189c5410c1d95d0c59fef7d4`  
		Last Modified: Fri, 26 Mar 2021 02:47:37 GMT  
		Size: 42.8 MB (42827913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23f2651d9b80a4fda0bc2e522bf7443e99f2c39dd3d311ce37bc033f8537bba`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d03e2e9070044a7885a8be244ede95ecf6f7d76120ac831e8a27fd662d79f68`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db1724bfa3036e85706162b1e2a86c5cabfcabb21a21a60966bb87c8d2ccb3c`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:5e95979eb0f587bdaa6bc9a907dec906caa691feea0879993f6238add7761df5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40887286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bac78aa811340290f5bcdb4fd6b795832d86439728d4d3c1ce82cf33fe83d45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:17:52 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 31 Mar 2021 18:17:53 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 31 Mar 2021 18:17:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:18:00 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:18:16 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:18:19 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:18:22 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:18:24 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:18:26 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:18:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:18:28 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:18:30 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:18:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecf3f2720c2819a62021fa2ddd31406cc9d809b36c240babf654d9aecfa175c`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc3089d78358b4878644e925bcb5bf9fe5926d68382f50983cf64d3e0f99234`  
		Last Modified: Wed, 31 Mar 2021 18:20:47 GMT  
		Size: 38.3 MB (38279335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6feb7541c18a5da452edc3d87e11122fb8274645e3b87f560526c1237d4e9607`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a695f91bd002196d854b0c991c3a73216c4777a448f289abba30876e00903`  
		Last Modified: Wed, 31 Mar 2021 18:20:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656c5b4d5174cceb4408fd595d02246961ef3dca2a97e9ba6933b79b23b16830`  
		Last Modified: Wed, 31 Mar 2021 18:20:37 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b797de25c60ed2af56407f40baaa7dce796343e43af16dec77175fdfdb3bdd45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41098380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b42762764b433e7b456d54f9ee7ac6e03a274262f35fc84e87bcfd7f5f616d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:44:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:44:20 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 25 Mar 2021 23:44:34 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 25 Mar 2021 23:44:46 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:45:00 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:46:07 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:46:13 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:46:21 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:46:27 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:46:40 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:46:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:46:49 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:46:52 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:47:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a9ea189dd08f9cdca4f7b3d3808cf25bddb9f95acf1afaad9572b2779f9f07`  
		Last Modified: Thu, 25 Mar 2021 23:52:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b052361d98f7c5204ae17b7ee9d041d81f3710ce4d8d48600e22efc7278b7bdf`  
		Last Modified: Thu, 25 Mar 2021 23:52:16 GMT  
		Size: 38.4 MB (38385390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96131dd11f70be23343d93e8cc6b166481fa0987d9200ed45a6f19bb4f174d8f`  
		Last Modified: Thu, 25 Mar 2021 23:52:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e8ffbc7fdec7b782ab1437aeb042a7dbdd0176df47f674ba33ff3b9bc65a38`  
		Last Modified: Thu, 25 Mar 2021 23:52:07 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572783dfcdc04987ef66bc438616b953f5f486b443f24e63b7d9ee39597e4a49`  
		Last Modified: Thu, 25 Mar 2021 23:52:07 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:23686a1dd3bdd3397129a652df5c3a20f2dbad52a9d788ee3f5817be8e5e776e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44977544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23acd3d24399e73e50541d91e938b76557481edaf1bd77430ed2c3cdcbfd2a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:08 GMT
ADD file:053c3a6154e80758106cbf0fec936c3b41dabf24a9f5eda36416caa90556810c in / 
# Wed, 31 Mar 2021 17:43:09 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 01:21:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 01:21:56 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 01 Apr 2021 01:21:57 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 01 Apr 2021 01:21:57 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 01:21:58 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 01:22:07 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 01:22:08 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 01:22:09 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 01:22:09 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 01:22:09 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 01:22:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 01:22:10 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 01:22:10 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 01:22:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 01:22:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eca83e4805e4c5e7b071425a4603bc4b02885b817aa7c1bba9605bd2cb9125a`  
		Last Modified: Wed, 31 Mar 2021 17:44:26 GMT  
		Size: 2.8 MB (2794977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7342c69e19efac9391e075228f97883422e2ead6bacdaa2395c2f0e542d679e6`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1319f6347360fb8e0afb9de289600ba4195b16af160154d83a8cb54b4700073b`  
		Last Modified: Thu, 01 Apr 2021 01:23:15 GMT  
		Size: 42.2 MB (42179275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4c83cec42bd7e817ed5295dd37c6bb5edd795f737d6dcaebe7bc0efc2a42e`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004e28eb9a622391f62ded8507411a3e48da8b561b7409087c1b939af1ac557`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df52be9f1d02c84167a282cb7aa9b2c4faf018338bde09132d55442dc0aa200`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.4`

```console
$ docker pull consul@sha256:27a4f100fbce2e5641e7e52d9bcc45c3c13807c7e8b311568ada4d9028b98b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.4` - linux; amd64

```console
$ docker pull consul@sha256:bec09274698fd058d6035434122715265d0d8a6e8ba83a7ddd3b2bd22a4fcd2a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45630966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f471bcfb979f8f38d9a06ec7f94e44f4f766a7e16af53b2ddbf511e2c420a26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:43:10 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 02:43:10 GMT
ARG CONSUL_VERSION=1.9.4
# Fri, 26 Mar 2021 02:43:11 GMT
LABEL org.opencontainers.image.version=1.9.4
# Fri, 26 Mar 2021 02:43:11 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 02:43:14 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 02:43:24 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 02:43:26 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 02:43:28 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:43:29 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 02:43:29 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 02:43:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 02:43:30 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 02:43:30 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 02:43:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 02:43:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d22e31ee01b8c422d795c73b65a9a8e75792393536ba3b99a0c3e36f0f67060`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7295ac900fa11a280a5cf85f90686414be12185189c5410c1d95d0c59fef7d4`  
		Last Modified: Fri, 26 Mar 2021 02:47:37 GMT  
		Size: 42.8 MB (42827913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23f2651d9b80a4fda0bc2e522bf7443e99f2c39dd3d311ce37bc033f8537bba`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d03e2e9070044a7885a8be244ede95ecf6f7d76120ac831e8a27fd662d79f68`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db1724bfa3036e85706162b1e2a86c5cabfcabb21a21a60966bb87c8d2ccb3c`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.4` - linux; arm variant v6

```console
$ docker pull consul@sha256:5e95979eb0f587bdaa6bc9a907dec906caa691feea0879993f6238add7761df5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40887286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bac78aa811340290f5bcdb4fd6b795832d86439728d4d3c1ce82cf33fe83d45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:17:52 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 31 Mar 2021 18:17:53 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 31 Mar 2021 18:17:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:18:00 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:18:16 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:18:19 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:18:22 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:18:24 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:18:26 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:18:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:18:28 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:18:30 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:18:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecf3f2720c2819a62021fa2ddd31406cc9d809b36c240babf654d9aecfa175c`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc3089d78358b4878644e925bcb5bf9fe5926d68382f50983cf64d3e0f99234`  
		Last Modified: Wed, 31 Mar 2021 18:20:47 GMT  
		Size: 38.3 MB (38279335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6feb7541c18a5da452edc3d87e11122fb8274645e3b87f560526c1237d4e9607`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a695f91bd002196d854b0c991c3a73216c4777a448f289abba30876e00903`  
		Last Modified: Wed, 31 Mar 2021 18:20:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656c5b4d5174cceb4408fd595d02246961ef3dca2a97e9ba6933b79b23b16830`  
		Last Modified: Wed, 31 Mar 2021 18:20:37 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b797de25c60ed2af56407f40baaa7dce796343e43af16dec77175fdfdb3bdd45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41098380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b42762764b433e7b456d54f9ee7ac6e03a274262f35fc84e87bcfd7f5f616d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:44:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:44:20 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 25 Mar 2021 23:44:34 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 25 Mar 2021 23:44:46 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:45:00 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:46:07 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:46:13 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:46:21 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:46:27 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:46:40 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:46:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:46:49 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:46:52 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:47:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a9ea189dd08f9cdca4f7b3d3808cf25bddb9f95acf1afaad9572b2779f9f07`  
		Last Modified: Thu, 25 Mar 2021 23:52:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b052361d98f7c5204ae17b7ee9d041d81f3710ce4d8d48600e22efc7278b7bdf`  
		Last Modified: Thu, 25 Mar 2021 23:52:16 GMT  
		Size: 38.4 MB (38385390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96131dd11f70be23343d93e8cc6b166481fa0987d9200ed45a6f19bb4f174d8f`  
		Last Modified: Thu, 25 Mar 2021 23:52:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e8ffbc7fdec7b782ab1437aeb042a7dbdd0176df47f674ba33ff3b9bc65a38`  
		Last Modified: Thu, 25 Mar 2021 23:52:07 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572783dfcdc04987ef66bc438616b953f5f486b443f24e63b7d9ee39597e4a49`  
		Last Modified: Thu, 25 Mar 2021 23:52:07 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.4` - linux; 386

```console
$ docker pull consul@sha256:23686a1dd3bdd3397129a652df5c3a20f2dbad52a9d788ee3f5817be8e5e776e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44977544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23acd3d24399e73e50541d91e938b76557481edaf1bd77430ed2c3cdcbfd2a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:08 GMT
ADD file:053c3a6154e80758106cbf0fec936c3b41dabf24a9f5eda36416caa90556810c in / 
# Wed, 31 Mar 2021 17:43:09 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 01:21:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 01:21:56 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 01 Apr 2021 01:21:57 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 01 Apr 2021 01:21:57 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 01:21:58 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 01:22:07 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 01:22:08 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 01:22:09 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 01:22:09 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 01:22:09 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 01:22:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 01:22:10 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 01:22:10 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 01:22:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 01:22:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eca83e4805e4c5e7b071425a4603bc4b02885b817aa7c1bba9605bd2cb9125a`  
		Last Modified: Wed, 31 Mar 2021 17:44:26 GMT  
		Size: 2.8 MB (2794977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7342c69e19efac9391e075228f97883422e2ead6bacdaa2395c2f0e542d679e6`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1319f6347360fb8e0afb9de289600ba4195b16af160154d83a8cb54b4700073b`  
		Last Modified: Thu, 01 Apr 2021 01:23:15 GMT  
		Size: 42.2 MB (42179275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4c83cec42bd7e817ed5295dd37c6bb5edd795f737d6dcaebe7bc0efc2a42e`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004e28eb9a622391f62ded8507411a3e48da8b561b7409087c1b939af1ac557`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df52be9f1d02c84167a282cb7aa9b2c4faf018338bde09132d55442dc0aa200`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:27a4f100fbce2e5641e7e52d9bcc45c3c13807c7e8b311568ada4d9028b98b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:bec09274698fd058d6035434122715265d0d8a6e8ba83a7ddd3b2bd22a4fcd2a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45630966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f471bcfb979f8f38d9a06ec7f94e44f4f766a7e16af53b2ddbf511e2c420a26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:43:10 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 02:43:10 GMT
ARG CONSUL_VERSION=1.9.4
# Fri, 26 Mar 2021 02:43:11 GMT
LABEL org.opencontainers.image.version=1.9.4
# Fri, 26 Mar 2021 02:43:11 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 02:43:14 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 02:43:24 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 02:43:26 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 02:43:28 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 02:43:29 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 02:43:29 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 02:43:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 02:43:30 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 02:43:30 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 02:43:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 02:43:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d22e31ee01b8c422d795c73b65a9a8e75792393536ba3b99a0c3e36f0f67060`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7295ac900fa11a280a5cf85f90686414be12185189c5410c1d95d0c59fef7d4`  
		Last Modified: Fri, 26 Mar 2021 02:47:37 GMT  
		Size: 42.8 MB (42827913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23f2651d9b80a4fda0bc2e522bf7443e99f2c39dd3d311ce37bc033f8537bba`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d03e2e9070044a7885a8be244ede95ecf6f7d76120ac831e8a27fd662d79f68`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db1724bfa3036e85706162b1e2a86c5cabfcabb21a21a60966bb87c8d2ccb3c`  
		Last Modified: Fri, 26 Mar 2021 02:47:24 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:5e95979eb0f587bdaa6bc9a907dec906caa691feea0879993f6238add7761df5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40887286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bac78aa811340290f5bcdb4fd6b795832d86439728d4d3c1ce82cf33fe83d45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:11 GMT
ADD file:00ac3d0df16779e7564cda9cbf94eef90ffa8043778a867272ff0135a1fb537f in / 
# Wed, 31 Mar 2021 17:19:12 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 18:17:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 31 Mar 2021 18:17:52 GMT
ARG CONSUL_VERSION=1.9.4
# Wed, 31 Mar 2021 18:17:53 GMT
LABEL org.opencontainers.image.version=1.9.4
# Wed, 31 Mar 2021 18:17:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 31 Mar 2021 18:18:00 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 31 Mar 2021 18:18:16 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 31 Mar 2021 18:18:19 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 31 Mar 2021 18:18:22 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 31 Mar 2021 18:18:24 GMT
VOLUME [/consul/data]
# Wed, 31 Mar 2021 18:18:26 GMT
EXPOSE 8300
# Wed, 31 Mar 2021 18:18:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 31 Mar 2021 18:18:28 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 31 Mar 2021 18:18:30 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 31 Mar 2021 18:18:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Mar 2021 18:18:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66e54586dae0889b30da12f7a66838d9b86511b58696c83c3b9166ff1a534bbe`  
		Last Modified: Wed, 31 Mar 2021 17:20:05 GMT  
		Size: 2.6 MB (2604658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecf3f2720c2819a62021fa2ddd31406cc9d809b36c240babf654d9aecfa175c`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc3089d78358b4878644e925bcb5bf9fe5926d68382f50983cf64d3e0f99234`  
		Last Modified: Wed, 31 Mar 2021 18:20:47 GMT  
		Size: 38.3 MB (38279335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6feb7541c18a5da452edc3d87e11122fb8274645e3b87f560526c1237d4e9607`  
		Last Modified: Wed, 31 Mar 2021 18:20:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a695f91bd002196d854b0c991c3a73216c4777a448f289abba30876e00903`  
		Last Modified: Wed, 31 Mar 2021 18:20:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656c5b4d5174cceb4408fd595d02246961ef3dca2a97e9ba6933b79b23b16830`  
		Last Modified: Wed, 31 Mar 2021 18:20:37 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b797de25c60ed2af56407f40baaa7dce796343e43af16dec77175fdfdb3bdd45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41098380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b42762764b433e7b456d54f9ee7ac6e03a274262f35fc84e87bcfd7f5f616d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:44:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:44:20 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 25 Mar 2021 23:44:34 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 25 Mar 2021 23:44:46 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:45:00 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:46:07 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:46:13 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:46:21 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:46:27 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:46:40 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:46:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:46:49 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:46:52 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:47:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a9ea189dd08f9cdca4f7b3d3808cf25bddb9f95acf1afaad9572b2779f9f07`  
		Last Modified: Thu, 25 Mar 2021 23:52:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b052361d98f7c5204ae17b7ee9d041d81f3710ce4d8d48600e22efc7278b7bdf`  
		Last Modified: Thu, 25 Mar 2021 23:52:16 GMT  
		Size: 38.4 MB (38385390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96131dd11f70be23343d93e8cc6b166481fa0987d9200ed45a6f19bb4f174d8f`  
		Last Modified: Thu, 25 Mar 2021 23:52:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e8ffbc7fdec7b782ab1437aeb042a7dbdd0176df47f674ba33ff3b9bc65a38`  
		Last Modified: Thu, 25 Mar 2021 23:52:07 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572783dfcdc04987ef66bc438616b953f5f486b443f24e63b7d9ee39597e4a49`  
		Last Modified: Thu, 25 Mar 2021 23:52:07 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:23686a1dd3bdd3397129a652df5c3a20f2dbad52a9d788ee3f5817be8e5e776e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44977544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23acd3d24399e73e50541d91e938b76557481edaf1bd77430ed2c3cdcbfd2a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:08 GMT
ADD file:053c3a6154e80758106cbf0fec936c3b41dabf24a9f5eda36416caa90556810c in / 
# Wed, 31 Mar 2021 17:43:09 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 01:21:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 01 Apr 2021 01:21:56 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 01 Apr 2021 01:21:57 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 01 Apr 2021 01:21:57 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 01 Apr 2021 01:21:58 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 01 Apr 2021 01:22:07 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 01 Apr 2021 01:22:08 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 01 Apr 2021 01:22:09 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 01:22:09 GMT
VOLUME [/consul/data]
# Thu, 01 Apr 2021 01:22:09 GMT
EXPOSE 8300
# Thu, 01 Apr 2021 01:22:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 01 Apr 2021 01:22:10 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 01 Apr 2021 01:22:10 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 01 Apr 2021 01:22:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 01:22:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eca83e4805e4c5e7b071425a4603bc4b02885b817aa7c1bba9605bd2cb9125a`  
		Last Modified: Wed, 31 Mar 2021 17:44:26 GMT  
		Size: 2.8 MB (2794977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7342c69e19efac9391e075228f97883422e2ead6bacdaa2395c2f0e542d679e6`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1319f6347360fb8e0afb9de289600ba4195b16af160154d83a8cb54b4700073b`  
		Last Modified: Thu, 01 Apr 2021 01:23:15 GMT  
		Size: 42.2 MB (42179275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4c83cec42bd7e817ed5295dd37c6bb5edd795f737d6dcaebe7bc0efc2a42e`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004e28eb9a622391f62ded8507411a3e48da8b561b7409087c1b939af1ac557`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df52be9f1d02c84167a282cb7aa9b2c4faf018338bde09132d55442dc0aa200`  
		Last Modified: Thu, 01 Apr 2021 01:23:08 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
