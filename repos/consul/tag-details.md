<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.7`](#consul17)
-	[`consul:1.7.11`](#consul1711)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.7`](#consul187)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.1`](#consul191)
-	[`consul:latest`](#consullatest)

## `consul:1.7`

```console
$ docker pull consul@sha256:cde7e3f1710954dd06145583fb0e72d3be97c57c5a5410663c1f3c09eded7d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7` - linux; amd64

```console
$ docker pull consul@sha256:bc16b5304bdcc40a3cea9f6c106363434717586467744d1ce78b2e63a1e5dc6f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43093842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bd34dbc3c3f1f7f4b43cd12ed01b4015baa93ac1392d2b07a12689c6254721`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:56:13 GMT
ENV CONSUL_VERSION=1.7.10
# Fri, 11 Dec 2020 02:56:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:56:15 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:56:22 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:56:24 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:56:25 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:56:25 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:56:25 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:56:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:56:26 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:56:26 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:56:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574c36a12202c0f0e34f4b8bf84ddde9f9a0924c19895a461058527f3a0a2cdd`  
		Last Modified: Fri, 11 Dec 2020 02:57:55 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0855f7e506d7ddff6882d7974e8eb68c3505d7c723ad5698323743bd64fcd902`  
		Last Modified: Fri, 11 Dec 2020 02:58:04 GMT  
		Size: 40.3 MB (40293661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1238aa95aaba6e5cdc6775497bf004a2e4228df6c8da4e7b2bfa7ef9c4f794`  
		Last Modified: Fri, 11 Dec 2020 02:57:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b6c78cc972e1067d1fd8489942639d41f191f3905fc0ce3a2e7130aac3d1be`  
		Last Modified: Fri, 11 Dec 2020 02:57:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02172411f977cfe47523404a06fd5b7b3d3cda3780e621ca6740a4431d8e236`  
		Last Modified: Fri, 11 Dec 2020 02:57:54 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:f2dce1c8bfcf33d175732fe0ef56342674735edb3be2224f65a341cbec18b3c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38812406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f691a1d42bb1229ec76bd15c35360f0584fa52ad6f32c6d1581c35753a197d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:12:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 00:55:24 GMT
ENV CONSUL_VERSION=1.7.11
# Sat, 12 Dec 2020 00:55:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 00:55:30 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 00:55:42 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 00:55:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 00:55:49 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 00:55:50 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 00:55:55 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 00:55:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 00:55:58 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 00:55:59 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 00:56:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 00:56:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c131071c301e2d6e6f5d5a5eefb8d6932e5a4f4077ffd76525ebe1553258ab3f`  
		Last Modified: Sat, 12 Dec 2020 00:57:08 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad9bae7fe82dcc03de361eae7942072cb328d4470ad1f235f375e8d20b0eec6`  
		Last Modified: Sat, 12 Dec 2020 00:57:18 GMT  
		Size: 36.2 MB (36207123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371c83906741a4af030f924c9adaae9d4f7a6383f8a400ace5baf03163eabaf1`  
		Last Modified: Sat, 12 Dec 2020 00:57:08 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860a4026e11b38efec011508b265799304407bed92877804317bbd3828455152`  
		Last Modified: Sat, 12 Dec 2020 00:57:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b5950edec2988c46cc03ca2a8562adfae3399761b2aa13145cf97b96958433`  
		Last Modified: Sat, 12 Dec 2020 00:57:09 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:5741d7cbcdbcdee8df6fd569dd0a1821026610ffad717deb8b0d7447078b46c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39020690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d84b92201c235c95047f58df92783a12f112e6201855e360450c0fcc3f9ef16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:36:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 14:08:32 GMT
ENV CONSUL_VERSION=1.7.11
# Sat, 12 Dec 2020 14:08:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 14:08:35 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 14:08:42 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 14:08:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 14:08:48 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 14:08:49 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 14:08:49 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 14:08:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 14:08:51 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 14:08:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 14:08:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 14:08:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2013218a4de91072d128f42f581a286f763ca311ba03a40919119c685eac0f41`  
		Last Modified: Sat, 12 Dec 2020 14:09:46 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358f4028c41610ee96392fb6837b2c2060e820f9cae0e700541965028084ad22`  
		Last Modified: Sat, 12 Dec 2020 14:09:54 GMT  
		Size: 36.3 MB (36310779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5349efa350c0ffd84c5fc595d20cb1bc02ac5dcd8d3cc454cc42d97247ec774`  
		Last Modified: Sat, 12 Dec 2020 14:09:46 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf3ea6c2326d360c03390f51b0ecbf53ca155f3b4d9315a0c40289c041edbd7`  
		Last Modified: Sat, 12 Dec 2020 14:09:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c0f0523202f2ac153b3cddf46ef3f6fb4d15972464c94a8cd03910ecac4486`  
		Last Modified: Sat, 12 Dec 2020 14:09:46 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; 386

```console
$ docker pull consul@sha256:fa2995deadb49259c2821a61076b7508ca114b783c9974892827a7a3ac4d90d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41899460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9c09e1209cfd388e3163734cc25736c17867dc0c81db591a4f55af55c18c86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:01:14 GMT
ADD file:8812e502f26af2dc4efdfb7387f8bf99f2a098b6c95b9f6abf900df2ce74e3da in / 
# Fri, 11 Dec 2020 02:01:14 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:57:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 05:58:24 GMT
ENV CONSUL_VERSION=1.7.10
# Fri, 11 Dec 2020 05:58:24 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 05:58:25 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 05:58:30 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 05:58:31 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 05:58:32 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:58:32 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 05:58:32 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 05:58:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 05:58:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 05:58:33 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 05:58:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:58:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b62269920a7a62a905817c7c1b33f33b6e658121e9a054715ff052a23f7de3a0`  
		Last Modified: Fri, 11 Dec 2020 02:01:43 GMT  
		Size: 2.8 MB (2791504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cc0f6337d59b4f548d58ec56698a57d683ff821774692e5ca36700323e3e27`  
		Last Modified: Fri, 11 Dec 2020 05:59:48 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bde287b2ce9b4cd93c59e085663fc0ef9ec7d645c9ca3b0e6a8528450a5082`  
		Last Modified: Fri, 11 Dec 2020 05:59:55 GMT  
		Size: 39.1 MB (39104726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fa7e1c5063e3685ccb2cf8fd22f93c23168f1dcf048f7c157d77d0de90dc7e`  
		Last Modified: Fri, 11 Dec 2020 05:59:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9143144e1c3b602b450b4c2e2e340d965095f4532be4e2c72bb0197affa879cb`  
		Last Modified: Fri, 11 Dec 2020 05:59:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2c20f4ce0e208b444438ab9ac69e85751340626733638110e138117be30e83`  
		Last Modified: Fri, 11 Dec 2020 05:59:47 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7.11`

```console
$ docker pull consul@sha256:1f7fd9ee1fd425517f10e549166acc27d5a7fb8c882b53498ad8b588411a6af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `consul:1.7.11` - linux; arm variant v6

```console
$ docker pull consul@sha256:f2dce1c8bfcf33d175732fe0ef56342674735edb3be2224f65a341cbec18b3c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38812406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f691a1d42bb1229ec76bd15c35360f0584fa52ad6f32c6d1581c35753a197d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:12:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 00:55:24 GMT
ENV CONSUL_VERSION=1.7.11
# Sat, 12 Dec 2020 00:55:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 00:55:30 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 00:55:42 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 00:55:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 00:55:49 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 00:55:50 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 00:55:55 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 00:55:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 00:55:58 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 00:55:59 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 00:56:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 00:56:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c131071c301e2d6e6f5d5a5eefb8d6932e5a4f4077ffd76525ebe1553258ab3f`  
		Last Modified: Sat, 12 Dec 2020 00:57:08 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad9bae7fe82dcc03de361eae7942072cb328d4470ad1f235f375e8d20b0eec6`  
		Last Modified: Sat, 12 Dec 2020 00:57:18 GMT  
		Size: 36.2 MB (36207123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371c83906741a4af030f924c9adaae9d4f7a6383f8a400ace5baf03163eabaf1`  
		Last Modified: Sat, 12 Dec 2020 00:57:08 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860a4026e11b38efec011508b265799304407bed92877804317bbd3828455152`  
		Last Modified: Sat, 12 Dec 2020 00:57:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b5950edec2988c46cc03ca2a8562adfae3399761b2aa13145cf97b96958433`  
		Last Modified: Sat, 12 Dec 2020 00:57:09 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.11` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:5741d7cbcdbcdee8df6fd569dd0a1821026610ffad717deb8b0d7447078b46c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39020690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d84b92201c235c95047f58df92783a12f112e6201855e360450c0fcc3f9ef16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:36:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 14:08:32 GMT
ENV CONSUL_VERSION=1.7.11
# Sat, 12 Dec 2020 14:08:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 14:08:35 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 14:08:42 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 14:08:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 14:08:48 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 14:08:49 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 14:08:49 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 14:08:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 14:08:51 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 14:08:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 14:08:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 14:08:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2013218a4de91072d128f42f581a286f763ca311ba03a40919119c685eac0f41`  
		Last Modified: Sat, 12 Dec 2020 14:09:46 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358f4028c41610ee96392fb6837b2c2060e820f9cae0e700541965028084ad22`  
		Last Modified: Sat, 12 Dec 2020 14:09:54 GMT  
		Size: 36.3 MB (36310779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5349efa350c0ffd84c5fc595d20cb1bc02ac5dcd8d3cc454cc42d97247ec774`  
		Last Modified: Sat, 12 Dec 2020 14:09:46 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf3ea6c2326d360c03390f51b0ecbf53ca155f3b4d9315a0c40289c041edbd7`  
		Last Modified: Sat, 12 Dec 2020 14:09:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c0f0523202f2ac153b3cddf46ef3f6fb4d15972464c94a8cd03910ecac4486`  
		Last Modified: Sat, 12 Dec 2020 14:09:46 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:4adebccbcf42869ba975845d925ad05ecc3ccf9aa78b25ad1b2c38e074a9581f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:3efabf42b246dae092b236df440d95b25cc79f08941128653fbb490d8068f779
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46461787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36094c09e82962f378f08056864385d0ac1a28ef278b9050423de34b6bd2d07d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:55:54 GMT
ENV CONSUL_VERSION=1.8.6
# Fri, 11 Dec 2020 02:55:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:55:56 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:56:03 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:56:04 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:56:06 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:56:06 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:56:06 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:56:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:56:07 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:56:07 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:56:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:56:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe56e704066b43589bb857c9465831a2c34bbbef933b423569c4afe1f8511e3`  
		Last Modified: Fri, 11 Dec 2020 02:57:37 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7854da3823fa235c4710a7558b08efd96290dd80cf0c0252c3100b83f264dfc5`  
		Last Modified: Fri, 11 Dec 2020 02:57:47 GMT  
		Size: 43.7 MB (43661611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b68bd84e508f434ab57fdd39663b88c3e9541e86b01051eb13f41e02049edaa`  
		Last Modified: Fri, 11 Dec 2020 02:57:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8494b9fb8d1cc1a0ce36ca17d71f50be0eeb0a299ac3fa836fc54beb2a75e4d`  
		Last Modified: Fri, 11 Dec 2020 02:57:38 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cce9eef4f2ebc00b962a237fa3e9451a52b28d2d744e48f2ee9d751b4c8d2f0`  
		Last Modified: Fri, 11 Dec 2020 02:57:38 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:d78749199ec26b1313131548f125f1595bcaba8f19fa40eff30a6eb6d05b2f62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41749676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4486a0b825fa5403d9d2449076e560f2b30976a4ae39ecd82fd97f222007be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:12:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 00:54:32 GMT
ENV CONSUL_VERSION=1.8.7
# Sat, 12 Dec 2020 00:54:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 00:54:44 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 00:54:56 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 00:55:01 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 00:55:05 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 00:55:06 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 00:55:08 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 00:55:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 00:55:11 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 00:55:12 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 00:55:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 00:55:17 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f867519477f47aa70333212857fd1ddb46b69bf4b98f518e1bbe496438bef1e`  
		Last Modified: Sat, 12 Dec 2020 00:56:44 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac0e237f16c96907f707d86f37dda73ac40da0793884c2bb4fa1e67fbccbc04`  
		Last Modified: Sat, 12 Dec 2020 00:56:54 GMT  
		Size: 39.1 MB (39144390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74c932c87fa8ab2b3cd86e4bf0aef7aa6adc3ed9fa50da38be177307f3c563c`  
		Last Modified: Sat, 12 Dec 2020 00:56:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccf3c7a7aa5c54f02663b1de91e984939c9f1354c58aee6a6a3aa3c8d27ba2b`  
		Last Modified: Sat, 12 Dec 2020 00:56:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab18aa67b4fa150d63f8e9e8a82430c854fcf2e0de132e88d335c1bec6cea07`  
		Last Modified: Sat, 12 Dec 2020 00:56:43 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1a35f1ef79f8c8485f695a16385f32aa161c7d72e54fc7533bfdbb1b512bc99d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41922422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302ba2caae5a6a35ad9f35271c7684c2d15befe556695f5367ba1f143731340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:36:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 14:08:04 GMT
ENV CONSUL_VERSION=1.8.7
# Sat, 12 Dec 2020 14:08:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 14:08:08 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 14:08:14 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 14:08:17 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 14:08:18 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 14:08:19 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 14:08:20 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 14:08:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 14:08:21 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 14:08:22 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 14:08:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 14:08:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd7aff50e3b65b8c18402716fd1ce5d2d97de2bf856953410d51b1082b1b7f`  
		Last Modified: Sat, 12 Dec 2020 14:09:27 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c0d7faf267bf65aba7a1d0e9f8562170e12c03e7bbf12260d44fcefeab243a`  
		Last Modified: Sat, 12 Dec 2020 14:09:36 GMT  
		Size: 39.2 MB (39212510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c39d9c93d21f37cd1d1003d0912ffa8c5560292d3206e39318bb7588d820fa`  
		Last Modified: Sat, 12 Dec 2020 14:09:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3a1facbf5164132306c810a5016c33aea489b57da3975ac0face40c38c4c70`  
		Last Modified: Sat, 12 Dec 2020 14:09:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fda8a31b605c2fe24343e315f58d5cf3ec4d8b50aa97fa26d3c71de60c24b4`  
		Last Modified: Sat, 12 Dec 2020 14:09:27 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:85fefe5602dd831f39cc48ba305214e9a58d3fa716aad75d1690a1768b407983
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45977770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4f6e5c399bd188b5db02a18b4fd7ddb2a4b11188bc6acd509f4b9c14021d72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:01:14 GMT
ADD file:8812e502f26af2dc4efdfb7387f8bf99f2a098b6c95b9f6abf900df2ce74e3da in / 
# Fri, 11 Dec 2020 02:01:14 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:57:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 05:58:09 GMT
ENV CONSUL_VERSION=1.8.6
# Fri, 11 Dec 2020 05:58:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 05:58:10 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 05:58:16 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 05:58:16 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 05:58:17 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:58:17 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 05:58:18 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 05:58:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 05:58:18 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 05:58:18 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 05:58:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:58:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b62269920a7a62a905817c7c1b33f33b6e658121e9a054715ff052a23f7de3a0`  
		Last Modified: Fri, 11 Dec 2020 02:01:43 GMT  
		Size: 2.8 MB (2791504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3b9efcaeb2dbc7ef5c8359ca60af2d6eacfe9b8cec10c676a7224b61b29f45`  
		Last Modified: Fri, 11 Dec 2020 05:59:33 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007d39e8e687f4cbc4651839da96cb525195a2c56555a6a5de6a49494c0bff60`  
		Last Modified: Fri, 11 Dec 2020 05:59:42 GMT  
		Size: 43.2 MB (43183041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e863958157023ad0dad39cf7496ac2d3c55b7106693634db00d48d07646cb0`  
		Last Modified: Fri, 11 Dec 2020 05:59:33 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed9bf5bd61a919fbe3f6067e80644c2dd6c67b8b0d814501d7423f48a6d5c39`  
		Last Modified: Fri, 11 Dec 2020 05:59:33 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c85341267d481eeb94983ec273ea114ab2e11fd6e4ff694154b2ae1ccf5d02`  
		Last Modified: Fri, 11 Dec 2020 05:59:33 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.7`

```console
$ docker pull consul@sha256:b52612d14cc475a0cc028a22a3c9012e23cb6571c91b32b6b0bfd6c5f7a8d672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `consul:1.8.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:d78749199ec26b1313131548f125f1595bcaba8f19fa40eff30a6eb6d05b2f62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41749676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4486a0b825fa5403d9d2449076e560f2b30976a4ae39ecd82fd97f222007be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:12:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 00:54:32 GMT
ENV CONSUL_VERSION=1.8.7
# Sat, 12 Dec 2020 00:54:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 00:54:44 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 00:54:56 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 00:55:01 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 00:55:05 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 00:55:06 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 00:55:08 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 00:55:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 00:55:11 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 00:55:12 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 00:55:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 00:55:17 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f867519477f47aa70333212857fd1ddb46b69bf4b98f518e1bbe496438bef1e`  
		Last Modified: Sat, 12 Dec 2020 00:56:44 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac0e237f16c96907f707d86f37dda73ac40da0793884c2bb4fa1e67fbccbc04`  
		Last Modified: Sat, 12 Dec 2020 00:56:54 GMT  
		Size: 39.1 MB (39144390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74c932c87fa8ab2b3cd86e4bf0aef7aa6adc3ed9fa50da38be177307f3c563c`  
		Last Modified: Sat, 12 Dec 2020 00:56:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccf3c7a7aa5c54f02663b1de91e984939c9f1354c58aee6a6a3aa3c8d27ba2b`  
		Last Modified: Sat, 12 Dec 2020 00:56:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab18aa67b4fa150d63f8e9e8a82430c854fcf2e0de132e88d335c1bec6cea07`  
		Last Modified: Sat, 12 Dec 2020 00:56:43 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1a35f1ef79f8c8485f695a16385f32aa161c7d72e54fc7533bfdbb1b512bc99d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41922422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302ba2caae5a6a35ad9f35271c7684c2d15befe556695f5367ba1f143731340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:36:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 14:08:04 GMT
ENV CONSUL_VERSION=1.8.7
# Sat, 12 Dec 2020 14:08:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 14:08:08 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 14:08:14 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 14:08:17 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 14:08:18 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 14:08:19 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 14:08:20 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 14:08:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 14:08:21 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 14:08:22 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 14:08:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 14:08:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebd7aff50e3b65b8c18402716fd1ce5d2d97de2bf856953410d51b1082b1b7f`  
		Last Modified: Sat, 12 Dec 2020 14:09:27 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c0d7faf267bf65aba7a1d0e9f8562170e12c03e7bbf12260d44fcefeab243a`  
		Last Modified: Sat, 12 Dec 2020 14:09:36 GMT  
		Size: 39.2 MB (39212510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c39d9c93d21f37cd1d1003d0912ffa8c5560292d3206e39318bb7588d820fa`  
		Last Modified: Sat, 12 Dec 2020 14:09:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3a1facbf5164132306c810a5016c33aea489b57da3975ac0face40c38c4c70`  
		Last Modified: Sat, 12 Dec 2020 14:09:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fda8a31b605c2fe24343e315f58d5cf3ec4d8b50aa97fa26d3c71de60c24b4`  
		Last Modified: Sat, 12 Dec 2020 14:09:27 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:c69b4d4bff41aff8e40ff084f9bd6a379995f5163880860fc2dd49a1c6006817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:3aeb5ab2d0fa9189ed99692f8cce218d1c5eb591255ac38c389b680aad3bd5bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8429e82f47dd20c7833966453d571fc43ece763fa5cadec460390351f99d839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:55:15 GMT
ENV CONSUL_VERSION=1.9.0
# Fri, 11 Dec 2020 02:55:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:55:17 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:55:24 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:55:26 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:55:27 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:55:28 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:55:29 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:55:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:55:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dc5b4d599656ad90b0d9809894af2414f9ffadb68145140f4038ecac2eb174`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07ae847c23d3422b795a3bdf170616176238924d44bb8b99503f34b86222246`  
		Last Modified: Fri, 11 Dec 2020 02:57:17 GMT  
		Size: 42.7 MB (42720248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f01f506e7a1412784c106cd451bf530c4e2fa89b82da5494eb7fcee179ee04`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54d30ff31eeef79e6a8ecf14d92c4324b82f4be1176b8a22b89172bdbb1e535`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0811e7d6f99e0f9f0104dbcbb3682d6b9da402b2d9993c9ba173c6c014904e3`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:ba2cf92ad7a299b67b0836ec07dc80362f4e4983ef588cf78778a5c8b1453a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40832579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41486a63c4ded8d1f8cac34fd763459ae65be3c5802bef1fed8232cc2f8336d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:12:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 00:53:40 GMT
ENV CONSUL_VERSION=1.9.1
# Sat, 12 Dec 2020 00:53:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 00:53:46 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 00:53:56 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 00:53:58 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 00:54:02 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 00:54:03 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 00:54:04 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 00:54:05 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 00:54:08 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 00:54:12 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 00:54:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 00:54:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f07005897aa5ca7dc61824b38a71822bf3c41d8ee1381f410f3cec7e71295e`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0abaf0b0db4322f0c362e05a8f33b4bd9459c9e5b10d7fb9460d51bd0aec91`  
		Last Modified: Sat, 12 Dec 2020 00:56:33 GMT  
		Size: 38.2 MB (38227295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd18ac82951699c3cf6a5d413f6934917c183b4e08716016d14566525a71bcd0`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5326c928d9eb761f450fad803c5bc4643fa105e666092783558b85557c8b3bc0`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48742b61655f27ca3ed3c85be1b091efb7b1e1024749a53d4984a4c1e178bf8d`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:01d2cef184a6ff688693974cfcc36c5d92f9a37832381b2a008e460b26d358f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41052267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e983dda7fd04f095f885f204ae5c644845ca023ce29555418af478cf5d046c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:36:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 14:07:35 GMT
ENV CONSUL_VERSION=1.9.1
# Sat, 12 Dec 2020 14:07:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 14:07:37 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 14:07:44 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 14:07:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 14:07:50 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 14:07:51 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 14:07:52 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 14:07:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 14:07:55 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 14:07:55 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 14:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 14:07:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c8060704c53f3ff052629f979f702282b4cdedc728a02c83ddfcb511067de2`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fc274a81c60ca4deddc3eb2021465a3cacb68e5c35024212cf02fa2a3055da`  
		Last Modified: Sat, 12 Dec 2020 14:09:16 GMT  
		Size: 38.3 MB (38342356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421085bf757533067046c72d4f76aa17383fe82a1c5a709df6015e5f3f7a3af3`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92d7c3c09e2f09ab13919755506eb2699a0dbcf2b107a570e6bc9ca536be912`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa6ebe29a594ab16a614fc400231c0e5d0b79f316e51ebf17b0ebcdd0db9875`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:011cea977b0f335aa8b43b049fda85bf3097213f272f015e0aa1382b823fdf25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44857211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1eeaaeaef66065328787653703bd3bd70f8c89e440efe723b9cd3a0937ec5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:01:14 GMT
ADD file:8812e502f26af2dc4efdfb7387f8bf99f2a098b6c95b9f6abf900df2ce74e3da in / 
# Fri, 11 Dec 2020 02:01:14 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:57:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 05:57:39 GMT
ENV CONSUL_VERSION=1.9.0
# Fri, 11 Dec 2020 05:57:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 05:57:40 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 05:57:45 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 05:57:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 05:57:47 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:47 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 05:57:47 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 05:57:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 05:57:48 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 05:57:48 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 05:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:57:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b62269920a7a62a905817c7c1b33f33b6e658121e9a054715ff052a23f7de3a0`  
		Last Modified: Fri, 11 Dec 2020 02:01:43 GMT  
		Size: 2.8 MB (2791504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d19e00b093c0916475a088f3ed6f9b2639fae7165fe16c97995381ed277a07`  
		Last Modified: Fri, 11 Dec 2020 05:59:05 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1fe592dd342b87165eefaac9626321a0ce7cd0b444d845de3b1d8ea7051bd0`  
		Last Modified: Fri, 11 Dec 2020 05:59:13 GMT  
		Size: 42.1 MB (42062481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2683019cdf3b191a80f3576881b606b43d49d40cd3e8479212ecad67252266`  
		Last Modified: Fri, 11 Dec 2020 05:59:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38303cbe4569f0323c09593536c06fc4e346a343ddf40ffe6f73ecb19d5ffaa`  
		Last Modified: Fri, 11 Dec 2020 05:59:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be8941323c8b19851764f2fc37934a92e4f6e8b1b67b4360ab67fecdc797b43`  
		Last Modified: Fri, 11 Dec 2020 05:59:05 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.1`

```console
$ docker pull consul@sha256:21917af5c15e7db66335d8402a85e158ab6e1c9f75f34ff162ad1c76f61d1179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `consul:1.9.1` - linux; arm variant v6

```console
$ docker pull consul@sha256:ba2cf92ad7a299b67b0836ec07dc80362f4e4983ef588cf78778a5c8b1453a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40832579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41486a63c4ded8d1f8cac34fd763459ae65be3c5802bef1fed8232cc2f8336d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:12:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 00:53:40 GMT
ENV CONSUL_VERSION=1.9.1
# Sat, 12 Dec 2020 00:53:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 00:53:46 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 00:53:56 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 00:53:58 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 00:54:02 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 00:54:03 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 00:54:04 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 00:54:05 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 00:54:08 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 00:54:12 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 00:54:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 00:54:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f07005897aa5ca7dc61824b38a71822bf3c41d8ee1381f410f3cec7e71295e`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0abaf0b0db4322f0c362e05a8f33b4bd9459c9e5b10d7fb9460d51bd0aec91`  
		Last Modified: Sat, 12 Dec 2020 00:56:33 GMT  
		Size: 38.2 MB (38227295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd18ac82951699c3cf6a5d413f6934917c183b4e08716016d14566525a71bcd0`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5326c928d9eb761f450fad803c5bc4643fa105e666092783558b85557c8b3bc0`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48742b61655f27ca3ed3c85be1b091efb7b1e1024749a53d4984a4c1e178bf8d`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.1` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:01d2cef184a6ff688693974cfcc36c5d92f9a37832381b2a008e460b26d358f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41052267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e983dda7fd04f095f885f204ae5c644845ca023ce29555418af478cf5d046c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:36:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 14:07:35 GMT
ENV CONSUL_VERSION=1.9.1
# Sat, 12 Dec 2020 14:07:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 14:07:37 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 14:07:44 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 14:07:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 14:07:50 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 14:07:51 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 14:07:52 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 14:07:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 14:07:55 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 14:07:55 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 14:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 14:07:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c8060704c53f3ff052629f979f702282b4cdedc728a02c83ddfcb511067de2`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fc274a81c60ca4deddc3eb2021465a3cacb68e5c35024212cf02fa2a3055da`  
		Last Modified: Sat, 12 Dec 2020 14:09:16 GMT  
		Size: 38.3 MB (38342356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421085bf757533067046c72d4f76aa17383fe82a1c5a709df6015e5f3f7a3af3`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92d7c3c09e2f09ab13919755506eb2699a0dbcf2b107a570e6bc9ca536be912`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa6ebe29a594ab16a614fc400231c0e5d0b79f316e51ebf17b0ebcdd0db9875`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:c69b4d4bff41aff8e40ff084f9bd6a379995f5163880860fc2dd49a1c6006817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:3aeb5ab2d0fa9189ed99692f8cce218d1c5eb591255ac38c389b680aad3bd5bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8429e82f47dd20c7833966453d571fc43ece763fa5cadec460390351f99d839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:55:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 02:55:15 GMT
ENV CONSUL_VERSION=1.9.0
# Fri, 11 Dec 2020 02:55:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 02:55:17 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 02:55:24 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 02:55:26 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 02:55:27 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:55:28 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 02:55:28 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 02:55:29 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 02:55:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 02:55:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dc5b4d599656ad90b0d9809894af2414f9ffadb68145140f4038ecac2eb174`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07ae847c23d3422b795a3bdf170616176238924d44bb8b99503f34b86222246`  
		Last Modified: Fri, 11 Dec 2020 02:57:17 GMT  
		Size: 42.7 MB (42720248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f01f506e7a1412784c106cd451bf530c4e2fa89b82da5494eb7fcee179ee04`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54d30ff31eeef79e6a8ecf14d92c4324b82f4be1176b8a22b89172bdbb1e535`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0811e7d6f99e0f9f0104dbcbb3682d6b9da402b2d9993c9ba173c6c014904e3`  
		Last Modified: Fri, 11 Dec 2020 02:57:08 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:ba2cf92ad7a299b67b0836ec07dc80362f4e4983ef588cf78778a5c8b1453a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40832579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41486a63c4ded8d1f8cac34fd763459ae65be3c5802bef1fed8232cc2f8336d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:12:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 00:53:40 GMT
ENV CONSUL_VERSION=1.9.1
# Sat, 12 Dec 2020 00:53:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 00:53:46 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 00:53:56 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 00:53:58 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 00:54:02 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 00:54:03 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 00:54:04 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 00:54:05 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 00:54:08 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 00:54:12 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 00:54:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 00:54:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f07005897aa5ca7dc61824b38a71822bf3c41d8ee1381f410f3cec7e71295e`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0abaf0b0db4322f0c362e05a8f33b4bd9459c9e5b10d7fb9460d51bd0aec91`  
		Last Modified: Sat, 12 Dec 2020 00:56:33 GMT  
		Size: 38.2 MB (38227295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd18ac82951699c3cf6a5d413f6934917c183b4e08716016d14566525a71bcd0`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5326c928d9eb761f450fad803c5bc4643fa105e666092783558b85557c8b3bc0`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48742b61655f27ca3ed3c85be1b091efb7b1e1024749a53d4984a4c1e178bf8d`  
		Last Modified: Sat, 12 Dec 2020 00:56:24 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:01d2cef184a6ff688693974cfcc36c5d92f9a37832381b2a008e460b26d358f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41052267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e983dda7fd04f095f885f204ae5c644845ca023ce29555418af478cf5d046c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:36:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Sat, 12 Dec 2020 14:07:35 GMT
ENV CONSUL_VERSION=1.9.1
# Sat, 12 Dec 2020 14:07:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 12 Dec 2020 14:07:37 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 12 Dec 2020 14:07:44 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 12 Dec 2020 14:07:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 12 Dec 2020 14:07:50 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 12 Dec 2020 14:07:51 GMT
VOLUME [/consul/data]
# Sat, 12 Dec 2020 14:07:52 GMT
EXPOSE 8300
# Sat, 12 Dec 2020 14:07:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 12 Dec 2020 14:07:55 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 12 Dec 2020 14:07:55 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 12 Dec 2020 14:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Dec 2020 14:07:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c8060704c53f3ff052629f979f702282b4cdedc728a02c83ddfcb511067de2`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fc274a81c60ca4deddc3eb2021465a3cacb68e5c35024212cf02fa2a3055da`  
		Last Modified: Sat, 12 Dec 2020 14:09:16 GMT  
		Size: 38.3 MB (38342356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421085bf757533067046c72d4f76aa17383fe82a1c5a709df6015e5f3f7a3af3`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92d7c3c09e2f09ab13919755506eb2699a0dbcf2b107a570e6bc9ca536be912`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa6ebe29a594ab16a614fc400231c0e5d0b79f316e51ebf17b0ebcdd0db9875`  
		Last Modified: Sat, 12 Dec 2020 14:09:08 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:011cea977b0f335aa8b43b049fda85bf3097213f272f015e0aa1382b823fdf25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44857211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1eeaaeaef66065328787653703bd3bd70f8c89e440efe723b9cd3a0937ec5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 11 Dec 2020 02:01:14 GMT
ADD file:8812e502f26af2dc4efdfb7387f8bf99f2a098b6c95b9f6abf900df2ce74e3da in / 
# Fri, 11 Dec 2020 02:01:14 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:57:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 11 Dec 2020 05:57:39 GMT
ENV CONSUL_VERSION=1.9.0
# Fri, 11 Dec 2020 05:57:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 11 Dec 2020 05:57:40 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 11 Dec 2020 05:57:45 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 11 Dec 2020 05:57:46 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 11 Dec 2020 05:57:47 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:47 GMT
VOLUME [/consul/data]
# Fri, 11 Dec 2020 05:57:47 GMT
EXPOSE 8300
# Fri, 11 Dec 2020 05:57:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 11 Dec 2020 05:57:48 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 11 Dec 2020 05:57:48 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 11 Dec 2020 05:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:57:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b62269920a7a62a905817c7c1b33f33b6e658121e9a054715ff052a23f7de3a0`  
		Last Modified: Fri, 11 Dec 2020 02:01:43 GMT  
		Size: 2.8 MB (2791504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d19e00b093c0916475a088f3ed6f9b2639fae7165fe16c97995381ed277a07`  
		Last Modified: Fri, 11 Dec 2020 05:59:05 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1fe592dd342b87165eefaac9626321a0ce7cd0b444d845de3b1d8ea7051bd0`  
		Last Modified: Fri, 11 Dec 2020 05:59:13 GMT  
		Size: 42.1 MB (42062481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2683019cdf3b191a80f3576881b606b43d49d40cd3e8479212ecad67252266`  
		Last Modified: Fri, 11 Dec 2020 05:59:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38303cbe4569f0323c09593536c06fc4e346a343ddf40ffe6f73ecb19d5ffaa`  
		Last Modified: Fri, 11 Dec 2020 05:59:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be8941323c8b19851764f2fc37934a92e4f6e8b1b67b4360ab67fecdc797b43`  
		Last Modified: Fri, 11 Dec 2020 05:59:05 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
