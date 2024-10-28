<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.8.3`](#api-firewall083)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.8.3`

```console
$ docker pull api-firewall@sha256:ece37de5aeec41ba981b542962dfd26868442a0bbd4e785d36a8fb390119ef04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.8.3` - linux; amd64

```console
$ docker pull api-firewall@sha256:47b60c6cd7557d5bb68cbdaf32954d28151c55b09b0145ffd284734b96399f0a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14855630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a44f8db6bce1c76325b20dda6a6a4a0f4646af597b9c7f4851469c737e7f76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:37:40 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 06 Sep 2024 22:37:40 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 22:37:41 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 28 Oct 2024 18:19:22 GMT
ENV APIFIREWALL_VERSION=v0.8.3
# Mon, 28 Oct 2024 18:19:24 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='a171cc705d31ee926c1de099269e44a7b9578f57602a084aef8a7d8c4b1fef0f';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='98d1e41181f9b49c334dad086899f0239abee13d50e6015e240dfdf956247c1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='aa2389d8c80e52e4356b6a4c24c7987717c20e2bb6925d5e4f91885df7e5a39e';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 28 Oct 2024 18:19:25 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 28 Oct 2024 18:19:25 GMT
USER api-firewall
# Mon, 28 Oct 2024 18:19:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 18:19:25 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf40d3d747019b351164402fd0d05781c2bfcac612fc6f83ea4684a63bd6885`  
		Last Modified: Fri, 06 Sep 2024 22:37:52 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9330c16c229560a4852c52ff593a431b85629e4c3cade6a2edb9698b365ae34`  
		Last Modified: Mon, 28 Oct 2024 18:19:35 GMT  
		Size: 11.2 MB (11230560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bed235c0da357532855beacafd795db79966d5a681851a167059fc2dad7595a`  
		Last Modified: Mon, 28 Oct 2024 18:19:33 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.8.3` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:55b0115ff6962a7b03d45915b1e726df60a633d1d9616df434a2552b7c5c6615
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14461205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279a74edbd4f68a55eff3e60310f2b2d40fd7b3c7f26678a6eeac6cfbac72ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:03:55 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 06 Sep 2024 23:03:55 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 23:03:55 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 28 Oct 2024 18:39:15 GMT
ENV APIFIREWALL_VERSION=v0.8.3
# Mon, 28 Oct 2024 18:39:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='a171cc705d31ee926c1de099269e44a7b9578f57602a084aef8a7d8c4b1fef0f';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='98d1e41181f9b49c334dad086899f0239abee13d50e6015e240dfdf956247c1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='aa2389d8c80e52e4356b6a4c24c7987717c20e2bb6925d5e4f91885df7e5a39e';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 28 Oct 2024 18:39:18 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 28 Oct 2024 18:39:18 GMT
USER api-firewall
# Mon, 28 Oct 2024 18:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 18:39:19 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65232210b9dc810dc66a876c2ed0208b0c13199f26228136e2fd2684553e72f3`  
		Last Modified: Fri, 06 Sep 2024 23:04:04 GMT  
		Size: 909.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec413fe92a0695a184ba7bd3ab2173eb53e475d0231f01e534bb1633890eec8c`  
		Last Modified: Mon, 28 Oct 2024 18:39:27 GMT  
		Size: 10.4 MB (10372297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b165c4f2dac4b05686f7e171e696f59b79ae86e6ef19676bb76259ad0ba07167`  
		Last Modified: Mon, 28 Oct 2024 18:39:26 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.8.3` - linux; 386

```console
$ docker pull api-firewall@sha256:fe1edddcaef2ca015adcfb88995ef20ca1f4cfde33a88a0d18eec53c70cf1a07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13219819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902a9391c247f32937828f13109884dc5d2b18b4bd6017e539cd9e3e995f9ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:57:20 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 07 Sep 2024 01:57:20 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Sep 2024 01:57:20 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 28 Oct 2024 18:38:15 GMT
ENV APIFIREWALL_VERSION=v0.8.3
# Mon, 28 Oct 2024 18:38:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='a171cc705d31ee926c1de099269e44a7b9578f57602a084aef8a7d8c4b1fef0f';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='98d1e41181f9b49c334dad086899f0239abee13d50e6015e240dfdf956247c1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='aa2389d8c80e52e4356b6a4c24c7987717c20e2bb6925d5e4f91885df7e5a39e';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 28 Oct 2024 18:38:18 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 28 Oct 2024 18:38:18 GMT
USER api-firewall
# Mon, 28 Oct 2024 18:38:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 18:38:19 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60e28bdd66504eebf65ca6892bddb641021505edb92d813701b39c212ef4cef`  
		Last Modified: Sat, 07 Sep 2024 01:57:30 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214df8351eb76c8e5def80697a88f0b76ec44018f56bb2737d5cc95e58eb0fd7`  
		Last Modified: Mon, 28 Oct 2024 18:38:29 GMT  
		Size: 9.7 MB (9749387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0011d256505a51a9f7efe54f53c629be9e04343f325d3dcc0db803577dcd5fbb`  
		Last Modified: Mon, 28 Oct 2024 18:38:27 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:ece37de5aeec41ba981b542962dfd26868442a0bbd4e785d36a8fb390119ef04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:47b60c6cd7557d5bb68cbdaf32954d28151c55b09b0145ffd284734b96399f0a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14855630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a44f8db6bce1c76325b20dda6a6a4a0f4646af597b9c7f4851469c737e7f76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:37:40 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 06 Sep 2024 22:37:40 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 22:37:41 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 28 Oct 2024 18:19:22 GMT
ENV APIFIREWALL_VERSION=v0.8.3
# Mon, 28 Oct 2024 18:19:24 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='a171cc705d31ee926c1de099269e44a7b9578f57602a084aef8a7d8c4b1fef0f';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='98d1e41181f9b49c334dad086899f0239abee13d50e6015e240dfdf956247c1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='aa2389d8c80e52e4356b6a4c24c7987717c20e2bb6925d5e4f91885df7e5a39e';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 28 Oct 2024 18:19:25 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 28 Oct 2024 18:19:25 GMT
USER api-firewall
# Mon, 28 Oct 2024 18:19:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 18:19:25 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf40d3d747019b351164402fd0d05781c2bfcac612fc6f83ea4684a63bd6885`  
		Last Modified: Fri, 06 Sep 2024 22:37:52 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9330c16c229560a4852c52ff593a431b85629e4c3cade6a2edb9698b365ae34`  
		Last Modified: Mon, 28 Oct 2024 18:19:35 GMT  
		Size: 11.2 MB (11230560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bed235c0da357532855beacafd795db79966d5a681851a167059fc2dad7595a`  
		Last Modified: Mon, 28 Oct 2024 18:19:33 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:55b0115ff6962a7b03d45915b1e726df60a633d1d9616df434a2552b7c5c6615
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14461205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e279a74edbd4f68a55eff3e60310f2b2d40fd7b3c7f26678a6eeac6cfbac72ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:03:55 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 06 Sep 2024 23:03:55 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 23:03:55 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 28 Oct 2024 18:39:15 GMT
ENV APIFIREWALL_VERSION=v0.8.3
# Mon, 28 Oct 2024 18:39:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='a171cc705d31ee926c1de099269e44a7b9578f57602a084aef8a7d8c4b1fef0f';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='98d1e41181f9b49c334dad086899f0239abee13d50e6015e240dfdf956247c1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='aa2389d8c80e52e4356b6a4c24c7987717c20e2bb6925d5e4f91885df7e5a39e';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 28 Oct 2024 18:39:18 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 28 Oct 2024 18:39:18 GMT
USER api-firewall
# Mon, 28 Oct 2024 18:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 18:39:19 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65232210b9dc810dc66a876c2ed0208b0c13199f26228136e2fd2684553e72f3`  
		Last Modified: Fri, 06 Sep 2024 23:04:04 GMT  
		Size: 909.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec413fe92a0695a184ba7bd3ab2173eb53e475d0231f01e534bb1633890eec8c`  
		Last Modified: Mon, 28 Oct 2024 18:39:27 GMT  
		Size: 10.4 MB (10372297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b165c4f2dac4b05686f7e171e696f59b79ae86e6ef19676bb76259ad0ba07167`  
		Last Modified: Mon, 28 Oct 2024 18:39:26 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:fe1edddcaef2ca015adcfb88995ef20ca1f4cfde33a88a0d18eec53c70cf1a07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13219819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902a9391c247f32937828f13109884dc5d2b18b4bd6017e539cd9e3e995f9ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 01:57:20 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 07 Sep 2024 01:57:20 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Sep 2024 01:57:20 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 28 Oct 2024 18:38:15 GMT
ENV APIFIREWALL_VERSION=v0.8.3
# Mon, 28 Oct 2024 18:38:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='a171cc705d31ee926c1de099269e44a7b9578f57602a084aef8a7d8c4b1fef0f';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='98d1e41181f9b49c334dad086899f0239abee13d50e6015e240dfdf956247c1b';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='aa2389d8c80e52e4356b6a4c24c7987717c20e2bb6925d5e4f91885df7e5a39e';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 28 Oct 2024 18:38:18 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 28 Oct 2024 18:38:18 GMT
USER api-firewall
# Mon, 28 Oct 2024 18:38:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 18:38:19 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60e28bdd66504eebf65ca6892bddb641021505edb92d813701b39c212ef4cef`  
		Last Modified: Sat, 07 Sep 2024 01:57:30 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214df8351eb76c8e5def80697a88f0b76ec44018f56bb2737d5cc95e58eb0fd7`  
		Last Modified: Mon, 28 Oct 2024 18:38:29 GMT  
		Size: 9.7 MB (9749387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0011d256505a51a9f7efe54f53c629be9e04343f325d3dcc0db803577dcd5fbb`  
		Last Modified: Mon, 28 Oct 2024 18:38:27 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
