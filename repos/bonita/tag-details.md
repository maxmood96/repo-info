<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2021.1`](#bonita20211)
-	[`bonita:2021.2`](#bonita20212)
-	[`bonita:2021.2-u0`](#bonita20212-u0)
-	[`bonita:2022.1`](#bonita20221)
-	[`bonita:2022.1-u0`](#bonita20221-u0)
-	[`bonita:7.11`](#bonita711)
-	[`bonita:7.11.4`](#bonita7114)
-	[`bonita:7.12`](#bonita712)
-	[`bonita:7.12.1`](#bonita7121)
-	[`bonita:7.13`](#bonita713)
-	[`bonita:7.13.0`](#bonita7130)
-	[`bonita:7.14`](#bonita714)
-	[`bonita:7.14.0`](#bonita7140)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2021.1`

```console
$ docker pull bonita@sha256:a93b06d83c07fdd22d914ecc443425145920e2d62e3c74d018ce4d79999a6bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:4ac754cc035059600a7192046e95be18bea425a9fd0ca4fe81706bb26926cc35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237372463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394162fea48e580bb2f465e10c9878a90ca1a59ec6a1b158fa32908bea9016f8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:22:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 22 Apr 2022 01:23:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 01:23:23 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 22 Apr 2022 01:23:23 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 22 Apr 2022 01:23:26 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 22 Apr 2022 01:23:26 GMT
ARG BONITA_VERSION
# Fri, 22 Apr 2022 01:23:43 GMT
ARG BRANDING_VERSION
# Fri, 22 Apr 2022 01:23:43 GMT
ARG BONITA_SHA256
# Fri, 22 Apr 2022 01:23:44 GMT
ARG BASE_URL
# Fri, 22 Apr 2022 01:23:44 GMT
ARG BONITA_URL
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 22 Apr 2022 01:23:44 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 22 Apr 2022 01:23:45 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 22 Apr 2022 01:23:45 GMT
RUN mkdir /opt/files
# Fri, 22 Apr 2022 01:23:45 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 22 Apr 2022 01:23:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 22 Apr 2022 01:23:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 22 Apr 2022 01:23:54 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 22 Apr 2022 01:23:54 GMT
VOLUME [/opt/bonita]
# Fri, 22 Apr 2022 01:23:54 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 22 Apr 2022 01:23:54 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 01:23:54 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66265528ccecf43b685e8cc6014acbda3604444f53c17f7d14a0ca4caad3b5fe`  
		Last Modified: Fri, 22 Apr 2022 01:25:10 GMT  
		Size: 93.7 MB (93659383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16c9efc2ba105a4c6440eeae034968f0a4403632dac03bfca64505847e96af`  
		Last Modified: Fri, 22 Apr 2022 01:24:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab5365759ee5f8e017f1e43a3183a827225526aad95bfe08d2ff0df2eef3320`  
		Last Modified: Fri, 22 Apr 2022 01:24:58 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd8fecd5bb01e2452c1a8086513d196c0a2702a0ed879dd6ce1504860b7ff30`  
		Last Modified: Fri, 22 Apr 2022 01:24:56 GMT  
		Size: 577.0 KB (576952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03889de4a415a8a95d2384cb03675cba1acd8c169d3c501017b995ceba9c623e`  
		Last Modified: Fri, 22 Apr 2022 01:25:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7413ea3a75cf10e37a77cbd15ca87e744a91f5a0323d771e74a3226378e306`  
		Last Modified: Fri, 22 Apr 2022 01:25:20 GMT  
		Size: 6.9 KB (6942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1d6cdf8f58fe752dfc13fdc708024416b564711d822a926bc96046822d63a0`  
		Last Modified: Fri, 22 Apr 2022 01:25:25 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c730a101a1ffb1bf94a0ea76b7863b678ce7d2610f1a5499021357167ef16443`  
		Last Modified: Fri, 22 Apr 2022 01:25:20 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:f9ffffd1db585db1ded556470d59c594a6af2706329d79c4a5e19e92fba88250
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226465666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812a03713b8021c286fd182ced0166ed2be62cfad6c26c1a622f0372b4c0630e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:58:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 22:59:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 22:59:14 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 22:59:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 05 Apr 2022 22:59:19 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 05 Apr 2022 22:59:19 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 23:00:02 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 23:00:03 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 23:00:04 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 23:00:05 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 23:00:06 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 05 Apr 2022 23:00:07 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 05 Apr 2022 23:00:08 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 05 Apr 2022 23:00:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 05 Apr 2022 23:00:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 23:00:11 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 05 Apr 2022 23:00:12 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 05 Apr 2022 23:00:13 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 23:00:15 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 05 Apr 2022 23:00:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 05 Apr 2022 23:00:32 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 05 Apr 2022 23:00:33 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 05 Apr 2022 23:00:34 GMT
VOLUME [/opt/bonita]
# Tue, 05 Apr 2022 23:00:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 05 Apr 2022 23:00:36 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 23:00:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c33ecc03ac3ec45c755fe7c9affd84d05cd4c5aeff7430264708c5c324e46a`  
		Last Modified: Tue, 05 Apr 2022 23:02:34 GMT  
		Size: 85.8 MB (85761773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd208172af52c2410b7046f45ab089b878466337ed2bd5b3a79e50f04133270a`  
		Last Modified: Tue, 05 Apr 2022 23:02:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9b10b9b4ad0ba30bcd3c3518782f025923f40643795a0b21b2361b2505c5a6`  
		Last Modified: Tue, 05 Apr 2022 23:02:22 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db00845da6fa4fc633f85ebfefd4635aaf4774b5e764ef56cf42a730fd4269a`  
		Last Modified: Tue, 05 Apr 2022 23:02:20 GMT  
		Size: 546.9 KB (546931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9efd36fb83002aa96ebbed0d93fd192ce4b59c665b95ff9baa0ad7e3b8391e`  
		Last Modified: Tue, 05 Apr 2022 23:02:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3f9d3d8bcb63c7a643e3b8894fb6ee4debf999158718d5d5df2f9a56e0de62`  
		Last Modified: Tue, 05 Apr 2022 23:02:44 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea233d274933c0623185dd20805f5a4ab98c801653213018efc760522ef9296`  
		Last Modified: Tue, 05 Apr 2022 23:02:56 GMT  
		Size: 116.4 MB (116415400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45b5439fff196f2045afe202e70b58b492eebce3e6c4f7609081d226dd0a66f`  
		Last Modified: Tue, 05 Apr 2022 23:02:44 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:3da6e391662ee228d240886065907d6648dca1e3135e0ffbe2a030c6db60e1e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233968534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e500fbb269dcc1826f931278272919705ddfa8333bd87b9c584137ace4761`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 03:57:28 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 06 Apr 2022 04:00:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:00:26 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 06 Apr 2022 04:00:39 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 06 Apr 2022 04:00:52 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 06 Apr 2022 04:00:56 GMT
ARG BONITA_VERSION
# Wed, 06 Apr 2022 04:03:05 GMT
ARG BRANDING_VERSION
# Wed, 06 Apr 2022 04:03:12 GMT
ARG BONITA_SHA256
# Wed, 06 Apr 2022 04:03:14 GMT
ARG BASE_URL
# Wed, 06 Apr 2022 04:03:19 GMT
ARG BONITA_URL
# Wed, 06 Apr 2022 04:03:22 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 06 Apr 2022 04:03:26 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 06 Apr 2022 04:03:31 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 06 Apr 2022 04:03:38 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 06 Apr 2022 04:03:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 06 Apr 2022 04:03:50 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 06 Apr 2022 04:03:59 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 06 Apr 2022 04:04:05 GMT
RUN mkdir /opt/files
# Wed, 06 Apr 2022 04:04:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 06 Apr 2022 04:04:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 06 Apr 2022 04:04:28 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 06 Apr 2022 04:04:38 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 06 Apr 2022 04:04:42 GMT
VOLUME [/opt/bonita]
# Wed, 06 Apr 2022 04:04:45 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 06 Apr 2022 04:04:48 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 04:04:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3797140b1f3932691017aa275137964432dbeff45bcc6f8a8cfed91439f9eb8c`  
		Last Modified: Wed, 06 Apr 2022 04:11:09 GMT  
		Size: 86.6 MB (86557112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bcdf9f7a07427bac5eb4b0abb9524330d19ae7739f209e225c558657e3d4cd`  
		Last Modified: Wed, 06 Apr 2022 04:10:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedb609f92c0b35515c47a526be80f7c51dfbcbc2e2b104ecc0c0418461d3911`  
		Last Modified: Wed, 06 Apr 2022 04:10:54 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a98badb926d158087565b1dc5bc89334e25cf502a7fe73edaea153ac4cd066`  
		Last Modified: Wed, 06 Apr 2022 04:10:52 GMT  
		Size: 546.7 KB (546744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abca8c880793aa57ea79c8b5c52ea0fe3fb77c4f739bbff396c2e81234670434`  
		Last Modified: Wed, 06 Apr 2022 04:11:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca00e5906707c86c965a1bf6dcaf9240a72a9d462516be71e4506b1dc4a5c38`  
		Last Modified: Wed, 06 Apr 2022 04:11:23 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c537633c59a2e9dffaafc4fad2d5b2a64cd706730b458f3d48f858db0d366b38`  
		Last Modified: Wed, 06 Apr 2022 04:11:32 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3a364bfb6112c878a6da2b3add53147a9abf1acf561989f011a4565058b9e`  
		Last Modified: Wed, 06 Apr 2022 04:11:23 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:88f76d905825b6adef4ca430901bcf99138da7c4ff7be8b59fc6e9ad6a398ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:5333d829c04a1259d09976844335b68efc3204ce9e803b86b278ee7c3576ef6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235106399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175bba281ea3436183dbd367a8b7b0818e75bc71614d6d93312ba200b5ec058e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:22:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 22 Apr 2022 01:24:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 01:24:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 22 Apr 2022 01:24:18 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 22 Apr 2022 01:24:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_VERSION
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BRANDING_VERSION
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_SHA256
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BASE_URL
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_URL
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 22 Apr 2022 01:24:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 22 Apr 2022 01:24:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 22 Apr 2022 01:24:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 22 Apr 2022 01:24:22 GMT
RUN mkdir /opt/files
# Fri, 22 Apr 2022 01:24:22 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 22 Apr 2022 01:24:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 22 Apr 2022 01:24:31 GMT
ENV HTTP_API=false
# Fri, 22 Apr 2022 01:24:32 GMT
VOLUME [/opt/bonita]
# Fri, 22 Apr 2022 01:24:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 22 Apr 2022 01:24:32 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 01:24:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a6bfdda70147d18bf20d9f200b0e89f9bf12aaf4163a53aec413a1fbac49db`  
		Last Modified: Fri, 22 Apr 2022 01:25:53 GMT  
		Size: 93.7 MB (93658186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0180a51e6fbc6fc70250b21e2e0c058314e2a1783da77cfbf5a6b4e8fddc031f`  
		Last Modified: Fri, 22 Apr 2022 01:25:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30cced3fa023cbba53f6a23f693c3a561d545c4877416403e79d840933093d6`  
		Last Modified: Fri, 22 Apr 2022 01:25:41 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068bb8acea2c65c3874287c6d855fce18e57bb7f1f690a6059bfd20138005a3d`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 1.0 MB (1003215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bde2f1d36d17d2dfbc1723f84055675909c30ceb780a024a5a1414980795fe`  
		Last Modified: Fri, 22 Apr 2022 01:25:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe3a412ac8d0dfce451f851d783a4ed81040f60be605a9ecfe48272c6e11a1a`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767fb402b4d4e27d1d99a8d9275e6e09aaacac06459d626f92518dfb2a070bb4`  
		Last Modified: Fri, 22 Apr 2022 01:25:44 GMT  
		Size: 113.7 MB (113727920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80904747d961983d36afe3fc428ee94bbfb12d2f98926694505ad9b6980b86e`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:994746b77042bb103ae89f29a0d68042bc74633e9c2fae10e5c71810cf90ef78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbf266641b2d0fdb4823734476faaccd1edabce516ddc2ba9d9ff5d5054f284`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:58:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 23:01:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:01:09 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 23:01:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 05 Apr 2022 23:01:14 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 05 Apr 2022 23:01:14 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 23:01:15 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 23:01:16 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 23:01:17 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 23:01:18 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 23:01:19 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 05 Apr 2022 23:01:20 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 05 Apr 2022 23:01:21 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 05 Apr 2022 23:01:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 05 Apr 2022 23:01:23 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 23:01:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 05 Apr 2022 23:01:25 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 23:01:27 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 05 Apr 2022 23:01:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 05 Apr 2022 23:01:37 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 23:01:39 GMT
VOLUME [/opt/bonita]
# Tue, 05 Apr 2022 23:01:40 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 05 Apr 2022 23:01:40 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 23:01:41 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a342eca32d8c7efdcc6518a6a024c82a904b40b2299718265db4f700b611f`  
		Last Modified: Tue, 05 Apr 2022 23:03:24 GMT  
		Size: 85.8 MB (85761767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6773dd32221fab5034b6afb8252d9ddb02fd6967ed56e534598ac4d2daaa9a82`  
		Last Modified: Tue, 05 Apr 2022 23:03:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80d1794db296ab170d35b2fa0cb8a5a33bd169cb994a1a36d625024401e2f9`  
		Last Modified: Tue, 05 Apr 2022 23:03:13 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d39709d3a66d0bbb19d4f86c2795a02d679145064d5512dfd94db88b9aea032`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 929.4 KB (929406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cbb8c35dfc0a421349a18295b22a952b19fd917d51d96e0696f793f96294f0`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc72ca6f6cffbcb3df92677851d567dccf1ced29efb7ad910e78f212ee5ac93`  
		Last Modified: Tue, 05 Apr 2022 23:03:10 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b11332953363ba30aa8af0f6cf77f67f7e6f089403c0394425b0c827e02b12`  
		Last Modified: Tue, 05 Apr 2022 23:03:19 GMT  
		Size: 113.7 MB (113727849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385f85a63a52a608a0746be33ba569cb6efd10095d3a2de638d0b22e4cbaf846`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:91668825b7a481026185e944d94ea679de83c532e02e5e70afc6b45ba4b6b2aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebaa35ead7bbad7dd4241931df4b2b8edfbfdb3bef58ab88435a18fb6384de3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 03:57:28 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 06 Apr 2022 04:07:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:08:07 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 06 Apr 2022 04:08:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 06 Apr 2022 04:08:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 06 Apr 2022 04:08:35 GMT
ARG BONITA_VERSION
# Wed, 06 Apr 2022 04:08:37 GMT
ARG BRANDING_VERSION
# Wed, 06 Apr 2022 04:08:40 GMT
ARG BONITA_SHA256
# Wed, 06 Apr 2022 04:08:45 GMT
ARG BASE_URL
# Wed, 06 Apr 2022 04:08:48 GMT
ARG BONITA_URL
# Wed, 06 Apr 2022 04:08:52 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 06 Apr 2022 04:08:55 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 06 Apr 2022 04:08:57 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 06 Apr 2022 04:09:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 06 Apr 2022 04:09:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 06 Apr 2022 04:09:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 06 Apr 2022 04:09:14 GMT
RUN mkdir /opt/files
# Wed, 06 Apr 2022 04:09:17 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 06 Apr 2022 04:09:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 06 Apr 2022 04:09:43 GMT
ENV HTTP_API=false
# Wed, 06 Apr 2022 04:09:48 GMT
VOLUME [/opt/bonita]
# Wed, 06 Apr 2022 04:09:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 06 Apr 2022 04:09:54 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 04:09:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1faaa0ff16cf6a07daa39cb3b0b600a672ed410aa0655a3d47818258f587b49`  
		Last Modified: Wed, 06 Apr 2022 04:12:06 GMT  
		Size: 86.6 MB (86556858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a502123895652556962416c26c4f1f5b36ae9e4f6aae3cc5dadc6aca8c68a20`  
		Last Modified: Wed, 06 Apr 2022 04:11:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf13516d8ca4b08100d618913f86648c25b7ccb2de2906ece3073c1183287812`  
		Last Modified: Wed, 06 Apr 2022 04:11:50 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f588c67fbe00f626d24d6fafa4c35622614c75bb361fd075ed1504ffbef4a7`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 904.2 KB (904213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4473c3d5fdb46b6c1425eb08f4b66ad3cf9e934116b6198ea30fbd15fee96`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75681f610194b1b6f355b0b62e17f1a1b944e64c60811d20f7389af29e5fb95`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4929458e28211f39954235d13e2970a1046415afd41578ffb9cb9db83466070b`  
		Last Modified: Wed, 06 Apr 2022 04:11:58 GMT  
		Size: 113.7 MB (113727924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8271d2c547727e51acca08b86e2ff4e026b400487783cb68d63a30913032f4`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:88f76d905825b6adef4ca430901bcf99138da7c4ff7be8b59fc6e9ad6a398ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:5333d829c04a1259d09976844335b68efc3204ce9e803b86b278ee7c3576ef6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235106399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175bba281ea3436183dbd367a8b7b0818e75bc71614d6d93312ba200b5ec058e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:22:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 22 Apr 2022 01:24:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 01:24:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 22 Apr 2022 01:24:18 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 22 Apr 2022 01:24:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_VERSION
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BRANDING_VERSION
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_SHA256
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BASE_URL
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_URL
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 22 Apr 2022 01:24:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 22 Apr 2022 01:24:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 22 Apr 2022 01:24:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 22 Apr 2022 01:24:22 GMT
RUN mkdir /opt/files
# Fri, 22 Apr 2022 01:24:22 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 22 Apr 2022 01:24:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 22 Apr 2022 01:24:31 GMT
ENV HTTP_API=false
# Fri, 22 Apr 2022 01:24:32 GMT
VOLUME [/opt/bonita]
# Fri, 22 Apr 2022 01:24:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 22 Apr 2022 01:24:32 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 01:24:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a6bfdda70147d18bf20d9f200b0e89f9bf12aaf4163a53aec413a1fbac49db`  
		Last Modified: Fri, 22 Apr 2022 01:25:53 GMT  
		Size: 93.7 MB (93658186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0180a51e6fbc6fc70250b21e2e0c058314e2a1783da77cfbf5a6b4e8fddc031f`  
		Last Modified: Fri, 22 Apr 2022 01:25:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30cced3fa023cbba53f6a23f693c3a561d545c4877416403e79d840933093d6`  
		Last Modified: Fri, 22 Apr 2022 01:25:41 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068bb8acea2c65c3874287c6d855fce18e57bb7f1f690a6059bfd20138005a3d`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 1.0 MB (1003215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bde2f1d36d17d2dfbc1723f84055675909c30ceb780a024a5a1414980795fe`  
		Last Modified: Fri, 22 Apr 2022 01:25:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe3a412ac8d0dfce451f851d783a4ed81040f60be605a9ecfe48272c6e11a1a`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767fb402b4d4e27d1d99a8d9275e6e09aaacac06459d626f92518dfb2a070bb4`  
		Last Modified: Fri, 22 Apr 2022 01:25:44 GMT  
		Size: 113.7 MB (113727920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80904747d961983d36afe3fc428ee94bbfb12d2f98926694505ad9b6980b86e`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:994746b77042bb103ae89f29a0d68042bc74633e9c2fae10e5c71810cf90ef78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbf266641b2d0fdb4823734476faaccd1edabce516ddc2ba9d9ff5d5054f284`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:58:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 23:01:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:01:09 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 23:01:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 05 Apr 2022 23:01:14 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 05 Apr 2022 23:01:14 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 23:01:15 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 23:01:16 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 23:01:17 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 23:01:18 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 23:01:19 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 05 Apr 2022 23:01:20 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 05 Apr 2022 23:01:21 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 05 Apr 2022 23:01:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 05 Apr 2022 23:01:23 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 23:01:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 05 Apr 2022 23:01:25 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 23:01:27 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 05 Apr 2022 23:01:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 05 Apr 2022 23:01:37 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 23:01:39 GMT
VOLUME [/opt/bonita]
# Tue, 05 Apr 2022 23:01:40 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 05 Apr 2022 23:01:40 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 23:01:41 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a342eca32d8c7efdcc6518a6a024c82a904b40b2299718265db4f700b611f`  
		Last Modified: Tue, 05 Apr 2022 23:03:24 GMT  
		Size: 85.8 MB (85761767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6773dd32221fab5034b6afb8252d9ddb02fd6967ed56e534598ac4d2daaa9a82`  
		Last Modified: Tue, 05 Apr 2022 23:03:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80d1794db296ab170d35b2fa0cb8a5a33bd169cb994a1a36d625024401e2f9`  
		Last Modified: Tue, 05 Apr 2022 23:03:13 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d39709d3a66d0bbb19d4f86c2795a02d679145064d5512dfd94db88b9aea032`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 929.4 KB (929406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cbb8c35dfc0a421349a18295b22a952b19fd917d51d96e0696f793f96294f0`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc72ca6f6cffbcb3df92677851d567dccf1ced29efb7ad910e78f212ee5ac93`  
		Last Modified: Tue, 05 Apr 2022 23:03:10 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b11332953363ba30aa8af0f6cf77f67f7e6f089403c0394425b0c827e02b12`  
		Last Modified: Tue, 05 Apr 2022 23:03:19 GMT  
		Size: 113.7 MB (113727849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385f85a63a52a608a0746be33ba569cb6efd10095d3a2de638d0b22e4cbaf846`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:91668825b7a481026185e944d94ea679de83c532e02e5e70afc6b45ba4b6b2aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebaa35ead7bbad7dd4241931df4b2b8edfbfdb3bef58ab88435a18fb6384de3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 03:57:28 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 06 Apr 2022 04:07:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:08:07 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 06 Apr 2022 04:08:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 06 Apr 2022 04:08:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 06 Apr 2022 04:08:35 GMT
ARG BONITA_VERSION
# Wed, 06 Apr 2022 04:08:37 GMT
ARG BRANDING_VERSION
# Wed, 06 Apr 2022 04:08:40 GMT
ARG BONITA_SHA256
# Wed, 06 Apr 2022 04:08:45 GMT
ARG BASE_URL
# Wed, 06 Apr 2022 04:08:48 GMT
ARG BONITA_URL
# Wed, 06 Apr 2022 04:08:52 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 06 Apr 2022 04:08:55 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 06 Apr 2022 04:08:57 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 06 Apr 2022 04:09:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 06 Apr 2022 04:09:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 06 Apr 2022 04:09:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 06 Apr 2022 04:09:14 GMT
RUN mkdir /opt/files
# Wed, 06 Apr 2022 04:09:17 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 06 Apr 2022 04:09:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 06 Apr 2022 04:09:43 GMT
ENV HTTP_API=false
# Wed, 06 Apr 2022 04:09:48 GMT
VOLUME [/opt/bonita]
# Wed, 06 Apr 2022 04:09:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 06 Apr 2022 04:09:54 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 04:09:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1faaa0ff16cf6a07daa39cb3b0b600a672ed410aa0655a3d47818258f587b49`  
		Last Modified: Wed, 06 Apr 2022 04:12:06 GMT  
		Size: 86.6 MB (86556858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a502123895652556962416c26c4f1f5b36ae9e4f6aae3cc5dadc6aca8c68a20`  
		Last Modified: Wed, 06 Apr 2022 04:11:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf13516d8ca4b08100d618913f86648c25b7ccb2de2906ece3073c1183287812`  
		Last Modified: Wed, 06 Apr 2022 04:11:50 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f588c67fbe00f626d24d6fafa4c35622614c75bb361fd075ed1504ffbef4a7`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 904.2 KB (904213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4473c3d5fdb46b6c1425eb08f4b66ad3cf9e934116b6198ea30fbd15fee96`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75681f610194b1b6f355b0b62e17f1a1b944e64c60811d20f7389af29e5fb95`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4929458e28211f39954235d13e2970a1046415afd41578ffb9cb9db83466070b`  
		Last Modified: Wed, 06 Apr 2022 04:11:58 GMT  
		Size: 113.7 MB (113727924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8271d2c547727e51acca08b86e2ff4e026b400487783cb68d63a30913032f4`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1`

```console
$ docker pull bonita@sha256:9bd37caef5943cf2cdc2a20993002c2d8d794f6f549da01f08ac9fdc56d2ae2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1` - linux; amd64

```console
$ docker pull bonita@sha256:aa6c404694792455f659ab29b685840a58847a82ee8d6b933510ab9b8d415e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791a1d923d653fa2c3fc2640e7509051adf42a471ba281268d753580e1da5f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:23:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 04:23:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 04:23:38 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 04:23:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 04:23:39 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 04:23:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:40 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 04:23:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 04:23:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 04:23:48 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 04:23:49 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 04:23:49 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 04:23:49 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 04:23:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 04:23:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff37705a3721b6f0fa369c96374cf9da30cff49af0d8000271ef496b3a770df`  
		Last Modified: Tue, 05 Apr 2022 04:24:23 GMT  
		Size: 60.7 MB (60744505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f66c34cc10d0cb3a031ef3da4ba3f1bd013bcc964d4956c60fad86f44fe69`  
		Last Modified: Tue, 05 Apr 2022 04:24:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578f03d3de8ca415ec7f424f8e565acd05fed61f7ae257c04a206815af3329f`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217417d523fc2999c4b2897458c8186aaae7637ca11cffcf678f5a94676243c3`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bafdba13f86b25d0530d42b1945be474d808e2e57c54eb92525278fd97b4066`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7700ffe2df31bc40779a5addc28e3643352992303bc5cd5013f722caeea46b`  
		Last Modified: Tue, 05 Apr 2022 04:24:20 GMT  
		Size: 116.7 MB (116690800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f64f512c1d336d8e3ad42228cc6f701c2f9ef296cccb6001395170ba33d88`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ec277986357bc1492ec4256aeb59f9509b5206166178468fae72d7b396672ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7da5778516cbbaa93e6b5f1f1812601e1ea647ac7f864ea7770f27872c6bf2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:09:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 03:09:35 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 03:09:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 03:09:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 03:09:37 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 03:09:38 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 03:09:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 03:09:40 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 03:09:41 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 03:09:42 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 03:09:43 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 03:09:44 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 03:09:45 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 03:09:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:48 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 03:09:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 03:09:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 03:09:58 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 03:09:59 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 03:10:00 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 03:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 03:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 03:10:03 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 03:10:04 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 03:10:05 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 03:10:06 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 03:10:07 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 03:10:08 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 03:10:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 03:10:10 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 03:10:12 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 03:10:12 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 03:10:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 03:10:14 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f256ad0fc5640d4ad6542e63ff033094b79f2158b7b837af471110ea8a336`  
		Last Modified: Tue, 05 Apr 2022 03:11:08 GMT  
		Size: 60.1 MB (60067315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f94323a629942950a0ffa4ebd9b9a9a67e2e99450c1b63b7caa029bb6fbab5`  
		Last Modified: Tue, 05 Apr 2022 03:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6976ee94f88624b6444d82e171da5997a9fc114743925400901581ea08c58`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5aabbb25b6ba30936e48e8d131ebfb29068a96236f7ce6e56f8aea4faafaf`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ba33b8f8be7b90a8de59a31f336886c4e754bd8846e3019ee792422b0c930`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 3.0 KB (3000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb65a72bf0159fbfb5326ef80a1e211664490a96659378c1d97748689b176279`  
		Last Modified: Tue, 05 Apr 2022 03:11:05 GMT  
		Size: 116.7 MB (116688761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b61e2452bca6bb834b08988d9199d49b4c4ffd3228c57b794b855215c36116`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:a8b99264c74f1637a78eb549f8e83bee8f0f2146850d2757e4d483465a901317
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176075045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766bd47323049c15860a8cea6025a09aab1552c1868c15db5ef57c14d7cc9633`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:02:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 09:02:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 09:02:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 09:03:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 09:03:03 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:03:05 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 09:03:09 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:03:12 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:03:16 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:03:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 09:03:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 09:03:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 09:03:31 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:03:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:46 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:03:49 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 09:04:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 09:04:13 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 09:04:16 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 09:04:20 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 09:04:24 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 09:04:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 09:04:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 09:04:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 09:04:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 09:04:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 09:04:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 09:04:50 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 09:04:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 09:04:59 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 09:05:01 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 09:05:03 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 09:05:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 09:05:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434586e006643fe98fc4f4804ae9fc2bda4db5b77b98a9fd444e497dfe6b0d0`  
		Last Modified: Tue, 05 Apr 2022 09:06:41 GMT  
		Size: 56.6 MB (56562945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edcf9db5a1b38af5bb9fdf73e674526ec2ea289819852645d9d188fad87bf21`  
		Last Modified: Tue, 05 Apr 2022 09:06:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c2e63c2fbfc1abb8e0d67e64b0f60853a2071bc30215f0a253be92cb274c6`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4adf978bd9de05949fabf35a650d95b209d0cf397d6a01c098b30cc4072089`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144701e366b871fd0167a7150ebd9e22e946ad67a354ed2ec7cb3871ee76bb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847d35ce919fdc67b9945f9238ecff157ddbabd7d47bcfd9897bfc32b81e3c5`  
		Last Modified: Tue, 05 Apr 2022 09:06:38 GMT  
		Size: 116.7 MB (116690887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341eef26fc26324a7ea91c42a1be66b6b8a7d8230c1df8986f8c6e22e2fa38d4`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 5.4 KB (5429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1-u0`

```console
$ docker pull bonita@sha256:9bd37caef5943cf2cdc2a20993002c2d8d794f6f549da01f08ac9fdc56d2ae2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:aa6c404694792455f659ab29b685840a58847a82ee8d6b933510ab9b8d415e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791a1d923d653fa2c3fc2640e7509051adf42a471ba281268d753580e1da5f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:23:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 04:23:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 04:23:38 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 04:23:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 04:23:39 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 04:23:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:40 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 04:23:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 04:23:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 04:23:48 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 04:23:49 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 04:23:49 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 04:23:49 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 04:23:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 04:23:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff37705a3721b6f0fa369c96374cf9da30cff49af0d8000271ef496b3a770df`  
		Last Modified: Tue, 05 Apr 2022 04:24:23 GMT  
		Size: 60.7 MB (60744505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f66c34cc10d0cb3a031ef3da4ba3f1bd013bcc964d4956c60fad86f44fe69`  
		Last Modified: Tue, 05 Apr 2022 04:24:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578f03d3de8ca415ec7f424f8e565acd05fed61f7ae257c04a206815af3329f`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217417d523fc2999c4b2897458c8186aaae7637ca11cffcf678f5a94676243c3`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bafdba13f86b25d0530d42b1945be474d808e2e57c54eb92525278fd97b4066`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7700ffe2df31bc40779a5addc28e3643352992303bc5cd5013f722caeea46b`  
		Last Modified: Tue, 05 Apr 2022 04:24:20 GMT  
		Size: 116.7 MB (116690800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f64f512c1d336d8e3ad42228cc6f701c2f9ef296cccb6001395170ba33d88`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ec277986357bc1492ec4256aeb59f9509b5206166178468fae72d7b396672ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7da5778516cbbaa93e6b5f1f1812601e1ea647ac7f864ea7770f27872c6bf2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:09:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 03:09:35 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 03:09:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 03:09:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 03:09:37 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 03:09:38 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 03:09:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 03:09:40 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 03:09:41 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 03:09:42 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 03:09:43 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 03:09:44 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 03:09:45 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 03:09:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:48 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 03:09:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 03:09:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 03:09:58 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 03:09:59 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 03:10:00 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 03:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 03:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 03:10:03 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 03:10:04 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 03:10:05 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 03:10:06 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 03:10:07 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 03:10:08 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 03:10:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 03:10:10 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 03:10:12 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 03:10:12 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 03:10:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 03:10:14 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f256ad0fc5640d4ad6542e63ff033094b79f2158b7b837af471110ea8a336`  
		Last Modified: Tue, 05 Apr 2022 03:11:08 GMT  
		Size: 60.1 MB (60067315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f94323a629942950a0ffa4ebd9b9a9a67e2e99450c1b63b7caa029bb6fbab5`  
		Last Modified: Tue, 05 Apr 2022 03:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6976ee94f88624b6444d82e171da5997a9fc114743925400901581ea08c58`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5aabbb25b6ba30936e48e8d131ebfb29068a96236f7ce6e56f8aea4faafaf`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ba33b8f8be7b90a8de59a31f336886c4e754bd8846e3019ee792422b0c930`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 3.0 KB (3000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb65a72bf0159fbfb5326ef80a1e211664490a96659378c1d97748689b176279`  
		Last Modified: Tue, 05 Apr 2022 03:11:05 GMT  
		Size: 116.7 MB (116688761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b61e2452bca6bb834b08988d9199d49b4c4ffd3228c57b794b855215c36116`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:a8b99264c74f1637a78eb549f8e83bee8f0f2146850d2757e4d483465a901317
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176075045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766bd47323049c15860a8cea6025a09aab1552c1868c15db5ef57c14d7cc9633`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:02:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 09:02:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 09:02:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 09:03:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 09:03:03 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:03:05 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 09:03:09 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:03:12 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:03:16 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:03:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 09:03:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 09:03:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 09:03:31 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:03:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:46 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:03:49 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 09:04:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 09:04:13 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 09:04:16 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 09:04:20 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 09:04:24 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 09:04:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 09:04:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 09:04:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 09:04:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 09:04:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 09:04:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 09:04:50 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 09:04:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 09:04:59 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 09:05:01 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 09:05:03 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 09:05:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 09:05:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434586e006643fe98fc4f4804ae9fc2bda4db5b77b98a9fd444e497dfe6b0d0`  
		Last Modified: Tue, 05 Apr 2022 09:06:41 GMT  
		Size: 56.6 MB (56562945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edcf9db5a1b38af5bb9fdf73e674526ec2ea289819852645d9d188fad87bf21`  
		Last Modified: Tue, 05 Apr 2022 09:06:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c2e63c2fbfc1abb8e0d67e64b0f60853a2071bc30215f0a253be92cb274c6`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4adf978bd9de05949fabf35a650d95b209d0cf397d6a01c098b30cc4072089`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144701e366b871fd0167a7150ebd9e22e946ad67a354ed2ec7cb3871ee76bb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847d35ce919fdc67b9945f9238ecff157ddbabd7d47bcfd9897bfc32b81e3c5`  
		Last Modified: Tue, 05 Apr 2022 09:06:38 GMT  
		Size: 116.7 MB (116690887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341eef26fc26324a7ea91c42a1be66b6b8a7d8230c1df8986f8c6e22e2fa38d4`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 5.4 KB (5429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:e8033303eac4a43ad8826b4824fc77609e2b3175eb6167331883b5b1dd4eb0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:b61b0cead340f24819f17b5df2873f398551e673689a5b43413f983974f76a1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234304839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2552beba9b4b8ee48aaf246e0d16fcf15b8db7256902743824268df7ebd2c0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:22:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 22 Apr 2022 01:23:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 01:23:23 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 22 Apr 2022 01:23:23 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 22 Apr 2022 01:23:26 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 22 Apr 2022 01:23:26 GMT
ARG BONITA_VERSION
# Fri, 22 Apr 2022 01:23:26 GMT
ARG BONITA_SHA256
# Fri, 22 Apr 2022 01:23:26 GMT
ARG BASE_URL
# Fri, 22 Apr 2022 01:23:26 GMT
ARG BONITA_URL
# Fri, 22 Apr 2022 01:23:26 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 22 Apr 2022 01:23:26 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 22 Apr 2022 01:23:26 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 22 Apr 2022 01:23:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 22 Apr 2022 01:23:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 22 Apr 2022 01:23:27 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 22 Apr 2022 01:23:28 GMT
RUN mkdir /opt/files
# Fri, 22 Apr 2022 01:23:28 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 22 Apr 2022 01:23:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 22 Apr 2022 01:23:35 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 22 Apr 2022 01:23:37 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 22 Apr 2022 01:23:37 GMT
VOLUME [/opt/bonita]
# Fri, 22 Apr 2022 01:23:37 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 22 Apr 2022 01:23:37 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 01:23:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66265528ccecf43b685e8cc6014acbda3604444f53c17f7d14a0ca4caad3b5fe`  
		Last Modified: Fri, 22 Apr 2022 01:25:10 GMT  
		Size: 93.7 MB (93659383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16c9efc2ba105a4c6440eeae034968f0a4403632dac03bfca64505847e96af`  
		Last Modified: Fri, 22 Apr 2022 01:24:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab5365759ee5f8e017f1e43a3183a827225526aad95bfe08d2ff0df2eef3320`  
		Last Modified: Fri, 22 Apr 2022 01:24:58 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd8fecd5bb01e2452c1a8086513d196c0a2702a0ed879dd6ce1504860b7ff30`  
		Last Modified: Fri, 22 Apr 2022 01:24:56 GMT  
		Size: 577.0 KB (576952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c6995b8a0687d00b28a53b523ca1323383676f0db2cdc6bd1435741bf0ae62`  
		Last Modified: Fri, 22 Apr 2022 01:24:56 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef1b403272ff10579b70ec4b3a3960c3c237eea0f2d5b392b047cb8a7bcfb8e`  
		Last Modified: Fri, 22 Apr 2022 01:24:56 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa108a1a4ba0d6ba78210b69ddbea05f66be0867355c7a90b730cc68e65b556`  
		Last Modified: Fri, 22 Apr 2022 01:25:02 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d6a223f21d1dbd101107ccf6404405c40a8642fccf3029235650b68a631ac4`  
		Last Modified: Fri, 22 Apr 2022 01:24:56 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:64e2c8182eca87681781cfc05326529ff746e2f41e040c68ab1d43c1071daa41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223398036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97240d730430aabd0b7e02fc6eebfbcf1888cacc0f4e9821b2d343cfae35434e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:58:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 22:59:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 22:59:14 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 22:59:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 05 Apr 2022 22:59:19 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 05 Apr 2022 22:59:19 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 22:59:20 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 22:59:21 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 22:59:22 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 22:59:23 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 05 Apr 2022 22:59:24 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 05 Apr 2022 22:59:25 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 05 Apr 2022 22:59:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 22:59:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 05 Apr 2022 22:59:28 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 05 Apr 2022 22:59:29 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 22:59:31 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 05 Apr 2022 22:59:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 05 Apr 2022 22:59:42 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 05 Apr 2022 22:59:43 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 05 Apr 2022 22:59:44 GMT
VOLUME [/opt/bonita]
# Tue, 05 Apr 2022 22:59:46 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 05 Apr 2022 22:59:46 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 22:59:47 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c33ecc03ac3ec45c755fe7c9affd84d05cd4c5aeff7430264708c5c324e46a`  
		Last Modified: Tue, 05 Apr 2022 23:02:34 GMT  
		Size: 85.8 MB (85761773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd208172af52c2410b7046f45ab089b878466337ed2bd5b3a79e50f04133270a`  
		Last Modified: Tue, 05 Apr 2022 23:02:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9b10b9b4ad0ba30bcd3c3518782f025923f40643795a0b21b2361b2505c5a6`  
		Last Modified: Tue, 05 Apr 2022 23:02:22 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db00845da6fa4fc633f85ebfefd4635aaf4774b5e764ef56cf42a730fd4269a`  
		Last Modified: Tue, 05 Apr 2022 23:02:20 GMT  
		Size: 546.9 KB (546931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38b1b99d036d17d3c955787d065351dc6ea9634784be42ad6574b91317bf1c9`  
		Last Modified: Tue, 05 Apr 2022 23:02:20 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5916f250dbee91f448a6c49909b61157b69b2c11e85c1fb374900e564658778f`  
		Last Modified: Tue, 05 Apr 2022 23:02:20 GMT  
		Size: 6.9 KB (6865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379b59a7ad10f52210fc7067b74154cc7fc4c78d9d57d3378e676bc627a77b97`  
		Last Modified: Tue, 05 Apr 2022 23:02:30 GMT  
		Size: 113.3 MB (113347827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa3653e6a86f952ee809b55dbaf1a83d069350ba21b63e5b80c7a36fe7be84f`  
		Last Modified: Tue, 05 Apr 2022 23:02:20 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:f17ecfb397b1df44a8fafb43244150c42268296ac1e5aa8609459aafc518c904
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230900908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcf8df8d27f1cbd2b22a642e4e49a3d32398d65a5bd0fa8c666e418d06cfdd5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 03:57:28 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 06 Apr 2022 04:00:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:00:26 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 06 Apr 2022 04:00:39 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 06 Apr 2022 04:00:52 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 06 Apr 2022 04:00:56 GMT
ARG BONITA_VERSION
# Wed, 06 Apr 2022 04:00:59 GMT
ARG BONITA_SHA256
# Wed, 06 Apr 2022 04:01:01 GMT
ARG BASE_URL
# Wed, 06 Apr 2022 04:01:04 GMT
ARG BONITA_URL
# Wed, 06 Apr 2022 04:01:10 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 06 Apr 2022 04:01:15 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 06 Apr 2022 04:01:18 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 06 Apr 2022 04:01:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 06 Apr 2022 04:01:23 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 06 Apr 2022 04:01:32 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 06 Apr 2022 04:01:47 GMT
RUN mkdir /opt/files
# Wed, 06 Apr 2022 04:01:51 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 06 Apr 2022 04:02:16 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 06 Apr 2022 04:02:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 06 Apr 2022 04:02:35 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 06 Apr 2022 04:02:39 GMT
VOLUME [/opt/bonita]
# Wed, 06 Apr 2022 04:02:42 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 06 Apr 2022 04:02:46 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 04:02:50 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3797140b1f3932691017aa275137964432dbeff45bcc6f8a8cfed91439f9eb8c`  
		Last Modified: Wed, 06 Apr 2022 04:11:09 GMT  
		Size: 86.6 MB (86557112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bcdf9f7a07427bac5eb4b0abb9524330d19ae7739f209e225c558657e3d4cd`  
		Last Modified: Wed, 06 Apr 2022 04:10:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedb609f92c0b35515c47a526be80f7c51dfbcbc2e2b104ecc0c0418461d3911`  
		Last Modified: Wed, 06 Apr 2022 04:10:54 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a98badb926d158087565b1dc5bc89334e25cf502a7fe73edaea153ac4cd066`  
		Last Modified: Wed, 06 Apr 2022 04:10:52 GMT  
		Size: 546.7 KB (546744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c816b69125e2463711768afa773433b812b8e7dffe6091c05ecc4b7df09f8912`  
		Last Modified: Wed, 06 Apr 2022 04:10:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac16ea8c2f4867ada9ea46a9359dff02c614dad05813b001ddde9975760ec61`  
		Last Modified: Wed, 06 Apr 2022 04:10:51 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831bca001c313693d1d9e530d19e18ea49ece6982daefd15c66c1a555831b55a`  
		Last Modified: Wed, 06 Apr 2022 04:11:00 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85bb3f355189f0267f01c3fdf45ac21b6f4e561c6ee66a1b5d1513d8da17a1c`  
		Last Modified: Wed, 06 Apr 2022 04:10:51 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:e8033303eac4a43ad8826b4824fc77609e2b3175eb6167331883b5b1dd4eb0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:b61b0cead340f24819f17b5df2873f398551e673689a5b43413f983974f76a1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234304839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2552beba9b4b8ee48aaf246e0d16fcf15b8db7256902743824268df7ebd2c0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:22:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 22 Apr 2022 01:23:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 01:23:23 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 22 Apr 2022 01:23:23 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 22 Apr 2022 01:23:26 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 22 Apr 2022 01:23:26 GMT
ARG BONITA_VERSION
# Fri, 22 Apr 2022 01:23:26 GMT
ARG BONITA_SHA256
# Fri, 22 Apr 2022 01:23:26 GMT
ARG BASE_URL
# Fri, 22 Apr 2022 01:23:26 GMT
ARG BONITA_URL
# Fri, 22 Apr 2022 01:23:26 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 22 Apr 2022 01:23:26 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 22 Apr 2022 01:23:26 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 22 Apr 2022 01:23:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 22 Apr 2022 01:23:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 22 Apr 2022 01:23:27 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 22 Apr 2022 01:23:28 GMT
RUN mkdir /opt/files
# Fri, 22 Apr 2022 01:23:28 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 22 Apr 2022 01:23:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 22 Apr 2022 01:23:35 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 22 Apr 2022 01:23:37 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 22 Apr 2022 01:23:37 GMT
VOLUME [/opt/bonita]
# Fri, 22 Apr 2022 01:23:37 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 22 Apr 2022 01:23:37 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 01:23:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66265528ccecf43b685e8cc6014acbda3604444f53c17f7d14a0ca4caad3b5fe`  
		Last Modified: Fri, 22 Apr 2022 01:25:10 GMT  
		Size: 93.7 MB (93659383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16c9efc2ba105a4c6440eeae034968f0a4403632dac03bfca64505847e96af`  
		Last Modified: Fri, 22 Apr 2022 01:24:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab5365759ee5f8e017f1e43a3183a827225526aad95bfe08d2ff0df2eef3320`  
		Last Modified: Fri, 22 Apr 2022 01:24:58 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd8fecd5bb01e2452c1a8086513d196c0a2702a0ed879dd6ce1504860b7ff30`  
		Last Modified: Fri, 22 Apr 2022 01:24:56 GMT  
		Size: 577.0 KB (576952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c6995b8a0687d00b28a53b523ca1323383676f0db2cdc6bd1435741bf0ae62`  
		Last Modified: Fri, 22 Apr 2022 01:24:56 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef1b403272ff10579b70ec4b3a3960c3c237eea0f2d5b392b047cb8a7bcfb8e`  
		Last Modified: Fri, 22 Apr 2022 01:24:56 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa108a1a4ba0d6ba78210b69ddbea05f66be0867355c7a90b730cc68e65b556`  
		Last Modified: Fri, 22 Apr 2022 01:25:02 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d6a223f21d1dbd101107ccf6404405c40a8642fccf3029235650b68a631ac4`  
		Last Modified: Fri, 22 Apr 2022 01:24:56 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:64e2c8182eca87681781cfc05326529ff746e2f41e040c68ab1d43c1071daa41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223398036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97240d730430aabd0b7e02fc6eebfbcf1888cacc0f4e9821b2d343cfae35434e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:58:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 22:59:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 22:59:14 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 22:59:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 05 Apr 2022 22:59:19 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 05 Apr 2022 22:59:19 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 22:59:20 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 22:59:21 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 22:59:22 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 22:59:23 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 05 Apr 2022 22:59:24 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 05 Apr 2022 22:59:25 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 05 Apr 2022 22:59:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 22:59:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 05 Apr 2022 22:59:28 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 05 Apr 2022 22:59:29 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 22:59:31 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 05 Apr 2022 22:59:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 05 Apr 2022 22:59:42 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 05 Apr 2022 22:59:43 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 05 Apr 2022 22:59:44 GMT
VOLUME [/opt/bonita]
# Tue, 05 Apr 2022 22:59:46 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 05 Apr 2022 22:59:46 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 22:59:47 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c33ecc03ac3ec45c755fe7c9affd84d05cd4c5aeff7430264708c5c324e46a`  
		Last Modified: Tue, 05 Apr 2022 23:02:34 GMT  
		Size: 85.8 MB (85761773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd208172af52c2410b7046f45ab089b878466337ed2bd5b3a79e50f04133270a`  
		Last Modified: Tue, 05 Apr 2022 23:02:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9b10b9b4ad0ba30bcd3c3518782f025923f40643795a0b21b2361b2505c5a6`  
		Last Modified: Tue, 05 Apr 2022 23:02:22 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db00845da6fa4fc633f85ebfefd4635aaf4774b5e764ef56cf42a730fd4269a`  
		Last Modified: Tue, 05 Apr 2022 23:02:20 GMT  
		Size: 546.9 KB (546931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38b1b99d036d17d3c955787d065351dc6ea9634784be42ad6574b91317bf1c9`  
		Last Modified: Tue, 05 Apr 2022 23:02:20 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5916f250dbee91f448a6c49909b61157b69b2c11e85c1fb374900e564658778f`  
		Last Modified: Tue, 05 Apr 2022 23:02:20 GMT  
		Size: 6.9 KB (6865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379b59a7ad10f52210fc7067b74154cc7fc4c78d9d57d3378e676bc627a77b97`  
		Last Modified: Tue, 05 Apr 2022 23:02:30 GMT  
		Size: 113.3 MB (113347827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa3653e6a86f952ee809b55dbaf1a83d069350ba21b63e5b80c7a36fe7be84f`  
		Last Modified: Tue, 05 Apr 2022 23:02:20 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:f17ecfb397b1df44a8fafb43244150c42268296ac1e5aa8609459aafc518c904
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230900908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcf8df8d27f1cbd2b22a642e4e49a3d32398d65a5bd0fa8c666e418d06cfdd5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 03:57:28 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 06 Apr 2022 04:00:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:00:26 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 06 Apr 2022 04:00:39 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 06 Apr 2022 04:00:52 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 06 Apr 2022 04:00:56 GMT
ARG BONITA_VERSION
# Wed, 06 Apr 2022 04:00:59 GMT
ARG BONITA_SHA256
# Wed, 06 Apr 2022 04:01:01 GMT
ARG BASE_URL
# Wed, 06 Apr 2022 04:01:04 GMT
ARG BONITA_URL
# Wed, 06 Apr 2022 04:01:10 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 06 Apr 2022 04:01:15 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 06 Apr 2022 04:01:18 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 06 Apr 2022 04:01:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 06 Apr 2022 04:01:23 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 06 Apr 2022 04:01:32 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 06 Apr 2022 04:01:47 GMT
RUN mkdir /opt/files
# Wed, 06 Apr 2022 04:01:51 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 06 Apr 2022 04:02:16 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 06 Apr 2022 04:02:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 06 Apr 2022 04:02:35 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 06 Apr 2022 04:02:39 GMT
VOLUME [/opt/bonita]
# Wed, 06 Apr 2022 04:02:42 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 06 Apr 2022 04:02:46 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 04:02:50 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3797140b1f3932691017aa275137964432dbeff45bcc6f8a8cfed91439f9eb8c`  
		Last Modified: Wed, 06 Apr 2022 04:11:09 GMT  
		Size: 86.6 MB (86557112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bcdf9f7a07427bac5eb4b0abb9524330d19ae7739f209e225c558657e3d4cd`  
		Last Modified: Wed, 06 Apr 2022 04:10:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedb609f92c0b35515c47a526be80f7c51dfbcbc2e2b104ecc0c0418461d3911`  
		Last Modified: Wed, 06 Apr 2022 04:10:54 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a98badb926d158087565b1dc5bc89334e25cf502a7fe73edaea153ac4cd066`  
		Last Modified: Wed, 06 Apr 2022 04:10:52 GMT  
		Size: 546.7 KB (546744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c816b69125e2463711768afa773433b812b8e7dffe6091c05ecc4b7df09f8912`  
		Last Modified: Wed, 06 Apr 2022 04:10:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac16ea8c2f4867ada9ea46a9359dff02c614dad05813b001ddde9975760ec61`  
		Last Modified: Wed, 06 Apr 2022 04:10:51 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831bca001c313693d1d9e530d19e18ea49ece6982daefd15c66c1a555831b55a`  
		Last Modified: Wed, 06 Apr 2022 04:11:00 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85bb3f355189f0267f01c3fdf45ac21b6f4e561c6ee66a1b5d1513d8da17a1c`  
		Last Modified: Wed, 06 Apr 2022 04:10:51 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:a93b06d83c07fdd22d914ecc443425145920e2d62e3c74d018ce4d79999a6bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:4ac754cc035059600a7192046e95be18bea425a9fd0ca4fe81706bb26926cc35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237372463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394162fea48e580bb2f465e10c9878a90ca1a59ec6a1b158fa32908bea9016f8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:22:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 22 Apr 2022 01:23:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 01:23:23 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 22 Apr 2022 01:23:23 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 22 Apr 2022 01:23:26 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 22 Apr 2022 01:23:26 GMT
ARG BONITA_VERSION
# Fri, 22 Apr 2022 01:23:43 GMT
ARG BRANDING_VERSION
# Fri, 22 Apr 2022 01:23:43 GMT
ARG BONITA_SHA256
# Fri, 22 Apr 2022 01:23:44 GMT
ARG BASE_URL
# Fri, 22 Apr 2022 01:23:44 GMT
ARG BONITA_URL
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 22 Apr 2022 01:23:44 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 22 Apr 2022 01:23:45 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 22 Apr 2022 01:23:45 GMT
RUN mkdir /opt/files
# Fri, 22 Apr 2022 01:23:45 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 22 Apr 2022 01:23:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 22 Apr 2022 01:23:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 22 Apr 2022 01:23:54 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 22 Apr 2022 01:23:54 GMT
VOLUME [/opt/bonita]
# Fri, 22 Apr 2022 01:23:54 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 22 Apr 2022 01:23:54 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 01:23:54 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66265528ccecf43b685e8cc6014acbda3604444f53c17f7d14a0ca4caad3b5fe`  
		Last Modified: Fri, 22 Apr 2022 01:25:10 GMT  
		Size: 93.7 MB (93659383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16c9efc2ba105a4c6440eeae034968f0a4403632dac03bfca64505847e96af`  
		Last Modified: Fri, 22 Apr 2022 01:24:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab5365759ee5f8e017f1e43a3183a827225526aad95bfe08d2ff0df2eef3320`  
		Last Modified: Fri, 22 Apr 2022 01:24:58 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd8fecd5bb01e2452c1a8086513d196c0a2702a0ed879dd6ce1504860b7ff30`  
		Last Modified: Fri, 22 Apr 2022 01:24:56 GMT  
		Size: 577.0 KB (576952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03889de4a415a8a95d2384cb03675cba1acd8c169d3c501017b995ceba9c623e`  
		Last Modified: Fri, 22 Apr 2022 01:25:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7413ea3a75cf10e37a77cbd15ca87e744a91f5a0323d771e74a3226378e306`  
		Last Modified: Fri, 22 Apr 2022 01:25:20 GMT  
		Size: 6.9 KB (6942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1d6cdf8f58fe752dfc13fdc708024416b564711d822a926bc96046822d63a0`  
		Last Modified: Fri, 22 Apr 2022 01:25:25 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c730a101a1ffb1bf94a0ea76b7863b678ce7d2610f1a5499021357167ef16443`  
		Last Modified: Fri, 22 Apr 2022 01:25:20 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:f9ffffd1db585db1ded556470d59c594a6af2706329d79c4a5e19e92fba88250
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226465666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812a03713b8021c286fd182ced0166ed2be62cfad6c26c1a622f0372b4c0630e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:58:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 22:59:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 22:59:14 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 22:59:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 05 Apr 2022 22:59:19 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 05 Apr 2022 22:59:19 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 23:00:02 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 23:00:03 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 23:00:04 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 23:00:05 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 23:00:06 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 05 Apr 2022 23:00:07 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 05 Apr 2022 23:00:08 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 05 Apr 2022 23:00:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 05 Apr 2022 23:00:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 23:00:11 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 05 Apr 2022 23:00:12 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 05 Apr 2022 23:00:13 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 23:00:15 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 05 Apr 2022 23:00:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 05 Apr 2022 23:00:32 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 05 Apr 2022 23:00:33 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 05 Apr 2022 23:00:34 GMT
VOLUME [/opt/bonita]
# Tue, 05 Apr 2022 23:00:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 05 Apr 2022 23:00:36 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 23:00:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c33ecc03ac3ec45c755fe7c9affd84d05cd4c5aeff7430264708c5c324e46a`  
		Last Modified: Tue, 05 Apr 2022 23:02:34 GMT  
		Size: 85.8 MB (85761773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd208172af52c2410b7046f45ab089b878466337ed2bd5b3a79e50f04133270a`  
		Last Modified: Tue, 05 Apr 2022 23:02:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9b10b9b4ad0ba30bcd3c3518782f025923f40643795a0b21b2361b2505c5a6`  
		Last Modified: Tue, 05 Apr 2022 23:02:22 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db00845da6fa4fc633f85ebfefd4635aaf4774b5e764ef56cf42a730fd4269a`  
		Last Modified: Tue, 05 Apr 2022 23:02:20 GMT  
		Size: 546.9 KB (546931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9efd36fb83002aa96ebbed0d93fd192ce4b59c665b95ff9baa0ad7e3b8391e`  
		Last Modified: Tue, 05 Apr 2022 23:02:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3f9d3d8bcb63c7a643e3b8894fb6ee4debf999158718d5d5df2f9a56e0de62`  
		Last Modified: Tue, 05 Apr 2022 23:02:44 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea233d274933c0623185dd20805f5a4ab98c801653213018efc760522ef9296`  
		Last Modified: Tue, 05 Apr 2022 23:02:56 GMT  
		Size: 116.4 MB (116415400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45b5439fff196f2045afe202e70b58b492eebce3e6c4f7609081d226dd0a66f`  
		Last Modified: Tue, 05 Apr 2022 23:02:44 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:3da6e391662ee228d240886065907d6648dca1e3135e0ffbe2a030c6db60e1e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233968534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e500fbb269dcc1826f931278272919705ddfa8333bd87b9c584137ace4761`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 03:57:28 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 06 Apr 2022 04:00:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:00:26 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 06 Apr 2022 04:00:39 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 06 Apr 2022 04:00:52 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 06 Apr 2022 04:00:56 GMT
ARG BONITA_VERSION
# Wed, 06 Apr 2022 04:03:05 GMT
ARG BRANDING_VERSION
# Wed, 06 Apr 2022 04:03:12 GMT
ARG BONITA_SHA256
# Wed, 06 Apr 2022 04:03:14 GMT
ARG BASE_URL
# Wed, 06 Apr 2022 04:03:19 GMT
ARG BONITA_URL
# Wed, 06 Apr 2022 04:03:22 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 06 Apr 2022 04:03:26 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 06 Apr 2022 04:03:31 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 06 Apr 2022 04:03:38 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 06 Apr 2022 04:03:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 06 Apr 2022 04:03:50 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 06 Apr 2022 04:03:59 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 06 Apr 2022 04:04:05 GMT
RUN mkdir /opt/files
# Wed, 06 Apr 2022 04:04:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 06 Apr 2022 04:04:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 06 Apr 2022 04:04:28 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 06 Apr 2022 04:04:38 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 06 Apr 2022 04:04:42 GMT
VOLUME [/opt/bonita]
# Wed, 06 Apr 2022 04:04:45 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 06 Apr 2022 04:04:48 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 04:04:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3797140b1f3932691017aa275137964432dbeff45bcc6f8a8cfed91439f9eb8c`  
		Last Modified: Wed, 06 Apr 2022 04:11:09 GMT  
		Size: 86.6 MB (86557112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bcdf9f7a07427bac5eb4b0abb9524330d19ae7739f209e225c558657e3d4cd`  
		Last Modified: Wed, 06 Apr 2022 04:10:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedb609f92c0b35515c47a526be80f7c51dfbcbc2e2b104ecc0c0418461d3911`  
		Last Modified: Wed, 06 Apr 2022 04:10:54 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a98badb926d158087565b1dc5bc89334e25cf502a7fe73edaea153ac4cd066`  
		Last Modified: Wed, 06 Apr 2022 04:10:52 GMT  
		Size: 546.7 KB (546744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abca8c880793aa57ea79c8b5c52ea0fe3fb77c4f739bbff396c2e81234670434`  
		Last Modified: Wed, 06 Apr 2022 04:11:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca00e5906707c86c965a1bf6dcaf9240a72a9d462516be71e4506b1dc4a5c38`  
		Last Modified: Wed, 06 Apr 2022 04:11:23 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c537633c59a2e9dffaafc4fad2d5b2a64cd706730b458f3d48f858db0d366b38`  
		Last Modified: Wed, 06 Apr 2022 04:11:32 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3a364bfb6112c878a6da2b3add53147a9abf1acf561989f011a4565058b9e`  
		Last Modified: Wed, 06 Apr 2022 04:11:23 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:a93b06d83c07fdd22d914ecc443425145920e2d62e3c74d018ce4d79999a6bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:4ac754cc035059600a7192046e95be18bea425a9fd0ca4fe81706bb26926cc35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237372463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394162fea48e580bb2f465e10c9878a90ca1a59ec6a1b158fa32908bea9016f8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:22:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 22 Apr 2022 01:23:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 01:23:23 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 22 Apr 2022 01:23:23 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 22 Apr 2022 01:23:26 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 22 Apr 2022 01:23:26 GMT
ARG BONITA_VERSION
# Fri, 22 Apr 2022 01:23:43 GMT
ARG BRANDING_VERSION
# Fri, 22 Apr 2022 01:23:43 GMT
ARG BONITA_SHA256
# Fri, 22 Apr 2022 01:23:44 GMT
ARG BASE_URL
# Fri, 22 Apr 2022 01:23:44 GMT
ARG BONITA_URL
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 22 Apr 2022 01:23:44 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 22 Apr 2022 01:23:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 22 Apr 2022 01:23:45 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 22 Apr 2022 01:23:45 GMT
RUN mkdir /opt/files
# Fri, 22 Apr 2022 01:23:45 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 22 Apr 2022 01:23:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 22 Apr 2022 01:23:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 22 Apr 2022 01:23:54 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 22 Apr 2022 01:23:54 GMT
VOLUME [/opt/bonita]
# Fri, 22 Apr 2022 01:23:54 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 22 Apr 2022 01:23:54 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 01:23:54 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66265528ccecf43b685e8cc6014acbda3604444f53c17f7d14a0ca4caad3b5fe`  
		Last Modified: Fri, 22 Apr 2022 01:25:10 GMT  
		Size: 93.7 MB (93659383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16c9efc2ba105a4c6440eeae034968f0a4403632dac03bfca64505847e96af`  
		Last Modified: Fri, 22 Apr 2022 01:24:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab5365759ee5f8e017f1e43a3183a827225526aad95bfe08d2ff0df2eef3320`  
		Last Modified: Fri, 22 Apr 2022 01:24:58 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd8fecd5bb01e2452c1a8086513d196c0a2702a0ed879dd6ce1504860b7ff30`  
		Last Modified: Fri, 22 Apr 2022 01:24:56 GMT  
		Size: 577.0 KB (576952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03889de4a415a8a95d2384cb03675cba1acd8c169d3c501017b995ceba9c623e`  
		Last Modified: Fri, 22 Apr 2022 01:25:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7413ea3a75cf10e37a77cbd15ca87e744a91f5a0323d771e74a3226378e306`  
		Last Modified: Fri, 22 Apr 2022 01:25:20 GMT  
		Size: 6.9 KB (6942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1d6cdf8f58fe752dfc13fdc708024416b564711d822a926bc96046822d63a0`  
		Last Modified: Fri, 22 Apr 2022 01:25:25 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c730a101a1ffb1bf94a0ea76b7863b678ce7d2610f1a5499021357167ef16443`  
		Last Modified: Fri, 22 Apr 2022 01:25:20 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:f9ffffd1db585db1ded556470d59c594a6af2706329d79c4a5e19e92fba88250
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226465666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812a03713b8021c286fd182ced0166ed2be62cfad6c26c1a622f0372b4c0630e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:58:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 22:59:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 22:59:14 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 22:59:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 05 Apr 2022 22:59:19 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 05 Apr 2022 22:59:19 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 23:00:02 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 23:00:03 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 23:00:04 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 23:00:05 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 23:00:06 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 05 Apr 2022 23:00:07 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 05 Apr 2022 23:00:08 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 05 Apr 2022 23:00:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 05 Apr 2022 23:00:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 23:00:11 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 05 Apr 2022 23:00:12 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 05 Apr 2022 23:00:13 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 23:00:15 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 05 Apr 2022 23:00:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 05 Apr 2022 23:00:32 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 05 Apr 2022 23:00:33 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 05 Apr 2022 23:00:34 GMT
VOLUME [/opt/bonita]
# Tue, 05 Apr 2022 23:00:36 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 05 Apr 2022 23:00:36 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 23:00:37 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c33ecc03ac3ec45c755fe7c9affd84d05cd4c5aeff7430264708c5c324e46a`  
		Last Modified: Tue, 05 Apr 2022 23:02:34 GMT  
		Size: 85.8 MB (85761773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd208172af52c2410b7046f45ab089b878466337ed2bd5b3a79e50f04133270a`  
		Last Modified: Tue, 05 Apr 2022 23:02:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9b10b9b4ad0ba30bcd3c3518782f025923f40643795a0b21b2361b2505c5a6`  
		Last Modified: Tue, 05 Apr 2022 23:02:22 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db00845da6fa4fc633f85ebfefd4635aaf4774b5e764ef56cf42a730fd4269a`  
		Last Modified: Tue, 05 Apr 2022 23:02:20 GMT  
		Size: 546.9 KB (546931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9efd36fb83002aa96ebbed0d93fd192ce4b59c665b95ff9baa0ad7e3b8391e`  
		Last Modified: Tue, 05 Apr 2022 23:02:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3f9d3d8bcb63c7a643e3b8894fb6ee4debf999158718d5d5df2f9a56e0de62`  
		Last Modified: Tue, 05 Apr 2022 23:02:44 GMT  
		Size: 6.9 KB (6918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea233d274933c0623185dd20805f5a4ab98c801653213018efc760522ef9296`  
		Last Modified: Tue, 05 Apr 2022 23:02:56 GMT  
		Size: 116.4 MB (116415400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45b5439fff196f2045afe202e70b58b492eebce3e6c4f7609081d226dd0a66f`  
		Last Modified: Tue, 05 Apr 2022 23:02:44 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:3da6e391662ee228d240886065907d6648dca1e3135e0ffbe2a030c6db60e1e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233968534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7e500fbb269dcc1826f931278272919705ddfa8333bd87b9c584137ace4761`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 03:57:28 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 06 Apr 2022 04:00:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:00:26 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 06 Apr 2022 04:00:39 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 06 Apr 2022 04:00:52 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 06 Apr 2022 04:00:56 GMT
ARG BONITA_VERSION
# Wed, 06 Apr 2022 04:03:05 GMT
ARG BRANDING_VERSION
# Wed, 06 Apr 2022 04:03:12 GMT
ARG BONITA_SHA256
# Wed, 06 Apr 2022 04:03:14 GMT
ARG BASE_URL
# Wed, 06 Apr 2022 04:03:19 GMT
ARG BONITA_URL
# Wed, 06 Apr 2022 04:03:22 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 06 Apr 2022 04:03:26 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 06 Apr 2022 04:03:31 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 06 Apr 2022 04:03:38 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 06 Apr 2022 04:03:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 06 Apr 2022 04:03:50 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 06 Apr 2022 04:03:59 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 06 Apr 2022 04:04:05 GMT
RUN mkdir /opt/files
# Wed, 06 Apr 2022 04:04:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 06 Apr 2022 04:04:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 06 Apr 2022 04:04:28 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 06 Apr 2022 04:04:38 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 06 Apr 2022 04:04:42 GMT
VOLUME [/opt/bonita]
# Wed, 06 Apr 2022 04:04:45 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 06 Apr 2022 04:04:48 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 04:04:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3797140b1f3932691017aa275137964432dbeff45bcc6f8a8cfed91439f9eb8c`  
		Last Modified: Wed, 06 Apr 2022 04:11:09 GMT  
		Size: 86.6 MB (86557112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bcdf9f7a07427bac5eb4b0abb9524330d19ae7739f209e225c558657e3d4cd`  
		Last Modified: Wed, 06 Apr 2022 04:10:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedb609f92c0b35515c47a526be80f7c51dfbcbc2e2b104ecc0c0418461d3911`  
		Last Modified: Wed, 06 Apr 2022 04:10:54 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a98badb926d158087565b1dc5bc89334e25cf502a7fe73edaea153ac4cd066`  
		Last Modified: Wed, 06 Apr 2022 04:10:52 GMT  
		Size: 546.7 KB (546744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abca8c880793aa57ea79c8b5c52ea0fe3fb77c4f739bbff396c2e81234670434`  
		Last Modified: Wed, 06 Apr 2022 04:11:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca00e5906707c86c965a1bf6dcaf9240a72a9d462516be71e4506b1dc4a5c38`  
		Last Modified: Wed, 06 Apr 2022 04:11:23 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c537633c59a2e9dffaafc4fad2d5b2a64cd706730b458f3d48f858db0d366b38`  
		Last Modified: Wed, 06 Apr 2022 04:11:32 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3a364bfb6112c878a6da2b3add53147a9abf1acf561989f011a4565058b9e`  
		Last Modified: Wed, 06 Apr 2022 04:11:23 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:88f76d905825b6adef4ca430901bcf99138da7c4ff7be8b59fc6e9ad6a398ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:5333d829c04a1259d09976844335b68efc3204ce9e803b86b278ee7c3576ef6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235106399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175bba281ea3436183dbd367a8b7b0818e75bc71614d6d93312ba200b5ec058e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:22:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 22 Apr 2022 01:24:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 01:24:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 22 Apr 2022 01:24:18 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 22 Apr 2022 01:24:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_VERSION
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BRANDING_VERSION
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_SHA256
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BASE_URL
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_URL
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 22 Apr 2022 01:24:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 22 Apr 2022 01:24:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 22 Apr 2022 01:24:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 22 Apr 2022 01:24:22 GMT
RUN mkdir /opt/files
# Fri, 22 Apr 2022 01:24:22 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 22 Apr 2022 01:24:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 22 Apr 2022 01:24:31 GMT
ENV HTTP_API=false
# Fri, 22 Apr 2022 01:24:32 GMT
VOLUME [/opt/bonita]
# Fri, 22 Apr 2022 01:24:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 22 Apr 2022 01:24:32 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 01:24:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a6bfdda70147d18bf20d9f200b0e89f9bf12aaf4163a53aec413a1fbac49db`  
		Last Modified: Fri, 22 Apr 2022 01:25:53 GMT  
		Size: 93.7 MB (93658186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0180a51e6fbc6fc70250b21e2e0c058314e2a1783da77cfbf5a6b4e8fddc031f`  
		Last Modified: Fri, 22 Apr 2022 01:25:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30cced3fa023cbba53f6a23f693c3a561d545c4877416403e79d840933093d6`  
		Last Modified: Fri, 22 Apr 2022 01:25:41 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068bb8acea2c65c3874287c6d855fce18e57bb7f1f690a6059bfd20138005a3d`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 1.0 MB (1003215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bde2f1d36d17d2dfbc1723f84055675909c30ceb780a024a5a1414980795fe`  
		Last Modified: Fri, 22 Apr 2022 01:25:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe3a412ac8d0dfce451f851d783a4ed81040f60be605a9ecfe48272c6e11a1a`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767fb402b4d4e27d1d99a8d9275e6e09aaacac06459d626f92518dfb2a070bb4`  
		Last Modified: Fri, 22 Apr 2022 01:25:44 GMT  
		Size: 113.7 MB (113727920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80904747d961983d36afe3fc428ee94bbfb12d2f98926694505ad9b6980b86e`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:994746b77042bb103ae89f29a0d68042bc74633e9c2fae10e5c71810cf90ef78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbf266641b2d0fdb4823734476faaccd1edabce516ddc2ba9d9ff5d5054f284`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:58:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 23:01:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:01:09 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 23:01:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 05 Apr 2022 23:01:14 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 05 Apr 2022 23:01:14 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 23:01:15 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 23:01:16 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 23:01:17 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 23:01:18 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 23:01:19 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 05 Apr 2022 23:01:20 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 05 Apr 2022 23:01:21 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 05 Apr 2022 23:01:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 05 Apr 2022 23:01:23 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 23:01:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 05 Apr 2022 23:01:25 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 23:01:27 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 05 Apr 2022 23:01:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 05 Apr 2022 23:01:37 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 23:01:39 GMT
VOLUME [/opt/bonita]
# Tue, 05 Apr 2022 23:01:40 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 05 Apr 2022 23:01:40 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 23:01:41 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a342eca32d8c7efdcc6518a6a024c82a904b40b2299718265db4f700b611f`  
		Last Modified: Tue, 05 Apr 2022 23:03:24 GMT  
		Size: 85.8 MB (85761767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6773dd32221fab5034b6afb8252d9ddb02fd6967ed56e534598ac4d2daaa9a82`  
		Last Modified: Tue, 05 Apr 2022 23:03:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80d1794db296ab170d35b2fa0cb8a5a33bd169cb994a1a36d625024401e2f9`  
		Last Modified: Tue, 05 Apr 2022 23:03:13 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d39709d3a66d0bbb19d4f86c2795a02d679145064d5512dfd94db88b9aea032`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 929.4 KB (929406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cbb8c35dfc0a421349a18295b22a952b19fd917d51d96e0696f793f96294f0`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc72ca6f6cffbcb3df92677851d567dccf1ced29efb7ad910e78f212ee5ac93`  
		Last Modified: Tue, 05 Apr 2022 23:03:10 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b11332953363ba30aa8af0f6cf77f67f7e6f089403c0394425b0c827e02b12`  
		Last Modified: Tue, 05 Apr 2022 23:03:19 GMT  
		Size: 113.7 MB (113727849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385f85a63a52a608a0746be33ba569cb6efd10095d3a2de638d0b22e4cbaf846`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:91668825b7a481026185e944d94ea679de83c532e02e5e70afc6b45ba4b6b2aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebaa35ead7bbad7dd4241931df4b2b8edfbfdb3bef58ab88435a18fb6384de3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 03:57:28 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 06 Apr 2022 04:07:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:08:07 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 06 Apr 2022 04:08:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 06 Apr 2022 04:08:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 06 Apr 2022 04:08:35 GMT
ARG BONITA_VERSION
# Wed, 06 Apr 2022 04:08:37 GMT
ARG BRANDING_VERSION
# Wed, 06 Apr 2022 04:08:40 GMT
ARG BONITA_SHA256
# Wed, 06 Apr 2022 04:08:45 GMT
ARG BASE_URL
# Wed, 06 Apr 2022 04:08:48 GMT
ARG BONITA_URL
# Wed, 06 Apr 2022 04:08:52 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 06 Apr 2022 04:08:55 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 06 Apr 2022 04:08:57 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 06 Apr 2022 04:09:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 06 Apr 2022 04:09:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 06 Apr 2022 04:09:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 06 Apr 2022 04:09:14 GMT
RUN mkdir /opt/files
# Wed, 06 Apr 2022 04:09:17 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 06 Apr 2022 04:09:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 06 Apr 2022 04:09:43 GMT
ENV HTTP_API=false
# Wed, 06 Apr 2022 04:09:48 GMT
VOLUME [/opt/bonita]
# Wed, 06 Apr 2022 04:09:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 06 Apr 2022 04:09:54 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 04:09:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1faaa0ff16cf6a07daa39cb3b0b600a672ed410aa0655a3d47818258f587b49`  
		Last Modified: Wed, 06 Apr 2022 04:12:06 GMT  
		Size: 86.6 MB (86556858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a502123895652556962416c26c4f1f5b36ae9e4f6aae3cc5dadc6aca8c68a20`  
		Last Modified: Wed, 06 Apr 2022 04:11:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf13516d8ca4b08100d618913f86648c25b7ccb2de2906ece3073c1183287812`  
		Last Modified: Wed, 06 Apr 2022 04:11:50 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f588c67fbe00f626d24d6fafa4c35622614c75bb361fd075ed1504ffbef4a7`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 904.2 KB (904213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4473c3d5fdb46b6c1425eb08f4b66ad3cf9e934116b6198ea30fbd15fee96`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75681f610194b1b6f355b0b62e17f1a1b944e64c60811d20f7389af29e5fb95`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4929458e28211f39954235d13e2970a1046415afd41578ffb9cb9db83466070b`  
		Last Modified: Wed, 06 Apr 2022 04:11:58 GMT  
		Size: 113.7 MB (113727924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8271d2c547727e51acca08b86e2ff4e026b400487783cb68d63a30913032f4`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:88f76d905825b6adef4ca430901bcf99138da7c4ff7be8b59fc6e9ad6a398ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:5333d829c04a1259d09976844335b68efc3204ce9e803b86b278ee7c3576ef6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235106399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175bba281ea3436183dbd367a8b7b0818e75bc71614d6d93312ba200b5ec058e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Apr 2022 22:59:58 GMT
ADD file:5131314b62b7386e388b173018be7058491e96459344f78e6a2220771a65a2cd in / 
# Thu, 21 Apr 2022 22:59:58 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:22:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 22 Apr 2022 01:24:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 01:24:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 22 Apr 2022 01:24:18 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 22 Apr 2022 01:24:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_VERSION
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BRANDING_VERSION
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_SHA256
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BASE_URL
# Fri, 22 Apr 2022 01:24:21 GMT
ARG BONITA_URL
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 22 Apr 2022 01:24:21 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 22 Apr 2022 01:24:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 22 Apr 2022 01:24:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 22 Apr 2022 01:24:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 22 Apr 2022 01:24:22 GMT
RUN mkdir /opt/files
# Fri, 22 Apr 2022 01:24:22 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 22 Apr 2022 01:24:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 22 Apr 2022 01:24:31 GMT
ENV HTTP_API=false
# Fri, 22 Apr 2022 01:24:32 GMT
VOLUME [/opt/bonita]
# Fri, 22 Apr 2022 01:24:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 22 Apr 2022 01:24:32 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 01:24:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:88736512a147458c580cd28c969698561f236abba2ef04dbf0d7940cb3d7375e`  
		Last Modified: Tue, 19 Apr 2022 13:10:00 GMT  
		Size: 26.7 MB (26709883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a6bfdda70147d18bf20d9f200b0e89f9bf12aaf4163a53aec413a1fbac49db`  
		Last Modified: Fri, 22 Apr 2022 01:25:53 GMT  
		Size: 93.7 MB (93658186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0180a51e6fbc6fc70250b21e2e0c058314e2a1783da77cfbf5a6b4e8fddc031f`  
		Last Modified: Fri, 22 Apr 2022 01:25:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30cced3fa023cbba53f6a23f693c3a561d545c4877416403e79d840933093d6`  
		Last Modified: Fri, 22 Apr 2022 01:25:41 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068bb8acea2c65c3874287c6d855fce18e57bb7f1f690a6059bfd20138005a3d`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 1.0 MB (1003215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bde2f1d36d17d2dfbc1723f84055675909c30ceb780a024a5a1414980795fe`  
		Last Modified: Fri, 22 Apr 2022 01:25:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe3a412ac8d0dfce451f851d783a4ed81040f60be605a9ecfe48272c6e11a1a`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767fb402b4d4e27d1d99a8d9275e6e09aaacac06459d626f92518dfb2a070bb4`  
		Last Modified: Fri, 22 Apr 2022 01:25:44 GMT  
		Size: 113.7 MB (113727920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80904747d961983d36afe3fc428ee94bbfb12d2f98926694505ad9b6980b86e`  
		Last Modified: Fri, 22 Apr 2022 01:25:38 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:994746b77042bb103ae89f29a0d68042bc74633e9c2fae10e5c71810cf90ef78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbf266641b2d0fdb4823734476faaccd1edabce516ddc2ba9d9ff5d5054f284`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:58:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 23:01:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:01:09 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 23:01:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 05 Apr 2022 23:01:14 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 05 Apr 2022 23:01:14 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 23:01:15 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 23:01:16 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 23:01:17 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 23:01:18 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 23:01:19 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 05 Apr 2022 23:01:20 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 05 Apr 2022 23:01:21 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 05 Apr 2022 23:01:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 05 Apr 2022 23:01:23 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 23:01:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 05 Apr 2022 23:01:25 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 23:01:27 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 05 Apr 2022 23:01:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 05 Apr 2022 23:01:37 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 23:01:39 GMT
VOLUME [/opt/bonita]
# Tue, 05 Apr 2022 23:01:40 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 05 Apr 2022 23:01:40 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 23:01:41 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a342eca32d8c7efdcc6518a6a024c82a904b40b2299718265db4f700b611f`  
		Last Modified: Tue, 05 Apr 2022 23:03:24 GMT  
		Size: 85.8 MB (85761767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6773dd32221fab5034b6afb8252d9ddb02fd6967ed56e534598ac4d2daaa9a82`  
		Last Modified: Tue, 05 Apr 2022 23:03:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80d1794db296ab170d35b2fa0cb8a5a33bd169cb994a1a36d625024401e2f9`  
		Last Modified: Tue, 05 Apr 2022 23:03:13 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d39709d3a66d0bbb19d4f86c2795a02d679145064d5512dfd94db88b9aea032`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 929.4 KB (929406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cbb8c35dfc0a421349a18295b22a952b19fd917d51d96e0696f793f96294f0`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc72ca6f6cffbcb3df92677851d567dccf1ced29efb7ad910e78f212ee5ac93`  
		Last Modified: Tue, 05 Apr 2022 23:03:10 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b11332953363ba30aa8af0f6cf77f67f7e6f089403c0394425b0c827e02b12`  
		Last Modified: Tue, 05 Apr 2022 23:03:19 GMT  
		Size: 113.7 MB (113727849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385f85a63a52a608a0746be33ba569cb6efd10095d3a2de638d0b22e4cbaf846`  
		Last Modified: Tue, 05 Apr 2022 23:03:11 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:91668825b7a481026185e944d94ea679de83c532e02e5e70afc6b45ba4b6b2aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebaa35ead7bbad7dd4241931df4b2b8edfbfdb3bef58ab88435a18fb6384de3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 03:57:28 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 06 Apr 2022 04:07:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:08:07 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 06 Apr 2022 04:08:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 06 Apr 2022 04:08:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 06 Apr 2022 04:08:35 GMT
ARG BONITA_VERSION
# Wed, 06 Apr 2022 04:08:37 GMT
ARG BRANDING_VERSION
# Wed, 06 Apr 2022 04:08:40 GMT
ARG BONITA_SHA256
# Wed, 06 Apr 2022 04:08:45 GMT
ARG BASE_URL
# Wed, 06 Apr 2022 04:08:48 GMT
ARG BONITA_URL
# Wed, 06 Apr 2022 04:08:52 GMT
ENV BONITA_VERSION=7.13.0
# Wed, 06 Apr 2022 04:08:55 GMT
ENV BRANDING_VERSION=2021.2-u0
# Wed, 06 Apr 2022 04:08:57 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Wed, 06 Apr 2022 04:09:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Wed, 06 Apr 2022 04:09:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 06 Apr 2022 04:09:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Wed, 06 Apr 2022 04:09:14 GMT
RUN mkdir /opt/files
# Wed, 06 Apr 2022 04:09:17 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Wed, 06 Apr 2022 04:09:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Wed, 06 Apr 2022 04:09:43 GMT
ENV HTTP_API=false
# Wed, 06 Apr 2022 04:09:48 GMT
VOLUME [/opt/bonita]
# Wed, 06 Apr 2022 04:09:49 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 06 Apr 2022 04:09:54 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 04:09:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1faaa0ff16cf6a07daa39cb3b0b600a672ed410aa0655a3d47818258f587b49`  
		Last Modified: Wed, 06 Apr 2022 04:12:06 GMT  
		Size: 86.6 MB (86556858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a502123895652556962416c26c4f1f5b36ae9e4f6aae3cc5dadc6aca8c68a20`  
		Last Modified: Wed, 06 Apr 2022 04:11:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf13516d8ca4b08100d618913f86648c25b7ccb2de2906ece3073c1183287812`  
		Last Modified: Wed, 06 Apr 2022 04:11:50 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f588c67fbe00f626d24d6fafa4c35622614c75bb361fd075ed1504ffbef4a7`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 904.2 KB (904213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4473c3d5fdb46b6c1425eb08f4b66ad3cf9e934116b6198ea30fbd15fee96`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75681f610194b1b6f355b0b62e17f1a1b944e64c60811d20f7389af29e5fb95`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4929458e28211f39954235d13e2970a1046415afd41578ffb9cb9db83466070b`  
		Last Modified: Wed, 06 Apr 2022 04:11:58 GMT  
		Size: 113.7 MB (113727924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8271d2c547727e51acca08b86e2ff4e026b400487783cb68d63a30913032f4`  
		Last Modified: Wed, 06 Apr 2022 04:11:48 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14`

```console
$ docker pull bonita@sha256:9bd37caef5943cf2cdc2a20993002c2d8d794f6f549da01f08ac9fdc56d2ae2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14` - linux; amd64

```console
$ docker pull bonita@sha256:aa6c404694792455f659ab29b685840a58847a82ee8d6b933510ab9b8d415e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791a1d923d653fa2c3fc2640e7509051adf42a471ba281268d753580e1da5f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:23:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 04:23:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 04:23:38 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 04:23:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 04:23:39 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 04:23:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:40 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 04:23:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 04:23:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 04:23:48 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 04:23:49 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 04:23:49 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 04:23:49 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 04:23:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 04:23:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff37705a3721b6f0fa369c96374cf9da30cff49af0d8000271ef496b3a770df`  
		Last Modified: Tue, 05 Apr 2022 04:24:23 GMT  
		Size: 60.7 MB (60744505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f66c34cc10d0cb3a031ef3da4ba3f1bd013bcc964d4956c60fad86f44fe69`  
		Last Modified: Tue, 05 Apr 2022 04:24:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578f03d3de8ca415ec7f424f8e565acd05fed61f7ae257c04a206815af3329f`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217417d523fc2999c4b2897458c8186aaae7637ca11cffcf678f5a94676243c3`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bafdba13f86b25d0530d42b1945be474d808e2e57c54eb92525278fd97b4066`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7700ffe2df31bc40779a5addc28e3643352992303bc5cd5013f722caeea46b`  
		Last Modified: Tue, 05 Apr 2022 04:24:20 GMT  
		Size: 116.7 MB (116690800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f64f512c1d336d8e3ad42228cc6f701c2f9ef296cccb6001395170ba33d88`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ec277986357bc1492ec4256aeb59f9509b5206166178468fae72d7b396672ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7da5778516cbbaa93e6b5f1f1812601e1ea647ac7f864ea7770f27872c6bf2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:09:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 03:09:35 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 03:09:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 03:09:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 03:09:37 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 03:09:38 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 03:09:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 03:09:40 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 03:09:41 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 03:09:42 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 03:09:43 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 03:09:44 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 03:09:45 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 03:09:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:48 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 03:09:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 03:09:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 03:09:58 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 03:09:59 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 03:10:00 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 03:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 03:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 03:10:03 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 03:10:04 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 03:10:05 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 03:10:06 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 03:10:07 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 03:10:08 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 03:10:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 03:10:10 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 03:10:12 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 03:10:12 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 03:10:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 03:10:14 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f256ad0fc5640d4ad6542e63ff033094b79f2158b7b837af471110ea8a336`  
		Last Modified: Tue, 05 Apr 2022 03:11:08 GMT  
		Size: 60.1 MB (60067315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f94323a629942950a0ffa4ebd9b9a9a67e2e99450c1b63b7caa029bb6fbab5`  
		Last Modified: Tue, 05 Apr 2022 03:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6976ee94f88624b6444d82e171da5997a9fc114743925400901581ea08c58`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5aabbb25b6ba30936e48e8d131ebfb29068a96236f7ce6e56f8aea4faafaf`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ba33b8f8be7b90a8de59a31f336886c4e754bd8846e3019ee792422b0c930`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 3.0 KB (3000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb65a72bf0159fbfb5326ef80a1e211664490a96659378c1d97748689b176279`  
		Last Modified: Tue, 05 Apr 2022 03:11:05 GMT  
		Size: 116.7 MB (116688761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b61e2452bca6bb834b08988d9199d49b4c4ffd3228c57b794b855215c36116`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; ppc64le

```console
$ docker pull bonita@sha256:a8b99264c74f1637a78eb549f8e83bee8f0f2146850d2757e4d483465a901317
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176075045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766bd47323049c15860a8cea6025a09aab1552c1868c15db5ef57c14d7cc9633`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:02:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 09:02:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 09:02:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 09:03:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 09:03:03 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:03:05 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 09:03:09 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:03:12 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:03:16 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:03:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 09:03:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 09:03:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 09:03:31 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:03:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:46 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:03:49 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 09:04:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 09:04:13 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 09:04:16 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 09:04:20 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 09:04:24 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 09:04:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 09:04:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 09:04:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 09:04:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 09:04:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 09:04:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 09:04:50 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 09:04:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 09:04:59 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 09:05:01 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 09:05:03 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 09:05:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 09:05:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434586e006643fe98fc4f4804ae9fc2bda4db5b77b98a9fd444e497dfe6b0d0`  
		Last Modified: Tue, 05 Apr 2022 09:06:41 GMT  
		Size: 56.6 MB (56562945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edcf9db5a1b38af5bb9fdf73e674526ec2ea289819852645d9d188fad87bf21`  
		Last Modified: Tue, 05 Apr 2022 09:06:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c2e63c2fbfc1abb8e0d67e64b0f60853a2071bc30215f0a253be92cb274c6`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4adf978bd9de05949fabf35a650d95b209d0cf397d6a01c098b30cc4072089`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144701e366b871fd0167a7150ebd9e22e946ad67a354ed2ec7cb3871ee76bb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847d35ce919fdc67b9945f9238ecff157ddbabd7d47bcfd9897bfc32b81e3c5`  
		Last Modified: Tue, 05 Apr 2022 09:06:38 GMT  
		Size: 116.7 MB (116690887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341eef26fc26324a7ea91c42a1be66b6b8a7d8230c1df8986f8c6e22e2fa38d4`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 5.4 KB (5429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14.0`

```console
$ docker pull bonita@sha256:9bd37caef5943cf2cdc2a20993002c2d8d794f6f549da01f08ac9fdc56d2ae2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14.0` - linux; amd64

```console
$ docker pull bonita@sha256:aa6c404694792455f659ab29b685840a58847a82ee8d6b933510ab9b8d415e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791a1d923d653fa2c3fc2640e7509051adf42a471ba281268d753580e1da5f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:23:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 04:23:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 04:23:38 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 04:23:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 04:23:39 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 04:23:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:40 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 04:23:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 04:23:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 04:23:48 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 04:23:49 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 04:23:49 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 04:23:49 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 04:23:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 04:23:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff37705a3721b6f0fa369c96374cf9da30cff49af0d8000271ef496b3a770df`  
		Last Modified: Tue, 05 Apr 2022 04:24:23 GMT  
		Size: 60.7 MB (60744505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f66c34cc10d0cb3a031ef3da4ba3f1bd013bcc964d4956c60fad86f44fe69`  
		Last Modified: Tue, 05 Apr 2022 04:24:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578f03d3de8ca415ec7f424f8e565acd05fed61f7ae257c04a206815af3329f`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217417d523fc2999c4b2897458c8186aaae7637ca11cffcf678f5a94676243c3`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bafdba13f86b25d0530d42b1945be474d808e2e57c54eb92525278fd97b4066`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7700ffe2df31bc40779a5addc28e3643352992303bc5cd5013f722caeea46b`  
		Last Modified: Tue, 05 Apr 2022 04:24:20 GMT  
		Size: 116.7 MB (116690800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f64f512c1d336d8e3ad42228cc6f701c2f9ef296cccb6001395170ba33d88`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ec277986357bc1492ec4256aeb59f9509b5206166178468fae72d7b396672ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7da5778516cbbaa93e6b5f1f1812601e1ea647ac7f864ea7770f27872c6bf2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:09:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 03:09:35 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 03:09:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 03:09:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 03:09:37 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 03:09:38 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 03:09:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 03:09:40 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 03:09:41 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 03:09:42 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 03:09:43 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 03:09:44 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 03:09:45 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 03:09:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:48 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 03:09:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 03:09:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 03:09:58 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 03:09:59 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 03:10:00 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 03:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 03:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 03:10:03 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 03:10:04 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 03:10:05 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 03:10:06 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 03:10:07 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 03:10:08 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 03:10:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 03:10:10 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 03:10:12 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 03:10:12 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 03:10:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 03:10:14 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f256ad0fc5640d4ad6542e63ff033094b79f2158b7b837af471110ea8a336`  
		Last Modified: Tue, 05 Apr 2022 03:11:08 GMT  
		Size: 60.1 MB (60067315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f94323a629942950a0ffa4ebd9b9a9a67e2e99450c1b63b7caa029bb6fbab5`  
		Last Modified: Tue, 05 Apr 2022 03:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6976ee94f88624b6444d82e171da5997a9fc114743925400901581ea08c58`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5aabbb25b6ba30936e48e8d131ebfb29068a96236f7ce6e56f8aea4faafaf`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ba33b8f8be7b90a8de59a31f336886c4e754bd8846e3019ee792422b0c930`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 3.0 KB (3000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb65a72bf0159fbfb5326ef80a1e211664490a96659378c1d97748689b176279`  
		Last Modified: Tue, 05 Apr 2022 03:11:05 GMT  
		Size: 116.7 MB (116688761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b61e2452bca6bb834b08988d9199d49b4c4ffd3228c57b794b855215c36116`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:a8b99264c74f1637a78eb549f8e83bee8f0f2146850d2757e4d483465a901317
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176075045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766bd47323049c15860a8cea6025a09aab1552c1868c15db5ef57c14d7cc9633`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:02:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 09:02:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 09:02:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 09:03:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 09:03:03 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:03:05 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 09:03:09 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:03:12 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:03:16 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:03:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 09:03:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 09:03:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 09:03:31 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:03:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:46 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:03:49 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 09:04:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 09:04:13 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 09:04:16 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 09:04:20 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 09:04:24 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 09:04:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 09:04:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 09:04:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 09:04:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 09:04:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 09:04:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 09:04:50 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 09:04:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 09:04:59 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 09:05:01 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 09:05:03 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 09:05:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 09:05:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434586e006643fe98fc4f4804ae9fc2bda4db5b77b98a9fd444e497dfe6b0d0`  
		Last Modified: Tue, 05 Apr 2022 09:06:41 GMT  
		Size: 56.6 MB (56562945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edcf9db5a1b38af5bb9fdf73e674526ec2ea289819852645d9d188fad87bf21`  
		Last Modified: Tue, 05 Apr 2022 09:06:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c2e63c2fbfc1abb8e0d67e64b0f60853a2071bc30215f0a253be92cb274c6`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4adf978bd9de05949fabf35a650d95b209d0cf397d6a01c098b30cc4072089`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144701e366b871fd0167a7150ebd9e22e946ad67a354ed2ec7cb3871ee76bb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847d35ce919fdc67b9945f9238ecff157ddbabd7d47bcfd9897bfc32b81e3c5`  
		Last Modified: Tue, 05 Apr 2022 09:06:38 GMT  
		Size: 116.7 MB (116690887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341eef26fc26324a7ea91c42a1be66b6b8a7d8230c1df8986f8c6e22e2fa38d4`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 5.4 KB (5429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:9bd37caef5943cf2cdc2a20993002c2d8d794f6f549da01f08ac9fdc56d2ae2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:aa6c404694792455f659ab29b685840a58847a82ee8d6b933510ab9b8d415e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791a1d923d653fa2c3fc2640e7509051adf42a471ba281268d753580e1da5f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:23:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 04:23:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 04:23:38 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 04:23:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 04:23:39 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 04:23:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:40 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 04:23:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 04:23:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 04:23:48 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 04:23:49 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 04:23:49 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 04:23:49 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 04:23:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 04:23:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff37705a3721b6f0fa369c96374cf9da30cff49af0d8000271ef496b3a770df`  
		Last Modified: Tue, 05 Apr 2022 04:24:23 GMT  
		Size: 60.7 MB (60744505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f66c34cc10d0cb3a031ef3da4ba3f1bd013bcc964d4956c60fad86f44fe69`  
		Last Modified: Tue, 05 Apr 2022 04:24:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578f03d3de8ca415ec7f424f8e565acd05fed61f7ae257c04a206815af3329f`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217417d523fc2999c4b2897458c8186aaae7637ca11cffcf678f5a94676243c3`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bafdba13f86b25d0530d42b1945be474d808e2e57c54eb92525278fd97b4066`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7700ffe2df31bc40779a5addc28e3643352992303bc5cd5013f722caeea46b`  
		Last Modified: Tue, 05 Apr 2022 04:24:20 GMT  
		Size: 116.7 MB (116690800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f64f512c1d336d8e3ad42228cc6f701c2f9ef296cccb6001395170ba33d88`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ec277986357bc1492ec4256aeb59f9509b5206166178468fae72d7b396672ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7da5778516cbbaa93e6b5f1f1812601e1ea647ac7f864ea7770f27872c6bf2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:09:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 03:09:35 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 03:09:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 03:09:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 03:09:37 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 03:09:38 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 03:09:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 03:09:40 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 03:09:41 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 03:09:42 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 03:09:43 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 03:09:44 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 03:09:45 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 03:09:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:48 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 03:09:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 03:09:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 03:09:58 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 03:09:59 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 03:10:00 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 03:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 03:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 03:10:03 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 03:10:04 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 03:10:05 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 03:10:06 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 03:10:07 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 03:10:08 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 03:10:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 03:10:10 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 03:10:12 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 03:10:12 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 03:10:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 03:10:14 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f256ad0fc5640d4ad6542e63ff033094b79f2158b7b837af471110ea8a336`  
		Last Modified: Tue, 05 Apr 2022 03:11:08 GMT  
		Size: 60.1 MB (60067315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f94323a629942950a0ffa4ebd9b9a9a67e2e99450c1b63b7caa029bb6fbab5`  
		Last Modified: Tue, 05 Apr 2022 03:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6976ee94f88624b6444d82e171da5997a9fc114743925400901581ea08c58`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5aabbb25b6ba30936e48e8d131ebfb29068a96236f7ce6e56f8aea4faafaf`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ba33b8f8be7b90a8de59a31f336886c4e754bd8846e3019ee792422b0c930`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 3.0 KB (3000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb65a72bf0159fbfb5326ef80a1e211664490a96659378c1d97748689b176279`  
		Last Modified: Tue, 05 Apr 2022 03:11:05 GMT  
		Size: 116.7 MB (116688761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b61e2452bca6bb834b08988d9199d49b4c4ffd3228c57b794b855215c36116`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:a8b99264c74f1637a78eb549f8e83bee8f0f2146850d2757e4d483465a901317
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176075045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766bd47323049c15860a8cea6025a09aab1552c1868c15db5ef57c14d7cc9633`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:02:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 09:02:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 09:02:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 09:03:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 09:03:03 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:03:05 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 09:03:09 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:03:12 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:03:16 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:03:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 09:03:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 09:03:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 09:03:31 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:03:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:46 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:03:49 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 09:04:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 09:04:13 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 09:04:16 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 09:04:20 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 09:04:24 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 09:04:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 09:04:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 09:04:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 09:04:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 09:04:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 09:04:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 09:04:50 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 09:04:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 09:04:59 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 09:05:01 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 09:05:03 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 09:05:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 09:05:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434586e006643fe98fc4f4804ae9fc2bda4db5b77b98a9fd444e497dfe6b0d0`  
		Last Modified: Tue, 05 Apr 2022 09:06:41 GMT  
		Size: 56.6 MB (56562945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edcf9db5a1b38af5bb9fdf73e674526ec2ea289819852645d9d188fad87bf21`  
		Last Modified: Tue, 05 Apr 2022 09:06:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c2e63c2fbfc1abb8e0d67e64b0f60853a2071bc30215f0a253be92cb274c6`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4adf978bd9de05949fabf35a650d95b209d0cf397d6a01c098b30cc4072089`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144701e366b871fd0167a7150ebd9e22e946ad67a354ed2ec7cb3871ee76bb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847d35ce919fdc67b9945f9238ecff157ddbabd7d47bcfd9897bfc32b81e3c5`  
		Last Modified: Tue, 05 Apr 2022 09:06:38 GMT  
		Size: 116.7 MB (116690887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341eef26fc26324a7ea91c42a1be66b6b8a7d8230c1df8986f8c6e22e2fa38d4`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 5.4 KB (5429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
