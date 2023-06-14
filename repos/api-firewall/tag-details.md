<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.6.10`](#api-firewall0610)
-	[`api-firewall:0.6.11`](#api-firewall0611)
-	[`api-firewall:0.6.9`](#api-firewall069)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.6.10`

```console
$ docker pull api-firewall@sha256:17a2306374ed445a2c46712b2b2bd1179e9cae7c1b38ca8a058e44d99c3c2eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.10` - linux; amd64

```console
$ docker pull api-firewall@sha256:43799aabddcd4a0d5b9cf8617892200eba01f7e9455dffae8a942d71414b85f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8918145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a0b11796a0af91de6ca63859b080b172073a33563dbabd9e939e425c949571`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:33:23 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 29 Mar 2023 19:33:24 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 19:33:24 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 29 Mar 2023 19:33:29 GMT
ENV APIFIREWALL_VERSION=v0.6.10
# Wed, 29 Mar 2023 19:33:31 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='774d29f694142984e11e31443398a973a882d19c491e06390de13f0ceabd04a4';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='6ef69fbafb2503c7b01681d39138ea1abe99da910912fde33b1c317a819d2804';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='a9ccd2757bb4703b70aeea44b8aa992ce0dc1025d36accf311a023d87b1b6f57';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 29 Mar 2023 19:33:31 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 29 Mar 2023 19:33:31 GMT
USER api-firewall
# Wed, 29 Mar 2023 19:33:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:33:32 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085aa53bc6dba091a419b6c3e1f745a1748914575dca4114e1003fac0fdb0938`  
		Last Modified: Wed, 29 Mar 2023 19:33:44 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2afde1001068e2f8babe58586d6e21a2e845bd1c89c500ea763486049703c4d`  
		Last Modified: Wed, 29 Mar 2023 19:33:53 GMT  
		Size: 5.5 MB (5542030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56218a390691827539633511b1fb8772431b64debd0eefb99b92c32bc0e3a8c`  
		Last Modified: Wed, 29 Mar 2023 19:33:52 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.10` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:bc12d5e059c48f59f4ba3e481c05353cf85ffe7ad1be28011bd11df5f5af2719
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8430808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24e325ed2b4da2da2694cfae1182bd3ed08691fe5366699856da30bded3d3dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:55:45 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 14 Jun 2023 22:55:45 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 22:55:45 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 14 Jun 2023 22:55:49 GMT
ENV APIFIREWALL_VERSION=v0.6.10
# Wed, 14 Jun 2023 22:55:51 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='774d29f694142984e11e31443398a973a882d19c491e06390de13f0ceabd04a4';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='6ef69fbafb2503c7b01681d39138ea1abe99da910912fde33b1c317a819d2804';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='a9ccd2757bb4703b70aeea44b8aa992ce0dc1025d36accf311a023d87b1b6f57';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 14 Jun 2023 22:55:51 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 14 Jun 2023 22:55:51 GMT
USER api-firewall
# Wed, 14 Jun 2023 22:55:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:55:51 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7088b7a9c2f02d26362553ecf88235bb03c90adb851cbd1abaf221335f7caf`  
		Last Modified: Wed, 14 Jun 2023 22:56:05 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776279e32c9294345566bc5d94b001947b7435d5e358b38b97bf37cbccc3f026`  
		Last Modified: Wed, 14 Jun 2023 22:56:14 GMT  
		Size: 5.2 MB (5168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918254eaaab2ae9f40dbc157cc36a9aff6e8e9fab822d64b32bff2c3c11cebb0`  
		Last Modified: Wed, 14 Jun 2023 22:56:13 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.10` - linux; 386

```console
$ docker pull api-firewall@sha256:3eceb0cd20b9b658d33d7fb9781b531d26ed9b94fa6beef06fc21a107fad6d88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8816276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4552b7804ecfb5b9babc6fbd17156fde0adff1400dbb97a6390ff05d13826aa7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:30 GMT
ADD file:61bc44c9685b610d18bddd05d2ea1e57b4313f5f433a0a0b7e5269ec24f108b0 in / 
# Wed, 29 Mar 2023 17:38:30 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:17:56 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 29 Mar 2023 19:17:56 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 19:17:57 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 29 Mar 2023 19:18:01 GMT
ENV APIFIREWALL_VERSION=v0.6.10
# Wed, 29 Mar 2023 19:18:04 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='774d29f694142984e11e31443398a973a882d19c491e06390de13f0ceabd04a4';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='6ef69fbafb2503c7b01681d39138ea1abe99da910912fde33b1c317a819d2804';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='a9ccd2757bb4703b70aeea44b8aa992ce0dc1025d36accf311a023d87b1b6f57';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 29 Mar 2023 19:18:04 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 29 Mar 2023 19:18:04 GMT
USER api-firewall
# Wed, 29 Mar 2023 19:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:18:04 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:b2b0f0faedf1b87a3c77cf90d027fb7a25aa67f35400244a4655ad5842a757e4`  
		Last Modified: Wed, 29 Mar 2023 17:39:00 GMT  
		Size: 3.4 MB (3412260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcc6ef49f75790d9a4fb6684238589d6fc72825a48cda0434f5722341357027`  
		Last Modified: Wed, 29 Mar 2023 19:18:17 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0f79cd26ac5ea14fee06181bb3972ccc23a30974d37cf60f3344e3faeb9c9d`  
		Last Modified: Wed, 29 Mar 2023 19:18:27 GMT  
		Size: 5.4 MB (5402458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0d6d2650826491310bfaf692a42392d137d8a22922ee94f728fcc408bf3e49`  
		Last Modified: Wed, 29 Mar 2023 19:18:26 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:0.6.11`

```console
$ docker pull api-firewall@sha256:afc1ba449c30f90576061ebd3b0972c0c2f8ed59c766caf503bb2b02941bf9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.11` - linux; amd64

```console
$ docker pull api-firewall@sha256:034b3292ce4aa149a6cff097e2b9fc58bba2ce1e00c6b4645cabb030c5b52aab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8982910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e38530f647b5d3ba25cba838b86300f8700f4a87f0c72c02945dc7bd5a8a0e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:33:23 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 29 Mar 2023 19:33:24 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 19:33:24 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 29 Mar 2023 19:33:24 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Wed, 29 Mar 2023 19:33:27 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 29 Mar 2023 19:33:27 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 29 Mar 2023 19:33:27 GMT
USER api-firewall
# Wed, 29 Mar 2023 19:33:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:33:27 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085aa53bc6dba091a419b6c3e1f745a1748914575dca4114e1003fac0fdb0938`  
		Last Modified: Wed, 29 Mar 2023 19:33:44 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af23408db57eb594b9ee9b7d3fa611016f3e0d53e2e8e5ac78ef7381b501e1d2`  
		Last Modified: Wed, 29 Mar 2023 19:33:45 GMT  
		Size: 5.6 MB (5606792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67872c68496533df2c11048e1059194bc373470daa17890ef72b6846018a7270`  
		Last Modified: Wed, 29 Mar 2023 19:33:44 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.11` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:3233013d824d2b14368c4799de0622db298d100232771b6eb2279ae2c24973c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8491181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf7552534c17bfb79c344e9e84d2d6e7ed4eab5df285f6f4181068f0c8f93b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:55:45 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 14 Jun 2023 22:55:45 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 22:55:45 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 14 Jun 2023 22:55:45 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Wed, 14 Jun 2023 22:55:47 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 14 Jun 2023 22:55:47 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 14 Jun 2023 22:55:47 GMT
USER api-firewall
# Wed, 14 Jun 2023 22:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:55:48 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7088b7a9c2f02d26362553ecf88235bb03c90adb851cbd1abaf221335f7caf`  
		Last Modified: Wed, 14 Jun 2023 22:56:05 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74abfa69820d287e8e6a6ed724ac3c6b65f35741c610af350bad754533d3b50c`  
		Last Modified: Wed, 14 Jun 2023 22:56:06 GMT  
		Size: 5.2 MB (5228486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02b3eb7e151fac5d7c1fd8e70ae1a10b09476b1083751b9160714f25b3b8a94`  
		Last Modified: Wed, 14 Jun 2023 22:56:05 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.11` - linux; 386

```console
$ docker pull api-firewall@sha256:d3138561a5682a0675f13cba44a2be3d97cc6ea6a1e87007d4605ab091fa3f99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8878913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812df08e1f395951a453a224323c1089001b523fcfbb8cc6b22677822633e214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:30 GMT
ADD file:61bc44c9685b610d18bddd05d2ea1e57b4313f5f433a0a0b7e5269ec24f108b0 in / 
# Wed, 29 Mar 2023 17:38:30 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:17:56 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 29 Mar 2023 19:17:56 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 19:17:57 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 29 Mar 2023 19:17:57 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Wed, 29 Mar 2023 19:17:59 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 29 Mar 2023 19:17:59 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 29 Mar 2023 19:17:59 GMT
USER api-firewall
# Wed, 29 Mar 2023 19:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:18:00 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:b2b0f0faedf1b87a3c77cf90d027fb7a25aa67f35400244a4655ad5842a757e4`  
		Last Modified: Wed, 29 Mar 2023 17:39:00 GMT  
		Size: 3.4 MB (3412260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcc6ef49f75790d9a4fb6684238589d6fc72825a48cda0434f5722341357027`  
		Last Modified: Wed, 29 Mar 2023 19:18:17 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d704a7e1675f0bb9d3a68d49137a870d0d38a59f79bca9c450fe94cb377e483`  
		Last Modified: Wed, 29 Mar 2023 19:18:18 GMT  
		Size: 5.5 MB (5465099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7b31015c4f49667a96a8a7b5935e6e23a8b5d85d6849de025e398520732753`  
		Last Modified: Wed, 29 Mar 2023 19:18:17 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:0.6.9`

```console
$ docker pull api-firewall@sha256:d4a65be62317ff3bab7bc89487d18508055c9008c5184bac6f8e6989a545d1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.9` - linux; amd64

```console
$ docker pull api-firewall@sha256:70db33d53be4c5b3833ba6db6fa76ee3b26980b3171799d41ed6eaf7fe075d86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7997295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7915fa0daa7aea7328b02bd63463b7f0775cc4edf50db7bcf6758044fa96198`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:33:33 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 29 Mar 2023 19:33:33 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 19:33:34 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 29 Mar 2023 19:33:34 GMT
ENV APIFIREWALL_VERSION=v0.6.9
# Wed, 29 Mar 2023 19:33:36 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='12f0b039e84f71298ebc17777910cdd7618e76f65f3356d2e890c3b45f01ef19';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='4f31329e9f2391460450e83096b0b17afa08649e17870f8667f1187aacc5ae00';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='acdce9e1e3d5ecc46be56d3a6b5a70a84de44c53d342a02b8e5f848624ae4b16';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 29 Mar 2023 19:33:36 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 29 Mar 2023 19:33:36 GMT
USER api-firewall
# Wed, 29 Mar 2023 19:33:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:33:36 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e9a374bd90c6a98953d63d14c253a3443e23b999c5c2d4c121b6bdf4b08882`  
		Last Modified: Wed, 29 Mar 2023 19:33:58 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68008ceb5c60b433cbfff07d4d1939c836bc50f261715eb4690a1839062b4f42`  
		Last Modified: Wed, 29 Mar 2023 19:33:59 GMT  
		Size: 5.2 MB (5187939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd0ae2237971ca008b486ae7674cdd05309d5ff217c91693bb8c03538013c52`  
		Last Modified: Wed, 29 Mar 2023 19:33:59 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.9` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:884261a0409903fc86a8795720265c1b37f6386e561f8d99cc815e103ec5f1cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5676e08f6bc8ead8cecec17653000257cb54c7834255ece0ba179886ccb1d264`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:55:53 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 14 Jun 2023 22:55:53 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 22:55:54 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 14 Jun 2023 22:55:54 GMT
ENV APIFIREWALL_VERSION=v0.6.9
# Wed, 14 Jun 2023 22:55:57 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='12f0b039e84f71298ebc17777910cdd7618e76f65f3356d2e890c3b45f01ef19';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='4f31329e9f2391460450e83096b0b17afa08649e17870f8667f1187aacc5ae00';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='acdce9e1e3d5ecc46be56d3a6b5a70a84de44c53d342a02b8e5f848624ae4b16';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 14 Jun 2023 22:55:57 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 14 Jun 2023 22:55:57 GMT
USER api-firewall
# Wed, 14 Jun 2023 22:55:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:55:57 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cce8b99e5b37ed8f7bf314f9778a1ec62e2dde13bf53991a11ca1a155abad4`  
		Last Modified: Wed, 14 Jun 2023 22:56:20 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdffd72a6322a073b6b4b83fa8f829e39e2c60165b970cc55bfcb24094c2508`  
		Last Modified: Wed, 14 Jun 2023 22:56:20 GMT  
		Size: 4.8 MB (4781081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1699e475ab8311b9b829f625d8f22be9072a863606454aa2a8ff47509e51b71`  
		Last Modified: Wed, 14 Jun 2023 22:56:20 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.9` - linux; 386

```console
$ docker pull api-firewall@sha256:7bdfef2a468baedfe441033adf86b7cbad10b2ed0ce3198d85a8365d1003f83c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7856393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03a047cf8fda5dfda939f87e7265bde1c410d6515b89ba5e9f39f4ba9da627f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:33 GMT
ADD file:c9d37b1a7eee54b1a8c1ebde284829510ec289f7b7db2c16059b26f01b416fe0 in / 
# Wed, 29 Mar 2023 17:38:33 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:18:06 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 29 Mar 2023 19:18:06 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 19:18:06 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 29 Mar 2023 19:18:07 GMT
ENV APIFIREWALL_VERSION=v0.6.9
# Wed, 29 Mar 2023 19:18:09 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='12f0b039e84f71298ebc17777910cdd7618e76f65f3356d2e890c3b45f01ef19';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='4f31329e9f2391460450e83096b0b17afa08649e17870f8667f1187aacc5ae00';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='acdce9e1e3d5ecc46be56d3a6b5a70a84de44c53d342a02b8e5f848624ae4b16';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 29 Mar 2023 19:18:09 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 29 Mar 2023 19:18:09 GMT
USER api-firewall
# Wed, 29 Mar 2023 19:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:18:09 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:dea45757091f21722aec41fb20845e57a04f4bb8c199531491f1dc070480a574`  
		Last Modified: Wed, 29 Mar 2023 17:39:11 GMT  
		Size: 2.8 MB (2810814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419d16b206ea679765410b67b0ae990a31aee75c2dcd105b0132451a729f656a`  
		Last Modified: Wed, 29 Mar 2023 19:18:33 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946990d641967461eb4b8c95b528cf27910570b7379ea89b6393fcec52a44925`  
		Last Modified: Wed, 29 Mar 2023 19:18:34 GMT  
		Size: 5.0 MB (5044020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b316834a1af77ac998200f82b7010182bbe1712bc1d83d9c45ecf57580069c6f`  
		Last Modified: Wed, 29 Mar 2023 19:18:33 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:afc1ba449c30f90576061ebd3b0972c0c2f8ed59c766caf503bb2b02941bf9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:034b3292ce4aa149a6cff097e2b9fc58bba2ce1e00c6b4645cabb030c5b52aab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8982910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e38530f647b5d3ba25cba838b86300f8700f4a87f0c72c02945dc7bd5a8a0e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:33:23 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 29 Mar 2023 19:33:24 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 19:33:24 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 29 Mar 2023 19:33:24 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Wed, 29 Mar 2023 19:33:27 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 29 Mar 2023 19:33:27 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 29 Mar 2023 19:33:27 GMT
USER api-firewall
# Wed, 29 Mar 2023 19:33:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:33:27 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085aa53bc6dba091a419b6c3e1f745a1748914575dca4114e1003fac0fdb0938`  
		Last Modified: Wed, 29 Mar 2023 19:33:44 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af23408db57eb594b9ee9b7d3fa611016f3e0d53e2e8e5ac78ef7381b501e1d2`  
		Last Modified: Wed, 29 Mar 2023 19:33:45 GMT  
		Size: 5.6 MB (5606792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67872c68496533df2c11048e1059194bc373470daa17890ef72b6846018a7270`  
		Last Modified: Wed, 29 Mar 2023 19:33:44 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:3233013d824d2b14368c4799de0622db298d100232771b6eb2279ae2c24973c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8491181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf7552534c17bfb79c344e9e84d2d6e7ed4eab5df285f6f4181068f0c8f93b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:55:45 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 14 Jun 2023 22:55:45 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 22:55:45 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 14 Jun 2023 22:55:45 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Wed, 14 Jun 2023 22:55:47 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 14 Jun 2023 22:55:47 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 14 Jun 2023 22:55:47 GMT
USER api-firewall
# Wed, 14 Jun 2023 22:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:55:48 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7088b7a9c2f02d26362553ecf88235bb03c90adb851cbd1abaf221335f7caf`  
		Last Modified: Wed, 14 Jun 2023 22:56:05 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74abfa69820d287e8e6a6ed724ac3c6b65f35741c610af350bad754533d3b50c`  
		Last Modified: Wed, 14 Jun 2023 22:56:06 GMT  
		Size: 5.2 MB (5228486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02b3eb7e151fac5d7c1fd8e70ae1a10b09476b1083751b9160714f25b3b8a94`  
		Last Modified: Wed, 14 Jun 2023 22:56:05 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:d3138561a5682a0675f13cba44a2be3d97cc6ea6a1e87007d4605ab091fa3f99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8878913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812df08e1f395951a453a224323c1089001b523fcfbb8cc6b22677822633e214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:30 GMT
ADD file:61bc44c9685b610d18bddd05d2ea1e57b4313f5f433a0a0b7e5269ec24f108b0 in / 
# Wed, 29 Mar 2023 17:38:30 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:17:56 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 29 Mar 2023 19:17:56 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 19:17:57 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 29 Mar 2023 19:17:57 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Wed, 29 Mar 2023 19:17:59 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 29 Mar 2023 19:17:59 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 29 Mar 2023 19:17:59 GMT
USER api-firewall
# Wed, 29 Mar 2023 19:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:18:00 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:b2b0f0faedf1b87a3c77cf90d027fb7a25aa67f35400244a4655ad5842a757e4`  
		Last Modified: Wed, 29 Mar 2023 17:39:00 GMT  
		Size: 3.4 MB (3412260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcc6ef49f75790d9a4fb6684238589d6fc72825a48cda0434f5722341357027`  
		Last Modified: Wed, 29 Mar 2023 19:18:17 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d704a7e1675f0bb9d3a68d49137a870d0d38a59f79bca9c450fe94cb377e483`  
		Last Modified: Wed, 29 Mar 2023 19:18:18 GMT  
		Size: 5.5 MB (5465099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7b31015c4f49667a96a8a7b5935e6e23a8b5d85d6849de025e398520732753`  
		Last Modified: Wed, 29 Mar 2023 19:18:17 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
