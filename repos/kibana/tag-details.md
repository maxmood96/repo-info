<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.23`](#kibana6823)
-	[`kibana:7.17.0`](#kibana7170)
-	[`kibana:8.0.0`](#kibana800)

## `kibana:6.8.23`

```console
$ docker pull kibana@sha256:dd123d133fa7e995f83eef23df6aad30c589711e6171fee8db63097a7706eae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kibana:6.8.23` - linux; amd64

```console
$ docker pull kibana@sha256:adb468810c34ccc141f01ea79135d5a2f48d09890ecd08ce59ec94444f0a09f1
```

-	Docker Version: 20.10.10
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325750637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e174261beaec7ef8b8fc7e3df6b62b87e442f3451d408e7fe4525b151a061ebd`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Jan 2022 22:40:29 GMT
EXPOSE 5601
# Thu, 06 Jan 2022 22:41:30 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Thu, 06 Jan 2022 22:42:25 GMT
COPY --chown=1000:0dir:91d1ac171c4ceb98ce1764191b4bde36072fa18167199a2214eb559670a34b06 in /usr/share/kibana 
# Thu, 06 Jan 2022 22:42:28 GMT
WORKDIR /usr/share/kibana
# Thu, 06 Jan 2022 22:42:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Thu, 06 Jan 2022 22:42:30 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 06 Jan 2022 22:42:30 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 22:42:31 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Thu, 06 Jan 2022 22:42:31 GMT
COPY --chown=1000:0file:7d472d1939e23e2f10e7c5fd1e9166eefd646214aa0d8a1c09d92af71c9cbd87 in /usr/local/bin/ 
# Thu, 06 Jan 2022 22:42:34 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Thu, 06 Jan 2022 22:42:39 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Thu, 06 Jan 2022 22:42:39 GMT
USER kibana
# Thu, 06 Jan 2022 22:42:40 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.23 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Thu, 06 Jan 2022 22:42:41 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842e4249e10492c4ab35d3e76f93cad922781f7d61752e1b4b3ca25636b5c56f`  
		Last Modified: Thu, 13 Jan 2022 16:11:43 GMT  
		Size: 61.0 MB (61010271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f4609300d658bf52b006741f5590abdf93d8d575e0ddf04ce5be28e82b50a4`  
		Last Modified: Thu, 13 Jan 2022 16:11:58 GMT  
		Size: 188.6 MB (188638449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784cf3007996898653e12b85f6cf71597349b95377a60e1c57d40aaf682ddc3e`  
		Last Modified: Thu, 13 Jan 2022 16:11:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e291dafdd6a7112a1b18f88f42cbef2225094f58f18d2f364d0d34006b69e1`  
		Last Modified: Thu, 13 Jan 2022 16:11:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c90f666fc9fbd62181b8b51f391386e0a1a137451605b6f0a105171abe51380`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8abc3a9f73c2948571140a610a8c9f79b87c33bcbfdf320cd0f6e5d9fbe944`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73634fb3f49af52529a1b025a3cebf50531fdbcbdb3876b7b00908dfe9dc0a85`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.17.0`

```console
$ docker pull kibana@sha256:a98b0797fd5357ba8a64c32df0e2e24dc7ad2df3320891b090a1f713124f1c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:7.17.0` - linux; amd64

```console
$ docker pull kibana@sha256:887457756836a54c7139c4ddf2bf84d6f5cf3a987e21c6b4cf29468049180f8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342818229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9fdad811157e0b1658c36fef97a4bd37c696aa79392dd6b9196d7061eeb81d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 28 Jan 2022 09:36:37 GMT
EXPOSE 5601
# Fri, 28 Jan 2022 09:36:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code)
# Fri, 28 Jan 2022 09:36:57 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini
# Fri, 28 Jan 2022 09:36:57 GMT
RUN mkdir /usr/share/fonts/local
# Fri, 28 Jan 2022 09:36:58 GMT
RUN curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc
# Fri, 28 Jan 2022 09:36:59 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c -
# Fri, 28 Jan 2022 09:37:00 GMT
RUN fc-cache -v
# Fri, 28 Jan 2022 09:37:29 GMT
COPY --chown=1000:0dir:308f5be207d03a295377e2a50478ae7cc36563e2c872d130459d34b568b67619 in /usr/share/kibana 
# Fri, 28 Jan 2022 09:37:40 GMT
WORKDIR /usr/share/kibana
# Fri, 28 Jan 2022 09:37:40 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Fri, 28 Jan 2022 09:37:40 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 28 Jan 2022 09:37:40 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jan 2022 09:37:41 GMT
COPY --chown=1000:0file:6db5413736a28ead04731f52a5ef1acaa8f3ca1c1d2eaf6bb2b80d8f232794a2 in /usr/share/kibana/config/kibana.yml 
# Fri, 28 Jan 2022 09:37:41 GMT
COPY file:4b05cc4ee8dc464b192dc25102b9385329fd96ca9e48428d3b36b7d2a9e4be58 in /usr/local/bin/ 
# Fri, 28 Jan 2022 09:37:42 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Fri, 28 Jan 2022 09:37:44 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Fri, 28 Jan 2022 09:37:44 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana
# Fri, 28 Jan 2022 09:37:45 GMT
LABEL org.label-schema.build-date=2022-01-28T08:41:40.944Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=60a9838d21b6420bbdb5a4d07099111b74c68ceb org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.0 org.opencontainers.image.created=2022-01-28T08:41:40.944Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=60a9838d21b6420bbdb5a4d07099111b74c68ceb org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.0
# Fri, 28 Jan 2022 09:37:45 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 28 Jan 2022 09:37:45 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 28 Jan 2022 09:37:45 GMT
USER kibana
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94aca20bb05bbd05582984bc49d0b191547817e651e837fde85e0b7afcab2670`  
		Last Modified: Tue, 01 Feb 2022 20:12:22 GMT  
		Size: 10.9 MB (10928887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ae9e597e8604e219448a947b8400e34bee5a61a06996dfcdb9ab86a89f2185`  
		Last Modified: Tue, 01 Feb 2022 20:12:19 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29743d928b1edf0ea08e4cf5e5031167639c8e8ada9d6778bdf3a31a806defc`  
		Last Modified: Tue, 01 Feb 2022 20:12:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23891b890413c440ffd0c6c4c15c12b7e1c57fabbdc949765520705cd1f9e9e7`  
		Last Modified: Tue, 01 Feb 2022 20:12:18 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf7af96af27d8c271084905c75846f26eecfbaf971f25a588644eda37a92d13`  
		Last Modified: Tue, 01 Feb 2022 20:12:15 GMT  
		Size: 5.3 KB (5277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014dfb291cad1548dc1851df3ecf9fcb9c795e24e8694f10df87e9af22f5d473`  
		Last Modified: Tue, 01 Feb 2022 20:13:21 GMT  
		Size: 286.7 MB (286650832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf3742fc3900f3b2db724f09a8efafd2278ea33d7a56567f2d498e56c5aabdf`  
		Last Modified: Tue, 01 Feb 2022 20:12:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0e9c8dbcb73f9c70d15e31ad43eaaadba18c2eca530cdf90e1fb9d5782de4a`  
		Last Modified: Tue, 01 Feb 2022 20:12:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dab17aa538564e2f4cd5eb8712b04dfff198a0b66b157c639de6e2bdf15f2d0`  
		Last Modified: Tue, 01 Feb 2022 20:12:12 GMT  
		Size: 4.5 KB (4477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807090e8d21fc3e3e0f6a75ff59ffa866da06fde5348a883f5ff4231950fd3c7`  
		Last Modified: Tue, 01 Feb 2022 20:12:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d0ac3cb26eeee9bfa407ce251acd9d8410a09dbe2e15260033afb11a38ebb9`  
		Last Modified: Tue, 01 Feb 2022 20:12:12 GMT  
		Size: 189.4 KB (189379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92e0cf24d40ee7ed41bc7beb9d88b0317e773e48e6388b773e68af18bfd245`  
		Last Modified: Tue, 01 Feb 2022 20:12:12 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:7.17.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:0b6e187ac87407c7458892f3e220a41c889ce426ca5e215cf97d3132fd96d504
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.9 MB (355913752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24d96e394a045991673bc27f115b90fb8d6da965ff53bb22b29e01036b8ebb9`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 28 Jan 2022 10:55:09 GMT
EXPOSE 5601
# Fri, 28 Jan 2022 10:55:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code)
# Fri, 28 Jan 2022 10:55:29 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini
# Fri, 28 Jan 2022 10:55:30 GMT
RUN mkdir /usr/share/fonts/local
# Fri, 28 Jan 2022 10:55:31 GMT
RUN curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc
# Fri, 28 Jan 2022 10:55:32 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c -
# Fri, 28 Jan 2022 10:55:33 GMT
RUN fc-cache -v
# Fri, 28 Jan 2022 10:55:58 GMT
COPY --chown=1000:0dir:9865d82ec0aa9c4ca43aed440d96a183aa1c9d30527b51ef5c47bcfa2a06e63c in /usr/share/kibana 
# Fri, 28 Jan 2022 10:56:02 GMT
WORKDIR /usr/share/kibana
# Fri, 28 Jan 2022 10:56:03 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Fri, 28 Jan 2022 10:56:03 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 28 Jan 2022 10:56:03 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jan 2022 10:56:03 GMT
COPY --chown=1000:0file:6db5413736a28ead04731f52a5ef1acaa8f3ca1c1d2eaf6bb2b80d8f232794a2 in /usr/share/kibana/config/kibana.yml 
# Fri, 28 Jan 2022 10:56:03 GMT
COPY file:4b05cc4ee8dc464b192dc25102b9385329fd96ca9e48428d3b36b7d2a9e4be58 in /usr/local/bin/ 
# Fri, 28 Jan 2022 10:56:04 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Fri, 28 Jan 2022 10:56:06 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Fri, 28 Jan 2022 10:56:06 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana
# Fri, 28 Jan 2022 10:56:06 GMT
LABEL org.label-schema.build-date=2022-01-28T10:51:45.485Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=60a9838d21b6420bbdb5a4d07099111b74c68ceb org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.0 org.opencontainers.image.created=2022-01-28T10:51:45.485Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=60a9838d21b6420bbdb5a4d07099111b74c68ceb org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.0
# Fri, 28 Jan 2022 10:56:06 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 28 Jan 2022 10:56:07 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 28 Jan 2022 10:56:07 GMT
USER kibana
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b382744b5a277e22af1cbf77c70f70bfb7af8b9b9193801bcf8def6114feb4c`  
		Last Modified: Fri, 04 Feb 2022 03:17:24 GMT  
		Size: 10.8 MB (10795157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadebb4ead515dd44a728ec42efcf07f2a2f8a82e2da7b5c63633134f623793f`  
		Last Modified: Fri, 04 Feb 2022 03:17:22 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be8b1ce907b7d9e50650cd5633eee694bfd1cdaf66f307c76a97c97f1c6d081`  
		Last Modified: Fri, 04 Feb 2022 03:17:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499903d9447a75df698e1968de6907f9f58b3fc0cfe2ab73dd0561eed98cac9d`  
		Last Modified: Fri, 04 Feb 2022 03:17:22 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82956d530b6eb5f479fc079baebdf313cda8a5b73a61c1befb24533565b59af`  
		Last Modified: Fri, 04 Feb 2022 03:17:19 GMT  
		Size: 5.3 KB (5281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0b420d9c2143aecdb9603f11617320835d52898f750576b4172bb86f0e1f3d`  
		Last Modified: Fri, 04 Feb 2022 03:18:00 GMT  
		Size: 301.3 MB (301281863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd882e1a37dc37c5e086ae0f9939949bab1bd6fd242bacbb68e267186e16996`  
		Last Modified: Fri, 04 Feb 2022 03:17:19 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10488ee81e3c9fa3df8cb4e6418904a1996573ca25f5ea1b914da99c13652be2`  
		Last Modified: Fri, 04 Feb 2022 03:17:16 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0327ee552e5fec27ac3a5841db792b5181dc73888a3a5d88d82394a74ccb9f`  
		Last Modified: Fri, 04 Feb 2022 03:17:16 GMT  
		Size: 4.5 KB (4482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e423dea7fcda2bab60ebe38f0026160ccfe20078f25b9e07a0688b0c0c250`  
		Last Modified: Fri, 04 Feb 2022 03:17:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845138837344a09fc91992cd76881bbbaf4c43f9c578503d66f5e78e819714e3`  
		Last Modified: Fri, 04 Feb 2022 03:17:17 GMT  
		Size: 183.4 KB (183368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993742d7d0c1f24dd2afbde52a9fb3207d2ecad5f2e33ed7b16449e779106574`  
		Last Modified: Fri, 04 Feb 2022 03:17:16 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:8.0.0`

```console
$ docker pull kibana@sha256:498cfc53922d8299baa88e5a0f306a7fbf7f50bd85ac79b4eb43cbfd2ed89ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:8.0.0` - linux; amd64

```console
$ docker pull kibana@sha256:bcfc4ce2c999bd3901c9e509d894892e226273142decf6c875889b2d2dbfe6f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337881429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b752a783190b8b4cfb543a1af83c86944b62662558c9e2f16611989e1314a73c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Thu, 03 Feb 2022 23:14:35 GMT
EXPOSE 5601
# Thu, 03 Feb 2022 23:14:52 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code)
# Thu, 03 Feb 2022 23:14:54 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini
# Thu, 03 Feb 2022 23:14:54 GMT
RUN mkdir /usr/share/fonts/local
# Thu, 03 Feb 2022 23:14:55 GMT
RUN curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc
# Thu, 03 Feb 2022 23:14:56 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c -
# Thu, 03 Feb 2022 23:14:57 GMT
RUN fc-cache -v
# Thu, 03 Feb 2022 23:15:28 GMT
COPY --chown=1000:0dir:53dd7743a31b255e7ba6619b6adaec8a032045082af1c214d28743431a9cf074 in /usr/share/kibana 
# Thu, 03 Feb 2022 23:15:33 GMT
WORKDIR /usr/share/kibana
# Thu, 03 Feb 2022 23:15:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Thu, 03 Feb 2022 23:15:34 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 03 Feb 2022 23:15:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:15:34 GMT
COPY --chown=1000:0file:6db5413736a28ead04731f52a5ef1acaa8f3ca1c1d2eaf6bb2b80d8f232794a2 in /usr/share/kibana/config/kibana.yml 
# Thu, 03 Feb 2022 23:15:35 GMT
COPY file:52e8ac9215e9f098c5481c490f121df8283bdefe968591a8fd8e938bb4b6e17c in /usr/local/bin/ 
# Thu, 03 Feb 2022 23:15:36 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Thu, 03 Feb 2022 23:15:37 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Thu, 03 Feb 2022 23:15:38 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana
# Thu, 03 Feb 2022 23:15:38 GMT
LABEL org.label-schema.build-date=2022-02-03T23:06:21.184Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=57ca5e139a33dd2eed927ce98d8231a1f217cd15 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.0.0 org.opencontainers.image.created=2022-02-03T23:06:21.184Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=57ca5e139a33dd2eed927ce98d8231a1f217cd15 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.0.0
# Thu, 03 Feb 2022 23:15:38 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 03 Feb 2022 23:15:38 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 03 Feb 2022 23:15:38 GMT
USER kibana
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cac208572220b09acd89fd334e11523358da2cf3bdce26c4a02a6ed7ae9c9d3`  
		Last Modified: Fri, 11 Feb 2022 00:20:12 GMT  
		Size: 10.5 MB (10513690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2d54237758d8341cbd317c44fab9abcaa6403778b46d1f2366f77560f38185`  
		Last Modified: Fri, 11 Feb 2022 00:20:06 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d88031e34513090ce9080191b849b3ab8db4eb3fdf399c6e30c706ffa00738e`  
		Last Modified: Fri, 11 Feb 2022 00:20:06 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb4e11ae24c0e5a9cc00ad416ea6152f847e10501f64adc8b04e8ccb2ec7aaa`  
		Last Modified: Fri, 11 Feb 2022 00:20:25 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1551c6b40305a6e60d117e4d62d30d3e9c817f3dea5506e96c72576410c64892`  
		Last Modified: Fri, 11 Feb 2022 00:20:00 GMT  
		Size: 5.3 KB (5274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdab9f7cdc3e5d7778f84b53487451b398c14d83fd27f981b0bd312c3c7db29d`  
		Last Modified: Fri, 11 Feb 2022 00:22:41 GMT  
		Size: 282.1 MB (282131825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3ffc2a87e10db6cfeaa45e446148f8a49b0a842531390086d53e29c5cc351b`  
		Last Modified: Fri, 11 Feb 2022 00:20:00 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2140ecc0308d9d4bb9f6059d63fc44124e49cccf857e6c329d8633becc9316a6`  
		Last Modified: Fri, 11 Feb 2022 00:19:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1848eaae82c0e1ebcd05adfbb7bb6aab153fc10269da11913bbd01fe023203d`  
		Last Modified: Fri, 11 Feb 2022 00:19:54 GMT  
		Size: 4.2 KB (4207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd7ae2e4c619dc20276b8bf2789faf907f3c277e6e434dbb203c1e46e017c18`  
		Last Modified: Fri, 11 Feb 2022 00:19:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9995898cfb9edd9b3478f77c58f25c3d40f43581fba5d2145d79aa7aaceb7`  
		Last Modified: Fri, 11 Feb 2022 00:19:55 GMT  
		Size: 189.4 KB (189376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b040f72553edeba6b784898128efdc608ec035499fc701e843412b4ebd92cf46`  
		Last Modified: Fri, 11 Feb 2022 00:19:54 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:8.0.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:b07303d94c51503709c22bf18686759020fb030ec623ba95d24b28a912098a92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350975538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b44188102926339c4ecb5c95dcd68d8cb56be3ca68ab74aaa1a5681278197ff`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Thu, 03 Feb 2022 23:10:58 GMT
EXPOSE 5601
# Thu, 03 Feb 2022 23:11:14 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code)
# Thu, 03 Feb 2022 23:11:16 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini
# Thu, 03 Feb 2022 23:11:16 GMT
RUN mkdir /usr/share/fonts/local
# Thu, 03 Feb 2022 23:11:18 GMT
RUN curl -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc
# Thu, 03 Feb 2022 23:11:19 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c -
# Thu, 03 Feb 2022 23:11:20 GMT
RUN fc-cache -v
# Thu, 03 Feb 2022 23:11:48 GMT
COPY --chown=1000:0dir:b38dae499c4d98bac5870cfe5bfb42086f26753399222bfb903b91e822b10ca4 in /usr/share/kibana 
# Thu, 03 Feb 2022 23:11:50 GMT
WORKDIR /usr/share/kibana
# Thu, 03 Feb 2022 23:11:51 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Thu, 03 Feb 2022 23:11:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 03 Feb 2022 23:11:51 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:11:51 GMT
COPY --chown=1000:0file:6db5413736a28ead04731f52a5ef1acaa8f3ca1c1d2eaf6bb2b80d8f232794a2 in /usr/share/kibana/config/kibana.yml 
# Thu, 03 Feb 2022 23:11:51 GMT
COPY file:52e8ac9215e9f098c5481c490f121df8283bdefe968591a8fd8e938bb4b6e17c in /usr/local/bin/ 
# Thu, 03 Feb 2022 23:11:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Thu, 03 Feb 2022 23:11:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Thu, 03 Feb 2022 23:11:54 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana
# Thu, 03 Feb 2022 23:11:54 GMT
LABEL org.label-schema.build-date=2022-02-03T23:07:20.765Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=57ca5e139a33dd2eed927ce98d8231a1f217cd15 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.0.0 org.opencontainers.image.created=2022-02-03T23:07:20.765Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=57ca5e139a33dd2eed927ce98d8231a1f217cd15 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.0.0
# Thu, 03 Feb 2022 23:11:54 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 03 Feb 2022 23:11:54 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 03 Feb 2022 23:11:54 GMT
USER kibana
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e44ab9baafcfbf63916acfb488c18518543c331d02c246a517f8fa207b84d3f`  
		Last Modified: Fri, 11 Feb 2022 23:55:48 GMT  
		Size: 10.4 MB (10383589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969122bb40456eaa86d5b5c08733b103cec585c7bf6327f1a58a9aa6dc3f2f63`  
		Last Modified: Fri, 11 Feb 2022 23:55:46 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7758b2256ee5d89fab6b0bfa6d1882f11863c91658702e89c96d6128a105c332`  
		Last Modified: Fri, 11 Feb 2022 23:55:44 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7e04db5954fc47d14a1f65f0afc7554d13e901338ebb3a2f97a6c14559e108`  
		Last Modified: Fri, 11 Feb 2022 23:55:46 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ed2d251bb1a52e7ec32d631d2c91faad155e388c753a3cd6ecc6a315bd8a8`  
		Last Modified: Fri, 11 Feb 2022 23:55:44 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae40ac1cc496ee2987c55bcd3db1d42a7e624f5b4243f52840c787abb7d6371`  
		Last Modified: Fri, 11 Feb 2022 23:56:25 GMT  
		Size: 296.8 MB (296756921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf0ad4e69e64c82745e63815266611e49b72990ace08a6b1a3ed5c3210fab75`  
		Last Modified: Fri, 11 Feb 2022 23:55:44 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b6d73c7a03a2010f709aaf926c0487b264fbe804340ed28a61b91d5005344`  
		Last Modified: Fri, 11 Feb 2022 23:55:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e1f2823b5242f9838d03b1400061cf7f05b4297cb4cf879d9f7bae961d191f`  
		Last Modified: Fri, 11 Feb 2022 23:55:41 GMT  
		Size: 4.2 KB (4210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75047b3d18c041042f1e3daf50e158b373706de4097d7335d90691f0f4584921`  
		Last Modified: Fri, 11 Feb 2022 23:55:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce99149f569bab63e22559e10a56364f981fe78fe519ca8b9bfc1d53ccdab39b`  
		Last Modified: Fri, 11 Feb 2022 23:55:42 GMT  
		Size: 183.4 KB (183369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5c15a2e9109698127400c0bad1a1962d1cc93fbb201146cc47099d1a198cb3`  
		Last Modified: Fri, 11 Feb 2022 23:55:41 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
