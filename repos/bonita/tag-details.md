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
$ docker pull bonita@sha256:eadcfc347646575bfc80103ede0823cafaebf0cce1ccc63889fe392c3eba1334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:faa5c9ed7d34ccec525035d081de48feca3c8e0b75ea802b7dfebeee9dc0a223
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237408988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207ab007fc31f10d70929a6658dacf1e9f9b761573cc6e383ee33f375d0c2b49`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:38:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:39:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:39:49 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:39:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:39:52 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:39:52 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:40:11 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 29 Apr 2022 23:40:12 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:40:12 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:40:13 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:40:13 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 29 Apr 2022 23:40:21 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:40:22 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:40:23 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:40:23 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:40:24 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:40:24 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:40:24 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca3aae8c772c52e56d308d7a94719a1f5837917f6e87a216400d4a5445ebdf`  
		Last Modified: Fri, 29 Apr 2022 23:41:39 GMT  
		Size: 93.7 MB (93695508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1643a51cc7a8bfcca6148bcf66667508761251947a4fdef917b047ce60fe5570`  
		Last Modified: Fri, 29 Apr 2022 23:41:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2402a2b3c43454a2bad134131e419b0e8b9a83eb7aa0a0d3e87b613995daf641`  
		Last Modified: Fri, 29 Apr 2022 23:41:27 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05300e43655cf3d031bbecd3cf1a14416512ddc88b712a229c2ad91d3f0803c1`  
		Last Modified: Fri, 29 Apr 2022 23:41:26 GMT  
		Size: 578.1 KB (578132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db44dfe88160e6c127c511e7fac5edee94a42b93554ef13ac2c88af9703b318f`  
		Last Modified: Fri, 29 Apr 2022 23:41:49 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7390092e3be5c3e2b3ed82a087431e69a65a0bbb8a42b1b01be95faa95e643`  
		Last Modified: Fri, 29 Apr 2022 23:41:49 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f4fb48fb3f279efa4dc8e52c45283f7e73ebbf61233fca30a29cb02e1378bd`  
		Last Modified: Fri, 29 Apr 2022 23:41:54 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def6e6b22eec7d322588e14e73ebd9229f5c2a6d3f4fef1b9211a1d00798f118`  
		Last Modified: Fri, 29 Apr 2022 23:41:49 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5551862c7660da4af0f7cc9c9a9e5edcec09345a006e1498b5532fbf6d8a3eed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226520879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a11c5b28dad948c4bdead527a2cea3128803d8a4fe7125586fe0f6cd993c282`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:08:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:08:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:08:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:08:32 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:08:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:08:42 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:09:19 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:09:20 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:09:21 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:09:22 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:09:23 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 29 Apr 2022 23:09:24 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 29 Apr 2022 23:09:25 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 29 Apr 2022 23:09:26 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:09:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:09:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:09:29 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:09:30 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:09:32 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 29 Apr 2022 23:09:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:09:38 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:09:40 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:09:40 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:09:42 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:09:42 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:09:43 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f12337ad9a174c4f77881b8dbcb65f62a7fc10574a432c7118b59ad112dbd2`  
		Last Modified: Fri, 29 Apr 2022 23:11:40 GMT  
		Size: 85.8 MB (85811732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91166d3caec0b5cacb26aae01bc16d5d7782a114b68ab5e09a68b18a90c3dfc6`  
		Last Modified: Fri, 29 Apr 2022 23:11:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b44ff2f6d502d14b27d552c3874024acd360c54e4d65f15f24de7479e27ec2`  
		Last Modified: Fri, 29 Apr 2022 23:11:28 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d38292d92a3d092cb6db160054239872b77c787f359641e8906be79fbf199`  
		Last Modified: Fri, 29 Apr 2022 23:11:26 GMT  
		Size: 548.0 KB (547952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4560861bc9d90d917021f62f13ca94caa3b3788cb23417b1747db412c6ac3`  
		Last Modified: Fri, 29 Apr 2022 23:11:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c6c74c3589f19f8f7ec7b7183735a478fe4982b8fc99cf52c9b00eb6e28ae`  
		Last Modified: Fri, 29 Apr 2022 23:11:58 GMT  
		Size: 6.9 KB (6919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d42ad0290cbf4cb4fabb2417f1d23f5171f25427693b1061a150ce7d0ce1acb`  
		Last Modified: Fri, 29 Apr 2022 23:12:11 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e9caef6820bca8f174b94f9d89f513378fbb6107eb8d47ebf6b709a7455b6f`  
		Last Modified: Fri, 29 Apr 2022 23:11:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:d77e581d514ec36f7fd60696402ee3fb28221ab181c77113e6961cb60ee03035
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234016890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a497448bf878ff716bff19ddaf76fe1e0d8949ca6c1d09bb2759b8159e6d9f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:00 GMT
ADD file:2d91cfcbab5facf9c027064efd477cfde81eca0c1a62c6611ac694bafb94d817 in / 
# Fri, 29 Apr 2022 23:22:04 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:42:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:44:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:44:19 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:44:24 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:44:34 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:44:38 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:45:52 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:45:54 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:45:56 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:45:58 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:46:00 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 29 Apr 2022 23:46:01 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 29 Apr 2022 23:46:03 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 29 Apr 2022 23:46:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:46:06 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:46:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:46:15 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:46:20 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:46:22 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 29 Apr 2022 23:46:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:46:40 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:46:46 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:46:49 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:46:50 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:46:53 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:46:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c70b79613e1f9e69f0d6473fa0b3f8b10d376e24350617c381ed64978f4bae97`  
		Last Modified: Fri, 29 Apr 2022 23:24:58 GMT  
		Size: 30.4 MB (30443183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd4b165cd40db0cccb113fe5db2529c203d2f8e6233e4856d5ab51822a7ca78`  
		Last Modified: Fri, 29 Apr 2022 23:51:28 GMT  
		Size: 86.6 MB (86599389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010b459db0081f915d9a7c41392066a7781dd27712e4f04841025302a64561c3`  
		Last Modified: Fri, 29 Apr 2022 23:51:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accb2c91951f1916d579ffdb3901dc305589121f573800fdd2ace816c64045b2`  
		Last Modified: Fri, 29 Apr 2022 23:51:14 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9abf09cd0519cd230adc8755ad47a39fb9f3355ea62a945c9d67e1ba28394`  
		Last Modified: Fri, 29 Apr 2022 23:51:11 GMT  
		Size: 548.1 KB (548056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504f615b88c769994f6c1f59eeb36011a7ec531fd75d1e82fd98a8fd2a578a0c`  
		Last Modified: Fri, 29 Apr 2022 23:51:42 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2c560155d0f72409306405f691e4eacf847b9e8fa8f81d31aa56a1abf54600`  
		Last Modified: Fri, 29 Apr 2022 23:51:42 GMT  
		Size: 6.9 KB (6949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b02ffdd196eb892ec1377617408f5950029359e4d48de8d0604f2c07f4bf9d6`  
		Last Modified: Fri, 29 Apr 2022 23:51:51 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68692de04f0e13b0d4dde26186c9e90f987ea69968f718392fc52eb8209c23a`  
		Last Modified: Fri, 29 Apr 2022 23:51:42 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:9487b6af1d504a058af15e4d8d8a2c7d82ca9ac316513c401f5e2baac0fd5661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:4d8fcc5650559a9f84cc25840eb3bcd39ee2d3a5f18efaa451ec77bdada60f77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235144210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26c807accd1744aa32c8ee7e69a76d1e0b6f9af4df7b645e7a4868dc5ddec64`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:38:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:40:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:40:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:40:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:40:51 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:40:52 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:40:53 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:40:53 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:40:53 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:41:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:41:03 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:41:04 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:41:04 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:41:04 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:41:05 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51001e033728e38556e8f467791283bb5c15aa83ca21b2876d835fc8b485b67d`  
		Last Modified: Fri, 29 Apr 2022 23:42:21 GMT  
		Size: 93.7 MB (93695487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02be2d5c1146b536e95a5fa093a866dd8c9726783bce7b4b8330106f912bb33`  
		Last Modified: Fri, 29 Apr 2022 23:42:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3771da1ca1f8f634b07a12a05fa426e901c4d15632a5c18a200312e67be4954`  
		Last Modified: Fri, 29 Apr 2022 23:42:08 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49abe543ff4d480784016ade446923e24f6b3fecdd317e636a0ea72c62af441d`  
		Last Modified: Fri, 29 Apr 2022 23:42:07 GMT  
		Size: 1.0 MB (1004487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffad7a2566a8872093031b5400f6a574518065c58240406a3f12338fa6742668`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5e254a2196f04e94e4fc0ab7200a1ebaabf4d634d023ae8b1c3413a4f77c88`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fbdaebe08cf21cb06442973376b8186478b44ff82b74d2b2d9444ef7213cce`  
		Last Modified: Fri, 29 Apr 2022 23:42:12 GMT  
		Size: 113.7 MB (113727931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3b8e00805dfe5cf5b2c7e68ff542a708783f33341a78d4d37d9a226c635d40`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:3af661a7c52a5409780d209fda26d58e4ebbb2661ef62af959de78624be939cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224212249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9b29fe51e5a35155174a7683a95671f76ae8d08cebf947de9094428653b198`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:08:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:10:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:10:15 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:10:16 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:10:19 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:10:20 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:10:21 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:10:22 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:10:23 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:10:24 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:10:25 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:10:26 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:10:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:10:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:10:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:10:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:10:31 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:10:33 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:10:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:10:41 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:10:42 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:10:44 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:10:44 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:10:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7c6b58b91fda219f6d212772d707e631638c7dcd39b2e8d8b54e89af4da048`  
		Last Modified: Fri, 29 Apr 2022 23:12:40 GMT  
		Size: 85.8 MB (85811865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1679eb7667cf32f2ef9fbcfb9d4fd30fc2a8660d36933951b257350fcd875b0`  
		Last Modified: Fri, 29 Apr 2022 23:12:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109119428bd0ae9f33c8dbfd2125b9fad99099887b120b39ac67d8b2e90a20f1`  
		Last Modified: Fri, 29 Apr 2022 23:12:28 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ada91d0d9d714658cdff68bc3f4584da1e53b3477155e8ef2a948f481a3b76`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 930.4 KB (930363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705b22c08ed07680e735d82301760ccedeef6faeb15f3bbd170d6844d1f0e2e7`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e2c6dd4d0fccd5cb4574b629e5baee3e955c627a05d9fdbe0506383528a36c`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550d463259f5921736dd8eca23c2b5e26d50f46184dca4c3b2aa718aad181fc`  
		Last Modified: Fri, 29 Apr 2022 23:12:39 GMT  
		Size: 113.7 MB (113727847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa65a595d61be5491036f079b45671789dc856512a21ed4abe8606dfe6e1dd2c`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:35f088b553608215a1a04aa7d6d7925c7be125a2e2a3fec269e0893bc26c3cac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231682648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a29796054a97d455674bb2af1196bc1adfb792c01dbca0707050c660352bbc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:00 GMT
ADD file:2d91cfcbab5facf9c027064efd477cfde81eca0c1a62c6611ac694bafb94d817 in / 
# Fri, 29 Apr 2022 23:22:04 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:42:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:48:57 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:49:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:49:11 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:49:14 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:49:15 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:49:17 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:49:19 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:49:20 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:49:22 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:49:24 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:49:26 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:49:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:49:30 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:49:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:49:37 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:49:38 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:49:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:49:57 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:50:02 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:50:04 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:50:07 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:50:12 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c70b79613e1f9e69f0d6473fa0b3f8b10d376e24350617c381ed64978f4bae97`  
		Last Modified: Fri, 29 Apr 2022 23:24:58 GMT  
		Size: 30.4 MB (30443183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e50182c712bf33fc0f438a5d9eaae53173c02649534111b34e975ac61920959`  
		Last Modified: Fri, 29 Apr 2022 23:52:25 GMT  
		Size: 86.6 MB (86598850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77fbfa22a6f28c7616546baab7de384e0b1f78830bd593ac9e5c1679bd7625`  
		Last Modified: Fri, 29 Apr 2022 23:52:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51ad52b26ccf11895c2d3b13d30f6c4eec421717cd41a0c5f9f13c8a09d7c9d`  
		Last Modified: Fri, 29 Apr 2022 23:52:10 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b39eabf154744057585bc5be42e82311fc0664e2c53a10542cab6f46fc3403c`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 905.5 KB (905481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e8d78f86ce6031586a13f2efde16157feead30febb422d6e89e8b447b354b0`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd479022cf1dd0e30016f8269cb9f91ce243e80e9676f33c6f6f422478e73946`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1445875b590ad220f338f4dab7bd07c9b7b87bbc8ebb1000f3f94863985c87`  
		Last Modified: Fri, 29 Apr 2022 23:52:18 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aaadb5d32249a3bff4d26a39a584b5bf9f3aa3755bfd724decf06f3c4918`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:9487b6af1d504a058af15e4d8d8a2c7d82ca9ac316513c401f5e2baac0fd5661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:4d8fcc5650559a9f84cc25840eb3bcd39ee2d3a5f18efaa451ec77bdada60f77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235144210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26c807accd1744aa32c8ee7e69a76d1e0b6f9af4df7b645e7a4868dc5ddec64`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:38:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:40:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:40:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:40:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:40:51 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:40:52 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:40:53 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:40:53 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:40:53 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:41:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:41:03 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:41:04 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:41:04 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:41:04 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:41:05 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51001e033728e38556e8f467791283bb5c15aa83ca21b2876d835fc8b485b67d`  
		Last Modified: Fri, 29 Apr 2022 23:42:21 GMT  
		Size: 93.7 MB (93695487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02be2d5c1146b536e95a5fa093a866dd8c9726783bce7b4b8330106f912bb33`  
		Last Modified: Fri, 29 Apr 2022 23:42:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3771da1ca1f8f634b07a12a05fa426e901c4d15632a5c18a200312e67be4954`  
		Last Modified: Fri, 29 Apr 2022 23:42:08 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49abe543ff4d480784016ade446923e24f6b3fecdd317e636a0ea72c62af441d`  
		Last Modified: Fri, 29 Apr 2022 23:42:07 GMT  
		Size: 1.0 MB (1004487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffad7a2566a8872093031b5400f6a574518065c58240406a3f12338fa6742668`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5e254a2196f04e94e4fc0ab7200a1ebaabf4d634d023ae8b1c3413a4f77c88`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fbdaebe08cf21cb06442973376b8186478b44ff82b74d2b2d9444ef7213cce`  
		Last Modified: Fri, 29 Apr 2022 23:42:12 GMT  
		Size: 113.7 MB (113727931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3b8e00805dfe5cf5b2c7e68ff542a708783f33341a78d4d37d9a226c635d40`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:3af661a7c52a5409780d209fda26d58e4ebbb2661ef62af959de78624be939cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224212249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9b29fe51e5a35155174a7683a95671f76ae8d08cebf947de9094428653b198`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:08:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:10:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:10:15 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:10:16 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:10:19 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:10:20 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:10:21 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:10:22 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:10:23 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:10:24 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:10:25 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:10:26 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:10:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:10:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:10:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:10:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:10:31 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:10:33 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:10:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:10:41 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:10:42 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:10:44 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:10:44 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:10:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7c6b58b91fda219f6d212772d707e631638c7dcd39b2e8d8b54e89af4da048`  
		Last Modified: Fri, 29 Apr 2022 23:12:40 GMT  
		Size: 85.8 MB (85811865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1679eb7667cf32f2ef9fbcfb9d4fd30fc2a8660d36933951b257350fcd875b0`  
		Last Modified: Fri, 29 Apr 2022 23:12:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109119428bd0ae9f33c8dbfd2125b9fad99099887b120b39ac67d8b2e90a20f1`  
		Last Modified: Fri, 29 Apr 2022 23:12:28 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ada91d0d9d714658cdff68bc3f4584da1e53b3477155e8ef2a948f481a3b76`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 930.4 KB (930363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705b22c08ed07680e735d82301760ccedeef6faeb15f3bbd170d6844d1f0e2e7`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e2c6dd4d0fccd5cb4574b629e5baee3e955c627a05d9fdbe0506383528a36c`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550d463259f5921736dd8eca23c2b5e26d50f46184dca4c3b2aa718aad181fc`  
		Last Modified: Fri, 29 Apr 2022 23:12:39 GMT  
		Size: 113.7 MB (113727847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa65a595d61be5491036f079b45671789dc856512a21ed4abe8606dfe6e1dd2c`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:35f088b553608215a1a04aa7d6d7925c7be125a2e2a3fec269e0893bc26c3cac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231682648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a29796054a97d455674bb2af1196bc1adfb792c01dbca0707050c660352bbc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:00 GMT
ADD file:2d91cfcbab5facf9c027064efd477cfde81eca0c1a62c6611ac694bafb94d817 in / 
# Fri, 29 Apr 2022 23:22:04 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:42:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:48:57 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:49:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:49:11 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:49:14 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:49:15 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:49:17 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:49:19 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:49:20 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:49:22 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:49:24 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:49:26 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:49:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:49:30 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:49:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:49:37 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:49:38 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:49:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:49:57 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:50:02 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:50:04 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:50:07 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:50:12 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c70b79613e1f9e69f0d6473fa0b3f8b10d376e24350617c381ed64978f4bae97`  
		Last Modified: Fri, 29 Apr 2022 23:24:58 GMT  
		Size: 30.4 MB (30443183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e50182c712bf33fc0f438a5d9eaae53173c02649534111b34e975ac61920959`  
		Last Modified: Fri, 29 Apr 2022 23:52:25 GMT  
		Size: 86.6 MB (86598850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77fbfa22a6f28c7616546baab7de384e0b1f78830bd593ac9e5c1679bd7625`  
		Last Modified: Fri, 29 Apr 2022 23:52:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51ad52b26ccf11895c2d3b13d30f6c4eec421717cd41a0c5f9f13c8a09d7c9d`  
		Last Modified: Fri, 29 Apr 2022 23:52:10 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b39eabf154744057585bc5be42e82311fc0664e2c53a10542cab6f46fc3403c`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 905.5 KB (905481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e8d78f86ce6031586a13f2efde16157feead30febb422d6e89e8b447b354b0`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd479022cf1dd0e30016f8269cb9f91ce243e80e9676f33c6f6f422478e73946`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1445875b590ad220f338f4dab7bd07c9b7b87bbc8ebb1000f3f94863985c87`  
		Last Modified: Fri, 29 Apr 2022 23:52:18 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aaadb5d32249a3bff4d26a39a584b5bf9f3aa3755bfd724decf06f3c4918`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
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
$ docker pull bonita@sha256:934a6bdac07170343188fb53428cdc3dcf8910fd61741ac4f3bce42d8ecf8341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:985a20f667de7fb548f9ea3aa222bf7ecac8b11d64f298de231c7dbdb04e39a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234341364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abc08105c23a33d9c72c07bb6314f13dccb2fc91acc6451e8f0969f176cc065`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:38:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:39:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:39:49 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:39:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:39:52 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:39:52 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:39:52 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:39:53 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:39:53 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:39:53 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 29 Apr 2022 23:39:53 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 29 Apr 2022 23:39:53 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:39:53 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:39:53 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:39:54 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:39:54 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:39:54 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 29 Apr 2022 23:39:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:40:01 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:40:02 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:40:02 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:40:02 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:40:02 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:40:02 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca3aae8c772c52e56d308d7a94719a1f5837917f6e87a216400d4a5445ebdf`  
		Last Modified: Fri, 29 Apr 2022 23:41:39 GMT  
		Size: 93.7 MB (93695508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1643a51cc7a8bfcca6148bcf66667508761251947a4fdef917b047ce60fe5570`  
		Last Modified: Fri, 29 Apr 2022 23:41:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2402a2b3c43454a2bad134131e419b0e8b9a83eb7aa0a0d3e87b613995daf641`  
		Last Modified: Fri, 29 Apr 2022 23:41:27 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05300e43655cf3d031bbecd3cf1a14416512ddc88b712a229c2ad91d3f0803c1`  
		Last Modified: Fri, 29 Apr 2022 23:41:26 GMT  
		Size: 578.1 KB (578132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fddfbce9af12487b436efe750ec1463559f0178f739c7180c8659568421c3c`  
		Last Modified: Fri, 29 Apr 2022 23:41:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aee2fc8f945f262ca9e120af0d95fedb6a9696c20c34868940441aee023c707`  
		Last Modified: Fri, 29 Apr 2022 23:41:25 GMT  
		Size: 6.9 KB (6893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55612cb996be3e2d47072438c88f447fb60eea843adcf6114426727fefa8a809`  
		Last Modified: Fri, 29 Apr 2022 23:41:29 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3d8f48ef0ae5db7fe7b432f73227ef18550b60d5e0994c166c9536842ecaba`  
		Last Modified: Fri, 29 Apr 2022 23:41:25 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4fe28eec154021f12b3062100148baa16ca1ce08c3358bbb82c927fa4184526e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223453248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660ee76b0ff98e1f85842787ba776762ef00c6ea90585a9ffe4bee75c6abbc7d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:08:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:08:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:08:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:08:32 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:08:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:08:42 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:08:43 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:08:44 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:08:45 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:08:46 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 29 Apr 2022 23:08:47 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 29 Apr 2022 23:08:48 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:08:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:08:50 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:08:51 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:08:52 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:08:54 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 29 Apr 2022 23:08:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:08:59 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:09:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:09:01 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:09:03 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:09:03 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:09:04 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f12337ad9a174c4f77881b8dbcb65f62a7fc10574a432c7118b59ad112dbd2`  
		Last Modified: Fri, 29 Apr 2022 23:11:40 GMT  
		Size: 85.8 MB (85811732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91166d3caec0b5cacb26aae01bc16d5d7782a114b68ab5e09a68b18a90c3dfc6`  
		Last Modified: Fri, 29 Apr 2022 23:11:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b44ff2f6d502d14b27d552c3874024acd360c54e4d65f15f24de7479e27ec2`  
		Last Modified: Fri, 29 Apr 2022 23:11:28 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d38292d92a3d092cb6db160054239872b77c787f359641e8906be79fbf199`  
		Last Modified: Fri, 29 Apr 2022 23:11:26 GMT  
		Size: 548.0 KB (547952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cea3833e8efab22866078f14739ca3873a822bc81f19a259fe203ccdad96557`  
		Last Modified: Fri, 29 Apr 2022 23:11:26 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb2b4c51f1eb8efdb4245128d6be96befd4582a5bf5b33d09eac090267b79c7`  
		Last Modified: Fri, 29 Apr 2022 23:11:26 GMT  
		Size: 6.9 KB (6865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d342390946d39de98ef08ebe70120e8e7ef2db224f2674a6bfa247151c2977`  
		Last Modified: Fri, 29 Apr 2022 23:11:36 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f9c201078b013ec75d1e8184a23c035cc53fad03dca59c934278425a22dcdf`  
		Last Modified: Fri, 29 Apr 2022 23:11:26 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:f10b3a2fb3efb9c64896c30dfae7a4bf285d25479e8ba14926271a44b255df45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230949257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9704995f1eef869ecfc92f0d47743413313750abb71b86b6ec2c250dacc24e4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:00 GMT
ADD file:2d91cfcbab5facf9c027064efd477cfde81eca0c1a62c6611ac694bafb94d817 in / 
# Fri, 29 Apr 2022 23:22:04 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:42:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:44:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:44:19 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:44:24 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:44:34 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:44:38 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:44:40 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:44:42 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:44:45 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:44:47 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 29 Apr 2022 23:44:49 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 29 Apr 2022 23:44:51 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:44:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:44:54 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:44:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:45:01 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:45:02 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 29 Apr 2022 23:45:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:45:17 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:45:25 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:45:30 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:45:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:45:33 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:45:35 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c70b79613e1f9e69f0d6473fa0b3f8b10d376e24350617c381ed64978f4bae97`  
		Last Modified: Fri, 29 Apr 2022 23:24:58 GMT  
		Size: 30.4 MB (30443183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd4b165cd40db0cccb113fe5db2529c203d2f8e6233e4856d5ab51822a7ca78`  
		Last Modified: Fri, 29 Apr 2022 23:51:28 GMT  
		Size: 86.6 MB (86599389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010b459db0081f915d9a7c41392066a7781dd27712e4f04841025302a64561c3`  
		Last Modified: Fri, 29 Apr 2022 23:51:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accb2c91951f1916d579ffdb3901dc305589121f573800fdd2ace816c64045b2`  
		Last Modified: Fri, 29 Apr 2022 23:51:14 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9abf09cd0519cd230adc8755ad47a39fb9f3355ea62a945c9d67e1ba28394`  
		Last Modified: Fri, 29 Apr 2022 23:51:11 GMT  
		Size: 548.1 KB (548056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f1d82e7ee6c661cf6928369eef0e3c943fab4574f522768cd375fc1e48a1f`  
		Last Modified: Fri, 29 Apr 2022 23:51:11 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81430b13ec8cfd26c8ef3b0486d7ce1dbd4dbdac24e8044b35550d55b948c6c4`  
		Last Modified: Fri, 29 Apr 2022 23:51:11 GMT  
		Size: 6.9 KB (6896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ecb0e3801f7b2b643bc25343d670001cafa46656835f48ba19968e8d884753`  
		Last Modified: Fri, 29 Apr 2022 23:51:19 GMT  
		Size: 113.3 MB (113347832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d0ba15b78752c65d343acc09a8bb083b039d1fb66ab67ba9e12a8390f1a1a`  
		Last Modified: Fri, 29 Apr 2022 23:51:10 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:934a6bdac07170343188fb53428cdc3dcf8910fd61741ac4f3bce42d8ecf8341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:985a20f667de7fb548f9ea3aa222bf7ecac8b11d64f298de231c7dbdb04e39a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234341364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abc08105c23a33d9c72c07bb6314f13dccb2fc91acc6451e8f0969f176cc065`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:38:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:39:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:39:49 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:39:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:39:52 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:39:52 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:39:52 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:39:53 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:39:53 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:39:53 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 29 Apr 2022 23:39:53 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 29 Apr 2022 23:39:53 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:39:53 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:39:53 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:39:54 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:39:54 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:39:54 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 29 Apr 2022 23:39:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:40:01 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:40:02 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:40:02 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:40:02 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:40:02 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:40:02 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca3aae8c772c52e56d308d7a94719a1f5837917f6e87a216400d4a5445ebdf`  
		Last Modified: Fri, 29 Apr 2022 23:41:39 GMT  
		Size: 93.7 MB (93695508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1643a51cc7a8bfcca6148bcf66667508761251947a4fdef917b047ce60fe5570`  
		Last Modified: Fri, 29 Apr 2022 23:41:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2402a2b3c43454a2bad134131e419b0e8b9a83eb7aa0a0d3e87b613995daf641`  
		Last Modified: Fri, 29 Apr 2022 23:41:27 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05300e43655cf3d031bbecd3cf1a14416512ddc88b712a229c2ad91d3f0803c1`  
		Last Modified: Fri, 29 Apr 2022 23:41:26 GMT  
		Size: 578.1 KB (578132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fddfbce9af12487b436efe750ec1463559f0178f739c7180c8659568421c3c`  
		Last Modified: Fri, 29 Apr 2022 23:41:24 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aee2fc8f945f262ca9e120af0d95fedb6a9696c20c34868940441aee023c707`  
		Last Modified: Fri, 29 Apr 2022 23:41:25 GMT  
		Size: 6.9 KB (6893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55612cb996be3e2d47072438c88f447fb60eea843adcf6114426727fefa8a809`  
		Last Modified: Fri, 29 Apr 2022 23:41:29 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3d8f48ef0ae5db7fe7b432f73227ef18550b60d5e0994c166c9536842ecaba`  
		Last Modified: Fri, 29 Apr 2022 23:41:25 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4fe28eec154021f12b3062100148baa16ca1ce08c3358bbb82c927fa4184526e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223453248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660ee76b0ff98e1f85842787ba776762ef00c6ea90585a9ffe4bee75c6abbc7d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:08:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:08:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:08:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:08:32 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:08:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:08:42 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:08:43 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:08:44 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:08:45 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:08:46 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 29 Apr 2022 23:08:47 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 29 Apr 2022 23:08:48 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:08:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:08:50 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:08:51 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:08:52 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:08:54 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 29 Apr 2022 23:08:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:08:59 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:09:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:09:01 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:09:03 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:09:03 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:09:04 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f12337ad9a174c4f77881b8dbcb65f62a7fc10574a432c7118b59ad112dbd2`  
		Last Modified: Fri, 29 Apr 2022 23:11:40 GMT  
		Size: 85.8 MB (85811732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91166d3caec0b5cacb26aae01bc16d5d7782a114b68ab5e09a68b18a90c3dfc6`  
		Last Modified: Fri, 29 Apr 2022 23:11:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b44ff2f6d502d14b27d552c3874024acd360c54e4d65f15f24de7479e27ec2`  
		Last Modified: Fri, 29 Apr 2022 23:11:28 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d38292d92a3d092cb6db160054239872b77c787f359641e8906be79fbf199`  
		Last Modified: Fri, 29 Apr 2022 23:11:26 GMT  
		Size: 548.0 KB (547952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cea3833e8efab22866078f14739ca3873a822bc81f19a259fe203ccdad96557`  
		Last Modified: Fri, 29 Apr 2022 23:11:26 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb2b4c51f1eb8efdb4245128d6be96befd4582a5bf5b33d09eac090267b79c7`  
		Last Modified: Fri, 29 Apr 2022 23:11:26 GMT  
		Size: 6.9 KB (6865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d342390946d39de98ef08ebe70120e8e7ef2db224f2674a6bfa247151c2977`  
		Last Modified: Fri, 29 Apr 2022 23:11:36 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f9c201078b013ec75d1e8184a23c035cc53fad03dca59c934278425a22dcdf`  
		Last Modified: Fri, 29 Apr 2022 23:11:26 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:f10b3a2fb3efb9c64896c30dfae7a4bf285d25479e8ba14926271a44b255df45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230949257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9704995f1eef869ecfc92f0d47743413313750abb71b86b6ec2c250dacc24e4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:00 GMT
ADD file:2d91cfcbab5facf9c027064efd477cfde81eca0c1a62c6611ac694bafb94d817 in / 
# Fri, 29 Apr 2022 23:22:04 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:42:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:44:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:44:19 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:44:24 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:44:34 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:44:38 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:44:40 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:44:42 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:44:45 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:44:47 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 29 Apr 2022 23:44:49 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 29 Apr 2022 23:44:51 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:44:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:44:54 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 29 Apr 2022 23:44:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:45:01 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:45:02 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 29 Apr 2022 23:45:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:45:17 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:45:25 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:45:30 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:45:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:45:33 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:45:35 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c70b79613e1f9e69f0d6473fa0b3f8b10d376e24350617c381ed64978f4bae97`  
		Last Modified: Fri, 29 Apr 2022 23:24:58 GMT  
		Size: 30.4 MB (30443183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd4b165cd40db0cccb113fe5db2529c203d2f8e6233e4856d5ab51822a7ca78`  
		Last Modified: Fri, 29 Apr 2022 23:51:28 GMT  
		Size: 86.6 MB (86599389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010b459db0081f915d9a7c41392066a7781dd27712e4f04841025302a64561c3`  
		Last Modified: Fri, 29 Apr 2022 23:51:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accb2c91951f1916d579ffdb3901dc305589121f573800fdd2ace816c64045b2`  
		Last Modified: Fri, 29 Apr 2022 23:51:14 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9abf09cd0519cd230adc8755ad47a39fb9f3355ea62a945c9d67e1ba28394`  
		Last Modified: Fri, 29 Apr 2022 23:51:11 GMT  
		Size: 548.1 KB (548056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f1d82e7ee6c661cf6928369eef0e3c943fab4574f522768cd375fc1e48a1f`  
		Last Modified: Fri, 29 Apr 2022 23:51:11 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81430b13ec8cfd26c8ef3b0486d7ce1dbd4dbdac24e8044b35550d55b948c6c4`  
		Last Modified: Fri, 29 Apr 2022 23:51:11 GMT  
		Size: 6.9 KB (6896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ecb0e3801f7b2b643bc25343d670001cafa46656835f48ba19968e8d884753`  
		Last Modified: Fri, 29 Apr 2022 23:51:19 GMT  
		Size: 113.3 MB (113347832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d0ba15b78752c65d343acc09a8bb083b039d1fb66ab67ba9e12a8390f1a1a`  
		Last Modified: Fri, 29 Apr 2022 23:51:10 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:eadcfc347646575bfc80103ede0823cafaebf0cce1ccc63889fe392c3eba1334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:faa5c9ed7d34ccec525035d081de48feca3c8e0b75ea802b7dfebeee9dc0a223
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237408988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207ab007fc31f10d70929a6658dacf1e9f9b761573cc6e383ee33f375d0c2b49`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:38:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:39:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:39:49 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:39:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:39:52 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:39:52 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:40:11 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 29 Apr 2022 23:40:12 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:40:12 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:40:13 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:40:13 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 29 Apr 2022 23:40:21 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:40:22 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:40:23 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:40:23 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:40:24 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:40:24 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:40:24 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca3aae8c772c52e56d308d7a94719a1f5837917f6e87a216400d4a5445ebdf`  
		Last Modified: Fri, 29 Apr 2022 23:41:39 GMT  
		Size: 93.7 MB (93695508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1643a51cc7a8bfcca6148bcf66667508761251947a4fdef917b047ce60fe5570`  
		Last Modified: Fri, 29 Apr 2022 23:41:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2402a2b3c43454a2bad134131e419b0e8b9a83eb7aa0a0d3e87b613995daf641`  
		Last Modified: Fri, 29 Apr 2022 23:41:27 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05300e43655cf3d031bbecd3cf1a14416512ddc88b712a229c2ad91d3f0803c1`  
		Last Modified: Fri, 29 Apr 2022 23:41:26 GMT  
		Size: 578.1 KB (578132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db44dfe88160e6c127c511e7fac5edee94a42b93554ef13ac2c88af9703b318f`  
		Last Modified: Fri, 29 Apr 2022 23:41:49 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7390092e3be5c3e2b3ed82a087431e69a65a0bbb8a42b1b01be95faa95e643`  
		Last Modified: Fri, 29 Apr 2022 23:41:49 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f4fb48fb3f279efa4dc8e52c45283f7e73ebbf61233fca30a29cb02e1378bd`  
		Last Modified: Fri, 29 Apr 2022 23:41:54 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def6e6b22eec7d322588e14e73ebd9229f5c2a6d3f4fef1b9211a1d00798f118`  
		Last Modified: Fri, 29 Apr 2022 23:41:49 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5551862c7660da4af0f7cc9c9a9e5edcec09345a006e1498b5532fbf6d8a3eed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226520879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a11c5b28dad948c4bdead527a2cea3128803d8a4fe7125586fe0f6cd993c282`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:08:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:08:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:08:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:08:32 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:08:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:08:42 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:09:19 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:09:20 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:09:21 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:09:22 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:09:23 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 29 Apr 2022 23:09:24 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 29 Apr 2022 23:09:25 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 29 Apr 2022 23:09:26 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:09:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:09:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:09:29 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:09:30 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:09:32 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 29 Apr 2022 23:09:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:09:38 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:09:40 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:09:40 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:09:42 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:09:42 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:09:43 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f12337ad9a174c4f77881b8dbcb65f62a7fc10574a432c7118b59ad112dbd2`  
		Last Modified: Fri, 29 Apr 2022 23:11:40 GMT  
		Size: 85.8 MB (85811732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91166d3caec0b5cacb26aae01bc16d5d7782a114b68ab5e09a68b18a90c3dfc6`  
		Last Modified: Fri, 29 Apr 2022 23:11:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b44ff2f6d502d14b27d552c3874024acd360c54e4d65f15f24de7479e27ec2`  
		Last Modified: Fri, 29 Apr 2022 23:11:28 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d38292d92a3d092cb6db160054239872b77c787f359641e8906be79fbf199`  
		Last Modified: Fri, 29 Apr 2022 23:11:26 GMT  
		Size: 548.0 KB (547952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4560861bc9d90d917021f62f13ca94caa3b3788cb23417b1747db412c6ac3`  
		Last Modified: Fri, 29 Apr 2022 23:11:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c6c74c3589f19f8f7ec7b7183735a478fe4982b8fc99cf52c9b00eb6e28ae`  
		Last Modified: Fri, 29 Apr 2022 23:11:58 GMT  
		Size: 6.9 KB (6919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d42ad0290cbf4cb4fabb2417f1d23f5171f25427693b1061a150ce7d0ce1acb`  
		Last Modified: Fri, 29 Apr 2022 23:12:11 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e9caef6820bca8f174b94f9d89f513378fbb6107eb8d47ebf6b709a7455b6f`  
		Last Modified: Fri, 29 Apr 2022 23:11:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:d77e581d514ec36f7fd60696402ee3fb28221ab181c77113e6961cb60ee03035
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234016890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a497448bf878ff716bff19ddaf76fe1e0d8949ca6c1d09bb2759b8159e6d9f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:00 GMT
ADD file:2d91cfcbab5facf9c027064efd477cfde81eca0c1a62c6611ac694bafb94d817 in / 
# Fri, 29 Apr 2022 23:22:04 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:42:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:44:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:44:19 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:44:24 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:44:34 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:44:38 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:45:52 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:45:54 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:45:56 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:45:58 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:46:00 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 29 Apr 2022 23:46:01 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 29 Apr 2022 23:46:03 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 29 Apr 2022 23:46:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:46:06 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:46:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:46:15 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:46:20 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:46:22 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 29 Apr 2022 23:46:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:46:40 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:46:46 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:46:49 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:46:50 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:46:53 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:46:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c70b79613e1f9e69f0d6473fa0b3f8b10d376e24350617c381ed64978f4bae97`  
		Last Modified: Fri, 29 Apr 2022 23:24:58 GMT  
		Size: 30.4 MB (30443183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd4b165cd40db0cccb113fe5db2529c203d2f8e6233e4856d5ab51822a7ca78`  
		Last Modified: Fri, 29 Apr 2022 23:51:28 GMT  
		Size: 86.6 MB (86599389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010b459db0081f915d9a7c41392066a7781dd27712e4f04841025302a64561c3`  
		Last Modified: Fri, 29 Apr 2022 23:51:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accb2c91951f1916d579ffdb3901dc305589121f573800fdd2ace816c64045b2`  
		Last Modified: Fri, 29 Apr 2022 23:51:14 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9abf09cd0519cd230adc8755ad47a39fb9f3355ea62a945c9d67e1ba28394`  
		Last Modified: Fri, 29 Apr 2022 23:51:11 GMT  
		Size: 548.1 KB (548056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504f615b88c769994f6c1f59eeb36011a7ec531fd75d1e82fd98a8fd2a578a0c`  
		Last Modified: Fri, 29 Apr 2022 23:51:42 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2c560155d0f72409306405f691e4eacf847b9e8fa8f81d31aa56a1abf54600`  
		Last Modified: Fri, 29 Apr 2022 23:51:42 GMT  
		Size: 6.9 KB (6949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b02ffdd196eb892ec1377617408f5950029359e4d48de8d0604f2c07f4bf9d6`  
		Last Modified: Fri, 29 Apr 2022 23:51:51 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68692de04f0e13b0d4dde26186c9e90f987ea69968f718392fc52eb8209c23a`  
		Last Modified: Fri, 29 Apr 2022 23:51:42 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:eadcfc347646575bfc80103ede0823cafaebf0cce1ccc63889fe392c3eba1334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:faa5c9ed7d34ccec525035d081de48feca3c8e0b75ea802b7dfebeee9dc0a223
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237408988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207ab007fc31f10d70929a6658dacf1e9f9b761573cc6e383ee33f375d0c2b49`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:38:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:39:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:39:49 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:39:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:39:52 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:39:52 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:40:11 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:40:11 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 29 Apr 2022 23:40:12 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:40:12 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:40:12 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:40:13 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:40:13 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 29 Apr 2022 23:40:21 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:40:22 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:40:23 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:40:23 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:40:24 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:40:24 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:40:24 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ca3aae8c772c52e56d308d7a94719a1f5837917f6e87a216400d4a5445ebdf`  
		Last Modified: Fri, 29 Apr 2022 23:41:39 GMT  
		Size: 93.7 MB (93695508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1643a51cc7a8bfcca6148bcf66667508761251947a4fdef917b047ce60fe5570`  
		Last Modified: Fri, 29 Apr 2022 23:41:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2402a2b3c43454a2bad134131e419b0e8b9a83eb7aa0a0d3e87b613995daf641`  
		Last Modified: Fri, 29 Apr 2022 23:41:27 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05300e43655cf3d031bbecd3cf1a14416512ddc88b712a229c2ad91d3f0803c1`  
		Last Modified: Fri, 29 Apr 2022 23:41:26 GMT  
		Size: 578.1 KB (578132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db44dfe88160e6c127c511e7fac5edee94a42b93554ef13ac2c88af9703b318f`  
		Last Modified: Fri, 29 Apr 2022 23:41:49 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7390092e3be5c3e2b3ed82a087431e69a65a0bbb8a42b1b01be95faa95e643`  
		Last Modified: Fri, 29 Apr 2022 23:41:49 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f4fb48fb3f279efa4dc8e52c45283f7e73ebbf61233fca30a29cb02e1378bd`  
		Last Modified: Fri, 29 Apr 2022 23:41:54 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def6e6b22eec7d322588e14e73ebd9229f5c2a6d3f4fef1b9211a1d00798f118`  
		Last Modified: Fri, 29 Apr 2022 23:41:49 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5551862c7660da4af0f7cc9c9a9e5edcec09345a006e1498b5532fbf6d8a3eed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226520879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a11c5b28dad948c4bdead527a2cea3128803d8a4fe7125586fe0f6cd993c282`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:08:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:08:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:08:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:08:32 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:08:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:08:42 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:09:19 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:09:20 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:09:21 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:09:22 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:09:23 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 29 Apr 2022 23:09:24 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 29 Apr 2022 23:09:25 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 29 Apr 2022 23:09:26 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:09:27 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:09:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:09:29 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:09:30 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:09:32 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 29 Apr 2022 23:09:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:09:38 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:09:40 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:09:40 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:09:42 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:09:42 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:09:43 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f12337ad9a174c4f77881b8dbcb65f62a7fc10574a432c7118b59ad112dbd2`  
		Last Modified: Fri, 29 Apr 2022 23:11:40 GMT  
		Size: 85.8 MB (85811732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91166d3caec0b5cacb26aae01bc16d5d7782a114b68ab5e09a68b18a90c3dfc6`  
		Last Modified: Fri, 29 Apr 2022 23:11:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b44ff2f6d502d14b27d552c3874024acd360c54e4d65f15f24de7479e27ec2`  
		Last Modified: Fri, 29 Apr 2022 23:11:28 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d38292d92a3d092cb6db160054239872b77c787f359641e8906be79fbf199`  
		Last Modified: Fri, 29 Apr 2022 23:11:26 GMT  
		Size: 548.0 KB (547952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4560861bc9d90d917021f62f13ca94caa3b3788cb23417b1747db412c6ac3`  
		Last Modified: Fri, 29 Apr 2022 23:11:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c6c74c3589f19f8f7ec7b7183735a478fe4982b8fc99cf52c9b00eb6e28ae`  
		Last Modified: Fri, 29 Apr 2022 23:11:58 GMT  
		Size: 6.9 KB (6919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d42ad0290cbf4cb4fabb2417f1d23f5171f25427693b1061a150ce7d0ce1acb`  
		Last Modified: Fri, 29 Apr 2022 23:12:11 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e9caef6820bca8f174b94f9d89f513378fbb6107eb8d47ebf6b709a7455b6f`  
		Last Modified: Fri, 29 Apr 2022 23:11:58 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:d77e581d514ec36f7fd60696402ee3fb28221ab181c77113e6961cb60ee03035
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234016890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a497448bf878ff716bff19ddaf76fe1e0d8949ca6c1d09bb2759b8159e6d9f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:00 GMT
ADD file:2d91cfcbab5facf9c027064efd477cfde81eca0c1a62c6611ac694bafb94d817 in / 
# Fri, 29 Apr 2022 23:22:04 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:42:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:44:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:44:19 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:44:24 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:44:34 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:44:38 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:45:52 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:45:54 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:45:56 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:45:58 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:46:00 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 29 Apr 2022 23:46:01 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 29 Apr 2022 23:46:03 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 29 Apr 2022 23:46:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:46:06 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:46:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 29 Apr 2022 23:46:15 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 29 Apr 2022 23:46:20 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:46:22 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 29 Apr 2022 23:46:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 29 Apr 2022 23:46:40 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 29 Apr 2022 23:46:46 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 29 Apr 2022 23:46:49 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:46:50 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:46:53 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:46:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c70b79613e1f9e69f0d6473fa0b3f8b10d376e24350617c381ed64978f4bae97`  
		Last Modified: Fri, 29 Apr 2022 23:24:58 GMT  
		Size: 30.4 MB (30443183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd4b165cd40db0cccb113fe5db2529c203d2f8e6233e4856d5ab51822a7ca78`  
		Last Modified: Fri, 29 Apr 2022 23:51:28 GMT  
		Size: 86.6 MB (86599389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010b459db0081f915d9a7c41392066a7781dd27712e4f04841025302a64561c3`  
		Last Modified: Fri, 29 Apr 2022 23:51:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accb2c91951f1916d579ffdb3901dc305589121f573800fdd2ace816c64045b2`  
		Last Modified: Fri, 29 Apr 2022 23:51:14 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b9abf09cd0519cd230adc8755ad47a39fb9f3355ea62a945c9d67e1ba28394`  
		Last Modified: Fri, 29 Apr 2022 23:51:11 GMT  
		Size: 548.1 KB (548056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504f615b88c769994f6c1f59eeb36011a7ec531fd75d1e82fd98a8fd2a578a0c`  
		Last Modified: Fri, 29 Apr 2022 23:51:42 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2c560155d0f72409306405f691e4eacf847b9e8fa8f81d31aa56a1abf54600`  
		Last Modified: Fri, 29 Apr 2022 23:51:42 GMT  
		Size: 6.9 KB (6949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b02ffdd196eb892ec1377617408f5950029359e4d48de8d0604f2c07f4bf9d6`  
		Last Modified: Fri, 29 Apr 2022 23:51:51 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68692de04f0e13b0d4dde26186c9e90f987ea69968f718392fc52eb8209c23a`  
		Last Modified: Fri, 29 Apr 2022 23:51:42 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:9487b6af1d504a058af15e4d8d8a2c7d82ca9ac316513c401f5e2baac0fd5661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:4d8fcc5650559a9f84cc25840eb3bcd39ee2d3a5f18efaa451ec77bdada60f77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235144210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26c807accd1744aa32c8ee7e69a76d1e0b6f9af4df7b645e7a4868dc5ddec64`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:38:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:40:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:40:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:40:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:40:51 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:40:52 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:40:53 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:40:53 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:40:53 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:41:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:41:03 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:41:04 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:41:04 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:41:04 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:41:05 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51001e033728e38556e8f467791283bb5c15aa83ca21b2876d835fc8b485b67d`  
		Last Modified: Fri, 29 Apr 2022 23:42:21 GMT  
		Size: 93.7 MB (93695487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02be2d5c1146b536e95a5fa093a866dd8c9726783bce7b4b8330106f912bb33`  
		Last Modified: Fri, 29 Apr 2022 23:42:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3771da1ca1f8f634b07a12a05fa426e901c4d15632a5c18a200312e67be4954`  
		Last Modified: Fri, 29 Apr 2022 23:42:08 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49abe543ff4d480784016ade446923e24f6b3fecdd317e636a0ea72c62af441d`  
		Last Modified: Fri, 29 Apr 2022 23:42:07 GMT  
		Size: 1.0 MB (1004487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffad7a2566a8872093031b5400f6a574518065c58240406a3f12338fa6742668`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5e254a2196f04e94e4fc0ab7200a1ebaabf4d634d023ae8b1c3413a4f77c88`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fbdaebe08cf21cb06442973376b8186478b44ff82b74d2b2d9444ef7213cce`  
		Last Modified: Fri, 29 Apr 2022 23:42:12 GMT  
		Size: 113.7 MB (113727931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3b8e00805dfe5cf5b2c7e68ff542a708783f33341a78d4d37d9a226c635d40`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:3af661a7c52a5409780d209fda26d58e4ebbb2661ef62af959de78624be939cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224212249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9b29fe51e5a35155174a7683a95671f76ae8d08cebf947de9094428653b198`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:08:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:10:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:10:15 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:10:16 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:10:19 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:10:20 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:10:21 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:10:22 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:10:23 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:10:24 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:10:25 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:10:26 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:10:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:10:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:10:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:10:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:10:31 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:10:33 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:10:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:10:41 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:10:42 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:10:44 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:10:44 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:10:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7c6b58b91fda219f6d212772d707e631638c7dcd39b2e8d8b54e89af4da048`  
		Last Modified: Fri, 29 Apr 2022 23:12:40 GMT  
		Size: 85.8 MB (85811865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1679eb7667cf32f2ef9fbcfb9d4fd30fc2a8660d36933951b257350fcd875b0`  
		Last Modified: Fri, 29 Apr 2022 23:12:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109119428bd0ae9f33c8dbfd2125b9fad99099887b120b39ac67d8b2e90a20f1`  
		Last Modified: Fri, 29 Apr 2022 23:12:28 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ada91d0d9d714658cdff68bc3f4584da1e53b3477155e8ef2a948f481a3b76`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 930.4 KB (930363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705b22c08ed07680e735d82301760ccedeef6faeb15f3bbd170d6844d1f0e2e7`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e2c6dd4d0fccd5cb4574b629e5baee3e955c627a05d9fdbe0506383528a36c`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550d463259f5921736dd8eca23c2b5e26d50f46184dca4c3b2aa718aad181fc`  
		Last Modified: Fri, 29 Apr 2022 23:12:39 GMT  
		Size: 113.7 MB (113727847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa65a595d61be5491036f079b45671789dc856512a21ed4abe8606dfe6e1dd2c`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:35f088b553608215a1a04aa7d6d7925c7be125a2e2a3fec269e0893bc26c3cac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231682648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a29796054a97d455674bb2af1196bc1adfb792c01dbca0707050c660352bbc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:00 GMT
ADD file:2d91cfcbab5facf9c027064efd477cfde81eca0c1a62c6611ac694bafb94d817 in / 
# Fri, 29 Apr 2022 23:22:04 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:42:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:48:57 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:49:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:49:11 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:49:14 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:49:15 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:49:17 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:49:19 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:49:20 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:49:22 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:49:24 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:49:26 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:49:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:49:30 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:49:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:49:37 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:49:38 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:49:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:49:57 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:50:02 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:50:04 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:50:07 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:50:12 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c70b79613e1f9e69f0d6473fa0b3f8b10d376e24350617c381ed64978f4bae97`  
		Last Modified: Fri, 29 Apr 2022 23:24:58 GMT  
		Size: 30.4 MB (30443183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e50182c712bf33fc0f438a5d9eaae53173c02649534111b34e975ac61920959`  
		Last Modified: Fri, 29 Apr 2022 23:52:25 GMT  
		Size: 86.6 MB (86598850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77fbfa22a6f28c7616546baab7de384e0b1f78830bd593ac9e5c1679bd7625`  
		Last Modified: Fri, 29 Apr 2022 23:52:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51ad52b26ccf11895c2d3b13d30f6c4eec421717cd41a0c5f9f13c8a09d7c9d`  
		Last Modified: Fri, 29 Apr 2022 23:52:10 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b39eabf154744057585bc5be42e82311fc0664e2c53a10542cab6f46fc3403c`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 905.5 KB (905481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e8d78f86ce6031586a13f2efde16157feead30febb422d6e89e8b447b354b0`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd479022cf1dd0e30016f8269cb9f91ce243e80e9676f33c6f6f422478e73946`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1445875b590ad220f338f4dab7bd07c9b7b87bbc8ebb1000f3f94863985c87`  
		Last Modified: Fri, 29 Apr 2022 23:52:18 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aaadb5d32249a3bff4d26a39a584b5bf9f3aa3755bfd724decf06f3c4918`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:9487b6af1d504a058af15e4d8d8a2c7d82ca9ac316513c401f5e2baac0fd5661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:4d8fcc5650559a9f84cc25840eb3bcd39ee2d3a5f18efaa451ec77bdada60f77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235144210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26c807accd1744aa32c8ee7e69a76d1e0b6f9af4df7b645e7a4868dc5ddec64`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:51 GMT
ADD file:f657a56a18426c3a88d620a7024e7b91424d926e7b47faa6a97c2369c4c4a228 in / 
# Fri, 29 Apr 2022 23:20:51 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:38:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:40:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:40:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:40:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:40:51 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:40:52 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:40:52 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:40:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:40:53 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:40:53 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:40:53 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:41:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:41:03 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:41:04 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:41:04 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:41:04 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:41:05 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:40dd5be53814ae70b2898558673b7ea18d58bf7ab3433560b9ce3cb76d9ff0b1`  
		Last Modified: Fri, 29 Apr 2022 23:22:07 GMT  
		Size: 26.7 MB (26709108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51001e033728e38556e8f467791283bb5c15aa83ca21b2876d835fc8b485b67d`  
		Last Modified: Fri, 29 Apr 2022 23:42:21 GMT  
		Size: 93.7 MB (93695487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02be2d5c1146b536e95a5fa093a866dd8c9726783bce7b4b8330106f912bb33`  
		Last Modified: Fri, 29 Apr 2022 23:42:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3771da1ca1f8f634b07a12a05fa426e901c4d15632a5c18a200312e67be4954`  
		Last Modified: Fri, 29 Apr 2022 23:42:08 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49abe543ff4d480784016ade446923e24f6b3fecdd317e636a0ea72c62af441d`  
		Last Modified: Fri, 29 Apr 2022 23:42:07 GMT  
		Size: 1.0 MB (1004487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffad7a2566a8872093031b5400f6a574518065c58240406a3f12338fa6742668`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5e254a2196f04e94e4fc0ab7200a1ebaabf4d634d023ae8b1c3413a4f77c88`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fbdaebe08cf21cb06442973376b8186478b44ff82b74d2b2d9444ef7213cce`  
		Last Modified: Fri, 29 Apr 2022 23:42:12 GMT  
		Size: 113.7 MB (113727931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3b8e00805dfe5cf5b2c7e68ff542a708783f33341a78d4d37d9a226c635d40`  
		Last Modified: Fri, 29 Apr 2022 23:42:06 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:3af661a7c52a5409780d209fda26d58e4ebbb2661ef62af959de78624be939cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224212249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9b29fe51e5a35155174a7683a95671f76ae8d08cebf947de9094428653b198`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:26 GMT
ADD file:78300bda9e889eaa778190cac0e569ff379d5e533e86b086248476e6ba9b4b2d in / 
# Fri, 29 Apr 2022 22:49:26 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:08:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:10:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:10:15 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:10:16 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:10:19 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:10:20 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:10:21 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:10:22 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:10:23 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:10:24 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:10:25 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:10:26 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:10:27 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:10:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:10:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:10:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:10:31 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:10:33 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:10:41 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:10:41 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:10:42 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:10:44 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:10:44 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:10:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e196da37f904f62d236ea302bf13ba07711cc62b35774f86ecda18bcc9ed57c6`  
		Last Modified: Fri, 29 Apr 2022 22:51:14 GMT  
		Size: 23.7 MB (23735089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7c6b58b91fda219f6d212772d707e631638c7dcd39b2e8d8b54e89af4da048`  
		Last Modified: Fri, 29 Apr 2022 23:12:40 GMT  
		Size: 85.8 MB (85811865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1679eb7667cf32f2ef9fbcfb9d4fd30fc2a8660d36933951b257350fcd875b0`  
		Last Modified: Fri, 29 Apr 2022 23:12:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109119428bd0ae9f33c8dbfd2125b9fad99099887b120b39ac67d8b2e90a20f1`  
		Last Modified: Fri, 29 Apr 2022 23:12:28 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ada91d0d9d714658cdff68bc3f4584da1e53b3477155e8ef2a948f481a3b76`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 930.4 KB (930363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705b22c08ed07680e735d82301760ccedeef6faeb15f3bbd170d6844d1f0e2e7`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e2c6dd4d0fccd5cb4574b629e5baee3e955c627a05d9fdbe0506383528a36c`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550d463259f5921736dd8eca23c2b5e26d50f46184dca4c3b2aa718aad181fc`  
		Last Modified: Fri, 29 Apr 2022 23:12:39 GMT  
		Size: 113.7 MB (113727847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa65a595d61be5491036f079b45671789dc856512a21ed4abe8606dfe6e1dd2c`  
		Last Modified: Fri, 29 Apr 2022 23:12:26 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:35f088b553608215a1a04aa7d6d7925c7be125a2e2a3fec269e0893bc26c3cac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231682648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a29796054a97d455674bb2af1196bc1adfb792c01dbca0707050c660352bbc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:00 GMT
ADD file:2d91cfcbab5facf9c027064efd477cfde81eca0c1a62c6611ac694bafb94d817 in / 
# Fri, 29 Apr 2022 23:22:04 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:42:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 29 Apr 2022 23:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:48:57 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 29 Apr 2022 23:49:02 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 29 Apr 2022 23:49:11 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 29 Apr 2022 23:49:14 GMT
ARG BONITA_VERSION
# Fri, 29 Apr 2022 23:49:15 GMT
ARG BRANDING_VERSION
# Fri, 29 Apr 2022 23:49:17 GMT
ARG BONITA_SHA256
# Fri, 29 Apr 2022 23:49:19 GMT
ARG BASE_URL
# Fri, 29 Apr 2022 23:49:20 GMT
ARG BONITA_URL
# Fri, 29 Apr 2022 23:49:22 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 29 Apr 2022 23:49:24 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 29 Apr 2022 23:49:26 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 29 Apr 2022 23:49:28 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:49:30 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 29 Apr 2022 23:49:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 29 Apr 2022 23:49:37 GMT
RUN mkdir /opt/files
# Fri, 29 Apr 2022 23:49:38 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 29 Apr 2022 23:49:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 29 Apr 2022 23:49:57 GMT
ENV HTTP_API=false
# Fri, 29 Apr 2022 23:50:02 GMT
VOLUME [/opt/bonita]
# Fri, 29 Apr 2022 23:50:04 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 29 Apr 2022 23:50:07 GMT
EXPOSE 8080
# Fri, 29 Apr 2022 23:50:12 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c70b79613e1f9e69f0d6473fa0b3f8b10d376e24350617c381ed64978f4bae97`  
		Last Modified: Fri, 29 Apr 2022 23:24:58 GMT  
		Size: 30.4 MB (30443183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e50182c712bf33fc0f438a5d9eaae53173c02649534111b34e975ac61920959`  
		Last Modified: Fri, 29 Apr 2022 23:52:25 GMT  
		Size: 86.6 MB (86598850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77fbfa22a6f28c7616546baab7de384e0b1f78830bd593ac9e5c1679bd7625`  
		Last Modified: Fri, 29 Apr 2022 23:52:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51ad52b26ccf11895c2d3b13d30f6c4eec421717cd41a0c5f9f13c8a09d7c9d`  
		Last Modified: Fri, 29 Apr 2022 23:52:10 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b39eabf154744057585bc5be42e82311fc0664e2c53a10542cab6f46fc3403c`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 905.5 KB (905481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e8d78f86ce6031586a13f2efde16157feead30febb422d6e89e8b447b354b0`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd479022cf1dd0e30016f8269cb9f91ce243e80e9676f33c6f6f422478e73946`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1445875b590ad220f338f4dab7bd07c9b7b87bbc8ebb1000f3f94863985c87`  
		Last Modified: Fri, 29 Apr 2022 23:52:18 GMT  
		Size: 113.7 MB (113727930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aaadb5d32249a3bff4d26a39a584b5bf9f3aa3755bfd724decf06f3c4918`  
		Last Modified: Fri, 29 Apr 2022 23:52:08 GMT  
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
