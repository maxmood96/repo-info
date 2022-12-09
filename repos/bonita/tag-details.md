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
$ docker pull bonita@sha256:82a35f6942e00b9b591dea09b6fc567b084aada14d283a38c9df69cb2e465f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:c3cf540fee0521c60722d4d51e80b7568232f286fc830b40a450998e4a3af4bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235201259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88f421734e8683cbb7b04cda4c99f556aa110f4807e3ce31d648790d22031fe`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:37:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 01:39:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:39:09 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 01:39:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 01:39:13 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 01:39:13 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 09 Dec 2022 01:39:13 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 09 Dec 2022 01:39:13 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 09 Dec 2022 01:39:14 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 01:39:14 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 01:39:14 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 01:39:14 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 09 Dec 2022 01:39:15 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 01:39:15 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 09 Dec 2022 01:39:21 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 09 Dec 2022 01:39:22 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 09 Dec 2022 01:39:24 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 09 Dec 2022 01:39:24 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 01:39:24 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 01:39:24 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 01:39:24 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b67400bfb952641453ba80f3c8352940d972e13ae827722fe00874b7a782bd7`  
		Last Modified: Fri, 09 Dec 2022 01:40:59 GMT  
		Size: 91.6 MB (91557204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99e03c424b14911c0f0c6dac50e7d30110552db7adec43f29da8b2bb783cd69`  
		Last Modified: Fri, 09 Dec 2022 01:40:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93602938c75e0044ab3bf7eb3d1b8d8dff27e7a3787d9b839d72b2ae1d923cc`  
		Last Modified: Fri, 09 Dec 2022 01:40:47 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de9806b14c1ec0238e9079a1af7623b802cc2b6d31fac5fe61aaf713d69ce65`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 506.3 KB (506349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e26287b7e0019047f9af00cd8171c388fadccd7291fee3e4754c09ca0d2f35`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cb5f2d9d06d9c4115feeac474252e3ed25fcf990be5868c555ca1c5e4f9b8a`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e853cd9d6bc3f28e220d4456bea0693ac9155c149155fc88c36e8e72c5ddd9e`  
		Last Modified: Fri, 09 Dec 2022 01:40:50 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad90fc345c43e7ac805bd0ea952adeb457b5ed917ec9ec2283e4818b0038d9`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2039acc3d6d87fee602e76340546029bceb3b4f60a5de42d1e20e452250d19f3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226680953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64ae0b5ab900428694cece97a5d5983fcd2596ed2b1e520f834bd2c7f49d6c8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:43 GMT
ADD file:eb8b2914800b2ed866666fbff73c8234f4ac2a5ef01743d6fea0984230c2f464 in / 
# Fri, 09 Dec 2022 01:46:44 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:04:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 02:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:05:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 02:05:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 02:05:22 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 09 Dec 2022 02:05:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 02:05:23 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 09 Dec 2022 02:05:23 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 02:05:23 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 09 Dec 2022 02:05:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 09 Dec 2022 02:05:31 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 09 Dec 2022 02:05:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 09 Dec 2022 02:05:32 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 02:05:33 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 02:05:33 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 02:05:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:87acad9590b042ceb59687d498c396e9344cf2e381923fecd299555966b14975`  
		Last Modified: Fri, 09 Dec 2022 01:47:46 GMT  
		Size: 23.7 MB (23734135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ffac93d267d530fafcbf3948d26bf0025ce131f9dade39647f983d1a2ed9fd`  
		Last Modified: Fri, 09 Dec 2022 02:07:11 GMT  
		Size: 86.0 MB (86044770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcddf2b92098154350da6805d84d940415262e21cf27fb7a6df223e69aa0e0`  
		Last Modified: Fri, 09 Dec 2022 02:07:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e24951d75d953c619b81ec714dd5dfc9eaedf4421f9bfb9b4e061f83abcf65`  
		Last Modified: Fri, 09 Dec 2022 02:07:02 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48c99a89a076d928a09a78c054b3cb2f12d066cb36d71c883359107cbe3e1cf`  
		Last Modified: Fri, 09 Dec 2022 02:07:00 GMT  
		Size: 475.8 KB (475803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1994cfd02ac4b76dadd88d259826ad18b892ef74811610f3d3d7d675adf68a49`  
		Last Modified: Fri, 09 Dec 2022 02:07:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e25c0e977faa88e9a18bddc27b3344fe9e84902c52d08eb6238b31fcdfd9b9`  
		Last Modified: Fri, 09 Dec 2022 02:07:00 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab59efe62197bb620c16f0ee01ee97860daa2aea892959c3ef38d98999f37fe`  
		Last Modified: Fri, 09 Dec 2022 02:07:04 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55073cab065a6b4b9bf411189e0c70e0b95c2260387737aab0cfb70e3ee874d6`  
		Last Modified: Fri, 09 Dec 2022 02:07:01 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:5ef4e3a6c96b32ec231f530e059dfe1b71baaa78cf750ab37b77ce2a360a13fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234160943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0875be850095eb8c2e1a31ee88f765296c9b98bf35f7e4c74819045b70cab1`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:34 GMT
ADD file:254e11be9bc865d645aba7c16a39a04f5ce227b7aa4280f7a42baec47b0c6ee0 in / 
# Tue, 25 Oct 2022 03:25:36 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:58:59 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 25 Oct 2022 15:00:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 15:00:32 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 25 Oct 2022 15:00:33 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 25 Oct 2022 15:00:39 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 25 Oct 2022 15:00:39 GMT
ARG BONITA_VERSION
# Tue, 25 Oct 2022 15:00:39 GMT
ARG BRANDING_VERSION
# Tue, 25 Oct 2022 15:00:40 GMT
ARG BONITA_SHA256
# Tue, 25 Oct 2022 15:00:40 GMT
ARG BASE_URL
# Tue, 25 Oct 2022 15:00:40 GMT
ARG BONITA_URL
# Tue, 25 Oct 2022 15:00:40 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 25 Oct 2022 15:00:41 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 25 Oct 2022 15:00:41 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 25 Oct 2022 15:00:41 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 25 Oct 2022 15:00:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 25 Oct 2022 15:00:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 25 Oct 2022 15:00:43 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 25 Oct 2022 15:00:45 GMT
RUN mkdir /opt/files
# Tue, 25 Oct 2022 15:00:45 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 25 Oct 2022 15:00:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 25 Oct 2022 15:00:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 25 Oct 2022 15:00:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 25 Oct 2022 15:00:57 GMT
VOLUME [/opt/bonita]
# Tue, 25 Oct 2022 15:00:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 25 Oct 2022 15:00:58 GMT
EXPOSE 8080
# Tue, 25 Oct 2022 15:00:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:21b8f46bc1957ff60412d81678134500cf7a4f0e7f198ba384fedb2e5747d847`  
		Last Modified: Tue, 25 Oct 2022 03:27:21 GMT  
		Size: 30.4 MB (30443225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786bf908b740a06082b8cd17325b6597a3ef1380e9b186700b0fd995d958f16e`  
		Last Modified: Tue, 25 Oct 2022 15:03:47 GMT  
		Size: 86.8 MB (86816119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33059b8fceb675324742914a9bee1d0d76a22aa07638a8de985fe581d01f8703`  
		Last Modified: Tue, 25 Oct 2022 15:03:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948dcaef92716cfc0a27df29c6b4400bfbb5c016b38b0b198c9bc23afd1f95a`  
		Last Modified: Tue, 25 Oct 2022 15:03:24 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e4dbce9799a10ec7fb02699ab08e330dce68115b62afc5a8608a8789c870d9`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd48608a926fc9739c766d7212ad37c4e1b10431297e5804efbf57cb6fd41c`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d248f05ade088bc58ecb87d89fd543bc55a5c0e5f50b5b6a4672193188708ea`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e377df32a41bd395185b6a33edd822a7cd31e8bc9f43c65ac8cc97048ed381c7`  
		Last Modified: Tue, 25 Oct 2022 15:03:29 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ace1f942b1e9c2a34bcae77510d4ab73f379b2a3ba7f59d733c2d9be57e7a0e`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:7e82d12d8861f18cbe0d926b8f364eecd7df76236cc2e36c15dde58aba260fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:0996a1680b072443e0b81b3454cb4d2dd56f8da52d40420380678f656be17e29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232933922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5645866da2f25291506ef3419337b323510eb13e2dbbf74fec6491d17dacb921`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:37:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 01:39:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:39:55 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 01:39:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 01:40:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 09 Dec 2022 01:40:01 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 01:40:02 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 01:40:02 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 09 Dec 2022 01:40:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 09 Dec 2022 01:40:12 GMT
ENV HTTP_API=false
# Fri, 09 Dec 2022 01:40:12 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 01:40:13 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 01:40:13 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 01:40:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406e7b136a801ee1a5bbf5e252bec711ddeea134370829fe8edc02a09eef95ed`  
		Last Modified: Fri, 09 Dec 2022 01:41:25 GMT  
		Size: 91.6 MB (91556856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8524cec796b184bcd33942fe43bd8bac96210599581f877a6001cb5b573f2ad4`  
		Last Modified: Fri, 09 Dec 2022 01:41:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f90f0ede28c3e1f7635cd15aea20020219f32f96e7526844354f230542194`  
		Last Modified: Fri, 09 Dec 2022 01:41:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44525932583267f7864099d721358ea022fde03e80c4e5dc69172f7a090da90c`  
		Last Modified: Fri, 09 Dec 2022 01:41:11 GMT  
		Size: 930.5 KB (930479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a8426728803d922b091c2f9340e0f9b6aa63b9df59f990f8194cfb0ce4f82`  
		Last Modified: Fri, 09 Dec 2022 01:41:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0fc80c6982cf79c22f13422e2d1257f9f8ae07871bab90166e2b29e2c96d13`  
		Last Modified: Fri, 09 Dec 2022 01:41:11 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6743aa3280060c8928bc0c73f250ad7589a2ccbc5ff193ef7bae39fa52d66a12`  
		Last Modified: Fri, 09 Dec 2022 01:41:17 GMT  
		Size: 113.7 MB (113727926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935f80896a70001c8496a3c509b8797bf197a7d0c5bc8a85a5d13b7f3e951b66`  
		Last Modified: Fri, 09 Dec 2022 01:41:10 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:396489758e8965e93b099161dcc8c34db19ae5bbf307c2db0d3fb443ee2b38b3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224373724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3db79cf288db9acdc1dd7c63a5fbc0c826a9e9dfe2038f9b86d95ee3097d3d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:43 GMT
ADD file:eb8b2914800b2ed866666fbff73c8234f4ac2a5ef01743d6fea0984230c2f464 in / 
# Fri, 09 Dec 2022 01:46:44 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:04:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 02:05:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:05:54 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 02:05:55 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 02:05:59 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 02:05:59 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 02:05:59 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 09 Dec 2022 02:06:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 02:06:01 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 02:06:01 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 09 Dec 2022 02:06:26 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 09 Dec 2022 02:06:27 GMT
ENV HTTP_API=false
# Fri, 09 Dec 2022 02:06:28 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 02:06:28 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 02:06:29 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 02:06:30 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:87acad9590b042ceb59687d498c396e9344cf2e381923fecd299555966b14975`  
		Last Modified: Fri, 09 Dec 2022 01:47:46 GMT  
		Size: 23.7 MB (23734135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a78dcd7724e318e858792c3e2a7589e7a806a4742b6b9259e08c22b592da80d`  
		Last Modified: Fri, 09 Dec 2022 02:07:33 GMT  
		Size: 86.0 MB (86044869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad1a691a32b383b8bea642426334da5f7d3e513c15cc728fa9bf6f08b10e8c7`  
		Last Modified: Fri, 09 Dec 2022 02:07:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f04ea5a67added4c9f347857b4f58ab8eb44323b68bf580320bdce5950276f1`  
		Last Modified: Fri, 09 Dec 2022 02:07:24 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86359a032a372565e1cbb0792e99bb8a42ddd0a1183a94d876ed551791dd3c4b`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 859.6 KB (859577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084fa6561ba69ed0e85c3ba9151f0eda270dcdb5f088192657f2aed22c5b9106`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0434b57a4d6b8be7e667d35445b7f98f9b29396af9073caf5d39ef14628efb02`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314ae0f7b7c9269563c763de5335ff7b0201e4a70a5084cfb0db72142da687ca`  
		Last Modified: Fri, 09 Dec 2022 02:07:27 GMT  
		Size: 113.7 MB (113727935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f664eae3782404c798fa8ff6e174b999763985b43e6929e401f64863e4ff5c`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:1c8d0507483f67a146cd92ee71a9932bb7c6d4322c75f804df880c2f03c5dfd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231826002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e64debf4d35b95287c13910032120f63ecd6d1528cd9cb6023e7abc7a6e2da`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:34 GMT
ADD file:254e11be9bc865d645aba7c16a39a04f5ce227b7aa4280f7a42baec47b0c6ee0 in / 
# Tue, 25 Oct 2022 03:25:36 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:58:59 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 25 Oct 2022 15:01:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 15:01:50 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 25 Oct 2022 15:01:51 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 25 Oct 2022 15:01:56 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BONITA_VERSION
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BRANDING_VERSION
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BONITA_SHA256
# Tue, 25 Oct 2022 15:01:57 GMT
ARG BASE_URL
# Tue, 25 Oct 2022 15:01:57 GMT
ARG BONITA_URL
# Tue, 25 Oct 2022 15:01:57 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 25 Oct 2022 15:01:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 25 Oct 2022 15:01:59 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 25 Oct 2022 15:02:00 GMT
RUN mkdir /opt/files
# Tue, 25 Oct 2022 15:02:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 25 Oct 2022 15:02:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 25 Oct 2022 15:02:16 GMT
ENV HTTP_API=false
# Tue, 25 Oct 2022 15:02:18 GMT
VOLUME [/opt/bonita]
# Tue, 25 Oct 2022 15:02:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 25 Oct 2022 15:02:20 GMT
EXPOSE 8080
# Tue, 25 Oct 2022 15:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:21b8f46bc1957ff60412d81678134500cf7a4f0e7f198ba384fedb2e5747d847`  
		Last Modified: Tue, 25 Oct 2022 03:27:21 GMT  
		Size: 30.4 MB (30443225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0bd46ad19567c08c1713a7725bc00aed8394fd8f3ed9bec7ce4479c7b86c69`  
		Last Modified: Tue, 25 Oct 2022 15:04:25 GMT  
		Size: 86.8 MB (86816051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ee497a65fbc1669cf497d7ff89f1db3a0bced0347b40783fe209d3d89a3b81`  
		Last Modified: Tue, 25 Oct 2022 15:04:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca0ee0d23f6a8f675abb762ed413d8dd07e65f10b9bff344fd67aa25e41b97f`  
		Last Modified: Tue, 25 Oct 2022 15:04:06 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0f272d29db7fb9f929358e96e47a2bf8e985f250fb1f95263cc65ceda4a739`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 831.6 KB (831579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2593595c89246ea872f1210053f7de8f27b8acedefb4457a7555967dfa6c21b`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625b956766cd724dc4b950cbc195f0ec3d47ba2afcfac99a559d3768331b07c7`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a965377d658a6e91c602615fed50e102395e8d0f341e60b676cb62f27c69d`  
		Last Modified: Tue, 25 Oct 2022 15:04:19 GMT  
		Size: 113.7 MB (113727947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f50859dcba4b5885bbf6f5f1b214871dfe8ab0be5c20d65e8e4cee31a75d4e`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:7e82d12d8861f18cbe0d926b8f364eecd7df76236cc2e36c15dde58aba260fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:0996a1680b072443e0b81b3454cb4d2dd56f8da52d40420380678f656be17e29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232933922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5645866da2f25291506ef3419337b323510eb13e2dbbf74fec6491d17dacb921`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:37:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 01:39:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:39:55 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 01:39:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 01:40:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 09 Dec 2022 01:40:01 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 01:40:02 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 01:40:02 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 09 Dec 2022 01:40:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 09 Dec 2022 01:40:12 GMT
ENV HTTP_API=false
# Fri, 09 Dec 2022 01:40:12 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 01:40:13 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 01:40:13 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 01:40:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406e7b136a801ee1a5bbf5e252bec711ddeea134370829fe8edc02a09eef95ed`  
		Last Modified: Fri, 09 Dec 2022 01:41:25 GMT  
		Size: 91.6 MB (91556856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8524cec796b184bcd33942fe43bd8bac96210599581f877a6001cb5b573f2ad4`  
		Last Modified: Fri, 09 Dec 2022 01:41:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f90f0ede28c3e1f7635cd15aea20020219f32f96e7526844354f230542194`  
		Last Modified: Fri, 09 Dec 2022 01:41:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44525932583267f7864099d721358ea022fde03e80c4e5dc69172f7a090da90c`  
		Last Modified: Fri, 09 Dec 2022 01:41:11 GMT  
		Size: 930.5 KB (930479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a8426728803d922b091c2f9340e0f9b6aa63b9df59f990f8194cfb0ce4f82`  
		Last Modified: Fri, 09 Dec 2022 01:41:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0fc80c6982cf79c22f13422e2d1257f9f8ae07871bab90166e2b29e2c96d13`  
		Last Modified: Fri, 09 Dec 2022 01:41:11 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6743aa3280060c8928bc0c73f250ad7589a2ccbc5ff193ef7bae39fa52d66a12`  
		Last Modified: Fri, 09 Dec 2022 01:41:17 GMT  
		Size: 113.7 MB (113727926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935f80896a70001c8496a3c509b8797bf197a7d0c5bc8a85a5d13b7f3e951b66`  
		Last Modified: Fri, 09 Dec 2022 01:41:10 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:396489758e8965e93b099161dcc8c34db19ae5bbf307c2db0d3fb443ee2b38b3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224373724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3db79cf288db9acdc1dd7c63a5fbc0c826a9e9dfe2038f9b86d95ee3097d3d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:43 GMT
ADD file:eb8b2914800b2ed866666fbff73c8234f4ac2a5ef01743d6fea0984230c2f464 in / 
# Fri, 09 Dec 2022 01:46:44 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:04:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 02:05:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:05:54 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 02:05:55 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 02:05:59 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 02:05:59 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 02:05:59 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 09 Dec 2022 02:06:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 02:06:01 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 02:06:01 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 09 Dec 2022 02:06:26 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 09 Dec 2022 02:06:27 GMT
ENV HTTP_API=false
# Fri, 09 Dec 2022 02:06:28 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 02:06:28 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 02:06:29 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 02:06:30 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:87acad9590b042ceb59687d498c396e9344cf2e381923fecd299555966b14975`  
		Last Modified: Fri, 09 Dec 2022 01:47:46 GMT  
		Size: 23.7 MB (23734135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a78dcd7724e318e858792c3e2a7589e7a806a4742b6b9259e08c22b592da80d`  
		Last Modified: Fri, 09 Dec 2022 02:07:33 GMT  
		Size: 86.0 MB (86044869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad1a691a32b383b8bea642426334da5f7d3e513c15cc728fa9bf6f08b10e8c7`  
		Last Modified: Fri, 09 Dec 2022 02:07:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f04ea5a67added4c9f347857b4f58ab8eb44323b68bf580320bdce5950276f1`  
		Last Modified: Fri, 09 Dec 2022 02:07:24 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86359a032a372565e1cbb0792e99bb8a42ddd0a1183a94d876ed551791dd3c4b`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 859.6 KB (859577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084fa6561ba69ed0e85c3ba9151f0eda270dcdb5f088192657f2aed22c5b9106`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0434b57a4d6b8be7e667d35445b7f98f9b29396af9073caf5d39ef14628efb02`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314ae0f7b7c9269563c763de5335ff7b0201e4a70a5084cfb0db72142da687ca`  
		Last Modified: Fri, 09 Dec 2022 02:07:27 GMT  
		Size: 113.7 MB (113727935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f664eae3782404c798fa8ff6e174b999763985b43e6929e401f64863e4ff5c`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:1c8d0507483f67a146cd92ee71a9932bb7c6d4322c75f804df880c2f03c5dfd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231826002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e64debf4d35b95287c13910032120f63ecd6d1528cd9cb6023e7abc7a6e2da`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:34 GMT
ADD file:254e11be9bc865d645aba7c16a39a04f5ce227b7aa4280f7a42baec47b0c6ee0 in / 
# Tue, 25 Oct 2022 03:25:36 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:58:59 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 25 Oct 2022 15:01:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 15:01:50 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 25 Oct 2022 15:01:51 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 25 Oct 2022 15:01:56 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BONITA_VERSION
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BRANDING_VERSION
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BONITA_SHA256
# Tue, 25 Oct 2022 15:01:57 GMT
ARG BASE_URL
# Tue, 25 Oct 2022 15:01:57 GMT
ARG BONITA_URL
# Tue, 25 Oct 2022 15:01:57 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 25 Oct 2022 15:01:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 25 Oct 2022 15:01:59 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 25 Oct 2022 15:02:00 GMT
RUN mkdir /opt/files
# Tue, 25 Oct 2022 15:02:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 25 Oct 2022 15:02:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 25 Oct 2022 15:02:16 GMT
ENV HTTP_API=false
# Tue, 25 Oct 2022 15:02:18 GMT
VOLUME [/opt/bonita]
# Tue, 25 Oct 2022 15:02:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 25 Oct 2022 15:02:20 GMT
EXPOSE 8080
# Tue, 25 Oct 2022 15:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:21b8f46bc1957ff60412d81678134500cf7a4f0e7f198ba384fedb2e5747d847`  
		Last Modified: Tue, 25 Oct 2022 03:27:21 GMT  
		Size: 30.4 MB (30443225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0bd46ad19567c08c1713a7725bc00aed8394fd8f3ed9bec7ce4479c7b86c69`  
		Last Modified: Tue, 25 Oct 2022 15:04:25 GMT  
		Size: 86.8 MB (86816051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ee497a65fbc1669cf497d7ff89f1db3a0bced0347b40783fe209d3d89a3b81`  
		Last Modified: Tue, 25 Oct 2022 15:04:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca0ee0d23f6a8f675abb762ed413d8dd07e65f10b9bff344fd67aa25e41b97f`  
		Last Modified: Tue, 25 Oct 2022 15:04:06 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0f272d29db7fb9f929358e96e47a2bf8e985f250fb1f95263cc65ceda4a739`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 831.6 KB (831579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2593595c89246ea872f1210053f7de8f27b8acedefb4457a7555967dfa6c21b`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625b956766cd724dc4b950cbc195f0ec3d47ba2afcfac99a559d3768331b07c7`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a965377d658a6e91c602615fed50e102395e8d0f341e60b676cb62f27c69d`  
		Last Modified: Tue, 25 Oct 2022 15:04:19 GMT  
		Size: 113.7 MB (113727947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f50859dcba4b5885bbf6f5f1b214871dfe8ab0be5c20d65e8e4cee31a75d4e`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1`

```console
$ docker pull bonita@sha256:0f038ccdde32fa4b90a855ec5bb41db8434cfbe432cecbcde8abd01c88b0ad8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1` - linux; amd64

```console
$ docker pull bonita@sha256:862fefb5c63bd62f0d955db355c2f3f4f22e193522753d8eedc527cd683c6d9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bff25d56fe4420a99127f674a2df8588fc8fdf9319915429e3416e6f76dc008`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:14:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 06 Oct 2022 20:14:13 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 06 Oct 2022 20:14:14 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 06 Oct 2022 20:14:14 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 06 Oct 2022 20:14:14 GMT
ARG BONITA_VERSION
# Thu, 06 Oct 2022 20:14:14 GMT
ARG BRANDING_VERSION
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BONITA_SHA256
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BASE_URL
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BONITA_URL
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 06 Oct 2022 20:14:15 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 20:14:16 GMT
RUN mkdir /opt/files
# Thu, 06 Oct 2022 20:14:16 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 06 Oct 2022 20:14:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API_PASSWORD=
# Thu, 06 Oct 2022 20:14:31 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 06 Oct 2022 20:14:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 06 Oct 2022 20:14:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 06 Oct 2022 20:14:32 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 06 Oct 2022 20:14:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 06 Oct 2022 20:14:32 GMT
EXPOSE 8080 9000
# Thu, 06 Oct 2022 20:14:32 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 06 Oct 2022 20:14:32 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ede2860654ad6d68046410f9ebec3dd9b9dca61c6fd599f0045a6f5741bf9d6`  
		Last Modified: Thu, 06 Oct 2022 20:15:08 GMT  
		Size: 60.8 MB (60808866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce69fcdc27b67a89739ff4629aa93b1c46f792c65d81f096c0f8a7d81a47728`  
		Last Modified: Thu, 06 Oct 2022 20:15:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af59dcbbf223b0ac4dc3fd0d01996906c078459ddaae9684440c4cea484b89c`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2805f0e33650a409f35745444bc7f23d5e82f697438025abb67df81ec03caf4`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173969905ee8acb031228953620f4d6f959d48886d22214974e9764c2d27e28a`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afce6ae14f1b5883093c182f12ce1d593988cae499bb4372256b0301c1b00e9e`  
		Last Modified: Thu, 06 Oct 2022 20:15:05 GMT  
		Size: 116.7 MB (116690804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98acc053b219affe2080f6ddfad206474004eda9666c5b092bf9fc90aa31659`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:92b3b92dc468cfc22704a83368c85d4758c878808548637ad8401f6ba78e5282
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176177804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a01742b56399308f70d74c2477c82b5f0562160950db295a6adb0b48e8dadf`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 21:31:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 10 Nov 2022 21:31:12 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 10 Nov 2022 21:31:14 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 10 Nov 2022 21:31:14 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BONITA_VERSION
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BRANDING_VERSION
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BONITA_SHA256
# Thu, 10 Nov 2022 21:31:15 GMT
ARG BASE_URL
# Thu, 10 Nov 2022 21:31:15 GMT
ARG BONITA_URL
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 10 Nov 2022 21:31:15 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 10 Nov 2022 21:31:16 GMT
RUN mkdir /opt/files
# Thu, 10 Nov 2022 21:31:16 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 10 Nov 2022 21:31:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API_PASSWORD=
# Thu, 10 Nov 2022 21:31:25 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 10 Nov 2022 21:31:25 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 10 Nov 2022 21:31:25 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 10 Nov 2022 21:31:26 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 10 Nov 2022 21:31:26 GMT
EXPOSE 8080 9000
# Thu, 10 Nov 2022 21:31:26 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 10 Nov 2022 21:31:26 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a3ecf9c0764240ea4a002e97a93756470158670ab2d476271c5dff63411aba`  
		Last Modified: Thu, 10 Nov 2022 21:32:24 GMT  
		Size: 56.8 MB (56758527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6a3561b22a1c5d6d0052ed6e609a9b4f439038a3c9316e4a18d113bccb1cbb`  
		Last Modified: Thu, 10 Nov 2022 21:32:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3521a1d72476ad9583383dfcada876476cbebf359be2854f3719b473260f64`  
		Last Modified: Thu, 10 Nov 2022 21:32:11 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ecdb4041b3ae0840a5435e5c6d2ae2cf6a480e838b043cd029bc990ebfbbb2`  
		Last Modified: Thu, 10 Nov 2022 21:32:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2977a32ef333556aa544c36b6595d83f2cf92d76f429a58780b327eac6de9aca`  
		Last Modified: Thu, 10 Nov 2022 21:32:12 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411efc41606a6fed8126df1e7a47259412bf23cca1aad6619f8bde287a1e2a81`  
		Last Modified: Thu, 10 Nov 2022 21:32:16 GMT  
		Size: 116.7 MB (116690815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a2c6540a466d20ce7e64cbabe62163e54d535f2a5f75f8b7dfaae489c50e8e`  
		Last Modified: Thu, 10 Nov 2022 21:32:11 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:ed30ab3ec5061aff1dc71c87ce3b52a60cc3aacc160f8dcfd7692cf5f1c91383
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9e92713926d622cf557e08cf608df8445515cc2805d567604854576eabb7a1`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:20 GMT
ADD file:be31abb0aba89ed5ff9200736a1c46091abc3845d0e332efd5e5c874ef2c99d1 in / 
# Tue, 09 Aug 2022 17:17:21 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 19:56:39 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 06 Oct 2022 19:56:48 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 06 Oct 2022 19:56:51 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 06 Oct 2022 19:56:52 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BONITA_VERSION
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BRANDING_VERSION
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BONITA_SHA256
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BASE_URL
# Thu, 06 Oct 2022 19:56:54 GMT
ARG BONITA_URL
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 06 Oct 2022 19:56:55 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 19:56:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 06 Oct 2022 19:56:55 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 19:56:56 GMT
RUN mkdir /opt/files
# Thu, 06 Oct 2022 19:56:57 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 06 Oct 2022 19:57:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 06 Oct 2022 19:57:11 GMT
ENV HTTP_API=false
# Thu, 06 Oct 2022 19:57:11 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 06 Oct 2022 19:57:12 GMT
ENV HTTP_API_PASSWORD=
# Thu, 06 Oct 2022 19:57:12 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 06 Oct 2022 19:57:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 06 Oct 2022 19:57:13 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 06 Oct 2022 19:57:13 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 06 Oct 2022 19:57:13 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 06 Oct 2022 19:57:15 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 06 Oct 2022 19:57:15 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 06 Oct 2022 19:57:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 06 Oct 2022 19:57:15 GMT
EXPOSE 8080 9000
# Thu, 06 Oct 2022 19:57:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 06 Oct 2022 19:57:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:deb7065b3304c3a9834f31b8a53e8d6089060e9c6522668abd22f1f4d9f52ca7`  
		Last Modified: Tue, 09 Aug 2022 17:18:45 GMT  
		Size: 2.8 MB (2812989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef077ba375222dadf88017804c6db49ec3e6c7c7dda2b13cfe326acb96e5573`  
		Last Modified: Thu, 06 Oct 2022 19:58:18 GMT  
		Size: 56.6 MB (56628443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f9b2a0c46e4583581aea4b26d7e4888620778734b640fde9a243c60896a85c`  
		Last Modified: Thu, 06 Oct 2022 19:58:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d02cbac52ba92d847db176427502c97ac8cfce0205b8df2e17984291749fb48`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5d063ca3ad4a351f1d87243e8704f415833c9636631b3c787fdabc5893e198`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ea1f55b182c3f8c835160384e887986ba36466e0bc71aa145f0065f4198f0`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679dc7c2196ec38ed7be31a96dd4f6c81db83b6e9a8bc4efd5f2edd63c8b4fbc`  
		Last Modified: Thu, 06 Oct 2022 19:58:14 GMT  
		Size: 116.7 MB (116690860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00f2bd54e8ef56344883e905c4ee8e2f08246937858fd47004be957103b17bb`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1-u0`

```console
$ docker pull bonita@sha256:0f038ccdde32fa4b90a855ec5bb41db8434cfbe432cecbcde8abd01c88b0ad8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:862fefb5c63bd62f0d955db355c2f3f4f22e193522753d8eedc527cd683c6d9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bff25d56fe4420a99127f674a2df8588fc8fdf9319915429e3416e6f76dc008`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:14:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 06 Oct 2022 20:14:13 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 06 Oct 2022 20:14:14 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 06 Oct 2022 20:14:14 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 06 Oct 2022 20:14:14 GMT
ARG BONITA_VERSION
# Thu, 06 Oct 2022 20:14:14 GMT
ARG BRANDING_VERSION
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BONITA_SHA256
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BASE_URL
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BONITA_URL
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 06 Oct 2022 20:14:15 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 20:14:16 GMT
RUN mkdir /opt/files
# Thu, 06 Oct 2022 20:14:16 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 06 Oct 2022 20:14:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API_PASSWORD=
# Thu, 06 Oct 2022 20:14:31 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 06 Oct 2022 20:14:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 06 Oct 2022 20:14:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 06 Oct 2022 20:14:32 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 06 Oct 2022 20:14:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 06 Oct 2022 20:14:32 GMT
EXPOSE 8080 9000
# Thu, 06 Oct 2022 20:14:32 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 06 Oct 2022 20:14:32 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ede2860654ad6d68046410f9ebec3dd9b9dca61c6fd599f0045a6f5741bf9d6`  
		Last Modified: Thu, 06 Oct 2022 20:15:08 GMT  
		Size: 60.8 MB (60808866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce69fcdc27b67a89739ff4629aa93b1c46f792c65d81f096c0f8a7d81a47728`  
		Last Modified: Thu, 06 Oct 2022 20:15:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af59dcbbf223b0ac4dc3fd0d01996906c078459ddaae9684440c4cea484b89c`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2805f0e33650a409f35745444bc7f23d5e82f697438025abb67df81ec03caf4`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173969905ee8acb031228953620f4d6f959d48886d22214974e9764c2d27e28a`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afce6ae14f1b5883093c182f12ce1d593988cae499bb4372256b0301c1b00e9e`  
		Last Modified: Thu, 06 Oct 2022 20:15:05 GMT  
		Size: 116.7 MB (116690804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98acc053b219affe2080f6ddfad206474004eda9666c5b092bf9fc90aa31659`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:92b3b92dc468cfc22704a83368c85d4758c878808548637ad8401f6ba78e5282
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176177804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a01742b56399308f70d74c2477c82b5f0562160950db295a6adb0b48e8dadf`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 21:31:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 10 Nov 2022 21:31:12 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 10 Nov 2022 21:31:14 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 10 Nov 2022 21:31:14 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BONITA_VERSION
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BRANDING_VERSION
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BONITA_SHA256
# Thu, 10 Nov 2022 21:31:15 GMT
ARG BASE_URL
# Thu, 10 Nov 2022 21:31:15 GMT
ARG BONITA_URL
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 10 Nov 2022 21:31:15 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 10 Nov 2022 21:31:16 GMT
RUN mkdir /opt/files
# Thu, 10 Nov 2022 21:31:16 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 10 Nov 2022 21:31:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API_PASSWORD=
# Thu, 10 Nov 2022 21:31:25 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 10 Nov 2022 21:31:25 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 10 Nov 2022 21:31:25 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 10 Nov 2022 21:31:26 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 10 Nov 2022 21:31:26 GMT
EXPOSE 8080 9000
# Thu, 10 Nov 2022 21:31:26 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 10 Nov 2022 21:31:26 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a3ecf9c0764240ea4a002e97a93756470158670ab2d476271c5dff63411aba`  
		Last Modified: Thu, 10 Nov 2022 21:32:24 GMT  
		Size: 56.8 MB (56758527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6a3561b22a1c5d6d0052ed6e609a9b4f439038a3c9316e4a18d113bccb1cbb`  
		Last Modified: Thu, 10 Nov 2022 21:32:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3521a1d72476ad9583383dfcada876476cbebf359be2854f3719b473260f64`  
		Last Modified: Thu, 10 Nov 2022 21:32:11 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ecdb4041b3ae0840a5435e5c6d2ae2cf6a480e838b043cd029bc990ebfbbb2`  
		Last Modified: Thu, 10 Nov 2022 21:32:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2977a32ef333556aa544c36b6595d83f2cf92d76f429a58780b327eac6de9aca`  
		Last Modified: Thu, 10 Nov 2022 21:32:12 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411efc41606a6fed8126df1e7a47259412bf23cca1aad6619f8bde287a1e2a81`  
		Last Modified: Thu, 10 Nov 2022 21:32:16 GMT  
		Size: 116.7 MB (116690815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a2c6540a466d20ce7e64cbabe62163e54d535f2a5f75f8b7dfaae489c50e8e`  
		Last Modified: Thu, 10 Nov 2022 21:32:11 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:ed30ab3ec5061aff1dc71c87ce3b52a60cc3aacc160f8dcfd7692cf5f1c91383
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9e92713926d622cf557e08cf608df8445515cc2805d567604854576eabb7a1`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:20 GMT
ADD file:be31abb0aba89ed5ff9200736a1c46091abc3845d0e332efd5e5c874ef2c99d1 in / 
# Tue, 09 Aug 2022 17:17:21 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 19:56:39 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 06 Oct 2022 19:56:48 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 06 Oct 2022 19:56:51 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 06 Oct 2022 19:56:52 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BONITA_VERSION
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BRANDING_VERSION
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BONITA_SHA256
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BASE_URL
# Thu, 06 Oct 2022 19:56:54 GMT
ARG BONITA_URL
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 06 Oct 2022 19:56:55 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 19:56:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 06 Oct 2022 19:56:55 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 19:56:56 GMT
RUN mkdir /opt/files
# Thu, 06 Oct 2022 19:56:57 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 06 Oct 2022 19:57:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 06 Oct 2022 19:57:11 GMT
ENV HTTP_API=false
# Thu, 06 Oct 2022 19:57:11 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 06 Oct 2022 19:57:12 GMT
ENV HTTP_API_PASSWORD=
# Thu, 06 Oct 2022 19:57:12 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 06 Oct 2022 19:57:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 06 Oct 2022 19:57:13 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 06 Oct 2022 19:57:13 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 06 Oct 2022 19:57:13 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 06 Oct 2022 19:57:15 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 06 Oct 2022 19:57:15 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 06 Oct 2022 19:57:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 06 Oct 2022 19:57:15 GMT
EXPOSE 8080 9000
# Thu, 06 Oct 2022 19:57:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 06 Oct 2022 19:57:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:deb7065b3304c3a9834f31b8a53e8d6089060e9c6522668abd22f1f4d9f52ca7`  
		Last Modified: Tue, 09 Aug 2022 17:18:45 GMT  
		Size: 2.8 MB (2812989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef077ba375222dadf88017804c6db49ec3e6c7c7dda2b13cfe326acb96e5573`  
		Last Modified: Thu, 06 Oct 2022 19:58:18 GMT  
		Size: 56.6 MB (56628443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f9b2a0c46e4583581aea4b26d7e4888620778734b640fde9a243c60896a85c`  
		Last Modified: Thu, 06 Oct 2022 19:58:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d02cbac52ba92d847db176427502c97ac8cfce0205b8df2e17984291749fb48`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5d063ca3ad4a351f1d87243e8704f415833c9636631b3c787fdabc5893e198`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ea1f55b182c3f8c835160384e887986ba36466e0bc71aa145f0065f4198f0`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679dc7c2196ec38ed7be31a96dd4f6c81db83b6e9a8bc4efd5f2edd63c8b4fbc`  
		Last Modified: Thu, 06 Oct 2022 19:58:14 GMT  
		Size: 116.7 MB (116690860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00f2bd54e8ef56344883e905c4ee8e2f08246937858fd47004be957103b17bb`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.2`

```console
$ docker pull bonita@sha256:ab6c74c8f8157a5fca98141a6137586c41362da4a2e35a1a7b8e27aeb3d59a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2` - linux; amd64

```console
$ docker pull bonita@sha256:af0b3309cef222dc7bb8eea0171365ce7c1f04c653ce1fcb88946269cbdaa1bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183358999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9109ad12339446e49ea0fe59899c0fbc099861b68ba6dfff446717483f9db272`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:10:33 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 05:10:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 05:10:38 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 05:10:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 05:10:39 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 05:10:40 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 05:10:40 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 05:10:41 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 05:10:49 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 05:10:50 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 05:10:50 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 05:10:50 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 05:10:51 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 05:10:51 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 05:10:51 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 05:10:51 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 05:10:51 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 05:10:51 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 05:10:51 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f44ece23391fa62ec0b54a5223b0e83bf3afdf487aac2e8bcf40fceafe3c7f9`  
		Last Modified: Sat, 12 Nov 2022 05:11:27 GMT  
		Size: 61.3 MB (61349663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2f737142fcee545435fb87aad8ba19c0c5161b2123af22ed53f23cbbe74a40`  
		Last Modified: Sat, 12 Nov 2022 05:11:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b03e552725b71e9a3c2d21554036dbc8c8f37d789460fb85a83a2caf824e0a8`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8381b9f3f89adb3f9b9d686274b546978dcc1f8be9c09645ca12db9a3c0fa144`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e828375313adaa2ecd577320401dd912202ef128213370630fa123ddf458322`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cbec32dd5245f88019c4158f869ef58fdc51e7151d35b1adbcbb4d987469d0`  
		Last Modified: Sat, 12 Nov 2022 05:11:23 GMT  
		Size: 119.2 MB (119193030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ac6aa1740a5547ebbd19730284cda96651ea618939ce1a72b2db0103764307`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:bde00eff2d5e13f1c0f5a0f252e7c53e25c810d4451913d76329abfd16f89f88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182510902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb8eb0b9144f3d0cdcba7e22c5cad653298929ff2c0800dee8831210724443`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:12:26 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 04:12:30 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 04:12:31 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 04:12:32 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 04:12:32 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:12:33 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 04:12:33 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 04:12:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 04:12:42 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 04:12:42 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 04:12:43 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 04:12:43 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 04:12:43 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 04:12:43 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 04:12:43 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 04:12:43 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ce4c0a72e6d1f312d742245a673d03cf1c1a40071986286029e0a00a67480f`  
		Last Modified: Sat, 12 Nov 2022 04:13:20 GMT  
		Size: 60.6 MB (60600121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caf2b4f26366c9aae2cf0ff0f36b0ac4bf366208f938eeeab3b21f32657639c`  
		Last Modified: Sat, 12 Nov 2022 04:13:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8835deb94e6aaa2b983a18fb02dd0f8170a3e79b46ce9d67fe76b9390ccf1a12`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66d5ecba2c4fc8f635b2b2e3954ef6e3f2a3c9e881e00c59b35ed8f0e7c7b3`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dab80d34b1704dded6340f627700423b28bf8257b13c50a5812a341a71de0c`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ab7f4c30d1b1e3a2e766637f44f630946117f6aa4b404086c57031afef18d2`  
		Last Modified: Sat, 12 Nov 2022 04:13:15 GMT  
		Size: 119.2 MB (119192997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60912611891a306ce975f3597861cc95698c4f4831b69483b30193d2fbfe64d4`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:bc646851cea3a34aaeab8a829e05dec0b922b6c5e8f164f1a5388a6c04c5efa3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179512965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097c6f360acaa7279b69d25d1ad4db629ebbbcbc5e6745a637f19029edd7bf16`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:33:08 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 04:33:24 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 04:33:27 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 04:33:28 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 04:33:28 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 04:33:30 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 04:33:30 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 04:33:31 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 04:33:31 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 04:33:32 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:33:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 04:33:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:33:34 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 04:33:34 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 04:33:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 04:33:54 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 04:33:55 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 04:33:55 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 04:33:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 04:33:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 04:33:58 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 04:33:58 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 04:33:58 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 04:33:58 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 04:33:59 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a59594f530089b9a64ebc37b50c12ff83c1569c34d1d31a8d9f8eafd01bc0d8`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 57.5 MB (57508396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dfbbf9fbe77af1267d6ef466813e355c78a4b827f69744a76a1178c1165a9c`  
		Last Modified: Sat, 12 Nov 2022 04:34:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba451e84465bdf445877d0098a73aa0811961f2d4d03eb32f40162e5aeeba26f`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88b20935842b33aa0fadf0982a1cc1a4522a21dcc3d7d0062187c68adece9fd`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a540c740bc35002c6104e6212b741283455567c9395bbb50870b249cec397295`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717fd7aec4ecaedcffa16c8c06fcfc48e41141994da313ea21f63164fa3d8692`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 119.2 MB (119192984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7709ea2302b6abbd61cdf354155d561cec710e2f3db1efb45fe3bb7803466be8`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.2-u0`

```console
$ docker pull bonita@sha256:ab6c74c8f8157a5fca98141a6137586c41362da4a2e35a1a7b8e27aeb3d59a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:af0b3309cef222dc7bb8eea0171365ce7c1f04c653ce1fcb88946269cbdaa1bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183358999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9109ad12339446e49ea0fe59899c0fbc099861b68ba6dfff446717483f9db272`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:10:33 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 05:10:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 05:10:38 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 05:10:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 05:10:39 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 05:10:40 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 05:10:40 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 05:10:41 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 05:10:49 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 05:10:50 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 05:10:50 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 05:10:50 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 05:10:51 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 05:10:51 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 05:10:51 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 05:10:51 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 05:10:51 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 05:10:51 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 05:10:51 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f44ece23391fa62ec0b54a5223b0e83bf3afdf487aac2e8bcf40fceafe3c7f9`  
		Last Modified: Sat, 12 Nov 2022 05:11:27 GMT  
		Size: 61.3 MB (61349663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2f737142fcee545435fb87aad8ba19c0c5161b2123af22ed53f23cbbe74a40`  
		Last Modified: Sat, 12 Nov 2022 05:11:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b03e552725b71e9a3c2d21554036dbc8c8f37d789460fb85a83a2caf824e0a8`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8381b9f3f89adb3f9b9d686274b546978dcc1f8be9c09645ca12db9a3c0fa144`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e828375313adaa2ecd577320401dd912202ef128213370630fa123ddf458322`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cbec32dd5245f88019c4158f869ef58fdc51e7151d35b1adbcbb4d987469d0`  
		Last Modified: Sat, 12 Nov 2022 05:11:23 GMT  
		Size: 119.2 MB (119193030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ac6aa1740a5547ebbd19730284cda96651ea618939ce1a72b2db0103764307`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:bde00eff2d5e13f1c0f5a0f252e7c53e25c810d4451913d76329abfd16f89f88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182510902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb8eb0b9144f3d0cdcba7e22c5cad653298929ff2c0800dee8831210724443`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:12:26 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 04:12:30 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 04:12:31 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 04:12:32 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 04:12:32 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:12:33 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 04:12:33 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 04:12:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 04:12:42 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 04:12:42 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 04:12:43 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 04:12:43 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 04:12:43 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 04:12:43 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 04:12:43 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 04:12:43 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ce4c0a72e6d1f312d742245a673d03cf1c1a40071986286029e0a00a67480f`  
		Last Modified: Sat, 12 Nov 2022 04:13:20 GMT  
		Size: 60.6 MB (60600121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caf2b4f26366c9aae2cf0ff0f36b0ac4bf366208f938eeeab3b21f32657639c`  
		Last Modified: Sat, 12 Nov 2022 04:13:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8835deb94e6aaa2b983a18fb02dd0f8170a3e79b46ce9d67fe76b9390ccf1a12`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66d5ecba2c4fc8f635b2b2e3954ef6e3f2a3c9e881e00c59b35ed8f0e7c7b3`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dab80d34b1704dded6340f627700423b28bf8257b13c50a5812a341a71de0c`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ab7f4c30d1b1e3a2e766637f44f630946117f6aa4b404086c57031afef18d2`  
		Last Modified: Sat, 12 Nov 2022 04:13:15 GMT  
		Size: 119.2 MB (119192997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60912611891a306ce975f3597861cc95698c4f4831b69483b30193d2fbfe64d4`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:bc646851cea3a34aaeab8a829e05dec0b922b6c5e8f164f1a5388a6c04c5efa3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179512965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097c6f360acaa7279b69d25d1ad4db629ebbbcbc5e6745a637f19029edd7bf16`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:33:08 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 04:33:24 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 04:33:27 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 04:33:28 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 04:33:28 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 04:33:30 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 04:33:30 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 04:33:31 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 04:33:31 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 04:33:32 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:33:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 04:33:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:33:34 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 04:33:34 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 04:33:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 04:33:54 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 04:33:55 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 04:33:55 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 04:33:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 04:33:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 04:33:58 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 04:33:58 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 04:33:58 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 04:33:58 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 04:33:59 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a59594f530089b9a64ebc37b50c12ff83c1569c34d1d31a8d9f8eafd01bc0d8`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 57.5 MB (57508396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dfbbf9fbe77af1267d6ef466813e355c78a4b827f69744a76a1178c1165a9c`  
		Last Modified: Sat, 12 Nov 2022 04:34:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba451e84465bdf445877d0098a73aa0811961f2d4d03eb32f40162e5aeeba26f`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88b20935842b33aa0fadf0982a1cc1a4522a21dcc3d7d0062187c68adece9fd`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a540c740bc35002c6104e6212b741283455567c9395bbb50870b249cec397295`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717fd7aec4ecaedcffa16c8c06fcfc48e41141994da313ea21f63164fa3d8692`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 119.2 MB (119192984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7709ea2302b6abbd61cdf354155d561cec710e2f3db1efb45fe3bb7803466be8`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:82a35f6942e00b9b591dea09b6fc567b084aada14d283a38c9df69cb2e465f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:c3cf540fee0521c60722d4d51e80b7568232f286fc830b40a450998e4a3af4bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235201259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88f421734e8683cbb7b04cda4c99f556aa110f4807e3ce31d648790d22031fe`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:37:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 01:39:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:39:09 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 01:39:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 01:39:13 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 01:39:13 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 09 Dec 2022 01:39:13 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 09 Dec 2022 01:39:13 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 09 Dec 2022 01:39:14 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 01:39:14 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 01:39:14 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 01:39:14 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 09 Dec 2022 01:39:15 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 01:39:15 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 09 Dec 2022 01:39:21 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 09 Dec 2022 01:39:22 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 09 Dec 2022 01:39:24 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 09 Dec 2022 01:39:24 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 01:39:24 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 01:39:24 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 01:39:24 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b67400bfb952641453ba80f3c8352940d972e13ae827722fe00874b7a782bd7`  
		Last Modified: Fri, 09 Dec 2022 01:40:59 GMT  
		Size: 91.6 MB (91557204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99e03c424b14911c0f0c6dac50e7d30110552db7adec43f29da8b2bb783cd69`  
		Last Modified: Fri, 09 Dec 2022 01:40:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93602938c75e0044ab3bf7eb3d1b8d8dff27e7a3787d9b839d72b2ae1d923cc`  
		Last Modified: Fri, 09 Dec 2022 01:40:47 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de9806b14c1ec0238e9079a1af7623b802cc2b6d31fac5fe61aaf713d69ce65`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 506.3 KB (506349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e26287b7e0019047f9af00cd8171c388fadccd7291fee3e4754c09ca0d2f35`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cb5f2d9d06d9c4115feeac474252e3ed25fcf990be5868c555ca1c5e4f9b8a`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e853cd9d6bc3f28e220d4456bea0693ac9155c149155fc88c36e8e72c5ddd9e`  
		Last Modified: Fri, 09 Dec 2022 01:40:50 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad90fc345c43e7ac805bd0ea952adeb457b5ed917ec9ec2283e4818b0038d9`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2039acc3d6d87fee602e76340546029bceb3b4f60a5de42d1e20e452250d19f3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226680953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64ae0b5ab900428694cece97a5d5983fcd2596ed2b1e520f834bd2c7f49d6c8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:43 GMT
ADD file:eb8b2914800b2ed866666fbff73c8234f4ac2a5ef01743d6fea0984230c2f464 in / 
# Fri, 09 Dec 2022 01:46:44 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:04:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 02:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:05:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 02:05:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 02:05:22 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 09 Dec 2022 02:05:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 02:05:23 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 09 Dec 2022 02:05:23 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 02:05:23 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 09 Dec 2022 02:05:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 09 Dec 2022 02:05:31 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 09 Dec 2022 02:05:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 09 Dec 2022 02:05:32 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 02:05:33 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 02:05:33 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 02:05:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:87acad9590b042ceb59687d498c396e9344cf2e381923fecd299555966b14975`  
		Last Modified: Fri, 09 Dec 2022 01:47:46 GMT  
		Size: 23.7 MB (23734135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ffac93d267d530fafcbf3948d26bf0025ce131f9dade39647f983d1a2ed9fd`  
		Last Modified: Fri, 09 Dec 2022 02:07:11 GMT  
		Size: 86.0 MB (86044770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcddf2b92098154350da6805d84d940415262e21cf27fb7a6df223e69aa0e0`  
		Last Modified: Fri, 09 Dec 2022 02:07:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e24951d75d953c619b81ec714dd5dfc9eaedf4421f9bfb9b4e061f83abcf65`  
		Last Modified: Fri, 09 Dec 2022 02:07:02 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48c99a89a076d928a09a78c054b3cb2f12d066cb36d71c883359107cbe3e1cf`  
		Last Modified: Fri, 09 Dec 2022 02:07:00 GMT  
		Size: 475.8 KB (475803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1994cfd02ac4b76dadd88d259826ad18b892ef74811610f3d3d7d675adf68a49`  
		Last Modified: Fri, 09 Dec 2022 02:07:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e25c0e977faa88e9a18bddc27b3344fe9e84902c52d08eb6238b31fcdfd9b9`  
		Last Modified: Fri, 09 Dec 2022 02:07:00 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab59efe62197bb620c16f0ee01ee97860daa2aea892959c3ef38d98999f37fe`  
		Last Modified: Fri, 09 Dec 2022 02:07:04 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55073cab065a6b4b9bf411189e0c70e0b95c2260387737aab0cfb70e3ee874d6`  
		Last Modified: Fri, 09 Dec 2022 02:07:01 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:5ef4e3a6c96b32ec231f530e059dfe1b71baaa78cf750ab37b77ce2a360a13fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234160943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0875be850095eb8c2e1a31ee88f765296c9b98bf35f7e4c74819045b70cab1`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:34 GMT
ADD file:254e11be9bc865d645aba7c16a39a04f5ce227b7aa4280f7a42baec47b0c6ee0 in / 
# Tue, 25 Oct 2022 03:25:36 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:58:59 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 25 Oct 2022 15:00:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 15:00:32 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 25 Oct 2022 15:00:33 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 25 Oct 2022 15:00:39 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 25 Oct 2022 15:00:39 GMT
ARG BONITA_VERSION
# Tue, 25 Oct 2022 15:00:39 GMT
ARG BRANDING_VERSION
# Tue, 25 Oct 2022 15:00:40 GMT
ARG BONITA_SHA256
# Tue, 25 Oct 2022 15:00:40 GMT
ARG BASE_URL
# Tue, 25 Oct 2022 15:00:40 GMT
ARG BONITA_URL
# Tue, 25 Oct 2022 15:00:40 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 25 Oct 2022 15:00:41 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 25 Oct 2022 15:00:41 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 25 Oct 2022 15:00:41 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 25 Oct 2022 15:00:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 25 Oct 2022 15:00:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 25 Oct 2022 15:00:43 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 25 Oct 2022 15:00:45 GMT
RUN mkdir /opt/files
# Tue, 25 Oct 2022 15:00:45 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 25 Oct 2022 15:00:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 25 Oct 2022 15:00:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 25 Oct 2022 15:00:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 25 Oct 2022 15:00:57 GMT
VOLUME [/opt/bonita]
# Tue, 25 Oct 2022 15:00:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 25 Oct 2022 15:00:58 GMT
EXPOSE 8080
# Tue, 25 Oct 2022 15:00:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:21b8f46bc1957ff60412d81678134500cf7a4f0e7f198ba384fedb2e5747d847`  
		Last Modified: Tue, 25 Oct 2022 03:27:21 GMT  
		Size: 30.4 MB (30443225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786bf908b740a06082b8cd17325b6597a3ef1380e9b186700b0fd995d958f16e`  
		Last Modified: Tue, 25 Oct 2022 15:03:47 GMT  
		Size: 86.8 MB (86816119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33059b8fceb675324742914a9bee1d0d76a22aa07638a8de985fe581d01f8703`  
		Last Modified: Tue, 25 Oct 2022 15:03:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948dcaef92716cfc0a27df29c6b4400bfbb5c016b38b0b198c9bc23afd1f95a`  
		Last Modified: Tue, 25 Oct 2022 15:03:24 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e4dbce9799a10ec7fb02699ab08e330dce68115b62afc5a8608a8789c870d9`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd48608a926fc9739c766d7212ad37c4e1b10431297e5804efbf57cb6fd41c`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d248f05ade088bc58ecb87d89fd543bc55a5c0e5f50b5b6a4672193188708ea`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e377df32a41bd395185b6a33edd822a7cd31e8bc9f43c65ac8cc97048ed381c7`  
		Last Modified: Tue, 25 Oct 2022 15:03:29 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ace1f942b1e9c2a34bcae77510d4ab73f379b2a3ba7f59d733c2d9be57e7a0e`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:82a35f6942e00b9b591dea09b6fc567b084aada14d283a38c9df69cb2e465f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:c3cf540fee0521c60722d4d51e80b7568232f286fc830b40a450998e4a3af4bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235201259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88f421734e8683cbb7b04cda4c99f556aa110f4807e3ce31d648790d22031fe`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:37:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 01:39:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:39:09 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 01:39:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 01:39:13 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 01:39:13 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 01:39:13 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 09 Dec 2022 01:39:13 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 09 Dec 2022 01:39:13 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 09 Dec 2022 01:39:14 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 01:39:14 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 01:39:14 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 01:39:14 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 09 Dec 2022 01:39:15 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 01:39:15 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 09 Dec 2022 01:39:21 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 09 Dec 2022 01:39:22 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 09 Dec 2022 01:39:24 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 09 Dec 2022 01:39:24 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 01:39:24 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 01:39:24 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 01:39:24 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b67400bfb952641453ba80f3c8352940d972e13ae827722fe00874b7a782bd7`  
		Last Modified: Fri, 09 Dec 2022 01:40:59 GMT  
		Size: 91.6 MB (91557204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99e03c424b14911c0f0c6dac50e7d30110552db7adec43f29da8b2bb783cd69`  
		Last Modified: Fri, 09 Dec 2022 01:40:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93602938c75e0044ab3bf7eb3d1b8d8dff27e7a3787d9b839d72b2ae1d923cc`  
		Last Modified: Fri, 09 Dec 2022 01:40:47 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de9806b14c1ec0238e9079a1af7623b802cc2b6d31fac5fe61aaf713d69ce65`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 506.3 KB (506349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e26287b7e0019047f9af00cd8171c388fadccd7291fee3e4754c09ca0d2f35`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cb5f2d9d06d9c4115feeac474252e3ed25fcf990be5868c555ca1c5e4f9b8a`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e853cd9d6bc3f28e220d4456bea0693ac9155c149155fc88c36e8e72c5ddd9e`  
		Last Modified: Fri, 09 Dec 2022 01:40:50 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad90fc345c43e7ac805bd0ea952adeb457b5ed917ec9ec2283e4818b0038d9`  
		Last Modified: Fri, 09 Dec 2022 01:40:45 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2039acc3d6d87fee602e76340546029bceb3b4f60a5de42d1e20e452250d19f3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226680953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64ae0b5ab900428694cece97a5d5983fcd2596ed2b1e520f834bd2c7f49d6c8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:43 GMT
ADD file:eb8b2914800b2ed866666fbff73c8234f4ac2a5ef01743d6fea0984230c2f464 in / 
# Fri, 09 Dec 2022 01:46:44 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:04:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 02:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:05:18 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 02:05:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 02:05:22 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 02:05:22 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 09 Dec 2022 02:05:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 02:05:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 09 Dec 2022 02:05:23 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 09 Dec 2022 02:05:23 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 02:05:23 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 09 Dec 2022 02:05:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 09 Dec 2022 02:05:31 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 09 Dec 2022 02:05:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 09 Dec 2022 02:05:32 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 02:05:33 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 02:05:33 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 02:05:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:87acad9590b042ceb59687d498c396e9344cf2e381923fecd299555966b14975`  
		Last Modified: Fri, 09 Dec 2022 01:47:46 GMT  
		Size: 23.7 MB (23734135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ffac93d267d530fafcbf3948d26bf0025ce131f9dade39647f983d1a2ed9fd`  
		Last Modified: Fri, 09 Dec 2022 02:07:11 GMT  
		Size: 86.0 MB (86044770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcddf2b92098154350da6805d84d940415262e21cf27fb7a6df223e69aa0e0`  
		Last Modified: Fri, 09 Dec 2022 02:07:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e24951d75d953c619b81ec714dd5dfc9eaedf4421f9bfb9b4e061f83abcf65`  
		Last Modified: Fri, 09 Dec 2022 02:07:02 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48c99a89a076d928a09a78c054b3cb2f12d066cb36d71c883359107cbe3e1cf`  
		Last Modified: Fri, 09 Dec 2022 02:07:00 GMT  
		Size: 475.8 KB (475803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1994cfd02ac4b76dadd88d259826ad18b892ef74811610f3d3d7d675adf68a49`  
		Last Modified: Fri, 09 Dec 2022 02:07:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e25c0e977faa88e9a18bddc27b3344fe9e84902c52d08eb6238b31fcdfd9b9`  
		Last Modified: Fri, 09 Dec 2022 02:07:00 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab59efe62197bb620c16f0ee01ee97860daa2aea892959c3ef38d98999f37fe`  
		Last Modified: Fri, 09 Dec 2022 02:07:04 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55073cab065a6b4b9bf411189e0c70e0b95c2260387737aab0cfb70e3ee874d6`  
		Last Modified: Fri, 09 Dec 2022 02:07:01 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:5ef4e3a6c96b32ec231f530e059dfe1b71baaa78cf750ab37b77ce2a360a13fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234160943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0875be850095eb8c2e1a31ee88f765296c9b98bf35f7e4c74819045b70cab1`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:34 GMT
ADD file:254e11be9bc865d645aba7c16a39a04f5ce227b7aa4280f7a42baec47b0c6ee0 in / 
# Tue, 25 Oct 2022 03:25:36 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:58:59 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 25 Oct 2022 15:00:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 15:00:32 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 25 Oct 2022 15:00:33 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 25 Oct 2022 15:00:39 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 25 Oct 2022 15:00:39 GMT
ARG BONITA_VERSION
# Tue, 25 Oct 2022 15:00:39 GMT
ARG BRANDING_VERSION
# Tue, 25 Oct 2022 15:00:40 GMT
ARG BONITA_SHA256
# Tue, 25 Oct 2022 15:00:40 GMT
ARG BASE_URL
# Tue, 25 Oct 2022 15:00:40 GMT
ARG BONITA_URL
# Tue, 25 Oct 2022 15:00:40 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 25 Oct 2022 15:00:41 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 25 Oct 2022 15:00:41 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 25 Oct 2022 15:00:41 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 25 Oct 2022 15:00:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 25 Oct 2022 15:00:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 25 Oct 2022 15:00:43 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 25 Oct 2022 15:00:45 GMT
RUN mkdir /opt/files
# Tue, 25 Oct 2022 15:00:45 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 25 Oct 2022 15:00:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 25 Oct 2022 15:00:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 25 Oct 2022 15:00:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 25 Oct 2022 15:00:57 GMT
VOLUME [/opt/bonita]
# Tue, 25 Oct 2022 15:00:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 25 Oct 2022 15:00:58 GMT
EXPOSE 8080
# Tue, 25 Oct 2022 15:00:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:21b8f46bc1957ff60412d81678134500cf7a4f0e7f198ba384fedb2e5747d847`  
		Last Modified: Tue, 25 Oct 2022 03:27:21 GMT  
		Size: 30.4 MB (30443225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786bf908b740a06082b8cd17325b6597a3ef1380e9b186700b0fd995d958f16e`  
		Last Modified: Tue, 25 Oct 2022 15:03:47 GMT  
		Size: 86.8 MB (86816119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33059b8fceb675324742914a9bee1d0d76a22aa07638a8de985fe581d01f8703`  
		Last Modified: Tue, 25 Oct 2022 15:03:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948dcaef92716cfc0a27df29c6b4400bfbb5c016b38b0b198c9bc23afd1f95a`  
		Last Modified: Tue, 25 Oct 2022 15:03:24 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e4dbce9799a10ec7fb02699ab08e330dce68115b62afc5a8608a8789c870d9`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd48608a926fc9739c766d7212ad37c4e1b10431297e5804efbf57cb6fd41c`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d248f05ade088bc58ecb87d89fd543bc55a5c0e5f50b5b6a4672193188708ea`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e377df32a41bd395185b6a33edd822a7cd31e8bc9f43c65ac8cc97048ed381c7`  
		Last Modified: Tue, 25 Oct 2022 15:03:29 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ace1f942b1e9c2a34bcae77510d4ab73f379b2a3ba7f59d733c2d9be57e7a0e`  
		Last Modified: Tue, 25 Oct 2022 15:03:21 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:7e82d12d8861f18cbe0d926b8f364eecd7df76236cc2e36c15dde58aba260fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:0996a1680b072443e0b81b3454cb4d2dd56f8da52d40420380678f656be17e29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232933922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5645866da2f25291506ef3419337b323510eb13e2dbbf74fec6491d17dacb921`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:37:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 01:39:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:39:55 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 01:39:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 01:40:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 09 Dec 2022 01:40:01 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 01:40:02 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 01:40:02 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 09 Dec 2022 01:40:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 09 Dec 2022 01:40:12 GMT
ENV HTTP_API=false
# Fri, 09 Dec 2022 01:40:12 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 01:40:13 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 01:40:13 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 01:40:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406e7b136a801ee1a5bbf5e252bec711ddeea134370829fe8edc02a09eef95ed`  
		Last Modified: Fri, 09 Dec 2022 01:41:25 GMT  
		Size: 91.6 MB (91556856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8524cec796b184bcd33942fe43bd8bac96210599581f877a6001cb5b573f2ad4`  
		Last Modified: Fri, 09 Dec 2022 01:41:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f90f0ede28c3e1f7635cd15aea20020219f32f96e7526844354f230542194`  
		Last Modified: Fri, 09 Dec 2022 01:41:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44525932583267f7864099d721358ea022fde03e80c4e5dc69172f7a090da90c`  
		Last Modified: Fri, 09 Dec 2022 01:41:11 GMT  
		Size: 930.5 KB (930479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a8426728803d922b091c2f9340e0f9b6aa63b9df59f990f8194cfb0ce4f82`  
		Last Modified: Fri, 09 Dec 2022 01:41:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0fc80c6982cf79c22f13422e2d1257f9f8ae07871bab90166e2b29e2c96d13`  
		Last Modified: Fri, 09 Dec 2022 01:41:11 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6743aa3280060c8928bc0c73f250ad7589a2ccbc5ff193ef7bae39fa52d66a12`  
		Last Modified: Fri, 09 Dec 2022 01:41:17 GMT  
		Size: 113.7 MB (113727926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935f80896a70001c8496a3c509b8797bf197a7d0c5bc8a85a5d13b7f3e951b66`  
		Last Modified: Fri, 09 Dec 2022 01:41:10 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:396489758e8965e93b099161dcc8c34db19ae5bbf307c2db0d3fb443ee2b38b3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224373724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3db79cf288db9acdc1dd7c63a5fbc0c826a9e9dfe2038f9b86d95ee3097d3d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:43 GMT
ADD file:eb8b2914800b2ed866666fbff73c8234f4ac2a5ef01743d6fea0984230c2f464 in / 
# Fri, 09 Dec 2022 01:46:44 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:04:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 02:05:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:05:54 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 02:05:55 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 02:05:59 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 02:05:59 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 02:05:59 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 09 Dec 2022 02:06:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 02:06:01 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 02:06:01 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 09 Dec 2022 02:06:26 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 09 Dec 2022 02:06:27 GMT
ENV HTTP_API=false
# Fri, 09 Dec 2022 02:06:28 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 02:06:28 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 02:06:29 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 02:06:30 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:87acad9590b042ceb59687d498c396e9344cf2e381923fecd299555966b14975`  
		Last Modified: Fri, 09 Dec 2022 01:47:46 GMT  
		Size: 23.7 MB (23734135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a78dcd7724e318e858792c3e2a7589e7a806a4742b6b9259e08c22b592da80d`  
		Last Modified: Fri, 09 Dec 2022 02:07:33 GMT  
		Size: 86.0 MB (86044869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad1a691a32b383b8bea642426334da5f7d3e513c15cc728fa9bf6f08b10e8c7`  
		Last Modified: Fri, 09 Dec 2022 02:07:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f04ea5a67added4c9f347857b4f58ab8eb44323b68bf580320bdce5950276f1`  
		Last Modified: Fri, 09 Dec 2022 02:07:24 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86359a032a372565e1cbb0792e99bb8a42ddd0a1183a94d876ed551791dd3c4b`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 859.6 KB (859577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084fa6561ba69ed0e85c3ba9151f0eda270dcdb5f088192657f2aed22c5b9106`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0434b57a4d6b8be7e667d35445b7f98f9b29396af9073caf5d39ef14628efb02`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314ae0f7b7c9269563c763de5335ff7b0201e4a70a5084cfb0db72142da687ca`  
		Last Modified: Fri, 09 Dec 2022 02:07:27 GMT  
		Size: 113.7 MB (113727935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f664eae3782404c798fa8ff6e174b999763985b43e6929e401f64863e4ff5c`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:1c8d0507483f67a146cd92ee71a9932bb7c6d4322c75f804df880c2f03c5dfd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231826002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e64debf4d35b95287c13910032120f63ecd6d1528cd9cb6023e7abc7a6e2da`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:34 GMT
ADD file:254e11be9bc865d645aba7c16a39a04f5ce227b7aa4280f7a42baec47b0c6ee0 in / 
# Tue, 25 Oct 2022 03:25:36 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:58:59 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 25 Oct 2022 15:01:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 15:01:50 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 25 Oct 2022 15:01:51 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 25 Oct 2022 15:01:56 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BONITA_VERSION
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BRANDING_VERSION
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BONITA_SHA256
# Tue, 25 Oct 2022 15:01:57 GMT
ARG BASE_URL
# Tue, 25 Oct 2022 15:01:57 GMT
ARG BONITA_URL
# Tue, 25 Oct 2022 15:01:57 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 25 Oct 2022 15:01:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 25 Oct 2022 15:01:59 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 25 Oct 2022 15:02:00 GMT
RUN mkdir /opt/files
# Tue, 25 Oct 2022 15:02:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 25 Oct 2022 15:02:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 25 Oct 2022 15:02:16 GMT
ENV HTTP_API=false
# Tue, 25 Oct 2022 15:02:18 GMT
VOLUME [/opt/bonita]
# Tue, 25 Oct 2022 15:02:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 25 Oct 2022 15:02:20 GMT
EXPOSE 8080
# Tue, 25 Oct 2022 15:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:21b8f46bc1957ff60412d81678134500cf7a4f0e7f198ba384fedb2e5747d847`  
		Last Modified: Tue, 25 Oct 2022 03:27:21 GMT  
		Size: 30.4 MB (30443225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0bd46ad19567c08c1713a7725bc00aed8394fd8f3ed9bec7ce4479c7b86c69`  
		Last Modified: Tue, 25 Oct 2022 15:04:25 GMT  
		Size: 86.8 MB (86816051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ee497a65fbc1669cf497d7ff89f1db3a0bced0347b40783fe209d3d89a3b81`  
		Last Modified: Tue, 25 Oct 2022 15:04:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca0ee0d23f6a8f675abb762ed413d8dd07e65f10b9bff344fd67aa25e41b97f`  
		Last Modified: Tue, 25 Oct 2022 15:04:06 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0f272d29db7fb9f929358e96e47a2bf8e985f250fb1f95263cc65ceda4a739`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 831.6 KB (831579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2593595c89246ea872f1210053f7de8f27b8acedefb4457a7555967dfa6c21b`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625b956766cd724dc4b950cbc195f0ec3d47ba2afcfac99a559d3768331b07c7`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a965377d658a6e91c602615fed50e102395e8d0f341e60b676cb62f27c69d`  
		Last Modified: Tue, 25 Oct 2022 15:04:19 GMT  
		Size: 113.7 MB (113727947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f50859dcba4b5885bbf6f5f1b214871dfe8ab0be5c20d65e8e4cee31a75d4e`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:7e82d12d8861f18cbe0d926b8f364eecd7df76236cc2e36c15dde58aba260fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:0996a1680b072443e0b81b3454cb4d2dd56f8da52d40420380678f656be17e29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232933922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5645866da2f25291506ef3419337b323510eb13e2dbbf74fec6491d17dacb921`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:37:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 01:39:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:39:55 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 01:39:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 01:40:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 01:40:00 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 09 Dec 2022 01:40:01 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 01:40:01 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 01:40:02 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 01:40:02 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 09 Dec 2022 01:40:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 09 Dec 2022 01:40:12 GMT
ENV HTTP_API=false
# Fri, 09 Dec 2022 01:40:12 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 01:40:13 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 01:40:13 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 01:40:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406e7b136a801ee1a5bbf5e252bec711ddeea134370829fe8edc02a09eef95ed`  
		Last Modified: Fri, 09 Dec 2022 01:41:25 GMT  
		Size: 91.6 MB (91556856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8524cec796b184bcd33942fe43bd8bac96210599581f877a6001cb5b573f2ad4`  
		Last Modified: Fri, 09 Dec 2022 01:41:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f90f0ede28c3e1f7635cd15aea20020219f32f96e7526844354f230542194`  
		Last Modified: Fri, 09 Dec 2022 01:41:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44525932583267f7864099d721358ea022fde03e80c4e5dc69172f7a090da90c`  
		Last Modified: Fri, 09 Dec 2022 01:41:11 GMT  
		Size: 930.5 KB (930479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a8426728803d922b091c2f9340e0f9b6aa63b9df59f990f8194cfb0ce4f82`  
		Last Modified: Fri, 09 Dec 2022 01:41:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0fc80c6982cf79c22f13422e2d1257f9f8ae07871bab90166e2b29e2c96d13`  
		Last Modified: Fri, 09 Dec 2022 01:41:11 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6743aa3280060c8928bc0c73f250ad7589a2ccbc5ff193ef7bae39fa52d66a12`  
		Last Modified: Fri, 09 Dec 2022 01:41:17 GMT  
		Size: 113.7 MB (113727926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935f80896a70001c8496a3c509b8797bf197a7d0c5bc8a85a5d13b7f3e951b66`  
		Last Modified: Fri, 09 Dec 2022 01:41:10 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:396489758e8965e93b099161dcc8c34db19ae5bbf307c2db0d3fb443ee2b38b3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224373724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3db79cf288db9acdc1dd7c63a5fbc0c826a9e9dfe2038f9b86d95ee3097d3d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:43 GMT
ADD file:eb8b2914800b2ed866666fbff73c8234f4ac2a5ef01743d6fea0984230c2f464 in / 
# Fri, 09 Dec 2022 01:46:44 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:04:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 09 Dec 2022 02:05:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:05:54 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 09 Dec 2022 02:05:55 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 09 Dec 2022 02:05:59 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 09 Dec 2022 02:05:59 GMT
ARG BONITA_VERSION
# Fri, 09 Dec 2022 02:05:59 GMT
ARG BRANDING_VERSION
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BONITA_SHA256
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BASE_URL
# Fri, 09 Dec 2022 02:06:00 GMT
ARG BONITA_URL
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 09 Dec 2022 02:06:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 09 Dec 2022 02:06:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 09 Dec 2022 02:06:01 GMT
RUN mkdir /opt/files
# Fri, 09 Dec 2022 02:06:01 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 09 Dec 2022 02:06:26 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 09 Dec 2022 02:06:27 GMT
ENV HTTP_API=false
# Fri, 09 Dec 2022 02:06:28 GMT
VOLUME [/opt/bonita]
# Fri, 09 Dec 2022 02:06:28 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 09 Dec 2022 02:06:29 GMT
EXPOSE 8080
# Fri, 09 Dec 2022 02:06:30 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:87acad9590b042ceb59687d498c396e9344cf2e381923fecd299555966b14975`  
		Last Modified: Fri, 09 Dec 2022 01:47:46 GMT  
		Size: 23.7 MB (23734135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a78dcd7724e318e858792c3e2a7589e7a806a4742b6b9259e08c22b592da80d`  
		Last Modified: Fri, 09 Dec 2022 02:07:33 GMT  
		Size: 86.0 MB (86044869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad1a691a32b383b8bea642426334da5f7d3e513c15cc728fa9bf6f08b10e8c7`  
		Last Modified: Fri, 09 Dec 2022 02:07:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f04ea5a67added4c9f347857b4f58ab8eb44323b68bf580320bdce5950276f1`  
		Last Modified: Fri, 09 Dec 2022 02:07:24 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86359a032a372565e1cbb0792e99bb8a42ddd0a1183a94d876ed551791dd3c4b`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 859.6 KB (859577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084fa6561ba69ed0e85c3ba9151f0eda270dcdb5f088192657f2aed22c5b9106`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0434b57a4d6b8be7e667d35445b7f98f9b29396af9073caf5d39ef14628efb02`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314ae0f7b7c9269563c763de5335ff7b0201e4a70a5084cfb0db72142da687ca`  
		Last Modified: Fri, 09 Dec 2022 02:07:27 GMT  
		Size: 113.7 MB (113727935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f664eae3782404c798fa8ff6e174b999763985b43e6929e401f64863e4ff5c`  
		Last Modified: Fri, 09 Dec 2022 02:07:22 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:1c8d0507483f67a146cd92ee71a9932bb7c6d4322c75f804df880c2f03c5dfd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231826002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e64debf4d35b95287c13910032120f63ecd6d1528cd9cb6023e7abc7a6e2da`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:34 GMT
ADD file:254e11be9bc865d645aba7c16a39a04f5ce227b7aa4280f7a42baec47b0c6ee0 in / 
# Tue, 25 Oct 2022 03:25:36 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:58:59 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 25 Oct 2022 15:01:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 15:01:50 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 25 Oct 2022 15:01:51 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 25 Oct 2022 15:01:56 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BONITA_VERSION
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BRANDING_VERSION
# Tue, 25 Oct 2022 15:01:56 GMT
ARG BONITA_SHA256
# Tue, 25 Oct 2022 15:01:57 GMT
ARG BASE_URL
# Tue, 25 Oct 2022 15:01:57 GMT
ARG BONITA_URL
# Tue, 25 Oct 2022 15:01:57 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 25 Oct 2022 15:01:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 25 Oct 2022 15:01:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 25 Oct 2022 15:01:59 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 25 Oct 2022 15:02:00 GMT
RUN mkdir /opt/files
# Tue, 25 Oct 2022 15:02:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 25 Oct 2022 15:02:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 25 Oct 2022 15:02:16 GMT
ENV HTTP_API=false
# Tue, 25 Oct 2022 15:02:18 GMT
VOLUME [/opt/bonita]
# Tue, 25 Oct 2022 15:02:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 25 Oct 2022 15:02:20 GMT
EXPOSE 8080
# Tue, 25 Oct 2022 15:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:21b8f46bc1957ff60412d81678134500cf7a4f0e7f198ba384fedb2e5747d847`  
		Last Modified: Tue, 25 Oct 2022 03:27:21 GMT  
		Size: 30.4 MB (30443225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0bd46ad19567c08c1713a7725bc00aed8394fd8f3ed9bec7ce4479c7b86c69`  
		Last Modified: Tue, 25 Oct 2022 15:04:25 GMT  
		Size: 86.8 MB (86816051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ee497a65fbc1669cf497d7ff89f1db3a0bced0347b40783fe209d3d89a3b81`  
		Last Modified: Tue, 25 Oct 2022 15:04:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca0ee0d23f6a8f675abb762ed413d8dd07e65f10b9bff344fd67aa25e41b97f`  
		Last Modified: Tue, 25 Oct 2022 15:04:06 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0f272d29db7fb9f929358e96e47a2bf8e985f250fb1f95263cc65ceda4a739`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 831.6 KB (831579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2593595c89246ea872f1210053f7de8f27b8acedefb4457a7555967dfa6c21b`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625b956766cd724dc4b950cbc195f0ec3d47ba2afcfac99a559d3768331b07c7`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a965377d658a6e91c602615fed50e102395e8d0f341e60b676cb62f27c69d`  
		Last Modified: Tue, 25 Oct 2022 15:04:19 GMT  
		Size: 113.7 MB (113727947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f50859dcba4b5885bbf6f5f1b214871dfe8ab0be5c20d65e8e4cee31a75d4e`  
		Last Modified: Tue, 25 Oct 2022 15:04:04 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14`

```console
$ docker pull bonita@sha256:0f038ccdde32fa4b90a855ec5bb41db8434cfbe432cecbcde8abd01c88b0ad8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14` - linux; amd64

```console
$ docker pull bonita@sha256:862fefb5c63bd62f0d955db355c2f3f4f22e193522753d8eedc527cd683c6d9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bff25d56fe4420a99127f674a2df8588fc8fdf9319915429e3416e6f76dc008`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:14:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 06 Oct 2022 20:14:13 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 06 Oct 2022 20:14:14 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 06 Oct 2022 20:14:14 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 06 Oct 2022 20:14:14 GMT
ARG BONITA_VERSION
# Thu, 06 Oct 2022 20:14:14 GMT
ARG BRANDING_VERSION
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BONITA_SHA256
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BASE_URL
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BONITA_URL
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 06 Oct 2022 20:14:15 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 20:14:16 GMT
RUN mkdir /opt/files
# Thu, 06 Oct 2022 20:14:16 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 06 Oct 2022 20:14:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API_PASSWORD=
# Thu, 06 Oct 2022 20:14:31 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 06 Oct 2022 20:14:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 06 Oct 2022 20:14:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 06 Oct 2022 20:14:32 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 06 Oct 2022 20:14:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 06 Oct 2022 20:14:32 GMT
EXPOSE 8080 9000
# Thu, 06 Oct 2022 20:14:32 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 06 Oct 2022 20:14:32 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ede2860654ad6d68046410f9ebec3dd9b9dca61c6fd599f0045a6f5741bf9d6`  
		Last Modified: Thu, 06 Oct 2022 20:15:08 GMT  
		Size: 60.8 MB (60808866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce69fcdc27b67a89739ff4629aa93b1c46f792c65d81f096c0f8a7d81a47728`  
		Last Modified: Thu, 06 Oct 2022 20:15:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af59dcbbf223b0ac4dc3fd0d01996906c078459ddaae9684440c4cea484b89c`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2805f0e33650a409f35745444bc7f23d5e82f697438025abb67df81ec03caf4`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173969905ee8acb031228953620f4d6f959d48886d22214974e9764c2d27e28a`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afce6ae14f1b5883093c182f12ce1d593988cae499bb4372256b0301c1b00e9e`  
		Last Modified: Thu, 06 Oct 2022 20:15:05 GMT  
		Size: 116.7 MB (116690804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98acc053b219affe2080f6ddfad206474004eda9666c5b092bf9fc90aa31659`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:92b3b92dc468cfc22704a83368c85d4758c878808548637ad8401f6ba78e5282
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176177804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a01742b56399308f70d74c2477c82b5f0562160950db295a6adb0b48e8dadf`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 21:31:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 10 Nov 2022 21:31:12 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 10 Nov 2022 21:31:14 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 10 Nov 2022 21:31:14 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BONITA_VERSION
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BRANDING_VERSION
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BONITA_SHA256
# Thu, 10 Nov 2022 21:31:15 GMT
ARG BASE_URL
# Thu, 10 Nov 2022 21:31:15 GMT
ARG BONITA_URL
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 10 Nov 2022 21:31:15 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 10 Nov 2022 21:31:16 GMT
RUN mkdir /opt/files
# Thu, 10 Nov 2022 21:31:16 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 10 Nov 2022 21:31:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API_PASSWORD=
# Thu, 10 Nov 2022 21:31:25 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 10 Nov 2022 21:31:25 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 10 Nov 2022 21:31:25 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 10 Nov 2022 21:31:26 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 10 Nov 2022 21:31:26 GMT
EXPOSE 8080 9000
# Thu, 10 Nov 2022 21:31:26 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 10 Nov 2022 21:31:26 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a3ecf9c0764240ea4a002e97a93756470158670ab2d476271c5dff63411aba`  
		Last Modified: Thu, 10 Nov 2022 21:32:24 GMT  
		Size: 56.8 MB (56758527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6a3561b22a1c5d6d0052ed6e609a9b4f439038a3c9316e4a18d113bccb1cbb`  
		Last Modified: Thu, 10 Nov 2022 21:32:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3521a1d72476ad9583383dfcada876476cbebf359be2854f3719b473260f64`  
		Last Modified: Thu, 10 Nov 2022 21:32:11 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ecdb4041b3ae0840a5435e5c6d2ae2cf6a480e838b043cd029bc990ebfbbb2`  
		Last Modified: Thu, 10 Nov 2022 21:32:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2977a32ef333556aa544c36b6595d83f2cf92d76f429a58780b327eac6de9aca`  
		Last Modified: Thu, 10 Nov 2022 21:32:12 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411efc41606a6fed8126df1e7a47259412bf23cca1aad6619f8bde287a1e2a81`  
		Last Modified: Thu, 10 Nov 2022 21:32:16 GMT  
		Size: 116.7 MB (116690815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a2c6540a466d20ce7e64cbabe62163e54d535f2a5f75f8b7dfaae489c50e8e`  
		Last Modified: Thu, 10 Nov 2022 21:32:11 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; ppc64le

```console
$ docker pull bonita@sha256:ed30ab3ec5061aff1dc71c87ce3b52a60cc3aacc160f8dcfd7692cf5f1c91383
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9e92713926d622cf557e08cf608df8445515cc2805d567604854576eabb7a1`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:20 GMT
ADD file:be31abb0aba89ed5ff9200736a1c46091abc3845d0e332efd5e5c874ef2c99d1 in / 
# Tue, 09 Aug 2022 17:17:21 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 19:56:39 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 06 Oct 2022 19:56:48 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 06 Oct 2022 19:56:51 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 06 Oct 2022 19:56:52 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BONITA_VERSION
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BRANDING_VERSION
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BONITA_SHA256
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BASE_URL
# Thu, 06 Oct 2022 19:56:54 GMT
ARG BONITA_URL
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 06 Oct 2022 19:56:55 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 19:56:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 06 Oct 2022 19:56:55 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 19:56:56 GMT
RUN mkdir /opt/files
# Thu, 06 Oct 2022 19:56:57 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 06 Oct 2022 19:57:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 06 Oct 2022 19:57:11 GMT
ENV HTTP_API=false
# Thu, 06 Oct 2022 19:57:11 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 06 Oct 2022 19:57:12 GMT
ENV HTTP_API_PASSWORD=
# Thu, 06 Oct 2022 19:57:12 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 06 Oct 2022 19:57:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 06 Oct 2022 19:57:13 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 06 Oct 2022 19:57:13 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 06 Oct 2022 19:57:13 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 06 Oct 2022 19:57:15 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 06 Oct 2022 19:57:15 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 06 Oct 2022 19:57:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 06 Oct 2022 19:57:15 GMT
EXPOSE 8080 9000
# Thu, 06 Oct 2022 19:57:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 06 Oct 2022 19:57:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:deb7065b3304c3a9834f31b8a53e8d6089060e9c6522668abd22f1f4d9f52ca7`  
		Last Modified: Tue, 09 Aug 2022 17:18:45 GMT  
		Size: 2.8 MB (2812989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef077ba375222dadf88017804c6db49ec3e6c7c7dda2b13cfe326acb96e5573`  
		Last Modified: Thu, 06 Oct 2022 19:58:18 GMT  
		Size: 56.6 MB (56628443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f9b2a0c46e4583581aea4b26d7e4888620778734b640fde9a243c60896a85c`  
		Last Modified: Thu, 06 Oct 2022 19:58:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d02cbac52ba92d847db176427502c97ac8cfce0205b8df2e17984291749fb48`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5d063ca3ad4a351f1d87243e8704f415833c9636631b3c787fdabc5893e198`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ea1f55b182c3f8c835160384e887986ba36466e0bc71aa145f0065f4198f0`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679dc7c2196ec38ed7be31a96dd4f6c81db83b6e9a8bc4efd5f2edd63c8b4fbc`  
		Last Modified: Thu, 06 Oct 2022 19:58:14 GMT  
		Size: 116.7 MB (116690860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00f2bd54e8ef56344883e905c4ee8e2f08246937858fd47004be957103b17bb`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14.0`

```console
$ docker pull bonita@sha256:0f038ccdde32fa4b90a855ec5bb41db8434cfbe432cecbcde8abd01c88b0ad8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14.0` - linux; amd64

```console
$ docker pull bonita@sha256:862fefb5c63bd62f0d955db355c2f3f4f22e193522753d8eedc527cd683c6d9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bff25d56fe4420a99127f674a2df8588fc8fdf9319915429e3416e6f76dc008`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:14:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 06 Oct 2022 20:14:13 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 06 Oct 2022 20:14:14 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 06 Oct 2022 20:14:14 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 06 Oct 2022 20:14:14 GMT
ARG BONITA_VERSION
# Thu, 06 Oct 2022 20:14:14 GMT
ARG BRANDING_VERSION
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BONITA_SHA256
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BASE_URL
# Thu, 06 Oct 2022 20:14:15 GMT
ARG BONITA_URL
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 06 Oct 2022 20:14:15 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 06 Oct 2022 20:14:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 20:14:16 GMT
RUN mkdir /opt/files
# Thu, 06 Oct 2022 20:14:16 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 06 Oct 2022 20:14:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 06 Oct 2022 20:14:31 GMT
ENV HTTP_API_PASSWORD=
# Thu, 06 Oct 2022 20:14:31 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 06 Oct 2022 20:14:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 06 Oct 2022 20:14:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 06 Oct 2022 20:14:31 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 06 Oct 2022 20:14:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 06 Oct 2022 20:14:32 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 06 Oct 2022 20:14:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 06 Oct 2022 20:14:32 GMT
EXPOSE 8080 9000
# Thu, 06 Oct 2022 20:14:32 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 06 Oct 2022 20:14:32 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ede2860654ad6d68046410f9ebec3dd9b9dca61c6fd599f0045a6f5741bf9d6`  
		Last Modified: Thu, 06 Oct 2022 20:15:08 GMT  
		Size: 60.8 MB (60808866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce69fcdc27b67a89739ff4629aa93b1c46f792c65d81f096c0f8a7d81a47728`  
		Last Modified: Thu, 06 Oct 2022 20:15:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af59dcbbf223b0ac4dc3fd0d01996906c078459ddaae9684440c4cea484b89c`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2805f0e33650a409f35745444bc7f23d5e82f697438025abb67df81ec03caf4`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173969905ee8acb031228953620f4d6f959d48886d22214974e9764c2d27e28a`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afce6ae14f1b5883093c182f12ce1d593988cae499bb4372256b0301c1b00e9e`  
		Last Modified: Thu, 06 Oct 2022 20:15:05 GMT  
		Size: 116.7 MB (116690804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98acc053b219affe2080f6ddfad206474004eda9666c5b092bf9fc90aa31659`  
		Last Modified: Thu, 06 Oct 2022 20:14:58 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:92b3b92dc468cfc22704a83368c85d4758c878808548637ad8401f6ba78e5282
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176177804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a01742b56399308f70d74c2477c82b5f0562160950db295a6adb0b48e8dadf`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Thu, 10 Nov 2022 21:31:09 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 10 Nov 2022 21:31:12 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 10 Nov 2022 21:31:14 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 10 Nov 2022 21:31:14 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BONITA_VERSION
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BRANDING_VERSION
# Thu, 10 Nov 2022 21:31:14 GMT
ARG BONITA_SHA256
# Thu, 10 Nov 2022 21:31:15 GMT
ARG BASE_URL
# Thu, 10 Nov 2022 21:31:15 GMT
ARG BONITA_URL
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 10 Nov 2022 21:31:15 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 10 Nov 2022 21:31:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 10 Nov 2022 21:31:16 GMT
RUN mkdir /opt/files
# Thu, 10 Nov 2022 21:31:16 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 10 Nov 2022 21:31:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_API_PASSWORD=
# Thu, 10 Nov 2022 21:31:25 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 10 Nov 2022 21:31:25 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 10 Nov 2022 21:31:25 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 10 Nov 2022 21:31:25 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 10 Nov 2022 21:31:25 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 10 Nov 2022 21:31:26 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 10 Nov 2022 21:31:26 GMT
EXPOSE 8080 9000
# Thu, 10 Nov 2022 21:31:26 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 10 Nov 2022 21:31:26 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a3ecf9c0764240ea4a002e97a93756470158670ab2d476271c5dff63411aba`  
		Last Modified: Thu, 10 Nov 2022 21:32:24 GMT  
		Size: 56.8 MB (56758527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6a3561b22a1c5d6d0052ed6e609a9b4f439038a3c9316e4a18d113bccb1cbb`  
		Last Modified: Thu, 10 Nov 2022 21:32:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3521a1d72476ad9583383dfcada876476cbebf359be2854f3719b473260f64`  
		Last Modified: Thu, 10 Nov 2022 21:32:11 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ecdb4041b3ae0840a5435e5c6d2ae2cf6a480e838b043cd029bc990ebfbbb2`  
		Last Modified: Thu, 10 Nov 2022 21:32:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2977a32ef333556aa544c36b6595d83f2cf92d76f429a58780b327eac6de9aca`  
		Last Modified: Thu, 10 Nov 2022 21:32:12 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411efc41606a6fed8126df1e7a47259412bf23cca1aad6619f8bde287a1e2a81`  
		Last Modified: Thu, 10 Nov 2022 21:32:16 GMT  
		Size: 116.7 MB (116690815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a2c6540a466d20ce7e64cbabe62163e54d535f2a5f75f8b7dfaae489c50e8e`  
		Last Modified: Thu, 10 Nov 2022 21:32:11 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:ed30ab3ec5061aff1dc71c87ce3b52a60cc3aacc160f8dcfd7692cf5f1c91383
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9e92713926d622cf557e08cf608df8445515cc2805d567604854576eabb7a1`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:20 GMT
ADD file:be31abb0aba89ed5ff9200736a1c46091abc3845d0e332efd5e5c874ef2c99d1 in / 
# Tue, 09 Aug 2022 17:17:21 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 19:56:39 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 06 Oct 2022 19:56:48 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Thu, 06 Oct 2022 19:56:51 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 06 Oct 2022 19:56:52 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BONITA_VERSION
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BRANDING_VERSION
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BONITA_SHA256
# Thu, 06 Oct 2022 19:56:53 GMT
ARG BASE_URL
# Thu, 06 Oct 2022 19:56:54 GMT
ARG BONITA_URL
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BONITA_VERSION=7.14.0
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BRANDING_VERSION=2022.1-u0
# Thu, 06 Oct 2022 19:56:54 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Thu, 06 Oct 2022 19:56:55 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 19:56:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 06 Oct 2022 19:56:55 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Thu, 06 Oct 2022 19:56:56 GMT
RUN mkdir /opt/files
# Thu, 06 Oct 2022 19:56:57 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Thu, 06 Oct 2022 19:57:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 06 Oct 2022 19:57:11 GMT
ENV HTTP_API=false
# Thu, 06 Oct 2022 19:57:11 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 06 Oct 2022 19:57:12 GMT
ENV HTTP_API_PASSWORD=
# Thu, 06 Oct 2022 19:57:12 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 06 Oct 2022 19:57:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 06 Oct 2022 19:57:13 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 06 Oct 2022 19:57:13 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 06 Oct 2022 19:57:13 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 06 Oct 2022 19:57:14 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 06 Oct 2022 19:57:15 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 06 Oct 2022 19:57:15 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 06 Oct 2022 19:57:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Thu, 06 Oct 2022 19:57:15 GMT
EXPOSE 8080 9000
# Thu, 06 Oct 2022 19:57:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 06 Oct 2022 19:57:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:deb7065b3304c3a9834f31b8a53e8d6089060e9c6522668abd22f1f4d9f52ca7`  
		Last Modified: Tue, 09 Aug 2022 17:18:45 GMT  
		Size: 2.8 MB (2812989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef077ba375222dadf88017804c6db49ec3e6c7c7dda2b13cfe326acb96e5573`  
		Last Modified: Thu, 06 Oct 2022 19:58:18 GMT  
		Size: 56.6 MB (56628443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f9b2a0c46e4583581aea4b26d7e4888620778734b640fde9a243c60896a85c`  
		Last Modified: Thu, 06 Oct 2022 19:58:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d02cbac52ba92d847db176427502c97ac8cfce0205b8df2e17984291749fb48`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5d063ca3ad4a351f1d87243e8704f415833c9636631b3c787fdabc5893e198`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8ea1f55b182c3f8c835160384e887986ba36466e0bc71aa145f0065f4198f0`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679dc7c2196ec38ed7be31a96dd4f6c81db83b6e9a8bc4efd5f2edd63c8b4fbc`  
		Last Modified: Thu, 06 Oct 2022 19:58:14 GMT  
		Size: 116.7 MB (116690860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00f2bd54e8ef56344883e905c4ee8e2f08246937858fd47004be957103b17bb`  
		Last Modified: Thu, 06 Oct 2022 19:58:03 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.15`

```console
$ docker pull bonita@sha256:ab6c74c8f8157a5fca98141a6137586c41362da4a2e35a1a7b8e27aeb3d59a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15` - linux; amd64

```console
$ docker pull bonita@sha256:af0b3309cef222dc7bb8eea0171365ce7c1f04c653ce1fcb88946269cbdaa1bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183358999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9109ad12339446e49ea0fe59899c0fbc099861b68ba6dfff446717483f9db272`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:10:33 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 05:10:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 05:10:38 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 05:10:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 05:10:39 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 05:10:40 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 05:10:40 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 05:10:41 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 05:10:49 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 05:10:50 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 05:10:50 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 05:10:50 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 05:10:51 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 05:10:51 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 05:10:51 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 05:10:51 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 05:10:51 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 05:10:51 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 05:10:51 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f44ece23391fa62ec0b54a5223b0e83bf3afdf487aac2e8bcf40fceafe3c7f9`  
		Last Modified: Sat, 12 Nov 2022 05:11:27 GMT  
		Size: 61.3 MB (61349663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2f737142fcee545435fb87aad8ba19c0c5161b2123af22ed53f23cbbe74a40`  
		Last Modified: Sat, 12 Nov 2022 05:11:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b03e552725b71e9a3c2d21554036dbc8c8f37d789460fb85a83a2caf824e0a8`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8381b9f3f89adb3f9b9d686274b546978dcc1f8be9c09645ca12db9a3c0fa144`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e828375313adaa2ecd577320401dd912202ef128213370630fa123ddf458322`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cbec32dd5245f88019c4158f869ef58fdc51e7151d35b1adbcbb4d987469d0`  
		Last Modified: Sat, 12 Nov 2022 05:11:23 GMT  
		Size: 119.2 MB (119193030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ac6aa1740a5547ebbd19730284cda96651ea618939ce1a72b2db0103764307`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:bde00eff2d5e13f1c0f5a0f252e7c53e25c810d4451913d76329abfd16f89f88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182510902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb8eb0b9144f3d0cdcba7e22c5cad653298929ff2c0800dee8831210724443`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:12:26 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 04:12:30 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 04:12:31 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 04:12:32 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 04:12:32 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:12:33 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 04:12:33 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 04:12:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 04:12:42 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 04:12:42 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 04:12:43 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 04:12:43 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 04:12:43 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 04:12:43 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 04:12:43 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 04:12:43 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ce4c0a72e6d1f312d742245a673d03cf1c1a40071986286029e0a00a67480f`  
		Last Modified: Sat, 12 Nov 2022 04:13:20 GMT  
		Size: 60.6 MB (60600121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caf2b4f26366c9aae2cf0ff0f36b0ac4bf366208f938eeeab3b21f32657639c`  
		Last Modified: Sat, 12 Nov 2022 04:13:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8835deb94e6aaa2b983a18fb02dd0f8170a3e79b46ce9d67fe76b9390ccf1a12`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66d5ecba2c4fc8f635b2b2e3954ef6e3f2a3c9e881e00c59b35ed8f0e7c7b3`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dab80d34b1704dded6340f627700423b28bf8257b13c50a5812a341a71de0c`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ab7f4c30d1b1e3a2e766637f44f630946117f6aa4b404086c57031afef18d2`  
		Last Modified: Sat, 12 Nov 2022 04:13:15 GMT  
		Size: 119.2 MB (119192997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60912611891a306ce975f3597861cc95698c4f4831b69483b30193d2fbfe64d4`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; ppc64le

```console
$ docker pull bonita@sha256:bc646851cea3a34aaeab8a829e05dec0b922b6c5e8f164f1a5388a6c04c5efa3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179512965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097c6f360acaa7279b69d25d1ad4db629ebbbcbc5e6745a637f19029edd7bf16`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:33:08 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 04:33:24 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 04:33:27 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 04:33:28 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 04:33:28 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 04:33:30 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 04:33:30 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 04:33:31 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 04:33:31 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 04:33:32 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:33:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 04:33:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:33:34 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 04:33:34 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 04:33:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 04:33:54 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 04:33:55 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 04:33:55 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 04:33:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 04:33:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 04:33:58 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 04:33:58 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 04:33:58 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 04:33:58 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 04:33:59 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a59594f530089b9a64ebc37b50c12ff83c1569c34d1d31a8d9f8eafd01bc0d8`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 57.5 MB (57508396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dfbbf9fbe77af1267d6ef466813e355c78a4b827f69744a76a1178c1165a9c`  
		Last Modified: Sat, 12 Nov 2022 04:34:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba451e84465bdf445877d0098a73aa0811961f2d4d03eb32f40162e5aeeba26f`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88b20935842b33aa0fadf0982a1cc1a4522a21dcc3d7d0062187c68adece9fd`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a540c740bc35002c6104e6212b741283455567c9395bbb50870b249cec397295`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717fd7aec4ecaedcffa16c8c06fcfc48e41141994da313ea21f63164fa3d8692`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 119.2 MB (119192984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7709ea2302b6abbd61cdf354155d561cec710e2f3db1efb45fe3bb7803466be8`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.15.0`

```console
$ docker pull bonita@sha256:ab6c74c8f8157a5fca98141a6137586c41362da4a2e35a1a7b8e27aeb3d59a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15.0` - linux; amd64

```console
$ docker pull bonita@sha256:af0b3309cef222dc7bb8eea0171365ce7c1f04c653ce1fcb88946269cbdaa1bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183358999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9109ad12339446e49ea0fe59899c0fbc099861b68ba6dfff446717483f9db272`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:10:33 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 05:10:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 05:10:38 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 05:10:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 05:10:39 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 05:10:40 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 05:10:40 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 05:10:41 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 05:10:49 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 05:10:50 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 05:10:50 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 05:10:50 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 05:10:51 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 05:10:51 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 05:10:51 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 05:10:51 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 05:10:51 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 05:10:51 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 05:10:51 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f44ece23391fa62ec0b54a5223b0e83bf3afdf487aac2e8bcf40fceafe3c7f9`  
		Last Modified: Sat, 12 Nov 2022 05:11:27 GMT  
		Size: 61.3 MB (61349663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2f737142fcee545435fb87aad8ba19c0c5161b2123af22ed53f23cbbe74a40`  
		Last Modified: Sat, 12 Nov 2022 05:11:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b03e552725b71e9a3c2d21554036dbc8c8f37d789460fb85a83a2caf824e0a8`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8381b9f3f89adb3f9b9d686274b546978dcc1f8be9c09645ca12db9a3c0fa144`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e828375313adaa2ecd577320401dd912202ef128213370630fa123ddf458322`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cbec32dd5245f88019c4158f869ef58fdc51e7151d35b1adbcbb4d987469d0`  
		Last Modified: Sat, 12 Nov 2022 05:11:23 GMT  
		Size: 119.2 MB (119193030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ac6aa1740a5547ebbd19730284cda96651ea618939ce1a72b2db0103764307`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:bde00eff2d5e13f1c0f5a0f252e7c53e25c810d4451913d76329abfd16f89f88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182510902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb8eb0b9144f3d0cdcba7e22c5cad653298929ff2c0800dee8831210724443`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:12:26 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 04:12:30 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 04:12:31 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 04:12:32 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 04:12:32 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:12:33 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 04:12:33 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 04:12:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 04:12:42 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 04:12:42 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 04:12:43 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 04:12:43 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 04:12:43 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 04:12:43 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 04:12:43 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 04:12:43 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ce4c0a72e6d1f312d742245a673d03cf1c1a40071986286029e0a00a67480f`  
		Last Modified: Sat, 12 Nov 2022 04:13:20 GMT  
		Size: 60.6 MB (60600121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caf2b4f26366c9aae2cf0ff0f36b0ac4bf366208f938eeeab3b21f32657639c`  
		Last Modified: Sat, 12 Nov 2022 04:13:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8835deb94e6aaa2b983a18fb02dd0f8170a3e79b46ce9d67fe76b9390ccf1a12`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66d5ecba2c4fc8f635b2b2e3954ef6e3f2a3c9e881e00c59b35ed8f0e7c7b3`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dab80d34b1704dded6340f627700423b28bf8257b13c50a5812a341a71de0c`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ab7f4c30d1b1e3a2e766637f44f630946117f6aa4b404086c57031afef18d2`  
		Last Modified: Sat, 12 Nov 2022 04:13:15 GMT  
		Size: 119.2 MB (119192997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60912611891a306ce975f3597861cc95698c4f4831b69483b30193d2fbfe64d4`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:bc646851cea3a34aaeab8a829e05dec0b922b6c5e8f164f1a5388a6c04c5efa3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179512965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097c6f360acaa7279b69d25d1ad4db629ebbbcbc5e6745a637f19029edd7bf16`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:33:08 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 04:33:24 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 04:33:27 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 04:33:28 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 04:33:28 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 04:33:30 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 04:33:30 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 04:33:31 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 04:33:31 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 04:33:32 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:33:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 04:33:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:33:34 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 04:33:34 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 04:33:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 04:33:54 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 04:33:55 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 04:33:55 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 04:33:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 04:33:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 04:33:58 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 04:33:58 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 04:33:58 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 04:33:58 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 04:33:59 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a59594f530089b9a64ebc37b50c12ff83c1569c34d1d31a8d9f8eafd01bc0d8`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 57.5 MB (57508396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dfbbf9fbe77af1267d6ef466813e355c78a4b827f69744a76a1178c1165a9c`  
		Last Modified: Sat, 12 Nov 2022 04:34:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba451e84465bdf445877d0098a73aa0811961f2d4d03eb32f40162e5aeeba26f`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88b20935842b33aa0fadf0982a1cc1a4522a21dcc3d7d0062187c68adece9fd`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a540c740bc35002c6104e6212b741283455567c9395bbb50870b249cec397295`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717fd7aec4ecaedcffa16c8c06fcfc48e41141994da313ea21f63164fa3d8692`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 119.2 MB (119192984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7709ea2302b6abbd61cdf354155d561cec710e2f3db1efb45fe3bb7803466be8`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:ab6c74c8f8157a5fca98141a6137586c41362da4a2e35a1a7b8e27aeb3d59a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:af0b3309cef222dc7bb8eea0171365ce7c1f04c653ce1fcb88946269cbdaa1bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183358999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9109ad12339446e49ea0fe59899c0fbc099861b68ba6dfff446717483f9db272`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:10:33 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 05:10:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 05:10:38 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 05:10:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 05:10:39 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 05:10:39 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 05:10:40 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 05:10:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 05:10:40 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 05:10:41 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 05:10:49 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 05:10:50 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 05:10:50 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 05:10:50 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 05:10:50 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 05:10:50 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 05:10:51 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 05:10:51 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 05:10:51 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 05:10:51 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 05:10:51 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 05:10:51 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 05:10:51 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f44ece23391fa62ec0b54a5223b0e83bf3afdf487aac2e8bcf40fceafe3c7f9`  
		Last Modified: Sat, 12 Nov 2022 05:11:27 GMT  
		Size: 61.3 MB (61349663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2f737142fcee545435fb87aad8ba19c0c5161b2123af22ed53f23cbbe74a40`  
		Last Modified: Sat, 12 Nov 2022 05:11:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b03e552725b71e9a3c2d21554036dbc8c8f37d789460fb85a83a2caf824e0a8`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8381b9f3f89adb3f9b9d686274b546978dcc1f8be9c09645ca12db9a3c0fa144`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e828375313adaa2ecd577320401dd912202ef128213370630fa123ddf458322`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cbec32dd5245f88019c4158f869ef58fdc51e7151d35b1adbcbb4d987469d0`  
		Last Modified: Sat, 12 Nov 2022 05:11:23 GMT  
		Size: 119.2 MB (119193030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ac6aa1740a5547ebbd19730284cda96651ea618939ce1a72b2db0103764307`  
		Last Modified: Sat, 12 Nov 2022 05:11:16 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:bde00eff2d5e13f1c0f5a0f252e7c53e25c810d4451913d76329abfd16f89f88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182510902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb8eb0b9144f3d0cdcba7e22c5cad653298929ff2c0800dee8831210724443`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:12:26 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 04:12:30 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 04:12:31 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 04:12:32 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 04:12:32 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 04:12:32 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 04:12:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:12:33 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 04:12:33 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 04:12:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 04:12:42 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 04:12:42 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 04:12:42 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 04:12:43 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 04:12:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 04:12:43 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 04:12:43 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 04:12:43 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 04:12:43 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 04:12:43 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ce4c0a72e6d1f312d742245a673d03cf1c1a40071986286029e0a00a67480f`  
		Last Modified: Sat, 12 Nov 2022 04:13:20 GMT  
		Size: 60.6 MB (60600121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2caf2b4f26366c9aae2cf0ff0f36b0ac4bf366208f938eeeab3b21f32657639c`  
		Last Modified: Sat, 12 Nov 2022 04:13:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8835deb94e6aaa2b983a18fb02dd0f8170a3e79b46ce9d67fe76b9390ccf1a12`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66d5ecba2c4fc8f635b2b2e3954ef6e3f2a3c9e881e00c59b35ed8f0e7c7b3`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dab80d34b1704dded6340f627700423b28bf8257b13c50a5812a341a71de0c`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ab7f4c30d1b1e3a2e766637f44f630946117f6aa4b404086c57031afef18d2`  
		Last Modified: Sat, 12 Nov 2022 04:13:15 GMT  
		Size: 119.2 MB (119192997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60912611891a306ce975f3597861cc95698c4f4831b69483b30193d2fbfe64d4`  
		Last Modified: Sat, 12 Nov 2022 04:13:10 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:bc646851cea3a34aaeab8a829e05dec0b922b6c5e8f164f1a5388a6c04c5efa3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179512965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097c6f360acaa7279b69d25d1ad4db629ebbbcbc5e6745a637f19029edd7bf16`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:33:08 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 12 Nov 2022 04:33:24 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 12 Nov 2022 04:33:27 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 12 Nov 2022 04:33:28 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 12 Nov 2022 04:33:28 GMT
ARG BONITA_VERSION
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BRANDING_VERSION
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BONITA_SHA256
# Sat, 12 Nov 2022 04:33:29 GMT
ARG BASE_URL
# Sat, 12 Nov 2022 04:33:30 GMT
ARG BONITA_URL
# Sat, 12 Nov 2022 04:33:30 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 12 Nov 2022 04:33:31 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 12 Nov 2022 04:33:31 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 12 Nov 2022 04:33:32 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:33:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 12 Nov 2022 04:33:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 12 Nov 2022 04:33:34 GMT
RUN mkdir /opt/files
# Sat, 12 Nov 2022 04:33:34 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 12 Nov 2022 04:33:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API=false
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 12 Nov 2022 04:33:54 GMT
ENV HTTP_API_PASSWORD=
# Sat, 12 Nov 2022 04:33:54 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 12 Nov 2022 04:33:55 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 12 Nov 2022 04:33:55 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 12 Nov 2022 04:33:56 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 12 Nov 2022 04:33:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 12 Nov 2022 04:33:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 12 Nov 2022 04:33:58 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 12 Nov 2022 04:33:58 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 12 Nov 2022 04:33:58 GMT
EXPOSE 8080 9000
# Sat, 12 Nov 2022 04:33:58 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 12 Nov 2022 04:33:59 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a59594f530089b9a64ebc37b50c12ff83c1569c34d1d31a8d9f8eafd01bc0d8`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 57.5 MB (57508396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dfbbf9fbe77af1267d6ef466813e355c78a4b827f69744a76a1178c1165a9c`  
		Last Modified: Sat, 12 Nov 2022 04:34:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba451e84465bdf445877d0098a73aa0811961f2d4d03eb32f40162e5aeeba26f`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88b20935842b33aa0fadf0982a1cc1a4522a21dcc3d7d0062187c68adece9fd`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a540c740bc35002c6104e6212b741283455567c9395bbb50870b249cec397295`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717fd7aec4ecaedcffa16c8c06fcfc48e41141994da313ea21f63164fa3d8692`  
		Last Modified: Sat, 12 Nov 2022 04:35:11 GMT  
		Size: 119.2 MB (119192984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7709ea2302b6abbd61cdf354155d561cec710e2f3db1efb45fe3bb7803466be8`  
		Last Modified: Sat, 12 Nov 2022 04:34:55 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
