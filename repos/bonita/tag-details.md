<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2021.1`](#bonita20211)
-	[`bonita:2021.2`](#bonita20212)
-	[`bonita:2021.2-u0`](#bonita20212-u0)
-	[`bonita:7.11`](#bonita711)
-	[`bonita:7.11.4`](#bonita7114)
-	[`bonita:7.12`](#bonita712)
-	[`bonita:7.12.1`](#bonita7121)
-	[`bonita:7.13`](#bonita713)
-	[`bonita:7.13.0`](#bonita7130)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2021.1`

```console
$ docker pull bonita@sha256:d675ad340e9b8fad82a6b49aa58186753f50aa528f4f3876a8e703d7f0db04f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:950607cd74458c8c97131dbbbf3e991228ac0a4b631b85f529299e913ff9a9ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237292009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a67995d4904a843db141d7a8e559f0d2df49fb1e4b5a83fdc2c8748c572499`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:38:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:38:01 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:38:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:38:48 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:38:48 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:39:06 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:39:07 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:39:07 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:39:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:39:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:39:25 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:39:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:39:26 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:39:26 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:39:27 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:39:27 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e26f312b55420283ec88133940bf7f91764464f58f1861612d697d10d903eb`  
		Last Modified: Thu, 03 Mar 2022 20:41:22 GMT  
		Size: 93.6 MB (93580470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6595d65755dfd2db718649f213935c206a04e2443e94d9def82004cec13c8f7`  
		Last Modified: Thu, 03 Mar 2022 20:41:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e1156933eb4b5b0948b99e92616dac6f646a7b59e40c374300e7f2ca2bb7e8`  
		Last Modified: Thu, 03 Mar 2022 20:41:08 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350751d0c7f7b09c79a65f4ec9b3e85f6aaec7d073eb09b491a7403681b16956`  
		Last Modified: Thu, 03 Mar 2022 20:41:06 GMT  
		Size: 577.0 KB (576971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e8553193e7c7dff14b7075c2d1ce330b77813068e11eb2b0a589a167545dda`  
		Last Modified: Thu, 03 Mar 2022 20:41:32 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e010bd86a6d1788aabe769d0aa7ebc66123ea6a1a576bfbd72d9efe570392`  
		Last Modified: Thu, 03 Mar 2022 20:41:32 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d7315e3b64151f7aa7eb9000af282c5763c9d89fc5138b2802738ad528f741`  
		Last Modified: Thu, 03 Mar 2022 20:41:38 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bacaf2b6a20a3cf00f54d2c39ecbda1f23d6a1851f325c94e3470982f471da`  
		Last Modified: Thu, 03 Mar 2022 20:41:32 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:682c04575d0e3964f325488cc0ce7b4e17fd0ffbd7ae07b7f948c1fff21848a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226401706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267e77b75883c0b4cd7601b35b5b94925fedb24299ceb7639abbd2d82be03975`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 19:59:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 19:59:20 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 19:59:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:00:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:00:03 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:00:33 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:00:34 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:00:35 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:00:36 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:00:37 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:00:38 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:00:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:00:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:00:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:43 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:00:44 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:00:46 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:00:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:00:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:00:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:00:55 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:00:57 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:00:57 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:00:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603888e2649b74be803a493ad60570eaf6fa7a0db55350510ca362482d1d046a`  
		Last Modified: Thu, 03 Mar 2022 20:03:22 GMT  
		Size: 85.7 MB (85699004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245a1b8ba7feeb0507a81ce2a5116d45572650fecbe18e02c2be9bd9370d55b5`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a077eeefcedfb7f8b0ead8b47dc2ee5f00ce4d1dd5996efe00956a83d83b4a`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4295b7f5f73ca4ad6fd600da6f0e006b109fcc6d6ee8c2e5883aaca4dc72d33`  
		Last Modified: Thu, 03 Mar 2022 20:03:08 GMT  
		Size: 546.9 KB (546947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dbb8e122d99aa3835c03f0449d5945c7bebba698810aad047ef9a94a44136e`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13fcb4bf6e01237803b44e91d6aa560b248b6332bf98a27a22220a010ceb0`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402eb2ec9cb549b7ebb5945d00cf5802b55e847b5f8cb132ce83c7ad4a5ab592`  
		Last Modified: Thu, 03 Mar 2022 20:03:44 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc7ab7b806dbaea4ad80109ddbe8b3b385c9e3253236066f663b92b4d3d17e7`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:74b4df5d2e53facb3a8215ae2293955564fb71ec0dc3298f314131aaad1aa624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233890360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bebe00266e33a543053f11093cee7698e14058a91a2f7ec6daa82634f8ea27`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:51:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:55:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:55:23 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:55:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:56:28 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:56:31 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:58:07 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:58:10 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:58:11 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:58:15 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:58:19 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:58:23 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:58:27 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:58:29 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:58:31 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:58:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:58:40 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:58:47 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:58:48 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:59:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:59:14 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:59:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:59:25 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:59:27 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:59:30 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:59:34 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824c4944012b553f9093e4bc1e34c33ddeb18de868b7cacfd5a78b48b74b37f5`  
		Last Modified: Thu, 03 Mar 2022 21:06:26 GMT  
		Size: 86.5 MB (86479373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efb9a70b1f279b93f95def9ea981d86b2156e3c0640a4846ce2576fe0bb55b3`  
		Last Modified: Thu, 03 Mar 2022 21:06:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d6f756fc6d9b3870ab63c0521bd95d37142793f8a1b5859f87b8cfda7e384`  
		Last Modified: Thu, 03 Mar 2022 21:06:11 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeeb94361b8348cd1f0858be15b2be0e88fd310c1a2ff1901f309d535659778`  
		Last Modified: Thu, 03 Mar 2022 21:06:08 GMT  
		Size: 546.8 KB (546761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6930075a3b7fbb94f2e755cd07ce6e4ac3818b4c6f97c2a5ca5a9165aa4a08`  
		Last Modified: Thu, 03 Mar 2022 21:06:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187d4414deec38368f14f9d8f42bc5adea82b0da115291d8f2adfd4cdb0baa13`  
		Last Modified: Thu, 03 Mar 2022 21:06:39 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d2b2337a4b6b1720fbf89495efe726fcd1c383ead391bfedf2dc9fcb3da2b5`  
		Last Modified: Thu, 03 Mar 2022 21:07:04 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e926d59f36cb836accb9ba5455047f6adb546069d2c7862f5ce66c58b3f397`  
		Last Modified: Thu, 03 Mar 2022 21:06:39 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:ae70f59184e1cd30262c8d5b2283c3e867c5f256c9c9df3bf4e1a6adcf9d7e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:fa15263f741dd4307b2313eb14b46d5a4b7028fd4159810ec0685e920df49b39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235026756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468e05946fa80fe40a05962e9cc79a26c5a7b75aef8631b29a3bf2ff3e78b649`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:39:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:39:49 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:39:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:40:27 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:40:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:40:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:40:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:40:37 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:40:37 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:40:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:40:38 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:40:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb39c6807fb77da5ac679d4ccc9b69c1e5e2b489f12512fd6afd7832322a1014`  
		Last Modified: Thu, 03 Mar 2022 20:42:07 GMT  
		Size: 93.6 MB (93580080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ec24994ba799cab97f0787dbc65a6d013d2f45a4517183cc832daaaa53806`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dea30f37956bb39717366343b060771f31e623af6aba2f86e813974d05eba8`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb4afdb8e8e60145dd448944a446796ee594b6ed02750c6a778fccb13c06b1`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.0 MB (1003219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a9593299b6a3fca6dfff678b66e215e06cd1a736134c85128529fc6dda9c2d`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fab1112aff8eb07783792488c0daa5baab18c2fc7c75694c29d0614168a5fa8`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a0464741182bc14bbe33d2c884e74116f9378f9c9315c84a1883f3ce66bfd6`  
		Last Modified: Thu, 03 Mar 2022 20:41:58 GMT  
		Size: 113.7 MB (113727934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d555acc5e9ae7ecfa9e04b37670d8176b389240748fce73de64097a0f1278ccc`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:100ee8d17ab9f711b3b560181ebe391c6382557a32c1e9ee08c049b184ebba69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224093072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33451a777c372afc9bcaafdd70428860e7ccdb93a3ecd2031be24a4be1e20af0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:01:30 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:01:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:02:12 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:02:12 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:02:13 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:02:14 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:02:15 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:02:16 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:02:17 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:02:18 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:02:19 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:02:20 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:02:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:23 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:02:25 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:02:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:02:33 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:02:34 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:02:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:02:37 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:02:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317020d81860f4c7f3d0ba08b7d4fabb73c6d59fe81659e9f50c7041b7814b0`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 85.7 MB (85699022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fea459b86c67196991d4f93a562a0b91ec70a8dcd5303e790ef56c191e7f12`  
		Last Modified: Thu, 03 Mar 2022 20:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf4b0ff3d93dc9669374295f2a3930620b900c402ec5de48f74f3f33bfdb6d`  
		Last Modified: Thu, 03 Mar 2022 20:04:00 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eadd2b8e2a128a021b257f112c085ff9c5299a0d29fac4cbe8555e080ec929`  
		Last Modified: Thu, 03 Mar 2022 20:03:59 GMT  
		Size: 929.4 KB (929408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93477d9b74cbd8b18541de0f27af75437711c5b8665cbd853d4b88d792a99ee6`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81bab5f39f03ce3454d06174f99f7813f8df3c156cb15a72cac301c89b22072`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb3a0dc70b11a8867f2e9cee7a71b464310b86ba571928b03f73ef0676a427`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 113.7 MB (113727904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11578b3399fa42d05b447eea7ca706fab624f17643b1bb859e73a0b640973d9a`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:05ce851ed0917fbcee9e1d1b49c9a23c6221b5c18eb3e0f11b85b1b9b6780dac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231556682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bd10858d8a7259ed0ba4bdec36846fa328761fe17c81c765a4b45260cbf942`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:51:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 21:02:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:02:36 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 21:02:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 21:03:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 21:03:40 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 21:03:47 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 21:03:53 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 21:03:56 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 21:04:00 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 21:04:03 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 21:04:05 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 21:04:07 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 21:04:11 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 21:04:13 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 21:04:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 21:04:21 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 21:04:24 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 21:04:46 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 21:04:50 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 21:04:59 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 21:05:03 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 21:05:12 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 21:05:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd1018e1260c9561d82efdfffa45043f4f806857f701720527abdb33825ef5`  
		Last Modified: Thu, 03 Mar 2022 21:07:39 GMT  
		Size: 86.5 MB (86479352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d853e81df26f16338fa043e2217f6e2953bd306a840c659e2a20cc78e3f9ca`  
		Last Modified: Thu, 03 Mar 2022 21:07:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88e578facc7180f6af572c1d6359f7bb6f7c90673af246986625fd02ae5ff31`  
		Last Modified: Thu, 03 Mar 2022 21:07:23 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2ce469a139a35f0b02508b9d0c30a011692b391cf78e02f1978dc404251ff`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 904.2 KB (904233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7de6bd457bf881f1b38ecc7d675303a23659972ba041fdf9200d507b18435d`  
		Last Modified: Thu, 03 Mar 2022 21:07:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f15648cd335e09045b7843c9d0177c8993e95487e85335410976303b91e794`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f45df47bfc2bc197e45e411efdec1ceee73dc8edec98993904ec703f8d355ca`  
		Last Modified: Thu, 03 Mar 2022 21:07:31 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad986b49367799f33c2b514c7e34e86748f83cd76d56c48cd77c7e55f2455c`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:ae70f59184e1cd30262c8d5b2283c3e867c5f256c9c9df3bf4e1a6adcf9d7e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:fa15263f741dd4307b2313eb14b46d5a4b7028fd4159810ec0685e920df49b39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235026756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468e05946fa80fe40a05962e9cc79a26c5a7b75aef8631b29a3bf2ff3e78b649`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:39:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:39:49 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:39:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:40:27 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:40:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:40:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:40:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:40:37 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:40:37 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:40:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:40:38 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:40:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb39c6807fb77da5ac679d4ccc9b69c1e5e2b489f12512fd6afd7832322a1014`  
		Last Modified: Thu, 03 Mar 2022 20:42:07 GMT  
		Size: 93.6 MB (93580080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ec24994ba799cab97f0787dbc65a6d013d2f45a4517183cc832daaaa53806`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dea30f37956bb39717366343b060771f31e623af6aba2f86e813974d05eba8`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb4afdb8e8e60145dd448944a446796ee594b6ed02750c6a778fccb13c06b1`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.0 MB (1003219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a9593299b6a3fca6dfff678b66e215e06cd1a736134c85128529fc6dda9c2d`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fab1112aff8eb07783792488c0daa5baab18c2fc7c75694c29d0614168a5fa8`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a0464741182bc14bbe33d2c884e74116f9378f9c9315c84a1883f3ce66bfd6`  
		Last Modified: Thu, 03 Mar 2022 20:41:58 GMT  
		Size: 113.7 MB (113727934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d555acc5e9ae7ecfa9e04b37670d8176b389240748fce73de64097a0f1278ccc`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:100ee8d17ab9f711b3b560181ebe391c6382557a32c1e9ee08c049b184ebba69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224093072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33451a777c372afc9bcaafdd70428860e7ccdb93a3ecd2031be24a4be1e20af0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:01:30 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:01:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:02:12 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:02:12 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:02:13 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:02:14 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:02:15 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:02:16 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:02:17 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:02:18 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:02:19 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:02:20 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:02:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:23 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:02:25 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:02:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:02:33 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:02:34 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:02:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:02:37 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:02:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317020d81860f4c7f3d0ba08b7d4fabb73c6d59fe81659e9f50c7041b7814b0`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 85.7 MB (85699022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fea459b86c67196991d4f93a562a0b91ec70a8dcd5303e790ef56c191e7f12`  
		Last Modified: Thu, 03 Mar 2022 20:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf4b0ff3d93dc9669374295f2a3930620b900c402ec5de48f74f3f33bfdb6d`  
		Last Modified: Thu, 03 Mar 2022 20:04:00 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eadd2b8e2a128a021b257f112c085ff9c5299a0d29fac4cbe8555e080ec929`  
		Last Modified: Thu, 03 Mar 2022 20:03:59 GMT  
		Size: 929.4 KB (929408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93477d9b74cbd8b18541de0f27af75437711c5b8665cbd853d4b88d792a99ee6`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81bab5f39f03ce3454d06174f99f7813f8df3c156cb15a72cac301c89b22072`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb3a0dc70b11a8867f2e9cee7a71b464310b86ba571928b03f73ef0676a427`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 113.7 MB (113727904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11578b3399fa42d05b447eea7ca706fab624f17643b1bb859e73a0b640973d9a`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:05ce851ed0917fbcee9e1d1b49c9a23c6221b5c18eb3e0f11b85b1b9b6780dac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231556682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bd10858d8a7259ed0ba4bdec36846fa328761fe17c81c765a4b45260cbf942`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:51:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 21:02:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:02:36 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 21:02:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 21:03:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 21:03:40 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 21:03:47 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 21:03:53 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 21:03:56 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 21:04:00 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 21:04:03 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 21:04:05 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 21:04:07 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 21:04:11 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 21:04:13 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 21:04:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 21:04:21 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 21:04:24 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 21:04:46 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 21:04:50 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 21:04:59 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 21:05:03 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 21:05:12 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 21:05:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd1018e1260c9561d82efdfffa45043f4f806857f701720527abdb33825ef5`  
		Last Modified: Thu, 03 Mar 2022 21:07:39 GMT  
		Size: 86.5 MB (86479352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d853e81df26f16338fa043e2217f6e2953bd306a840c659e2a20cc78e3f9ca`  
		Last Modified: Thu, 03 Mar 2022 21:07:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88e578facc7180f6af572c1d6359f7bb6f7c90673af246986625fd02ae5ff31`  
		Last Modified: Thu, 03 Mar 2022 21:07:23 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2ce469a139a35f0b02508b9d0c30a011692b391cf78e02f1978dc404251ff`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 904.2 KB (904233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7de6bd457bf881f1b38ecc7d675303a23659972ba041fdf9200d507b18435d`  
		Last Modified: Thu, 03 Mar 2022 21:07:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f15648cd335e09045b7843c9d0177c8993e95487e85335410976303b91e794`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f45df47bfc2bc197e45e411efdec1ceee73dc8edec98993904ec703f8d355ca`  
		Last Modified: Thu, 03 Mar 2022 21:07:31 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad986b49367799f33c2b514c7e34e86748f83cd76d56c48cd77c7e55f2455c`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:6339501348af9eb3a7e2039ef8055bee3d6f40b4c4660bd691811be0340589e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:02f9122ae6971c8a3f745440ab1d204d306b3efc4c453f3f570d740cc0ce69d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234224379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6061b9cfa4e1eeed21f2bef4dbba3845bc07b5d252f6c5acd947cd41649720fd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:38:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:38:01 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:38:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:38:48 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:38:48 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:38:48 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:38:48 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:38:48 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:38:48 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 03 Mar 2022 20:38:48 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 03 Mar 2022 20:38:48 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:38:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:38:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:38:49 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:38:49 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:38:50 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 03 Mar 2022 20:38:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:38:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:38:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:38:57 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:38:57 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:38:57 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:38:57 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e26f312b55420283ec88133940bf7f91764464f58f1861612d697d10d903eb`  
		Last Modified: Thu, 03 Mar 2022 20:41:22 GMT  
		Size: 93.6 MB (93580470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6595d65755dfd2db718649f213935c206a04e2443e94d9def82004cec13c8f7`  
		Last Modified: Thu, 03 Mar 2022 20:41:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e1156933eb4b5b0948b99e92616dac6f646a7b59e40c374300e7f2ca2bb7e8`  
		Last Modified: Thu, 03 Mar 2022 20:41:08 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350751d0c7f7b09c79a65f4ec9b3e85f6aaec7d073eb09b491a7403681b16956`  
		Last Modified: Thu, 03 Mar 2022 20:41:06 GMT  
		Size: 577.0 KB (576971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767a486682fa9367d576c90e860624344ccc3d0cbd1fbf1e737c19472f5c30ae`  
		Last Modified: Thu, 03 Mar 2022 20:41:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24348a172b025d9773d251891400a3d4d9ce5a6c6b739796de355e7b3c42a7b2`  
		Last Modified: Thu, 03 Mar 2022 20:41:06 GMT  
		Size: 6.9 KB (6889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b4debac004fda2af14c9425a3cb2f58b6f5404db907ec7d221e19221745bc0`  
		Last Modified: Thu, 03 Mar 2022 20:41:11 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f629828c9c3c375a753c42841653cc2cd16673314265fccbb268c6d71ab34131`  
		Last Modified: Thu, 03 Mar 2022 20:41:07 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6a81cc6c2253c285486f29e734599ccfd5b77751dbc0ce9e91781661d942aca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223334084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1829b38d779f8ecae6f13f0f1b1d910b61f7f82f3ae70a05fc3ce5f9066063b0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 19:59:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 19:59:20 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 19:59:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:00:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:00:03 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:00:04 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:00:05 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:00:06 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:00:07 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 03 Mar 2022 20:00:08 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 03 Mar 2022 20:00:09 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:00:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:00:11 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:00:12 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:00:13 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:00:15 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 03 Mar 2022 20:00:20 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:00:21 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:00:23 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:00:23 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:00:25 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:00:25 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:00:26 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603888e2649b74be803a493ad60570eaf6fa7a0db55350510ca362482d1d046a`  
		Last Modified: Thu, 03 Mar 2022 20:03:22 GMT  
		Size: 85.7 MB (85699004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245a1b8ba7feeb0507a81ce2a5116d45572650fecbe18e02c2be9bd9370d55b5`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a077eeefcedfb7f8b0ead8b47dc2ee5f00ce4d1dd5996efe00956a83d83b4a`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4295b7f5f73ca4ad6fd600da6f0e006b109fcc6d6ee8c2e5883aaca4dc72d33`  
		Last Modified: Thu, 03 Mar 2022 20:03:08 GMT  
		Size: 546.9 KB (546947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9de10c001f237ee55abd3ee02745208923c66fca86dc47b426d70f40739f9c3`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9d842f2e1f3898318118be910214bed49eef1fc50293e521740463c02bcb9d`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 6.9 KB (6870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30155b02834c5698b9f82c9103ca30c01979f28263d67af5cdb1e7d87e43af47`  
		Last Modified: Thu, 03 Mar 2022 20:03:24 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2b92809091e6d9c115b9597a33bd765c67a66d2c0ae867c45fd63bbe23734c`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:96154e438f18aa7a9e673b710cf77164457d5b5165c553b033d3420815622ffd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230822723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4042e382800f6deac12edec9dd2bc991ab375bcce3009ecb6c0873912caca00`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:51:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:55:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:55:23 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:55:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:56:28 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:56:31 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:56:34 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:56:37 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:56:40 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:56:44 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 03 Mar 2022 20:56:48 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 03 Mar 2022 20:56:51 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:56:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:56:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:57:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:57:15 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:57:16 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 03 Mar 2022 20:57:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:57:40 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:57:47 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:57:50 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:57:51 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:57:54 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:57:57 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824c4944012b553f9093e4bc1e34c33ddeb18de868b7cacfd5a78b48b74b37f5`  
		Last Modified: Thu, 03 Mar 2022 21:06:26 GMT  
		Size: 86.5 MB (86479373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efb9a70b1f279b93f95def9ea981d86b2156e3c0640a4846ce2576fe0bb55b3`  
		Last Modified: Thu, 03 Mar 2022 21:06:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d6f756fc6d9b3870ab63c0521bd95d37142793f8a1b5859f87b8cfda7e384`  
		Last Modified: Thu, 03 Mar 2022 21:06:11 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeeb94361b8348cd1f0858be15b2be0e88fd310c1a2ff1901f309d535659778`  
		Last Modified: Thu, 03 Mar 2022 21:06:08 GMT  
		Size: 546.8 KB (546761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed48e441532fbf84cc994434ac6f81cc1078258fcfb629503043297881010a73`  
		Last Modified: Thu, 03 Mar 2022 21:06:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f948c5c874ec40135e529de4ac45b8f1c216eb258add410e79b8f67dad5af4`  
		Last Modified: Thu, 03 Mar 2022 21:06:08 GMT  
		Size: 6.9 KB (6889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac85099ddf7a82bcbb0d31e70010ef4e0774fc6eeb9e065f35f7dc2cf4c50d`  
		Last Modified: Thu, 03 Mar 2022 21:06:18 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a893c8ea21d195f6a358d4107281bb07c5457fdc85cca21e5ce0af0e6f0a25b`  
		Last Modified: Thu, 03 Mar 2022 21:06:08 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:6339501348af9eb3a7e2039ef8055bee3d6f40b4c4660bd691811be0340589e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:02f9122ae6971c8a3f745440ab1d204d306b3efc4c453f3f570d740cc0ce69d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234224379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6061b9cfa4e1eeed21f2bef4dbba3845bc07b5d252f6c5acd947cd41649720fd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:38:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:38:01 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:38:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:38:48 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:38:48 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:38:48 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:38:48 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:38:48 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:38:48 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 03 Mar 2022 20:38:48 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 03 Mar 2022 20:38:48 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:38:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:38:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:38:49 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:38:49 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:38:50 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 03 Mar 2022 20:38:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:38:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:38:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:38:57 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:38:57 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:38:57 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:38:57 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e26f312b55420283ec88133940bf7f91764464f58f1861612d697d10d903eb`  
		Last Modified: Thu, 03 Mar 2022 20:41:22 GMT  
		Size: 93.6 MB (93580470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6595d65755dfd2db718649f213935c206a04e2443e94d9def82004cec13c8f7`  
		Last Modified: Thu, 03 Mar 2022 20:41:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e1156933eb4b5b0948b99e92616dac6f646a7b59e40c374300e7f2ca2bb7e8`  
		Last Modified: Thu, 03 Mar 2022 20:41:08 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350751d0c7f7b09c79a65f4ec9b3e85f6aaec7d073eb09b491a7403681b16956`  
		Last Modified: Thu, 03 Mar 2022 20:41:06 GMT  
		Size: 577.0 KB (576971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767a486682fa9367d576c90e860624344ccc3d0cbd1fbf1e737c19472f5c30ae`  
		Last Modified: Thu, 03 Mar 2022 20:41:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24348a172b025d9773d251891400a3d4d9ce5a6c6b739796de355e7b3c42a7b2`  
		Last Modified: Thu, 03 Mar 2022 20:41:06 GMT  
		Size: 6.9 KB (6889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b4debac004fda2af14c9425a3cb2f58b6f5404db907ec7d221e19221745bc0`  
		Last Modified: Thu, 03 Mar 2022 20:41:11 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f629828c9c3c375a753c42841653cc2cd16673314265fccbb268c6d71ab34131`  
		Last Modified: Thu, 03 Mar 2022 20:41:07 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6a81cc6c2253c285486f29e734599ccfd5b77751dbc0ce9e91781661d942aca9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223334084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1829b38d779f8ecae6f13f0f1b1d910b61f7f82f3ae70a05fc3ce5f9066063b0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 19:59:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 19:59:20 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 19:59:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:00:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:00:03 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:00:04 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:00:05 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:00:06 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:00:07 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 03 Mar 2022 20:00:08 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 03 Mar 2022 20:00:09 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:00:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:00:11 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:00:12 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:00:13 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:00:15 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 03 Mar 2022 20:00:20 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:00:21 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:00:23 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:00:23 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:00:25 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:00:25 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:00:26 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603888e2649b74be803a493ad60570eaf6fa7a0db55350510ca362482d1d046a`  
		Last Modified: Thu, 03 Mar 2022 20:03:22 GMT  
		Size: 85.7 MB (85699004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245a1b8ba7feeb0507a81ce2a5116d45572650fecbe18e02c2be9bd9370d55b5`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a077eeefcedfb7f8b0ead8b47dc2ee5f00ce4d1dd5996efe00956a83d83b4a`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4295b7f5f73ca4ad6fd600da6f0e006b109fcc6d6ee8c2e5883aaca4dc72d33`  
		Last Modified: Thu, 03 Mar 2022 20:03:08 GMT  
		Size: 546.9 KB (546947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9de10c001f237ee55abd3ee02745208923c66fca86dc47b426d70f40739f9c3`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9d842f2e1f3898318118be910214bed49eef1fc50293e521740463c02bcb9d`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 6.9 KB (6870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30155b02834c5698b9f82c9103ca30c01979f28263d67af5cdb1e7d87e43af47`  
		Last Modified: Thu, 03 Mar 2022 20:03:24 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2b92809091e6d9c115b9597a33bd765c67a66d2c0ae867c45fd63bbe23734c`  
		Last Modified: Thu, 03 Mar 2022 20:03:07 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:96154e438f18aa7a9e673b710cf77164457d5b5165c553b033d3420815622ffd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230822723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4042e382800f6deac12edec9dd2bc991ab375bcce3009ecb6c0873912caca00`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:51:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:55:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:55:23 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:55:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:56:28 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:56:31 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:56:34 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:56:37 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:56:40 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:56:44 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 03 Mar 2022 20:56:48 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 03 Mar 2022 20:56:51 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:56:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:56:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 03 Mar 2022 20:57:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:57:15 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:57:16 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 03 Mar 2022 20:57:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:57:40 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:57:47 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:57:50 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:57:51 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:57:54 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:57:57 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824c4944012b553f9093e4bc1e34c33ddeb18de868b7cacfd5a78b48b74b37f5`  
		Last Modified: Thu, 03 Mar 2022 21:06:26 GMT  
		Size: 86.5 MB (86479373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efb9a70b1f279b93f95def9ea981d86b2156e3c0640a4846ce2576fe0bb55b3`  
		Last Modified: Thu, 03 Mar 2022 21:06:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d6f756fc6d9b3870ab63c0521bd95d37142793f8a1b5859f87b8cfda7e384`  
		Last Modified: Thu, 03 Mar 2022 21:06:11 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeeb94361b8348cd1f0858be15b2be0e88fd310c1a2ff1901f309d535659778`  
		Last Modified: Thu, 03 Mar 2022 21:06:08 GMT  
		Size: 546.8 KB (546761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed48e441532fbf84cc994434ac6f81cc1078258fcfb629503043297881010a73`  
		Last Modified: Thu, 03 Mar 2022 21:06:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f948c5c874ec40135e529de4ac45b8f1c216eb258add410e79b8f67dad5af4`  
		Last Modified: Thu, 03 Mar 2022 21:06:08 GMT  
		Size: 6.9 KB (6889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac85099ddf7a82bcbb0d31e70010ef4e0774fc6eeb9e065f35f7dc2cf4c50d`  
		Last Modified: Thu, 03 Mar 2022 21:06:18 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a893c8ea21d195f6a358d4107281bb07c5457fdc85cca21e5ce0af0e6f0a25b`  
		Last Modified: Thu, 03 Mar 2022 21:06:08 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:d675ad340e9b8fad82a6b49aa58186753f50aa528f4f3876a8e703d7f0db04f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:950607cd74458c8c97131dbbbf3e991228ac0a4b631b85f529299e913ff9a9ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237292009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a67995d4904a843db141d7a8e559f0d2df49fb1e4b5a83fdc2c8748c572499`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:38:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:38:01 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:38:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:38:48 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:38:48 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:39:06 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:39:07 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:39:07 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:39:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:39:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:39:25 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:39:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:39:26 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:39:26 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:39:27 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:39:27 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e26f312b55420283ec88133940bf7f91764464f58f1861612d697d10d903eb`  
		Last Modified: Thu, 03 Mar 2022 20:41:22 GMT  
		Size: 93.6 MB (93580470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6595d65755dfd2db718649f213935c206a04e2443e94d9def82004cec13c8f7`  
		Last Modified: Thu, 03 Mar 2022 20:41:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e1156933eb4b5b0948b99e92616dac6f646a7b59e40c374300e7f2ca2bb7e8`  
		Last Modified: Thu, 03 Mar 2022 20:41:08 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350751d0c7f7b09c79a65f4ec9b3e85f6aaec7d073eb09b491a7403681b16956`  
		Last Modified: Thu, 03 Mar 2022 20:41:06 GMT  
		Size: 577.0 KB (576971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e8553193e7c7dff14b7075c2d1ce330b77813068e11eb2b0a589a167545dda`  
		Last Modified: Thu, 03 Mar 2022 20:41:32 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e010bd86a6d1788aabe769d0aa7ebc66123ea6a1a576bfbd72d9efe570392`  
		Last Modified: Thu, 03 Mar 2022 20:41:32 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d7315e3b64151f7aa7eb9000af282c5763c9d89fc5138b2802738ad528f741`  
		Last Modified: Thu, 03 Mar 2022 20:41:38 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bacaf2b6a20a3cf00f54d2c39ecbda1f23d6a1851f325c94e3470982f471da`  
		Last Modified: Thu, 03 Mar 2022 20:41:32 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:682c04575d0e3964f325488cc0ce7b4e17fd0ffbd7ae07b7f948c1fff21848a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226401706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267e77b75883c0b4cd7601b35b5b94925fedb24299ceb7639abbd2d82be03975`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 19:59:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 19:59:20 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 19:59:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:00:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:00:03 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:00:33 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:00:34 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:00:35 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:00:36 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:00:37 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:00:38 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:00:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:00:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:00:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:43 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:00:44 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:00:46 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:00:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:00:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:00:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:00:55 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:00:57 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:00:57 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:00:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603888e2649b74be803a493ad60570eaf6fa7a0db55350510ca362482d1d046a`  
		Last Modified: Thu, 03 Mar 2022 20:03:22 GMT  
		Size: 85.7 MB (85699004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245a1b8ba7feeb0507a81ce2a5116d45572650fecbe18e02c2be9bd9370d55b5`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a077eeefcedfb7f8b0ead8b47dc2ee5f00ce4d1dd5996efe00956a83d83b4a`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4295b7f5f73ca4ad6fd600da6f0e006b109fcc6d6ee8c2e5883aaca4dc72d33`  
		Last Modified: Thu, 03 Mar 2022 20:03:08 GMT  
		Size: 546.9 KB (546947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dbb8e122d99aa3835c03f0449d5945c7bebba698810aad047ef9a94a44136e`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13fcb4bf6e01237803b44e91d6aa560b248b6332bf98a27a22220a010ceb0`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402eb2ec9cb549b7ebb5945d00cf5802b55e847b5f8cb132ce83c7ad4a5ab592`  
		Last Modified: Thu, 03 Mar 2022 20:03:44 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc7ab7b806dbaea4ad80109ddbe8b3b385c9e3253236066f663b92b4d3d17e7`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:74b4df5d2e53facb3a8215ae2293955564fb71ec0dc3298f314131aaad1aa624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233890360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bebe00266e33a543053f11093cee7698e14058a91a2f7ec6daa82634f8ea27`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:51:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:55:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:55:23 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:55:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:56:28 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:56:31 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:58:07 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:58:10 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:58:11 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:58:15 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:58:19 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:58:23 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:58:27 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:58:29 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:58:31 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:58:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:58:40 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:58:47 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:58:48 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:59:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:59:14 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:59:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:59:25 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:59:27 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:59:30 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:59:34 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824c4944012b553f9093e4bc1e34c33ddeb18de868b7cacfd5a78b48b74b37f5`  
		Last Modified: Thu, 03 Mar 2022 21:06:26 GMT  
		Size: 86.5 MB (86479373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efb9a70b1f279b93f95def9ea981d86b2156e3c0640a4846ce2576fe0bb55b3`  
		Last Modified: Thu, 03 Mar 2022 21:06:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d6f756fc6d9b3870ab63c0521bd95d37142793f8a1b5859f87b8cfda7e384`  
		Last Modified: Thu, 03 Mar 2022 21:06:11 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeeb94361b8348cd1f0858be15b2be0e88fd310c1a2ff1901f309d535659778`  
		Last Modified: Thu, 03 Mar 2022 21:06:08 GMT  
		Size: 546.8 KB (546761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6930075a3b7fbb94f2e755cd07ce6e4ac3818b4c6f97c2a5ca5a9165aa4a08`  
		Last Modified: Thu, 03 Mar 2022 21:06:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187d4414deec38368f14f9d8f42bc5adea82b0da115291d8f2adfd4cdb0baa13`  
		Last Modified: Thu, 03 Mar 2022 21:06:39 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d2b2337a4b6b1720fbf89495efe726fcd1c383ead391bfedf2dc9fcb3da2b5`  
		Last Modified: Thu, 03 Mar 2022 21:07:04 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e926d59f36cb836accb9ba5455047f6adb546069d2c7862f5ce66c58b3f397`  
		Last Modified: Thu, 03 Mar 2022 21:06:39 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:d675ad340e9b8fad82a6b49aa58186753f50aa528f4f3876a8e703d7f0db04f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:950607cd74458c8c97131dbbbf3e991228ac0a4b631b85f529299e913ff9a9ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237292009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a67995d4904a843db141d7a8e559f0d2df49fb1e4b5a83fdc2c8748c572499`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:38:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:38:01 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:38:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:38:48 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:38:48 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:39:05 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:39:06 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:39:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:39:07 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:39:07 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:39:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:39:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:39:25 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:39:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:39:26 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:39:26 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:39:27 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:39:27 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e26f312b55420283ec88133940bf7f91764464f58f1861612d697d10d903eb`  
		Last Modified: Thu, 03 Mar 2022 20:41:22 GMT  
		Size: 93.6 MB (93580470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6595d65755dfd2db718649f213935c206a04e2443e94d9def82004cec13c8f7`  
		Last Modified: Thu, 03 Mar 2022 20:41:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e1156933eb4b5b0948b99e92616dac6f646a7b59e40c374300e7f2ca2bb7e8`  
		Last Modified: Thu, 03 Mar 2022 20:41:08 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350751d0c7f7b09c79a65f4ec9b3e85f6aaec7d073eb09b491a7403681b16956`  
		Last Modified: Thu, 03 Mar 2022 20:41:06 GMT  
		Size: 577.0 KB (576971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e8553193e7c7dff14b7075c2d1ce330b77813068e11eb2b0a589a167545dda`  
		Last Modified: Thu, 03 Mar 2022 20:41:32 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e010bd86a6d1788aabe769d0aa7ebc66123ea6a1a576bfbd72d9efe570392`  
		Last Modified: Thu, 03 Mar 2022 20:41:32 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d7315e3b64151f7aa7eb9000af282c5763c9d89fc5138b2802738ad528f741`  
		Last Modified: Thu, 03 Mar 2022 20:41:38 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bacaf2b6a20a3cf00f54d2c39ecbda1f23d6a1851f325c94e3470982f471da`  
		Last Modified: Thu, 03 Mar 2022 20:41:32 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:682c04575d0e3964f325488cc0ce7b4e17fd0ffbd7ae07b7f948c1fff21848a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226401706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267e77b75883c0b4cd7601b35b5b94925fedb24299ceb7639abbd2d82be03975`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 19:59:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 19:59:20 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 19:59:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:00:03 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:00:03 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:00:33 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:00:34 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:00:35 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:00:36 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:00:37 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:00:38 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:00:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:00:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:00:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:00:43 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:00:44 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:00:46 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:00:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:00:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:00:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:00:55 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:00:57 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:00:57 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:00:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603888e2649b74be803a493ad60570eaf6fa7a0db55350510ca362482d1d046a`  
		Last Modified: Thu, 03 Mar 2022 20:03:22 GMT  
		Size: 85.7 MB (85699004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245a1b8ba7feeb0507a81ce2a5116d45572650fecbe18e02c2be9bd9370d55b5`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a077eeefcedfb7f8b0ead8b47dc2ee5f00ce4d1dd5996efe00956a83d83b4a`  
		Last Modified: Thu, 03 Mar 2022 20:03:10 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4295b7f5f73ca4ad6fd600da6f0e006b109fcc6d6ee8c2e5883aaca4dc72d33`  
		Last Modified: Thu, 03 Mar 2022 20:03:08 GMT  
		Size: 546.9 KB (546947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dbb8e122d99aa3835c03f0449d5945c7bebba698810aad047ef9a94a44136e`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc13fcb4bf6e01237803b44e91d6aa560b248b6332bf98a27a22220a010ceb0`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402eb2ec9cb549b7ebb5945d00cf5802b55e847b5f8cb132ce83c7ad4a5ab592`  
		Last Modified: Thu, 03 Mar 2022 20:03:44 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc7ab7b806dbaea4ad80109ddbe8b3b385c9e3253236066f663b92b4d3d17e7`  
		Last Modified: Thu, 03 Mar 2022 20:03:35 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:74b4df5d2e53facb3a8215ae2293955564fb71ec0dc3298f314131aaad1aa624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233890360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bebe00266e33a543053f11093cee7698e14058a91a2f7ec6daa82634f8ea27`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:51:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:55:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:55:23 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:55:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:56:28 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:56:31 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:58:07 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:58:10 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:58:11 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:58:15 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:58:19 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 03 Mar 2022 20:58:23 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 03 Mar 2022 20:58:27 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 03 Mar 2022 20:58:29 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:58:31 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:58:33 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 03 Mar 2022 20:58:40 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 03 Mar 2022 20:58:47 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:58:48 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 03 Mar 2022 20:59:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 03 Mar 2022 20:59:14 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 03 Mar 2022 20:59:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 03 Mar 2022 20:59:25 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:59:27 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:59:30 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:59:34 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824c4944012b553f9093e4bc1e34c33ddeb18de868b7cacfd5a78b48b74b37f5`  
		Last Modified: Thu, 03 Mar 2022 21:06:26 GMT  
		Size: 86.5 MB (86479373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efb9a70b1f279b93f95def9ea981d86b2156e3c0640a4846ce2576fe0bb55b3`  
		Last Modified: Thu, 03 Mar 2022 21:06:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698d6f756fc6d9b3870ab63c0521bd95d37142793f8a1b5859f87b8cfda7e384`  
		Last Modified: Thu, 03 Mar 2022 21:06:11 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeeb94361b8348cd1f0858be15b2be0e88fd310c1a2ff1901f309d535659778`  
		Last Modified: Thu, 03 Mar 2022 21:06:08 GMT  
		Size: 546.8 KB (546761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6930075a3b7fbb94f2e755cd07ce6e4ac3818b4c6f97c2a5ca5a9165aa4a08`  
		Last Modified: Thu, 03 Mar 2022 21:06:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187d4414deec38368f14f9d8f42bc5adea82b0da115291d8f2adfd4cdb0baa13`  
		Last Modified: Thu, 03 Mar 2022 21:06:39 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d2b2337a4b6b1720fbf89495efe726fcd1c383ead391bfedf2dc9fcb3da2b5`  
		Last Modified: Thu, 03 Mar 2022 21:07:04 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e926d59f36cb836accb9ba5455047f6adb546069d2c7862f5ce66c58b3f397`  
		Last Modified: Thu, 03 Mar 2022 21:06:39 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:ae70f59184e1cd30262c8d5b2283c3e867c5f256c9c9df3bf4e1a6adcf9d7e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:fa15263f741dd4307b2313eb14b46d5a4b7028fd4159810ec0685e920df49b39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235026756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468e05946fa80fe40a05962e9cc79a26c5a7b75aef8631b29a3bf2ff3e78b649`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:39:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:39:49 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:39:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:40:27 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:40:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:40:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:40:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:40:37 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:40:37 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:40:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:40:38 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:40:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb39c6807fb77da5ac679d4ccc9b69c1e5e2b489f12512fd6afd7832322a1014`  
		Last Modified: Thu, 03 Mar 2022 20:42:07 GMT  
		Size: 93.6 MB (93580080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ec24994ba799cab97f0787dbc65a6d013d2f45a4517183cc832daaaa53806`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dea30f37956bb39717366343b060771f31e623af6aba2f86e813974d05eba8`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb4afdb8e8e60145dd448944a446796ee594b6ed02750c6a778fccb13c06b1`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.0 MB (1003219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a9593299b6a3fca6dfff678b66e215e06cd1a736134c85128529fc6dda9c2d`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fab1112aff8eb07783792488c0daa5baab18c2fc7c75694c29d0614168a5fa8`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a0464741182bc14bbe33d2c884e74116f9378f9c9315c84a1883f3ce66bfd6`  
		Last Modified: Thu, 03 Mar 2022 20:41:58 GMT  
		Size: 113.7 MB (113727934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d555acc5e9ae7ecfa9e04b37670d8176b389240748fce73de64097a0f1278ccc`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:100ee8d17ab9f711b3b560181ebe391c6382557a32c1e9ee08c049b184ebba69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224093072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33451a777c372afc9bcaafdd70428860e7ccdb93a3ecd2031be24a4be1e20af0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:01:30 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:01:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:02:12 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:02:12 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:02:13 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:02:14 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:02:15 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:02:16 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:02:17 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:02:18 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:02:19 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:02:20 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:02:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:23 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:02:25 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:02:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:02:33 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:02:34 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:02:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:02:37 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:02:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317020d81860f4c7f3d0ba08b7d4fabb73c6d59fe81659e9f50c7041b7814b0`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 85.7 MB (85699022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fea459b86c67196991d4f93a562a0b91ec70a8dcd5303e790ef56c191e7f12`  
		Last Modified: Thu, 03 Mar 2022 20:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf4b0ff3d93dc9669374295f2a3930620b900c402ec5de48f74f3f33bfdb6d`  
		Last Modified: Thu, 03 Mar 2022 20:04:00 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eadd2b8e2a128a021b257f112c085ff9c5299a0d29fac4cbe8555e080ec929`  
		Last Modified: Thu, 03 Mar 2022 20:03:59 GMT  
		Size: 929.4 KB (929408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93477d9b74cbd8b18541de0f27af75437711c5b8665cbd853d4b88d792a99ee6`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81bab5f39f03ce3454d06174f99f7813f8df3c156cb15a72cac301c89b22072`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb3a0dc70b11a8867f2e9cee7a71b464310b86ba571928b03f73ef0676a427`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 113.7 MB (113727904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11578b3399fa42d05b447eea7ca706fab624f17643b1bb859e73a0b640973d9a`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:05ce851ed0917fbcee9e1d1b49c9a23c6221b5c18eb3e0f11b85b1b9b6780dac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231556682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bd10858d8a7259ed0ba4bdec36846fa328761fe17c81c765a4b45260cbf942`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:51:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 21:02:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:02:36 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 21:02:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 21:03:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 21:03:40 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 21:03:47 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 21:03:53 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 21:03:56 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 21:04:00 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 21:04:03 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 21:04:05 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 21:04:07 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 21:04:11 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 21:04:13 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 21:04:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 21:04:21 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 21:04:24 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 21:04:46 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 21:04:50 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 21:04:59 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 21:05:03 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 21:05:12 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 21:05:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd1018e1260c9561d82efdfffa45043f4f806857f701720527abdb33825ef5`  
		Last Modified: Thu, 03 Mar 2022 21:07:39 GMT  
		Size: 86.5 MB (86479352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d853e81df26f16338fa043e2217f6e2953bd306a840c659e2a20cc78e3f9ca`  
		Last Modified: Thu, 03 Mar 2022 21:07:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88e578facc7180f6af572c1d6359f7bb6f7c90673af246986625fd02ae5ff31`  
		Last Modified: Thu, 03 Mar 2022 21:07:23 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2ce469a139a35f0b02508b9d0c30a011692b391cf78e02f1978dc404251ff`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 904.2 KB (904233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7de6bd457bf881f1b38ecc7d675303a23659972ba041fdf9200d507b18435d`  
		Last Modified: Thu, 03 Mar 2022 21:07:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f15648cd335e09045b7843c9d0177c8993e95487e85335410976303b91e794`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f45df47bfc2bc197e45e411efdec1ceee73dc8edec98993904ec703f8d355ca`  
		Last Modified: Thu, 03 Mar 2022 21:07:31 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad986b49367799f33c2b514c7e34e86748f83cd76d56c48cd77c7e55f2455c`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:ae70f59184e1cd30262c8d5b2283c3e867c5f256c9c9df3bf4e1a6adcf9d7e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:fa15263f741dd4307b2313eb14b46d5a4b7028fd4159810ec0685e920df49b39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235026756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468e05946fa80fe40a05962e9cc79a26c5a7b75aef8631b29a3bf2ff3e78b649`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:39:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:39:49 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:39:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:40:27 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:40:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:40:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:40:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:40:37 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:40:37 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:40:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:40:38 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:40:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb39c6807fb77da5ac679d4ccc9b69c1e5e2b489f12512fd6afd7832322a1014`  
		Last Modified: Thu, 03 Mar 2022 20:42:07 GMT  
		Size: 93.6 MB (93580080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ec24994ba799cab97f0787dbc65a6d013d2f45a4517183cc832daaaa53806`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dea30f37956bb39717366343b060771f31e623af6aba2f86e813974d05eba8`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb4afdb8e8e60145dd448944a446796ee594b6ed02750c6a778fccb13c06b1`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.0 MB (1003219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a9593299b6a3fca6dfff678b66e215e06cd1a736134c85128529fc6dda9c2d`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fab1112aff8eb07783792488c0daa5baab18c2fc7c75694c29d0614168a5fa8`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a0464741182bc14bbe33d2c884e74116f9378f9c9315c84a1883f3ce66bfd6`  
		Last Modified: Thu, 03 Mar 2022 20:41:58 GMT  
		Size: 113.7 MB (113727934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d555acc5e9ae7ecfa9e04b37670d8176b389240748fce73de64097a0f1278ccc`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:100ee8d17ab9f711b3b560181ebe391c6382557a32c1e9ee08c049b184ebba69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224093072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33451a777c372afc9bcaafdd70428860e7ccdb93a3ecd2031be24a4be1e20af0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:01:30 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:01:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:02:12 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:02:12 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:02:13 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:02:14 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:02:15 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:02:16 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:02:17 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:02:18 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:02:19 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:02:20 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:02:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:23 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:02:25 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:02:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:02:33 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:02:34 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:02:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:02:37 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:02:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317020d81860f4c7f3d0ba08b7d4fabb73c6d59fe81659e9f50c7041b7814b0`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 85.7 MB (85699022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fea459b86c67196991d4f93a562a0b91ec70a8dcd5303e790ef56c191e7f12`  
		Last Modified: Thu, 03 Mar 2022 20:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf4b0ff3d93dc9669374295f2a3930620b900c402ec5de48f74f3f33bfdb6d`  
		Last Modified: Thu, 03 Mar 2022 20:04:00 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eadd2b8e2a128a021b257f112c085ff9c5299a0d29fac4cbe8555e080ec929`  
		Last Modified: Thu, 03 Mar 2022 20:03:59 GMT  
		Size: 929.4 KB (929408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93477d9b74cbd8b18541de0f27af75437711c5b8665cbd853d4b88d792a99ee6`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81bab5f39f03ce3454d06174f99f7813f8df3c156cb15a72cac301c89b22072`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb3a0dc70b11a8867f2e9cee7a71b464310b86ba571928b03f73ef0676a427`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 113.7 MB (113727904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11578b3399fa42d05b447eea7ca706fab624f17643b1bb859e73a0b640973d9a`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:05ce851ed0917fbcee9e1d1b49c9a23c6221b5c18eb3e0f11b85b1b9b6780dac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231556682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bd10858d8a7259ed0ba4bdec36846fa328761fe17c81c765a4b45260cbf942`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:51:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 21:02:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:02:36 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 21:02:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 21:03:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 21:03:40 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 21:03:47 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 21:03:53 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 21:03:56 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 21:04:00 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 21:04:03 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 21:04:05 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 21:04:07 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 21:04:11 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 21:04:13 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 21:04:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 21:04:21 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 21:04:24 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 21:04:46 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 21:04:50 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 21:04:59 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 21:05:03 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 21:05:12 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 21:05:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd1018e1260c9561d82efdfffa45043f4f806857f701720527abdb33825ef5`  
		Last Modified: Thu, 03 Mar 2022 21:07:39 GMT  
		Size: 86.5 MB (86479352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d853e81df26f16338fa043e2217f6e2953bd306a840c659e2a20cc78e3f9ca`  
		Last Modified: Thu, 03 Mar 2022 21:07:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88e578facc7180f6af572c1d6359f7bb6f7c90673af246986625fd02ae5ff31`  
		Last Modified: Thu, 03 Mar 2022 21:07:23 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2ce469a139a35f0b02508b9d0c30a011692b391cf78e02f1978dc404251ff`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 904.2 KB (904233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7de6bd457bf881f1b38ecc7d675303a23659972ba041fdf9200d507b18435d`  
		Last Modified: Thu, 03 Mar 2022 21:07:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f15648cd335e09045b7843c9d0177c8993e95487e85335410976303b91e794`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f45df47bfc2bc197e45e411efdec1ceee73dc8edec98993904ec703f8d355ca`  
		Last Modified: Thu, 03 Mar 2022 21:07:31 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad986b49367799f33c2b514c7e34e86748f83cd76d56c48cd77c7e55f2455c`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:ae70f59184e1cd30262c8d5b2283c3e867c5f256c9c9df3bf4e1a6adcf9d7e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:fa15263f741dd4307b2313eb14b46d5a4b7028fd4159810ec0685e920df49b39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235026756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468e05946fa80fe40a05962e9cc79a26c5a7b75aef8631b29a3bf2ff3e78b649`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:39:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:39:49 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:39:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:40:27 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:40:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:40:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:40:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:40:28 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:40:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:40:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:40:37 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:40:37 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:40:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:40:38 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:40:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb39c6807fb77da5ac679d4ccc9b69c1e5e2b489f12512fd6afd7832322a1014`  
		Last Modified: Thu, 03 Mar 2022 20:42:07 GMT  
		Size: 93.6 MB (93580080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ec24994ba799cab97f0787dbc65a6d013d2f45a4517183cc832daaaa53806`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dea30f37956bb39717366343b060771f31e623af6aba2f86e813974d05eba8`  
		Last Modified: Thu, 03 Mar 2022 20:41:53 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb4afdb8e8e60145dd448944a446796ee594b6ed02750c6a778fccb13c06b1`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.0 MB (1003219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a9593299b6a3fca6dfff678b66e215e06cd1a736134c85128529fc6dda9c2d`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fab1112aff8eb07783792488c0daa5baab18c2fc7c75694c29d0614168a5fa8`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a0464741182bc14bbe33d2c884e74116f9378f9c9315c84a1883f3ce66bfd6`  
		Last Modified: Thu, 03 Mar 2022 20:41:58 GMT  
		Size: 113.7 MB (113727934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d555acc5e9ae7ecfa9e04b37670d8176b389240748fce73de64097a0f1278ccc`  
		Last Modified: Thu, 03 Mar 2022 20:41:51 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:100ee8d17ab9f711b3b560181ebe391c6382557a32c1e9ee08c049b184ebba69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224093072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33451a777c372afc9bcaafdd70428860e7ccdb93a3ecd2031be24a4be1e20af0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:58:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 20:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:01:30 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 20:01:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 20:02:12 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 20:02:12 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 20:02:13 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 20:02:14 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 20:02:15 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 20:02:16 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 20:02:17 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 20:02:18 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 20:02:19 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 20:02:20 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 20:02:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 20:02:23 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 20:02:25 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 20:02:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 20:02:33 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 20:02:34 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 20:02:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 20:02:37 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 20:02:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4317020d81860f4c7f3d0ba08b7d4fabb73c6d59fe81659e9f50c7041b7814b0`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 85.7 MB (85699022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fea459b86c67196991d4f93a562a0b91ec70a8dcd5303e790ef56c191e7f12`  
		Last Modified: Thu, 03 Mar 2022 20:04:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf4b0ff3d93dc9669374295f2a3930620b900c402ec5de48f74f3f33bfdb6d`  
		Last Modified: Thu, 03 Mar 2022 20:04:00 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eadd2b8e2a128a021b257f112c085ff9c5299a0d29fac4cbe8555e080ec929`  
		Last Modified: Thu, 03 Mar 2022 20:03:59 GMT  
		Size: 929.4 KB (929408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93477d9b74cbd8b18541de0f27af75437711c5b8665cbd853d4b88d792a99ee6`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81bab5f39f03ce3454d06174f99f7813f8df3c156cb15a72cac301c89b22072`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb3a0dc70b11a8867f2e9cee7a71b464310b86ba571928b03f73ef0676a427`  
		Last Modified: Thu, 03 Mar 2022 20:04:12 GMT  
		Size: 113.7 MB (113727904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11578b3399fa42d05b447eea7ca706fab624f17643b1bb859e73a0b640973d9a`  
		Last Modified: Thu, 03 Mar 2022 20:03:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:05ce851ed0917fbcee9e1d1b49c9a23c6221b5c18eb3e0f11b85b1b9b6780dac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231556682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bd10858d8a7259ed0ba4bdec36846fa328761fe17c81c765a4b45260cbf942`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:51:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 03 Mar 2022 21:02:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:02:36 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 03 Mar 2022 21:02:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 03 Mar 2022 21:03:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 03 Mar 2022 21:03:40 GMT
ARG BONITA_VERSION
# Thu, 03 Mar 2022 21:03:47 GMT
ARG BRANDING_VERSION
# Thu, 03 Mar 2022 21:03:53 GMT
ARG BONITA_SHA256
# Thu, 03 Mar 2022 21:03:56 GMT
ARG BASE_URL
# Thu, 03 Mar 2022 21:04:00 GMT
ARG BONITA_URL
# Thu, 03 Mar 2022 21:04:03 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 03 Mar 2022 21:04:05 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 03 Mar 2022 21:04:07 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 03 Mar 2022 21:04:11 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 21:04:13 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 03 Mar 2022 21:04:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 03 Mar 2022 21:04:21 GMT
RUN mkdir /opt/files
# Thu, 03 Mar 2022 21:04:24 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 03 Mar 2022 21:04:46 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 03 Mar 2022 21:04:50 GMT
ENV HTTP_API=false
# Thu, 03 Mar 2022 21:04:59 GMT
VOLUME [/opt/bonita]
# Thu, 03 Mar 2022 21:05:03 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 03 Mar 2022 21:05:12 GMT
EXPOSE 8080
# Thu, 03 Mar 2022 21:05:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd1018e1260c9561d82efdfffa45043f4f806857f701720527abdb33825ef5`  
		Last Modified: Thu, 03 Mar 2022 21:07:39 GMT  
		Size: 86.5 MB (86479352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d853e81df26f16338fa043e2217f6e2953bd306a840c659e2a20cc78e3f9ca`  
		Last Modified: Thu, 03 Mar 2022 21:07:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88e578facc7180f6af572c1d6359f7bb6f7c90673af246986625fd02ae5ff31`  
		Last Modified: Thu, 03 Mar 2022 21:07:23 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2ce469a139a35f0b02508b9d0c30a011692b391cf78e02f1978dc404251ff`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 904.2 KB (904233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7de6bd457bf881f1b38ecc7d675303a23659972ba041fdf9200d507b18435d`  
		Last Modified: Thu, 03 Mar 2022 21:07:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f15648cd335e09045b7843c9d0177c8993e95487e85335410976303b91e794`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f45df47bfc2bc197e45e411efdec1ceee73dc8edec98993904ec703f8d355ca`  
		Last Modified: Thu, 03 Mar 2022 21:07:31 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ad986b49367799f33c2b514c7e34e86748f83cd76d56c48cd77c7e55f2455c`  
		Last Modified: Thu, 03 Mar 2022 21:07:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
