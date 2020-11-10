<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.6`](#consul16)
-	[`consul:1.6.9`](#consul169)
-	[`consul:1.7`](#consul17)
-	[`consul:1.7.9`](#consul179)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.5`](#consul185)
-	[`consul:1.9.0-beta`](#consul190-beta)
-	[`consul:1.9.0-beta2`](#consul190-beta2)
-	[`consul:latest`](#consullatest)

## `consul:1.6`

```console
$ docker pull consul@sha256:cb126a8ba3b1e9338d836344d7b348022561910b2b4b9c01e37ef1d75149e306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.6` - linux; amd64

```console
$ docker pull consul@sha256:5b5f1b3ba3465882a2aebcaaea977ae4f34f0737419a20a54f5e25c81c2f99af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41876435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5207934c0f7102ad1f56bc59d0463fa4b0db22f914e3579663e2eaf74c2a2863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:17:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 03:18:33 GMT
ENV CONSUL_VERSION=1.6.9
# Thu, 22 Oct 2020 03:18:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 03:18:34 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 03:18:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 03:18:39 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 03:18:39 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:18:40 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 03:18:40 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 03:18:40 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 03:18:40 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 03:18:40 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 03:18:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 03:18:41 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cc3f32f0e27d7fac726129817fae6878496c1b4c62b4a7325c2ea7e697e66c`  
		Last Modified: Thu, 22 Oct 2020 03:19:35 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c6fad90b4c6d56b701482b4e231fffd52a9c134d5a41575debf9efcf273231`  
		Last Modified: Thu, 22 Oct 2020 03:19:41 GMT  
		Size: 39.1 MB (39076342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dbf5206913830fa67c472f42d776334ef4e10fa30e51abe9078545998faaf4`  
		Last Modified: Thu, 22 Oct 2020 03:19:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d53a2aaf01b1ef3df39ff27cc598238d76da9262f38dd741df52f9144961a14`  
		Last Modified: Thu, 22 Oct 2020 03:19:35 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c47673cd83f6bc5efeb05cb3df7cfc82bae8018ee2885afb14965e55612088`  
		Last Modified: Thu, 22 Oct 2020 03:19:35 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; arm variant v6

```console
$ docker pull consul@sha256:11402265c959324ae00a4be3e13c6b163fa028bdac6c516286cdcb602c7295ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37557209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c2989bc3346a2aec8227ad0d910bff035ff464b4c5eaff3075c05d7c1afd8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:19:05 GMT
ENV CONSUL_VERSION=1.6.9
# Thu, 22 Oct 2020 02:19:06 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:19:09 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:19:18 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:19:21 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:19:23 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:19:24 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:19:25 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:19:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:19:26 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:19:27 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:19:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd239832650b55fa048bc70f1d78fc8bbbd2c747915b960be35ea5d4b5eda01`  
		Last Modified: Thu, 22 Oct 2020 02:20:45 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9877f1a374dcd23efcd28ce516c7bdef47a2b906e6f0273844e30e0110c34e78`  
		Last Modified: Thu, 22 Oct 2020 02:20:53 GMT  
		Size: 35.0 MB (34952002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccb722985e3f755b5e11b4aa4934954ed81c6c29b7f514f54a8d5318f737b97`  
		Last Modified: Thu, 22 Oct 2020 02:20:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f37034126eb607ef4651ab1d37dd11ab119260e9e97c1456f8dde11568f22e`  
		Last Modified: Thu, 22 Oct 2020 02:20:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a159cc9bb0a9562a3f9a71eb14e64499ac3ca631199b8ae25fcb0190fecbed13`  
		Last Modified: Thu, 22 Oct 2020 02:20:44 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:651562ab568f0e5f048ff79fb85571a96020002a7303bdc4c38434b0d726ee2c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37770578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e4b0254d660feff03752cb9e82c296b041c1c345cc3b784a0fe2196fa28c70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:44:25 GMT
ENV CONSUL_VERSION=1.6.9
# Thu, 22 Oct 2020 02:44:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:44:28 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:44:34 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:44:38 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:44:43 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:44:44 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:44:46 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:44:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:44:47 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:44:48 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:44:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:44:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16997447fe87a1e8bbe78be659c82a0468ebd3c2da305fd40d5591a03dccb4a`  
		Last Modified: Thu, 22 Oct 2020 02:46:11 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d61c64ebeecfcbdcbb6fc2fce1e4ef538a936b94bca26de6e9ff54e0284731`  
		Last Modified: Thu, 22 Oct 2020 02:46:18 GMT  
		Size: 35.1 MB (35060733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616c87b38760da24b59bdbe435c945322b008564896a31be07d0a3c45d2053b9`  
		Last Modified: Thu, 22 Oct 2020 02:46:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed7362120f6af6391c8c69787dc5231391109ce44cce78be039956d3b5fe483`  
		Last Modified: Thu, 22 Oct 2020 02:46:11 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f83e82bb9fffaf33d87091dde5f758127f0a62a7bfd235ca3a727c8f919fe7`  
		Last Modified: Thu, 22 Oct 2020 02:46:11 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6` - linux; 386

```console
$ docker pull consul@sha256:c0ccc0d7d9d39b0b590ab7e7600d9a60622efedd792f4e29a1face7cb54fcef2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40711205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b939eaa71dd621532345005883735117cc2d10081e9f46c8e9a943f55c4b92c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:33:30 GMT
ENV CONSUL_VERSION=1.6.9
# Thu, 22 Oct 2020 02:33:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:33:31 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:33:35 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:33:36 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:33:37 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:33:37 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:33:37 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:33:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:33:38 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:33:38 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:33:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:33:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f593edb3ca181cedb465d47bc8d5f95fb0fbb2fd684196c9e5a9dcbaa452e2c`  
		Last Modified: Thu, 22 Oct 2020 02:34:34 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9045232253bcf9de8195d1df7cd598411be6b6a40b0e89818bb6befb51420643`  
		Last Modified: Thu, 22 Oct 2020 02:34:41 GMT  
		Size: 37.9 MB (37916567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87d11b33cb71552cd11e3aa1d36d118f3cf0e57d128f8857fd1af558334756b`  
		Last Modified: Thu, 22 Oct 2020 02:34:33 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7eaac794af9076db31f291ace339f2c6b5efb18de116ea29e2560eaab353628`  
		Last Modified: Thu, 22 Oct 2020 02:34:33 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2163c1d05156ee0574c9979e9426c9a6078d4b23ce7c23badf94a57e42f16fe2`  
		Last Modified: Thu, 22 Oct 2020 02:34:33 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.6.9`

```console
$ docker pull consul@sha256:cb126a8ba3b1e9338d836344d7b348022561910b2b4b9c01e37ef1d75149e306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.6.9` - linux; amd64

```console
$ docker pull consul@sha256:5b5f1b3ba3465882a2aebcaaea977ae4f34f0737419a20a54f5e25c81c2f99af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41876435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5207934c0f7102ad1f56bc59d0463fa4b0db22f914e3579663e2eaf74c2a2863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:17:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 03:18:33 GMT
ENV CONSUL_VERSION=1.6.9
# Thu, 22 Oct 2020 03:18:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 03:18:34 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 03:18:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 03:18:39 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 03:18:39 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:18:40 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 03:18:40 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 03:18:40 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 03:18:40 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 03:18:40 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 03:18:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 03:18:41 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cc3f32f0e27d7fac726129817fae6878496c1b4c62b4a7325c2ea7e697e66c`  
		Last Modified: Thu, 22 Oct 2020 03:19:35 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c6fad90b4c6d56b701482b4e231fffd52a9c134d5a41575debf9efcf273231`  
		Last Modified: Thu, 22 Oct 2020 03:19:41 GMT  
		Size: 39.1 MB (39076342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dbf5206913830fa67c472f42d776334ef4e10fa30e51abe9078545998faaf4`  
		Last Modified: Thu, 22 Oct 2020 03:19:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d53a2aaf01b1ef3df39ff27cc598238d76da9262f38dd741df52f9144961a14`  
		Last Modified: Thu, 22 Oct 2020 03:19:35 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c47673cd83f6bc5efeb05cb3df7cfc82bae8018ee2885afb14965e55612088`  
		Last Modified: Thu, 22 Oct 2020 03:19:35 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:11402265c959324ae00a4be3e13c6b163fa028bdac6c516286cdcb602c7295ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37557209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c2989bc3346a2aec8227ad0d910bff035ff464b4c5eaff3075c05d7c1afd8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:19:05 GMT
ENV CONSUL_VERSION=1.6.9
# Thu, 22 Oct 2020 02:19:06 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:19:09 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:19:18 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:19:21 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:19:23 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:19:24 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:19:25 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:19:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:19:26 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:19:27 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:19:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd239832650b55fa048bc70f1d78fc8bbbd2c747915b960be35ea5d4b5eda01`  
		Last Modified: Thu, 22 Oct 2020 02:20:45 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9877f1a374dcd23efcd28ce516c7bdef47a2b906e6f0273844e30e0110c34e78`  
		Last Modified: Thu, 22 Oct 2020 02:20:53 GMT  
		Size: 35.0 MB (34952002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccb722985e3f755b5e11b4aa4934954ed81c6c29b7f514f54a8d5318f737b97`  
		Last Modified: Thu, 22 Oct 2020 02:20:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f37034126eb607ef4651ab1d37dd11ab119260e9e97c1456f8dde11568f22e`  
		Last Modified: Thu, 22 Oct 2020 02:20:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a159cc9bb0a9562a3f9a71eb14e64499ac3ca631199b8ae25fcb0190fecbed13`  
		Last Modified: Thu, 22 Oct 2020 02:20:44 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:651562ab568f0e5f048ff79fb85571a96020002a7303bdc4c38434b0d726ee2c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37770578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e4b0254d660feff03752cb9e82c296b041c1c345cc3b784a0fe2196fa28c70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:44:25 GMT
ENV CONSUL_VERSION=1.6.9
# Thu, 22 Oct 2020 02:44:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:44:28 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:44:34 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:44:38 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:44:43 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:44:44 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:44:46 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:44:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:44:47 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:44:48 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:44:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:44:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16997447fe87a1e8bbe78be659c82a0468ebd3c2da305fd40d5591a03dccb4a`  
		Last Modified: Thu, 22 Oct 2020 02:46:11 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d61c64ebeecfcbdcbb6fc2fce1e4ef538a936b94bca26de6e9ff54e0284731`  
		Last Modified: Thu, 22 Oct 2020 02:46:18 GMT  
		Size: 35.1 MB (35060733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616c87b38760da24b59bdbe435c945322b008564896a31be07d0a3c45d2053b9`  
		Last Modified: Thu, 22 Oct 2020 02:46:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed7362120f6af6391c8c69787dc5231391109ce44cce78be039956d3b5fe483`  
		Last Modified: Thu, 22 Oct 2020 02:46:11 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f83e82bb9fffaf33d87091dde5f758127f0a62a7bfd235ca3a727c8f919fe7`  
		Last Modified: Thu, 22 Oct 2020 02:46:11 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.6.9` - linux; 386

```console
$ docker pull consul@sha256:c0ccc0d7d9d39b0b590ab7e7600d9a60622efedd792f4e29a1face7cb54fcef2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40711205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b939eaa71dd621532345005883735117cc2d10081e9f46c8e9a943f55c4b92c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:33:30 GMT
ENV CONSUL_VERSION=1.6.9
# Thu, 22 Oct 2020 02:33:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:33:31 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:33:35 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:33:36 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:33:37 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:33:37 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:33:37 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:33:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:33:38 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:33:38 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:33:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:33:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f593edb3ca181cedb465d47bc8d5f95fb0fbb2fd684196c9e5a9dcbaa452e2c`  
		Last Modified: Thu, 22 Oct 2020 02:34:34 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9045232253bcf9de8195d1df7cd598411be6b6a40b0e89818bb6befb51420643`  
		Last Modified: Thu, 22 Oct 2020 02:34:41 GMT  
		Size: 37.9 MB (37916567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87d11b33cb71552cd11e3aa1d36d118f3cf0e57d128f8857fd1af558334756b`  
		Last Modified: Thu, 22 Oct 2020 02:34:33 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7eaac794af9076db31f291ace339f2c6b5efb18de116ea29e2560eaab353628`  
		Last Modified: Thu, 22 Oct 2020 02:34:33 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2163c1d05156ee0574c9979e9426c9a6078d4b23ce7c23badf94a57e42f16fe2`  
		Last Modified: Thu, 22 Oct 2020 02:34:33 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7`

```console
$ docker pull consul@sha256:824dab354c4eaa1fc851f385aab4e3640db6a14c60b29c3bc573976e8eb115c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7` - linux; amd64

```console
$ docker pull consul@sha256:25f313de9d59276ace556ee03477c1a731fb24204a42ca7685d0d5d82979ebf0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43246973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4b7c1a00a632cbd3bf9f107b29b1d815403765d05993ce1513da8c812104f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:17:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 03:18:20 GMT
ENV CONSUL_VERSION=1.7.8
# Thu, 22 Oct 2020 03:18:20 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 03:18:21 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 03:18:25 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 03:18:26 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 03:18:27 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:18:27 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 03:18:27 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 03:18:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 03:18:28 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 03:18:28 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 03:18:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 03:18:28 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9070faa3b28ce1fd821969e32967a08c44c42d88b57530bdac5f9f4c06338efd`  
		Last Modified: Thu, 22 Oct 2020 03:19:17 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9099e63be530d042eb5e40fc3a6bbd2de0dbd83bfe28befed133ec9ccd50ceb`  
		Last Modified: Thu, 22 Oct 2020 03:19:24 GMT  
		Size: 40.4 MB (40446880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8093eb096d12f888532d00ceced752a3660f89f4848e5e45c14eaffef1a42d`  
		Last Modified: Thu, 22 Oct 2020 03:19:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00540f4a0f24e40d2f4a3760c525c36ec8ee02978071fb9890ff566c8b2ba6d`  
		Last Modified: Thu, 22 Oct 2020 03:19:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bb2a453b6ff1992e9e7553422f94c64ee4c0788b42fb604bea968f1d18199e`  
		Last Modified: Thu, 22 Oct 2020 03:19:18 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:2db40f6ad0da60a8bd9f7f00f71c56115f039cbf0316885c2cb20e23f0931dd1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38924120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8680f4300a83e027a835b43674073a118375528edcc4d4d10d18e0f4e4d13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:18:28 GMT
ENV CONSUL_VERSION=1.7.8
# Thu, 22 Oct 2020 02:18:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:18:32 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:18:40 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:18:43 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:18:46 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:18:48 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:18:50 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:18:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:18:54 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:18:54 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:18:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:18:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362d7bc1ef4aabc8f77c9ee4075120e73c1713da1a068e507628e93cfd70b9d5`  
		Last Modified: Thu, 22 Oct 2020 02:20:26 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0f913815265503adbe9d2795af3f68f558bedee744c1f2db9b2331181a5835`  
		Last Modified: Thu, 22 Oct 2020 02:20:36 GMT  
		Size: 36.3 MB (36318909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebc63ea7d35f00edbfbf244ab241567f12332a2dfb14366c2c45d8887315729`  
		Last Modified: Thu, 22 Oct 2020 02:20:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bbabb0d9883ceaafbb96aa45f4af26028284490ca6aa9b998982fffbd0de8d`  
		Last Modified: Thu, 22 Oct 2020 02:20:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b8b0280c0c57750295448b33f5585177c360ba3331fab6ce2209bebeb750b5`  
		Last Modified: Thu, 22 Oct 2020 02:20:27 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b8ae68f21657f99a78c35accfa81b273d4fb54394f37a427e98336aed2d536fd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39103791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf49477b99c8feb367ad880b495034920d284e1cc73e7a0ed4b9df8a207352e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:43:44 GMT
ENV CONSUL_VERSION=1.7.8
# Thu, 22 Oct 2020 02:43:46 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:43:50 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:44:02 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:44:05 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:44:08 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:44:08 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:44:09 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:44:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:44:11 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:44:12 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:44:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:44:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968982c6d6074d48939087574059ff72725e2958974fb5b80436f49161fdd115`  
		Last Modified: Thu, 22 Oct 2020 02:45:37 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5702da4067070094b526298b3a05abf0d2a9a8e0c60201bc7f1a6fc744d9d80`  
		Last Modified: Thu, 22 Oct 2020 02:46:03 GMT  
		Size: 36.4 MB (36393942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ccf2eb561e86187b01dfab1a20f1cf597967516917c1589489bd5e09c638b2`  
		Last Modified: Thu, 22 Oct 2020 02:45:37 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c2ba40bff249761f03bb4f4a5100e72cd0cf928ee37ef07015edcdbcf26153`  
		Last Modified: Thu, 22 Oct 2020 02:45:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04029515034058419f2d60d6c2dd1a06a6d10105a522f6d5575dd9c907249557`  
		Last Modified: Thu, 22 Oct 2020 02:45:37 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; 386

```console
$ docker pull consul@sha256:3926844f90e94a6f3be5bdbc889769528541d1e0be8b17c074b8073f922a36f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42034053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df2eac77c1efad58c3951fa319b458d1b7da01915f8a14a926a613f41d8873e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:33:16 GMT
ENV CONSUL_VERSION=1.7.8
# Thu, 22 Oct 2020 02:33:16 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:33:17 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:33:22 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:33:23 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:33:23 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:33:24 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:33:24 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:33:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:33:24 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:33:24 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:33:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:33:25 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846db40e649b58b8967aacf1f6f7a7d8627f1ffd6f918f6cb4367370d86f720e`  
		Last Modified: Thu, 22 Oct 2020 02:34:16 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731e87c48127e5fea1a2158e52aef1babde7f5bdc5f3fac254f813e8ac5871ab`  
		Last Modified: Thu, 22 Oct 2020 02:34:27 GMT  
		Size: 39.2 MB (39239414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef242b5bc816d7b2d2bc0a9a840fcc4a88c262936c3672739b5a2d91f32f711`  
		Last Modified: Thu, 22 Oct 2020 02:34:16 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e02e9eed1127a82a8898fea88eb8eb225449f970a78099c8fc7ac8348c9ab3`  
		Last Modified: Thu, 22 Oct 2020 02:34:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e0f6a184523db8b8a646ce977a666df54ba7508f2021b178f413a2823a020e`  
		Last Modified: Thu, 22 Oct 2020 02:34:16 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7.9`

**does not exist** (yet?)

## `consul:1.8`

```console
$ docker pull consul@sha256:b85322aa8c65355341dd81b5e95d5c0e8468e6419724d4e8a125198d40426a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:43eb37c372432743a4a7334f41dfde3aeac2e08ec6698c79cb23a6550898bff3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46463818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b214361a700e6ca4a014ff49035be3678c9375ba478a7b20bd0859bdcd9a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:17:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:19:39 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:19:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:19:40 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:19:45 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:19:45 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:19:46 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:19:46 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:19:46 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:19:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:19:47 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:19:47 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:19:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd0ad15d15483ddb156f9f3f293505ab3d80dd4f0298f988e53879107c17045`  
		Last Modified: Sat, 24 Oct 2020 00:20:05 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d30a01add5552182d8cf627fb6bfafb1bd6404bd9e8964d0f318e75ac909292`  
		Last Modified: Sat, 24 Oct 2020 00:20:11 GMT  
		Size: 43.7 MB (43663725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f3ae3ba267f18945e80a9a9d9b1aa4e960addad7330381e1eebeb178e893c1`  
		Last Modified: Sat, 24 Oct 2020 00:20:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0e80834954020a245984ab98e3a34b047ac702b81eb4674171d53caf4c95b`  
		Last Modified: Sat, 24 Oct 2020 00:20:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f607b07c9f2cfc208634b1170ebbfa675e6de56058826fec0ede6e593289b`  
		Last Modified: Sat, 24 Oct 2020 00:20:05 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:9cba8ea4acf03eec79ac41b0b0e86ef5d23819bcfaab38ad7d12aa4af5e3f86d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41724116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e7e84124bc9a52ebf375f54aa75182a64a07c13a9941e005da0cf936bcfb94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:50:53 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:50:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:50:55 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:51:03 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:51:06 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:51:08 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:51:10 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:51:11 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:51:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:51:13 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:51:13 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:51:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab63e1d933b90542c55c0589580d0ae8a9e2158b1a513a3f48ad426b6b19dc5`  
		Last Modified: Sat, 24 Oct 2020 00:51:36 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadae91cd7b954aab20e1a7852252f1d899656643f5a93419082e227368c1ba9`  
		Last Modified: Sat, 24 Oct 2020 00:51:48 GMT  
		Size: 39.1 MB (39118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aefd409dfcff320e4f4abc93acd6b79c75be32a4f8e945a7973b16e906f371`  
		Last Modified: Sat, 24 Oct 2020 00:51:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee425345016882213d153f7d97b63547b624b495d324a12f56499a64ec4bff4`  
		Last Modified: Sat, 24 Oct 2020 00:51:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2fb9fc2e5b60fa972411f03c730ae9062ba8f15afb38eb1bdda9787ec92001`  
		Last Modified: Sat, 24 Oct 2020 00:51:37 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b000c9a1b959e6e0f6a44e692719b859bbcf0a1dfce1457923223ad813de00ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41902164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbca14e16df0a545915052fd53f21614a74fc15be4d8f29f8c0b3778726f9feb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:39:48 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:39:49 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:39:51 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:39:58 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:40:00 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:40:02 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:40:02 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:40:03 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:40:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:40:04 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:40:06 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b6d3b9131728e261c4c4fc3af4cdd89e6dcba8ab1ab38c3c0f914e2eb39560`  
		Last Modified: Sat, 24 Oct 2020 00:40:31 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea498f059520372848099a86a79729c7818c4aebc0f8a0fe20587c848e59f415`  
		Last Modified: Sat, 24 Oct 2020 00:40:39 GMT  
		Size: 39.2 MB (39192313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9301e6a3342587e952ba4823d9d46356ef7f784b57e2e9fd46f14bfe405a08b6`  
		Last Modified: Sat, 24 Oct 2020 00:40:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d987f7d735d43368f22b2d5f0382da052100071025a829c766e8cc328f30f0`  
		Last Modified: Sat, 24 Oct 2020 00:40:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8904802b6e26f57003d8bce038eca94dc3b115a409726918967d41a91ab1a1`  
		Last Modified: Sat, 24 Oct 2020 00:40:31 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:b2b1abf3a45a2d4aab2e52e4211de930519d7602b448cd4ff1497c4783f2b59e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45976028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c5f30e70866e42e6cd1d5fca57611f44e3806485c2834b90d0a279e121cd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:38:28 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:38:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:38:29 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:38:34 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:38:35 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:38:36 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:38:36 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:38:36 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:38:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:38:37 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:38:37 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:38:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:38:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50575978b96251e969c7433bf747ff9948c7569cdba08b82642c9ff28dc3dad8`  
		Last Modified: Sat, 24 Oct 2020 00:38:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0bd61c7abe46d0a8800e07b99771a4a177768e7951b6e4bc406ef8c1ba5672`  
		Last Modified: Sat, 24 Oct 2020 00:39:04 GMT  
		Size: 43.2 MB (43181392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df109c109076c96fc724f585f9e9b2decc3c9c96a51c0a26891089492f2a793b`  
		Last Modified: Sat, 24 Oct 2020 00:38:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c51e22ab172236135e965946eaf3a7a7a54768ec71cf853a1a6b18c4326df4`  
		Last Modified: Sat, 24 Oct 2020 00:38:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf571036f9872b050d07d5272ddeebf9629fa2af03e0dac3456433ac857abca`  
		Last Modified: Sat, 24 Oct 2020 00:38:56 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.5`

```console
$ docker pull consul@sha256:b85322aa8c65355341dd81b5e95d5c0e8468e6419724d4e8a125198d40426a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.5` - linux; amd64

```console
$ docker pull consul@sha256:43eb37c372432743a4a7334f41dfde3aeac2e08ec6698c79cb23a6550898bff3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46463818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b214361a700e6ca4a014ff49035be3678c9375ba478a7b20bd0859bdcd9a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:17:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:19:39 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:19:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:19:40 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:19:45 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:19:45 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:19:46 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:19:46 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:19:46 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:19:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:19:47 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:19:47 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:19:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd0ad15d15483ddb156f9f3f293505ab3d80dd4f0298f988e53879107c17045`  
		Last Modified: Sat, 24 Oct 2020 00:20:05 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d30a01add5552182d8cf627fb6bfafb1bd6404bd9e8964d0f318e75ac909292`  
		Last Modified: Sat, 24 Oct 2020 00:20:11 GMT  
		Size: 43.7 MB (43663725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f3ae3ba267f18945e80a9a9d9b1aa4e960addad7330381e1eebeb178e893c1`  
		Last Modified: Sat, 24 Oct 2020 00:20:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0e80834954020a245984ab98e3a34b047ac702b81eb4674171d53caf4c95b`  
		Last Modified: Sat, 24 Oct 2020 00:20:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f607b07c9f2cfc208634b1170ebbfa675e6de56058826fec0ede6e593289b`  
		Last Modified: Sat, 24 Oct 2020 00:20:05 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.5` - linux; arm variant v6

```console
$ docker pull consul@sha256:9cba8ea4acf03eec79ac41b0b0e86ef5d23819bcfaab38ad7d12aa4af5e3f86d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41724116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e7e84124bc9a52ebf375f54aa75182a64a07c13a9941e005da0cf936bcfb94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:50:53 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:50:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:50:55 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:51:03 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:51:06 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:51:08 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:51:10 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:51:11 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:51:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:51:13 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:51:13 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:51:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab63e1d933b90542c55c0589580d0ae8a9e2158b1a513a3f48ad426b6b19dc5`  
		Last Modified: Sat, 24 Oct 2020 00:51:36 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadae91cd7b954aab20e1a7852252f1d899656643f5a93419082e227368c1ba9`  
		Last Modified: Sat, 24 Oct 2020 00:51:48 GMT  
		Size: 39.1 MB (39118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aefd409dfcff320e4f4abc93acd6b79c75be32a4f8e945a7973b16e906f371`  
		Last Modified: Sat, 24 Oct 2020 00:51:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee425345016882213d153f7d97b63547b624b495d324a12f56499a64ec4bff4`  
		Last Modified: Sat, 24 Oct 2020 00:51:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2fb9fc2e5b60fa972411f03c730ae9062ba8f15afb38eb1bdda9787ec92001`  
		Last Modified: Sat, 24 Oct 2020 00:51:37 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.5` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b000c9a1b959e6e0f6a44e692719b859bbcf0a1dfce1457923223ad813de00ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41902164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbca14e16df0a545915052fd53f21614a74fc15be4d8f29f8c0b3778726f9feb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:39:48 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:39:49 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:39:51 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:39:58 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:40:00 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:40:02 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:40:02 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:40:03 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:40:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:40:04 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:40:06 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b6d3b9131728e261c4c4fc3af4cdd89e6dcba8ab1ab38c3c0f914e2eb39560`  
		Last Modified: Sat, 24 Oct 2020 00:40:31 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea498f059520372848099a86a79729c7818c4aebc0f8a0fe20587c848e59f415`  
		Last Modified: Sat, 24 Oct 2020 00:40:39 GMT  
		Size: 39.2 MB (39192313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9301e6a3342587e952ba4823d9d46356ef7f784b57e2e9fd46f14bfe405a08b6`  
		Last Modified: Sat, 24 Oct 2020 00:40:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d987f7d735d43368f22b2d5f0382da052100071025a829c766e8cc328f30f0`  
		Last Modified: Sat, 24 Oct 2020 00:40:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8904802b6e26f57003d8bce038eca94dc3b115a409726918967d41a91ab1a1`  
		Last Modified: Sat, 24 Oct 2020 00:40:31 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.5` - linux; 386

```console
$ docker pull consul@sha256:b2b1abf3a45a2d4aab2e52e4211de930519d7602b448cd4ff1497c4783f2b59e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45976028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c5f30e70866e42e6cd1d5fca57611f44e3806485c2834b90d0a279e121cd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:38:28 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:38:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:38:29 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:38:34 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:38:35 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:38:36 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:38:36 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:38:36 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:38:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:38:37 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:38:37 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:38:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:38:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50575978b96251e969c7433bf747ff9948c7569cdba08b82642c9ff28dc3dad8`  
		Last Modified: Sat, 24 Oct 2020 00:38:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0bd61c7abe46d0a8800e07b99771a4a177768e7951b6e4bc406ef8c1ba5672`  
		Last Modified: Sat, 24 Oct 2020 00:39:04 GMT  
		Size: 43.2 MB (43181392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df109c109076c96fc724f585f9e9b2decc3c9c96a51c0a26891089492f2a793b`  
		Last Modified: Sat, 24 Oct 2020 00:38:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c51e22ab172236135e965946eaf3a7a7a54768ec71cf853a1a6b18c4326df4`  
		Last Modified: Sat, 24 Oct 2020 00:38:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf571036f9872b050d07d5272ddeebf9629fa2af03e0dac3456433ac857abca`  
		Last Modified: Sat, 24 Oct 2020 00:38:56 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.0-beta`

```console
$ docker pull consul@sha256:9b51627ddc586d25a45bc1d9aff393e39e23515e5fb8d35925cb36869fca03a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.0-beta` - linux; amd64

```console
$ docker pull consul@sha256:abc02251f80aba86160621cfc0c544e028f9e0db8a044206164fc23372ec9b70
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47611918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf08ac09b6bf06f275ccc6f6ae352b3e6375e2c778dd01c35c9f935aa9cc4ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:17:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 03:17:54 GMT
ENV CONSUL_VERSION=1.9.0-beta1
# Thu, 22 Oct 2020 03:17:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 03:17:55 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 03:18:00 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 03:18:01 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 03:18:02 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:18:02 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 03:18:02 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 03:18:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 03:18:02 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 03:18:03 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 03:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 03:18:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0df8ffede2b927dbb80ab6b5d85dde12d4a54deb66894bac730c7365ac2c352`  
		Last Modified: Thu, 22 Oct 2020 03:18:52 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75f95902e76e74012391451904c991cda67fe0bc465866a85d84c9d164ff6cc`  
		Last Modified: Thu, 22 Oct 2020 03:18:59 GMT  
		Size: 44.8 MB (44811824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033e314035e7334d913b320d38e978aff3d17678ddf6ad2126d9ef23cfba6a13`  
		Last Modified: Thu, 22 Oct 2020 03:18:51 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62e144d7d318b289f929203b38573e6197d92ba37404dd09e0e6919116f14df`  
		Last Modified: Thu, 22 Oct 2020 03:18:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ea9cfc407560b99f46f9b2e082fc1178e4b759395633e279fae3c405f1484c`  
		Last Modified: Thu, 22 Oct 2020 03:18:51 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.0-beta` - linux; arm variant v6

```console
$ docker pull consul@sha256:e7fc72551958e03470b8c03c19d09000a61b034832fbb55f0f4d738cd85de8b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42755955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb59ad52e173656e0d37e52ad3a2a4ec4a2f0ebf6c9c7afdd0fd0f5da58ca2cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:17:16 GMT
ENV CONSUL_VERSION=1.9.0-beta1
# Thu, 22 Oct 2020 02:17:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:17:19 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:17:29 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:17:33 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:17:36 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:17:37 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:17:38 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:17:39 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:17:40 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:17:41 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:17:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:17:46 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb599ef0b38d2b800e58e74a80f31d7487a726532c8f254d0e05bba6603385`  
		Last Modified: Thu, 22 Oct 2020 02:19:43 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4cec6230bd53ded39135fc8034bcce62320e90a5797428e5163be7b779ea92`  
		Last Modified: Thu, 22 Oct 2020 02:19:55 GMT  
		Size: 40.2 MB (40150746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab0596547824bed8f0b17196a88ba2af9967fc517221e8ea516753a1fe52335`  
		Last Modified: Thu, 22 Oct 2020 02:19:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b977009089ae5433276df5b2f18bc23cb00a63e99d941e5326a26944d85ac313`  
		Last Modified: Thu, 22 Oct 2020 02:19:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b252efd0fcdd733a2d9795e6c91ce4a9a45787ae12a9ad939cdc040486ffe812`  
		Last Modified: Thu, 22 Oct 2020 02:19:43 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.0-beta` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:40546a0a57a5bca1e7df9b3fc2106ad962bd6784307ca5b374e57959608560d6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42928725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d678b6b66c8d7e73effed28b73932b1f8f169b35235b3c8fd618bc3b9cd9e35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:42:39 GMT
ENV CONSUL_VERSION=1.9.0-beta1
# Thu, 22 Oct 2020 02:42:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:42:41 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:42:49 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:42:52 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:42:54 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:42:57 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:42:58 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:43:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:43:02 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:43:03 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:43:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:43:06 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7da2a8d23de5894604ad32a80a1f2d126d574b4a8c7cdf045a22fa0e4474b2`  
		Last Modified: Thu, 22 Oct 2020 02:45:04 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf97b02f0060a7ef5f6a44e897d20fe50b1820572e1d57f2d0a4c90399adaf3a`  
		Last Modified: Thu, 22 Oct 2020 02:45:12 GMT  
		Size: 40.2 MB (40218875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90f956b556e062ccf5b00512e74ad487505409e0c8c739a20c34b0b5be959a9`  
		Last Modified: Thu, 22 Oct 2020 02:45:04 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562e039c4c33e7fdffb4a8f85e7fda3c3ed3eff4261ee20608c3d144d0512afc`  
		Last Modified: Thu, 22 Oct 2020 02:45:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb23a4d41b227257d9c4d1c9452f49b5125ed9e4851f0690f88f3123ef661066`  
		Last Modified: Thu, 22 Oct 2020 02:45:04 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.0-beta` - linux; 386

```console
$ docker pull consul@sha256:5e065d9760024fe3580a52b9f063732fa986b52c91ff878399640bbd16faf894
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47138871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c68f91828b5d862325406a94f6ba7867a7c5cc90a4bdca28944e1b750ecc1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Thu, 22 Oct 2020 02:32:48 GMT
ENV CONSUL_VERSION=1.9.0-beta1
# Thu, 22 Oct 2020 02:32:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 22 Oct 2020 02:32:49 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 22 Oct 2020 02:32:54 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 22 Oct 2020 02:32:55 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 22 Oct 2020 02:32:56 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:32:56 GMT
VOLUME [/consul/data]
# Thu, 22 Oct 2020 02:32:56 GMT
EXPOSE 8300
# Thu, 22 Oct 2020 02:32:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 22 Oct 2020 02:32:56 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 22 Oct 2020 02:32:57 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Oct 2020 02:32:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 02:32:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9938449d4230918267ff788aabd4f1fb43fee53ade28166cba4854e13ee7d7e7`  
		Last Modified: Thu, 22 Oct 2020 02:33:50 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3248c43e54d8a39258c71eccacf966b1f371f15cb7de1c3b6104d9100ea8a5f1`  
		Last Modified: Thu, 22 Oct 2020 02:33:57 GMT  
		Size: 44.3 MB (44344230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0a0b3ecd556a5deda07794e649446be448e4f6347991a01e1c26bf6cf6b574`  
		Last Modified: Thu, 22 Oct 2020 02:33:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0dd6a9d0f77164977ec00259936c24a979ee022a753a7c9d72744a13359565`  
		Last Modified: Thu, 22 Oct 2020 02:33:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883cb925e3f5da96924b31152da91c1b2a599d78c0e77bc426b1cc1d1d610c6d`  
		Last Modified: Thu, 22 Oct 2020 02:33:49 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.0-beta2`

**does not exist** (yet?)

## `consul:latest`

```console
$ docker pull consul@sha256:b85322aa8c65355341dd81b5e95d5c0e8468e6419724d4e8a125198d40426a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:43eb37c372432743a4a7334f41dfde3aeac2e08ec6698c79cb23a6550898bff3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46463818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b214361a700e6ca4a014ff49035be3678c9375ba478a7b20bd0859bdcd9a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:17:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:19:39 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:19:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:19:40 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:19:45 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:19:45 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:19:46 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:19:46 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:19:46 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:19:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:19:47 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:19:47 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:19:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd0ad15d15483ddb156f9f3f293505ab3d80dd4f0298f988e53879107c17045`  
		Last Modified: Sat, 24 Oct 2020 00:20:05 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d30a01add5552182d8cf627fb6bfafb1bd6404bd9e8964d0f318e75ac909292`  
		Last Modified: Sat, 24 Oct 2020 00:20:11 GMT  
		Size: 43.7 MB (43663725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f3ae3ba267f18945e80a9a9d9b1aa4e960addad7330381e1eebeb178e893c1`  
		Last Modified: Sat, 24 Oct 2020 00:20:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0e80834954020a245984ab98e3a34b047ac702b81eb4674171d53caf4c95b`  
		Last Modified: Sat, 24 Oct 2020 00:20:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f607b07c9f2cfc208634b1170ebbfa675e6de56058826fec0ede6e593289b`  
		Last Modified: Sat, 24 Oct 2020 00:20:05 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:9cba8ea4acf03eec79ac41b0b0e86ef5d23819bcfaab38ad7d12aa4af5e3f86d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41724116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e7e84124bc9a52ebf375f54aa75182a64a07c13a9941e005da0cf936bcfb94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:17:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:50:53 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:50:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:50:55 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:51:03 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:51:06 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:51:08 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:51:10 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:51:11 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:51:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:51:13 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:51:13 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:51:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab63e1d933b90542c55c0589580d0ae8a9e2158b1a513a3f48ad426b6b19dc5`  
		Last Modified: Sat, 24 Oct 2020 00:51:36 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadae91cd7b954aab20e1a7852252f1d899656643f5a93419082e227368c1ba9`  
		Last Modified: Sat, 24 Oct 2020 00:51:48 GMT  
		Size: 39.1 MB (39118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aefd409dfcff320e4f4abc93acd6b79c75be32a4f8e945a7973b16e906f371`  
		Last Modified: Sat, 24 Oct 2020 00:51:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee425345016882213d153f7d97b63547b624b495d324a12f56499a64ec4bff4`  
		Last Modified: Sat, 24 Oct 2020 00:51:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2fb9fc2e5b60fa972411f03c730ae9062ba8f15afb38eb1bdda9787ec92001`  
		Last Modified: Sat, 24 Oct 2020 00:51:37 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b000c9a1b959e6e0f6a44e692719b859bbcf0a1dfce1457923223ad813de00ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41902164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbca14e16df0a545915052fd53f21614a74fc15be4d8f29f8c0b3778726f9feb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:42:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:39:48 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:39:49 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:39:51 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:39:58 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:40:00 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:40:02 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:40:02 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:40:03 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:40:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:40:04 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:40:06 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b6d3b9131728e261c4c4fc3af4cdd89e6dcba8ab1ab38c3c0f914e2eb39560`  
		Last Modified: Sat, 24 Oct 2020 00:40:31 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea498f059520372848099a86a79729c7818c4aebc0f8a0fe20587c848e59f415`  
		Last Modified: Sat, 24 Oct 2020 00:40:39 GMT  
		Size: 39.2 MB (39192313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9301e6a3342587e952ba4823d9d46356ef7f784b57e2e9fd46f14bfe405a08b6`  
		Last Modified: Sat, 24 Oct 2020 00:40:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d987f7d735d43368f22b2d5f0382da052100071025a829c766e8cc328f30f0`  
		Last Modified: Sat, 24 Oct 2020 00:40:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8904802b6e26f57003d8bce038eca94dc3b115a409726918967d41a91ab1a1`  
		Last Modified: Sat, 24 Oct 2020 00:40:31 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:b2b1abf3a45a2d4aab2e52e4211de930519d7602b448cd4ff1497c4783f2b59e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45976028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c5f30e70866e42e6cd1d5fca57611f44e3806485c2834b90d0a279e121cd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:32:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 24 Oct 2020 00:38:28 GMT
ENV CONSUL_VERSION=1.8.5
# Sat, 24 Oct 2020 00:38:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 24 Oct 2020 00:38:29 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 24 Oct 2020 00:38:34 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 24 Oct 2020 00:38:35 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 24 Oct 2020 00:38:36 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 24 Oct 2020 00:38:36 GMT
VOLUME [/consul/data]
# Sat, 24 Oct 2020 00:38:36 GMT
EXPOSE 8300
# Sat, 24 Oct 2020 00:38:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 24 Oct 2020 00:38:37 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 24 Oct 2020 00:38:37 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 24 Oct 2020 00:38:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 24 Oct 2020 00:38:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50575978b96251e969c7433bf747ff9948c7569cdba08b82642c9ff28dc3dad8`  
		Last Modified: Sat, 24 Oct 2020 00:38:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0bd61c7abe46d0a8800e07b99771a4a177768e7951b6e4bc406ef8c1ba5672`  
		Last Modified: Sat, 24 Oct 2020 00:39:04 GMT  
		Size: 43.2 MB (43181392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df109c109076c96fc724f585f9e9b2decc3c9c96a51c0a26891089492f2a793b`  
		Last Modified: Sat, 24 Oct 2020 00:38:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c51e22ab172236135e965946eaf3a7a7a54768ec71cf853a1a6b18c4326df4`  
		Last Modified: Sat, 24 Oct 2020 00:38:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf571036f9872b050d07d5272ddeebf9629fa2af03e0dac3456433ac857abca`  
		Last Modified: Sat, 24 Oct 2020 00:38:56 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
