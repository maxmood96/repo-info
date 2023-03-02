<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2021.1`](#bonita20211)
-	[`bonita:2021.2`](#bonita20212)
-	[`bonita:2021.2-u0`](#bonita20212-u0)
-	[`bonita:2022.1`](#bonita20221)
-	[`bonita:2022.1-u0`](#bonita20221-u0)
-	[`bonita:2022.2`](#bonita20222)
-	[`bonita:2022.2-u0`](#bonita20222-u0)
-	[`bonita:7.12`](#bonita712)
-	[`bonita:7.12.1`](#bonita7121)
-	[`bonita:7.13`](#bonita713)
-	[`bonita:7.13.0`](#bonita7130)
-	[`bonita:7.14`](#bonita714)
-	[`bonita:7.14.0`](#bonita7140)
-	[`bonita:7.15`](#bonita715)
-	[`bonita:7.15.0`](#bonita7150)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2021.1`

```console
$ docker pull bonita@sha256:e9e7272ebaf28c4f0615859af62ed1d3633d271f8d604f17cf34c1411158cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:b8cab40aa3d32c2f0c4652ec23412dec17ad22f2badb3b65cd4507f0785b39ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235199961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a032ff4420d6a2d6c74c9a1474b0f11e0803242ab946951b59ff3a77ad1a7`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 20:22:07 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 20:23:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 20:23:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 20:23:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 20:23:31 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Jan 2023 20:23:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 20:23:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Jan 2023 20:23:33 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 20:23:33 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Jan 2023 20:23:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Jan 2023 20:23:42 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Jan 2023 20:23:44 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Jan 2023 20:23:44 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 20:23:44 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 20:23:44 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 20:23:44 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7328ec4a801f0ca840972017aea45def56308ec5cba3c331787ffb44d3eac66`  
		Last Modified: Tue, 31 Jan 2023 20:25:16 GMT  
		Size: 91.6 MB (91555780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818f4e3f37cf9db739a87c3e0b5531b2b79b229b7ca649ca81d92a7b292842f`  
		Last Modified: Tue, 31 Jan 2023 20:25:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97679340a72be5274f67677e7287ef10be57d3c23bdb65ce6796e99ac1bfeb71`  
		Last Modified: Tue, 31 Jan 2023 20:25:04 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65264dbf9351cac3a5ed13251053a8007d6b23e971aa4a61cdf49ca7fa9e30c`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 506.3 KB (506347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4e6b556bfacd17c87d71fe2055ae9653f247130c0784953e8cbacaee80a252`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af10439a3473a952f6a287bea286b506668833d65a7fbf5525d170a9af6a8bba`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 6.9 KB (6941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffabc92591d5293700dafb8846f22891b91216f2079300759b899716f819d99`  
		Last Modified: Tue, 31 Jan 2023 20:25:08 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1ef8d07e1bac9fe0c9a0ae4b87a11211a2b872c6d7532f85ecfa9aa082765`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ea94c68131d6d44d582f4be6e04230227f3f731f5bcbfbf73550277e3e2e0e79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226706515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8322c5e58f12ac21f77cd8c6b198982012e2218f313b048832d34641cace78`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:06:44 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 02 Mar 2023 02:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:08:10 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 02 Mar 2023 02:08:11 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 02 Mar 2023 02:08:14 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BONITA_VERSION
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BRANDING_VERSION
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BONITA_SHA256
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BASE_URL
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BONITA_URL
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 02 Mar 2023 02:08:15 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 02 Mar 2023 02:08:16 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 02 Mar 2023 02:08:16 GMT
RUN mkdir /opt/files
# Thu, 02 Mar 2023 02:08:16 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 02 Mar 2023 02:08:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 02 Mar 2023 02:08:25 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 02 Mar 2023 02:08:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 02 Mar 2023 02:08:26 GMT
VOLUME [/opt/bonita]
# Thu, 02 Mar 2023 02:08:26 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 02 Mar 2023 02:08:26 GMT
EXPOSE 8080
# Thu, 02 Mar 2023 02:08:26 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:9de1bca73074c336fb93a7688a40903c720a195929a0da27bd4ea424d5817c78`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 23.7 MB (23733538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6f8c688bd3ccf7157aeee1c49333e977721b1470062452e844ef68c303c8af`  
		Last Modified: Thu, 02 Mar 2023 02:09:57 GMT  
		Size: 86.1 MB (86070944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0876628926e6159ed8e68395f1859141e8a4cd3d7e70d05cf12b6071d12909b3`  
		Last Modified: Thu, 02 Mar 2023 02:09:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7d3ea37a586be245c30401cfc13a806692adeaf6e5dae529170b7b12a2258d`  
		Last Modified: Thu, 02 Mar 2023 02:09:48 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996fdc9a7159608270265f22ba62b525b4642b52daead040fad7c81d16262399`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 475.8 KB (475798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123396bdb84cd6d9664aeffa96282e9d21b03264eabb833db2b4bd6e07848a02`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbf65f28cf93495acd928f9533dbf10bd28329dd11098100128f79a68d99869`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed41a3e54cb9ffa4dbaa7cd2d89e6bc774523eef3115c66e7a014239545e6aac`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f887bd4a303e9aaa73ff24e9f9164cdbbba4c2566f04130fd7c57658d5f716`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:2b9ea6b78681b7a9be289d12610c393f6cbf085f288f14981efc118e43e0bdd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234190094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c892c407585638a2a7b05efdfb724550d26ffae06a421b2be008938a69d7322`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:41:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 19:43:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:43:29 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 19:43:31 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 19:43:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 19:43:35 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 19:43:36 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 19:43:36 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 19:43:36 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 19:43:37 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 19:43:38 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Jan 2023 19:43:38 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Jan 2023 19:43:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Jan 2023 19:43:39 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 19:43:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 19:43:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 19:43:41 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Jan 2023 19:43:42 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 19:43:43 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Jan 2023 19:43:51 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Jan 2023 19:43:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Jan 2023 19:43:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Jan 2023 19:43:57 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 19:43:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 19:43:58 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 19:43:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dec4dcee66042a87e0e5551837258f90b916e09f049946007420a0f691de9f`  
		Last Modified: Tue, 31 Jan 2023 19:47:02 GMT  
		Size: 86.8 MB (86845915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2b031382ecb158c362b2e064bcaa11898a7dc3332f3cef6c0d2d1b63d94983`  
		Last Modified: Tue, 31 Jan 2023 19:46:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf8982c80714bee8016edb384cfb022ecb0bb7fed71affbf59dc2422ca7389a`  
		Last Modified: Tue, 31 Jan 2023 19:46:42 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be7c94c68f6e9570d2a9cd4d784e1b00ecd8bebd114d64db134740061f216d`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1990afbb6ef5e6700cad031b0c60037d83a9707861bf315306189d3da7c600`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070fc5f1bb9687c8c4ce1b05efbe0bf92f48c3f23425beaa70a8f674891e7a92`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316fa544506415f88d616f984732dc77964260a9514ae096938e37e10c376bef`  
		Last Modified: Tue, 31 Jan 2023 19:46:48 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a7eee6b49e407ca9bf283e00d9ea0be41d4714669159bb6818903fe4f142e8`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:0a3229aec1faf58c4230141a14b940d487f94972153cc49effc857d2eca8f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:fd0be2bc8b1b3580520d1c941b5c32c9e5f8974123203f851868a1c7923612a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232933233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63865f3dedcce11b2c96983ce415b3d98f2497f8731226bc724efeddf4ec0f4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 20:22:07 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 20:24:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 20:24:22 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 20:24:23 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 20:24:26 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 20:24:26 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 20:24:26 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 31 Jan 2023 20:24:27 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 20:24:28 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 20:24:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 31 Jan 2023 20:24:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 31 Jan 2023 20:24:34 GMT
ENV HTTP_API=false
# Tue, 31 Jan 2023 20:24:34 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 20:24:35 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 20:24:35 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 20:24:36 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba97969dd85d91907f2fc0705dabba826046cd6fead565759517131d1e27e88`  
		Last Modified: Tue, 31 Jan 2023 20:25:41 GMT  
		Size: 91.6 MB (91556051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4afd30cea7c96ad48fb9e0289edf467e408a8ea32f9c5a45650434f42e6e7d`  
		Last Modified: Tue, 31 Jan 2023 20:25:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b957206dc389298bf529853e92c39823dfe21e4335c35dde6bf4e92f12a3749c`  
		Last Modified: Tue, 31 Jan 2023 20:25:29 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4ddaf1e60c0dfff663d7b7c459a936685d45a1d073c4f06a161c8e58e22c35`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 930.5 KB (930473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b40a0d125e823df55ddcd338431fce9ae79df87d2394773d06019a391adec2`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ec9aa87334c9042ff31cfeaff83c1a3c14e6b3fcba091496b094952f25aa58`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c5ff3727ffb3ab343809ff323ddf2c855264021508d2e79496dd73b95e11d5`  
		Last Modified: Tue, 31 Jan 2023 20:25:33 GMT  
		Size: 113.7 MB (113727922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56eba647c73536d78afc9c24ffb78ea2d7804cec60c77780ab0126ac2e16e521`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2a8f5fef5eca108ec1fc148fdfb9fdd19f842f82d7e242091e09a8c897068a20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224399012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a867bcf236ff6e26005fc5aad844c87c05a9a2066260056f0b78a82fc86e571`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:06:44 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 02 Mar 2023 02:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:08:54 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 02 Mar 2023 02:08:54 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 02 Mar 2023 02:08:57 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BONITA_VERSION
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BRANDING_VERSION
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BONITA_SHA256
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BASE_URL
# Thu, 02 Mar 2023 02:08:58 GMT
ARG BONITA_URL
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 02 Mar 2023 02:08:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 02 Mar 2023 02:08:58 GMT
RUN mkdir /opt/files
# Thu, 02 Mar 2023 02:08:59 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 02 Mar 2023 02:09:13 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 02 Mar 2023 02:09:13 GMT
ENV HTTP_API=false
# Thu, 02 Mar 2023 02:09:14 GMT
VOLUME [/opt/bonita]
# Thu, 02 Mar 2023 02:09:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 02 Mar 2023 02:09:15 GMT
EXPOSE 8080
# Thu, 02 Mar 2023 02:09:17 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:9de1bca73074c336fb93a7688a40903c720a195929a0da27bd4ea424d5817c78`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 23.7 MB (23733538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fbb063e5c589f703cb3aeaee5c7c9724dbc799fe4719975633002505b8cf85`  
		Last Modified: Thu, 02 Mar 2023 02:10:19 GMT  
		Size: 86.1 MB (86070784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8c7f9af646ae3452dccc5b4504b78a3e1310b5967bd7027ad925e16ea6e7ac`  
		Last Modified: Thu, 02 Mar 2023 02:10:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e365ae68182fc69902d7d6c7f07e90ee959f615c925c91b051f771206573cd`  
		Last Modified: Thu, 02 Mar 2023 02:10:10 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0709ab65a352fffcc2b1c4f4455ee221dd0a3d8bcfa525b53886936ff9bc24`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 859.6 KB (859577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4d382643865f1584f3c8463b0c5c34cbe7817c5c9a46f28ccb9253490f6fee`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef04571e8ea7c8bca7678990add92f6e3df7cdf1cda1ef6b5679bbc6f885795a`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb828964136d3d92ee0a8d9811d377b7cc856039cb02a785e0d57083cf391ec`  
		Last Modified: Thu, 02 Mar 2023 02:10:13 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0307f9b5c2a9de64b005fc2d39e9aea2faa0f1164124b048e1d7c26f0dbf129`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:93391aa63425871df905e44d51cc0166c7e2ad8e54663a9dbb3040db48482e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231855236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be14cd370871d6210aa189b077498e1885375518794b71d6b6f4251b06de737`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:41:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 19:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:45:05 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 19:45:07 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 19:45:11 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 19:45:11 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 19:45:12 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 19:45:12 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 19:45:13 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 19:45:13 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 19:45:14 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 31 Jan 2023 19:45:14 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 31 Jan 2023 19:45:15 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 31 Jan 2023 19:45:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 19:45:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 19:45:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 19:45:18 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 19:45:18 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 31 Jan 2023 19:45:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 31 Jan 2023 19:45:34 GMT
ENV HTTP_API=false
# Tue, 31 Jan 2023 19:45:36 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 19:45:37 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 19:45:38 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 19:45:41 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7207648cefd934054d20bbcd76538dcb17b703a45aa2f7f4729e42b73eac094a`  
		Last Modified: Tue, 31 Jan 2023 19:47:38 GMT  
		Size: 86.8 MB (86845963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ee4eedc705e1187ff40602b65ece479b94e94a8a0cec74d68d166d530b4605`  
		Last Modified: Tue, 31 Jan 2023 19:47:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44082f9095e3ee7114fbed16930ebb78c54dc34780c156ee94736d276f63f68f`  
		Last Modified: Tue, 31 Jan 2023 19:47:18 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4307ede583209a0e3993a75be9c39ac1df424bd286a4971afc40a3dcb14a92bb`  
		Last Modified: Tue, 31 Jan 2023 19:47:17 GMT  
		Size: 831.6 KB (831571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a632a969fcf59bc731d0ad0c54f8cca5e568adf40d793be80f09605804712ba`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e810a25780c832ebeaa4cbc19dc01c93823e11ed41dcc5208625f1b65d7fd5cc`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d720760489ab042105da1fc12b16912e12c80856a76f4dac753114c0623a39bf`  
		Last Modified: Tue, 31 Jan 2023 19:47:27 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f9b039eb20902e8dfa61ac9f02d41ecff0a57fc10ab41e37a804dd32585b16`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:0a3229aec1faf58c4230141a14b940d487f94972153cc49effc857d2eca8f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:fd0be2bc8b1b3580520d1c941b5c32c9e5f8974123203f851868a1c7923612a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232933233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63865f3dedcce11b2c96983ce415b3d98f2497f8731226bc724efeddf4ec0f4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 20:22:07 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 20:24:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 20:24:22 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 20:24:23 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 20:24:26 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 20:24:26 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 20:24:26 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 31 Jan 2023 20:24:27 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 20:24:28 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 20:24:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 31 Jan 2023 20:24:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 31 Jan 2023 20:24:34 GMT
ENV HTTP_API=false
# Tue, 31 Jan 2023 20:24:34 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 20:24:35 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 20:24:35 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 20:24:36 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba97969dd85d91907f2fc0705dabba826046cd6fead565759517131d1e27e88`  
		Last Modified: Tue, 31 Jan 2023 20:25:41 GMT  
		Size: 91.6 MB (91556051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4afd30cea7c96ad48fb9e0289edf467e408a8ea32f9c5a45650434f42e6e7d`  
		Last Modified: Tue, 31 Jan 2023 20:25:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b957206dc389298bf529853e92c39823dfe21e4335c35dde6bf4e92f12a3749c`  
		Last Modified: Tue, 31 Jan 2023 20:25:29 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4ddaf1e60c0dfff663d7b7c459a936685d45a1d073c4f06a161c8e58e22c35`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 930.5 KB (930473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b40a0d125e823df55ddcd338431fce9ae79df87d2394773d06019a391adec2`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ec9aa87334c9042ff31cfeaff83c1a3c14e6b3fcba091496b094952f25aa58`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c5ff3727ffb3ab343809ff323ddf2c855264021508d2e79496dd73b95e11d5`  
		Last Modified: Tue, 31 Jan 2023 20:25:33 GMT  
		Size: 113.7 MB (113727922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56eba647c73536d78afc9c24ffb78ea2d7804cec60c77780ab0126ac2e16e521`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2a8f5fef5eca108ec1fc148fdfb9fdd19f842f82d7e242091e09a8c897068a20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224399012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a867bcf236ff6e26005fc5aad844c87c05a9a2066260056f0b78a82fc86e571`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:06:44 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 02 Mar 2023 02:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:08:54 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 02 Mar 2023 02:08:54 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 02 Mar 2023 02:08:57 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BONITA_VERSION
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BRANDING_VERSION
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BONITA_SHA256
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BASE_URL
# Thu, 02 Mar 2023 02:08:58 GMT
ARG BONITA_URL
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 02 Mar 2023 02:08:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 02 Mar 2023 02:08:58 GMT
RUN mkdir /opt/files
# Thu, 02 Mar 2023 02:08:59 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 02 Mar 2023 02:09:13 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 02 Mar 2023 02:09:13 GMT
ENV HTTP_API=false
# Thu, 02 Mar 2023 02:09:14 GMT
VOLUME [/opt/bonita]
# Thu, 02 Mar 2023 02:09:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 02 Mar 2023 02:09:15 GMT
EXPOSE 8080
# Thu, 02 Mar 2023 02:09:17 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:9de1bca73074c336fb93a7688a40903c720a195929a0da27bd4ea424d5817c78`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 23.7 MB (23733538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fbb063e5c589f703cb3aeaee5c7c9724dbc799fe4719975633002505b8cf85`  
		Last Modified: Thu, 02 Mar 2023 02:10:19 GMT  
		Size: 86.1 MB (86070784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8c7f9af646ae3452dccc5b4504b78a3e1310b5967bd7027ad925e16ea6e7ac`  
		Last Modified: Thu, 02 Mar 2023 02:10:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e365ae68182fc69902d7d6c7f07e90ee959f615c925c91b051f771206573cd`  
		Last Modified: Thu, 02 Mar 2023 02:10:10 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0709ab65a352fffcc2b1c4f4455ee221dd0a3d8bcfa525b53886936ff9bc24`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 859.6 KB (859577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4d382643865f1584f3c8463b0c5c34cbe7817c5c9a46f28ccb9253490f6fee`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef04571e8ea7c8bca7678990add92f6e3df7cdf1cda1ef6b5679bbc6f885795a`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb828964136d3d92ee0a8d9811d377b7cc856039cb02a785e0d57083cf391ec`  
		Last Modified: Thu, 02 Mar 2023 02:10:13 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0307f9b5c2a9de64b005fc2d39e9aea2faa0f1164124b048e1d7c26f0dbf129`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:93391aa63425871df905e44d51cc0166c7e2ad8e54663a9dbb3040db48482e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231855236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be14cd370871d6210aa189b077498e1885375518794b71d6b6f4251b06de737`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:41:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 19:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:45:05 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 19:45:07 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 19:45:11 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 19:45:11 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 19:45:12 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 19:45:12 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 19:45:13 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 19:45:13 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 19:45:14 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 31 Jan 2023 19:45:14 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 31 Jan 2023 19:45:15 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 31 Jan 2023 19:45:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 19:45:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 19:45:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 19:45:18 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 19:45:18 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 31 Jan 2023 19:45:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 31 Jan 2023 19:45:34 GMT
ENV HTTP_API=false
# Tue, 31 Jan 2023 19:45:36 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 19:45:37 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 19:45:38 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 19:45:41 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7207648cefd934054d20bbcd76538dcb17b703a45aa2f7f4729e42b73eac094a`  
		Last Modified: Tue, 31 Jan 2023 19:47:38 GMT  
		Size: 86.8 MB (86845963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ee4eedc705e1187ff40602b65ece479b94e94a8a0cec74d68d166d530b4605`  
		Last Modified: Tue, 31 Jan 2023 19:47:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44082f9095e3ee7114fbed16930ebb78c54dc34780c156ee94736d276f63f68f`  
		Last Modified: Tue, 31 Jan 2023 19:47:18 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4307ede583209a0e3993a75be9c39ac1df424bd286a4971afc40a3dcb14a92bb`  
		Last Modified: Tue, 31 Jan 2023 19:47:17 GMT  
		Size: 831.6 KB (831571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a632a969fcf59bc731d0ad0c54f8cca5e568adf40d793be80f09605804712ba`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e810a25780c832ebeaa4cbc19dc01c93823e11ed41dcc5208625f1b65d7fd5cc`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d720760489ab042105da1fc12b16912e12c80856a76f4dac753114c0623a39bf`  
		Last Modified: Tue, 31 Jan 2023 19:47:27 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f9b039eb20902e8dfa61ac9f02d41ecff0a57fc10ab41e37a804dd32585b16`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1`

```console
$ docker pull bonita@sha256:2f3c5eed0c94710458be82864edbe4ba9178d8135c9df47799216985906b6002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1` - linux; amd64

```console
$ docker pull bonita@sha256:02b3824ad75e32956ee983c1496672784d05c33a9be1f0128785b8c39353a978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176984103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32baedb9bbed9762a558ee13a022cc8010e548f3b59d0f457c42e8b5ceacb36`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:36:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 11 Feb 2023 07:36:25 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 11 Feb 2023 07:36:26 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 11 Feb 2023 07:36:26 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_VERSION
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BRANDING_VERSION
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_SHA256
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BASE_URL
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_URL
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 11 Feb 2023 07:36:27 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 11 Feb 2023 07:36:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 11 Feb 2023 07:36:28 GMT
RUN mkdir /opt/files
# Sat, 11 Feb 2023 07:36:28 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 11 Feb 2023 07:36:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API_PASSWORD=
# Sat, 11 Feb 2023 07:36:38 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 11 Feb 2023 07:36:38 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 11 Feb 2023 07:36:38 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 11 Feb 2023 07:36:39 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 11 Feb 2023 07:36:39 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 11 Feb 2023 07:36:39 GMT
EXPOSE 8080 9000
# Sat, 11 Feb 2023 07:36:39 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 11 Feb 2023 07:36:39 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230ac87c111c758dc330d34eec96b2fd040464085514c8bc299cc3ae6301bef`  
		Last Modified: Sat, 11 Feb 2023 07:37:49 GMT  
		Size: 57.5 MB (57457146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a94688547e8089bcb2955a83b3c000f4626945038edf17b181125190ed03cb2`  
		Last Modified: Sat, 11 Feb 2023 07:37:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801d3c8a6716925340bd1cba3509d4ed3ae9e214f42c3034e737f45e8976e10e`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762f5ac5ff165059fc8cb51b0ece4cc382c58bc04983a796e5df877f5800c95`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0ea9043ed6c4923c0f23d917a58009babceba34bd649442325f0b361d86aa2`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4c1ac5378dd5377fa6af775a4285f79537da5cc2e31082ddd1bf022e10c76b`  
		Last Modified: Sat, 11 Feb 2023 07:37:46 GMT  
		Size: 116.7 MB (116690797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eef05f4a0072c0d1417d0aeb36743fd44aef8f908913ab18244ff757658b7e2`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4369e5cb8a74d976d78b4cdc4c8393f501cc63a2914e61e652ea4d9c8e0b1c25
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176202935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0d03b50d68ea6eba6c765b08a84d909c5a2968c58a0f53ceea419be6d4e26b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:58:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 21:58:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 10 Feb 2023 21:58:46 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 21:58:47 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 21:58:47 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 10 Feb 2023 21:58:47 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 10 Feb 2023 21:58:48 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 21:58:48 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 21:58:48 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 10 Feb 2023 21:58:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 21:58:56 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 21:58:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 21:58:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 21:58:57 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 21:58:57 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 21:58:57 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 21:58:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 21:58:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e2109a84b98be453581984099b1e5905de15709f8462fd01ef9041a975f814`  
		Last Modified: Fri, 10 Feb 2023 21:59:49 GMT  
		Size: 56.8 MB (56780552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d915f6aab23e3a3243f320b98942b39e4269dda6727389cb292505d57d87070e`  
		Last Modified: Fri, 10 Feb 2023 21:59:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13344da817627abfaaa8f998dca6d0a93349f5ddcf1482d4b776cc634482722`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a9c725a2f28d4e241d63208dcbef03c7263a01889033998aacae2aeacd8671`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a436099d21c84764dfe4832afa1166dd2ddf43f451d49e56e47eb787a51e3c`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c55eb4882b2e4f60cc8a7a133b428594bcda8bf05708361f476857e093eb45b`  
		Last Modified: Fri, 10 Feb 2023 21:59:47 GMT  
		Size: 116.7 MB (116690810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5e9fd1bc9c10621aa7c5211a6b1be870cef856d036184db08a692c8b9aa953`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:0191aeef4a5882edad729e7ba9d3f866e05e9f7767dcbf4faa1c3abe4656a14d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172793970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cf165f9ce9e1a5741cbecbaa9df6eb357cbc2e0dfd8d0ebcb7d42d4023e924`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:52 GMT
ADD file:0db937922cfd604e84e5df7ed3bfe476af7113be3c4c1e216653f249fdacfd44 in / 
# Fri, 10 Feb 2023 21:20:53 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:09:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 22:09:28 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 10 Feb 2023 22:09:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 22:09:33 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 22:09:34 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 22:09:34 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 22:09:35 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 22:09:35 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 22:09:36 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 22:09:36 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 10 Feb 2023 22:09:36 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 10 Feb 2023 22:09:37 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 10 Feb 2023 22:09:38 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 22:09:38 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 22:09:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 22:09:40 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 22:09:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 10 Feb 2023 22:09:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 22:10:00 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 22:10:01 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 22:10:01 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 22:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 22:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 22:10:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 22:10:03 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 22:10:03 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 22:10:04 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 22:10:05 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 22:10:05 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 22:10:06 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 22:10:07 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 22:10:07 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 22:10:08 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 22:10:08 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 22:10:09 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5b42622f88c38596f558fe14b894eadc782d1b003f25d0374cf41bc92e716959`  
		Last Modified: Fri, 10 Feb 2023 21:22:05 GMT  
		Size: 2.8 MB (2813687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b13d8f05b508a7505125aca30065be998cdcdfca17cae08199630f66f2a5e8`  
		Last Modified: Fri, 10 Feb 2023 22:12:14 GMT  
		Size: 53.3 MB (53279469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541b2abe2c930f64fff252af8183fa8af7c1399a60f573966c284dc87cd102e`  
		Last Modified: Fri, 10 Feb 2023 22:12:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d999c19e37140fdfc6a79ddef921f4899f76153ac6f98ec4255ca7bbbe3836b6`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dff5215400cc8e206e0b8f5b659548d5dfc3248de04f06067851bc28a6ada54`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e3033fffec12c9bdde2e22b8daa43f15df18b4a70c0e2ddaf82e290e98b81d`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890d23e1786c784e08495019b2d059220016be2524706f6172eebcd6982a4d34`  
		Last Modified: Fri, 10 Feb 2023 22:12:10 GMT  
		Size: 116.7 MB (116690801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209e978febf076cfc30ca2cb9b6e22a75956a313738f3aea8821c2a339a12a20`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1-u0`

```console
$ docker pull bonita@sha256:2f3c5eed0c94710458be82864edbe4ba9178d8135c9df47799216985906b6002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:02b3824ad75e32956ee983c1496672784d05c33a9be1f0128785b8c39353a978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176984103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32baedb9bbed9762a558ee13a022cc8010e548f3b59d0f457c42e8b5ceacb36`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:36:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 11 Feb 2023 07:36:25 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 11 Feb 2023 07:36:26 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 11 Feb 2023 07:36:26 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_VERSION
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BRANDING_VERSION
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_SHA256
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BASE_URL
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_URL
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 11 Feb 2023 07:36:27 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 11 Feb 2023 07:36:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 11 Feb 2023 07:36:28 GMT
RUN mkdir /opt/files
# Sat, 11 Feb 2023 07:36:28 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 11 Feb 2023 07:36:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API_PASSWORD=
# Sat, 11 Feb 2023 07:36:38 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 11 Feb 2023 07:36:38 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 11 Feb 2023 07:36:38 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 11 Feb 2023 07:36:39 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 11 Feb 2023 07:36:39 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 11 Feb 2023 07:36:39 GMT
EXPOSE 8080 9000
# Sat, 11 Feb 2023 07:36:39 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 11 Feb 2023 07:36:39 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230ac87c111c758dc330d34eec96b2fd040464085514c8bc299cc3ae6301bef`  
		Last Modified: Sat, 11 Feb 2023 07:37:49 GMT  
		Size: 57.5 MB (57457146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a94688547e8089bcb2955a83b3c000f4626945038edf17b181125190ed03cb2`  
		Last Modified: Sat, 11 Feb 2023 07:37:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801d3c8a6716925340bd1cba3509d4ed3ae9e214f42c3034e737f45e8976e10e`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762f5ac5ff165059fc8cb51b0ece4cc382c58bc04983a796e5df877f5800c95`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0ea9043ed6c4923c0f23d917a58009babceba34bd649442325f0b361d86aa2`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4c1ac5378dd5377fa6af775a4285f79537da5cc2e31082ddd1bf022e10c76b`  
		Last Modified: Sat, 11 Feb 2023 07:37:46 GMT  
		Size: 116.7 MB (116690797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eef05f4a0072c0d1417d0aeb36743fd44aef8f908913ab18244ff757658b7e2`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4369e5cb8a74d976d78b4cdc4c8393f501cc63a2914e61e652ea4d9c8e0b1c25
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176202935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0d03b50d68ea6eba6c765b08a84d909c5a2968c58a0f53ceea419be6d4e26b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:58:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 21:58:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 10 Feb 2023 21:58:46 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 21:58:47 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 21:58:47 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 10 Feb 2023 21:58:47 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 10 Feb 2023 21:58:48 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 21:58:48 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 21:58:48 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 10 Feb 2023 21:58:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 21:58:56 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 21:58:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 21:58:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 21:58:57 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 21:58:57 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 21:58:57 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 21:58:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 21:58:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e2109a84b98be453581984099b1e5905de15709f8462fd01ef9041a975f814`  
		Last Modified: Fri, 10 Feb 2023 21:59:49 GMT  
		Size: 56.8 MB (56780552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d915f6aab23e3a3243f320b98942b39e4269dda6727389cb292505d57d87070e`  
		Last Modified: Fri, 10 Feb 2023 21:59:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13344da817627abfaaa8f998dca6d0a93349f5ddcf1482d4b776cc634482722`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a9c725a2f28d4e241d63208dcbef03c7263a01889033998aacae2aeacd8671`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a436099d21c84764dfe4832afa1166dd2ddf43f451d49e56e47eb787a51e3c`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c55eb4882b2e4f60cc8a7a133b428594bcda8bf05708361f476857e093eb45b`  
		Last Modified: Fri, 10 Feb 2023 21:59:47 GMT  
		Size: 116.7 MB (116690810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5e9fd1bc9c10621aa7c5211a6b1be870cef856d036184db08a692c8b9aa953`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:0191aeef4a5882edad729e7ba9d3f866e05e9f7767dcbf4faa1c3abe4656a14d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172793970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cf165f9ce9e1a5741cbecbaa9df6eb357cbc2e0dfd8d0ebcb7d42d4023e924`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:52 GMT
ADD file:0db937922cfd604e84e5df7ed3bfe476af7113be3c4c1e216653f249fdacfd44 in / 
# Fri, 10 Feb 2023 21:20:53 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:09:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 22:09:28 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 10 Feb 2023 22:09:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 22:09:33 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 22:09:34 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 22:09:34 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 22:09:35 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 22:09:35 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 22:09:36 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 22:09:36 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 10 Feb 2023 22:09:36 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 10 Feb 2023 22:09:37 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 10 Feb 2023 22:09:38 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 22:09:38 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 22:09:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 22:09:40 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 22:09:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 10 Feb 2023 22:09:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 22:10:00 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 22:10:01 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 22:10:01 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 22:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 22:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 22:10:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 22:10:03 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 22:10:03 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 22:10:04 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 22:10:05 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 22:10:05 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 22:10:06 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 22:10:07 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 22:10:07 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 22:10:08 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 22:10:08 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 22:10:09 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5b42622f88c38596f558fe14b894eadc782d1b003f25d0374cf41bc92e716959`  
		Last Modified: Fri, 10 Feb 2023 21:22:05 GMT  
		Size: 2.8 MB (2813687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b13d8f05b508a7505125aca30065be998cdcdfca17cae08199630f66f2a5e8`  
		Last Modified: Fri, 10 Feb 2023 22:12:14 GMT  
		Size: 53.3 MB (53279469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541b2abe2c930f64fff252af8183fa8af7c1399a60f573966c284dc87cd102e`  
		Last Modified: Fri, 10 Feb 2023 22:12:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d999c19e37140fdfc6a79ddef921f4899f76153ac6f98ec4255ca7bbbe3836b6`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dff5215400cc8e206e0b8f5b659548d5dfc3248de04f06067851bc28a6ada54`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e3033fffec12c9bdde2e22b8daa43f15df18b4a70c0e2ddaf82e290e98b81d`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890d23e1786c784e08495019b2d059220016be2524706f6172eebcd6982a4d34`  
		Last Modified: Fri, 10 Feb 2023 22:12:10 GMT  
		Size: 116.7 MB (116690801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209e978febf076cfc30ca2cb9b6e22a75956a313738f3aea8821c2a339a12a20`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.2`

```console
$ docker pull bonita@sha256:5a83ae61e42cdf265917c0901b79134a23e53b492e378282ad6ca527abe3e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2` - linux; amd64

```console
$ docker pull bonita@sha256:5d3ed4fd9f9d4cdbd623c66c5f2860105b17a18dc81152fd50709a6ac470caab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183375338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e19cd7ca4a306326e953fe500c4dd7bcf5e01b828fb0e84fd9cea954021a4ed`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:36:45 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 11 Feb 2023 07:36:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 11 Feb 2023 07:36:50 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 11 Feb 2023 07:36:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 11 Feb 2023 07:36:50 GMT
ARG BONITA_VERSION
# Sat, 11 Feb 2023 07:36:50 GMT
ARG BRANDING_VERSION
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BONITA_SHA256
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BASE_URL
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BONITA_URL
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 11 Feb 2023 07:36:51 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 11 Feb 2023 07:36:52 GMT
RUN mkdir /opt/files
# Sat, 11 Feb 2023 07:36:52 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 11 Feb 2023 07:37:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API_PASSWORD=
# Sat, 11 Feb 2023 07:37:12 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 11 Feb 2023 07:37:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 11 Feb 2023 07:37:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 11 Feb 2023 07:37:13 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 11 Feb 2023 07:37:13 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 11 Feb 2023 07:37:13 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 11 Feb 2023 07:37:13 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 11 Feb 2023 07:37:13 GMT
EXPOSE 8080 9000
# Sat, 11 Feb 2023 07:37:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 11 Feb 2023 07:37:13 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf6663e45425c152dfb7992b8c9eeb8d6cec3a4dc529df5805b63922a919b64`  
		Last Modified: Sat, 11 Feb 2023 07:38:13 GMT  
		Size: 61.4 MB (61364554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298fdbc8a6aaea5b1d47cf5e79516539019c8e4c801d07fab88568ea817933d2`  
		Last Modified: Sat, 11 Feb 2023 07:38:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6169c4b44f713d85daee9434e474d8ddb8ef418b07f2d84ed36b0ec3d86edf`  
		Last Modified: Sat, 11 Feb 2023 07:38:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda69351f0fed8d72a5e23d7b509a47ad85c0e095b97d21c648c7a9488aa8116`  
		Last Modified: Sat, 11 Feb 2023 07:38:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b74363046ff94dc8eac9b9006983ab60391b31d9d704a149b1c0ef0c45eeb9b`  
		Last Modified: Sat, 11 Feb 2023 07:38:03 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8497c92ada3f978eb9372afb70a400410a94485630824181b17ab5d0d07ecf`  
		Last Modified: Sat, 11 Feb 2023 07:38:09 GMT  
		Size: 119.2 MB (119192991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5401586f5efd8c65188ba61cda06c3a90b327feb812fedb4c5892af335e5f118`  
		Last Modified: Sat, 11 Feb 2023 07:38:02 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:d27829cdf839117630b67e67dda1aa36aee9e38b33ad3c9900103c27fd927561
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182533220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d743d25eeb0209db92987de7cf880598ab7cdeb1f10e8dc15a80befa4634599b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:59:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 21:59:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 10 Feb 2023 21:59:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 21:59:07 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 10 Feb 2023 21:59:07 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 21:59:08 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 21:59:08 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 10 Feb 2023 21:59:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 21:59:15 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 21:59:15 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 21:59:15 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 21:59:15 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 21:59:16 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 21:59:16 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 21:59:16 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 21:59:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 21:59:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6859fdd3217ce6cda78174b39b4159a001e759607691e5cd8ffd91a23e38dabf`  
		Last Modified: Fri, 10 Feb 2023 22:00:15 GMT  
		Size: 60.6 MB (60620702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a069538501b951d72a4315d077fb0d6693149fe6ecc98fdcc71c8f1c8b8b966a`  
		Last Modified: Fri, 10 Feb 2023 22:00:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf012f3ecb3cab9ab2cb88227277f4b401712ec5b1761fc017360232e4521d0`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47c031db4cdc6a5895f3ba624d23563b7908df002d2606f43c6e7feaff5841c`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c0d0174a76dc9d34b1e6d7426a494fe303b36af8093ab1210b4f53ac64d61c`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0a416592926bca0b0deafaa886d747cb587ddc1b74d8f739ac2854d5e57314`  
		Last Modified: Fri, 10 Feb 2023 22:00:09 GMT  
		Size: 119.2 MB (119192990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec94ca3e0917562632b04892b735ef93abe25764f6ab4d745cba047193a314`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:3afcd7c4a9cd6eb73634f6129e7f3345b2a875988b4b446e08af836f15f3ca98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179526480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9681e63339ee6e7dea654db4cf715448b01424ff9a19b9860fd5edd96254fa63`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:10:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 22:10:31 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 10 Feb 2023 22:10:34 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 22:10:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 22:10:36 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 22:10:36 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 22:10:37 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 22:10:37 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 22:10:38 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 22:10:38 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 10 Feb 2023 22:10:39 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 10 Feb 2023 22:10:40 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 10 Feb 2023 22:10:41 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 22:10:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 22:10:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 22:10:43 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 22:10:44 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 10 Feb 2023 22:11:02 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 22:11:04 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 22:11:05 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 22:11:05 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 22:11:06 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 22:11:06 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 22:11:07 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 22:11:07 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 22:11:08 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 22:11:08 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 22:11:09 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 22:11:09 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 22:11:10 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 22:11:10 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 22:11:11 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 22:11:11 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 22:11:11 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 22:11:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43027ea8f93d783e28c87470bd6f8dfa8a38caa6e59be6bde3fdc3adaf9e05c9`  
		Last Modified: Fri, 10 Feb 2023 22:12:48 GMT  
		Size: 57.5 MB (57518821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b812d024d679c82bd86e3b448076cd0e2c051c3e855f61230a439ccbad8aae35`  
		Last Modified: Fri, 10 Feb 2023 22:12:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9920d19a9c6f90b45d7019c0799f6ec0423d7c5742a26315093c028b625da33`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa1e85317a574bc98c9fa48eeb5a0a0de10a8012304acba65db2878efea8779`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a086a276cc700bb7070fa5ee6bd37e586495293f726db3021968bf2e98ed9a`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 3.0 KB (3050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c40145aeb952661664e02252dbfdb815944d0ca2810df50d71b13d85fbe0dc`  
		Last Modified: Fri, 10 Feb 2023 22:12:43 GMT  
		Size: 119.2 MB (119192995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa36806be8d83ec34fb0fb0cab52fd742b9d497959e7f7598d172d00fec74cdc`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.2-u0`

```console
$ docker pull bonita@sha256:5a83ae61e42cdf265917c0901b79134a23e53b492e378282ad6ca527abe3e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:5d3ed4fd9f9d4cdbd623c66c5f2860105b17a18dc81152fd50709a6ac470caab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183375338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e19cd7ca4a306326e953fe500c4dd7bcf5e01b828fb0e84fd9cea954021a4ed`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:36:45 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 11 Feb 2023 07:36:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 11 Feb 2023 07:36:50 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 11 Feb 2023 07:36:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 11 Feb 2023 07:36:50 GMT
ARG BONITA_VERSION
# Sat, 11 Feb 2023 07:36:50 GMT
ARG BRANDING_VERSION
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BONITA_SHA256
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BASE_URL
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BONITA_URL
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 11 Feb 2023 07:36:51 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 11 Feb 2023 07:36:52 GMT
RUN mkdir /opt/files
# Sat, 11 Feb 2023 07:36:52 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 11 Feb 2023 07:37:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API_PASSWORD=
# Sat, 11 Feb 2023 07:37:12 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 11 Feb 2023 07:37:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 11 Feb 2023 07:37:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 11 Feb 2023 07:37:13 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 11 Feb 2023 07:37:13 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 11 Feb 2023 07:37:13 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 11 Feb 2023 07:37:13 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 11 Feb 2023 07:37:13 GMT
EXPOSE 8080 9000
# Sat, 11 Feb 2023 07:37:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 11 Feb 2023 07:37:13 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf6663e45425c152dfb7992b8c9eeb8d6cec3a4dc529df5805b63922a919b64`  
		Last Modified: Sat, 11 Feb 2023 07:38:13 GMT  
		Size: 61.4 MB (61364554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298fdbc8a6aaea5b1d47cf5e79516539019c8e4c801d07fab88568ea817933d2`  
		Last Modified: Sat, 11 Feb 2023 07:38:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6169c4b44f713d85daee9434e474d8ddb8ef418b07f2d84ed36b0ec3d86edf`  
		Last Modified: Sat, 11 Feb 2023 07:38:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda69351f0fed8d72a5e23d7b509a47ad85c0e095b97d21c648c7a9488aa8116`  
		Last Modified: Sat, 11 Feb 2023 07:38:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b74363046ff94dc8eac9b9006983ab60391b31d9d704a149b1c0ef0c45eeb9b`  
		Last Modified: Sat, 11 Feb 2023 07:38:03 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8497c92ada3f978eb9372afb70a400410a94485630824181b17ab5d0d07ecf`  
		Last Modified: Sat, 11 Feb 2023 07:38:09 GMT  
		Size: 119.2 MB (119192991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5401586f5efd8c65188ba61cda06c3a90b327feb812fedb4c5892af335e5f118`  
		Last Modified: Sat, 11 Feb 2023 07:38:02 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:d27829cdf839117630b67e67dda1aa36aee9e38b33ad3c9900103c27fd927561
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182533220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d743d25eeb0209db92987de7cf880598ab7cdeb1f10e8dc15a80befa4634599b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:59:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 21:59:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 10 Feb 2023 21:59:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 21:59:07 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 10 Feb 2023 21:59:07 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 21:59:08 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 21:59:08 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 10 Feb 2023 21:59:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 21:59:15 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 21:59:15 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 21:59:15 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 21:59:15 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 21:59:16 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 21:59:16 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 21:59:16 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 21:59:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 21:59:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6859fdd3217ce6cda78174b39b4159a001e759607691e5cd8ffd91a23e38dabf`  
		Last Modified: Fri, 10 Feb 2023 22:00:15 GMT  
		Size: 60.6 MB (60620702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a069538501b951d72a4315d077fb0d6693149fe6ecc98fdcc71c8f1c8b8b966a`  
		Last Modified: Fri, 10 Feb 2023 22:00:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf012f3ecb3cab9ab2cb88227277f4b401712ec5b1761fc017360232e4521d0`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47c031db4cdc6a5895f3ba624d23563b7908df002d2606f43c6e7feaff5841c`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c0d0174a76dc9d34b1e6d7426a494fe303b36af8093ab1210b4f53ac64d61c`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0a416592926bca0b0deafaa886d747cb587ddc1b74d8f739ac2854d5e57314`  
		Last Modified: Fri, 10 Feb 2023 22:00:09 GMT  
		Size: 119.2 MB (119192990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec94ca3e0917562632b04892b735ef93abe25764f6ab4d745cba047193a314`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:3afcd7c4a9cd6eb73634f6129e7f3345b2a875988b4b446e08af836f15f3ca98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179526480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9681e63339ee6e7dea654db4cf715448b01424ff9a19b9860fd5edd96254fa63`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:10:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 22:10:31 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 10 Feb 2023 22:10:34 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 22:10:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 22:10:36 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 22:10:36 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 22:10:37 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 22:10:37 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 22:10:38 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 22:10:38 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 10 Feb 2023 22:10:39 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 10 Feb 2023 22:10:40 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 10 Feb 2023 22:10:41 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 22:10:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 22:10:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 22:10:43 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 22:10:44 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 10 Feb 2023 22:11:02 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 22:11:04 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 22:11:05 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 22:11:05 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 22:11:06 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 22:11:06 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 22:11:07 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 22:11:07 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 22:11:08 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 22:11:08 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 22:11:09 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 22:11:09 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 22:11:10 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 22:11:10 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 22:11:11 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 22:11:11 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 22:11:11 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 22:11:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43027ea8f93d783e28c87470bd6f8dfa8a38caa6e59be6bde3fdc3adaf9e05c9`  
		Last Modified: Fri, 10 Feb 2023 22:12:48 GMT  
		Size: 57.5 MB (57518821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b812d024d679c82bd86e3b448076cd0e2c051c3e855f61230a439ccbad8aae35`  
		Last Modified: Fri, 10 Feb 2023 22:12:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9920d19a9c6f90b45d7019c0799f6ec0423d7c5742a26315093c028b625da33`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa1e85317a574bc98c9fa48eeb5a0a0de10a8012304acba65db2878efea8779`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a086a276cc700bb7070fa5ee6bd37e586495293f726db3021968bf2e98ed9a`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 3.0 KB (3050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c40145aeb952661664e02252dbfdb815944d0ca2810df50d71b13d85fbe0dc`  
		Last Modified: Fri, 10 Feb 2023 22:12:43 GMT  
		Size: 119.2 MB (119192995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa36806be8d83ec34fb0fb0cab52fd742b9d497959e7f7598d172d00fec74cdc`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:e9e7272ebaf28c4f0615859af62ed1d3633d271f8d604f17cf34c1411158cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:b8cab40aa3d32c2f0c4652ec23412dec17ad22f2badb3b65cd4507f0785b39ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235199961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a032ff4420d6a2d6c74c9a1474b0f11e0803242ab946951b59ff3a77ad1a7`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 20:22:07 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 20:23:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 20:23:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 20:23:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 20:23:31 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Jan 2023 20:23:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 20:23:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Jan 2023 20:23:33 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 20:23:33 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Jan 2023 20:23:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Jan 2023 20:23:42 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Jan 2023 20:23:44 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Jan 2023 20:23:44 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 20:23:44 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 20:23:44 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 20:23:44 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7328ec4a801f0ca840972017aea45def56308ec5cba3c331787ffb44d3eac66`  
		Last Modified: Tue, 31 Jan 2023 20:25:16 GMT  
		Size: 91.6 MB (91555780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818f4e3f37cf9db739a87c3e0b5531b2b79b229b7ca649ca81d92a7b292842f`  
		Last Modified: Tue, 31 Jan 2023 20:25:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97679340a72be5274f67677e7287ef10be57d3c23bdb65ce6796e99ac1bfeb71`  
		Last Modified: Tue, 31 Jan 2023 20:25:04 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65264dbf9351cac3a5ed13251053a8007d6b23e971aa4a61cdf49ca7fa9e30c`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 506.3 KB (506347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4e6b556bfacd17c87d71fe2055ae9653f247130c0784953e8cbacaee80a252`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af10439a3473a952f6a287bea286b506668833d65a7fbf5525d170a9af6a8bba`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 6.9 KB (6941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffabc92591d5293700dafb8846f22891b91216f2079300759b899716f819d99`  
		Last Modified: Tue, 31 Jan 2023 20:25:08 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1ef8d07e1bac9fe0c9a0ae4b87a11211a2b872c6d7532f85ecfa9aa082765`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ea94c68131d6d44d582f4be6e04230227f3f731f5bcbfbf73550277e3e2e0e79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226706515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8322c5e58f12ac21f77cd8c6b198982012e2218f313b048832d34641cace78`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:06:44 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 02 Mar 2023 02:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:08:10 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 02 Mar 2023 02:08:11 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 02 Mar 2023 02:08:14 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BONITA_VERSION
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BRANDING_VERSION
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BONITA_SHA256
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BASE_URL
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BONITA_URL
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 02 Mar 2023 02:08:15 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 02 Mar 2023 02:08:16 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 02 Mar 2023 02:08:16 GMT
RUN mkdir /opt/files
# Thu, 02 Mar 2023 02:08:16 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 02 Mar 2023 02:08:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 02 Mar 2023 02:08:25 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 02 Mar 2023 02:08:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 02 Mar 2023 02:08:26 GMT
VOLUME [/opt/bonita]
# Thu, 02 Mar 2023 02:08:26 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 02 Mar 2023 02:08:26 GMT
EXPOSE 8080
# Thu, 02 Mar 2023 02:08:26 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:9de1bca73074c336fb93a7688a40903c720a195929a0da27bd4ea424d5817c78`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 23.7 MB (23733538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6f8c688bd3ccf7157aeee1c49333e977721b1470062452e844ef68c303c8af`  
		Last Modified: Thu, 02 Mar 2023 02:09:57 GMT  
		Size: 86.1 MB (86070944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0876628926e6159ed8e68395f1859141e8a4cd3d7e70d05cf12b6071d12909b3`  
		Last Modified: Thu, 02 Mar 2023 02:09:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7d3ea37a586be245c30401cfc13a806692adeaf6e5dae529170b7b12a2258d`  
		Last Modified: Thu, 02 Mar 2023 02:09:48 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996fdc9a7159608270265f22ba62b525b4642b52daead040fad7c81d16262399`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 475.8 KB (475798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123396bdb84cd6d9664aeffa96282e9d21b03264eabb833db2b4bd6e07848a02`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbf65f28cf93495acd928f9533dbf10bd28329dd11098100128f79a68d99869`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed41a3e54cb9ffa4dbaa7cd2d89e6bc774523eef3115c66e7a014239545e6aac`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f887bd4a303e9aaa73ff24e9f9164cdbbba4c2566f04130fd7c57658d5f716`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:2b9ea6b78681b7a9be289d12610c393f6cbf085f288f14981efc118e43e0bdd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234190094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c892c407585638a2a7b05efdfb724550d26ffae06a421b2be008938a69d7322`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:41:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 19:43:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:43:29 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 19:43:31 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 19:43:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 19:43:35 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 19:43:36 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 19:43:36 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 19:43:36 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 19:43:37 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 19:43:38 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Jan 2023 19:43:38 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Jan 2023 19:43:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Jan 2023 19:43:39 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 19:43:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 19:43:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 19:43:41 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Jan 2023 19:43:42 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 19:43:43 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Jan 2023 19:43:51 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Jan 2023 19:43:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Jan 2023 19:43:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Jan 2023 19:43:57 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 19:43:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 19:43:58 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 19:43:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dec4dcee66042a87e0e5551837258f90b916e09f049946007420a0f691de9f`  
		Last Modified: Tue, 31 Jan 2023 19:47:02 GMT  
		Size: 86.8 MB (86845915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2b031382ecb158c362b2e064bcaa11898a7dc3332f3cef6c0d2d1b63d94983`  
		Last Modified: Tue, 31 Jan 2023 19:46:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf8982c80714bee8016edb384cfb022ecb0bb7fed71affbf59dc2422ca7389a`  
		Last Modified: Tue, 31 Jan 2023 19:46:42 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be7c94c68f6e9570d2a9cd4d784e1b00ecd8bebd114d64db134740061f216d`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1990afbb6ef5e6700cad031b0c60037d83a9707861bf315306189d3da7c600`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070fc5f1bb9687c8c4ce1b05efbe0bf92f48c3f23425beaa70a8f674891e7a92`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316fa544506415f88d616f984732dc77964260a9514ae096938e37e10c376bef`  
		Last Modified: Tue, 31 Jan 2023 19:46:48 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a7eee6b49e407ca9bf283e00d9ea0be41d4714669159bb6818903fe4f142e8`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:e9e7272ebaf28c4f0615859af62ed1d3633d271f8d604f17cf34c1411158cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:b8cab40aa3d32c2f0c4652ec23412dec17ad22f2badb3b65cd4507f0785b39ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235199961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a032ff4420d6a2d6c74c9a1474b0f11e0803242ab946951b59ff3a77ad1a7`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 20:22:07 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 20:23:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 20:23:28 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 20:23:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 20:23:31 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 20:23:31 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Jan 2023 20:23:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 20:23:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 20:23:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Jan 2023 20:23:33 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 20:23:33 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Jan 2023 20:23:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Jan 2023 20:23:42 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Jan 2023 20:23:44 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Jan 2023 20:23:44 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 20:23:44 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 20:23:44 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 20:23:44 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7328ec4a801f0ca840972017aea45def56308ec5cba3c331787ffb44d3eac66`  
		Last Modified: Tue, 31 Jan 2023 20:25:16 GMT  
		Size: 91.6 MB (91555780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818f4e3f37cf9db739a87c3e0b5531b2b79b229b7ca649ca81d92a7b292842f`  
		Last Modified: Tue, 31 Jan 2023 20:25:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97679340a72be5274f67677e7287ef10be57d3c23bdb65ce6796e99ac1bfeb71`  
		Last Modified: Tue, 31 Jan 2023 20:25:04 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65264dbf9351cac3a5ed13251053a8007d6b23e971aa4a61cdf49ca7fa9e30c`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 506.3 KB (506347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4e6b556bfacd17c87d71fe2055ae9653f247130c0784953e8cbacaee80a252`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af10439a3473a952f6a287bea286b506668833d65a7fbf5525d170a9af6a8bba`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 6.9 KB (6941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffabc92591d5293700dafb8846f22891b91216f2079300759b899716f819d99`  
		Last Modified: Tue, 31 Jan 2023 20:25:08 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1ef8d07e1bac9fe0c9a0ae4b87a11211a2b872c6d7532f85ecfa9aa082765`  
		Last Modified: Tue, 31 Jan 2023 20:25:02 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ea94c68131d6d44d582f4be6e04230227f3f731f5bcbfbf73550277e3e2e0e79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226706515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8322c5e58f12ac21f77cd8c6b198982012e2218f313b048832d34641cace78`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:06:44 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 02 Mar 2023 02:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:08:10 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 02 Mar 2023 02:08:11 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 02 Mar 2023 02:08:14 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BONITA_VERSION
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BRANDING_VERSION
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BONITA_SHA256
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BASE_URL
# Thu, 02 Mar 2023 02:08:15 GMT
ARG BONITA_URL
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 02 Mar 2023 02:08:15 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 02 Mar 2023 02:08:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 02 Mar 2023 02:08:16 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 02 Mar 2023 02:08:16 GMT
RUN mkdir /opt/files
# Thu, 02 Mar 2023 02:08:16 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 02 Mar 2023 02:08:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 02 Mar 2023 02:08:25 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 02 Mar 2023 02:08:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 02 Mar 2023 02:08:26 GMT
VOLUME [/opt/bonita]
# Thu, 02 Mar 2023 02:08:26 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 02 Mar 2023 02:08:26 GMT
EXPOSE 8080
# Thu, 02 Mar 2023 02:08:26 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:9de1bca73074c336fb93a7688a40903c720a195929a0da27bd4ea424d5817c78`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 23.7 MB (23733538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6f8c688bd3ccf7157aeee1c49333e977721b1470062452e844ef68c303c8af`  
		Last Modified: Thu, 02 Mar 2023 02:09:57 GMT  
		Size: 86.1 MB (86070944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0876628926e6159ed8e68395f1859141e8a4cd3d7e70d05cf12b6071d12909b3`  
		Last Modified: Thu, 02 Mar 2023 02:09:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7d3ea37a586be245c30401cfc13a806692adeaf6e5dae529170b7b12a2258d`  
		Last Modified: Thu, 02 Mar 2023 02:09:48 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996fdc9a7159608270265f22ba62b525b4642b52daead040fad7c81d16262399`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 475.8 KB (475798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123396bdb84cd6d9664aeffa96282e9d21b03264eabb833db2b4bd6e07848a02`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbf65f28cf93495acd928f9533dbf10bd28329dd11098100128f79a68d99869`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed41a3e54cb9ffa4dbaa7cd2d89e6bc774523eef3115c66e7a014239545e6aac`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f887bd4a303e9aaa73ff24e9f9164cdbbba4c2566f04130fd7c57658d5f716`  
		Last Modified: Thu, 02 Mar 2023 02:09:46 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:2b9ea6b78681b7a9be289d12610c393f6cbf085f288f14981efc118e43e0bdd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234190094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c892c407585638a2a7b05efdfb724550d26ffae06a421b2be008938a69d7322`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:41:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 19:43:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:43:29 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 19:43:31 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 19:43:35 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 19:43:35 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 19:43:36 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 19:43:36 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 19:43:36 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 19:43:37 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 19:43:38 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Jan 2023 19:43:38 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Jan 2023 19:43:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Jan 2023 19:43:39 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 19:43:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 19:43:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Jan 2023 19:43:41 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Jan 2023 19:43:42 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 19:43:43 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Jan 2023 19:43:51 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Jan 2023 19:43:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Jan 2023 19:43:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Jan 2023 19:43:57 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 19:43:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 19:43:58 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 19:43:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dec4dcee66042a87e0e5551837258f90b916e09f049946007420a0f691de9f`  
		Last Modified: Tue, 31 Jan 2023 19:47:02 GMT  
		Size: 86.8 MB (86845915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2b031382ecb158c362b2e064bcaa11898a7dc3332f3cef6c0d2d1b63d94983`  
		Last Modified: Tue, 31 Jan 2023 19:46:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf8982c80714bee8016edb384cfb022ecb0bb7fed71affbf59dc2422ca7389a`  
		Last Modified: Tue, 31 Jan 2023 19:46:42 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be7c94c68f6e9570d2a9cd4d784e1b00ecd8bebd114d64db134740061f216d`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1990afbb6ef5e6700cad031b0c60037d83a9707861bf315306189d3da7c600`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070fc5f1bb9687c8c4ce1b05efbe0bf92f48c3f23425beaa70a8f674891e7a92`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316fa544506415f88d616f984732dc77964260a9514ae096938e37e10c376bef`  
		Last Modified: Tue, 31 Jan 2023 19:46:48 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a7eee6b49e407ca9bf283e00d9ea0be41d4714669159bb6818903fe4f142e8`  
		Last Modified: Tue, 31 Jan 2023 19:46:40 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:0a3229aec1faf58c4230141a14b940d487f94972153cc49effc857d2eca8f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:fd0be2bc8b1b3580520d1c941b5c32c9e5f8974123203f851868a1c7923612a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232933233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63865f3dedcce11b2c96983ce415b3d98f2497f8731226bc724efeddf4ec0f4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 20:22:07 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 20:24:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 20:24:22 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 20:24:23 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 20:24:26 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 20:24:26 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 20:24:26 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 31 Jan 2023 20:24:27 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 20:24:28 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 20:24:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 31 Jan 2023 20:24:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 31 Jan 2023 20:24:34 GMT
ENV HTTP_API=false
# Tue, 31 Jan 2023 20:24:34 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 20:24:35 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 20:24:35 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 20:24:36 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba97969dd85d91907f2fc0705dabba826046cd6fead565759517131d1e27e88`  
		Last Modified: Tue, 31 Jan 2023 20:25:41 GMT  
		Size: 91.6 MB (91556051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4afd30cea7c96ad48fb9e0289edf467e408a8ea32f9c5a45650434f42e6e7d`  
		Last Modified: Tue, 31 Jan 2023 20:25:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b957206dc389298bf529853e92c39823dfe21e4335c35dde6bf4e92f12a3749c`  
		Last Modified: Tue, 31 Jan 2023 20:25:29 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4ddaf1e60c0dfff663d7b7c459a936685d45a1d073c4f06a161c8e58e22c35`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 930.5 KB (930473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b40a0d125e823df55ddcd338431fce9ae79df87d2394773d06019a391adec2`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ec9aa87334c9042ff31cfeaff83c1a3c14e6b3fcba091496b094952f25aa58`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c5ff3727ffb3ab343809ff323ddf2c855264021508d2e79496dd73b95e11d5`  
		Last Modified: Tue, 31 Jan 2023 20:25:33 GMT  
		Size: 113.7 MB (113727922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56eba647c73536d78afc9c24ffb78ea2d7804cec60c77780ab0126ac2e16e521`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2a8f5fef5eca108ec1fc148fdfb9fdd19f842f82d7e242091e09a8c897068a20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224399012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a867bcf236ff6e26005fc5aad844c87c05a9a2066260056f0b78a82fc86e571`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:06:44 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 02 Mar 2023 02:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:08:54 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 02 Mar 2023 02:08:54 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 02 Mar 2023 02:08:57 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BONITA_VERSION
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BRANDING_VERSION
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BONITA_SHA256
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BASE_URL
# Thu, 02 Mar 2023 02:08:58 GMT
ARG BONITA_URL
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 02 Mar 2023 02:08:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 02 Mar 2023 02:08:58 GMT
RUN mkdir /opt/files
# Thu, 02 Mar 2023 02:08:59 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 02 Mar 2023 02:09:13 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 02 Mar 2023 02:09:13 GMT
ENV HTTP_API=false
# Thu, 02 Mar 2023 02:09:14 GMT
VOLUME [/opt/bonita]
# Thu, 02 Mar 2023 02:09:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 02 Mar 2023 02:09:15 GMT
EXPOSE 8080
# Thu, 02 Mar 2023 02:09:17 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:9de1bca73074c336fb93a7688a40903c720a195929a0da27bd4ea424d5817c78`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 23.7 MB (23733538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fbb063e5c589f703cb3aeaee5c7c9724dbc799fe4719975633002505b8cf85`  
		Last Modified: Thu, 02 Mar 2023 02:10:19 GMT  
		Size: 86.1 MB (86070784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8c7f9af646ae3452dccc5b4504b78a3e1310b5967bd7027ad925e16ea6e7ac`  
		Last Modified: Thu, 02 Mar 2023 02:10:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e365ae68182fc69902d7d6c7f07e90ee959f615c925c91b051f771206573cd`  
		Last Modified: Thu, 02 Mar 2023 02:10:10 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0709ab65a352fffcc2b1c4f4455ee221dd0a3d8bcfa525b53886936ff9bc24`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 859.6 KB (859577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4d382643865f1584f3c8463b0c5c34cbe7817c5c9a46f28ccb9253490f6fee`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef04571e8ea7c8bca7678990add92f6e3df7cdf1cda1ef6b5679bbc6f885795a`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb828964136d3d92ee0a8d9811d377b7cc856039cb02a785e0d57083cf391ec`  
		Last Modified: Thu, 02 Mar 2023 02:10:13 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0307f9b5c2a9de64b005fc2d39e9aea2faa0f1164124b048e1d7c26f0dbf129`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:93391aa63425871df905e44d51cc0166c7e2ad8e54663a9dbb3040db48482e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231855236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be14cd370871d6210aa189b077498e1885375518794b71d6b6f4251b06de737`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:41:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 19:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:45:05 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 19:45:07 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 19:45:11 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 19:45:11 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 19:45:12 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 19:45:12 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 19:45:13 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 19:45:13 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 19:45:14 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 31 Jan 2023 19:45:14 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 31 Jan 2023 19:45:15 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 31 Jan 2023 19:45:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 19:45:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 19:45:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 19:45:18 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 19:45:18 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 31 Jan 2023 19:45:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 31 Jan 2023 19:45:34 GMT
ENV HTTP_API=false
# Tue, 31 Jan 2023 19:45:36 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 19:45:37 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 19:45:38 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 19:45:41 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7207648cefd934054d20bbcd76538dcb17b703a45aa2f7f4729e42b73eac094a`  
		Last Modified: Tue, 31 Jan 2023 19:47:38 GMT  
		Size: 86.8 MB (86845963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ee4eedc705e1187ff40602b65ece479b94e94a8a0cec74d68d166d530b4605`  
		Last Modified: Tue, 31 Jan 2023 19:47:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44082f9095e3ee7114fbed16930ebb78c54dc34780c156ee94736d276f63f68f`  
		Last Modified: Tue, 31 Jan 2023 19:47:18 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4307ede583209a0e3993a75be9c39ac1df424bd286a4971afc40a3dcb14a92bb`  
		Last Modified: Tue, 31 Jan 2023 19:47:17 GMT  
		Size: 831.6 KB (831571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a632a969fcf59bc731d0ad0c54f8cca5e568adf40d793be80f09605804712ba`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e810a25780c832ebeaa4cbc19dc01c93823e11ed41dcc5208625f1b65d7fd5cc`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d720760489ab042105da1fc12b16912e12c80856a76f4dac753114c0623a39bf`  
		Last Modified: Tue, 31 Jan 2023 19:47:27 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f9b039eb20902e8dfa61ac9f02d41ecff0a57fc10ab41e37a804dd32585b16`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:0a3229aec1faf58c4230141a14b940d487f94972153cc49effc857d2eca8f054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:fd0be2bc8b1b3580520d1c941b5c32c9e5f8974123203f851868a1c7923612a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232933233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63865f3dedcce11b2c96983ce415b3d98f2497f8731226bc724efeddf4ec0f4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 20:22:07 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 20:24:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 20:24:22 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 20:24:23 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 20:24:26 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 20:24:26 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 20:24:26 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 20:24:27 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 31 Jan 2023 20:24:27 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 20:24:27 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 20:24:28 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 20:24:28 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 31 Jan 2023 20:24:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 31 Jan 2023 20:24:34 GMT
ENV HTTP_API=false
# Tue, 31 Jan 2023 20:24:34 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 20:24:35 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 20:24:35 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 20:24:36 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba97969dd85d91907f2fc0705dabba826046cd6fead565759517131d1e27e88`  
		Last Modified: Tue, 31 Jan 2023 20:25:41 GMT  
		Size: 91.6 MB (91556051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4afd30cea7c96ad48fb9e0289edf467e408a8ea32f9c5a45650434f42e6e7d`  
		Last Modified: Tue, 31 Jan 2023 20:25:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b957206dc389298bf529853e92c39823dfe21e4335c35dde6bf4e92f12a3749c`  
		Last Modified: Tue, 31 Jan 2023 20:25:29 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4ddaf1e60c0dfff663d7b7c459a936685d45a1d073c4f06a161c8e58e22c35`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 930.5 KB (930473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b40a0d125e823df55ddcd338431fce9ae79df87d2394773d06019a391adec2`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ec9aa87334c9042ff31cfeaff83c1a3c14e6b3fcba091496b094952f25aa58`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c5ff3727ffb3ab343809ff323ddf2c855264021508d2e79496dd73b95e11d5`  
		Last Modified: Tue, 31 Jan 2023 20:25:33 GMT  
		Size: 113.7 MB (113727922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56eba647c73536d78afc9c24ffb78ea2d7804cec60c77780ab0126ac2e16e521`  
		Last Modified: Tue, 31 Jan 2023 20:25:27 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2a8f5fef5eca108ec1fc148fdfb9fdd19f842f82d7e242091e09a8c897068a20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224399012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a867bcf236ff6e26005fc5aad844c87c05a9a2066260056f0b78a82fc86e571`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:06:44 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 02 Mar 2023 02:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:08:54 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 02 Mar 2023 02:08:54 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 02 Mar 2023 02:08:57 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BONITA_VERSION
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BRANDING_VERSION
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BONITA_SHA256
# Thu, 02 Mar 2023 02:08:57 GMT
ARG BASE_URL
# Thu, 02 Mar 2023 02:08:58 GMT
ARG BONITA_URL
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_VERSION=7.13.0
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BRANDING_VERSION=2021.2-u0
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Thu, 02 Mar 2023 02:08:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 02 Mar 2023 02:08:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Thu, 02 Mar 2023 02:08:58 GMT
RUN mkdir /opt/files
# Thu, 02 Mar 2023 02:08:59 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Thu, 02 Mar 2023 02:09:13 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Thu, 02 Mar 2023 02:09:13 GMT
ENV HTTP_API=false
# Thu, 02 Mar 2023 02:09:14 GMT
VOLUME [/opt/bonita]
# Thu, 02 Mar 2023 02:09:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 02 Mar 2023 02:09:15 GMT
EXPOSE 8080
# Thu, 02 Mar 2023 02:09:17 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:9de1bca73074c336fb93a7688a40903c720a195929a0da27bd4ea424d5817c78`  
		Last Modified: Thu, 02 Mar 2023 02:09:51 GMT  
		Size: 23.7 MB (23733538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fbb063e5c589f703cb3aeaee5c7c9724dbc799fe4719975633002505b8cf85`  
		Last Modified: Thu, 02 Mar 2023 02:10:19 GMT  
		Size: 86.1 MB (86070784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8c7f9af646ae3452dccc5b4504b78a3e1310b5967bd7027ad925e16ea6e7ac`  
		Last Modified: Thu, 02 Mar 2023 02:10:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e365ae68182fc69902d7d6c7f07e90ee959f615c925c91b051f771206573cd`  
		Last Modified: Thu, 02 Mar 2023 02:10:10 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0709ab65a352fffcc2b1c4f4455ee221dd0a3d8bcfa525b53886936ff9bc24`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 859.6 KB (859577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4d382643865f1584f3c8463b0c5c34cbe7817c5c9a46f28ccb9253490f6fee`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef04571e8ea7c8bca7678990add92f6e3df7cdf1cda1ef6b5679bbc6f885795a`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb828964136d3d92ee0a8d9811d377b7cc856039cb02a785e0d57083cf391ec`  
		Last Modified: Thu, 02 Mar 2023 02:10:13 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0307f9b5c2a9de64b005fc2d39e9aea2faa0f1164124b048e1d7c26f0dbf129`  
		Last Modified: Thu, 02 Mar 2023 02:10:08 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:93391aa63425871df905e44d51cc0166c7e2ad8e54663a9dbb3040db48482e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231855236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be14cd370871d6210aa189b077498e1885375518794b71d6b6f4251b06de737`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:41:50 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Jan 2023 19:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:45:05 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Jan 2023 19:45:07 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Jan 2023 19:45:11 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Jan 2023 19:45:11 GMT
ARG BONITA_VERSION
# Tue, 31 Jan 2023 19:45:12 GMT
ARG BRANDING_VERSION
# Tue, 31 Jan 2023 19:45:12 GMT
ARG BONITA_SHA256
# Tue, 31 Jan 2023 19:45:13 GMT
ARG BASE_URL
# Tue, 31 Jan 2023 19:45:13 GMT
ARG BONITA_URL
# Tue, 31 Jan 2023 19:45:14 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 31 Jan 2023 19:45:14 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 31 Jan 2023 19:45:15 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 31 Jan 2023 19:45:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 19:45:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Jan 2023 19:45:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 31 Jan 2023 19:45:18 GMT
RUN mkdir /opt/files
# Tue, 31 Jan 2023 19:45:18 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 31 Jan 2023 19:45:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 31 Jan 2023 19:45:34 GMT
ENV HTTP_API=false
# Tue, 31 Jan 2023 19:45:36 GMT
VOLUME [/opt/bonita]
# Tue, 31 Jan 2023 19:45:37 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Jan 2023 19:45:38 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 19:45:41 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7207648cefd934054d20bbcd76538dcb17b703a45aa2f7f4729e42b73eac094a`  
		Last Modified: Tue, 31 Jan 2023 19:47:38 GMT  
		Size: 86.8 MB (86845963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ee4eedc705e1187ff40602b65ece479b94e94a8a0cec74d68d166d530b4605`  
		Last Modified: Tue, 31 Jan 2023 19:47:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44082f9095e3ee7114fbed16930ebb78c54dc34780c156ee94736d276f63f68f`  
		Last Modified: Tue, 31 Jan 2023 19:47:18 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4307ede583209a0e3993a75be9c39ac1df424bd286a4971afc40a3dcb14a92bb`  
		Last Modified: Tue, 31 Jan 2023 19:47:17 GMT  
		Size: 831.6 KB (831571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a632a969fcf59bc731d0ad0c54f8cca5e568adf40d793be80f09605804712ba`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e810a25780c832ebeaa4cbc19dc01c93823e11ed41dcc5208625f1b65d7fd5cc`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d720760489ab042105da1fc12b16912e12c80856a76f4dac753114c0623a39bf`  
		Last Modified: Tue, 31 Jan 2023 19:47:27 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f9b039eb20902e8dfa61ac9f02d41ecff0a57fc10ab41e37a804dd32585b16`  
		Last Modified: Tue, 31 Jan 2023 19:47:16 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14`

```console
$ docker pull bonita@sha256:2f3c5eed0c94710458be82864edbe4ba9178d8135c9df47799216985906b6002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14` - linux; amd64

```console
$ docker pull bonita@sha256:02b3824ad75e32956ee983c1496672784d05c33a9be1f0128785b8c39353a978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176984103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32baedb9bbed9762a558ee13a022cc8010e548f3b59d0f457c42e8b5ceacb36`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:36:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 11 Feb 2023 07:36:25 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 11 Feb 2023 07:36:26 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 11 Feb 2023 07:36:26 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_VERSION
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BRANDING_VERSION
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_SHA256
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BASE_URL
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_URL
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 11 Feb 2023 07:36:27 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 11 Feb 2023 07:36:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 11 Feb 2023 07:36:28 GMT
RUN mkdir /opt/files
# Sat, 11 Feb 2023 07:36:28 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 11 Feb 2023 07:36:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API_PASSWORD=
# Sat, 11 Feb 2023 07:36:38 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 11 Feb 2023 07:36:38 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 11 Feb 2023 07:36:38 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 11 Feb 2023 07:36:39 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 11 Feb 2023 07:36:39 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 11 Feb 2023 07:36:39 GMT
EXPOSE 8080 9000
# Sat, 11 Feb 2023 07:36:39 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 11 Feb 2023 07:36:39 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230ac87c111c758dc330d34eec96b2fd040464085514c8bc299cc3ae6301bef`  
		Last Modified: Sat, 11 Feb 2023 07:37:49 GMT  
		Size: 57.5 MB (57457146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a94688547e8089bcb2955a83b3c000f4626945038edf17b181125190ed03cb2`  
		Last Modified: Sat, 11 Feb 2023 07:37:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801d3c8a6716925340bd1cba3509d4ed3ae9e214f42c3034e737f45e8976e10e`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762f5ac5ff165059fc8cb51b0ece4cc382c58bc04983a796e5df877f5800c95`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0ea9043ed6c4923c0f23d917a58009babceba34bd649442325f0b361d86aa2`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4c1ac5378dd5377fa6af775a4285f79537da5cc2e31082ddd1bf022e10c76b`  
		Last Modified: Sat, 11 Feb 2023 07:37:46 GMT  
		Size: 116.7 MB (116690797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eef05f4a0072c0d1417d0aeb36743fd44aef8f908913ab18244ff757658b7e2`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4369e5cb8a74d976d78b4cdc4c8393f501cc63a2914e61e652ea4d9c8e0b1c25
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176202935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0d03b50d68ea6eba6c765b08a84d909c5a2968c58a0f53ceea419be6d4e26b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:58:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 21:58:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 10 Feb 2023 21:58:46 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 21:58:47 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 21:58:47 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 10 Feb 2023 21:58:47 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 10 Feb 2023 21:58:48 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 21:58:48 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 21:58:48 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 10 Feb 2023 21:58:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 21:58:56 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 21:58:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 21:58:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 21:58:57 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 21:58:57 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 21:58:57 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 21:58:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 21:58:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e2109a84b98be453581984099b1e5905de15709f8462fd01ef9041a975f814`  
		Last Modified: Fri, 10 Feb 2023 21:59:49 GMT  
		Size: 56.8 MB (56780552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d915f6aab23e3a3243f320b98942b39e4269dda6727389cb292505d57d87070e`  
		Last Modified: Fri, 10 Feb 2023 21:59:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13344da817627abfaaa8f998dca6d0a93349f5ddcf1482d4b776cc634482722`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a9c725a2f28d4e241d63208dcbef03c7263a01889033998aacae2aeacd8671`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a436099d21c84764dfe4832afa1166dd2ddf43f451d49e56e47eb787a51e3c`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c55eb4882b2e4f60cc8a7a133b428594bcda8bf05708361f476857e093eb45b`  
		Last Modified: Fri, 10 Feb 2023 21:59:47 GMT  
		Size: 116.7 MB (116690810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5e9fd1bc9c10621aa7c5211a6b1be870cef856d036184db08a692c8b9aa953`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; ppc64le

```console
$ docker pull bonita@sha256:0191aeef4a5882edad729e7ba9d3f866e05e9f7767dcbf4faa1c3abe4656a14d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172793970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cf165f9ce9e1a5741cbecbaa9df6eb357cbc2e0dfd8d0ebcb7d42d4023e924`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:52 GMT
ADD file:0db937922cfd604e84e5df7ed3bfe476af7113be3c4c1e216653f249fdacfd44 in / 
# Fri, 10 Feb 2023 21:20:53 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:09:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 22:09:28 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 10 Feb 2023 22:09:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 22:09:33 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 22:09:34 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 22:09:34 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 22:09:35 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 22:09:35 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 22:09:36 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 22:09:36 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 10 Feb 2023 22:09:36 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 10 Feb 2023 22:09:37 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 10 Feb 2023 22:09:38 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 22:09:38 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 22:09:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 22:09:40 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 22:09:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 10 Feb 2023 22:09:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 22:10:00 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 22:10:01 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 22:10:01 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 22:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 22:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 22:10:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 22:10:03 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 22:10:03 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 22:10:04 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 22:10:05 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 22:10:05 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 22:10:06 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 22:10:07 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 22:10:07 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 22:10:08 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 22:10:08 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 22:10:09 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5b42622f88c38596f558fe14b894eadc782d1b003f25d0374cf41bc92e716959`  
		Last Modified: Fri, 10 Feb 2023 21:22:05 GMT  
		Size: 2.8 MB (2813687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b13d8f05b508a7505125aca30065be998cdcdfca17cae08199630f66f2a5e8`  
		Last Modified: Fri, 10 Feb 2023 22:12:14 GMT  
		Size: 53.3 MB (53279469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541b2abe2c930f64fff252af8183fa8af7c1399a60f573966c284dc87cd102e`  
		Last Modified: Fri, 10 Feb 2023 22:12:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d999c19e37140fdfc6a79ddef921f4899f76153ac6f98ec4255ca7bbbe3836b6`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dff5215400cc8e206e0b8f5b659548d5dfc3248de04f06067851bc28a6ada54`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e3033fffec12c9bdde2e22b8daa43f15df18b4a70c0e2ddaf82e290e98b81d`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890d23e1786c784e08495019b2d059220016be2524706f6172eebcd6982a4d34`  
		Last Modified: Fri, 10 Feb 2023 22:12:10 GMT  
		Size: 116.7 MB (116690801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209e978febf076cfc30ca2cb9b6e22a75956a313738f3aea8821c2a339a12a20`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14.0`

```console
$ docker pull bonita@sha256:2f3c5eed0c94710458be82864edbe4ba9178d8135c9df47799216985906b6002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14.0` - linux; amd64

```console
$ docker pull bonita@sha256:02b3824ad75e32956ee983c1496672784d05c33a9be1f0128785b8c39353a978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176984103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32baedb9bbed9762a558ee13a022cc8010e548f3b59d0f457c42e8b5ceacb36`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:36:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 11 Feb 2023 07:36:25 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 11 Feb 2023 07:36:26 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 11 Feb 2023 07:36:26 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_VERSION
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BRANDING_VERSION
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_SHA256
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BASE_URL
# Sat, 11 Feb 2023 07:36:27 GMT
ARG BONITA_URL
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 11 Feb 2023 07:36:27 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 11 Feb 2023 07:36:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 11 Feb 2023 07:36:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 11 Feb 2023 07:36:28 GMT
RUN mkdir /opt/files
# Sat, 11 Feb 2023 07:36:28 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Sat, 11 Feb 2023 07:36:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 11 Feb 2023 07:36:38 GMT
ENV HTTP_API_PASSWORD=
# Sat, 11 Feb 2023 07:36:38 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 11 Feb 2023 07:36:38 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 11 Feb 2023 07:36:38 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 11 Feb 2023 07:36:38 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 11 Feb 2023 07:36:39 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 11 Feb 2023 07:36:39 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 11 Feb 2023 07:36:39 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 11 Feb 2023 07:36:39 GMT
EXPOSE 8080 9000
# Sat, 11 Feb 2023 07:36:39 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 11 Feb 2023 07:36:39 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230ac87c111c758dc330d34eec96b2fd040464085514c8bc299cc3ae6301bef`  
		Last Modified: Sat, 11 Feb 2023 07:37:49 GMT  
		Size: 57.5 MB (57457146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a94688547e8089bcb2955a83b3c000f4626945038edf17b181125190ed03cb2`  
		Last Modified: Sat, 11 Feb 2023 07:37:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801d3c8a6716925340bd1cba3509d4ed3ae9e214f42c3034e737f45e8976e10e`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762f5ac5ff165059fc8cb51b0ece4cc382c58bc04983a796e5df877f5800c95`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0ea9043ed6c4923c0f23d917a58009babceba34bd649442325f0b361d86aa2`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4c1ac5378dd5377fa6af775a4285f79537da5cc2e31082ddd1bf022e10c76b`  
		Last Modified: Sat, 11 Feb 2023 07:37:46 GMT  
		Size: 116.7 MB (116690797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eef05f4a0072c0d1417d0aeb36743fd44aef8f908913ab18244ff757658b7e2`  
		Last Modified: Sat, 11 Feb 2023 07:37:40 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4369e5cb8a74d976d78b4cdc4c8393f501cc63a2914e61e652ea4d9c8e0b1c25
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176202935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0d03b50d68ea6eba6c765b08a84d909c5a2968c58a0f53ceea419be6d4e26b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:58:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 21:58:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 10 Feb 2023 21:58:46 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 21:58:47 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 21:58:47 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 21:58:47 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 10 Feb 2023 21:58:47 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 10 Feb 2023 21:58:48 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 21:58:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 21:58:48 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 21:58:48 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 10 Feb 2023 21:58:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 21:58:56 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 21:58:56 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 21:58:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 21:58:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 21:58:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 21:58:57 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 21:58:57 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 21:58:57 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 21:58:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 21:58:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e2109a84b98be453581984099b1e5905de15709f8462fd01ef9041a975f814`  
		Last Modified: Fri, 10 Feb 2023 21:59:49 GMT  
		Size: 56.8 MB (56780552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d915f6aab23e3a3243f320b98942b39e4269dda6727389cb292505d57d87070e`  
		Last Modified: Fri, 10 Feb 2023 21:59:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13344da817627abfaaa8f998dca6d0a93349f5ddcf1482d4b776cc634482722`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a9c725a2f28d4e241d63208dcbef03c7263a01889033998aacae2aeacd8671`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a436099d21c84764dfe4832afa1166dd2ddf43f451d49e56e47eb787a51e3c`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c55eb4882b2e4f60cc8a7a133b428594bcda8bf05708361f476857e093eb45b`  
		Last Modified: Fri, 10 Feb 2023 21:59:47 GMT  
		Size: 116.7 MB (116690810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5e9fd1bc9c10621aa7c5211a6b1be870cef856d036184db08a692c8b9aa953`  
		Last Modified: Fri, 10 Feb 2023 21:59:41 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:0191aeef4a5882edad729e7ba9d3f866e05e9f7767dcbf4faa1c3abe4656a14d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172793970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cf165f9ce9e1a5741cbecbaa9df6eb357cbc2e0dfd8d0ebcb7d42d4023e924`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:52 GMT
ADD file:0db937922cfd604e84e5df7ed3bfe476af7113be3c4c1e216653f249fdacfd44 in / 
# Fri, 10 Feb 2023 21:20:53 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:09:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 22:09:28 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 10 Feb 2023 22:09:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 22:09:33 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 22:09:34 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 22:09:34 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 22:09:35 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 22:09:35 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 22:09:36 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 22:09:36 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 10 Feb 2023 22:09:36 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 10 Feb 2023 22:09:37 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 10 Feb 2023 22:09:38 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 22:09:38 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 22:09:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 10 Feb 2023 22:09:40 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 22:09:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 10 Feb 2023 22:09:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 22:10:00 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 22:10:01 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 22:10:01 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 22:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 22:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 22:10:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 22:10:03 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 22:10:03 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 22:10:04 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 22:10:05 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 22:10:05 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 22:10:06 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 22:10:07 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 22:10:07 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 22:10:08 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 22:10:08 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 22:10:09 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5b42622f88c38596f558fe14b894eadc782d1b003f25d0374cf41bc92e716959`  
		Last Modified: Fri, 10 Feb 2023 21:22:05 GMT  
		Size: 2.8 MB (2813687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b13d8f05b508a7505125aca30065be998cdcdfca17cae08199630f66f2a5e8`  
		Last Modified: Fri, 10 Feb 2023 22:12:14 GMT  
		Size: 53.3 MB (53279469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541b2abe2c930f64fff252af8183fa8af7c1399a60f573966c284dc87cd102e`  
		Last Modified: Fri, 10 Feb 2023 22:12:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d999c19e37140fdfc6a79ddef921f4899f76153ac6f98ec4255ca7bbbe3836b6`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dff5215400cc8e206e0b8f5b659548d5dfc3248de04f06067851bc28a6ada54`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e3033fffec12c9bdde2e22b8daa43f15df18b4a70c0e2ddaf82e290e98b81d`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890d23e1786c784e08495019b2d059220016be2524706f6172eebcd6982a4d34`  
		Last Modified: Fri, 10 Feb 2023 22:12:10 GMT  
		Size: 116.7 MB (116690801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209e978febf076cfc30ca2cb9b6e22a75956a313738f3aea8821c2a339a12a20`  
		Last Modified: Fri, 10 Feb 2023 22:12:00 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.15`

```console
$ docker pull bonita@sha256:5a83ae61e42cdf265917c0901b79134a23e53b492e378282ad6ca527abe3e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15` - linux; amd64

```console
$ docker pull bonita@sha256:5d3ed4fd9f9d4cdbd623c66c5f2860105b17a18dc81152fd50709a6ac470caab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183375338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e19cd7ca4a306326e953fe500c4dd7bcf5e01b828fb0e84fd9cea954021a4ed`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:36:45 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 11 Feb 2023 07:36:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 11 Feb 2023 07:36:50 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 11 Feb 2023 07:36:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 11 Feb 2023 07:36:50 GMT
ARG BONITA_VERSION
# Sat, 11 Feb 2023 07:36:50 GMT
ARG BRANDING_VERSION
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BONITA_SHA256
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BASE_URL
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BONITA_URL
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 11 Feb 2023 07:36:51 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 11 Feb 2023 07:36:52 GMT
RUN mkdir /opt/files
# Sat, 11 Feb 2023 07:36:52 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 11 Feb 2023 07:37:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API_PASSWORD=
# Sat, 11 Feb 2023 07:37:12 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 11 Feb 2023 07:37:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 11 Feb 2023 07:37:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 11 Feb 2023 07:37:13 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 11 Feb 2023 07:37:13 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 11 Feb 2023 07:37:13 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 11 Feb 2023 07:37:13 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 11 Feb 2023 07:37:13 GMT
EXPOSE 8080 9000
# Sat, 11 Feb 2023 07:37:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 11 Feb 2023 07:37:13 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf6663e45425c152dfb7992b8c9eeb8d6cec3a4dc529df5805b63922a919b64`  
		Last Modified: Sat, 11 Feb 2023 07:38:13 GMT  
		Size: 61.4 MB (61364554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298fdbc8a6aaea5b1d47cf5e79516539019c8e4c801d07fab88568ea817933d2`  
		Last Modified: Sat, 11 Feb 2023 07:38:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6169c4b44f713d85daee9434e474d8ddb8ef418b07f2d84ed36b0ec3d86edf`  
		Last Modified: Sat, 11 Feb 2023 07:38:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda69351f0fed8d72a5e23d7b509a47ad85c0e095b97d21c648c7a9488aa8116`  
		Last Modified: Sat, 11 Feb 2023 07:38:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b74363046ff94dc8eac9b9006983ab60391b31d9d704a149b1c0ef0c45eeb9b`  
		Last Modified: Sat, 11 Feb 2023 07:38:03 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8497c92ada3f978eb9372afb70a400410a94485630824181b17ab5d0d07ecf`  
		Last Modified: Sat, 11 Feb 2023 07:38:09 GMT  
		Size: 119.2 MB (119192991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5401586f5efd8c65188ba61cda06c3a90b327feb812fedb4c5892af335e5f118`  
		Last Modified: Sat, 11 Feb 2023 07:38:02 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:d27829cdf839117630b67e67dda1aa36aee9e38b33ad3c9900103c27fd927561
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182533220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d743d25eeb0209db92987de7cf880598ab7cdeb1f10e8dc15a80befa4634599b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:59:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 21:59:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 10 Feb 2023 21:59:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 21:59:07 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 10 Feb 2023 21:59:07 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 21:59:08 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 21:59:08 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 10 Feb 2023 21:59:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 21:59:15 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 21:59:15 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 21:59:15 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 21:59:15 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 21:59:16 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 21:59:16 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 21:59:16 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 21:59:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 21:59:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6859fdd3217ce6cda78174b39b4159a001e759607691e5cd8ffd91a23e38dabf`  
		Last Modified: Fri, 10 Feb 2023 22:00:15 GMT  
		Size: 60.6 MB (60620702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a069538501b951d72a4315d077fb0d6693149fe6ecc98fdcc71c8f1c8b8b966a`  
		Last Modified: Fri, 10 Feb 2023 22:00:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf012f3ecb3cab9ab2cb88227277f4b401712ec5b1761fc017360232e4521d0`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47c031db4cdc6a5895f3ba624d23563b7908df002d2606f43c6e7feaff5841c`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c0d0174a76dc9d34b1e6d7426a494fe303b36af8093ab1210b4f53ac64d61c`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0a416592926bca0b0deafaa886d747cb587ddc1b74d8f739ac2854d5e57314`  
		Last Modified: Fri, 10 Feb 2023 22:00:09 GMT  
		Size: 119.2 MB (119192990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec94ca3e0917562632b04892b735ef93abe25764f6ab4d745cba047193a314`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; ppc64le

```console
$ docker pull bonita@sha256:3afcd7c4a9cd6eb73634f6129e7f3345b2a875988b4b446e08af836f15f3ca98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179526480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9681e63339ee6e7dea654db4cf715448b01424ff9a19b9860fd5edd96254fa63`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:10:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 22:10:31 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 10 Feb 2023 22:10:34 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 22:10:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 22:10:36 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 22:10:36 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 22:10:37 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 22:10:37 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 22:10:38 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 22:10:38 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 10 Feb 2023 22:10:39 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 10 Feb 2023 22:10:40 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 10 Feb 2023 22:10:41 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 22:10:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 22:10:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 22:10:43 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 22:10:44 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 10 Feb 2023 22:11:02 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 22:11:04 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 22:11:05 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 22:11:05 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 22:11:06 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 22:11:06 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 22:11:07 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 22:11:07 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 22:11:08 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 22:11:08 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 22:11:09 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 22:11:09 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 22:11:10 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 22:11:10 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 22:11:11 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 22:11:11 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 22:11:11 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 22:11:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43027ea8f93d783e28c87470bd6f8dfa8a38caa6e59be6bde3fdc3adaf9e05c9`  
		Last Modified: Fri, 10 Feb 2023 22:12:48 GMT  
		Size: 57.5 MB (57518821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b812d024d679c82bd86e3b448076cd0e2c051c3e855f61230a439ccbad8aae35`  
		Last Modified: Fri, 10 Feb 2023 22:12:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9920d19a9c6f90b45d7019c0799f6ec0423d7c5742a26315093c028b625da33`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa1e85317a574bc98c9fa48eeb5a0a0de10a8012304acba65db2878efea8779`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a086a276cc700bb7070fa5ee6bd37e586495293f726db3021968bf2e98ed9a`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 3.0 KB (3050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c40145aeb952661664e02252dbfdb815944d0ca2810df50d71b13d85fbe0dc`  
		Last Modified: Fri, 10 Feb 2023 22:12:43 GMT  
		Size: 119.2 MB (119192995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa36806be8d83ec34fb0fb0cab52fd742b9d497959e7f7598d172d00fec74cdc`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.15.0`

```console
$ docker pull bonita@sha256:5a83ae61e42cdf265917c0901b79134a23e53b492e378282ad6ca527abe3e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15.0` - linux; amd64

```console
$ docker pull bonita@sha256:5d3ed4fd9f9d4cdbd623c66c5f2860105b17a18dc81152fd50709a6ac470caab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183375338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e19cd7ca4a306326e953fe500c4dd7bcf5e01b828fb0e84fd9cea954021a4ed`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:36:45 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 11 Feb 2023 07:36:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 11 Feb 2023 07:36:50 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 11 Feb 2023 07:36:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 11 Feb 2023 07:36:50 GMT
ARG BONITA_VERSION
# Sat, 11 Feb 2023 07:36:50 GMT
ARG BRANDING_VERSION
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BONITA_SHA256
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BASE_URL
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BONITA_URL
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 11 Feb 2023 07:36:51 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 11 Feb 2023 07:36:52 GMT
RUN mkdir /opt/files
# Sat, 11 Feb 2023 07:36:52 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 11 Feb 2023 07:37:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API_PASSWORD=
# Sat, 11 Feb 2023 07:37:12 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 11 Feb 2023 07:37:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 11 Feb 2023 07:37:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 11 Feb 2023 07:37:13 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 11 Feb 2023 07:37:13 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 11 Feb 2023 07:37:13 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 11 Feb 2023 07:37:13 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 11 Feb 2023 07:37:13 GMT
EXPOSE 8080 9000
# Sat, 11 Feb 2023 07:37:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 11 Feb 2023 07:37:13 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf6663e45425c152dfb7992b8c9eeb8d6cec3a4dc529df5805b63922a919b64`  
		Last Modified: Sat, 11 Feb 2023 07:38:13 GMT  
		Size: 61.4 MB (61364554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298fdbc8a6aaea5b1d47cf5e79516539019c8e4c801d07fab88568ea817933d2`  
		Last Modified: Sat, 11 Feb 2023 07:38:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6169c4b44f713d85daee9434e474d8ddb8ef418b07f2d84ed36b0ec3d86edf`  
		Last Modified: Sat, 11 Feb 2023 07:38:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda69351f0fed8d72a5e23d7b509a47ad85c0e095b97d21c648c7a9488aa8116`  
		Last Modified: Sat, 11 Feb 2023 07:38:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b74363046ff94dc8eac9b9006983ab60391b31d9d704a149b1c0ef0c45eeb9b`  
		Last Modified: Sat, 11 Feb 2023 07:38:03 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8497c92ada3f978eb9372afb70a400410a94485630824181b17ab5d0d07ecf`  
		Last Modified: Sat, 11 Feb 2023 07:38:09 GMT  
		Size: 119.2 MB (119192991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5401586f5efd8c65188ba61cda06c3a90b327feb812fedb4c5892af335e5f118`  
		Last Modified: Sat, 11 Feb 2023 07:38:02 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:d27829cdf839117630b67e67dda1aa36aee9e38b33ad3c9900103c27fd927561
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182533220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d743d25eeb0209db92987de7cf880598ab7cdeb1f10e8dc15a80befa4634599b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:59:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 21:59:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 10 Feb 2023 21:59:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 21:59:07 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 10 Feb 2023 21:59:07 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 21:59:08 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 21:59:08 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 10 Feb 2023 21:59:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 21:59:15 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 21:59:15 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 21:59:15 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 21:59:15 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 21:59:16 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 21:59:16 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 21:59:16 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 21:59:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 21:59:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6859fdd3217ce6cda78174b39b4159a001e759607691e5cd8ffd91a23e38dabf`  
		Last Modified: Fri, 10 Feb 2023 22:00:15 GMT  
		Size: 60.6 MB (60620702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a069538501b951d72a4315d077fb0d6693149fe6ecc98fdcc71c8f1c8b8b966a`  
		Last Modified: Fri, 10 Feb 2023 22:00:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf012f3ecb3cab9ab2cb88227277f4b401712ec5b1761fc017360232e4521d0`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47c031db4cdc6a5895f3ba624d23563b7908df002d2606f43c6e7feaff5841c`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c0d0174a76dc9d34b1e6d7426a494fe303b36af8093ab1210b4f53ac64d61c`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0a416592926bca0b0deafaa886d747cb587ddc1b74d8f739ac2854d5e57314`  
		Last Modified: Fri, 10 Feb 2023 22:00:09 GMT  
		Size: 119.2 MB (119192990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec94ca3e0917562632b04892b735ef93abe25764f6ab4d745cba047193a314`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:3afcd7c4a9cd6eb73634f6129e7f3345b2a875988b4b446e08af836f15f3ca98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179526480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9681e63339ee6e7dea654db4cf715448b01424ff9a19b9860fd5edd96254fa63`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:10:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 22:10:31 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 10 Feb 2023 22:10:34 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 22:10:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 22:10:36 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 22:10:36 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 22:10:37 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 22:10:37 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 22:10:38 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 22:10:38 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 10 Feb 2023 22:10:39 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 10 Feb 2023 22:10:40 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 10 Feb 2023 22:10:41 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 22:10:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 22:10:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 22:10:43 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 22:10:44 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 10 Feb 2023 22:11:02 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 22:11:04 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 22:11:05 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 22:11:05 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 22:11:06 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 22:11:06 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 22:11:07 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 22:11:07 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 22:11:08 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 22:11:08 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 22:11:09 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 22:11:09 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 22:11:10 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 22:11:10 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 22:11:11 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 22:11:11 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 22:11:11 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 22:11:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43027ea8f93d783e28c87470bd6f8dfa8a38caa6e59be6bde3fdc3adaf9e05c9`  
		Last Modified: Fri, 10 Feb 2023 22:12:48 GMT  
		Size: 57.5 MB (57518821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b812d024d679c82bd86e3b448076cd0e2c051c3e855f61230a439ccbad8aae35`  
		Last Modified: Fri, 10 Feb 2023 22:12:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9920d19a9c6f90b45d7019c0799f6ec0423d7c5742a26315093c028b625da33`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa1e85317a574bc98c9fa48eeb5a0a0de10a8012304acba65db2878efea8779`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a086a276cc700bb7070fa5ee6bd37e586495293f726db3021968bf2e98ed9a`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 3.0 KB (3050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c40145aeb952661664e02252dbfdb815944d0ca2810df50d71b13d85fbe0dc`  
		Last Modified: Fri, 10 Feb 2023 22:12:43 GMT  
		Size: 119.2 MB (119192995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa36806be8d83ec34fb0fb0cab52fd742b9d497959e7f7598d172d00fec74cdc`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:5a83ae61e42cdf265917c0901b79134a23e53b492e378282ad6ca527abe3e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:5d3ed4fd9f9d4cdbd623c66c5f2860105b17a18dc81152fd50709a6ac470caab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183375338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e19cd7ca4a306326e953fe500c4dd7bcf5e01b828fb0e84fd9cea954021a4ed`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:36:45 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 11 Feb 2023 07:36:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 11 Feb 2023 07:36:50 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 11 Feb 2023 07:36:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 11 Feb 2023 07:36:50 GMT
ARG BONITA_VERSION
# Sat, 11 Feb 2023 07:36:50 GMT
ARG BRANDING_VERSION
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BONITA_SHA256
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BASE_URL
# Sat, 11 Feb 2023 07:36:51 GMT
ARG BONITA_URL
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 11 Feb 2023 07:36:51 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 11 Feb 2023 07:36:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 11 Feb 2023 07:36:52 GMT
RUN mkdir /opt/files
# Sat, 11 Feb 2023 07:36:52 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 11 Feb 2023 07:37:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 11 Feb 2023 07:37:12 GMT
ENV HTTP_API_PASSWORD=
# Sat, 11 Feb 2023 07:37:12 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 11 Feb 2023 07:37:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 11 Feb 2023 07:37:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 11 Feb 2023 07:37:12 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 11 Feb 2023 07:37:13 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 11 Feb 2023 07:37:13 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 11 Feb 2023 07:37:13 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 11 Feb 2023 07:37:13 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 11 Feb 2023 07:37:13 GMT
EXPOSE 8080 9000
# Sat, 11 Feb 2023 07:37:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 11 Feb 2023 07:37:13 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf6663e45425c152dfb7992b8c9eeb8d6cec3a4dc529df5805b63922a919b64`  
		Last Modified: Sat, 11 Feb 2023 07:38:13 GMT  
		Size: 61.4 MB (61364554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298fdbc8a6aaea5b1d47cf5e79516539019c8e4c801d07fab88568ea817933d2`  
		Last Modified: Sat, 11 Feb 2023 07:38:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6169c4b44f713d85daee9434e474d8ddb8ef418b07f2d84ed36b0ec3d86edf`  
		Last Modified: Sat, 11 Feb 2023 07:38:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda69351f0fed8d72a5e23d7b509a47ad85c0e095b97d21c648c7a9488aa8116`  
		Last Modified: Sat, 11 Feb 2023 07:38:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b74363046ff94dc8eac9b9006983ab60391b31d9d704a149b1c0ef0c45eeb9b`  
		Last Modified: Sat, 11 Feb 2023 07:38:03 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8497c92ada3f978eb9372afb70a400410a94485630824181b17ab5d0d07ecf`  
		Last Modified: Sat, 11 Feb 2023 07:38:09 GMT  
		Size: 119.2 MB (119192991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5401586f5efd8c65188ba61cda06c3a90b327feb812fedb4c5892af335e5f118`  
		Last Modified: Sat, 11 Feb 2023 07:38:02 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:d27829cdf839117630b67e67dda1aa36aee9e38b33ad3c9900103c27fd927561
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182533220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d743d25eeb0209db92987de7cf880598ab7cdeb1f10e8dc15a80befa4634599b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:59:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 21:59:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 10 Feb 2023 21:59:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 21:59:07 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 21:59:07 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 10 Feb 2023 21:59:07 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 21:59:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 21:59:08 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 21:59:08 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 10 Feb 2023 21:59:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 21:59:15 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 21:59:15 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 21:59:15 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 21:59:15 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 21:59:15 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 21:59:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 21:59:16 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 21:59:16 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 21:59:16 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 21:59:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 21:59:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6859fdd3217ce6cda78174b39b4159a001e759607691e5cd8ffd91a23e38dabf`  
		Last Modified: Fri, 10 Feb 2023 22:00:15 GMT  
		Size: 60.6 MB (60620702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a069538501b951d72a4315d077fb0d6693149fe6ecc98fdcc71c8f1c8b8b966a`  
		Last Modified: Fri, 10 Feb 2023 22:00:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf012f3ecb3cab9ab2cb88227277f4b401712ec5b1761fc017360232e4521d0`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47c031db4cdc6a5895f3ba624d23563b7908df002d2606f43c6e7feaff5841c`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c0d0174a76dc9d34b1e6d7426a494fe303b36af8093ab1210b4f53ac64d61c`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0a416592926bca0b0deafaa886d747cb587ddc1b74d8f739ac2854d5e57314`  
		Last Modified: Fri, 10 Feb 2023 22:00:09 GMT  
		Size: 119.2 MB (119192990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec94ca3e0917562632b04892b735ef93abe25764f6ab4d745cba047193a314`  
		Last Modified: Fri, 10 Feb 2023 22:00:05 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:3afcd7c4a9cd6eb73634f6129e7f3345b2a875988b4b446e08af836f15f3ca98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179526480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9681e63339ee6e7dea654db4cf715448b01424ff9a19b9860fd5edd96254fa63`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:10:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 10 Feb 2023 22:10:31 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 10 Feb 2023 22:10:34 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 10 Feb 2023 22:10:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 10 Feb 2023 22:10:36 GMT
ARG BONITA_VERSION
# Fri, 10 Feb 2023 22:10:36 GMT
ARG BRANDING_VERSION
# Fri, 10 Feb 2023 22:10:37 GMT
ARG BONITA_SHA256
# Fri, 10 Feb 2023 22:10:37 GMT
ARG BASE_URL
# Fri, 10 Feb 2023 22:10:38 GMT
ARG BONITA_URL
# Fri, 10 Feb 2023 22:10:38 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 10 Feb 2023 22:10:39 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 10 Feb 2023 22:10:40 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 10 Feb 2023 22:10:41 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 22:10:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 10 Feb 2023 22:10:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 10 Feb 2023 22:10:43 GMT
RUN mkdir /opt/files
# Fri, 10 Feb 2023 22:10:44 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 10 Feb 2023 22:11:02 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 10 Feb 2023 22:11:04 GMT
ENV HTTP_API=false
# Fri, 10 Feb 2023 22:11:05 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 10 Feb 2023 22:11:05 GMT
ENV HTTP_API_PASSWORD=
# Fri, 10 Feb 2023 22:11:06 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 10 Feb 2023 22:11:06 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 10 Feb 2023 22:11:07 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 10 Feb 2023 22:11:07 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 10 Feb 2023 22:11:08 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 10 Feb 2023 22:11:08 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 10 Feb 2023 22:11:09 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 10 Feb 2023 22:11:09 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 10 Feb 2023 22:11:10 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 10 Feb 2023 22:11:10 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 10 Feb 2023 22:11:11 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 10 Feb 2023 22:11:11 GMT
EXPOSE 8080 9000
# Fri, 10 Feb 2023 22:11:11 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 10 Feb 2023 22:11:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43027ea8f93d783e28c87470bd6f8dfa8a38caa6e59be6bde3fdc3adaf9e05c9`  
		Last Modified: Fri, 10 Feb 2023 22:12:48 GMT  
		Size: 57.5 MB (57518821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b812d024d679c82bd86e3b448076cd0e2c051c3e855f61230a439ccbad8aae35`  
		Last Modified: Fri, 10 Feb 2023 22:12:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9920d19a9c6f90b45d7019c0799f6ec0423d7c5742a26315093c028b625da33`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa1e85317a574bc98c9fa48eeb5a0a0de10a8012304acba65db2878efea8779`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a086a276cc700bb7070fa5ee6bd37e586495293f726db3021968bf2e98ed9a`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 3.0 KB (3050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c40145aeb952661664e02252dbfdb815944d0ca2810df50d71b13d85fbe0dc`  
		Last Modified: Fri, 10 Feb 2023 22:12:43 GMT  
		Size: 119.2 MB (119192995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa36806be8d83ec34fb0fb0cab52fd742b9d497959e7f7598d172d00fec74cdc`  
		Last Modified: Fri, 10 Feb 2023 22:12:32 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
