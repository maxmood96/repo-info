<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.13`](#consul113)
-	[`consul:1.13.8`](#consul1138)
-	[`consul:1.14`](#consul114)
-	[`consul:1.14.7`](#consul1147)
-	[`consul:1.15`](#consul115)
-	[`consul:1.15.3`](#consul1153)
-	[`consul:latest`](#consullatest)

## `consul:1.13`

```console
$ docker pull consul@sha256:9080f13f7d766c7b731a88aeea2c9e417a45c98b43106921a8b8497123ae3d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.13` - linux; amd64

```console
$ docker pull consul@sha256:b6ba521928cdb554f8fd160a537cad0f43073d48c0d8daaeeee553ef265feb3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53249938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3c7ef92a2c93c74afd836dc58c7b3d5a45240cc23ce8d5304e64d5c8fd992a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:21:54 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 17 May 2023 23:21:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:21:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:21:55 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:22:00 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:22:01 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:22:02 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:22:02 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:22:02 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:22:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:22:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8286ff1bc4a634dcd9b1566cbfa82c58f18aac2aa1356f6041cad9330001e979`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b9bc9b1f6484e62df572e77c880973a6a6b576167953550f5b7caaac0b88`  
		Last Modified: Wed, 17 May 2023 23:22:34 GMT  
		Size: 50.4 MB (50419917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1287366eeaa3b9fe5bae2eae5869cac08b74e18d4a4affc04646329f7bcbe04e`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e762d9c652f2055032bad6d4d7961fb7fdc268e576f21888ef1ac4d478f5871e`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81f71f475104174cd0a87cbc84764e046c3390b091e7fa751e14269b8bd69b0`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm variant v6

```console
$ docker pull consul@sha256:8a0433b0d4126b4b5d91f474861fabbc56c7a7be4cdf09db37bd3235ec6c5a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50351652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58442ee7a55f1f0631adf01d98955b7958dc3ffb699ccba2d05b1e3470005fde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:32 GMT
ADD file:b987db82fa4ce6e623de49a50612c1fd91c5ab2209a62a5727ab3436c2923e91 in / 
# Wed, 14 Jun 2023 18:49:32 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:25:20 GMT
ARG CONSUL_VERSION=1.13.8
# Thu, 15 Jun 2023 01:25:20 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 01:25:21 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 01:25:21 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 01:25:29 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 01:25:30 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 01:25:31 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 01:25:31 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 01:25:31 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 01:25:31 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 01:25:31 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 01:25:31 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 01:25:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 01:25:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:41c5c5b38e13af18def277385607129664fb24993d262d4b601a381e776482a9`  
		Last Modified: Wed, 14 Jun 2023 18:50:19 GMT  
		Size: 2.6 MB (2633060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4022e3966ca7b72e8ed31e85ded22169a74da0646724b4e5912a7342d5192102`  
		Last Modified: Thu, 15 Jun 2023 01:26:14 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7722bab3ebe08647f359a94e559c3ca9250fef90b5af47d65cc12bf3836670`  
		Last Modified: Thu, 15 Jun 2023 01:26:21 GMT  
		Size: 47.7 MB (47715167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8679bd219c0e84245a58e8495dbb9d77984110716f5a89b31607f07d7c700fd1`  
		Last Modified: Thu, 15 Jun 2023 01:26:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e66d9fc0290fb6f3bad661e2f4ac5a86d248dab74d46f7b0bd116c2712974a1`  
		Last Modified: Thu, 15 Jun 2023 01:26:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b115655f4f24c517b6cb390f718f47d8fab0d54d9d05e3901daeb64ddd500a06`  
		Last Modified: Thu, 15 Jun 2023 01:26:14 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:d3218e2f55c3706a4f7495082ece325fc2f06befb1df5e800c60fa2f0e866bba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49882249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e911bd3135547935e6281b785350eb8869a68c2afda31a7a961ebd5ff9168cc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:10 GMT
ADD file:2b463f242cb7bf946452bb4781838348ecbe80da144fbab09f51d7e050dc68f3 in / 
# Wed, 14 Jun 2023 20:49:11 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:38:29 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 14 Jun 2023 22:38:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 14 Jun 2023 22:38:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Jun 2023 22:38:30 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Jun 2023 22:38:36 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Jun 2023 22:38:37 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Jun 2023 22:38:37 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Jun 2023 22:38:38 GMT
VOLUME [/consul/data]
# Wed, 14 Jun 2023 22:38:38 GMT
EXPOSE 8300
# Wed, 14 Jun 2023 22:38:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Jun 2023 22:38:38 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Jun 2023 22:38:38 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Jun 2023 22:38:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:38:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a147224bf413aeffbbfcdcb5104d35c647256a5c32083f4d8134f09a4e74ddeb`  
		Last Modified: Wed, 14 Jun 2023 20:49:52 GMT  
		Size: 2.7 MB (2720801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55240541197f558cd2e339680b6c23082080cf65b4f0ceb25b00d3f4f63c277`  
		Last Modified: Wed, 14 Jun 2023 22:39:16 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d611630cb1c1af82bc49f7793beeb49a006bb274b84d66e5aff78801e1601bc0`  
		Last Modified: Wed, 14 Jun 2023 22:39:21 GMT  
		Size: 47.2 MB (47158021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54916a255eb8cffbca612f8f381146fc7f07c1e1ecedd8a5bf87af97bf210484`  
		Last Modified: Wed, 14 Jun 2023 22:39:16 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1ab5420d42ec1c431bce3d4f5022669a04bc50217a3b630567d53cca666cfb`  
		Last Modified: Wed, 14 Jun 2023 22:39:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52417ddbcebbfbb817fcc44a5cd99e6480b60f391b344a2c5acac0f8b88b2dd`  
		Last Modified: Wed, 14 Jun 2023 22:39:16 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; 386

```console
$ docker pull consul@sha256:afec66d2334c317ead9f3fe41edb330e9dbf75ccefb65e28dd8abe666b192ad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51689802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b945e486dcff3efd7ae87561344eee47aea5a514a440bd61759c2e8c67a05069`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:34 GMT
ADD file:92f6ab42e26a2cc37a3463b6f6508e29ae194413d31cb95f1609f93f32d2e94d in / 
# Wed, 14 Jun 2023 22:33:34 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:09:32 GMT
ARG CONSUL_VERSION=1.13.8
# Thu, 15 Jun 2023 02:09:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 02:09:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 02:09:33 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 02:09:40 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 02:09:41 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 02:09:42 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 02:09:42 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 02:09:42 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 02:09:42 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 02:09:42 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 02:09:42 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 02:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 02:09:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:74051fed7c11c74895f7583bcde366e9192af8539de4915832d9c990bd23f581`  
		Last Modified: Wed, 14 Jun 2023 22:34:17 GMT  
		Size: 2.8 MB (2832157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667c75ab6fd48a4065e8380cedd3414b18b40d2415db1f09f38e95554ad37c55`  
		Last Modified: Thu, 15 Jun 2023 02:10:28 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9465c397d9fda4c36786c1633335fa2af1b9733801f8e1d5eb37fc27fe3c2dc`  
		Last Modified: Thu, 15 Jun 2023 02:10:36 GMT  
		Size: 48.9 MB (48854217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b85586c7a6c24a6f120a6120cd9510b051e121c9716c12f4aa57b6c0e17fcb`  
		Last Modified: Thu, 15 Jun 2023 02:10:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12288f00d07fe0fcda384a4ed01e780f6f40f289bb29c3af609e5dd70dcc0b9f`  
		Last Modified: Thu, 15 Jun 2023 02:10:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408642479f6fdddd152a3367807628c02ce84e33d1bf074b29ffbce7b9992c14`  
		Last Modified: Thu, 15 Jun 2023 02:10:29 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.13.8`

```console
$ docker pull consul@sha256:9080f13f7d766c7b731a88aeea2c9e417a45c98b43106921a8b8497123ae3d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.13.8` - linux; amd64

```console
$ docker pull consul@sha256:b6ba521928cdb554f8fd160a537cad0f43073d48c0d8daaeeee553ef265feb3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53249938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3c7ef92a2c93c74afd836dc58c7b3d5a45240cc23ce8d5304e64d5c8fd992a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:21:54 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 17 May 2023 23:21:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:21:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:21:55 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:22:00 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:22:01 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:22:02 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:22:02 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:22:02 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:22:02 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:22:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:22:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8286ff1bc4a634dcd9b1566cbfa82c58f18aac2aa1356f6041cad9330001e979`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a38b9bc9b1f6484e62df572e77c880973a6a6b576167953550f5b7caaac0b88`  
		Last Modified: Wed, 17 May 2023 23:22:34 GMT  
		Size: 50.4 MB (50419917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1287366eeaa3b9fe5bae2eae5869cac08b74e18d4a4affc04646329f7bcbe04e`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e762d9c652f2055032bad6d4d7961fb7fdc268e576f21888ef1ac4d478f5871e`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81f71f475104174cd0a87cbc84764e046c3390b091e7fa751e14269b8bd69b0`  
		Last Modified: Wed, 17 May 2023 23:22:28 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:8a0433b0d4126b4b5d91f474861fabbc56c7a7be4cdf09db37bd3235ec6c5a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50351652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58442ee7a55f1f0631adf01d98955b7958dc3ffb699ccba2d05b1e3470005fde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:32 GMT
ADD file:b987db82fa4ce6e623de49a50612c1fd91c5ab2209a62a5727ab3436c2923e91 in / 
# Wed, 14 Jun 2023 18:49:32 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:25:20 GMT
ARG CONSUL_VERSION=1.13.8
# Thu, 15 Jun 2023 01:25:20 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 01:25:21 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 01:25:21 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 01:25:29 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 01:25:30 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 01:25:31 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 01:25:31 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 01:25:31 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 01:25:31 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 01:25:31 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 01:25:31 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 01:25:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 01:25:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:41c5c5b38e13af18def277385607129664fb24993d262d4b601a381e776482a9`  
		Last Modified: Wed, 14 Jun 2023 18:50:19 GMT  
		Size: 2.6 MB (2633060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4022e3966ca7b72e8ed31e85ded22169a74da0646724b4e5912a7342d5192102`  
		Last Modified: Thu, 15 Jun 2023 01:26:14 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7722bab3ebe08647f359a94e559c3ca9250fef90b5af47d65cc12bf3836670`  
		Last Modified: Thu, 15 Jun 2023 01:26:21 GMT  
		Size: 47.7 MB (47715167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8679bd219c0e84245a58e8495dbb9d77984110716f5a89b31607f07d7c700fd1`  
		Last Modified: Thu, 15 Jun 2023 01:26:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e66d9fc0290fb6f3bad661e2f4ac5a86d248dab74d46f7b0bd116c2712974a1`  
		Last Modified: Thu, 15 Jun 2023 01:26:14 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b115655f4f24c517b6cb390f718f47d8fab0d54d9d05e3901daeb64ddd500a06`  
		Last Modified: Thu, 15 Jun 2023 01:26:14 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:d3218e2f55c3706a4f7495082ece325fc2f06befb1df5e800c60fa2f0e866bba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49882249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e911bd3135547935e6281b785350eb8869a68c2afda31a7a961ebd5ff9168cc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:10 GMT
ADD file:2b463f242cb7bf946452bb4781838348ecbe80da144fbab09f51d7e050dc68f3 in / 
# Wed, 14 Jun 2023 20:49:11 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:38:29 GMT
ARG CONSUL_VERSION=1.13.8
# Wed, 14 Jun 2023 22:38:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 14 Jun 2023 22:38:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Jun 2023 22:38:30 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Jun 2023 22:38:36 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Jun 2023 22:38:37 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Jun 2023 22:38:37 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Jun 2023 22:38:38 GMT
VOLUME [/consul/data]
# Wed, 14 Jun 2023 22:38:38 GMT
EXPOSE 8300
# Wed, 14 Jun 2023 22:38:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Jun 2023 22:38:38 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Jun 2023 22:38:38 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Jun 2023 22:38:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:38:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a147224bf413aeffbbfcdcb5104d35c647256a5c32083f4d8134f09a4e74ddeb`  
		Last Modified: Wed, 14 Jun 2023 20:49:52 GMT  
		Size: 2.7 MB (2720801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55240541197f558cd2e339680b6c23082080cf65b4f0ceb25b00d3f4f63c277`  
		Last Modified: Wed, 14 Jun 2023 22:39:16 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d611630cb1c1af82bc49f7793beeb49a006bb274b84d66e5aff78801e1601bc0`  
		Last Modified: Wed, 14 Jun 2023 22:39:21 GMT  
		Size: 47.2 MB (47158021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54916a255eb8cffbca612f8f381146fc7f07c1e1ecedd8a5bf87af97bf210484`  
		Last Modified: Wed, 14 Jun 2023 22:39:16 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1ab5420d42ec1c431bce3d4f5022669a04bc50217a3b630567d53cca666cfb`  
		Last Modified: Wed, 14 Jun 2023 22:39:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52417ddbcebbfbb817fcc44a5cd99e6480b60f391b344a2c5acac0f8b88b2dd`  
		Last Modified: Wed, 14 Jun 2023 22:39:16 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.8` - linux; 386

```console
$ docker pull consul@sha256:afec66d2334c317ead9f3fe41edb330e9dbf75ccefb65e28dd8abe666b192ad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51689802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b945e486dcff3efd7ae87561344eee47aea5a514a440bd61759c2e8c67a05069`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:34 GMT
ADD file:92f6ab42e26a2cc37a3463b6f6508e29ae194413d31cb95f1609f93f32d2e94d in / 
# Wed, 14 Jun 2023 22:33:34 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:09:32 GMT
ARG CONSUL_VERSION=1.13.8
# Thu, 15 Jun 2023 02:09:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 02:09:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 02:09:33 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 02:09:40 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 02:09:41 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 02:09:42 GMT
# ARGS: CONSUL_VERSION=1.13.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 02:09:42 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 02:09:42 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 02:09:42 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 02:09:42 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 02:09:42 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 02:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 02:09:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:74051fed7c11c74895f7583bcde366e9192af8539de4915832d9c990bd23f581`  
		Last Modified: Wed, 14 Jun 2023 22:34:17 GMT  
		Size: 2.8 MB (2832157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667c75ab6fd48a4065e8380cedd3414b18b40d2415db1f09f38e95554ad37c55`  
		Last Modified: Thu, 15 Jun 2023 02:10:28 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9465c397d9fda4c36786c1633335fa2af1b9733801f8e1d5eb37fc27fe3c2dc`  
		Last Modified: Thu, 15 Jun 2023 02:10:36 GMT  
		Size: 48.9 MB (48854217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b85586c7a6c24a6f120a6120cd9510b051e121c9716c12f4aa57b6c0e17fcb`  
		Last Modified: Thu, 15 Jun 2023 02:10:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12288f00d07fe0fcda384a4ed01e780f6f40f289bb29c3af609e5dd70dcc0b9f`  
		Last Modified: Thu, 15 Jun 2023 02:10:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408642479f6fdddd152a3367807628c02ce84e33d1bf074b29ffbce7b9992c14`  
		Last Modified: Thu, 15 Jun 2023 02:10:29 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14`

```console
$ docker pull consul@sha256:29d89c3dbde641e96bbe614b3cd1ca6c6ab82e725246bd3a3fce7798da906c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.14` - linux; amd64

```console
$ docker pull consul@sha256:c5363f57ebd80acdb08eda2706da303d574800d96686d598991107ce24c4a001
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57044114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e9cc702d7e2c93f02d73f6bc9900bf40e573cdb6fe7909dc26ab96b4847964`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:21:43 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 17 May 2023 23:21:43 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:21:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:21:44 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:21:50 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:21:50 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:21:51 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:21:51 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:21:51 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:21:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001bd6942da9d529f3ee86b01a88dcc743c72ecbf1d0194c81b4a9a46153e098`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0349ac67f6ae8d5912668dbf97fc9b77f276f3d74b18e8d088ec322b22ae7e74`  
		Last Modified: Wed, 17 May 2023 23:22:20 GMT  
		Size: 54.2 MB (54214088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dca13136f6774035c2dde75e01445cfeba66d37c4f4d5cb339ff16c7d08b098`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8316eeeac047103fd632fd127a134a8a087670a870090c849ed9169ed3797e7a`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbce098aeaa4602998aa92509a72512a177c6063ee11b0895f0a41176b1ec6`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; arm variant v6

```console
$ docker pull consul@sha256:76774bc44c2b7040ded267f98bafcbd21e51f0a273a9ec7104061003ea718344
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53915157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9e7e579584bf7000eafde666109aa211a997112846d69440dd32a264c8d715`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:32 GMT
ADD file:b987db82fa4ce6e623de49a50612c1fd91c5ab2209a62a5727ab3436c2923e91 in / 
# Wed, 14 Jun 2023 18:49:32 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:25:07 GMT
ARG CONSUL_VERSION=1.14.7
# Thu, 15 Jun 2023 01:25:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 01:25:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 01:25:08 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 01:25:16 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 01:25:16 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 01:25:17 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 01:25:18 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 01:25:18 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 01:25:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 01:25:18 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 01:25:18 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 01:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 01:25:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:41c5c5b38e13af18def277385607129664fb24993d262d4b601a381e776482a9`  
		Last Modified: Wed, 14 Jun 2023 18:50:19 GMT  
		Size: 2.6 MB (2633060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13258989c71f0866b1872bd573153814a2a2c93c342273fba4ed6a792182129`  
		Last Modified: Thu, 15 Jun 2023 01:25:59 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac89fe99dbbe4eba59f1ca42f37934e55a7f59adb5a2c6b15c3240c07757181`  
		Last Modified: Thu, 15 Jun 2023 01:26:06 GMT  
		Size: 51.3 MB (51278669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f5d738f14227165a546d2e63c856023cabd733faa64ade1c794a78301fa45`  
		Last Modified: Thu, 15 Jun 2023 01:25:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acd9da5831b67d17370e2e34f2a3865d7048fc68c0917915f22644d29601761`  
		Last Modified: Thu, 15 Jun 2023 01:25:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76516ecfce632226d1910cd73bf01b327c7f721fc24cdd90cb65dd3f2f1f2e87`  
		Last Modified: Thu, 15 Jun 2023 01:25:59 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b3bbb6fde64dd95386ed690b7f6ab0a1fb60dd7a53d6b61563972c8298fc3b47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53470559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e16b3f9d963b06ff99a163e453989437fd8ebd19c9ec7cad9909e978494ab54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:10 GMT
ADD file:2b463f242cb7bf946452bb4781838348ecbe80da144fbab09f51d7e050dc68f3 in / 
# Wed, 14 Jun 2023 20:49:11 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:38:18 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 14 Jun 2023 22:38:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 14 Jun 2023 22:38:18 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Jun 2023 22:38:18 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Jun 2023 22:38:24 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Jun 2023 22:38:26 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Jun 2023 22:38:26 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Jun 2023 22:38:26 GMT
VOLUME [/consul/data]
# Wed, 14 Jun 2023 22:38:26 GMT
EXPOSE 8300
# Wed, 14 Jun 2023 22:38:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Jun 2023 22:38:26 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Jun 2023 22:38:26 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Jun 2023 22:38:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:38:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a147224bf413aeffbbfcdcb5104d35c647256a5c32083f4d8134f09a4e74ddeb`  
		Last Modified: Wed, 14 Jun 2023 20:49:52 GMT  
		Size: 2.7 MB (2720801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3fe053a164c645f70317c7bc8676a5770dcf79aad5cb1356b50793b522508e`  
		Last Modified: Wed, 14 Jun 2023 22:39:02 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3394d2371b6ba9115f9694aa39ebf939fe622d48a753a5b13b07165906cc905`  
		Last Modified: Wed, 14 Jun 2023 22:39:08 GMT  
		Size: 50.7 MB (50746334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0246651a8e31d99cc664cbbe638b0385390e21b0f777043a794f1b0e322d898`  
		Last Modified: Wed, 14 Jun 2023 22:39:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a0ac696786bf981eb29e9af83dd052a84b265f995bb0e83a655915aa59a201`  
		Last Modified: Wed, 14 Jun 2023 22:39:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42b83ab50c9178c73efb554ab56624fb60a8417235e401cb8477c31968e554d`  
		Last Modified: Wed, 14 Jun 2023 22:39:02 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; 386

```console
$ docker pull consul@sha256:1866fda7f3a6054469e95f297ac21acf449eabb794aee84537314ab5f0fe9b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55296444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6795533f8f7d26e8a5927f233a37f213410c902a5fe22f02191fda14e69179`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:34 GMT
ADD file:92f6ab42e26a2cc37a3463b6f6508e29ae194413d31cb95f1609f93f32d2e94d in / 
# Wed, 14 Jun 2023 22:33:34 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:09:19 GMT
ARG CONSUL_VERSION=1.14.7
# Thu, 15 Jun 2023 02:09:19 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 02:09:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 02:09:20 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 02:09:28 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 02:09:28 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 02:09:29 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 02:09:29 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 02:09:29 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 02:09:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 02:09:29 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 02:09:30 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 02:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 02:09:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:74051fed7c11c74895f7583bcde366e9192af8539de4915832d9c990bd23f581`  
		Last Modified: Wed, 14 Jun 2023 22:34:17 GMT  
		Size: 2.8 MB (2832157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a7b0777832ab41a213293ae6fe8387635051e4230d37f0530c4557c05afae5`  
		Last Modified: Thu, 15 Jun 2023 02:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9419d1945453b686bef523fbad0f84e0f50be79d0685a43b73a012eef0a24dbf`  
		Last Modified: Thu, 15 Jun 2023 02:10:20 GMT  
		Size: 52.5 MB (52460860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37854b0fe089d09909e34d4c66fc7eb9e08fce3fbb3e5407adfd0eaefb3cb658`  
		Last Modified: Thu, 15 Jun 2023 02:10:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778d35eb0679c0cbc03351be52db33dfcdf311de7128cb831039130c2da5b1de`  
		Last Modified: Thu, 15 Jun 2023 02:10:11 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dbe13d617eb1937369e1808d5764593eed5ed5042c70dc8b6d1c0084d99342`  
		Last Modified: Thu, 15 Jun 2023 02:10:11 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14.7`

```console
$ docker pull consul@sha256:29d89c3dbde641e96bbe614b3cd1ca6c6ab82e725246bd3a3fce7798da906c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.14.7` - linux; amd64

```console
$ docker pull consul@sha256:c5363f57ebd80acdb08eda2706da303d574800d96686d598991107ce24c4a001
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57044114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e9cc702d7e2c93f02d73f6bc9900bf40e573cdb6fe7909dc26ab96b4847964`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:21:43 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 17 May 2023 23:21:43 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 17 May 2023 23:21:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 17 May 2023 23:21:44 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 17 May 2023 23:21:50 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 17 May 2023 23:21:50 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 17 May 2023 23:21:51 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 17 May 2023 23:21:51 GMT
VOLUME [/consul/data]
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8300
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 17 May 2023 23:21:51 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 17 May 2023 23:21:51 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 17 May 2023 23:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:21:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001bd6942da9d529f3ee86b01a88dcc743c72ecbf1d0194c81b4a9a46153e098`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0349ac67f6ae8d5912668dbf97fc9b77f276f3d74b18e8d088ec322b22ae7e74`  
		Last Modified: Wed, 17 May 2023 23:22:20 GMT  
		Size: 54.2 MB (54214088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dca13136f6774035c2dde75e01445cfeba66d37c4f4d5cb339ff16c7d08b098`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8316eeeac047103fd632fd127a134a8a087670a870090c849ed9169ed3797e7a`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbce098aeaa4602998aa92509a72512a177c6063ee11b0895f0a41176b1ec6`  
		Last Modified: Wed, 17 May 2023 23:22:13 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:76774bc44c2b7040ded267f98bafcbd21e51f0a273a9ec7104061003ea718344
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53915157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9e7e579584bf7000eafde666109aa211a997112846d69440dd32a264c8d715`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:32 GMT
ADD file:b987db82fa4ce6e623de49a50612c1fd91c5ab2209a62a5727ab3436c2923e91 in / 
# Wed, 14 Jun 2023 18:49:32 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:25:07 GMT
ARG CONSUL_VERSION=1.14.7
# Thu, 15 Jun 2023 01:25:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 01:25:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 01:25:08 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 01:25:16 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 01:25:16 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 01:25:17 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 01:25:18 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 01:25:18 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 01:25:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 01:25:18 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 01:25:18 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 01:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 01:25:19 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:41c5c5b38e13af18def277385607129664fb24993d262d4b601a381e776482a9`  
		Last Modified: Wed, 14 Jun 2023 18:50:19 GMT  
		Size: 2.6 MB (2633060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13258989c71f0866b1872bd573153814a2a2c93c342273fba4ed6a792182129`  
		Last Modified: Thu, 15 Jun 2023 01:25:59 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac89fe99dbbe4eba59f1ca42f37934e55a7f59adb5a2c6b15c3240c07757181`  
		Last Modified: Thu, 15 Jun 2023 01:26:06 GMT  
		Size: 51.3 MB (51278669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f5d738f14227165a546d2e63c856023cabd733faa64ade1c794a78301fa45`  
		Last Modified: Thu, 15 Jun 2023 01:25:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acd9da5831b67d17370e2e34f2a3865d7048fc68c0917915f22644d29601761`  
		Last Modified: Thu, 15 Jun 2023 01:25:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76516ecfce632226d1910cd73bf01b327c7f721fc24cdd90cb65dd3f2f1f2e87`  
		Last Modified: Thu, 15 Jun 2023 01:25:59 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b3bbb6fde64dd95386ed690b7f6ab0a1fb60dd7a53d6b61563972c8298fc3b47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53470559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e16b3f9d963b06ff99a163e453989437fd8ebd19c9ec7cad9909e978494ab54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:10 GMT
ADD file:2b463f242cb7bf946452bb4781838348ecbe80da144fbab09f51d7e050dc68f3 in / 
# Wed, 14 Jun 2023 20:49:11 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:38:18 GMT
ARG CONSUL_VERSION=1.14.7
# Wed, 14 Jun 2023 22:38:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 14 Jun 2023 22:38:18 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Jun 2023 22:38:18 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Jun 2023 22:38:24 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Jun 2023 22:38:26 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Jun 2023 22:38:26 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Jun 2023 22:38:26 GMT
VOLUME [/consul/data]
# Wed, 14 Jun 2023 22:38:26 GMT
EXPOSE 8300
# Wed, 14 Jun 2023 22:38:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Jun 2023 22:38:26 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Jun 2023 22:38:26 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Jun 2023 22:38:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:38:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a147224bf413aeffbbfcdcb5104d35c647256a5c32083f4d8134f09a4e74ddeb`  
		Last Modified: Wed, 14 Jun 2023 20:49:52 GMT  
		Size: 2.7 MB (2720801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3fe053a164c645f70317c7bc8676a5770dcf79aad5cb1356b50793b522508e`  
		Last Modified: Wed, 14 Jun 2023 22:39:02 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3394d2371b6ba9115f9694aa39ebf939fe622d48a753a5b13b07165906cc905`  
		Last Modified: Wed, 14 Jun 2023 22:39:08 GMT  
		Size: 50.7 MB (50746334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0246651a8e31d99cc664cbbe638b0385390e21b0f777043a794f1b0e322d898`  
		Last Modified: Wed, 14 Jun 2023 22:39:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a0ac696786bf981eb29e9af83dd052a84b265f995bb0e83a655915aa59a201`  
		Last Modified: Wed, 14 Jun 2023 22:39:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42b83ab50c9178c73efb554ab56624fb60a8417235e401cb8477c31968e554d`  
		Last Modified: Wed, 14 Jun 2023 22:39:02 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.7` - linux; 386

```console
$ docker pull consul@sha256:1866fda7f3a6054469e95f297ac21acf449eabb794aee84537314ab5f0fe9b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55296444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6795533f8f7d26e8a5927f233a37f213410c902a5fe22f02191fda14e69179`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:34 GMT
ADD file:92f6ab42e26a2cc37a3463b6f6508e29ae194413d31cb95f1609f93f32d2e94d in / 
# Wed, 14 Jun 2023 22:33:34 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:09:19 GMT
ARG CONSUL_VERSION=1.14.7
# Thu, 15 Jun 2023 02:09:19 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 02:09:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 02:09:20 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 02:09:28 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 02:09:28 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 02:09:29 GMT
# ARGS: CONSUL_VERSION=1.14.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 02:09:29 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 02:09:29 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 02:09:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 02:09:29 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 02:09:30 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 02:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 02:09:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:74051fed7c11c74895f7583bcde366e9192af8539de4915832d9c990bd23f581`  
		Last Modified: Wed, 14 Jun 2023 22:34:17 GMT  
		Size: 2.8 MB (2832157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a7b0777832ab41a213293ae6fe8387635051e4230d37f0530c4557c05afae5`  
		Last Modified: Thu, 15 Jun 2023 02:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9419d1945453b686bef523fbad0f84e0f50be79d0685a43b73a012eef0a24dbf`  
		Last Modified: Thu, 15 Jun 2023 02:10:20 GMT  
		Size: 52.5 MB (52460860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37854b0fe089d09909e34d4c66fc7eb9e08fce3fbb3e5407adfd0eaefb3cb658`  
		Last Modified: Thu, 15 Jun 2023 02:10:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778d35eb0679c0cbc03351be52db33dfcdf311de7128cb831039130c2da5b1de`  
		Last Modified: Thu, 15 Jun 2023 02:10:11 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dbe13d617eb1937369e1808d5764593eed5ed5042c70dc8b6d1c0084d99342`  
		Last Modified: Thu, 15 Jun 2023 02:10:11 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.15`

```console
$ docker pull consul@sha256:ed3ba257184af30f2bb2c45c0597391caef8385451a9331b0d27bc27ee6854af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.15` - linux; amd64

```console
$ docker pull consul@sha256:3e1bd5bccd3e78b0aedb6c145ea6d5541f56d1a1156285a1323662367f52fc92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60732422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99d8a688dd368dfc01d7c582a58cce6499b05073367a431a0f1923ae1e75a37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Sun, 04 Jun 2023 17:39:56 GMT
ARG CONSUL_VERSION=1.15.3
# Sun, 04 Jun 2023 17:39:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sun, 04 Jun 2023 17:39:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sun, 04 Jun 2023 17:39:57 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sun, 04 Jun 2023 17:40:03 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sun, 04 Jun 2023 17:40:04 GMT
VOLUME [/consul/data]
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8300
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Sun, 04 Jun 2023 17:40:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sun, 04 Jun 2023 17:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 Jun 2023 17:40:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915e8f855b6690f0165f7483cef7426ea7282acab6c7b3702b3717021dd89a`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab4e1ebead2514ccc0c2dbe58db284c6cf68996f3c4810d393e144eaccd0ab0`  
		Last Modified: Sun, 04 Jun 2023 17:40:25 GMT  
		Size: 57.9 MB (57902395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef376008726bca2cf9c89957ce3f2d98b94b8fe38125f5250510378ab918391`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ea914c246d6fc3771aef0af68d090aa389bace0ea5039e9814bc4fccccd3b`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c5462ee475b4cfd8b65edf36981eb63a7db89e1112e7939e1c26b79fbec28c`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15` - linux; arm variant v6

```console
$ docker pull consul@sha256:a874d643975df120ac026e8a46b52cf97a4b304cdf323ed8ecc6ee6b294129e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56002497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57bbec227d1fdaf4829dd95668203fda2d95012de1f8c9bbc0f264d0885ed07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:32 GMT
ADD file:b987db82fa4ce6e623de49a50612c1fd91c5ab2209a62a5727ab3436c2923e91 in / 
# Wed, 14 Jun 2023 18:49:32 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:24:47 GMT
ARG CONSUL_VERSION=1.15.3
# Thu, 15 Jun 2023 01:24:48 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 01:24:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 01:24:48 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 01:25:02 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 01:25:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 01:25:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 01:25:04 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 01:25:04 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 01:25:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 01:25:05 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 01:25:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 01:25:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 01:25:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:41c5c5b38e13af18def277385607129664fb24993d262d4b601a381e776482a9`  
		Last Modified: Wed, 14 Jun 2023 18:50:19 GMT  
		Size: 2.6 MB (2633060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8796af763c35c14dc95c5ad51aacc6f38c14348304e99b8cc10349154b5c09`  
		Last Modified: Thu, 15 Jun 2023 01:25:42 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e3c869dfe4483f82ac26aa64118cf487cd77b6f0dc3a0d4033572c09129f43`  
		Last Modified: Thu, 15 Jun 2023 01:25:49 GMT  
		Size: 53.4 MB (53366009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f814c47a45d6b6c2a38fccdcd11e6d191a76377dd0b516dc97ac55b85fdf3`  
		Last Modified: Thu, 15 Jun 2023 01:25:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7891295a6c6879c09f5a98d3bc68a3c2d31e1e6780dd5a1e240b692b7c4eb6ac`  
		Last Modified: Thu, 15 Jun 2023 01:25:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af772f64f4cb332268597afef992effc116cf23974e455316e055b700e5a991a`  
		Last Modified: Thu, 15 Jun 2023 01:25:43 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:733356ad5c3089b578aaad28a9f2bbb31b220ac5f07e3fa008569ae458d15c04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55564525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a85d69e11c0e9880128d4a99fa858fad196c1e933a34b6f0885502aca09164a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:10 GMT
ADD file:2b463f242cb7bf946452bb4781838348ecbe80da144fbab09f51d7e050dc68f3 in / 
# Wed, 14 Jun 2023 20:49:11 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:38:06 GMT
ARG CONSUL_VERSION=1.15.3
# Wed, 14 Jun 2023 22:38:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 14 Jun 2023 22:38:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Jun 2023 22:38:07 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Jun 2023 22:38:13 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Jun 2023 22:38:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Jun 2023 22:38:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Jun 2023 22:38:14 GMT
VOLUME [/consul/data]
# Wed, 14 Jun 2023 22:38:14 GMT
EXPOSE 8300
# Wed, 14 Jun 2023 22:38:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Jun 2023 22:38:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Jun 2023 22:38:15 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Jun 2023 22:38:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:38:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a147224bf413aeffbbfcdcb5104d35c647256a5c32083f4d8134f09a4e74ddeb`  
		Last Modified: Wed, 14 Jun 2023 20:49:52 GMT  
		Size: 2.7 MB (2720801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6ecb287f8b815309167e72faab910b64cb461ee06c98450cb4c084d0e9d4f`  
		Last Modified: Wed, 14 Jun 2023 22:38:47 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82182ccdd08bc2d5e0f933a67cb0222fa72719c4dc5effd2e04ca976bb9a806`  
		Last Modified: Wed, 14 Jun 2023 22:38:52 GMT  
		Size: 52.8 MB (52840295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89685cf8b3738470c953cfd090b45530b5acab8d954dbf7f225ec8ac2d93f1dc`  
		Last Modified: Wed, 14 Jun 2023 22:38:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d34fe79a71e3ab6ab5fa8d70274cf1e5baa9167ded20425153a6ab99ff2f926`  
		Last Modified: Wed, 14 Jun 2023 22:38:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdca9688632f01af824b8c4402a9a0380aac986343ae5ad4d9783c460a6d1ea5`  
		Last Modified: Wed, 14 Jun 2023 22:38:48 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15` - linux; 386

```console
$ docker pull consul@sha256:b505abbc1a1df399278379244b784a867e6c6ae55bddf51dfeb12538227aeb8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57407314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7dd6acf9c71389e37b6a88c038284d26ccfe33d9a0a918a7be15811166b37e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:34 GMT
ADD file:92f6ab42e26a2cc37a3463b6f6508e29ae194413d31cb95f1609f93f32d2e94d in / 
# Wed, 14 Jun 2023 22:33:34 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:08:59 GMT
ARG CONSUL_VERSION=1.15.3
# Thu, 15 Jun 2023 02:08:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 02:09:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 02:09:00 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 02:09:13 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 02:09:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 02:09:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 02:09:15 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 02:09:15 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 02:09:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 02:09:15 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 02:09:15 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 02:09:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 02:09:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:74051fed7c11c74895f7583bcde366e9192af8539de4915832d9c990bd23f581`  
		Last Modified: Wed, 14 Jun 2023 22:34:17 GMT  
		Size: 2.8 MB (2832157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548514d225a829f6346f1663060a7761ced4cd659e113c1e775b24f44a3faf56`  
		Last Modified: Thu, 15 Jun 2023 02:09:51 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97eb9fed92133fe529e12458818700eb8cd8e497db8328b09c50a485e0eb0c76`  
		Last Modified: Thu, 15 Jun 2023 02:10:00 GMT  
		Size: 54.6 MB (54571732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70eefb0e171067dca85a06604a27cf0af253f687696a01771d3de5dffd8de5a`  
		Last Modified: Thu, 15 Jun 2023 02:09:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bd4b965b1bb55cafe71ab0146699690503b5908aa548c3bca8a35d74dd8eb1`  
		Last Modified: Thu, 15 Jun 2023 02:09:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c580ce52064ee829c5e589ca4149150eed8515c9fb8ef6cb97574a03932ff`  
		Last Modified: Thu, 15 Jun 2023 02:09:51 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.15.3`

```console
$ docker pull consul@sha256:ed3ba257184af30f2bb2c45c0597391caef8385451a9331b0d27bc27ee6854af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.15.3` - linux; amd64

```console
$ docker pull consul@sha256:3e1bd5bccd3e78b0aedb6c145ea6d5541f56d1a1156285a1323662367f52fc92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60732422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99d8a688dd368dfc01d7c582a58cce6499b05073367a431a0f1923ae1e75a37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Sun, 04 Jun 2023 17:39:56 GMT
ARG CONSUL_VERSION=1.15.3
# Sun, 04 Jun 2023 17:39:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sun, 04 Jun 2023 17:39:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sun, 04 Jun 2023 17:39:57 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sun, 04 Jun 2023 17:40:03 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sun, 04 Jun 2023 17:40:04 GMT
VOLUME [/consul/data]
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8300
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Sun, 04 Jun 2023 17:40:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sun, 04 Jun 2023 17:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 Jun 2023 17:40:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915e8f855b6690f0165f7483cef7426ea7282acab6c7b3702b3717021dd89a`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab4e1ebead2514ccc0c2dbe58db284c6cf68996f3c4810d393e144eaccd0ab0`  
		Last Modified: Sun, 04 Jun 2023 17:40:25 GMT  
		Size: 57.9 MB (57902395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef376008726bca2cf9c89957ce3f2d98b94b8fe38125f5250510378ab918391`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ea914c246d6fc3771aef0af68d090aa389bace0ea5039e9814bc4fccccd3b`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c5462ee475b4cfd8b65edf36981eb63a7db89e1112e7939e1c26b79fbec28c`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15.3` - linux; arm variant v6

```console
$ docker pull consul@sha256:a874d643975df120ac026e8a46b52cf97a4b304cdf323ed8ecc6ee6b294129e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56002497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57bbec227d1fdaf4829dd95668203fda2d95012de1f8c9bbc0f264d0885ed07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:32 GMT
ADD file:b987db82fa4ce6e623de49a50612c1fd91c5ab2209a62a5727ab3436c2923e91 in / 
# Wed, 14 Jun 2023 18:49:32 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:24:47 GMT
ARG CONSUL_VERSION=1.15.3
# Thu, 15 Jun 2023 01:24:48 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 01:24:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 01:24:48 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 01:25:02 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 01:25:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 01:25:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 01:25:04 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 01:25:04 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 01:25:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 01:25:05 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 01:25:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 01:25:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 01:25:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:41c5c5b38e13af18def277385607129664fb24993d262d4b601a381e776482a9`  
		Last Modified: Wed, 14 Jun 2023 18:50:19 GMT  
		Size: 2.6 MB (2633060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8796af763c35c14dc95c5ad51aacc6f38c14348304e99b8cc10349154b5c09`  
		Last Modified: Thu, 15 Jun 2023 01:25:42 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e3c869dfe4483f82ac26aa64118cf487cd77b6f0dc3a0d4033572c09129f43`  
		Last Modified: Thu, 15 Jun 2023 01:25:49 GMT  
		Size: 53.4 MB (53366009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f814c47a45d6b6c2a38fccdcd11e6d191a76377dd0b516dc97ac55b85fdf3`  
		Last Modified: Thu, 15 Jun 2023 01:25:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7891295a6c6879c09f5a98d3bc68a3c2d31e1e6780dd5a1e240b692b7c4eb6ac`  
		Last Modified: Thu, 15 Jun 2023 01:25:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af772f64f4cb332268597afef992effc116cf23974e455316e055b700e5a991a`  
		Last Modified: Thu, 15 Jun 2023 01:25:43 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15.3` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:733356ad5c3089b578aaad28a9f2bbb31b220ac5f07e3fa008569ae458d15c04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55564525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a85d69e11c0e9880128d4a99fa858fad196c1e933a34b6f0885502aca09164a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:10 GMT
ADD file:2b463f242cb7bf946452bb4781838348ecbe80da144fbab09f51d7e050dc68f3 in / 
# Wed, 14 Jun 2023 20:49:11 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:38:06 GMT
ARG CONSUL_VERSION=1.15.3
# Wed, 14 Jun 2023 22:38:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 14 Jun 2023 22:38:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Jun 2023 22:38:07 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Jun 2023 22:38:13 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Jun 2023 22:38:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Jun 2023 22:38:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Jun 2023 22:38:14 GMT
VOLUME [/consul/data]
# Wed, 14 Jun 2023 22:38:14 GMT
EXPOSE 8300
# Wed, 14 Jun 2023 22:38:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Jun 2023 22:38:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Jun 2023 22:38:15 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Jun 2023 22:38:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:38:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a147224bf413aeffbbfcdcb5104d35c647256a5c32083f4d8134f09a4e74ddeb`  
		Last Modified: Wed, 14 Jun 2023 20:49:52 GMT  
		Size: 2.7 MB (2720801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6ecb287f8b815309167e72faab910b64cb461ee06c98450cb4c084d0e9d4f`  
		Last Modified: Wed, 14 Jun 2023 22:38:47 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82182ccdd08bc2d5e0f933a67cb0222fa72719c4dc5effd2e04ca976bb9a806`  
		Last Modified: Wed, 14 Jun 2023 22:38:52 GMT  
		Size: 52.8 MB (52840295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89685cf8b3738470c953cfd090b45530b5acab8d954dbf7f225ec8ac2d93f1dc`  
		Last Modified: Wed, 14 Jun 2023 22:38:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d34fe79a71e3ab6ab5fa8d70274cf1e5baa9167ded20425153a6ab99ff2f926`  
		Last Modified: Wed, 14 Jun 2023 22:38:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdca9688632f01af824b8c4402a9a0380aac986343ae5ad4d9783c460a6d1ea5`  
		Last Modified: Wed, 14 Jun 2023 22:38:48 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15.3` - linux; 386

```console
$ docker pull consul@sha256:b505abbc1a1df399278379244b784a867e6c6ae55bddf51dfeb12538227aeb8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57407314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7dd6acf9c71389e37b6a88c038284d26ccfe33d9a0a918a7be15811166b37e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:34 GMT
ADD file:92f6ab42e26a2cc37a3463b6f6508e29ae194413d31cb95f1609f93f32d2e94d in / 
# Wed, 14 Jun 2023 22:33:34 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:08:59 GMT
ARG CONSUL_VERSION=1.15.3
# Thu, 15 Jun 2023 02:08:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 02:09:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 02:09:00 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 02:09:13 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 02:09:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 02:09:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 02:09:15 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 02:09:15 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 02:09:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 02:09:15 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 02:09:15 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 02:09:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 02:09:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:74051fed7c11c74895f7583bcde366e9192af8539de4915832d9c990bd23f581`  
		Last Modified: Wed, 14 Jun 2023 22:34:17 GMT  
		Size: 2.8 MB (2832157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548514d225a829f6346f1663060a7761ced4cd659e113c1e775b24f44a3faf56`  
		Last Modified: Thu, 15 Jun 2023 02:09:51 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97eb9fed92133fe529e12458818700eb8cd8e497db8328b09c50a485e0eb0c76`  
		Last Modified: Thu, 15 Jun 2023 02:10:00 GMT  
		Size: 54.6 MB (54571732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70eefb0e171067dca85a06604a27cf0af253f687696a01771d3de5dffd8de5a`  
		Last Modified: Thu, 15 Jun 2023 02:09:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bd4b965b1bb55cafe71ab0146699690503b5908aa548c3bca8a35d74dd8eb1`  
		Last Modified: Thu, 15 Jun 2023 02:09:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c580ce52064ee829c5e589ca4149150eed8515c9fb8ef6cb97574a03932ff`  
		Last Modified: Thu, 15 Jun 2023 02:09:51 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:ed3ba257184af30f2bb2c45c0597391caef8385451a9331b0d27bc27ee6854af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:3e1bd5bccd3e78b0aedb6c145ea6d5541f56d1a1156285a1323662367f52fc92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60732422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99d8a688dd368dfc01d7c582a58cce6499b05073367a431a0f1923ae1e75a37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Sun, 04 Jun 2023 17:39:56 GMT
ARG CONSUL_VERSION=1.15.3
# Sun, 04 Jun 2023 17:39:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sun, 04 Jun 2023 17:39:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sun, 04 Jun 2023 17:39:57 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sun, 04 Jun 2023 17:40:03 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sun, 04 Jun 2023 17:40:04 GMT
VOLUME [/consul/data]
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8300
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Sun, 04 Jun 2023 17:40:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sun, 04 Jun 2023 17:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 Jun 2023 17:40:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915e8f855b6690f0165f7483cef7426ea7282acab6c7b3702b3717021dd89a`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab4e1ebead2514ccc0c2dbe58db284c6cf68996f3c4810d393e144eaccd0ab0`  
		Last Modified: Sun, 04 Jun 2023 17:40:25 GMT  
		Size: 57.9 MB (57902395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef376008726bca2cf9c89957ce3f2d98b94b8fe38125f5250510378ab918391`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ea914c246d6fc3771aef0af68d090aa389bace0ea5039e9814bc4fccccd3b`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c5462ee475b4cfd8b65edf36981eb63a7db89e1112e7939e1c26b79fbec28c`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:a874d643975df120ac026e8a46b52cf97a4b304cdf323ed8ecc6ee6b294129e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56002497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57bbec227d1fdaf4829dd95668203fda2d95012de1f8c9bbc0f264d0885ed07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:32 GMT
ADD file:b987db82fa4ce6e623de49a50612c1fd91c5ab2209a62a5727ab3436c2923e91 in / 
# Wed, 14 Jun 2023 18:49:32 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:24:47 GMT
ARG CONSUL_VERSION=1.15.3
# Thu, 15 Jun 2023 01:24:48 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 01:24:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 01:24:48 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 01:25:02 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 01:25:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 01:25:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 01:25:04 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 01:25:04 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 01:25:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 01:25:05 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 01:25:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 01:25:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 01:25:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:41c5c5b38e13af18def277385607129664fb24993d262d4b601a381e776482a9`  
		Last Modified: Wed, 14 Jun 2023 18:50:19 GMT  
		Size: 2.6 MB (2633060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8796af763c35c14dc95c5ad51aacc6f38c14348304e99b8cc10349154b5c09`  
		Last Modified: Thu, 15 Jun 2023 01:25:42 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e3c869dfe4483f82ac26aa64118cf487cd77b6f0dc3a0d4033572c09129f43`  
		Last Modified: Thu, 15 Jun 2023 01:25:49 GMT  
		Size: 53.4 MB (53366009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f814c47a45d6b6c2a38fccdcd11e6d191a76377dd0b516dc97ac55b85fdf3`  
		Last Modified: Thu, 15 Jun 2023 01:25:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7891295a6c6879c09f5a98d3bc68a3c2d31e1e6780dd5a1e240b692b7c4eb6ac`  
		Last Modified: Thu, 15 Jun 2023 01:25:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af772f64f4cb332268597afef992effc116cf23974e455316e055b700e5a991a`  
		Last Modified: Thu, 15 Jun 2023 01:25:43 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:733356ad5c3089b578aaad28a9f2bbb31b220ac5f07e3fa008569ae458d15c04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55564525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a85d69e11c0e9880128d4a99fa858fad196c1e933a34b6f0885502aca09164a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:10 GMT
ADD file:2b463f242cb7bf946452bb4781838348ecbe80da144fbab09f51d7e050dc68f3 in / 
# Wed, 14 Jun 2023 20:49:11 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:38:06 GMT
ARG CONSUL_VERSION=1.15.3
# Wed, 14 Jun 2023 22:38:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 14 Jun 2023 22:38:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Jun 2023 22:38:07 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Jun 2023 22:38:13 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Jun 2023 22:38:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Jun 2023 22:38:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Jun 2023 22:38:14 GMT
VOLUME [/consul/data]
# Wed, 14 Jun 2023 22:38:14 GMT
EXPOSE 8300
# Wed, 14 Jun 2023 22:38:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Jun 2023 22:38:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Jun 2023 22:38:15 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Jun 2023 22:38:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:38:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a147224bf413aeffbbfcdcb5104d35c647256a5c32083f4d8134f09a4e74ddeb`  
		Last Modified: Wed, 14 Jun 2023 20:49:52 GMT  
		Size: 2.7 MB (2720801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6ecb287f8b815309167e72faab910b64cb461ee06c98450cb4c084d0e9d4f`  
		Last Modified: Wed, 14 Jun 2023 22:38:47 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82182ccdd08bc2d5e0f933a67cb0222fa72719c4dc5effd2e04ca976bb9a806`  
		Last Modified: Wed, 14 Jun 2023 22:38:52 GMT  
		Size: 52.8 MB (52840295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89685cf8b3738470c953cfd090b45530b5acab8d954dbf7f225ec8ac2d93f1dc`  
		Last Modified: Wed, 14 Jun 2023 22:38:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d34fe79a71e3ab6ab5fa8d70274cf1e5baa9167ded20425153a6ab99ff2f926`  
		Last Modified: Wed, 14 Jun 2023 22:38:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdca9688632f01af824b8c4402a9a0380aac986343ae5ad4d9783c460a6d1ea5`  
		Last Modified: Wed, 14 Jun 2023 22:38:48 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:b505abbc1a1df399278379244b784a867e6c6ae55bddf51dfeb12538227aeb8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57407314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7dd6acf9c71389e37b6a88c038284d26ccfe33d9a0a918a7be15811166b37e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:34 GMT
ADD file:92f6ab42e26a2cc37a3463b6f6508e29ae194413d31cb95f1609f93f32d2e94d in / 
# Wed, 14 Jun 2023 22:33:34 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:08:59 GMT
ARG CONSUL_VERSION=1.15.3
# Thu, 15 Jun 2023 02:08:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 15 Jun 2023 02:09:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 15 Jun 2023 02:09:00 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 15 Jun 2023 02:09:13 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 15 Jun 2023 02:09:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 15 Jun 2023 02:09:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 15 Jun 2023 02:09:15 GMT
VOLUME [/consul/data]
# Thu, 15 Jun 2023 02:09:15 GMT
EXPOSE 8300
# Thu, 15 Jun 2023 02:09:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 15 Jun 2023 02:09:15 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 15 Jun 2023 02:09:15 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Jun 2023 02:09:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 02:09:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:74051fed7c11c74895f7583bcde366e9192af8539de4915832d9c990bd23f581`  
		Last Modified: Wed, 14 Jun 2023 22:34:17 GMT  
		Size: 2.8 MB (2832157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548514d225a829f6346f1663060a7761ced4cd659e113c1e775b24f44a3faf56`  
		Last Modified: Thu, 15 Jun 2023 02:09:51 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97eb9fed92133fe529e12458818700eb8cd8e497db8328b09c50a485e0eb0c76`  
		Last Modified: Thu, 15 Jun 2023 02:10:00 GMT  
		Size: 54.6 MB (54571732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70eefb0e171067dca85a06604a27cf0af253f687696a01771d3de5dffd8de5a`  
		Last Modified: Thu, 15 Jun 2023 02:09:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bd4b965b1bb55cafe71ab0146699690503b5908aa548c3bca8a35d74dd8eb1`  
		Last Modified: Thu, 15 Jun 2023 02:09:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c580ce52064ee829c5e589ca4149150eed8515c9fb8ef6cb97574a03932ff`  
		Last Modified: Thu, 15 Jun 2023 02:09:51 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
