<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.12`](#consul11012)
-	[`consul:1.11`](#consul111)
-	[`consul:1.11.7`](#consul1117)
-	[`consul:1.12`](#consul112)
-	[`consul:1.12.3`](#consul1123)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:22aaefa008b7ef0cf6fd0997e564947ddfaf66ebb4883139d5e3cdcc067bd880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:8f4d8138591d6ada8165fc95bc18c32f10072573cc2f7645c7ade4e183ab2dea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43256009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b68d8424447ad33282f6952dac98fa6ac77e13e83a721c2b0c0f5718a20672d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 19:19:58 GMT
ARG CONSUL_VERSION=1.10.12
# Thu, 14 Jul 2022 19:19:58 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 19:19:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 19:19:59 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 19:20:04 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 19:20:05 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 19:20:06 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 19:20:06 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 19:20:06 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 19:20:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 19:20:06 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 19:20:06 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 19:20:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 19:20:06 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303fe1ce3855603861fb8e71c0e96b171aa9bd58cd7217b68ef0ac9bcd81004d`  
		Last Modified: Thu, 14 Jul 2022 19:20:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e9fb3062e9f85a447c9884be7894bfe6b61bab7f3971a293eca19e55fbde5f`  
		Last Modified: Thu, 14 Jul 2022 19:21:00 GMT  
		Size: 40.4 MB (40438072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e26375e4941f50b531b970f12d396a69c33f24bfd2f2271b0bff36788a6da`  
		Last Modified: Thu, 14 Jul 2022 19:20:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0d07d6bfe98ad9e97f0bbcb2bdf14cbc6d8cbc40e27e979d1a6f1ca8718979`  
		Last Modified: Thu, 14 Jul 2022 19:20:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b532be97c5e1466927826f3a51b3a34c62d6b78cc159b2d8df52ec7cdebcdc`  
		Last Modified: Thu, 14 Jul 2022 19:20:54 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:f11bccca3bc89115e1a40b9c7585687fc34b663492b0a00c3c89196ebca43665
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41043848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd961a6954bd5f251bb68935e0aff9bab9b115185bcc235af39026981aa8a1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:50:48 GMT
ARG CONSUL_VERSION=1.10.12
# Thu, 14 Jul 2022 18:50:48 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:50:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:50:50 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:51:02 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:51:04 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:51:05 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:51:05 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:51:06 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:51:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:51:07 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:51:07 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:51:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:51:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2536579b2bcac12d8b3921d5c52822283732bb7287acb12d06ce59de83822dad`  
		Last Modified: Thu, 14 Jul 2022 18:53:06 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc32d83acb5cfecd323abed26510d4db17c9999f96f61472d87061f11845bc4`  
		Last Modified: Thu, 14 Jul 2022 18:53:27 GMT  
		Size: 38.4 MB (38418494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e98589f4cec755c73fcaed1e819758215532ea7caf8fa0aa6784fd39b64f4e`  
		Last Modified: Thu, 14 Jul 2022 18:53:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8a82a6a59b1892fec5f2ef2ad7d6f0ea6bee9f9fd757cbbc7e5d00d7921392`  
		Last Modified: Thu, 14 Jul 2022 18:53:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556c7ac97189cd0210a05217e14fff01807c99406171e9a577a31802a5910113`  
		Last Modified: Thu, 14 Jul 2022 18:53:06 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:65ab15bc824d77c85c8581e6dc3128bbdb40ba8efe0a070c28b70f64648d8e17
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40902782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a65fe6f2605d7028b1fcb4fc9296f25a92ecd9e559da108f5bec2db063d7c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:40:22 GMT
ARG CONSUL_VERSION=1.10.12
# Thu, 14 Jul 2022 18:40:23 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:40:24 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:40:25 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:40:31 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:40:31 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:40:32 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:40:33 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:40:34 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:40:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:40:36 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:40:38 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:40:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28302b2801f36b9f8ef78fce8de3a417033661c9082cde12f08271216bb27240`  
		Last Modified: Thu, 14 Jul 2022 18:41:37 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614d254a5b06fec51b4c4d7b71b5a5811b76805344988ed979d8997add3a7579`  
		Last Modified: Thu, 14 Jul 2022 18:41:42 GMT  
		Size: 38.2 MB (38182985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf4cd258676ab0a1be6823b08070648a020bf55971f92946608e6ed79a6e0d4`  
		Last Modified: Thu, 14 Jul 2022 18:41:37 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c4f25f93650e479032bf5f13824f6360f0876f49a150d440bfddc8915d9920`  
		Last Modified: Thu, 14 Jul 2022 18:41:37 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d56b043d509c748a4e2700fbd30c78a505200f1c9a2e6713c2167680f52ec7`  
		Last Modified: Thu, 14 Jul 2022 18:41:37 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:5a15a04a006a9d34a01ba2f41a120c956e69ac9054987aaa367e6db25d12d11e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42094960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03f4b5a678dbdd680e21860da1b26f1f9208476999e015d589b218fd30a050d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:39:14 GMT
ARG CONSUL_VERSION=1.10.12
# Thu, 14 Jul 2022 18:39:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:39:16 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:39:17 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:39:23 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:39:23 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:39:24 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:39:25 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:39:26 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:39:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:39:28 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:39:30 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:39:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:39:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eed8617bf0534e48395b127167f9c8b7cbdee474704996f6f166f8b2659c6d`  
		Last Modified: Thu, 14 Jul 2022 18:40:35 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5353b41648a77e78f275adc2c78d3d39a2838f6a86aa20f3c83ec8110fc78f5`  
		Last Modified: Thu, 14 Jul 2022 18:40:41 GMT  
		Size: 39.3 MB (39272664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7a2605624cda5e6d4c3bc6226537c92d831062d37899112171ac5b45239035`  
		Last Modified: Thu, 14 Jul 2022 18:40:35 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724cea88979d9fb9de30585902522105e86702557ba1f276628cf5413776443e`  
		Last Modified: Thu, 14 Jul 2022 18:40:35 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18d85163fe85321ee15f2f2d85d325285da0cbad1e27cf2ac5bbfa2e969c28`  
		Last Modified: Thu, 14 Jul 2022 18:40:35 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.12`

```console
$ docker pull consul@sha256:22aaefa008b7ef0cf6fd0997e564947ddfaf66ebb4883139d5e3cdcc067bd880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.12` - linux; amd64

```console
$ docker pull consul@sha256:8f4d8138591d6ada8165fc95bc18c32f10072573cc2f7645c7ade4e183ab2dea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43256009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b68d8424447ad33282f6952dac98fa6ac77e13e83a721c2b0c0f5718a20672d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 19:19:58 GMT
ARG CONSUL_VERSION=1.10.12
# Thu, 14 Jul 2022 19:19:58 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 19:19:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 19:19:59 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 19:20:04 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 19:20:05 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 19:20:06 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 19:20:06 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 19:20:06 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 19:20:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 19:20:06 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 19:20:06 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 19:20:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 19:20:06 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303fe1ce3855603861fb8e71c0e96b171aa9bd58cd7217b68ef0ac9bcd81004d`  
		Last Modified: Thu, 14 Jul 2022 19:20:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e9fb3062e9f85a447c9884be7894bfe6b61bab7f3971a293eca19e55fbde5f`  
		Last Modified: Thu, 14 Jul 2022 19:21:00 GMT  
		Size: 40.4 MB (40438072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e26375e4941f50b531b970f12d396a69c33f24bfd2f2271b0bff36788a6da`  
		Last Modified: Thu, 14 Jul 2022 19:20:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0d07d6bfe98ad9e97f0bbcb2bdf14cbc6d8cbc40e27e979d1a6f1ca8718979`  
		Last Modified: Thu, 14 Jul 2022 19:20:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b532be97c5e1466927826f3a51b3a34c62d6b78cc159b2d8df52ec7cdebcdc`  
		Last Modified: Thu, 14 Jul 2022 19:20:54 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.12` - linux; arm variant v6

```console
$ docker pull consul@sha256:f11bccca3bc89115e1a40b9c7585687fc34b663492b0a00c3c89196ebca43665
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41043848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd961a6954bd5f251bb68935e0aff9bab9b115185bcc235af39026981aa8a1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:50:48 GMT
ARG CONSUL_VERSION=1.10.12
# Thu, 14 Jul 2022 18:50:48 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:50:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:50:50 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:51:02 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:51:04 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:51:05 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:51:05 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:51:06 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:51:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:51:07 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:51:07 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:51:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:51:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2536579b2bcac12d8b3921d5c52822283732bb7287acb12d06ce59de83822dad`  
		Last Modified: Thu, 14 Jul 2022 18:53:06 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc32d83acb5cfecd323abed26510d4db17c9999f96f61472d87061f11845bc4`  
		Last Modified: Thu, 14 Jul 2022 18:53:27 GMT  
		Size: 38.4 MB (38418494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e98589f4cec755c73fcaed1e819758215532ea7caf8fa0aa6784fd39b64f4e`  
		Last Modified: Thu, 14 Jul 2022 18:53:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8a82a6a59b1892fec5f2ef2ad7d6f0ea6bee9f9fd757cbbc7e5d00d7921392`  
		Last Modified: Thu, 14 Jul 2022 18:53:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556c7ac97189cd0210a05217e14fff01807c99406171e9a577a31802a5910113`  
		Last Modified: Thu, 14 Jul 2022 18:53:06 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.12` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:65ab15bc824d77c85c8581e6dc3128bbdb40ba8efe0a070c28b70f64648d8e17
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40902782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a65fe6f2605d7028b1fcb4fc9296f25a92ecd9e559da108f5bec2db063d7c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:40:22 GMT
ARG CONSUL_VERSION=1.10.12
# Thu, 14 Jul 2022 18:40:23 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:40:24 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:40:25 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:40:31 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:40:31 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:40:32 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:40:33 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:40:34 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:40:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:40:36 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:40:38 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:40:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28302b2801f36b9f8ef78fce8de3a417033661c9082cde12f08271216bb27240`  
		Last Modified: Thu, 14 Jul 2022 18:41:37 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614d254a5b06fec51b4c4d7b71b5a5811b76805344988ed979d8997add3a7579`  
		Last Modified: Thu, 14 Jul 2022 18:41:42 GMT  
		Size: 38.2 MB (38182985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf4cd258676ab0a1be6823b08070648a020bf55971f92946608e6ed79a6e0d4`  
		Last Modified: Thu, 14 Jul 2022 18:41:37 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c4f25f93650e479032bf5f13824f6360f0876f49a150d440bfddc8915d9920`  
		Last Modified: Thu, 14 Jul 2022 18:41:37 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d56b043d509c748a4e2700fbd30c78a505200f1c9a2e6713c2167680f52ec7`  
		Last Modified: Thu, 14 Jul 2022 18:41:37 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.12` - linux; 386

```console
$ docker pull consul@sha256:5a15a04a006a9d34a01ba2f41a120c956e69ac9054987aaa367e6db25d12d11e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42094960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03f4b5a678dbdd680e21860da1b26f1f9208476999e015d589b218fd30a050d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:39:14 GMT
ARG CONSUL_VERSION=1.10.12
# Thu, 14 Jul 2022 18:39:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:39:16 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:39:17 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:39:23 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:39:23 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:39:24 GMT
# ARGS: CONSUL_VERSION=1.10.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:39:25 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:39:26 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:39:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:39:28 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:39:30 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:39:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:39:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eed8617bf0534e48395b127167f9c8b7cbdee474704996f6f166f8b2659c6d`  
		Last Modified: Thu, 14 Jul 2022 18:40:35 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5353b41648a77e78f275adc2c78d3d39a2838f6a86aa20f3c83ec8110fc78f5`  
		Last Modified: Thu, 14 Jul 2022 18:40:41 GMT  
		Size: 39.3 MB (39272664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7a2605624cda5e6d4c3bc6226537c92d831062d37899112171ac5b45239035`  
		Last Modified: Thu, 14 Jul 2022 18:40:35 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724cea88979d9fb9de30585902522105e86702557ba1f276628cf5413776443e`  
		Last Modified: Thu, 14 Jul 2022 18:40:35 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18d85163fe85321ee15f2f2d85d325285da0cbad1e27cf2ac5bbfa2e969c28`  
		Last Modified: Thu, 14 Jul 2022 18:40:35 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11`

```console
$ docker pull consul@sha256:577ba349f3d0eeeb84467aa7123681adcbfe5e2de5a858c526c8f8d7d0d5d6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11` - linux; amd64

```console
$ docker pull consul@sha256:700fffe4dddf65da69736e0cf93d3c19ce9de6514f9d520c321fc95b8c0ed24c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43997533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c359761d01ca256c34d6afd050cb0ab5d11500a072b0a088879f23f92d9bd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 19:19:47 GMT
ARG CONSUL_VERSION=1.11.7
# Thu, 14 Jul 2022 19:19:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 19:19:47 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 19:19:47 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 19:19:53 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 19:19:54 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 19:19:54 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 19:19:55 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 19:19:55 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 19:19:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 19:19:55 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 19:19:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 19:19:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 19:19:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142f1d91b3c627ac08354015715f8507bccc36475fcf2a543f6d32c65159433d`  
		Last Modified: Thu, 14 Jul 2022 19:20:39 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7f0cb100ec2050ec5822b0d16e86f60dd16a56ccb2ad028a127f053bdf766b`  
		Last Modified: Thu, 14 Jul 2022 19:20:44 GMT  
		Size: 41.2 MB (41179591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8670c8f9990308d737ed6c8919664d63dcfbc65de0a0a13fddc8441ae4ec42ef`  
		Last Modified: Thu, 14 Jul 2022 19:20:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadbfc6b20d6bb3bd6909bef448827cd158832c63ad55b4b05a71122373b1bdc`  
		Last Modified: Thu, 14 Jul 2022 19:20:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a0cdc1037325d706eadca311c891e7fd0f2787c771ddfc422188ee057807e0`  
		Last Modified: Thu, 14 Jul 2022 19:20:39 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm variant v6

```console
$ docker pull consul@sha256:06c8587de8c97f000e2124797353e4aa24c87d512dfd74a188dfa7718a612345
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41741442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efadbab443ebebbee32a504c4041ae0739211d9a2bf288188e82b3349ece782c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:50:15 GMT
ARG CONSUL_VERSION=1.11.7
# Thu, 14 Jul 2022 18:50:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:50:16 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:50:17 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:50:29 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:50:31 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:50:32 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:50:33 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:50:33 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:50:34 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:50:34 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:50:35 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:50:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:50:35 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acace14f3c38a2f70505266571433a40eb6df226950bdc0733f18b4a79d05abf`  
		Last Modified: Thu, 14 Jul 2022 18:52:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc378c2adfbaf7f7434b4d6fcedf07a54128fff5b59d28789fcaeee65e6a4037`  
		Last Modified: Thu, 14 Jul 2022 18:52:54 GMT  
		Size: 39.1 MB (39116084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7ba43a2691369732efa404a687b9a37329d83be33212c3cfecdec511bc699c`  
		Last Modified: Thu, 14 Jul 2022 18:52:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985b94a576852cdc8d5692b213bad580140a72313cd798a3c87ed640abc8ed4c`  
		Last Modified: Thu, 14 Jul 2022 18:52:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ea4dd545f5ca959eb22f526a18075fcf24f363b461358facbb75470b1473`  
		Last Modified: Thu, 14 Jul 2022 18:52:32 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1136abc399a9fa74dac4f272b464c6368642adeb564183fe9ee18efcd1b7e9c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41568576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7279be88ab75453e8aee0877c764a894420dfb115442fbf94779eb8b731262f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:39:59 GMT
ARG CONSUL_VERSION=1.11.7
# Thu, 14 Jul 2022 18:40:00 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:40:01 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:40:02 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:40:08 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:40:08 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:40:09 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:40:10 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:40:11 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:40:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:40:13 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:40:15 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:40:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:40:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731f1351c80ea6463ca0169ad6dba9d61e78e063a4de9b43d0b43ea3168b7228`  
		Last Modified: Thu, 14 Jul 2022 18:41:20 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bda6ffec2921c0ea1e062ea1a2311b4c6467f029b5d1f9a7724526b7178fad6`  
		Last Modified: Thu, 14 Jul 2022 18:41:25 GMT  
		Size: 38.8 MB (38848777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caf6b8cc65b0eb49db04175242a4f4fe6c244832b9b8e4f30a1daee92cac3ff`  
		Last Modified: Thu, 14 Jul 2022 18:41:20 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b9e9f434ca97ff218723cf2dbc82b9e7d6e70c0e92429457062be376237463`  
		Last Modified: Thu, 14 Jul 2022 18:41:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0caac02f417ff07f3c7e2efb1eaee90581ff70e099044f608ce86433ce716a6`  
		Last Modified: Thu, 14 Jul 2022 18:41:20 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; 386

```console
$ docker pull consul@sha256:dced085990775b9d90bfd6bedc1a8c425b0cc0634ca0fd8bfb4662d5437bbfa1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42807697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe61df10ff269cb5875cbfe1cb2129458cd432aa974c963a30f783c1013a279`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:38:51 GMT
ARG CONSUL_VERSION=1.11.7
# Thu, 14 Jul 2022 18:38:52 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:38:53 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:38:54 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:39:00 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:39:00 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:39:01 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:39:02 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:39:03 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:39:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:39:05 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:39:07 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:39:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:39:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb01350b41a619072f39c08b0ef50a8e5c4eed0f82adb190888dd8481d0e5f`  
		Last Modified: Thu, 14 Jul 2022 18:40:18 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555b902d597ca868ca2a237d7c406e959fdaccb29dc521c7a7bba7e82cafffbf`  
		Last Modified: Thu, 14 Jul 2022 18:40:24 GMT  
		Size: 40.0 MB (39985397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ff3c6a374508c36924c7b86fd063bc1d3ec338dda7b775b26f011d04c9e50a`  
		Last Modified: Thu, 14 Jul 2022 18:40:20 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621e1b432c9beabb7c650a779df9c623c653482706c5e39d9cc2ce3a390b0ab5`  
		Last Modified: Thu, 14 Jul 2022 18:40:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218edb874f878629962dcabd31eb9fec3bd6ba2da756e060380f3f33907648e2`  
		Last Modified: Thu, 14 Jul 2022 18:40:19 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11.7`

```console
$ docker pull consul@sha256:577ba349f3d0eeeb84467aa7123681adcbfe5e2de5a858c526c8f8d7d0d5d6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11.7` - linux; amd64

```console
$ docker pull consul@sha256:700fffe4dddf65da69736e0cf93d3c19ce9de6514f9d520c321fc95b8c0ed24c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43997533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c359761d01ca256c34d6afd050cb0ab5d11500a072b0a088879f23f92d9bd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 19:19:47 GMT
ARG CONSUL_VERSION=1.11.7
# Thu, 14 Jul 2022 19:19:47 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 19:19:47 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 19:19:47 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 19:19:53 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 19:19:54 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 19:19:54 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 19:19:55 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 19:19:55 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 19:19:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 19:19:55 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 19:19:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 19:19:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 19:19:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142f1d91b3c627ac08354015715f8507bccc36475fcf2a543f6d32c65159433d`  
		Last Modified: Thu, 14 Jul 2022 19:20:39 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7f0cb100ec2050ec5822b0d16e86f60dd16a56ccb2ad028a127f053bdf766b`  
		Last Modified: Thu, 14 Jul 2022 19:20:44 GMT  
		Size: 41.2 MB (41179591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8670c8f9990308d737ed6c8919664d63dcfbc65de0a0a13fddc8441ae4ec42ef`  
		Last Modified: Thu, 14 Jul 2022 19:20:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadbfc6b20d6bb3bd6909bef448827cd158832c63ad55b4b05a71122373b1bdc`  
		Last Modified: Thu, 14 Jul 2022 19:20:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a0cdc1037325d706eadca311c891e7fd0f2787c771ddfc422188ee057807e0`  
		Last Modified: Thu, 14 Jul 2022 19:20:39 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:06c8587de8c97f000e2124797353e4aa24c87d512dfd74a188dfa7718a612345
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41741442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efadbab443ebebbee32a504c4041ae0739211d9a2bf288188e82b3349ece782c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:50:15 GMT
ARG CONSUL_VERSION=1.11.7
# Thu, 14 Jul 2022 18:50:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:50:16 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:50:17 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:50:29 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:50:31 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:50:32 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:50:33 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:50:33 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:50:34 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:50:34 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:50:35 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:50:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:50:35 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acace14f3c38a2f70505266571433a40eb6df226950bdc0733f18b4a79d05abf`  
		Last Modified: Thu, 14 Jul 2022 18:52:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc378c2adfbaf7f7434b4d6fcedf07a54128fff5b59d28789fcaeee65e6a4037`  
		Last Modified: Thu, 14 Jul 2022 18:52:54 GMT  
		Size: 39.1 MB (39116084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7ba43a2691369732efa404a687b9a37329d83be33212c3cfecdec511bc699c`  
		Last Modified: Thu, 14 Jul 2022 18:52:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985b94a576852cdc8d5692b213bad580140a72313cd798a3c87ed640abc8ed4c`  
		Last Modified: Thu, 14 Jul 2022 18:52:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ea4dd545f5ca959eb22f526a18075fcf24f363b461358facbb75470b1473`  
		Last Modified: Thu, 14 Jul 2022 18:52:32 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1136abc399a9fa74dac4f272b464c6368642adeb564183fe9ee18efcd1b7e9c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41568576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7279be88ab75453e8aee0877c764a894420dfb115442fbf94779eb8b731262f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:39:59 GMT
ARG CONSUL_VERSION=1.11.7
# Thu, 14 Jul 2022 18:40:00 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:40:01 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:40:02 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:40:08 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:40:08 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:40:09 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:40:10 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:40:11 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:40:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:40:13 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:40:15 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:40:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:40:16 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731f1351c80ea6463ca0169ad6dba9d61e78e063a4de9b43d0b43ea3168b7228`  
		Last Modified: Thu, 14 Jul 2022 18:41:20 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bda6ffec2921c0ea1e062ea1a2311b4c6467f029b5d1f9a7724526b7178fad6`  
		Last Modified: Thu, 14 Jul 2022 18:41:25 GMT  
		Size: 38.8 MB (38848777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caf6b8cc65b0eb49db04175242a4f4fe6c244832b9b8e4f30a1daee92cac3ff`  
		Last Modified: Thu, 14 Jul 2022 18:41:20 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b9e9f434ca97ff218723cf2dbc82b9e7d6e70c0e92429457062be376237463`  
		Last Modified: Thu, 14 Jul 2022 18:41:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0caac02f417ff07f3c7e2efb1eaee90581ff70e099044f608ce86433ce716a6`  
		Last Modified: Thu, 14 Jul 2022 18:41:20 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.7` - linux; 386

```console
$ docker pull consul@sha256:dced085990775b9d90bfd6bedc1a8c425b0cc0634ca0fd8bfb4662d5437bbfa1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42807697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe61df10ff269cb5875cbfe1cb2129458cd432aa974c963a30f783c1013a279`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:38:51 GMT
ARG CONSUL_VERSION=1.11.7
# Thu, 14 Jul 2022 18:38:52 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:38:53 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:38:54 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:39:00 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:39:00 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:39:01 GMT
# ARGS: CONSUL_VERSION=1.11.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:39:02 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:39:03 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:39:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:39:05 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:39:07 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:39:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:39:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdb01350b41a619072f39c08b0ef50a8e5c4eed0f82adb190888dd8481d0e5f`  
		Last Modified: Thu, 14 Jul 2022 18:40:18 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555b902d597ca868ca2a237d7c406e959fdaccb29dc521c7a7bba7e82cafffbf`  
		Last Modified: Thu, 14 Jul 2022 18:40:24 GMT  
		Size: 40.0 MB (39985397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ff3c6a374508c36924c7b86fd063bc1d3ec338dda7b775b26f011d04c9e50a`  
		Last Modified: Thu, 14 Jul 2022 18:40:20 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621e1b432c9beabb7c650a779df9c623c653482706c5e39d9cc2ce3a390b0ab5`  
		Last Modified: Thu, 14 Jul 2022 18:40:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218edb874f878629962dcabd31eb9fec3bd6ba2da756e060380f3f33907648e2`  
		Last Modified: Thu, 14 Jul 2022 18:40:19 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.12`

```console
$ docker pull consul@sha256:fad7bb5613939b48fcf01f65d5f4b32cf31d89757184f9893db729dce8de7161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.12` - linux; amd64

```console
$ docker pull consul@sha256:d1405ded5367efeb70f23f43385931b8c5d3170c7d57f7ed23fd1fb137baa346
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49564115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649c43a5f531a9a9486384343789ef8c0ced0e8b9fb7174f98e151a9a0ca7a64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 19:19:35 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 19:19:35 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 19:19:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 19:19:36 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 19:19:41 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 19:19:42 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 19:19:43 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 19:19:43 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 19:19:43 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 19:19:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 19:19:43 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 19:19:43 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 19:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 19:19:44 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1314a7a83e5b8854b47d2a22bd05428cd084ee9c8c7b7c474040a7c5cca15472`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda61b59674fb35f3b1b3b4fe94ae2b9fc697653624aa984d768e0414ba25b90`  
		Last Modified: Thu, 14 Jul 2022 19:20:26 GMT  
		Size: 46.7 MB (46746175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ad171f9d230317a5f80fb5318a14bd25cfbd58cdac2f425520786bc6d5d878`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5226d81572d6b863e743d85b65e0cc7bd174826b8afc0ffd4255639d63ea1490`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcaf0dd27116658f03cb7c978c64b47d54834076f8c2856b1780266e1f10e9a`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; arm variant v6

```console
$ docker pull consul@sha256:07803867b7c16c020cc0513b2f882b7c00e7ced48a8fe344a7c4b7a657a7b60f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47426865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f3be25e15d966079a1a068a5c2c9dbe4ca4ce13bff1d08aebb4d18059c0179`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:49:41 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 18:49:42 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:49:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:49:44 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:49:57 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:49:58 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:50:00 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:50:00 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:50:01 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:50:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:50:02 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:50:02 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:50:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:50:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd6e2e354c2eec200d354a8bb7f61f5872f6922cc73149f6710a3e8b072a284`  
		Last Modified: Thu, 14 Jul 2022 18:51:51 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19bd1f1cf3f9cd6317a18dafd724c012c62a1ee1b5398788214a8596ee2c9fe`  
		Last Modified: Thu, 14 Jul 2022 18:52:16 GMT  
		Size: 44.8 MB (44801511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2e79bd50208892f07f207ccffb549416149df16ef7ea12c0e6307e04f02cca`  
		Last Modified: Thu, 14 Jul 2022 18:51:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e22ed43a58f05ee71575a5bc333237dbdab104709916e07aac4858ca0d511`  
		Last Modified: Thu, 14 Jul 2022 18:51:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510a4c78bba431dc5413c0986a33f9fbca4cd36c5bc766fefc8ff59579c0365f`  
		Last Modified: Thu, 14 Jul 2022 18:51:51 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:599648ef005d3ef93af9dacf3e87f05eef5ae8f2e29fc638f2455f1e27eb8540
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47167200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f28ace522f609389f7511e2bafe250fd9ba175bdc6eb16c0cbae2b6d3aa226d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:39:35 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 18:39:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:39:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:39:38 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:39:44 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:39:45 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:39:46 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:39:47 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:39:48 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:39:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:39:50 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:39:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:39:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:39:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef55fc0efd418f9e0b564af9c45928e005e0b38f2dbe14f3468f7ae4f0222cec`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5436ddd7c5dbd711b21e48630d101fcd938d5dabaf7f12ff104d23f20ea87260`  
		Last Modified: Thu, 14 Jul 2022 18:41:05 GMT  
		Size: 44.4 MB (44447402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624fd5a018c20d9d36f156fb8c7d0961c4c391cc68047f2f9de7be091fcfe734`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaab46090c4ddfc931c1bd3838e6adfd7a2db4604d172ed3ff236eb2eef79d00`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d918f5d9b73550f7da6346c3864805786f63b93aa5984f30924b3a8bba6e9b1`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; 386

```console
$ docker pull consul@sha256:6752889eeac0ebefbc25d871179bffe0f0aabebf61decf5673f2669d7740102d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48626420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28d0edcab361500b222d55939abaf9f175834184f72ae6a1a78a52690d0f182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:38:25 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 18:38:26 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:38:27 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:38:28 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:38:36 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:38:36 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:38:37 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:38:38 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:38:39 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:38:40 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:38:41 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:38:43 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:38:44 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ffb6c6cfc52ced5ba32c058f167e69dfe3b838e76ae2a2310979e660b6117a`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80677307bc806c8736a4fad2775f5333f9cc9f61511177b108026005f11c5c8d`  
		Last Modified: Thu, 14 Jul 2022 18:40:04 GMT  
		Size: 45.8 MB (45804121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee35fd0dfcb67ad5650c515baa71c5b1c2f30c64cc725afb994b9734074051af`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee080bbe3f2d47a432f79cf916a4f3d30b4cf5468a11bb7ed0ff5d05c2a7fd6`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1770f90a0375427147c28163e5b407b6f0c35a055231dfae09e0f2b3c06bd0`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.12.3`

```console
$ docker pull consul@sha256:fad7bb5613939b48fcf01f65d5f4b32cf31d89757184f9893db729dce8de7161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.12.3` - linux; amd64

```console
$ docker pull consul@sha256:d1405ded5367efeb70f23f43385931b8c5d3170c7d57f7ed23fd1fb137baa346
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49564115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649c43a5f531a9a9486384343789ef8c0ced0e8b9fb7174f98e151a9a0ca7a64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 19:19:35 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 19:19:35 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 19:19:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 19:19:36 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 19:19:41 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 19:19:42 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 19:19:43 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 19:19:43 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 19:19:43 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 19:19:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 19:19:43 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 19:19:43 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 19:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 19:19:44 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1314a7a83e5b8854b47d2a22bd05428cd084ee9c8c7b7c474040a7c5cca15472`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda61b59674fb35f3b1b3b4fe94ae2b9fc697653624aa984d768e0414ba25b90`  
		Last Modified: Thu, 14 Jul 2022 19:20:26 GMT  
		Size: 46.7 MB (46746175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ad171f9d230317a5f80fb5318a14bd25cfbd58cdac2f425520786bc6d5d878`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5226d81572d6b863e743d85b65e0cc7bd174826b8afc0ffd4255639d63ea1490`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcaf0dd27116658f03cb7c978c64b47d54834076f8c2856b1780266e1f10e9a`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.3` - linux; arm variant v6

```console
$ docker pull consul@sha256:07803867b7c16c020cc0513b2f882b7c00e7ced48a8fe344a7c4b7a657a7b60f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47426865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f3be25e15d966079a1a068a5c2c9dbe4ca4ce13bff1d08aebb4d18059c0179`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:49:41 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 18:49:42 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:49:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:49:44 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:49:57 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:49:58 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:50:00 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:50:00 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:50:01 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:50:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:50:02 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:50:02 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:50:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:50:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd6e2e354c2eec200d354a8bb7f61f5872f6922cc73149f6710a3e8b072a284`  
		Last Modified: Thu, 14 Jul 2022 18:51:51 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19bd1f1cf3f9cd6317a18dafd724c012c62a1ee1b5398788214a8596ee2c9fe`  
		Last Modified: Thu, 14 Jul 2022 18:52:16 GMT  
		Size: 44.8 MB (44801511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2e79bd50208892f07f207ccffb549416149df16ef7ea12c0e6307e04f02cca`  
		Last Modified: Thu, 14 Jul 2022 18:51:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e22ed43a58f05ee71575a5bc333237dbdab104709916e07aac4858ca0d511`  
		Last Modified: Thu, 14 Jul 2022 18:51:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510a4c78bba431dc5413c0986a33f9fbca4cd36c5bc766fefc8ff59579c0365f`  
		Last Modified: Thu, 14 Jul 2022 18:51:51 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.3` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:599648ef005d3ef93af9dacf3e87f05eef5ae8f2e29fc638f2455f1e27eb8540
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47167200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f28ace522f609389f7511e2bafe250fd9ba175bdc6eb16c0cbae2b6d3aa226d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:39:35 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 18:39:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:39:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:39:38 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:39:44 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:39:45 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:39:46 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:39:47 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:39:48 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:39:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:39:50 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:39:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:39:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:39:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef55fc0efd418f9e0b564af9c45928e005e0b38f2dbe14f3468f7ae4f0222cec`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5436ddd7c5dbd711b21e48630d101fcd938d5dabaf7f12ff104d23f20ea87260`  
		Last Modified: Thu, 14 Jul 2022 18:41:05 GMT  
		Size: 44.4 MB (44447402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624fd5a018c20d9d36f156fb8c7d0961c4c391cc68047f2f9de7be091fcfe734`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaab46090c4ddfc931c1bd3838e6adfd7a2db4604d172ed3ff236eb2eef79d00`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d918f5d9b73550f7da6346c3864805786f63b93aa5984f30924b3a8bba6e9b1`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.3` - linux; 386

```console
$ docker pull consul@sha256:6752889eeac0ebefbc25d871179bffe0f0aabebf61decf5673f2669d7740102d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48626420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28d0edcab361500b222d55939abaf9f175834184f72ae6a1a78a52690d0f182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:38:25 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 18:38:26 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:38:27 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:38:28 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:38:36 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:38:36 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:38:37 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:38:38 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:38:39 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:38:40 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:38:41 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:38:43 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:38:44 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ffb6c6cfc52ced5ba32c058f167e69dfe3b838e76ae2a2310979e660b6117a`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80677307bc806c8736a4fad2775f5333f9cc9f61511177b108026005f11c5c8d`  
		Last Modified: Thu, 14 Jul 2022 18:40:04 GMT  
		Size: 45.8 MB (45804121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee35fd0dfcb67ad5650c515baa71c5b1c2f30c64cc725afb994b9734074051af`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee080bbe3f2d47a432f79cf916a4f3d30b4cf5468a11bb7ed0ff5d05c2a7fd6`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1770f90a0375427147c28163e5b407b6f0c35a055231dfae09e0f2b3c06bd0`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:fad7bb5613939b48fcf01f65d5f4b32cf31d89757184f9893db729dce8de7161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:d1405ded5367efeb70f23f43385931b8c5d3170c7d57f7ed23fd1fb137baa346
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49564115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649c43a5f531a9a9486384343789ef8c0ced0e8b9fb7174f98e151a9a0ca7a64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 19:19:35 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 19:19:35 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 19:19:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 19:19:36 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 19:19:41 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 19:19:42 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 19:19:43 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 19:19:43 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 19:19:43 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 19:19:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 19:19:43 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 19:19:43 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 19:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 19:19:44 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1314a7a83e5b8854b47d2a22bd05428cd084ee9c8c7b7c474040a7c5cca15472`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda61b59674fb35f3b1b3b4fe94ae2b9fc697653624aa984d768e0414ba25b90`  
		Last Modified: Thu, 14 Jul 2022 19:20:26 GMT  
		Size: 46.7 MB (46746175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ad171f9d230317a5f80fb5318a14bd25cfbd58cdac2f425520786bc6d5d878`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5226d81572d6b863e743d85b65e0cc7bd174826b8afc0ffd4255639d63ea1490`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcaf0dd27116658f03cb7c978c64b47d54834076f8c2856b1780266e1f10e9a`  
		Last Modified: Thu, 14 Jul 2022 19:20:20 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:07803867b7c16c020cc0513b2f882b7c00e7ced48a8fe344a7c4b7a657a7b60f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47426865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f3be25e15d966079a1a068a5c2c9dbe4ca4ce13bff1d08aebb4d18059c0179`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:49:41 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 18:49:42 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:49:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:49:44 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:49:57 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:49:58 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:50:00 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:50:00 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:50:01 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:50:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:50:02 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:50:02 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:50:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:50:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd6e2e354c2eec200d354a8bb7f61f5872f6922cc73149f6710a3e8b072a284`  
		Last Modified: Thu, 14 Jul 2022 18:51:51 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19bd1f1cf3f9cd6317a18dafd724c012c62a1ee1b5398788214a8596ee2c9fe`  
		Last Modified: Thu, 14 Jul 2022 18:52:16 GMT  
		Size: 44.8 MB (44801511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2e79bd50208892f07f207ccffb549416149df16ef7ea12c0e6307e04f02cca`  
		Last Modified: Thu, 14 Jul 2022 18:51:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e22ed43a58f05ee71575a5bc333237dbdab104709916e07aac4858ca0d511`  
		Last Modified: Thu, 14 Jul 2022 18:51:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510a4c78bba431dc5413c0986a33f9fbca4cd36c5bc766fefc8ff59579c0365f`  
		Last Modified: Thu, 14 Jul 2022 18:51:51 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:599648ef005d3ef93af9dacf3e87f05eef5ae8f2e29fc638f2455f1e27eb8540
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47167200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f28ace522f609389f7511e2bafe250fd9ba175bdc6eb16c0cbae2b6d3aa226d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:39:35 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 18:39:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:39:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:39:38 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:39:44 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:39:45 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:39:46 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:39:47 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:39:48 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:39:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:39:50 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:39:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:39:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:39:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef55fc0efd418f9e0b564af9c45928e005e0b38f2dbe14f3468f7ae4f0222cec`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5436ddd7c5dbd711b21e48630d101fcd938d5dabaf7f12ff104d23f20ea87260`  
		Last Modified: Thu, 14 Jul 2022 18:41:05 GMT  
		Size: 44.4 MB (44447402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624fd5a018c20d9d36f156fb8c7d0961c4c391cc68047f2f9de7be091fcfe734`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaab46090c4ddfc931c1bd3838e6adfd7a2db4604d172ed3ff236eb2eef79d00`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d918f5d9b73550f7da6346c3864805786f63b93aa5984f30924b3a8bba6e9b1`  
		Last Modified: Thu, 14 Jul 2022 18:41:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:6752889eeac0ebefbc25d871179bffe0f0aabebf61decf5673f2669d7740102d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48626420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28d0edcab361500b222d55939abaf9f175834184f72ae6a1a78a52690d0f182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Thu, 14 Jul 2022 18:38:25 GMT
ARG CONSUL_VERSION=1.12.3
# Thu, 14 Jul 2022 18:38:26 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 14 Jul 2022 18:38:27 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 14 Jul 2022 18:38:28 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 14 Jul 2022 18:38:36 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 14 Jul 2022 18:38:36 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 14 Jul 2022 18:38:37 GMT
# ARGS: CONSUL_VERSION=1.12.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 14 Jul 2022 18:38:38 GMT
VOLUME [/consul/data]
# Thu, 14 Jul 2022 18:38:39 GMT
EXPOSE 8300
# Thu, 14 Jul 2022 18:38:40 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 14 Jul 2022 18:38:41 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 14 Jul 2022 18:38:43 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 14 Jul 2022 18:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Jul 2022 18:38:44 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ffb6c6cfc52ced5ba32c058f167e69dfe3b838e76ae2a2310979e660b6117a`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80677307bc806c8736a4fad2775f5333f9cc9f61511177b108026005f11c5c8d`  
		Last Modified: Thu, 14 Jul 2022 18:40:04 GMT  
		Size: 45.8 MB (45804121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee35fd0dfcb67ad5650c515baa71c5b1c2f30c64cc725afb994b9734074051af`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee080bbe3f2d47a432f79cf916a4f3d30b4cf5468a11bb7ed0ff5d05c2a7fd6`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1770f90a0375427147c28163e5b407b6f0c35a055231dfae09e0f2b3c06bd0`  
		Last Modified: Thu, 14 Jul 2022 18:39:52 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
