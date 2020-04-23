## `consul:latest`

```console
$ docker pull consul@sha256:6b59b6ff9150eeaab1b0bb8fc5e6256ee1d29fac8d6b8abdeea25f9a5551cbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:2f03c533527fdf8b579647f093eb7fe88fc7f2038794cfbe20347b02eef68e1e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44031134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213e00e87c53c5489ba357ba79b831abd46b13de4f94f6ce73991eb2c4966910`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Tue, 17 Mar 2020 02:21:42 GMT
ENV CONSUL_VERSION=1.7.2
# Tue, 17 Mar 2020 02:21:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 17 Mar 2020 02:21:43 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 17 Mar 2020 02:21:48 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 17 Mar 2020 02:21:49 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 17 Mar 2020 02:21:50 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 17 Mar 2020 02:21:50 GMT
VOLUME [/consul/data]
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8300
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 17 Mar 2020 02:21:50 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 17 Mar 2020 02:21:51 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Mar 2020 02:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2020 02:21:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e53a83f2205caac853dba979ee0e2ec8c8b5d90afca5e4108f8467c0f71379`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64aa8d4cc8e6904c634c53644e5dd89e3de02465084a361007d8a7edc8bbb10`  
		Last Modified: Tue, 17 Mar 2020 02:22:38 GMT  
		Size: 41.3 MB (41263699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82481eff66f7571652f4b8322f7254ec061549efd50280ff1e4222151ce378a8`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aba2a452b629a1689862dce05fc3664b37849089dad576172dff92e127b037`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81d1cfdb2572cbdf90464dba06a3a2508ec42f60b0740b17860bef517cb20a`  
		Last Modified: Tue, 17 Mar 2020 02:22:31 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:2576c59acc486392580e50ded105e64b1978b932db016d9e90938b8e6d33d4b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41373378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79208c31c835cd5fec058474d924af104bdeeb4b9d96f534a2ff1896b12e7ff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:44 GMT
ADD file:7dd2657543fac7f63a125194d27bd38a8e472a3076831a2331c43a471794c210 in / 
# Thu, 23 Apr 2020 15:51:45 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 16:53:13 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 23 Apr 2020 16:53:14 GMT
ENV CONSUL_VERSION=1.7.2
# Thu, 23 Apr 2020 16:53:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 23 Apr 2020 16:53:17 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 23 Apr 2020 16:53:38 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 23 Apr 2020 16:53:40 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 23 Apr 2020 16:53:42 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 23 Apr 2020 16:53:43 GMT
VOLUME [/consul/data]
# Thu, 23 Apr 2020 16:53:43 GMT
EXPOSE 8300
# Thu, 23 Apr 2020 16:53:44 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 23 Apr 2020 16:53:45 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 23 Apr 2020 16:53:46 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Apr 2020 16:53:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 16:53:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27da80392aebe463671b839837d59af1261218364b4261ceb2eca0f814075270`  
		Last Modified: Thu, 23 Apr 2020 15:52:21 GMT  
		Size: 2.5 MB (2548725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9874fc1eb1d8751a0b682ebbc5d8c79d232643ec2a56f3b01f2fc7d1d0d2ebf2`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564cdd5be6d3d2f6363923b22e5b77dcc12bf2b1bd669768afda1448739539c4`  
		Last Modified: Thu, 23 Apr 2020 16:59:02 GMT  
		Size: 38.8 MB (38821333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685d58b44180c7be022003e491ecd91499d30bf07744be7129d578aedef8315c`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ac0ffd1df9fea7f273b6d0d2c4fe39c72b0734f71b4d228f3b8df05faf62da`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2aef728bacc9219868ef13d7868146b3397a1a23089fc08e14751f2740a6cbf`  
		Last Modified: Thu, 23 Apr 2020 16:58:48 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:722bf1c625cc356868b999bb71942880db3de719fb1575cc643be9616da99a1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41717466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbd2e6f19ef2f7eca2a608471f4f3cc1106fcb167836254ea32139208b056ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Tue, 17 Mar 2020 01:41:06 GMT
ENV CONSUL_VERSION=1.7.2
# Tue, 17 Mar 2020 01:41:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 17 Mar 2020 01:41:10 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 17 Mar 2020 01:41:21 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 17 Mar 2020 01:41:23 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 17 Mar 2020 01:41:25 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 17 Mar 2020 01:41:25 GMT
VOLUME [/consul/data]
# Tue, 17 Mar 2020 01:41:26 GMT
EXPOSE 8300
# Tue, 17 Mar 2020 01:41:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 17 Mar 2020 01:41:28 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 17 Mar 2020 01:41:28 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Mar 2020 01:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2020 01:41:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a290e0722d9ba02ecd57e64344813e3fbb0e36a0349fae7f659844dbf65be`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553963123c347234d9b628a4752e54566f63a2433fcb9fff1e82345b1e22c8c0`  
		Last Modified: Tue, 17 Mar 2020 01:42:36 GMT  
		Size: 39.0 MB (39020908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85194eac93fdf9bccb929349405df065c17bcae470d52df5ec33a1b5d678677c`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf62bdd07dd68e7efaa2e683c7708a54095a75ec3b01a12f2a1e76e751288cb`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c468b02becd03fba58d2e5d6d23ca84d0aa0d7777ee7ca2fdb478d0a0189773e`  
		Last Modified: Tue, 17 Mar 2020 01:42:26 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:a147eaa6502140f8041a39315ae24a9d26294e991bf864ec6add6614fad29dfb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42800741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142db19831f644bb5558094963d3c77de006238ada98d78d2fb99c0cd1257c29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:05 GMT
ADD file:4e7195ad2b3e9b85e4596b4a73719eb294f2a293a05b7b8e6096c4cfac0c6fde in / 
# Thu, 23 Jan 2020 16:53:05 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:57:03 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Tue, 17 Mar 2020 01:38:50 GMT
ENV CONSUL_VERSION=1.7.2
# Tue, 17 Mar 2020 01:38:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 17 Mar 2020 01:38:51 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 17 Mar 2020 01:39:00 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 17 Mar 2020 01:39:01 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 17 Mar 2020 01:39:02 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 17 Mar 2020 01:39:02 GMT
VOLUME [/consul/data]
# Tue, 17 Mar 2020 01:39:02 GMT
EXPOSE 8300
# Tue, 17 Mar 2020 01:39:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 17 Mar 2020 01:39:03 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 17 Mar 2020 01:39:03 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 17 Mar 2020 01:39:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2020 01:39:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fd25584d30bfc37afa2d99f41ef0a7055a4f2923907582dd992194fb4aa13f1c`  
		Last Modified: Thu, 23 Jan 2020 16:53:27 GMT  
		Size: 2.8 MB (2768519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0c1b4ee2cc8d68e2f4bac60a092bfb7c2aeafc41e929fe5f28cd0d71fcddf2`  
		Last Modified: Tue, 17 Mar 2020 01:39:43 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2509ec2ac347205f811578d33a6e992859ae53402b918680bb950d16210bfc6`  
		Last Modified: Tue, 17 Mar 2020 01:39:53 GMT  
		Size: 40.0 MB (40028963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007f2cb53e3d6afc6a03169898109d84a79045ebb442a191cc47c7e58942f931`  
		Last Modified: Tue, 17 Mar 2020 01:39:44 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e01193b469b5e3baa36d4941cdd5d38504d3540b52a93e2e0e097607d9e786`  
		Last Modified: Tue, 17 Mar 2020 01:39:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53d26d5b817b1deb64354c8d97504e49b61a9c2c2d0722f5f06335258359809`  
		Last Modified: Tue, 17 Mar 2020 01:39:43 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
