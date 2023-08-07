<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.6.10`](#api-firewall0610)
-	[`api-firewall:0.6.11`](#api-firewall0611)
-	[`api-firewall:0.6.9`](#api-firewall069)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.6.10`

```console
$ docker pull api-firewall@sha256:84334426cbc95dcaa7b904c04fa6394d0bcb43edaf6585ae1f0298be9075b5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.10` - linux; amd64

```console
$ docker pull api-firewall@sha256:cf5ebd4a47fff90a19e52b8b53443bd2263170d1da3baea5ac7fece449bae4c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da844bb9f06b3f3b432c3f9d140870a28cde329a2c459c4750350f9f8d44546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:10:17 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 07 Aug 2023 20:10:17 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:10:17 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 07 Aug 2023 20:10:22 GMT
ENV APIFIREWALL_VERSION=v0.6.10
# Mon, 07 Aug 2023 20:10:24 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='774d29f694142984e11e31443398a973a882d19c491e06390de13f0ceabd04a4';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='6ef69fbafb2503c7b01681d39138ea1abe99da910912fde33b1c317a819d2804';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='a9ccd2757bb4703b70aeea44b8aa992ce0dc1025d36accf311a023d87b1b6f57';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 07 Aug 2023 20:10:24 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 07 Aug 2023 20:10:24 GMT
USER api-firewall
# Mon, 07 Aug 2023 20:10:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:10:24 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc01ebde4290a0704589287422aa0dcbb6ce1b03aea189dc71b8723d1fc5000a`  
		Last Modified: Mon, 07 Aug 2023 20:10:39 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa550f4a84487f31933505eb8398bbbdac8b5e5e4250c52392b8999a9193125`  
		Last Modified: Mon, 07 Aug 2023 20:10:50 GMT  
		Size: 5.5 MB (5542415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c33bfda2356758a59a3ba3fae6add6e1f1396f46ea0839e9911e595805e545`  
		Last Modified: Mon, 07 Aug 2023 20:10:49 GMT  
		Size: 354.0 B  
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
$ docker pull api-firewall@sha256:745ce7447d527b8032c6614e82fdff4cd9635f4a0ddf347d544fee90b909a1e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8818650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c1f024ce9a1c09e4edd7ba3943c159f429f487c2a65d45b0a28cf1d1147cbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 19:54:49 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 07 Aug 2023 19:54:49 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 19:54:50 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 07 Aug 2023 19:54:56 GMT
ENV APIFIREWALL_VERSION=v0.6.10
# Mon, 07 Aug 2023 19:54:58 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='774d29f694142984e11e31443398a973a882d19c491e06390de13f0ceabd04a4';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='6ef69fbafb2503c7b01681d39138ea1abe99da910912fde33b1c317a819d2804';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='a9ccd2757bb4703b70aeea44b8aa992ce0dc1025d36accf311a023d87b1b6f57';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 07 Aug 2023 19:54:58 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 07 Aug 2023 19:54:58 GMT
USER api-firewall
# Mon, 07 Aug 2023 19:54:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 19:54:58 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8369a31228112c0157359acaea131105f3e06694cde24674971e644e3142b085`  
		Last Modified: Mon, 07 Aug 2023 19:55:16 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3238b5538fc02d9f42a45988f190548ba32681578544d61bcd03d2f39b24ec`  
		Last Modified: Mon, 07 Aug 2023 19:55:28 GMT  
		Size: 5.4 MB (5403312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3a2c319e632277bdc8eecbc7df872c9c009df2668e8b30552a4a8999346ff7`  
		Last Modified: Mon, 07 Aug 2023 19:55:27 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:0.6.11`

```console
$ docker pull api-firewall@sha256:6966b1eefb9d5133611fff4dffbea69d0937d70747df5c71f80a7ca4f432af24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.11` - linux; amd64

```console
$ docker pull api-firewall@sha256:d87dfb27357591cf0c001138a692b8cc8a6e286fb596319f00dc11f1c6740016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8987306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975bc7e72dc9951b0ceef3139162c004b2274a595b2a598508576a10682d0514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:10:17 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 07 Aug 2023 20:10:17 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:10:17 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 07 Aug 2023 20:10:17 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Mon, 07 Aug 2023 20:10:19 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 07 Aug 2023 20:10:19 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 07 Aug 2023 20:10:19 GMT
USER api-firewall
# Mon, 07 Aug 2023 20:10:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:10:19 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc01ebde4290a0704589287422aa0dcbb6ce1b03aea189dc71b8723d1fc5000a`  
		Last Modified: Mon, 07 Aug 2023 20:10:39 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edafb5a7beb02c6363bbc5f59527765c1a80bc3b36ede856892088644c447221`  
		Last Modified: Mon, 07 Aug 2023 20:10:40 GMT  
		Size: 5.6 MB (5607142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02daa2b84e9dc5d35ef9e86d72a7a107f9198fefeb651e4483195a8a2b37888`  
		Last Modified: Mon, 07 Aug 2023 20:10:39 GMT  
		Size: 352.0 B  
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
$ docker pull api-firewall@sha256:41999ca97a1cf50a4ae5085f453cc870b01dbbcfb28083de7c0b6a2a27ff07d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8881962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8eaad9244719be3b580fa6775824e7e51b588e9025be5cf8d435e3b12502f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 19:54:49 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 07 Aug 2023 19:54:49 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 19:54:50 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 07 Aug 2023 19:54:50 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Mon, 07 Aug 2023 19:54:53 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 07 Aug 2023 19:54:53 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 07 Aug 2023 19:54:53 GMT
USER api-firewall
# Mon, 07 Aug 2023 19:54:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 19:54:54 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8369a31228112c0157359acaea131105f3e06694cde24674971e644e3142b085`  
		Last Modified: Mon, 07 Aug 2023 19:55:16 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3d40320774ca8c85f2545368fe810995b10c8ea30b4f0c90d7bf7db99344bd`  
		Last Modified: Mon, 07 Aug 2023 19:55:18 GMT  
		Size: 5.5 MB (5466628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7850f2ea76bc93e0f7a99eed944ec87bd1ce2579eb1d49d1d812508bb11a298a`  
		Last Modified: Mon, 07 Aug 2023 19:55:16 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:0.6.9`

```console
$ docker pull api-firewall@sha256:1d47b88f21d96190c5e2aed686b78fde53e33b0b225ab3292fc2899acaa46512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.9` - linux; amd64

```console
$ docker pull api-firewall@sha256:7556108879ff742574cfada685ce57a191ae2f67e0020927cd86742b095be4d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7997188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee52471362247b12287523666a7fba2dc6a84fba43bb136ab12bd0d7aded9bd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:10:27 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 07 Aug 2023 20:10:27 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:10:27 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 07 Aug 2023 20:10:27 GMT
ENV APIFIREWALL_VERSION=v0.6.9
# Mon, 07 Aug 2023 20:10:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='12f0b039e84f71298ebc17777910cdd7618e76f65f3356d2e890c3b45f01ef19';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='4f31329e9f2391460450e83096b0b17afa08649e17870f8667f1187aacc5ae00';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='acdce9e1e3d5ecc46be56d3a6b5a70a84de44c53d342a02b8e5f848624ae4b16';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 07 Aug 2023 20:10:29 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 07 Aug 2023 20:10:29 GMT
USER api-firewall
# Mon, 07 Aug 2023 20:10:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:10:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4566d40afe21dfaf768af612aa737e4b400a1d66fe6480260d6f45f58ab7c52`  
		Last Modified: Mon, 07 Aug 2023 20:10:56 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5c98ae79cb0c8c379892043a38773dab5afef2e1fabce981f96d16e017f888`  
		Last Modified: Mon, 07 Aug 2023 20:10:57 GMT  
		Size: 5.2 MB (5187950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7297daaf2fab7f935f6881e7fbe73f522f221bf8b337a47b442b0b80320f9b80`  
		Last Modified: Mon, 07 Aug 2023 20:10:56 GMT  
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
$ docker pull api-firewall@sha256:296b5d487fbb160a50f916f9a16cf8c0f4316cc24f63ebda92a740d919513f5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7856134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ef54ced0e7268a78a846c319d77fd71c8e45425320fb796a07136cf01aa562`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:34 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 07 Aug 2023 19:38:34 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 19:55:01 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 07 Aug 2023 19:55:01 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 19:55:01 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 07 Aug 2023 19:55:01 GMT
ENV APIFIREWALL_VERSION=v0.6.9
# Mon, 07 Aug 2023 19:55:05 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='12f0b039e84f71298ebc17777910cdd7618e76f65f3356d2e890c3b45f01ef19';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='4f31329e9f2391460450e83096b0b17afa08649e17870f8667f1187aacc5ae00';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='acdce9e1e3d5ecc46be56d3a6b5a70a84de44c53d342a02b8e5f848624ae4b16';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 07 Aug 2023 19:55:05 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 07 Aug 2023 19:55:05 GMT
USER api-firewall
# Mon, 07 Aug 2023 19:55:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 19:55:05 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cd6f2048e3e1a54b23d8d546543ef5a2df0f269d715f944d16db7518c2b429`  
		Last Modified: Mon, 07 Aug 2023 19:55:35 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d91126e4f2a94282d58aaa19d88cea5a94dfa32ad2f18bdb1392e5a99220a9`  
		Last Modified: Mon, 07 Aug 2023 19:55:36 GMT  
		Size: 5.0 MB (5044020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a9fa1b3cdcda6784cf0b9980172f20ddbeec1c00881153441ffb67b8331e35`  
		Last Modified: Mon, 07 Aug 2023 19:55:35 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:6966b1eefb9d5133611fff4dffbea69d0937d70747df5c71f80a7ca4f432af24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:d87dfb27357591cf0c001138a692b8cc8a6e286fb596319f00dc11f1c6740016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8987306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975bc7e72dc9951b0ceef3139162c004b2274a595b2a598508576a10682d0514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:10:17 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 07 Aug 2023 20:10:17 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:10:17 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 07 Aug 2023 20:10:17 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Mon, 07 Aug 2023 20:10:19 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 07 Aug 2023 20:10:19 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 07 Aug 2023 20:10:19 GMT
USER api-firewall
# Mon, 07 Aug 2023 20:10:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:10:19 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc01ebde4290a0704589287422aa0dcbb6ce1b03aea189dc71b8723d1fc5000a`  
		Last Modified: Mon, 07 Aug 2023 20:10:39 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edafb5a7beb02c6363bbc5f59527765c1a80bc3b36ede856892088644c447221`  
		Last Modified: Mon, 07 Aug 2023 20:10:40 GMT  
		Size: 5.6 MB (5607142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02daa2b84e9dc5d35ef9e86d72a7a107f9198fefeb651e4483195a8a2b37888`  
		Last Modified: Mon, 07 Aug 2023 20:10:39 GMT  
		Size: 352.0 B  
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
$ docker pull api-firewall@sha256:41999ca97a1cf50a4ae5085f453cc870b01dbbcfb28083de7c0b6a2a27ff07d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8881962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8eaad9244719be3b580fa6775824e7e51b588e9025be5cf8d435e3b12502f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 19:54:49 GMT
ENV APIFW_PATH=/opt/api-firewall
# Mon, 07 Aug 2023 19:54:49 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 19:54:50 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Mon, 07 Aug 2023 19:54:50 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Mon, 07 Aug 2023 19:54:53 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Mon, 07 Aug 2023 19:54:53 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Mon, 07 Aug 2023 19:54:53 GMT
USER api-firewall
# Mon, 07 Aug 2023 19:54:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 19:54:54 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8369a31228112c0157359acaea131105f3e06694cde24674971e644e3142b085`  
		Last Modified: Mon, 07 Aug 2023 19:55:16 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3d40320774ca8c85f2545368fe810995b10c8ea30b4f0c90d7bf7db99344bd`  
		Last Modified: Mon, 07 Aug 2023 19:55:18 GMT  
		Size: 5.5 MB (5466628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7850f2ea76bc93e0f7a99eed944ec87bd1ce2579eb1d49d1d812508bb11a298a`  
		Last Modified: Mon, 07 Aug 2023 19:55:16 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
