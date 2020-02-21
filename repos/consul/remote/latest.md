## `consul:latest`

```console
$ docker pull consul@sha256:3e064c7f96231a95677a7d7af603ef99a8ca4d63d46a70e25de794c9fc392ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:0857aefc207857ac82462cce87e0abfcdd935c939797244d37264fb058eb2986
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44022416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2bcf61cdf1fa9f8438aef7fb08686f697941d9fe7162ab3dadb6aa4c12322d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:15:11 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 21 Feb 2020 02:36:06 GMT
ENV CONSUL_VERSION=1.7.1
# Fri, 21 Feb 2020 02:36:06 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 21 Feb 2020 02:36:07 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 21 Feb 2020 02:36:15 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 21 Feb 2020 02:36:16 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 21 Feb 2020 02:36:17 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 21 Feb 2020 02:36:18 GMT
VOLUME [/consul/data]
# Fri, 21 Feb 2020 02:36:18 GMT
EXPOSE 8300
# Fri, 21 Feb 2020 02:36:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 21 Feb 2020 02:36:19 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 21 Feb 2020 02:36:19 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Feb 2020 02:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 02:36:20 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86f60c5bca76e950740e5a986a1537ba8e3311fffe54185fc18f2bb0dfad9cd`  
		Last Modified: Fri, 21 Feb 2020 02:37:29 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797d2b209b117f4c985f728d83624a5d62001eb9e6da653ba2521b130ecd2221`  
		Last Modified: Fri, 21 Feb 2020 02:37:39 GMT  
		Size: 41.3 MB (41254983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c8a484f6b6ccc492a54df7cd2b7c5da0468440f6034086c82d40f8e8848d47`  
		Last Modified: Fri, 21 Feb 2020 02:37:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6170620a1ae470143e85414589e778211d954243726e6949f022a3cc4e5646a`  
		Last Modified: Fri, 21 Feb 2020 02:37:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf6b979311c34b048554e301a733269a8809de7b5715467b852abba021e988d`  
		Last Modified: Fri, 21 Feb 2020 02:37:29 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:6da0cb108ccafe772193327e439557c0d0a700645a57af2c5c10795aa62cc928
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41363939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8912f5c095a95740b69588214c12998a51647b94f5dba48e8b5143d7abcee793`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:38 GMT
ADD file:7e840db4b1f91900bcc3693359908c82f531fc44027d4d5327ef598e8710ed0f in / 
# Thu, 23 Jan 2020 16:53:40 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:12:38 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Thu, 20 Feb 2020 23:15:59 GMT
ENV CONSUL_VERSION=1.7.1
# Thu, 20 Feb 2020 23:16:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 20 Feb 2020 23:16:02 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 20 Feb 2020 23:16:12 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 20 Feb 2020 23:16:14 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 20 Feb 2020 23:16:16 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 20 Feb 2020 23:16:18 GMT
VOLUME [/consul/data]
# Thu, 20 Feb 2020 23:16:19 GMT
EXPOSE 8300
# Thu, 20 Feb 2020 23:16:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 20 Feb 2020 23:16:21 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 20 Feb 2020 23:16:22 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 20 Feb 2020 23:16:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2020 23:16:25 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1c8737e28b1ca4452315b0127f7c6f4ad64f0c4695a3b52b1a4a3d2d17d3bbd5`  
		Last Modified: Thu, 23 Jan 2020 16:54:15 GMT  
		Size: 2.5 MB (2547672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8421293b9877ae0b483f9e344fe80709ed8dfb64853bad4b78efffc47aed58b4`  
		Last Modified: Thu, 20 Feb 2020 23:18:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdbd63f2a182265619dd0cc3b5da7cd87abf9906d105f533fb2b7b8d99a2d0e`  
		Last Modified: Thu, 20 Feb 2020 23:18:17 GMT  
		Size: 38.8 MB (38812943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f0ae0374f7366aa02e05b88272653d9180227a2f0f01194a45fe48409de245`  
		Last Modified: Thu, 20 Feb 2020 23:18:02 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e823e59fb22c00dd2a8d7eac702daae01b4de634259d076d48bd4a1e75edcb0`  
		Last Modified: Thu, 20 Feb 2020 23:18:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c92ce8012293b1822eb152fbd2558cfc63874ef648dc3608dcc5c8d176e310`  
		Last Modified: Thu, 20 Feb 2020 23:18:02 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:3df9f6403d3e18844ad953ece121fce14efd95715c6dfca7b448f143fb2f7092
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41712584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47053f031ed9beb7c1f9c0daefe9afedd47015a258e0b2b98a30edc856d4ba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:19:49 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 21 Feb 2020 00:41:16 GMT
ENV CONSUL_VERSION=1.7.1
# Fri, 21 Feb 2020 00:41:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 21 Feb 2020 00:41:22 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 21 Feb 2020 00:41:32 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 21 Feb 2020 00:41:36 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 21 Feb 2020 00:41:38 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 21 Feb 2020 00:41:39 GMT
VOLUME [/consul/data]
# Fri, 21 Feb 2020 00:41:40 GMT
EXPOSE 8300
# Fri, 21 Feb 2020 00:41:40 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 21 Feb 2020 00:41:41 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 21 Feb 2020 00:41:42 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Feb 2020 00:41:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 00:41:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df75259228b427b9031eaf53b2495684d0e175f0436efd3dc5e1bec240a6d3c`  
		Last Modified: Fri, 21 Feb 2020 00:43:28 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ab041040b080f0f747ab8e41837d45cf0d2561bce5ea0521847906bc30626`  
		Last Modified: Fri, 21 Feb 2020 00:43:38 GMT  
		Size: 39.0 MB (39016031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6331da0196403c1397dd5c7197f57e8c00c85d0d6a42cd1bd14d77d08f62a7b`  
		Last Modified: Fri, 21 Feb 2020 00:43:28 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e38937503ec7eb499eeadd311ace58b21409e90d898665971f3ec857b8bbe67`  
		Last Modified: Fri, 21 Feb 2020 00:43:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6e1a93a97776d8b3877fdf5e5aec696f3fa9d5bd263cb5b63f7cfcb5e6490f`  
		Last Modified: Fri, 21 Feb 2020 00:43:28 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:d099c64747d178aa325a73450c45a6298b6e2c337f53129a4abded1b9b269236
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42791125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b6a7c85754a54ba02d0892bc6d722c23d1d08140d2a6e41ce4b722c3c4918f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:05 GMT
ADD file:4e7195ad2b3e9b85e4596b4a73719eb294f2a293a05b7b8e6096c4cfac0c6fde in / 
# Thu, 23 Jan 2020 16:53:05 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:57:03 GMT
MAINTAINER Consul Team <consul@hashicorp.com>
# Fri, 21 Feb 2020 03:20:56 GMT
ENV CONSUL_VERSION=1.7.1
# Fri, 21 Feb 2020 03:20:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 21 Feb 2020 03:20:57 GMT
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 21 Feb 2020 03:21:07 GMT
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 21 Feb 2020 03:21:08 GMT
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 21 Feb 2020 03:21:10 GMT
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 21 Feb 2020 03:21:10 GMT
VOLUME [/consul/data]
# Fri, 21 Feb 2020 03:21:10 GMT
EXPOSE 8300
# Fri, 21 Feb 2020 03:21:11 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 21 Feb 2020 03:21:11 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 21 Feb 2020 03:21:11 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Feb 2020 03:21:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 03:21:12 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fd25584d30bfc37afa2d99f41ef0a7055a4f2923907582dd992194fb4aa13f1c`  
		Last Modified: Thu, 23 Jan 2020 16:53:27 GMT  
		Size: 2.8 MB (2768519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68cde75e14d420dbf55729a17806c325e59bc73d03cb77199726523625482d3`  
		Last Modified: Fri, 21 Feb 2020 03:22:15 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47533f8349eba4e96a10594e09cfae0519e59c33524f5de87700312123016e40`  
		Last Modified: Fri, 21 Feb 2020 03:22:23 GMT  
		Size: 40.0 MB (40019345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f42fc0950658d4560e0bc60aaac04d6158609dea0db3f0cbfe9b27303ba506f`  
		Last Modified: Fri, 21 Feb 2020 03:22:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0612b9a4ef3ad88c4f216df360aaff20780125d98168e8aa1eee0b18566d53b5`  
		Last Modified: Fri, 21 Feb 2020 03:22:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def67436b212474916eaf3ea72beeaec8b613d9c20f3ccf3fc342b5cd78218aa`  
		Last Modified: Fri, 21 Feb 2020 03:22:16 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
