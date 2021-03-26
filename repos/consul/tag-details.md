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
$ docker pull consul@sha256:eba5e329a82f7f7badd4e7d67204fd8e326075c6acaf3ed08cca46167fdad2f2
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
$ docker pull consul@sha256:fa683e220e33336cc1f5e1da61aa50f927054793b9635884c00b45874d7a602b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38829827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c49daaabbc2cc31eab9ab686d1295c9e3bd63219e562cfb237a9c5761fbccc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:50:43 GMT
ADD file:65a3462a527f49c8c625927be6b8b57b4257c8cc37d685055a1f183d76c68920 in / 
# Thu, 25 Mar 2021 22:50:47 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 00:14:11 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 00:15:51 GMT
ARG CONSUL_VERSION=1.7.13
# Fri, 26 Mar 2021 00:15:54 GMT
LABEL org.opencontainers.image.version=1.7.13
# Fri, 26 Mar 2021 00:15:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 00:16:00 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 00:16:12 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 00:16:18 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 00:16:21 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 00:16:22 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 00:16:24 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 00:16:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 00:16:27 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 00:16:28 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 00:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 00:16:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:181a1446f0acaaa0871cec07aba4f733041f2d80ffbe01b19df43fe005df29f3`  
		Last Modified: Thu, 25 Mar 2021 22:55:06 GMT  
		Size: 2.6 MB (2604815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab63813515b49bdf0dab029c8fe51f7280a661f38d4d89fab0236295b12e34`  
		Last Modified: Fri, 26 Mar 2021 00:17:26 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f180c242feb21e2a699f74dd436c50deb78032d4932a5c5c50617f489310caa8`  
		Last Modified: Fri, 26 Mar 2021 00:17:39 GMT  
		Size: 36.2 MB (36221716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25714b74134f8af796da58e319559b6ba0cf502f685e96d809a5b2f5fcfea58e`  
		Last Modified: Fri, 26 Mar 2021 00:17:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98908917026614d05088194fa76d1a61a8a67a29af91efcc01261cbba68bba0d`  
		Last Modified: Fri, 26 Mar 2021 00:17:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8133330ee1df7214c5199f7dfb21614f3ed05ef67074a931a072add131514487`  
		Last Modified: Fri, 26 Mar 2021 00:17:26 GMT  
		Size: 1.7 KB (1706 bytes)  
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
$ docker pull consul@sha256:7ac91451b9e9fa7689a26e472e5fe4b4fc1638d157f53b102c2f353cc3f6cc9c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41938991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c92cfe18535041361a88ff314c233c1614976cc93b386e030e870d3702a844`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:38:33 GMT
ADD file:e1de160e7cc3d6bf2fb07933266ae79677b7a66bf08a227d4f62a15c4ad0143e in / 
# Thu, 25 Mar 2021 22:38:34 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:25:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:26:31 GMT
ARG CONSUL_VERSION=1.7.13
# Thu, 25 Mar 2021 23:26:31 GMT
LABEL org.opencontainers.image.version=1.7.13
# Thu, 25 Mar 2021 23:26:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:26:32 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:26:38 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:26:40 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:26:42 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:26:42 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:26:43 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:26:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:26:43 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:26:44 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:26:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:26:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1dafbb631785b9281f18282bddf80afd20b9820701771ef2e4492ad54682960d`  
		Last Modified: Thu, 25 Mar 2021 22:39:53 GMT  
		Size: 2.8 MB (2795009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be769969dbd8be850e7945da7fd5968ad20017bc438177cc41e27fc08b2ebb7`  
		Last Modified: Thu, 25 Mar 2021 23:28:21 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314ef27e65938fe076da911671e3ff5a79eaff3dc6a10aeb56c57e7f6410d3bf`  
		Last Modified: Thu, 25 Mar 2021 23:28:32 GMT  
		Size: 39.1 MB (39140692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2e42f579594e81bb1c1a7ddd7f55b56d9525a82b212fb57482127cf13b841d`  
		Last Modified: Thu, 25 Mar 2021 23:28:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470fbbf90d8682b26c552b232f0d663c52e8ff3d818d303fe3bae6df3ce33e75`  
		Last Modified: Thu, 25 Mar 2021 23:28:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc22b2cc3f74de3a522a14e371cb2494f27962533a2af469a0aa933869d3473`  
		Last Modified: Thu, 25 Mar 2021 23:28:21 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7.13`

```console
$ docker pull consul@sha256:eba5e329a82f7f7badd4e7d67204fd8e326075c6acaf3ed08cca46167fdad2f2
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
$ docker pull consul@sha256:fa683e220e33336cc1f5e1da61aa50f927054793b9635884c00b45874d7a602b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38829827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c49daaabbc2cc31eab9ab686d1295c9e3bd63219e562cfb237a9c5761fbccc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:50:43 GMT
ADD file:65a3462a527f49c8c625927be6b8b57b4257c8cc37d685055a1f183d76c68920 in / 
# Thu, 25 Mar 2021 22:50:47 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 00:14:11 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 00:15:51 GMT
ARG CONSUL_VERSION=1.7.13
# Fri, 26 Mar 2021 00:15:54 GMT
LABEL org.opencontainers.image.version=1.7.13
# Fri, 26 Mar 2021 00:15:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 00:16:00 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 00:16:12 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 00:16:18 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 00:16:21 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 00:16:22 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 00:16:24 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 00:16:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 00:16:27 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 00:16:28 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 00:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 00:16:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:181a1446f0acaaa0871cec07aba4f733041f2d80ffbe01b19df43fe005df29f3`  
		Last Modified: Thu, 25 Mar 2021 22:55:06 GMT  
		Size: 2.6 MB (2604815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab63813515b49bdf0dab029c8fe51f7280a661f38d4d89fab0236295b12e34`  
		Last Modified: Fri, 26 Mar 2021 00:17:26 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f180c242feb21e2a699f74dd436c50deb78032d4932a5c5c50617f489310caa8`  
		Last Modified: Fri, 26 Mar 2021 00:17:39 GMT  
		Size: 36.2 MB (36221716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25714b74134f8af796da58e319559b6ba0cf502f685e96d809a5b2f5fcfea58e`  
		Last Modified: Fri, 26 Mar 2021 00:17:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98908917026614d05088194fa76d1a61a8a67a29af91efcc01261cbba68bba0d`  
		Last Modified: Fri, 26 Mar 2021 00:17:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8133330ee1df7214c5199f7dfb21614f3ed05ef67074a931a072add131514487`  
		Last Modified: Fri, 26 Mar 2021 00:17:26 GMT  
		Size: 1.7 KB (1706 bytes)  
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
$ docker pull consul@sha256:7ac91451b9e9fa7689a26e472e5fe4b4fc1638d157f53b102c2f353cc3f6cc9c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41938991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c92cfe18535041361a88ff314c233c1614976cc93b386e030e870d3702a844`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:38:33 GMT
ADD file:e1de160e7cc3d6bf2fb07933266ae79677b7a66bf08a227d4f62a15c4ad0143e in / 
# Thu, 25 Mar 2021 22:38:34 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:25:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:26:31 GMT
ARG CONSUL_VERSION=1.7.13
# Thu, 25 Mar 2021 23:26:31 GMT
LABEL org.opencontainers.image.version=1.7.13
# Thu, 25 Mar 2021 23:26:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:26:32 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:26:38 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:26:40 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:26:42 GMT
# ARGS: CONSUL_VERSION=1.7.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:26:42 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:26:43 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:26:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:26:43 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:26:44 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:26:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:26:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1dafbb631785b9281f18282bddf80afd20b9820701771ef2e4492ad54682960d`  
		Last Modified: Thu, 25 Mar 2021 22:39:53 GMT  
		Size: 2.8 MB (2795009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be769969dbd8be850e7945da7fd5968ad20017bc438177cc41e27fc08b2ebb7`  
		Last Modified: Thu, 25 Mar 2021 23:28:21 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314ef27e65938fe076da911671e3ff5a79eaff3dc6a10aeb56c57e7f6410d3bf`  
		Last Modified: Thu, 25 Mar 2021 23:28:32 GMT  
		Size: 39.1 MB (39140692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2e42f579594e81bb1c1a7ddd7f55b56d9525a82b212fb57482127cf13b841d`  
		Last Modified: Thu, 25 Mar 2021 23:28:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470fbbf90d8682b26c552b232f0d663c52e8ff3d818d303fe3bae6df3ce33e75`  
		Last Modified: Thu, 25 Mar 2021 23:28:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc22b2cc3f74de3a522a14e371cb2494f27962533a2af469a0aa933869d3473`  
		Last Modified: Thu, 25 Mar 2021 23:28:21 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:86b952d332ab1a07f12e6c582417a09adf837cf0091ab9517e47fc38e4f5c814
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
$ docker pull consul@sha256:18ac02cf5e82d1b6df3c481ad6eea15121072cc158ebe243a29aef953b3ce1da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41787090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea12943309b2274b7270d8926a3ba924554840ce5f9deb145e3f0cc3fcfbd55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:50:43 GMT
ADD file:65a3462a527f49c8c625927be6b8b57b4257c8cc37d685055a1f183d76c68920 in / 
# Thu, 25 Mar 2021 22:50:47 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 00:14:11 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 00:15:02 GMT
ARG CONSUL_VERSION=1.8.9
# Fri, 26 Mar 2021 00:15:03 GMT
LABEL org.opencontainers.image.version=1.8.9
# Fri, 26 Mar 2021 00:15:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 00:15:07 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 00:15:20 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 00:15:24 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 00:15:27 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 00:15:28 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 00:15:29 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 00:15:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 00:15:33 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 00:15:35 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 00:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 00:15:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:181a1446f0acaaa0871cec07aba4f733041f2d80ffbe01b19df43fe005df29f3`  
		Last Modified: Thu, 25 Mar 2021 22:55:06 GMT  
		Size: 2.6 MB (2604815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42344ce8ea6c44570710b663b58ae345c1687915ddcaadacb27a5e9d3573df0a`  
		Last Modified: Fri, 26 Mar 2021 00:17:07 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eff31ec1e1526925608f82aeb5769ee6baa5b0cb7bdd8105d29b6aab0eaa720`  
		Last Modified: Fri, 26 Mar 2021 00:17:19 GMT  
		Size: 39.2 MB (39178983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e39ec1053e55cbba22280030f3fd8c95408be0827f3d96964ab064258da10c3`  
		Last Modified: Fri, 26 Mar 2021 00:17:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a99fc54ddfadc0abcf2df09b9c74b64f9183f030ab4766ae53fca17572f274a`  
		Last Modified: Fri, 26 Mar 2021 00:17:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c905355d91d89059174af2cb0437fec17aea10d99d3b18dd73ae43720a0d4392`  
		Last Modified: Fri, 26 Mar 2021 00:17:07 GMT  
		Size: 1.7 KB (1707 bytes)  
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
$ docker pull consul@sha256:cff564cf53b364ded5ef7cdb5071979ce866d4e7e57e5d19efe0f8376bf1def8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46043638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da12f9f1477bed59496a5a8f4d4a85700176c3c5d3a16c2a419b6c0b8b540b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:38:33 GMT
ADD file:e1de160e7cc3d6bf2fb07933266ae79677b7a66bf08a227d4f62a15c4ad0143e in / 
# Thu, 25 Mar 2021 22:38:34 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:25:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:26:13 GMT
ARG CONSUL_VERSION=1.8.9
# Thu, 25 Mar 2021 23:26:13 GMT
LABEL org.opencontainers.image.version=1.8.9
# Thu, 25 Mar 2021 23:26:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:26:14 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:26:21 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:26:23 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:26:23 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:26:24 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:26:24 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:26:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:26:24 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:26:24 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:26:25 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1dafbb631785b9281f18282bddf80afd20b9820701771ef2e4492ad54682960d`  
		Last Modified: Thu, 25 Mar 2021 22:39:53 GMT  
		Size: 2.8 MB (2795009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65284e36d8e54dd1cc74aae65be016ccf35f3cadfaef11886d481e443a51ec29`  
		Last Modified: Thu, 25 Mar 2021 23:27:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1832a4c51742d66d5e2223961653f5fa6672eb5f16b9888beb387e14acc939c`  
		Last Modified: Thu, 25 Mar 2021 23:28:07 GMT  
		Size: 43.2 MB (43245337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5a5103681f2f10d557298f66dc19fe3aed435998c0072405669a680a2f77da`  
		Last Modified: Thu, 25 Mar 2021 23:27:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6027647999bc5c00a873e761ce5e1c79f301f080240ad576117cf5d826d1e1c9`  
		Last Modified: Thu, 25 Mar 2021 23:27:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3af2863be01067c64890bcf7ce21941204038258944467f352608c2283678b`  
		Last Modified: Thu, 25 Mar 2021 23:27:56 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.9`

```console
$ docker pull consul@sha256:86b952d332ab1a07f12e6c582417a09adf837cf0091ab9517e47fc38e4f5c814
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
$ docker pull consul@sha256:18ac02cf5e82d1b6df3c481ad6eea15121072cc158ebe243a29aef953b3ce1da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41787090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea12943309b2274b7270d8926a3ba924554840ce5f9deb145e3f0cc3fcfbd55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:50:43 GMT
ADD file:65a3462a527f49c8c625927be6b8b57b4257c8cc37d685055a1f183d76c68920 in / 
# Thu, 25 Mar 2021 22:50:47 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 00:14:11 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 00:15:02 GMT
ARG CONSUL_VERSION=1.8.9
# Fri, 26 Mar 2021 00:15:03 GMT
LABEL org.opencontainers.image.version=1.8.9
# Fri, 26 Mar 2021 00:15:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 00:15:07 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 00:15:20 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 00:15:24 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 00:15:27 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 00:15:28 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 00:15:29 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 00:15:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 00:15:33 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 00:15:35 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 00:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 00:15:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:181a1446f0acaaa0871cec07aba4f733041f2d80ffbe01b19df43fe005df29f3`  
		Last Modified: Thu, 25 Mar 2021 22:55:06 GMT  
		Size: 2.6 MB (2604815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42344ce8ea6c44570710b663b58ae345c1687915ddcaadacb27a5e9d3573df0a`  
		Last Modified: Fri, 26 Mar 2021 00:17:07 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eff31ec1e1526925608f82aeb5769ee6baa5b0cb7bdd8105d29b6aab0eaa720`  
		Last Modified: Fri, 26 Mar 2021 00:17:19 GMT  
		Size: 39.2 MB (39178983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e39ec1053e55cbba22280030f3fd8c95408be0827f3d96964ab064258da10c3`  
		Last Modified: Fri, 26 Mar 2021 00:17:07 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a99fc54ddfadc0abcf2df09b9c74b64f9183f030ab4766ae53fca17572f274a`  
		Last Modified: Fri, 26 Mar 2021 00:17:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c905355d91d89059174af2cb0437fec17aea10d99d3b18dd73ae43720a0d4392`  
		Last Modified: Fri, 26 Mar 2021 00:17:07 GMT  
		Size: 1.7 KB (1707 bytes)  
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
$ docker pull consul@sha256:cff564cf53b364ded5ef7cdb5071979ce866d4e7e57e5d19efe0f8376bf1def8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46043638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da12f9f1477bed59496a5a8f4d4a85700176c3c5d3a16c2a419b6c0b8b540b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:38:33 GMT
ADD file:e1de160e7cc3d6bf2fb07933266ae79677b7a66bf08a227d4f62a15c4ad0143e in / 
# Thu, 25 Mar 2021 22:38:34 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:25:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:26:13 GMT
ARG CONSUL_VERSION=1.8.9
# Thu, 25 Mar 2021 23:26:13 GMT
LABEL org.opencontainers.image.version=1.8.9
# Thu, 25 Mar 2021 23:26:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:26:14 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:26:21 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:26:23 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:26:23 GMT
# ARGS: CONSUL_VERSION=1.8.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:26:24 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:26:24 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:26:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:26:24 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:26:24 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:26:25 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1dafbb631785b9281f18282bddf80afd20b9820701771ef2e4492ad54682960d`  
		Last Modified: Thu, 25 Mar 2021 22:39:53 GMT  
		Size: 2.8 MB (2795009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65284e36d8e54dd1cc74aae65be016ccf35f3cadfaef11886d481e443a51ec29`  
		Last Modified: Thu, 25 Mar 2021 23:27:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1832a4c51742d66d5e2223961653f5fa6672eb5f16b9888beb387e14acc939c`  
		Last Modified: Thu, 25 Mar 2021 23:28:07 GMT  
		Size: 43.2 MB (43245337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5a5103681f2f10d557298f66dc19fe3aed435998c0072405669a680a2f77da`  
		Last Modified: Thu, 25 Mar 2021 23:27:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6027647999bc5c00a873e761ce5e1c79f301f080240ad576117cf5d826d1e1c9`  
		Last Modified: Thu, 25 Mar 2021 23:27:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3af2863be01067c64890bcf7ce21941204038258944467f352608c2283678b`  
		Last Modified: Thu, 25 Mar 2021 23:27:56 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:dbc8dbda124b74f22f6a1757d505dd4c80f68e587c672351c8d797de3253ed9f
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
$ docker pull consul@sha256:bf12b51232f04315d771f6405293dfbe54d31a72ce86dc07f78d75bb791bc589
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40887420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ad5dd8a0f380a6578389895196a4cc399c8f3dc63ba7f0f6071ae1f22af0e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:50:43 GMT
ADD file:65a3462a527f49c8c625927be6b8b57b4257c8cc37d685055a1f183d76c68920 in / 
# Thu, 25 Mar 2021 22:50:47 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 00:14:11 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 00:14:13 GMT
ARG CONSUL_VERSION=1.9.4
# Fri, 26 Mar 2021 00:14:16 GMT
LABEL org.opencontainers.image.version=1.9.4
# Fri, 26 Mar 2021 00:14:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 00:14:21 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 00:14:34 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 00:14:39 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 00:14:44 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 00:14:46 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 00:14:47 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 00:14:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 00:14:49 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 00:14:50 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 00:14:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 00:14:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:181a1446f0acaaa0871cec07aba4f733041f2d80ffbe01b19df43fe005df29f3`  
		Last Modified: Thu, 25 Mar 2021 22:55:06 GMT  
		Size: 2.6 MB (2604815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d813a04af09382069adb1c56868e30c60a0c8b899fbfbb9bf7e9134752e751`  
		Last Modified: Fri, 26 Mar 2021 00:16:50 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b48abf4450807b48d190bbd2d8f287e27d5aa7f4fc36d175562fc04bf0e14e`  
		Last Modified: Fri, 26 Mar 2021 00:16:59 GMT  
		Size: 38.3 MB (38279312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0b8331e23477d117fb51ed1e9b7213e48b868a8745b7329bf2d8449347985`  
		Last Modified: Fri, 26 Mar 2021 00:16:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c231b1df1f03d4cc5deecee06c91397c79a9826a25377ca0f44ae3dc40ff1c1c`  
		Last Modified: Fri, 26 Mar 2021 00:16:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2907fc329adce4a371887daac9363fc5b0dc57df13eb144f51e65f1c87d23b33`  
		Last Modified: Fri, 26 Mar 2021 00:16:49 GMT  
		Size: 1.7 KB (1704 bytes)  
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
$ docker pull consul@sha256:6ed2bd7abe76e075f3723d9d9620d05a42c68286d8a117aa0acc9a736c6570fd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44977584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe91d0a6bddccabd8eaddb00a167688aaba8f9364d79d083c1717037eeb6ada`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:38:33 GMT
ADD file:e1de160e7cc3d6bf2fb07933266ae79677b7a66bf08a227d4f62a15c4ad0143e in / 
# Thu, 25 Mar 2021 22:38:34 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:25:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:25:55 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 25 Mar 2021 23:25:56 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 25 Mar 2021 23:25:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:25:57 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:26:03 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:26:04 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:26:05 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:26:05 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:26:05 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:26:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:26:06 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:26:06 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:26:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:26:07 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1dafbb631785b9281f18282bddf80afd20b9820701771ef2e4492ad54682960d`  
		Last Modified: Thu, 25 Mar 2021 22:39:53 GMT  
		Size: 2.8 MB (2795009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3c046deef7c9bd196ceb089c12599c0c8e70f120b33c2bd48be40a660f7da`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c724c525497d7c74061421f90ff7d2c1868a1753174aceba658b4bddd2b241f0`  
		Last Modified: Thu, 25 Mar 2021 23:27:31 GMT  
		Size: 42.2 MB (42179288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b1376f707ad860aa1b4a068172051e440e3b30f701887a6eb10142ac7c9061`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0fa8e62f248098bd92b1340c5b916b668b2a360aa7424f96c51f93b484cbc6`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acc2093653af7bc040d3ebcd2fc1a43e3ae359a87d1bc074360c4c09f24a6fa`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.4`

```console
$ docker pull consul@sha256:dbc8dbda124b74f22f6a1757d505dd4c80f68e587c672351c8d797de3253ed9f
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
$ docker pull consul@sha256:bf12b51232f04315d771f6405293dfbe54d31a72ce86dc07f78d75bb791bc589
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40887420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ad5dd8a0f380a6578389895196a4cc399c8f3dc63ba7f0f6071ae1f22af0e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:50:43 GMT
ADD file:65a3462a527f49c8c625927be6b8b57b4257c8cc37d685055a1f183d76c68920 in / 
# Thu, 25 Mar 2021 22:50:47 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 00:14:11 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 00:14:13 GMT
ARG CONSUL_VERSION=1.9.4
# Fri, 26 Mar 2021 00:14:16 GMT
LABEL org.opencontainers.image.version=1.9.4
# Fri, 26 Mar 2021 00:14:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 00:14:21 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 00:14:34 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 00:14:39 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 00:14:44 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 00:14:46 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 00:14:47 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 00:14:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 00:14:49 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 00:14:50 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 00:14:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 00:14:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:181a1446f0acaaa0871cec07aba4f733041f2d80ffbe01b19df43fe005df29f3`  
		Last Modified: Thu, 25 Mar 2021 22:55:06 GMT  
		Size: 2.6 MB (2604815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d813a04af09382069adb1c56868e30c60a0c8b899fbfbb9bf7e9134752e751`  
		Last Modified: Fri, 26 Mar 2021 00:16:50 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b48abf4450807b48d190bbd2d8f287e27d5aa7f4fc36d175562fc04bf0e14e`  
		Last Modified: Fri, 26 Mar 2021 00:16:59 GMT  
		Size: 38.3 MB (38279312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0b8331e23477d117fb51ed1e9b7213e48b868a8745b7329bf2d8449347985`  
		Last Modified: Fri, 26 Mar 2021 00:16:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c231b1df1f03d4cc5deecee06c91397c79a9826a25377ca0f44ae3dc40ff1c1c`  
		Last Modified: Fri, 26 Mar 2021 00:16:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2907fc329adce4a371887daac9363fc5b0dc57df13eb144f51e65f1c87d23b33`  
		Last Modified: Fri, 26 Mar 2021 00:16:49 GMT  
		Size: 1.7 KB (1704 bytes)  
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
$ docker pull consul@sha256:6ed2bd7abe76e075f3723d9d9620d05a42c68286d8a117aa0acc9a736c6570fd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44977584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe91d0a6bddccabd8eaddb00a167688aaba8f9364d79d083c1717037eeb6ada`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:38:33 GMT
ADD file:e1de160e7cc3d6bf2fb07933266ae79677b7a66bf08a227d4f62a15c4ad0143e in / 
# Thu, 25 Mar 2021 22:38:34 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:25:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:25:55 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 25 Mar 2021 23:25:56 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 25 Mar 2021 23:25:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:25:57 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:26:03 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:26:04 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:26:05 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:26:05 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:26:05 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:26:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:26:06 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:26:06 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:26:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:26:07 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1dafbb631785b9281f18282bddf80afd20b9820701771ef2e4492ad54682960d`  
		Last Modified: Thu, 25 Mar 2021 22:39:53 GMT  
		Size: 2.8 MB (2795009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3c046deef7c9bd196ceb089c12599c0c8e70f120b33c2bd48be40a660f7da`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c724c525497d7c74061421f90ff7d2c1868a1753174aceba658b4bddd2b241f0`  
		Last Modified: Thu, 25 Mar 2021 23:27:31 GMT  
		Size: 42.2 MB (42179288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b1376f707ad860aa1b4a068172051e440e3b30f701887a6eb10142ac7c9061`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0fa8e62f248098bd92b1340c5b916b668b2a360aa7424f96c51f93b484cbc6`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acc2093653af7bc040d3ebcd2fc1a43e3ae359a87d1bc074360c4c09f24a6fa`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:dbc8dbda124b74f22f6a1757d505dd4c80f68e587c672351c8d797de3253ed9f
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
$ docker pull consul@sha256:bf12b51232f04315d771f6405293dfbe54d31a72ce86dc07f78d75bb791bc589
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40887420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ad5dd8a0f380a6578389895196a4cc399c8f3dc63ba7f0f6071ae1f22af0e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:50:43 GMT
ADD file:65a3462a527f49c8c625927be6b8b57b4257c8cc37d685055a1f183d76c68920 in / 
# Thu, 25 Mar 2021 22:50:47 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 00:14:11 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 26 Mar 2021 00:14:13 GMT
ARG CONSUL_VERSION=1.9.4
# Fri, 26 Mar 2021 00:14:16 GMT
LABEL org.opencontainers.image.version=1.9.4
# Fri, 26 Mar 2021 00:14:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 26 Mar 2021 00:14:21 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 26 Mar 2021 00:14:34 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 26 Mar 2021 00:14:39 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 26 Mar 2021 00:14:44 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 26 Mar 2021 00:14:46 GMT
VOLUME [/consul/data]
# Fri, 26 Mar 2021 00:14:47 GMT
EXPOSE 8300
# Fri, 26 Mar 2021 00:14:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 26 Mar 2021 00:14:49 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 26 Mar 2021 00:14:50 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 00:14:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 00:14:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:181a1446f0acaaa0871cec07aba4f733041f2d80ffbe01b19df43fe005df29f3`  
		Last Modified: Thu, 25 Mar 2021 22:55:06 GMT  
		Size: 2.6 MB (2604815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d813a04af09382069adb1c56868e30c60a0c8b899fbfbb9bf7e9134752e751`  
		Last Modified: Fri, 26 Mar 2021 00:16:50 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b48abf4450807b48d190bbd2d8f287e27d5aa7f4fc36d175562fc04bf0e14e`  
		Last Modified: Fri, 26 Mar 2021 00:16:59 GMT  
		Size: 38.3 MB (38279312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e0b8331e23477d117fb51ed1e9b7213e48b868a8745b7329bf2d8449347985`  
		Last Modified: Fri, 26 Mar 2021 00:16:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c231b1df1f03d4cc5deecee06c91397c79a9826a25377ca0f44ae3dc40ff1c1c`  
		Last Modified: Fri, 26 Mar 2021 00:16:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2907fc329adce4a371887daac9363fc5b0dc57df13eb144f51e65f1c87d23b33`  
		Last Modified: Fri, 26 Mar 2021 00:16:49 GMT  
		Size: 1.7 KB (1704 bytes)  
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
$ docker pull consul@sha256:6ed2bd7abe76e075f3723d9d9620d05a42c68286d8a117aa0acc9a736c6570fd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44977584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe91d0a6bddccabd8eaddb00a167688aaba8f9364d79d083c1717037eeb6ada`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 25 Mar 2021 22:38:33 GMT
ADD file:e1de160e7cc3d6bf2fb07933266ae79677b7a66bf08a227d4f62a15c4ad0143e in / 
# Thu, 25 Mar 2021 22:38:34 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:25:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 25 Mar 2021 23:25:55 GMT
ARG CONSUL_VERSION=1.9.4
# Thu, 25 Mar 2021 23:25:56 GMT
LABEL org.opencontainers.image.version=1.9.4
# Thu, 25 Mar 2021 23:25:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 25 Mar 2021 23:25:57 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 25 Mar 2021 23:26:03 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 25 Mar 2021 23:26:04 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 25 Mar 2021 23:26:05 GMT
# ARGS: CONSUL_VERSION=1.9.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 25 Mar 2021 23:26:05 GMT
VOLUME [/consul/data]
# Thu, 25 Mar 2021 23:26:05 GMT
EXPOSE 8300
# Thu, 25 Mar 2021 23:26:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 25 Mar 2021 23:26:06 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 25 Mar 2021 23:26:06 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 23:26:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 23:26:07 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1dafbb631785b9281f18282bddf80afd20b9820701771ef2e4492ad54682960d`  
		Last Modified: Thu, 25 Mar 2021 22:39:53 GMT  
		Size: 2.8 MB (2795009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3c046deef7c9bd196ceb089c12599c0c8e70f120b33c2bd48be40a660f7da`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c724c525497d7c74061421f90ff7d2c1868a1753174aceba658b4bddd2b241f0`  
		Last Modified: Thu, 25 Mar 2021 23:27:31 GMT  
		Size: 42.2 MB (42179288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b1376f707ad860aa1b4a068172051e440e3b30f701887a6eb10142ac7c9061`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0fa8e62f248098bd92b1340c5b916b668b2a360aa7424f96c51f93b484cbc6`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acc2093653af7bc040d3ebcd2fc1a43e3ae359a87d1bc074360c4c09f24a6fa`  
		Last Modified: Thu, 25 Mar 2021 23:27:20 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
